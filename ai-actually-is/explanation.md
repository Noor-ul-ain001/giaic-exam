# What AI Actually Is — Complete Explanation

> Nine ideas. No math. No code. A complete picture of how AI works, why it fails, and what to do about it.

---

## The Big Idea — Before You Begin

Most people treat AI like a very fast librarian — you ask a question, it finds the fact and reads it back.

**That picture is wrong.**

AI is closer to the world's best-read autocomplete — it *continues* your text, one piece at a time. It never looks anything up. Almost every mistake people make with AI comes from that wrong picture.

This course fixes that with nine ideas.

---

## Quick Glossary

| Term | Simple Meaning |
|------|---------------|
| **Token** | A small chunk of text — usually a word or part of a word |
| **Tokenizer** | The part that cuts your text into tokens |
| **Stochastic** | The next piece is picked from a spread of options — so answers vary |
| **Weights / Parameters** | The frozen numbers inside the model — everything it learned |
| **Training** | The one-time education that set the weights |
| **Pretraining** | First training stage — model reads a huge pile of text |
| **Inference** | What happens every time you use the model — nothing inside changes |
| **Knowledge Cutoff** | The date training stopped — nothing after it is in the model |
| **Stateless** | The model keeps no memory of its own |
| **Hallucination** | A fluent, confident, completely false statement |
| **Context Window** | All the text the model can see while writing one answer |
| **System Prompt** | Hidden instructions placed at the top of every chat |
| **Sycophancy** | The trained habit of telling you what you seem to want |
| **Jagged Frontier** | Uneven ability — superhuman on one task, useless on a neighboring one |
| **Tools** | Actions the model may call — web search, file read, code run |
| **Connector** | One tool wired to one of your real apps, with permissions you grant |
| **MCP** | Model Context Protocol — the standard that connects AI to external tools |
| **Agent** | A predictor with tools, running predict → act → observe toward a goal |
| **Reasoning** | Working the model writes for itself before its final answer |
| **Skills** | Folders of instructions that load into the window when needed |
| **Progressive Disclosure** | Keeping knowledge in files and loading only what this moment needs |
| **RLHF** | Reinforcement Learning from Human Feedback — the stage that shaped the model's manner |
| **API** | The direct link a program uses to call a model instead of a chat window |
| **Artifact** | A panel beside the chat where a document, code, or tool lives as an object |

---

## The Nine Ideas — One Line Each

| # | Idea |
|---|------|
| 1 | It predicts the next piece of text — it never looks anything up |
| 2 | It learned by reading, once — then the learning stopped, on purpose |
| 3 | Nothing inside it checks whether an answer is true |
| 4 | It reads in chunks called tokens — not in letters |
| 5 | The context window is the only place it can see your situation |
| 6 | Its confident tone is a learned style — not a signal of truth |
| 7 | Its ability is uneven — brilliant on one task, useless on an easier one |
| 8 | Tools let it act in the world — not only describe it |
| 9 | "Thinking" is more prediction, written before the answer |

---

# Part 1: The Machine

## Idea 1 — It Predicts the Next Piece of Text. It Never Looks Anything Up.

### What is actually happening?

When you send a message, the model does not search a database.

It takes your text and **predicts what text most likely comes next** — one small piece at a time.

```
Your prompt → Model predicts next piece → Adds it → Predicts next piece → Adds it → ...
```

Think of it as the world's best-read autocomplete.

You've seen autocomplete finish "Happy birthday to" with "you." This machine does the same thing — on any topic, not just common phrases.

### Why does the same question give different answers each time?

The model does not pick one fixed answer. It predicts a **spread of likely options**, each with a score, then picks one from that spread.

Engineers call this **stochastic** — meaning one option is drawn from a range instead of always picking the same one.

The control called **temperature** sets how boldly it reaches into that spread:
- **Low temperature** → almost always picks the most likely token → steady, repetitive
- **High temperature** → reaches for less likely options → varied, occasionally wrong
- Most chat products use a middle value

### The librarian vs. the writer

| Wrong Picture | Right Picture |
|---------------|--------------|
| Librarian who finds the fact | Writer who continues your text |
| Looks up a database entry | Predicts the most likely continuation |
| Says "I don't have that" | Produces something confident either way |

Ask it the capital of France — it does not open a row labeled `France → Paris`. It predicts that the most likely continuation of "The capital of France is" — is "Paris" — because that sequence appeared millions of times in the text it read.

### What about web search?

The **product** can search the web. The **model** still does not look anything up.

