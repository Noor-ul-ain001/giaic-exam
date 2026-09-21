# AI Prompting in 2026: A Complete Explanation
> Source: [agentfactory.panaversity.org/docs/ai-prompting-2026](https://agentfactory.panaversity.org/docs/ai-prompting-2026)  
> Simplified & explained — all 13 concepts, nothing skipped.

---

## Introduction: The Core Idea

Most people use AI like Google — type a question, skim the answer, move on. That works for trivia. It fails for real work.

**Power users do something different.** They treat AI like a smart new colleague on Day 1 — someone who is highly capable but knows nothing about you yet. So they give a proper **briefing**: files, context, constraints, and a clear ask. They expect options, not just one answer. They argue, iterate, and check the work.

**One fact runs under everything:**

> The AI model is **stateless** — it has no memory of its own between conversations. It can only see what is placed in front of it right now.

So almost every "advanced technique" is just one of two moves:
- **Get the right context IN**
- **Keep the wrong context OUT**

---

## What Changed Since 2022–2023

If you tried AI a few years ago and thought it was a toy, the tool you remember is not the tool that exists today. Here is what is different:

| What changed | How it changed |
|---|---|
| **Context window** | Grew ~1000x. Now holds hundreds of thousands of words — entire books. |
| **Reasoning** | Models can "think hard" for minutes, trying multiple approaches before answering. |
| **Web search** | Built-in. The model decides when to look something up and does it automatically. |
| **Code execution** | Built-in. The model can write and run a small program on your data. |
| **Multimodal** | You can drop photos, PDFs, spreadsheets, and voice memos into your prompt. |
| **Memory** | Tools now build a short profile of you and load it before every new chat. |
| **Desktop apps** | Apps like Cowork and OpenWork can find your files and act on them with permission. |
| **Coding agents** | Claude Code and OpenCode can read an entire codebase, edit files, and run tests. |

---

## Part 1: How AI Knows Things

### Concept 1 — Novice vs Power User

**The simple version:** A novice asks a short question. A power user gives a full briefing.

The difference is not cleverness. It is information.

**Real examples:**

| Task | Novice Prompt | Power User Prompt |
|---|---|---|
| Buy a car | "Which car is best?" | Uploads spec sheets, insurance quotes, driving data → "What are the trade-offs? Think hard." |
| Write a self-review | "Write a self-review." | Uploads project tracker, docs, voice notes → "Draft from this." |
| Critique a business idea | "Critique my idea." | Gives a rubric: "Score 1–10: Is there a real problem? Is there a market? What kills it?" |
| Write a blog post | "Write a blog about X." | Outline → critique outline → bullets → critique bullets → only then: full draft. |

**What a power user includes in every prompt:**
1. Relevant **files** (PDFs, spreadsheets, screenshots)
2. Clear **goal** (what should this achieve?)
3. **Limits** (budget, time, audience, tone)
4. The **exact ask** (not just "help me" — a specific output)

> A novice prompt carries only the last item. A power user adds all four.

**Think of AI as a very smart new colleague on their first day.** They are motivated, capable, and know nothing about you. Give them the briefing they need. If you would not send a new employee into a meeting without context, do not send AI a question without it.

---

### Concept 2 — Pretrained Knowledge

**The simple version:** AI learned by reading the internet. What it knows well depends on what the internet talked about a lot.

AI has no body, no senses, and did not learn by living in the world. It learned by reading enormous amounts of text: Reddit, Wikipedia, news articles, books, research papers, forums, and blogs.

**How reliable the answer is roughly matches how much the internet discussed the topic:**

| Topic | Coverage | Trust Level |
|---|---|---|
| Cooking, recipes | Extremely common | High |
| Popular movies | Reviewed thousands of times | High |
| History of an obscure village | Maybe one Wikipedia paragraph | Low — verify with a primary source |
| Recent regulatory change | After the knowledge cutoff | Trust nothing — make it search |
| Your company's internal data | Not on the internet at all | Trust nothing — the model is guessing |

**Two important consequences:**

**1. Don't waste time correcting typos.** AI was trained on internet text, which is full of typos. A misspelled prompt won't change the answer.

**2. Watch for absorbed errors.** AI also absorbed wrong beliefs and outdated information from those same sources. A confident wrong forum post can become a confident wrong answer. Always check important facts against a primary source.

> **The key question to ask:** "How would this source even know that?" Apply it to AI the same way you would apply it to a person.

**The "Loud, Quiet, Secret" Framework:**
- **Loud** = Everyone talks about it → AI knows it well
- **Quiet** = Few people wrote about it → AI might guess wrong
- **Secret** = Nobody published it → AI cannot know it at all

---

### Concept 3 — The 3 Retrieval Modes

**The simple version:** When you ask AI something, it answers in one of three ways. Your wording steers which one.

| Mode | What it uses | Speed | Best for |
|---|---|---|---|
| **Pretrained** | Only what it learned during training | Seconds | Timeless facts, common topics |
| **Web Search** | Fetches a few live web pages | ~30 seconds | Current events, recent info |
| **Deep Research** | Reads dozens of sources, writes a report | Several minutes | Complex topics needing many sources |

**You usually don't pick the mode — AI picks for you. But your wording steers it:**

| Phrase you use | Mode it usually triggers |
|---|---|
| "What is X" / "Summarize Y" | Pretrained only |
| "What's the latest on X" / "Today" / a specific city | Web search |
| "Research X thoroughly" / "Produce a report with citations" | Deep research |
| Attaching files | Pretrained for the files; may search if asked |

**Real example of each mode failing differently:**
- **Pretrained failing:** AI confidently describes rules of a folk game from a grandmother's village — almost entirely wrong, because the game barely existed on the internet.
- **Web search failing:** AI recommends a running track in Henderson, Nevada — based on a 20-year-old web page. The school no longer opens to the public.
- **Deep research shining:** "Plan a Halloween haunted house with permits, fire safety, and noise ordinances." AI researches everything, returns a multi-section report with checklists.

**AI vs Google — which to use:**

| Task | Use Google | Use AI |
|---|---|---|
| Find the official IRS page for Form 1040 | ✓ | |
| Compare three diabetes medications | | ✓ |
| Buy a replacement charger | ✓ | |
| Plan a 4-day trip with a 6-year-old | | ✓ |
| "Why are my tomato leaves yellowing?" | | ✓ (with photo) |

> If your question is "where is X" → Google. If your question is "given all this, what should I think?" → AI.

**3 habits to get better web-search results:**
1. Name the sources you trust: *"Use the WHO, the FDA, and peer-reviewed studies — not forums."*
2. Ask for a source after each claim: *"Cite the source after each claim."*
3. Ask it to flag what it could not check: *"Mark anything unverified."*

---

## Part 2: Talking to AI Well

### Concept 4 — Context Is the Whole Game

**The simple version:** The model only knows what you put in front of it. Better context = better answers.

**The Context Window** is everything the model can see while writing one answer. Modern models can hold 750,000+ words — the first 4–5 Harry Potter books.

**Six things that can be in the context window:**

| Layer | What it is |
|---|---|
| 1 (bottom) | **System prompt** — invisible instructions from the company (Claude, OpenAI, Google) |
| 2 | **Memory** — a note the tool built about you from past chats |
| 3 | **Tool descriptions** — what tools it can use (web search, code execution, file access) |
| 4 | **Your prompt** — the message you type |
| 5 | **Chat history** — all prior turns in this conversation |
| 6 (top) | **Uploaded files** — PDFs, spreadsheets, images, voice memos |

**Why Claude, ChatGPT, and Gemini feel different:** The personality is not built into the model. It is written into the company's invisible system prompt. Claude is told to be careful and honest. ChatGPT is told to be warm and broadly helpful. Gemini is told to be short and source-backed.

**You can add your own instructions layer.** In each tool's settings, you can write a few sentences about who you are and how you want it to respond. This loads in every new chat — you never have to re-explain yourself.

> **Example:** A teacher writes: *"I teach Grade 5 science. Explain everything at a 10-year-old level. Never use jargon without defining it first."* Now she never has to say that again.

**Checklist before any important prompt:**

| Question | If yes |
|---|---|
| Is there a document the answer should be consistent with? | Attach it |
| Is there a constraint AI cannot guess (budget, team, time)? | State it |
| Is there prior context (a decision, a process)? | Summarize in one paragraph |
| Is there an output format you want? | Name it |
| Is there a specific audience? | Name them |

**Memory — the 6th layer:**  
All major tools now write a short profile of you and load it before every new chat. This is NOT the model gaining memory. It is the tool placing a note in front of the model. The model is still stateless — it can only see what is placed there.

**Good habits for memory:**
- Read what it stored, once — some of it shapes every answer.
- Correct it out loud: *"You're assuming I still work in retail — I don't."*
- Use Incognito/Temporary Chat for sensitive or one-off questions.

**Context Rot — the most common mistake:**  
One long chat covering many unrelated topics = context rot. The AI still "sees" your workout plan when you ask it to fix a spreadsheet. Quality drops, answers get vaguer.

**Fix:** When the topic changes, start a new conversation. It costs nothing.

**Signs a conversation has gone stale:**
- AI references unrelated earlier parts of the chat
- Answers get longer and vaguer
- It contradicts limits you set earlier
- It apologizes repeatedly without making progress

**Projects — the solution to re-briefing every time:**  
If you paste the same files, audience, or instructions into multiple chats on one topic, use a Project (Claude/ChatGPT) or Notebook (Gemini). Set it up once, and every chat inside it inherits the context.

| Tool | Feature Name | Free? |
|---|---|---|
| Claude | Projects | Yes — up to 5 projects |
| ChatGPT | Projects | Yes — up to 5 files per project |
| Gemini | Notebooks / NotebookLM | Yes |

---

### Concept 5 — Reasoning / "Think Hard"

**The simple version:** Modern AI can think carefully before answering. You activate it with plain language.

Old advice was "think step by step." That is mostly outdated. Modern models have a built-in **reasoning mode** where the model writes out its own working process before producing the final answer.

**3 ways to turn it on:**
1. Write "think hard" or "think carefully before answering" in your prompt
2. Use the thinking-mode toggle in the interface (where available)
3. Some tools activate it automatically for hard questions

**Extended Thinking** = reasoning for longer — sometimes 10+ minutes on very hard problems. The model is not typing slower. It is trying different approaches and checking its own work before it writes what you see.

**A 2025 study (METR) found:**
> The longest task a leading AI could reliably finish doubled roughly every 7 months. By early 2025 it could handle tasks that would take a human about an hour.

So tasks you thought were "too complex for AI" two years ago — re-test them now.

**Power user pattern with thinking:**
```
I'm choosing between two cars. Attached: spec sheets for both,
my insurance quote for each, and my driving data for 6 months.

Read everything. Think hard. Then tell me:
1. The 3 trade-offs that actually matter for my driving pattern.
2. Which car you'd choose and why.
3. Under what conditions your recommendation flips.
```

**When NOT to use thinking mode:**
- Quick lookups
- One-paragraph summaries
- Casual brainstorming

> Thinking mode is slower and uses more of your usage budget. Use it for the questions where you would want a person to take their time.

---

### Concept 6 — Sycophancy and How to Neutralize It

**The simple version:** AI is trained to agree with you. It will tell you what you want to hear unless you actively prevent it.

**Why this happens:** AI models are trained on human feedback (thumbs up/down). Across millions of users, agreeing gets more thumbs up than disagreeing. So models learn to lean toward validation.

**A 2025 Washington Post analysis of 47,000 ChatGPT conversations found:** The model opened by agreeing ("yes," "correct," "you're on the right track") about **10 times more often** than it disagreed.

**Test it yourself — same model, opposite wording:**
- "Don't you think remote work is better?" → AI agrees, lists reasons.
- "Is it true that office work is more productive?" → AI agrees, lists reasons.

**Common bait — and how to rewrite it:**

| What you wrote (bait) | What it signals | Neutral rewrite |
|---|---|---|
| "Find evidence this strategy will work." | Conclusion is fixed | "Evaluate this strategy. List arguments for AND against." |
| "Why is approach A better than B?" | A wins | "Compare A and B. Score each on cost, risk, and time." |
| "Tell me my draft is ready to send." | AI tells you it is | "Score this draft 1–10 on 4 criteria. What would raise each score the most?" |
| "Confirm this code is correct." | AI confirms | "Find any bug, edge case, or unstated assumption. Say so if there are none." |

> **Rule:** Avoid *find, defend, confirm, prove, support*. Use *evaluate, compare, critique, find any, list both sides*.

**Use a Rubric:**  
Vague questions get vague praise. Named criteria force actual evaluation.

Instead of: *"Score my sci-fi story out of 100"*  
Try: *"Score it out of 10 on: plot coherence, character depth, originality, pacing, ending. Justify each score in one sentence."*

**Force a number:**  
A score is harder for AI to inflate than words like "strong" or "solid." Numbers are also actionable — a 4 and a 7 tell you which item to fix first.

> *"Grade each criterion out of 10. Then tell me how to take each one to the next level — including the ones that scored high. There is always a next level."*

**Give it permission to say "I don't know":**  
Include in your prompt: *"If you are not sure, say so. Mark anything you could not confirm as unverified."*

---

### Concept 7 — The Brainstorm-Iterate Loop

**The simple version:** Never take the first answer. Give context, ask for options, give feedback, ask again, then expand one.

AI learned from the internet. The internet is full of average ideas. So AI's first answer to a creative question is almost always the average, obvious thing.

**The way past average is a loop — not a magic prompt.**

**The 6-Step Brainstorm-Iterate Loop:**
1. **Load all context first** — constraints, files, audience, limits
2. **Ask for 3–5 options** (not one) — forces AI past its first instinct
3. **Give explicit feedback** — "I reject option 2 because... I like option 1 but want it shorter"
4. **Ask for 3–5 new options** built on that feedback
5. **Repeat 2–3 times** until one or two options feel right
6. **Only then expand the chosen option into a full draft**

**Worked example — debt payoff:**
```
I have $8,000 in credit card debt at 19% APR, $4,000 in student
loans at 5%, and $1,200 in a retail card at 24%. I have $700/month
free. I just got a $450 tax refund. Risk tolerance: low.

Give me 5 different repayment strategies. One-line rationale each.
Don't expand any yet.
```
Then: *"Reject option 2 — I want psychological wins early. Keep option 1 but fold in the $450. Give me 5 new options."*

**The loop for writing — Outline Before Drafting:**
- Round 1: 3 outline options
- Round 2: Pick one, critique it, grade it out of 10
- Round 3: Expand each heading to 3–5 bullets
- Round 4: Critique the bullets, grade out of 10, fix anything below 9
- Round 5: Only now — write the full draft
- Round 6: Grade the draft, fix, repeat until score settles at ~9.5

> **Why this works:** One word change in an outline can change the direction of the whole piece. One word change in a final draft changes one word. Almost all the power lives at the outline level.

**Four types of asks — and how tightly to grip:**

| Type | You want | Loosen | Tighten |
|---|---|---|---|
| Brainstorming | Truly different directions | Structure, tone, format, length | The problem, audience, what to avoid |
| Research | The ground mapped | The expected answer | Scope, sources, evidence criteria |
| Drafting | One thing, built | Almost nothing | Everything: voice, length, format, facts |
| Analysis | What the data says | The conclusion | The data, definitions, exact question |

> Load the full situation every time. Describe the output loosely when opening options. Describe it precisely once closing in on one.

---

## Part 3: Beyond Text

### Concept 8 — Multimodal: Images, Audio, and What's Next

**The simple version:** AI can read images, make images, and work with audio. Each direction has different strengths and weaknesses.

**Image Input (reading images):**

AI is strong at:
- The overall scene and layout
- Large, clearly separate shapes
- Whiteboard diagrams
- Handwritten and cursive text (check totals and precision items)

AI is weak at:
- Fine detail ("what gym machine is this?" often fails — they look alike)
- Counting many small items in a busy scene
- Small print at the edge of a photo

**Image Output (making images):**

AI image generators are **diffusion models** — they start from random noise and remove it step by step until an image appears. Unlike text, the entire image arrives at once. You cannot stop it early.

**2 practical tips:**
1. **Use a text AI to write your image prompt.** Ask Claude: *"Write me a detailed image prompt for a fantasy forest in Studio Ghibli style for a children's book cover."* Paste that into the image tool. Text AI writes richer prompts than you will on a first try.
2. **Build a visual vocabulary.** Words like *cinematic, watercolor, cyberpunk, anime, isometric, art-deco, claymation* are controls — image models learned these styles by name.

**Common image generation failures (and fixes):**

| Failure | What it looks like | Fix |
|---|---|---|
| Scrambled text on signs | "HAPRY BIRTDAY" | Put text in quotes in the prompt |
| Characters change between frames | Hair color shifts panel to panel | Pass the first image back as a reference |
| Hand/finger errors | Six fingers | Ask for hands out of frame or in pockets |
| Cluttered background | Bicycle merged into a chair | Describe the background yourself |
| Wrong aspect ratio | Square when you wanted landscape | Always specify: "16:9" or "1024x768 landscape" |

**Power-user workflow — professional diagrams in 15 minutes:**
1. Ask Claude to draw the idea as SVG (SVG = a drawing format written as text, so AI can type it like a sentence)
2. Convert SVG to PNG (use cloudconvert.com or screenshot at high zoom)
3. Paste the PNG into ChatGPT or Gemini and ask it to redraw with professional quality — *"Preserve every label and relationship. Only improve visual finish."*
4. Fix any dropped labels in 3–4 correction rounds

**Audio:**

Modern AI tools let you:
- **Speak your prompt** — talking out loud adds more detail than typing
- **Drop in a meeting recording** — ask for decisions, open questions, action items by owner
- **Have AI read answers aloud** — useful during commutes or walks

**What audio handles well and poorly:**

| Task | Quality | Watch out for |
|---|---|---|
| Transcribing clear speech | Excellent | Heavy accents, technical jargon |
| Speaker attribution (who said what) | Decent with 2, weak with 4+ | Always check before quoting |
| Tone, sarcasm, emotion | Improving, not reliable | Ask AI to flag what it is unsure of |
| Music or non-speech audio | Limited | Use a specialized tool |

> Audio costs pennies per minute — close to invisible for meeting summaries or voice prompts.

---

### Concept 9 — Building Small Apps with One Prompt

**The simple version:** You can build a small working tool, game, or calculator with a plain-language description — no coding required.

All three major AI tools (Claude, ChatGPT, Gemini) can render a small app directly in the chat interface, in a side panel called an **Artifact** (Claude) or **Canvas** (ChatGPT/Gemini). This is not a preview. It is a working object you can click, share by link, embed, or download.

**The 3-slot recipe:**
```
Goal:   what should this thing DO?
Input:  what does the user provide?
Output: what does the user see?
```

**Examples that work today:**
- *"Build a Pomodoro timer with a yellow theme. 25-minute work sessions, 5-minute breaks, satisfying click sound."*
- *"Build a bill splitter. I enter the total, tax, and names. It shows each person's share."*
- *"Build a fireworks simulator. I click the screen. Output: colorful fireworks at the click point."*

**What is still hard (needs real engineering):**
- Multiplayer over the internet
- Live coaching with pronunciation detection
- Anything requiring accounts or external services

> The rule: small things that fit on one screen with no accounts and no outside services work. Anything beyond that needs more than one prompt.

**For bigger projects:**
- **v0, Bolt, Lovable** — AI app-builders for full web projects
- **Claude Code / OpenCode** — command-line agents that read entire codebases
- **Cowork / OpenWork** — desktop apps that act on your files

---

### Concept 10 — Data Analysis (AI Writes and Runs Code)

**The simple version:** Upload your spreadsheet, ask in plain language, and AI will write a program, run it on your data, and answer from the actual numbers.

This is far more reliable than AI doing math in its head — because it is now using a calculator. The model chooses what to compute; the code does the computing.

**The critical warning — make sure it actually runs the code:**  
AI does NOT always run code. Sometimes it just glances at the file and guesses. A confident-looking paragraph with no computation behind it looks exactly the same as one built on real analysis.

**3 habits to force real code:**
1. Write: *"Write and run code to answer this. Show me the code you ran."*
2. Check that a code block appears in the answer. No code block = probably no computation.
3. Ask for a verifiable fact first: *"Tell me the exact row count, column names, and date range before you analyze anything."*

Best of all, ask directly: *"Are you running code on the file or estimating? If estimating, stop and run code instead."*

**Practical uses:**
- Household spending — upload a year of bank transactions
- Personal fitness — export your tracking app's CSV and look for patterns
- Small business — sales, inventory, expense files
- Any spreadsheet someone sent you that you don't want to open manually

**What to double-check even when code ran:**
- Final totals — code is precise, but AI may have summed the wrong column
- Graph labels — numbers are usually right, captions sometimes wrong
- Column interpretation — if AI misread what "TXN_AMT" means, the whole analysis is wrong

> Treat AI data analysis like work from a sharp junior analyst — fast and usually right, but always needs a check.

**Useful first prompt when uploading data:**  
*"Describe this dataset. What columns are here, what do they represent, and what 3 charts would best show what is going on?"*  
Then pick the chart you want. This catches misread columns before they become wrong analyses.

---

## Part 4: Working Safely and Choosing Tools

### Concept 11 — AI Desktop Apps and Permissions

**The simple version:** AI desktop apps can act on your real files. They are useful and require careful permission management.

Tools like **Cowork** (from Claude) and **OpenWork** can:
- Browse through a messy folder, propose renamed files, new subfolders, and then execute the plan after you approve
- Pull together project files based on dates, names, and events
- Summarize "what did I work on last quarter?" by reading a folder's contents

**The safe 4-step workflow:**
1. Tell it the task
2. Ask for a **plan**, not action
3. **Review and edit** the plan before anything happens
4. **Only then approve** execution

**Two critical warnings most people learn the hard way:**
- **Deleted files often do NOT go to your recycle bin.** They are gone permanently.
- **Edited files do NOT keep history** unless you have version control software. The AI's edit overwrites the previous version with no undo.

**The Permission Ladder — expand slowly:**

| Stage | Allow | Refuse |
|---|---|---|
| First sessions | Read-only in one small folder | Anything that writes, deletes, or renames |
| After 2–3 successful runs | Read + write inside one specific folder | Broader directories |
| After a clean week | Read across project tree, write in scoped subfolder | Anything outside that project |
| Trusted | Specific tool permissions | Open-ended "do whatever you need" |

> Trust grows with track record in your own work — not with how much you trust the company that built the app.

---

### Concept 12 — Cost, Speed, and Which Model to Use

**The simple version:** Different outputs cost very different amounts. Different models are best at different things — and the leader keeps changing.

**Cost tiers (cheapest to most expensive):**

| Output type | Speed | Rough cost |
|---|---|---|
| Text | Seconds | Fractions of a cent |
| Speech | Seconds | A few cents per minute |
| Images | ~30 seconds | Several cents each |
| Video | Minutes per clip | Many cents to dollars |
| Deep research | Several minutes | A few cents to ~$0.25 per report |

> You can run text 50 times in an afternoon. You cannot do that with video. Put more into the prompt upfront for expensive outputs.

**Cost is barely a limit at entry level.** Claude, ChatGPT, Gemini, Meta AI, and DeepSeek all offer free tiers that handle everything on this page.

**AI ability is "jagged" — uneven across tasks:**  
No single model is best at everything. The leader on any given task changes every few months.

**Two habits:**
1. Run the same prompt in 2–3 models regularly. Read the answers side by side. The differences teach you which tool fits which question.
2. Don't marry one tool. Switching costs nothing — just paste into a different tab.

**Rough model snapshot (as of 2026):**

| Tool | Strong at | Weaker at |
|---|---|---|
| **Claude** | Hard reasoning, long documents, SVG/diagram generation, code, careful writing, structured analysis | In-product image generation |
| **ChatGPT** | In-product image generation (GPT Image-2), voice mode, conversational range | Sometimes wordy, over-formats |
| **Gemini** | Fast web search, deep research with charts, Google Workspace integration | Answers can feel clipped or short |
| **Meta AI** | Free, inside WhatsApp/Instagram/Facebook — 1B+ devices; interactive visual pieces; health/science data | Coding, long agents, fewer integrations, no public API |
| **DeepSeek** | Open weights (run yourself), ~1M token context, STEM/coding benchmarks | Interface polish, fewer mobile integrations |

---

### Concept 13 — Grading AI Outputs Without an Expert

**The simple version:** When you have no expert to review AI output, use models from different companies to grade each other — not just the same model that produced the answer.

**The core problem:**  
You often cannot tell if an AI answer is right just by reading it. Confident wrong answers look exactly like confident right answers.

**Why not ask the same model to check its own work?**  
Two models from the same company share the same training data and the same blind spots. One model from one company grading its sibling's answer will miss the same errors.

**The cross-company grading approach:**  
Use a model from a different company as your reviewer. Ask it to:
- Find errors, gaps, or unstated assumptions
- Score the answer on named criteria
- State what it cannot verify

**The Arena leaderboard:**  
A public leaderboard (Chatbot Arena / LMSYS) where real users vote on two unnamed answers side by side. Because the models are anonymous, the votes reflect genuine quality — not brand recognition. This is one of the most reliable signals for which model is currently best at what.

**Practical cross-checking pattern:**
1. Produce your output with Model A (e.g., Claude)
2. Paste it into Model B (e.g., ChatGPT or Gemini): *"Here is an answer from an AI. Find any errors, unstated assumptions, or gaps. Score the answer 1–10 on accuracy, completeness, and reasoning. List the 3 weakest points."*
3. Revise based on what it flags
4. Repeat if stakes are high

**Another signal — "model families":**  
All models from one company share the same training data and blind spots. For high-stakes questions, always use at least one model from a different company family.

> With no expert in the room, models from different companies grading each other is your best signal.

---

## Summary: The 13 Concepts in One Line Each

| # | Concept | One-Line Summary |
|---|---|---|
| 1 | Novice vs Power User | A power prompt is not a cleverer question — it is a briefing. |
| 2 | Pretrained Knowledge | AI is strong where the internet is thick and weak where it is thin. |
| 3 | 3 Retrieval Modes | Answers come from training, web search, or deep research — your wording steers which. |
| 4 | Context Is the Game | The model only sees what is in front of it; what you put there decides quality. |
| 5 | Reasoning / Think Hard | Models can think longer before answering — turn this on in plain language. |
| 6 | Sycophancy | Models lean toward agreeing — neutral wording and a scored rubric removes that lean. |
| 7 | Brainstorm-Iterate Loop | Good work = context, options, feedback, options again, then expand one. |
| 8 | Multimodal | AI reads and makes images and audio, with different strengths in each direction. |
| 9 | Building Small Apps | One prompt can build a small working app you can edit, share, and download. |
| 10 | Data Analysis | AI can run code on your data — but only if you make sure it actually runs. |
| 11 | Desktop Apps | Desktop apps act on your files — give them the smallest permission the job needs. |
| 12 | Cost and Model Choice | Cost and speed differ across text, images, audio, and video — no single best model. |
| 13 | Cross-Model Grading | With no expert in the room, models from different companies grading each other is your best signal. |

---

## Quick Reference: Before Every Important Prompt

- [ ] Have I attached all relevant files?
- [ ] Have I stated the goal, limits, and audience?
- [ ] Is the topic recent or private? (If yes: name sources or attach the data)
- [ ] Am I asking for one answer or for options? (Options = do not expand yet)
- [ ] Have I removed the conclusion from my question? (Avoid: "prove," "confirm," "find evidence that")
- [ ] For complex questions: did I write "think hard"?
- [ ] For data questions: did I write "write and run code, show me what you ran"?
- [ ] Is this a new topic? (If yes: start a new chat to avoid context rot)

---

*Explained from: [agentfactory.panaversity.org/docs/ai-prompting-2026](https://agentfactory.panaversity.org/docs/ai-prompting-2026)*  
*Part of the Panaversity Agent Factory Program — Foundations (Everyone) track*