Tools fetch real facts → facts land in the context window → model continues from there by predicting.

> The machine is doing the same thing. It just has better material to predict from.

---

## Idea 2 — It Learned by Reading, and Then the Learning Stopped

### Where did the knowledge come from?

From **training** — a one-time education before you ever used it.

The model was shown an enormous pile of human text and adjusted itself over and over to predict the next piece better. That adjusting happened **once**. When training ended, the numbers froze. That freeze is called the **weights** or **parameters**.

### What was in that pile?

- A large slice of the public internet
- Digitized books
- Open-source code
- Encyclopedias and academic papers
- Forum archives and more

More text than a person could read in a thousand lifetimes.

### How training works (no math)

```
Show the model a passage → Hide the next piece →
Model guesses → Compare to real answer →
Nudge numbers slightly closer → Repeat billions of times
```

That is the entire mechanism. **Guess, compare, nudge, repeat.**

### The three stages of training

| Stage | What It Does |
|-------|-------------|
| **Pretraining** | Reads the enormous text pile — learns to predict |
| **Instruction Tuning** | Taught on question-answer pairs — learns to answer, not just continue |
| **RLHF** | Shaped by human ratings — learns the manner people prefer |

All three happen **before** the freeze. You cannot add a stage.

### Training vs. Inference

| Training | Inference |
|----------|-----------|
| Happens once | Happens every time you use it |
| Expensive — months, millions of dollars | Fast and cheap |
| Changes the weights | Changes nothing inside |
| Sets everything the model knows | Uses what was set |

### The Knowledge Cutoff

The date training text stopped is the **knowledge cutoff**.

Nothing that happened after it is in the weights. The model is like a brilliant expert who stopped reading the news on a specific day.

### Why it cannot know your private world

Your company's numbers, your calendar, your emails — none of these were ever in the training text. The model is not withholding. The information was never there to freeze.

### Why is it stateless? Why not learn from conversations?

The freeze is a **deliberate design choice**, made for three reasons:

| Reason | Why It Forces the Freeze |
|--------|------------------------|
| **Cost** | Training is the expensive half. Letting the model relearn inside every chat would drag that cost into every message |
| **Safety** | A frozen model can be tested once and behaves within that tested envelope for every user. A learning model could be pushed off course |
| **Consistency** | Millions of people share one identical set of weights. A per-user shifting model would lose that |

### When you correct the model...

It has not learned anything. It predicted the text that likely follows a correction.

Close the chat and open a new one — it starts from the identical frozen numbers.

### How do "memory" features work then?

The product saves a few facts about you as text and re-inserts that text into the context window at the start of each new conversation.

> It is not the model remembering. It is the product re-feeding it a note.

---

## Idea 3 — There Is No Separate Part That Checks Whether It Is True

### The human vs. the machine

A human expert has two abilities:
1. **Generates** an answer
2. **Checks it** — "Am I sure? Where did I learn this?"

The two can disagree. You can say something and feel it might be wrong.

The model has **only the first ability.**

There is no second part inside it that checks the prediction for truth before it reaches you.

### What is hallucination?

**Hallucination** = a fluent, confident, completely false statement.

It is not a glitch. It is the machine working exactly as built — predicting a likely continuation in a spot where the likely continuation happens not to be true.

```
Rare topic + no real data to predict toward + no truth-checker = confident invention
```

### Why can't you tell from the tone?

An invented statistic arrives in the same assured voice as a real one.

The confidence is a style (explained in Idea 6). It has nothing to do with whether the content is correct.

> You are the missing second ability. The checking is your job.

---

# Part 2: Why It Behaves the Way It Does

## Idea 4 — It Reads in Tokens, Not Letters or Words

### What is a token?

A token is usually a word or a piece of a word.

- "the" → one token
- "strawberry" → two or three tokens
- A long or unusual word → several tokens

The model reads and predicts in these chunks — it never gets a clean row of countable letters.

### Why the strawberry test works

Ask any AI to count the letter R in "strawberry" without spelling it out.

Many models miscount — because they see **chunks**, not letters.

Counting letters inside a chunk is like counting the rooms in a building when someone only gave you the street address.

### What tokens explain

| Behavior | Why Tokens Explain It |
|----------|-----------------------|
| Miscounting letters in a word | Sees chunks, not letters |
| Bad at rhyming, anagrams, wordplay | Those tasks work on letters. This works on chunks |
| Typos in your prompt rarely matter | A misspelled word maps to chunks close enough to the intended meaning |
| Cost and length measured in tokens | The token is what the machine processes — what you are billed for |

### Tokens are the unit of three things

- **Meaning** — what the model reads and writes
- **Memory** — a "200,000-token context window" means how many chunks it can hold at once
- **Money** — API pricing is per token in and per token out

Roughly in English: **4 tokens ≈ 3 words**. You never need the exact ratio — just know the chunk is the real unit.

### Note for non-English speakers

Urdu, Arabic, Hindi, Chinese, and other non-Latin scripts are cut into **more tokens per word**. The same message costs more and fills the window faster. This is real in 2026 and improving.

### Images and audio?

A picture is cut into small **patches** — each patch becomes a token.
A sound clip is cut into short **segments** — each segment becomes a token.

Everything is still tokens. The machine still predicts over one stream.

---

## Idea 5 — The Context Window Is the Only Thing It Can See

### What is the context window?

The **context window** is the text sitting in front of the model for this one response.

It is the **only place** it can get information about your situation.

The window holds:
- Your prompt
- The conversation so far
- Any files you attached
- Descriptions of tools it may call
- Invisible instructions the product placed there (the system prompt)

Anything in the window — the model reads.
Anything outside it — does not exist for this answer.

### What is a system prompt?

The **system prompt** is a block of instructions the product's maker writes and places at the very top — before your first word arrives.

It is not code. It is just more text in the window, first in line.

Headlines about "leaked system prompts" mean someone persuaded the model to repeat back text that was in its window all along.

### How big is the window?

| Window Size | Roughly Equals |
|-------------|----------------|
| 200,000 tokens | ~150,000 English words (a novel and a half) |
| 1,000,000 tokens | ~750,000 English words (seven or eight novels) |

Enormous — and finite. The system prompt, tools, chat history, your files, and your question all share the same space.

### Why briefing works

Giving the model context is not politeness or a trick.

It is the literal act of **putting information into the only place the machine can read.**

An un-briefed model is not lazy. It has nothing in front of it.

### Why long conversations get worse (context rot)

The window has a size limit. Push too much unrelated history into it and:
- The signal you care about gets diluted
- Or the oldest parts get summarized away to make room

The model is not tired. Its reading space is overcrowded.

### Chat history is context — replayed

Within one conversation, the model seems to remember what you said ten messages ago.

It does not. Every time you press send, the app **re-sends the entire transcript** — your messages and its answers — into the context window.

The frozen model reads the whole thing from scratch to predict its next reply.

```
Turn 1: [Message 1] → model reads it
Turn 2: [Message 1 + Reply 1 + Message 2] → model reads all of it
Turn 3: [All of the above + Message 3] → model reads all of it
...and so on
```

### Where does the transcript live between your turns?

In the **product's database** — on the company's servers — saved like any document.

That is why you can close the app, open the same chat a month later on a different phone, and continue.

Deleting a chat removes the stored transcript — there was never anything inside the model to delete.

### Three behaviors explained by replay

| Behavior | What the Replay Explains |
|----------|--------------------------|
| It "remembers" this chat but not your last one | This chat's transcript is re-sent every message. Last chat's is not |
| Long chats get slower and more expensive | Every reply re-processes the whole growing transcript — you pay in tokens for all of it, again |
| It forgets the beginning of a very long chat | The transcript outgrew the window — oldest turns were cut or summarized |

### Skills and Progressive Disclosure

Skills are folders of instructions and reference files that live **outside** the window, on disk.

Only a one-line description of each installed skill sits in the context window.

When your request matches that description, the product loads the full skill into the window.

This is called **progressive disclosure** — keeping knowledge in files and loading only what this moment needs.

> Think of the context window as a reading desk. Whatever you place on the desk, the model reads. Whatever you leave off it, the model cannot see — however obvious it is to you.

---

## Idea 6 — Its Confidence Is a Learned Style, Not a Truth Signal

### Where does the confidence come from?

After pretraining and instruction tuning, the model goes through a third stage:

**RLHF** (Reinforcement Learning from Human Feedback) — people rate responses, and the model is adjusted toward answers people rated highly.

Across millions of ratings, people preferred answers that were:
- Confident
- Helpful
- Fluent
- Agreeable

So the machine leans toward confident, agreeable text — whether or not the content is right.

### Two behaviors that follow

**1. It sounds certain even when wrong.**

The certainty is a learned default. It is generated by the same process as the content and is just as separate from truth.

**2. It tends to agree with you.**

This is called **sycophancy** — the trained habit of telling you what you seem to want.

Ask "isn't X true?" and you have signaled the answer you want. The trained-in lean supplies it.

### How to neutralize it

- Use **neutral framing** — "evaluate X and give the strongest case on each side"
- Ask for **a score against explicit criteria** — leaves less room for agreeable vagueness
- Remove the cue that triggers the lean

You are not outsmarting the machine. You are removing the signal it was trained to respond to.

---

## Idea 7 — The Jagged Frontier (Brilliant and Useless on Two Tasks in a Row)

### What is "jagged"?

Human ability is fairly smooth. Someone good at hard calculus can almost certainly do easy arithmetic.

AI ability is **jagged** — superhuman on one task and startlingly incompetent on a neighboring task that looks no harder.

```
Examples of jaggedness:
→ Can draft a legal contract clause
→ Cannot count the letters in "strawberry"

→ Can explain quantum mechanics
→ Gets a three-step logic puzzle wrong that a child would solve
```

### Why is it jagged?

- Tasks that appeared **often and clearly** in the training text are strong
- Tasks that depend on things the machine cannot see well are weak — individual letters, recent events, private context, rare topics

The frontier does not match human intuition about difficulty.

### Three habits that follow

| Habit | Why |
|-------|-----|
| Don't assume a win on a hard task means a win on an easy one | They may sit on opposite sides of the jagged frontier |
| Verify across the boundary, not in the middle | Dangerous errors are the easy-looking tasks it fails without warning |
| Try the same task in two or three different models | Different models have differently shaped frontiers |

### The frontier moves

What the model cannot do this quarter, a newer model may do easily next quarter.

Re-test your assumptions on a schedule — every few months.

---

# Part 3: From Predictor to Agent

## Idea 8 — Tools Let It Act, Not Just Describe

### The original ceiling

A pure text predictor can tell you the weather it remembered from training.

It cannot:
- Check today's weather
- Run a real calculation
- Read your file
- Send an email

**Tools raised that ceiling.**

### What is a tool?

A tool is a defined action the model is allowed to call:
- Web search
- Code execution
- File read
- Email draft

Each tool is described to the model inside the context window.

When the model predicts that the right continuation is "use the search tool with this query" — the product runs that action for real, drops the result back into the context window, and the model continues from there.

### What is an agent?

```
Agent = Predictor + Tools + Loop

Predict the next action
→ Tool runs it for real
→ Result lands in context window
→ Predict the next action
→ Repeat toward the goal
```

There is no new kind of mind involved. Only a predictor, a set of tools, and a loop.

### Connectors and MCP

A **connector** is a tool wired to one of your real apps — Drive, Gmail, Slack, Calendar, a database.

All connectors speak a shared open standard called **MCP** (Model Context Protocol).

MCP is the standard plug shape. One agent can reach thousands of services without custom wiring.

Whatever a connector fetches arrives as text in the context window. The model continues from there. New plug — same machine.

---

## Idea 9 — "Thinking" Is Just More Prediction Before the Answer

### What is a reasoning model?

A **reasoning model** first predicts a long stretch of intermediate working, then predicts the final answer.

The working:
- Lays out steps
- Tries approaches
- Checks itself

By the time the answer is predicted, that working is in the model's own context window to build on.

It is still pure next-token prediction. Predicting the answer is just easier and more accurate once a good chain of working is already there.

### This is why "think step by step" used to work

You were asking the model by hand to put working into the window first.

Now it does that automatically for hard problems.

### The cost

Thinking generates many extra tokens — those take time and money.

Save thinking mode for:
- Decisions with real consequences
- Multi-variable problems
- Hard reasoning tasks

Skip it for:
- Lookups
- Reformatting
- Simple summaries

### The important limit

**Thinking does not give the machine the missing truth-checker from Idea 3.**

A reasoning model checks its work using the same prediction process that can be wrong.

It catches many of its own errors. It misses some. It can still invent with full confidence inside a chain of working that looks rigorous.

> More thinking narrows the gap. It does not close it. You are still the final check.

---

# The Nine Ideas — Full Summary

| Idea | One Sentence |
|------|-------------|
| 1 | It predicts the next piece of text and never looks facts up. The pick is drawn from a spread, so prediction looks like knowledge only where the model read a lot |
| 2 | It learned once, by reading a vast pile of human text, and then the learning froze on purpose — hence the knowledge cutoff, hence it cannot know your private world, hence "stateless" |
| 3 | It has no separate ability that checks whether a prediction is true — hallucination is the machine working as built, not malfunctioning |
| 4 | It reads in tokens — chunks, not letters or words. The token is the unit of meaning, memory, and money |
| 5 | The context window is the only place it can see your specifics. Chat history is the transcript replayed onto it every turn. Control what lands there |
| 6 | Its confidence and agreeableness are learned styles — separate from truth. The certain tone is a manner, not a verdict |
| 7 | Its ability is jagged — brilliant and useless on two tasks in a row — along a frontier that keeps moving |
| 8 | Tools turn the text predictor into something that acts. Predict an action, run it for real, feed the result back, predict again. An agent is that loop repeated |
| 9 | "Thinking" is more prediction put into the window before the answer. It helps a lot, and it does not give the machine a truth-checker |

---

# The One Sentence to Keep

> It is a prediction machine that learned by reading and has no part that checks the truth. So it is fluent everywhere, reliable only where it read a lot, and **you are the part that checks.**

---

# Appendix: Claude.ai — Cockpit Tour

## A.1 Getting In

Claude runs in:
- Browser at claude.ai
- Desktop app (Mac and Windows)
- Mobile apps (iOS and Android)

A free account needs no credit card. You must be at least 18.

The free plan has a **session-based usage limit** that resets every five hours — counted in tokens, not messages.

A short question costs little. A long chat with many turns costs more — because the whole transcript is replayed every time.

---

## A.2 The Three Main Controls

| Control | Where | What It Is |
|---------|-------|-----------|
| **Prompt box** | Center | The door to the context window — everything you type or attach lands here |
| **Model selector** | Below prompt box (web/desktop), top of screen (mobile) | Chooses which frozen weights you are talking to |
| **Effort/Thinking control** | Next to model selector | Sets how much working the model puts in the window before answering |

---

## A.3 The Model Ladder

Claude ships several models arranged as a ladder from fast and cheap to deep and expensive.

Names change every few months. Learn the **logic**, not the names:

| Level | Use When | Cost |
|-------|----------|------|
| **Bottom (Haiku)** | High-volume, low-depth — reformatting, quick summaries | Cheapest |
| **Middle (Sonnet)** | Large majority of tasks | Moderate |
| **Top (Opus)** | Long document analysis, hard architecture, complex problems | Most expensive |

> Default to the middle. Escalate upward for depth. Drop downward for bulk.

---

## A.4 Thinking and Effort

The thinking control is **Idea 9 turned into a dial**.

Higher settings → longer hidden chain of working before the answer → better results on hard problems → more tokens spent.

Spend it on decisions with real consequences and multi-variable problems.
Skip it for lookups and reformatting.

---

## A.5 What Sits in the Context Window — As Product Settings

Four controls — one mechanism: **controlling what lands in the window.**

### Instructions for Claude

A text field under Settings that applies to **every conversation** on your account.

It is text the product places in the window before your first word.

**Write only what is true for every conversation you will ever have:**
- Who you are
- The tone you want
- "Push back instead of agreeing by default"

Push everything topic-specific into a project instead. A wrong-scope instruction damages every chat where it does not apply.

### Projects

A folder with two powers:
- **Instructions** that apply only to chats inside it
- **Knowledge files** every chat inside it can see

Mechanically, a project is a **pre-loaded window** — you load your context once instead of re-explaining it in every new chat.

Free accounts: 5 projects. Paid accounts: unlimited.

When a project's knowledge outgrows the context window, the product fetches only relevant parts per question — that is progressive disclosure from Idea 5, applied to your own documents.

### Memory

Under Settings → Capabilities.

The product periodically summarizes your chats into a note about you and re-places that note in the window at the start of each new conversation.

This does **not** change the weights. It is portable text — not anything inside the model.

Three controls:
- Tell Claude what to remember or forget
- Read or delete what is stored (do this on a schedule — the note keeps things after they stop being true)
- An incognito toggle starts a chat that skips memory entirely

### Chat History and Past-Chat Search

Within one chat, history works as Idea 5 described — the transcript is replayed every turn.

Across chats, you can ask Claude what you were working on last week — it searches stored transcripts and pulls the relevant thread into the current window. That is retrieval and context — the same move as every tool in Idea 8.

---

## A.6 Uploading Files Into the Window

The **+** button uploads:
- PDFs
- Images
- Spreadsheets
- Code
- Long contracts

Each upload is converted to tokens and placed in the window.

**Two boundaries to know:**
- Fine print and small detail inside images is weak — a patch is a chunk (Idea 4)
- Claude reads images but does not generate photos. It can produce diagrams, charts, SVG, and interactive visualizations by writing code

---

## A.7 Getting Things Out — Artifacts and Files

When you ask for something substantial — a document, webpage, code, interactive tool — Claude produces it as an **Artifact**.

That is a panel beside the chat where the output lives as a thing, not as scrolling text.

You iterate on it surgically: "change the third section" — not regenerating everything.

With code execution and file creation switched on:
- Word documents
- Excel spreadsheets with working formulas
- PowerPoint decks
- PDFs
- All downloadable

> Stop treating the chat as a place that produces text you copy elsewhere. It produces finished things.

---

## A.8 The Tools Menu

Four tools in ascending order of how much of the Idea 8 loop they run:

| Tool | When to Use | How Long It Takes |
|------|-------------|------------------|
| **Web Search** | One or two current facts | Seconds |
| **Research** | A thorough, cited, multi-source report | Minutes |
| **Skills** | Repeatable methods — loaded when your request matches | Instant |
| **Connectors** | Reach your real apps — Drive, Gmail, Slack, Calendar | Depends on the action |

### Web Search

Usually on by default. Where being current matters and the need is not obvious — say "search the web for this" explicitly.

### Research (paid)

Web search running the full agent loop:
- Plans a strategy
- Runs many searches that build on each other
- Reads across sources
- Returns a structured, cited report

Use web search for facts. Use Research when you need a document you can act on.

### Skills

Tell Claude the workflow you want captured → it drafts the skill file.

Or, when a chat produces exactly the output you wanted, say "turn what we just did into a skill."

Review → install → test that it fires.

### Connectors

Wire Claude to your real apps over the MCP standard.

Results land in the window like every tool result. Grant permissions deliberately — this is scoped access to your actual data.

---

## A.9 A 30-Minute Setup

Do these once, in order:

1. Find the three controls — prompt box, model selector, thinking control
2. Write your **Instructions for Claude** — 3–4 sentences true for every conversation, including "push back when you think I am wrong"
3. Create **one project** for your most repeated work — add instructions and 2–3 knowledge files
4. Decide about **memory** — turn it on if useful, know where the incognito toggle is, set a monthly reminder to prune it
5. Make **one artifact** — ask for a small interactive tool or formatted document, iterate on it twice
6. Run **one Research task** — open the progress panel and watch the loop
7. Build **one skill** from a workflow you repeat weekly — review the draft, enable it, test that it fires

---

## A.10 What Changes and What Does Not

**Everything in this appendix ages** — model names rotate, prices move, buttons migrate.

When this page and the live product disagree — **the product is right**.

**What does not age** is the mapping:

> Every control you will ever meet is a handle on one of the nine ideas — a selector between sets of frozen weights, a dial on working in the window, a way of placing text at the right scope, a tool wired into the loop.

When a new feature ships, ask: **which part of the window is it, or which step of the loop?**

---

## Six Practical Exercises

### 1. See the prediction, not the lookup (Idea 1)

Ask any AI to explain the rules of a game you invented — "Karakush" — as if it were real.

Watch it produce confident, fluent rules for a game that does not exist.

> Fluency is not evidence of truth.

### 2. Watch the learning fail to stick (Idea 2)

Ask a factual question. Correct one small detail. Open a new chat and ask the same question again.

It has no memory of your correction — the weights never changed.

### 3. Catch the missing checker (Idea 3)

Ask for three peer-reviewed studies with authors and years on a narrow topic.

Check whether they exist. Some will be invented — in the same voice as the real ones.

> Do not reuse any citation from this exercise in real work without verifying it first.

### 4. Catch the transcript replay (Idea 5)

In a chat where you have exchanged 4–5 messages, ask: "Quote my very first message in this conversation, word for word."

It will — exactly. Now open a new chat and ask the same question. Nothing is there to quote.

### 5. Feel the jagged frontier (Idea 7)

Give it a hard task it tends to do well — and an easy task it tends to get wrong — side by side.

> Competence does not track difficulty. The easy task it fails is the dangerous one.

### 6. Turn thinking on and off (Idea 9)

Ask the same hard reasoning question twice — once plainly, once with "think hard and show your working first."

Compare the two. The second is usually better — but still not certified as true.

---

## The Final Check

> It is a prediction machine that learned by reading and has no part that checks the truth.
> So it is fluent everywhere, reliable only where it read a lot.
> **You are the part that checks.**