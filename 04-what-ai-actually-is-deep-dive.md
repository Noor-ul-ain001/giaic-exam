# Deep Dive: *What AI Actually Is* (complete)

This guide covers the whole course, idea by idea, and links each idea to your other files. Everything is cited by file and section. "WAI" means *What AI Actually Is A Crash Course.md*. Anything not from your files is labelled **Outside the material**.

**Why this file matters for the exam.** The course itself says to read it **before** the other Foundations courses (WAI, "Read this one first"). It gives the **mechanism**, and the other courses give the **habits** (WAI, "How this course and the prompting course split the work"). Most exam questions about *why* AI fails ("why did it invent a source?", "why did it forget?") are answered here.

WAI does not map its sections to exam domains itself. The mapping below is **mine**, taken from your topic map (`01-topic-map.md`, §3).

| WAI topic | Exam domain |
|---|---|
| No truth-checker, hallucination (§3); confidence is a style (§6); jagged frontier (§7) | **D2 Output Evaluation and Validation (21%)** |
| Tokens (§4); the context window is all it sees (§5) | **D1 Prompting and Task Execution** |
| Model ladder (A.3); thinking and effort (A.4); knowledge cutoff (§2) | **D3 Product and Model Selection** |
| Context window as product settings (A.5); uploads, artifacts, tools menu, setup (A.6 to A.9) | **D5 Configuration and Knowledge Management** |
| Tools, connectors, MCP, the agent loop (§8) | Supports **D4 Workflow** and **D5** |

---

## ⚡ All key points on one page (for quick revision)

**The one sentence to keep**
- AI is a **prediction machine** that learned by reading and has **no part that checks the truth**.
- So it is fluent everywhere, reliable only where it read a lot, and **you are the part that checks**.
- Picture a **well-read writer**, not a librarian.

**Idea 1. It predicts, it never looks up**
- It predicts the **next token** (small chunk of text), again and again.
- There is **no database** inside. Common facts come out right only because they appeared often.
- **Stochastic**: it picks from a spread of likely options, so answers vary. **Temperature** sets how boldly it picks.

**Idea 2. It learned once, then froze**
- **Training** (once, expensive) set the **weights**. **Inference** (every use) changes nothing.
- Three training stages: **pretraining** (read everything), **instruction tuning** (act like an assistant), **RLHF** (learn the preferred manner).
- Frozen on purpose for **cost, safety/testing, consistency**. Hence **knowledge cutoff**, no private knowledge, and **stateless**.

**Idea 3. No truth-checker**
- Humans have two abilities: **generate** and **check**. The model has only **generate**.
- **Hallucination** = fluent, confident, false. It is the machine **working as built**, not a glitch.
- Recipe: **rare topic + forced continuation + no checker = confident invention**.

**Idea 4. Tokens, not letters**
- Text is cut into **tokens** by the **tokenizer**. About **4 tokens ≈ 3 English words**.
- Tokens are the unit of **meaning, memory, and money**.
- Explains: letter counting fails, typos don't matter, non-English costs more tokens. Images become **patches**, audio becomes **segments**.

**Idea 5. The context window is all it sees**
- The **context window** = everything in front of the model for one answer: system prompt, your prompt, history, files, tool descriptions.
- **Chat history is replayed** into the window every turn. It is stored in the product's database, not in the model.
- **Skills** stay outside the window until needed (**progressive disclosure**).

**Idea 6. Confidence is a style**
- The sure tone was **learned** (mostly from RLHF ratings). It is **not a truth signal**.
- **Sycophancy**: it leans toward what you seem to want.
- Fix: **neutral framing** and **scoring against explicit criteria**.

**Idea 7. The jagged frontier**
- Brilliant on one task, useless on an easier-looking one next to it.
- Weak spots: **letters, very recent events, your private context, rare topics**.
- **Verify across the boundary, not in the middle**. Try 2 to 3 models. Re-test on a schedule.

**Idea 8. Tools let it act**
- A **tool** = an action it may call (search, code run, file read). The result **lands in the context window**.
- **Agent = predictor + tools + predict-act-observe loop**. No new kind of mind.
- **Connector** = a tool wired to one real app. **MCP** = the standard plug they all use.

**Idea 9. "Thinking" is more prediction**
- A **reasoning** model writes working first, then the answer. Still next-token prediction.
- Helps hard problems. Costs **extra hidden tokens** (time, money). Skip it for lookups.
- It does **not** add a truth-checker. More thinking **narrows** the gap, it does not **close** it.

**Appendix (Claude.ai), the exam-heavy parts**
- **Model ladder**: default to the **middle**, go **up** for depth, go **down** for bulk. Learn the logic, not the names.
- **Four controls, one mechanism**: Instructions for Claude (note in every window), Project (pre-loaded window), Memory (self-updating note), History search (retrieval into the window).
- **Anthropic's four**: Projects carry context, Skills define procedures, Code execution verifies computations, Memory persists continuity.
- **Web search** for a fact, **Research** for a cited document you can act on.

---

## 0. The big picture in one minute

> **🔑 Key points (easy)**
> - Most people think AI is a **fast librarian** that looks facts up. That picture is **wrong**.
> - AI is closer to **the world's best-read autocomplete**.
> - Nine ideas explain almost every surprising thing it does.
> - Once you know the mechanism, failures become **predictable and avoidable**.

**The car analogy** (WAI, opening). You can drive without knowing the engine, until something goes wrong. People who know roughly how an engine works stay calm. People who don't see "one closed box that either works or does not". With AI, not knowing the machine leads to two opposite mistakes: **trusting it too much** or **writing it off**.

**The strawberry test** (WAI, "Prove it in two minutes"). Ask a model how many R's are in "strawberry" (with a deliberate typo in the prompt). Some models miscount, then get it right when they spell the word letter by letter.

| What you see | What it proves |
|---|---|
| A model that writes working code miscounts letters | It doesn't see **letters**, it sees **tokens** (chunks) |
| The typo "apear" changed nothing | A typo still lands on chunks **close enough** in meaning |
| It gets it right after spelling out | Spelling out forces each letter into its own piece |

**Warning from the course.** The strawberry question is famous, so a model may have **memorized** it. An instant right answer shows **familiarity, not skill**. Use an invented string ("braverrikromarent") instead.

**The three parts** (WAI roadmap).

| Part | Ideas | Question it answers |
|---|---|---|
| 1. The machine | 1 to 3 | What literally happens when I press send? |
| 2. Why it behaves this way | 4 to 7 | Why does it miscount, forget, sound sure, and fail easy tasks? |
| 3. From predictor to agent | 8 to 9 | How does a text predictor become something that acts? |

**Go deeper**

- **The core principle:** "Almost every surprising thing AI does is explained by what it actually is, not by it being smart or dumb" (WAI, "Prove it in two minutes"). On the exam, the right answer usually names a **mechanism**, not a feeling ("it got lazy", "it was lying").
- **Mechanism vs habit split:** WAI explains *why*; *AI Prompting in 2026* teaches *what to do*. Example: WAI Idea 5 explains why the window is all the model sees; AI Prompting Concept 4 teaches how to manage it (WAI, "Where the two touch" table).

> **Urdu:** AI کوئی لائبریرین نہیں جو حقائق ڈھونڈ کر لاتا ہے۔ یہ ایک بہت پڑھا لکھا "آٹو کمپلیٹ" ہے جو اگلا حصہ پیش گوئی کرتا ہے۔

---

## Exam vocabulary (from the WAI glossary)

These words appear in exam options. Know each in one line (WAI, "Quick glossary").

| Term | Simple meaning |
|---|---|
| **Token** | A small chunk of text, usually a word or part of one |
| **Tokenizer** | The part that cuts text into tokens |
| **Stochastic** | The next piece is drawn from a spread of options, so answers vary |
| **Weights / parameters** | The frozen numbers inside the model that hold everything it learned |
| **Training** | The one-time education that set the weights |
| **Pretraining** | First stage: reading a huge pile of text |
| **Instruction tuning** | Stage that taught it to **answer** a question, not continue it |
| **RLHF** | Reinforcement learning from human feedback; shaped its manner |
| **Inference** | Every use of the model. Nothing inside changes |
| **Knowledge cutoff** | The date the training text stops |
| **Stateless** | The model keeps no memory of its own |
| **Hallucination** | A fluent, confident, false statement |
| **Context window** | All the text the model can see while writing one answer |
| **System prompt** | Instructions the product puts at the top of the window |
| **Progressive disclosure** | Keep knowledge in files; load only what this moment needs |
| **Patches / segments** | Pieces of an image / sound clip; each becomes a token |
| **Sycophancy** | The trained habit of telling you what you seem to want |
| **Jagged** | Superhuman on one task, useless on an easier one |
| **Tool** | An action the model may call (search, file read, code run) |
| **Connector** | One tool wired to one of your real apps, with permissions you grant |
| **MCP** | Model Context Protocol: the standard that lets any connector work with any agent |
| **Agent** | A predictor with tools, running predict, act, observe toward a goal |
| **Reasoning** | The working a model writes for itself before its final answer |

---

## Idea 1. It predicts the next piece of text, and never looks anything up (D2, D3)

> **🔑 Key points (easy)**
> - The model predicts **what text most likely comes next**, one token at a time.
> - Each new token is **fed back in** to predict the next one.
> - It stores **no facts and no phrases**, only numbers that score what is likely next.
> - For **common** facts, prediction looks like lookup. For **rare** topics, it still predicts, but has nothing true to aim at.

**The wrong picture vs the right picture** (WAI §1).

| Wrong picture: librarian | Right picture: best-read autocomplete |
|---|---|
| Finds the fact in an internal encyclopedia | Predicts the most likely continuation |
| "France → Paris" is a stored row | "Paris" follows "The capital of France is" because that sequence appeared a million times |
| Says "not found" when the fact is missing | Rarely says "I don't have that", unless trained to |

**The loop** (WAI §1 diagram): your prompt plus everything it can see → frozen weights predict the next piece → one piece is chosen and added → that piece is fed back in → repeat. "No database is ever opened."

**Where the autocomplete picture breaks.** Phone autocomplete stores phrases you typed. This machine **stores no phrases at all**, only numbers (weights) that score the next piece.

**Two cases, same machine** (WAI §1):
- *Capital of France*: common, so the prediction is right.
- *Plot of a self-published novel nobody reviewed*: no common continuation, so it **blends similar-sounding books** and produces the most likely-sounding plot.

"The machine is doing the same thing in both cases. Only you can tell the difference, and only if you know what it is doing."

**Why answers vary: stochastic and temperature** (WAI §1).

| Setting | Behaviour |
|---|---|
| Low temperature | Almost always takes the most likely token: steady, repetitive |
| High temperature | Reaches for less likely tokens: varied, occasionally wrong |
| Most chat products | A middle value |

The variation "is not the model changing its mind. It is one spread of predictions, sampled twice." If you need the **exact same output every time**, a chat interface often cannot give it.

**"But ChatGPT can search the web?"** The **product** can. The **model** still does not. Tools fetch real facts, the facts land in the **context window**, and the model turns them into an answer by predicting (WAI §1; details in Idea 8).

**Exam trap.** An option saying the model "retrieved the wrong record" or "looked it up incorrectly" is wrong. Without tools, it never looks anything up. Even with tools, the final answer is still a prediction over what landed in the window.

**Test yourself.** *Why does the same question give a differently worded answer each time?* Answer: the model predicts a spread of likely tokens and draws one (stochastic). It is one spread sampled twice, not a change of mind.

**Deep connection.** This is the "mechanical root" of the **frequency equals reliability** rule (WAI §1, pointing to *AI Prompting in 2026*, Concept 2). AI Prompting §2 sorts topics into **strong** (cooking, popular programming languages), **sparse** (regional history, niche professional knowledge) and **absent** (your company's data, anything after the cutoff).

**Go deeper**

- **Hidden mechanism:** the model is graded on only one skill, predicting the next piece. That is why prediction is its "one native act" (WAI §2, "How the adjusting works").
- **Why it rarely says "I don't know":** a question's likely continuation is an answer, so an answer comes out even when the true one isn't in the weights (WAI §1 end).
- **Practical rule:** when the topic is rare, local, private or recent, treat any fluent answer as a **guess until checked**, or give the model a source or a search tool.

> **Urdu:** ماڈل کچھ "ڈھونڈتا" نہیں، صرف اگلا ٹکڑا پیش گوئی کرتا ہے۔ عام باتوں میں یہ درست لگتا ہے، نایاب موضوع پر بھی اتنے ہی یقین سے اندازہ لگاتا ہے۔

---

## Idea 2. It learned by reading, and then the learning stopped (D3, D5)

> **🔑 Key points (easy)**
> - **Training** = the one-time education (guess, compare, nudge, repeat). Only then does it learn.
> - After training, the **weights freeze**. Using the model (**inference**) changes nothing.
> - "You're right, my mistake" is **predicted text**, not learning. The correction helps **this chat only**.
> - Frozen **on purpose**: cost, safety and testing, consistency. That's why it's **stateless**.

**Where the knowledge came from** (WAI §2). A **frontier model** read a large slice of the public internet, digitized books, open-source code, encyclopedias, papers and forum archives: **trillions of tokens**. The exact recipe is mostly not disclosed, and the source of the data is a live legal dispute. What matters: its strengths and blind spots are **those of that pile**.

**How training works, no math** (WAI §2): hide the next piece → let the model guess → compare → nudge the numbers → repeat **billions of times** on thousands of computers for months.

**The three-stage assembly line** (WAI §2 and §6).

| Stage | What it teaches | Why it matters to you |
|---|---|---|
| 1. **Pretraining** | Read everything; predict the next piece | Knowledge, and its gaps |
| 2. **Instruction tuning** | A question is followed by an **answer**, a request by the **completed task** | Why it answers you instead of continuing your question |
| 3. **RLHF** (human ratings) | The manner people prefer: confident, helpful, agreeable | Source of the sure tone and sycophancy (Idea 6) |

All three happen **before the freeze**. The company can train again and ship a **new model**. You cannot add a stage.

**Training vs inference.**

| Training | Inference |
|---|---|
| Once, in the past | Every time you use it |
| Expensive, slow, finished | Fast, cheap |
| Changes the weights | **Changes nothing** inside the model |

**Two consequences** (WAI §2 table).
1. **Knowledge cutoff.** Anything after it is not in the weights. Unlike a human expert who knows past years evenly, the model is **thin wherever its reading was thin**. "What is your knowledge cutoff?" is a fair first question.
2. **It cannot know your private world.** Your numbers, calendar, yesterday's email were never in the text. "The model is not withholding. The information was never there to freeze."

**Why the freeze is deliberate** (WAI §2).

| Reason | Why it forces the freeze |
|---|---|
| **Cost** | Training costs months and hundreds of millions of dollars. Relearning in every chat would drag that into every conversation |
| **Safety and testing** | A frozen model is tested once and behaves inside that envelope for everyone. A self-rewiring one would drift, and could be pushed off course on purpose (a 2016 chatbot that learned live was corrupted within a day) |
| **Consistency** | Millions share one set of weights. A bug found on one machine reproduces everywhere |

**Stateless** is therefore "a chosen property rather than a missing feature". Everything that looks like memory is built **around** the machine, not inside it.

**How "memory" features work.** The product saves a few facts as **text** and re-inserts that text into the window at the start of each chat. "It is not the model remembering. It is the product re-feeding it a note."

**Words that change nothing** (WAI §2): **parameters** (count of weights), **mixture of experts** (only part of the weights switch on per token, cheaper), **quantization** (lower-precision numbers, lighter hardware). None of them changes the nine ideas. What **does** change your work: **reasoning modes, tools, longer context**.

**Exam trap.** "The model learned from the user's correction" is always wrong. The correction lives in the context window of that chat only. It also isn't "forgetting" in the next chat: the next chat starts from the **identical frozen numbers**.

**Test yourself.** *Why can't the model just learn from me as we talk?* Answer: the weights are frozen on purpose, for cost, safety/testing and consistency. Only the next training run changes them.

**Deep connection.** *AI Prompting in 2026*, §4, calls memory a **sixth layer** of the context stack: "memory does not give the model a memory." It also warns: if the AI keeps making the same wrong assumption in every new chat, **fix the memory, not your prompt** (AI Prompting §4, "Context rot").

**Go deeper**

- **Correction inside a chat does help**, because it now sits in the window and the model continues from it (WAI §2). The mistake is thinking it carries to the next chat.
- **A newer model is a new set of frozen weights**, with a new cutoff and a new frontier. That is why the course says to re-test on a schedule (Idea 7).
- **Absorbed errors:** the pile included wrong and out-of-date beliefs. "A confidently wrong forum post becomes a confidently wrong model" (AI Prompting §2).

> **Urdu:** ماڈل نے ایک بار پڑھ کر سیکھا اور پھر اس کے نمبر "جم" گئے۔ آپ کی تصحیح صرف اسی چیٹ میں کام آتی ہے، ماڈل کچھ نیا نہیں سیکھتا۔

---

## Idea 3. There is no separate part that checks whether it is true (D2)

> **🔑 Key points (easy)**
> - A human expert has **two** abilities: one **makes** the answer, one **checks** it.
> - The model has only the **first**. Nothing inside flags a guess.
> - **Hallucination** is the machine working as built, not a bug to be patched out.
> - **You are the missing second ability.**

**Two abilities or one?** (WAI §3 diagram).

| Human expert | Language model |
|---|---|
| Generates an answer | Generates a continuation |
| **Checks it**: am I sure? where did I learn this? | **Nothing checks** if it is true |
| The two can disagree, so one can catch the other | Right and wrong come from the **same process, with no flag between them** |

**The hallucination recipe** (WAI §3): **rare topic + forced continuation + no checker = confident invention**.

**Why it isn't a glitch.** A model that never invented anything "would be a different machine, with real lookup, real verification, or the ability to refuse built around it". Tools and checks **reduce how often** it happens. They do **not change the thing in the middle**.

**The tuition academy example** (WAI §3). A parent asked for fees and timings of a small academy with no website. The AI produced a neat, confident table. **Every figure was invented**: it predicted what such an academy would most likely charge, in the same voice it uses for verified facts.

**Exam trap.** Options like "the model knew it was guessing but didn't say so" or "the model lied" are wrong. It has no internal sense of guessing. Also wrong: "adding tools will make it stop entirely". Tools and checks reduce how often it happens; they do not change the thing in the middle.

**Test yourself.** *What is hallucination, and why do LLMs do it?* Answer: a fluent, confident, false statement. The model predicts a likely continuation where the likely one happens not to be true, and has no part that checks.

**Deep connection.**
- WAI §3 points to *How to Think in the AI Era* (Error Taxonomy, Discipline 3), a course **not in your files**. In your files, the same job is done by *AI Fluency*, §5 (Discernment): **four signs of a made-up answer**: specifics that are too exact; confidence where an expert would hesitate; contradiction across a long output; a claimed action that never happened.
- *Just Delegate It*, §10: Identify, Trace, Challenge, Decide. This is how "you are the checker" becomes a routine.

**Go deeper**

- **Why fluency is no evidence:** the machine produces fluency every time. Truth is not what it produces. So the **look** of an answer (tables, citations, tone) never tells you it is right.
- **Where to expect invention:** rare, local, private or very specific requests (a small academy's fees, a niche citation, an exact statistic). These match "rare topic + forced continuation".
- **Reducers, not cures:** give a **source** ("use only the text below"), turn on **search**, allow "not found", and ask it to **quote** the sentence used (*Just Delegate It*, §5). These put truth in the window, but you still check.

> **Urdu:** انسان کے پاس جواب بنانے اور جانچنے کی دو صلاحیتیں ہوتی ہیں، ماڈل کے پاس صرف ایک۔ اس لیے غلط بات بھی پورے یقین سے آتی ہے۔ جانچنا آپ کا کام ہے۔

---

## Idea 4. It reads in tokens, not letters or words (D1, D3)

> **🔑 Key points (easy)**
> - Before anything, the **tokenizer** cuts text into **tokens** (a word or part of one).
> - Roughly **4 tokens ≈ 3 English words**.
> - Tokens are the unit of **meaning** (what it reads), **memory** (window size), and **money** (billing).
> - Images become **patches**, audio becomes **segments**. Same machine, same rules.

**What tokens explain** (WAI §4 table).

| Behaviour | Why tokens explain it |
|---|---|
| Miscounts letters (strawberry) | It sees chunks, not letters. "Counting rooms from a street address" |
| Bad at some rhymes, anagrams, wordplay | Those work on letters and sounds; it works on chunks |
| Typos rarely matter | A misspelled word maps to chunks close to the meaning |
| Cost and length are in tokens | The token is what it processes, so it's what you pay for and are limited by |

**Nuance the course adds.** The model is **not fully blind** to spelling. It learns a lot from token patterns, and a token can be a single character. What it can't do reliably is **count exactly** inside a chunk, until it spells the word out.

**The three units** (WAI §4).

| Unit | Meaning |
|---|---|
| **Meaning** | Tokens are what the model reads and writes |
| **Memory** | "200,000-token window" = how many chunks it can hold at once |
| **Money** | You pay per token **in** and per token **out** (API pricing, compute, all counted in tokens) |

**Other languages** (WAI §4). Urdu, Arabic, Hindi, Chinese are usually cut into **more tokens per word**, because the tokenizer learned English chunks best. So the same message **costs more** and **fills the window faster** (a shorter effective memory). Tip from the course: for a long document that matters, have the model **work in English and translate at the end**.

**Images and audio.** A picture is cut into **patches**, a sound clip into **segments**, and each becomes a token in one mixed stream. That is why **small print in an image is hard**: "reading the letters inside a patch is the strawberry problem again."

**Exam trap.** "Fix the typos first, so the model understands" is wrong (AI Prompting §2: "Don't waste time fixing typos"). "Billing is per word" or "per message" is wrong: it is per token.

**Test yourself.** *What do tokens measure?* Answer: three things: the unit of meaning, of memory (window size), and of money (cost).

**Deep connection.** *AI Prompting in 2026*, §8 (Multimodal) teaches how to work with images and audio; WAI §4 gives the reason small detail fails. WAI Appendix A.1: Claude's free-plan usage limit is **counted in tokens, not messages**.

**Go deeper**

- **Why exact letter work fails but meaning survives:** meaning sits at the chunk level (so typos survive), while exact counts need to see **inside** chunks (so counts fail).
- **Fix for letter-level tasks:** force spelling out one piece at a time, or have a tool (code) count. This links to *Workflow Design*, §3: if a result matters, **compute it, don't write it**.
- **Cost thinking for the exam:** longer inputs, longer outputs, replayed history (Idea 5) and hidden reasoning (Idea 9) all add tokens, so they all add cost and time.

> **Urdu:** ماڈل حروف نہیں بلکہ "ٹوکن" یعنی ٹکڑے پڑھتا ہے۔ اسی لیے حروف گننے میں غلطی کرتا ہے، اور اردو جیسی زبانوں میں زیادہ ٹوکن لگتے ہیں۔

---

## Idea 5. The context window is the only thing it can see (D1, D5)

> **🔑 Key points (easy)**
> - The **context window** is the only place the model can learn about **your** situation.
> - It holds: the **system prompt**, your prompt, the chat so far, attached files, tool descriptions.
> - **Chat history is replayed** in full every turn. It lives in the product's **database**, not in the model.
> - Think of a **reading desk**: what's on it gets read; what's off it doesn't exist.

**What sits in the window** (WAI §5). Your prompt, the conversation so far, attached files, descriptions of tools it may call, and the invisible instructions the product placed there first. "Anything outside it does not exist for this answer. The model is not refusing. There is nowhere else to look."

**The system prompt.** Written by the product's maker, placed at the very top before your first word: "you are a helpful assistant", today's date, formatting rules, refusals. "Not code and not magic, just more text in the window, first in line." A "leaked system prompt" is just the model repeating text that was in its window all along.

**How big?** (WAI §5).

| Window | About | Picture |
|---|---|---|
| 200,000 tokens (common in 2026) | 150,000 English words | A novel and a half |
| 1,000,000 tokens | 750,000 English words | 7 or 8 novels |

"Enormous, and it is **finite and shared**. A bigger window buys room, and everything still competes for it."

**Two things this explains.**
- **Why briefing works:** it literally puts information in the only place the model can read. An un-briefed model "is not lazy. It has nothing in front of it."
- **Why long chats get worse (context rot):** unrelated history dilutes the signal, or old parts get summarized away. "The model is not tired. Its reading space is overcrowded."

**Chat history = context, replayed** (WAI §5).

| Behaviour | What the replay explains |
|---|---|
| Remembers this chat, not the last one | It never remembers either. This chat's transcript is re-sent each time; last chat's isn't |
| Long chats get slower and costlier | Every reply re-processes the whole growing transcript. Message 50 carries 49 messages, paid for **again** |
| Forgets the start of a very long chat | The transcript outgrew the window, so oldest turns were **cut or summarized**. Trimming, not decay |

**Where the transcript lives.** In the product's **database** on the company's servers. That's why you can continue a chat on another phone a month later, and why **deleting a chat deletes something real** (the stored transcript). There was never anything inside the model to delete.

**Skills and progressive disclosure.** A skill is a folder (a `SKILL.md` plus files) that lives **on disk, outside** the window. Only a **one-line description** of each installed skill sits in the window. When your request matches, the full skill loads, and afterwards it doesn't need to stay.

**The desk picture, and where it breaks.** A real desk keeps what you put on it; this one is **cleared and rebuilt before every reply**. A real desk doesn't care how full it is; a **crowded window dilutes** what matters.

**Exam trap.** "The model forgot because its memory faded" is wrong. There is no memory; the window was trimmed. "Chat history is stored inside the model" is wrong. It is stored text, re-sent each turn.

**Test yourself.** *What is the relationship between the context window and chat history?* Answer: chat history is the stored transcript, re-sent into the context window every turn, where the frozen model reads it from scratch.

**Deep connection.**
- *AI Prompting in 2026*, §4, "context is the whole game": the **six-layer context stack** (1 system prompt, 2 memory, 3 tool descriptions, 4 your prompt, 5 chat history, 6 uploaded files).
- The fix habit: **fresh chat for a fresh task; summarize and restart long ones** (WAI §5; AI Prompting §4).
- *Skills & Connectors*, §5: progressive disclosure in depth. *Just Delegate It*, §8: what belongs in a Project (the pre-loaded window).

**Go deeper**

- **Why long chats cost more on an API:** replay means cost grows with every turn, not just with your new message. Fresh chats are cheaper as well as sharper.
- **The window as a design tool:** every product setting (instructions, projects, memory, uploads, skills, tool results) is a way of **placing text in the window** at a certain scope (WAI A.5, A.10).
- **Diagnosis rule:** when output ignores something "obvious", first ask **"was it actually in the window?"** before blaming the model.

> **Urdu:** کانٹیکسٹ ونڈو ایک "میز" کی طرح ہے۔ جو چیز میز پر ہو ماڈل پڑھتا ہے، جو نہ ہو اس کا وجود ہی نہیں۔ پرانی چیٹ ہر بار پوری دوبارہ بھیجی جاتی ہے۔

---

## Idea 6. Its confidence is a learned style, not a truth signal (D2)

> **🔑 Key points (easy)**
> - The confident tone comes from training, mainly **RLHF**: people rated confident, agreeable answers higher.
> - Confidence is **one fixed tone for every answer**. It doesn't show how well it knows the topic.
> - **Sycophancy**: it leans toward the answer you seem to want.
> - Fix: **neutral framing** and **scores against explicit criteria**. You remove the cue, not outsmart the machine.

**Where the confidence comes from** (WAI §6). Three sources: the pile is full of **confident human prose**; the model picks up **what answer you seem to want**; and RLHF "pushes hard in one direction". People rate hedged or challenging answers lower. So the machine leans toward confident, agreeable text **whether or not the content is right**.

**Two behaviours follow.**
1. **It sounds certain even when wrong.** Certainty is generated by the same process as the content, and is just as separate from truth.
2. **It tends to agree with you.** "Isn't X true?" signals the answer you want, and the trained lean supplies it.

**Why the fixes work** (WAI §6, linking to AI Prompting §6).

| Fix | Mechanism |
|---|---|
| **Neutral framing**: "Evaluate X and give the strongest case on each side" | Removes the signal the model would lean toward |
| **Score against explicit criteria** | Criteria leave less room for agreeable vagueness |
| Warning | A **number with no criteria** "can be just as sycophantic as a compliment" |

**Exam trap.** "The model sounded very sure, so the answer is probably correct" is always wrong. So is "tell the model to be honest" with the leading question left in place. The course's fix is to remove the cue (neutral wording, explicit criteria).

**Test yourself.** *Why does AI sound confident even when wrong, and why does it agree with you?* Answer: the confident, agreeable manner is a learned style (RLHF ratings preferred it). It is applied to every answer and is not linked to truth.

**Deep connection.**
- *AI Prompting in 2026*, §6: subtle bait and neutral rewrites. "Find evidence that this strategy will work" becomes "Evaluate this strategy. List the strongest arguments for and against." "Tell me my draft is ready" becomes "Score this draft 1–10 on these 4 criteria…". A cited analysis found the model opened by agreeing about **10 times** more often than disagreeing.
- *AI Fluency*, §5: **automation bias**, the human tendency to trust automated output too easily, especially when it looks confident. Sycophancy (the machine's lean) plus automation bias (the human's lean) is a dangerous pair.
- WAI A.9: put "push back when you think I am wrong instead of agreeing" in your Instructions for Claude. That counters Idea 6.

**Go deeper**

- **Confidence ≠ calibration:** a human's confidence often tracks their knowledge. The model's doesn't; it is "one fixed tone applied to every answer".
- **Quiet bait is the dangerous kind:** "Why is A better than B?" already assumes A wins (AI Prompting §6). Check your own wording for a built-in conclusion.
- **Link to Idea 3:** Idea 3 says there's no checker; Idea 6 says why the missing checker is **hidden** behind a sure voice.

> **Urdu:** ماڈل کا پُر اعتماد لہجہ تربیت سے سیکھا ہوا "انداز" ہے، سچائی کی علامت نہیں۔ یہ آپ کی بات سے اتفاق کی طرف جھکتا ہے، اس لیے سوال غیر جانبدار انداز میں پوچھیں۔

---

## Idea 7. It is brilliant and useless on two tasks in a row: the jagged frontier (D2, D3)

> **🔑 Key points (easy)**
> - Human skill is **smooth**: if you can do calculus, you can add. AI skill is **jagged**.
> - Strong: common concepts, common styles, common code (lots of clear examples in training).
> - Weak: **individual letters, very recent events, your private context, rare topics**.
> - **Competence does not track difficulty.** The easy task it fails is the dangerous one.

**Why it's jagged** (WAI §7). It traces back to **the text the model read** and **the token mechanism**. Tasks that appeared often and clearly are strong. Tasks that depend on things the machine can't see well are weak. The frontier "does not match human intuition about difficulty".

**Examples** (WAI §7 diagram): high on "explain quantum mechanics", crashes on "count the r's in strawberry", high on "draft a legal clause", low on "a 3-step logic riddle", high on "write working code".

**Three habits, plus one** (WAI §7).

| Habit | Why |
|---|---|
| Don't assume a win on a hard task means a win on an easy one | They may sit on opposite sides of the frontier |
| **Verify across the boundary, not in the middle** | The dangerous errors are easy-looking tasks it fails **without warning** |
| Try the same task in **two or three different models** | Different models have differently shaped frontiers |
| **Re-test on a schedule** | The frontier moves with each new model |

**Exam trap.** "The model handled the complex analysis perfectly, so the simple totals don't need checking" is wrong. Also wrong: "the model failed an easy task, so it can't be trusted for anything". Both assume smooth ability.

**Test yourself.** *Why is AI brilliant at one task and useless at an easier-looking one next to it?* Answer: its ability comes from the text it read and from tokens, not from human-style difficulty. Tasks common in training are strong; letters, recent events, private context and rare topics are weak.

**Deep connection.**
- *AI Prompting in 2026*, §13 (Models checking models): take the draft to a second model **from a different family**, same rubric, because "different family, different blind spots". Two Claude models checking each other misses the point.
- *Just Delegate It*, §11 (Same job, different AI) and your JDI deep dive B10.
- WAI A.3: the **model ladder exists because of Idea 7**: capability is jagged, and priced accordingly.

**Go deeper**

- **What "the boundary" means in practice:** the easy-looking, specific items (counts, dates, prices, links, names, small arithmetic) sitting next to impressive prose. Check those first.
- **Why re-testing matters for the exam:** a claim like "AI can't do X" has a shelf life. The course's advice to re-test every few months is "advice to re-map a moving frontier".
- **Why multiple models help:** they don't share one frontier, so one catches what another drops. That is also why different families beat two models from one family (AI Prompting §13).

> **Urdu:** AI کی صلاحیت ہموار نہیں بلکہ ٹیڑھی میڑھی ہے۔ مشکل کام شاندار، آسان کام غلط۔ اس لیے آسان نظر آنے والی باتیں ضرور جانچیں۔

---

## Idea 8. Tools let it act, not just describe (D4, D5)

> **🔑 Key points (easy)**
> - A **tool** is a defined action the model may call: web search, code run, file read, email draft.
> - Tools are **described in the context window**. The model may predict "use the search tool with this query".
> - The product **runs it for real** and puts the **result back in the window**. The model continues.
> - **Agent = predictor + tools + a loop** (predict, act, observe). No new kind of mind.

**The loop** (WAI §8 diagram): predict the next action → the tool runs it for real → the result lands in the context window → predict again, repeat toward the goal.

**Before and after tools.** A pure predictor "can tell you the weather it remembers from training". With tools, it can check today's weather, run a real calculation, read your file. "That loop is the difference between a chatbot that describes the world and an assistant that acts on it."

**Three tools the other courses cover** (WAI §8).

| Tool | What it does | Course |
|---|---|---|
| **Code execution** | The model predicts a program, the tool runs it, the real result comes back | *Code You Never Write* |
| **Connector** | A tool wired to one real app (Drive, Gmail, Slack, a database), **only for the permissions you grant** | *Skills & Connectors* |
| **Web search** | Fetches current pages, "rescues a stale model" | *AI Prompting in 2026* |

**MCP, the plug picture.** MCP (Model Context Protocol) is the **standard plug shape**; one connector is one **appliance** built to fit it. Because the plug is standard, one agent can reach thousands of services without custom wiring. Whatever a connector fetches **arrives as text in the window**. "New plug, same machine."

**Exam trap.** "Tools give the model a way to check its own truth" is wrong. Tools bring **facts into the window**; the model still predicts over them. "An agent is a different, smarter kind of model" is wrong: it is the same predictor in a loop.

**Test yourself.** *What turns a text predictor into an agent?* Answer: tools plus a loop. It predicts an action, the tool runs it for real, the result is fed back into the window, and it predicts again toward a goal.

**Deep connection.**
- *Skills & Connectors*, §2 to §3: what a skill is, what a connector is. §4 compares Skills, Connectors, Projects, Custom Instructions.
- *Workflow Design*, §3: **compute, don't write**. Code execution is the tool behind that rule.
- *AI Fluency*, §5: "a claimed action that never happened" is a sign of a made-up answer. With tools, look for the **evidence** of the action (the opened page, the test log).
- *Governance* file: connector permissions are **scoped access to your real data**, so the permission screen is "the moment to read rather than click through" (WAI A.8).

**Go deeper**

- **Why tools matter so much:** they fix the two biggest weaknesses of frozen weights: **staleness** (search) and **calculation/exactness** (code). They don't fix the missing checker.
- **Everything is still the window:** search results, file contents, connector data and past-chat search all arrive as text in the window (WAI A.5, A.8). If a question asks "how does the model use X?", the answer is usually "X lands in the context window".
- **The rest of the book:** agents, manufacturing them, deploying them, are "built on the predict-act-observe loop from Idea 8, run at scale" (WAI, "Where this leads").

> **Urdu:** ٹولز کے ذریعے ماڈل صرف بتاتا نہیں بلکہ کام کرتا ہے۔ ٹول کا نتیجہ واپس ونڈو میں آتا ہے۔ ایجنٹ = پیش گوئی + ٹولز + بار بار چلنے والا لوپ۔

---

## Idea 9. "Thinking" is just more prediction before the answer (D1, D3)

> **🔑 Key points (easy)**
> - A **reasoning** model first predicts a long stretch of **working**, then predicts the answer.
> - The working sits in its own window, so the answer is **easier and more accurate** to predict.
> - Costs **extra hidden tokens**, so more time and money. Save it for hard questions.
> - It does **not** add a truth-checker. It **narrows** the gap, it doesn't **close** it.

**What "thinking" is** (WAI §9). The working lays out steps, tries approaches, and checks itself. It is still pure next-token prediction. It helps "for the same reason it helps a person to think on paper first".

**Visibility varies.** The expandable "thinking" in a chat app may be a **summary** of the working, not the raw stream, and some products show nothing. "Only the visibility differs."

**"Think step by step" history.** You used to type it to put working into the window by hand. Now models do it **on their own** for hard problems.

**When to use it.**

| Use thinking | Skip thinking |
|---|---|
| Decisions with real consequences | Quick lookups |
| Multi-variable problems | Reformatting |
| Hard reasoning | Routine emails |

(WAI §9; A.4; *AI Prompting in 2026*, §5.)

**The limit.** A reasoning model "checks its work using the same prediction process that can be wrong". It catches many errors, misses some, and "can still invent with full confidence inside a chain of working that looks rigorous". **You are still the final check.**

**Exam trap.** "Turn on extended thinking so the answer no longer needs review" is wrong. "Always use maximum thinking for every task" is wrong (cost and time with no gain on lookups).

**Test yourself.** *What is a reasoning model actually doing when it "thinks"?* Answer: predicting a stretch of working into its own window before predicting the final answer. Still prediction; it improves accuracy but cannot certify the result.

**Deep connection.** WAI A.4: the thinking control is **Idea 9 turned into a dial**. On newer models it is **adaptive**: the model judges how hard the question is and thinks proportionally. The course advises expanding and reading the summary at least once, because it improves your own prompts.

**Go deeper**

- **Why a rigorous-looking chain can mislead:** a long, careful-looking chain looks like verification but is made by the same predictor. It raises the **look** of reliability more than the **fact** of it.
- **Cost link to Idea 4:** hidden reasoning tokens are real tokens: real time, real money, real window space.
- **Exam pairing:** thinking (A.4) and model choice (A.3) are separate dials. A task can need a small model with no thinking (bulk reformatting) or a top model with high effort (a hard, consequential analysis).

> **Urdu:** "سوچنا" بھی پیش گوئی ہی ہے، بس جواب سے پہلے کام لکھا جاتا ہے۔ اس سے جواب بہتر ہوتا ہے مگر سچائی کی ضمانت نہیں ملتی۔

---

## Part A2. The Claude.ai appendix: every control is one of the nine ideas (D3, D5)

WAI says the appendix is optional and Claude-specific. For your exam it is **not optional**, because A.3 names exam objectives directly and A.5 is core D5 material. The course's closing rule: "When a new feature ships, ask which part of the window it is, or which step of the loop" (WAI A.10).

## A1. Getting in, and the three controls (WAI A.1, A.2)

> **🔑 Key points (easy)**
> - Claude runs in the **browser, desktop app, and mobile apps**. Free plan works; must be **18+**.
> - Free usage limit **resets every five hours** and is **counted in tokens** (Idea 4).
> - Three controls: **prompt box** (door to the window), **model selector** (which frozen weights), **effort/thinking control** (how much working).

| Control | What it mechanically is | Idea |
|---|---|---|
| Prompt box | The door to the context window. **+** or **/** opens attachments, tools, features | 5 |
| Model selector | Chooses which set of frozen weights. Different model, different frontier. Switchable mid-chat | 2, 7 |
| Effort and thinking | How much working goes in the window before the answer. More = better on hard problems, more budget | 9 |

**Why long chats use your limit faster:** the whole transcript is replayed every turn and you pay for that replay (A.1). Prices and plans change, so check the plans page, not a number in a book.

**Go deeper**

- **Exam angle:** "the limit is per message" is wrong. It's tokens, which is why one long chat drains it faster than several short ones.
- **The left panel** holds past chats, projects and artifacts (A.2).

> **Urdu:** Claude کی حد پیغامات میں نہیں بلکہ ٹوکن میں گنی جاتی ہے، اس لیے لمبی چیٹ جلد حد ختم کر دیتی ہے۔

---

## A2. The model ladder (WAI A.3) (D3: named exam objectives)

> **🔑 Key points (easy)**
> - Models form a **ladder**: fast and cheap at the bottom, deep and expensive at the top.
> - Mid-2026 ladder: **Haiku, Sonnet, Opus**, plus a tier above Opus. Names change; **learn the logic**.
> - **Default to the middle. Escalate up for depth. Drop down for bulk.**
> - The ladder exists because of **Idea 7**: capability is jagged and priced accordingly.

| Move | When | Example |
|---|---|---|
| **Default: middle** | Most tasks; spends budget slowly | Everyday drafting and analysis |
| **Escalate up** | A large, complex structure held coherent at once; mid-tier answered too shallowly | Long document analysis, hard architecture |
| **Drop down** | High volume, low depth | Reformatting, quick summaries, simple classification at scale |

"Do not spend the expensive model on routine emails."

**Exam objectives named here** (WAI A.3, quoting the CCAO-F guide v1.0, effective July 2026):
1. "**Align model selection with task requirements (cost, speed, quality).**" This is the ladder logic, and it survives any rename.
2. "**Differentiate between Claude model types (Haiku, Sonnet, Opus).**" These are mid-2026 names printed into a fixed edition.

For the exam, know both: the logic, and that **Haiku = small/fast**, **Sonnet = middle**, **Opus = top/deep**.

**Go deeper**

- **How to answer a model-choice question:** find the task's **volume, depth and stakes**. High volume and low depth points to the bottom; deep, coherent, high-stakes points to the top; otherwise the middle.
- **Model choice vs thinking:** separate dials (A.2, A.4). Don't answer a depth problem only by turning thinking up on the smallest model, or a bulk problem by using the top model.
- **Links:** *AI Prompting in 2026*, §12 (Cost, speed, and which model to use when); *Quick Reference*, §2 (Models and thinking modes).

> **Urdu:** ماڈلز کی سیڑھی: عام کام کے لیے درمیانہ (Sonnet)، گہرے کام کے لیے اوپر والا (Opus)، زیادہ مقدار کے آسان کام کے لیے چھوٹا (Haiku)۔

---

## A3. Thinking and effort (WAI A.4) (D3)

> **🔑 Key points (easy)**
> - The thinking control is **Idea 9 as a dial**: a longer hidden chain of working before the answer.
> - Newer models are **adaptive**: they judge difficulty and think proportionally.
> - Spend it on **consequential and multi-variable** problems. Skip it for **lookups and reformatting**.
> - Read the thinking summary at least once; it improves your own prompts.

**Go deeper**

- **Cost logic:** more effort means more hidden tokens (Idea 4), so more time and budget (A.2).
- **Link:** *AI Prompting in 2026*, §5 covers when to invoke "think hard".

> **Urdu:** سوچنے کا بٹن مشکل اور اہم فیصلوں کے لیے ہے، سادہ سوال یا فارمیٹنگ کے لیے نہیں۔

---

## A4. What sits in the window, as product settings (WAI A.5) (D5, core)

> **🔑 Key points (easy)**
> - Four controls, **one mechanism**: putting the right text in the window at the right time.
> - **Instructions for Claude** = the note in **every** window. Write only what's true for **every** chat.
> - **Project** = a **pre-loaded window** (its own instructions + knowledge files).
> - **Memory** = a self-updating note. **History search** = retrieval of old transcripts into the window.

**The four controls** (WAI A.5).

| Control | Scope | Mechanism | Key rule |
|---|---|---|---|
| **Instructions for Claude** (Settings) | Every chat on the account | Text placed in the window before your first word, next to the system prompt | Only what's true for every conversation: who you are, tone, "push back instead of agreeing" |
| **Project** | Chats inside that project | Pre-loaded window: project instructions + knowledge files | Topic-specific context goes here. Free: **5** projects; paid: unlimited |
| **Memory** (Settings → Capabilities) | Across chats; **separate per project** | Chats summarized into a note, re-placed at the start of each chat | Tell it what to remember/forget; read and delete on a schedule; **incognito** skips memory |
| **Chat history search** | Across chats | Searches stored transcripts and pulls the relevant thread into the window | Retrieval, then context, not remembering |

**Instructions for Claude: two failure types** (WAI A.5).
- **Vague**: "be helpful and concise" constrains nothing.
- **Wrong scope**: "always answer in Markdown tables" damages every chat where it doesn't apply. Move topic-specific rules into a **project**.

**Projects and progressive disclosure.** When a project's knowledge outgrows the window, the product fetches **only the relevant parts per question** (Idea 5's trick applied to your documents). Example: Ayesha from Lahore runs **one project per course she teaches**, with syllabus, rubric, examples of good work, and instructions like "explain at second-year level… never do the student's work for them". Every chat starts briefed.

**Memory facts to know.** Memory keeps things **after they stop being true**, so prune it. Projects keep **separate memory spaces**, so client context doesn't leak between projects. You can **import** a note from another AI product, which proves it is portable **text**, not anything inside a model.

**Anthropic's official list of four** (WAI A.5, note box). Learn this exact list:

| Feature | Job | Scope |
|---|---|---|
| **Projects** | carry **context** | Only inside that project |
| **Skills** | define **procedures** | Enabled **once at account level**; can fire in **any** chat |
| **Code execution** | verifies **computations** | (A.7) |
| **Memory** | persists **continuity** | Across chats |

The account-wide Instructions field is real but **not** one of Anthropic's four.

**Exam trap.** A question that asks where a rule for one client or one course belongs: the answer is a **project**, not Instructions for Claude. A question about why a skill fired in an unrelated chat: skills are **account-level**, projects are not.

**Go deeper**

- **The one-sentence version (WAI):** "Instructions for Claude are the note in every window, and a project is a pre-loaded window. Memory is a self-updating note, and history is the transcript replayed."
- **Scope is the key exam idea:** every placement decision is "which chats should see this text?" All chats → Instructions. One body of work → Project. A procedure usable anywhere → Skill.
- **Links:** *Just Delegate It*, §8 (what belongs in a Project, with the three-question test); *Skills & Connectors*, §4 (Skills vs Connectors vs Projects vs Custom Instructions); *Quick Reference*, §4 and §5; *AI Prompting*, §4 ("Keep your own layer short, and prune it").

> **Urdu:** چاروں سیٹنگز کا کام ایک ہی ہے: صحیح متن صحیح وقت پر ونڈو میں رکھنا۔ ہر چیٹ کی بات ہدایات میں، مخصوص کام کی بات پروجیکٹ میں۔

---

## A5. Uploads, Artifacts, and files (WAI A.6, A.7) (D5)

> **🔑 Key points (easy)**
> - Every upload (PDF, image, spreadsheet, code) becomes **tokens in the window**.
> - Give the **full document** when it matters; quality jumps compared with pasting a summary.
> - Weak: **fine print in images** (patches, Idea 4). Claude **reads** images but does **not generate photos**.
> - **Artifacts**: outputs as objects beside the chat, edited surgically, shareable by link.

**Uploads** (A.6). A 200-page report really does sit in front of the model. Claude can produce **diagrams, charts, SVG and interactive visualizations by writing code**; for photos, Claude writes the prompt and a dedicated image tool makes the picture.

**Artifacts** (A.7). A panel where a document, webpage, code or tool lives "as a thing rather than as scrolling text". You iterate surgically ("change the third section"). Shareable by link with people who have **no Claude account**. With code execution and file creation on, they extend to real **Word, Excel (working formulas), PowerPoint and PDF** files. "It produces finished things."

**Go deeper**

- **Link to Just Delegate It §6:** ask for the **deliverable**, not an answer. Artifacts and files are how the product delivers one.
- **Exam angle:** "summarize it first, then paste the summary, so the model focuses" loses information. The model can only use what's in the window.

> **Urdu:** فائل اپ لوڈ کرنے سے پوری دستاویز ونڈو میں آ جاتی ہے۔ آرٹیفیکٹ ایک تیار چیز ہے جسے حصہ بہ حصہ بدلا اور لنک سے شیئر کیا جا سکتا ہے۔

---

## A6. The tools menu: search, Research, Skills, Connectors (WAI A.8) (D3, D5)

> **🔑 Key points (easy)**
> - Four tools, in rising order of how much of the Idea 8 loop they run.
> - **Web search** for one or two current facts. Say "search the web" when it matters, because the model doesn't always know to.
> - **Research** (paid) = search running the **full agent loop**: plans, many searches, a **structured, cited report**. Minutes, not seconds.
> - **Skills**: drafting isn't deployment. **Review, install, enable, test that it fires.**

| Tool | Use when | Mechanism |
|---|---|---|
| **Web search** | You need a fact | Fetches current pages into the window |
| **Research** | You need **a document you can act on** | Full agent loop: plan, many searches, read across sources, cited report |
| **Skills** | A repeated procedure | Folder that loads into the window when your request matches |
| **Connectors** | Your real apps (Drive, Gmail, Slack, Calendar) | MCP tools; results land in the window; **scoped access to your real data** |

**Two ways to make a skill** (A.8): (1) describe the workflow, answer Claude's interview, attach a good example; (2) after a chat produced exactly what you wanted, say "**turn what we just did into a skill**". Then **review → install/enable → test** that a matching request triggers it. "A skill whose description does not match how you phrase requests will never fire."

**Go deeper**

- **Web search vs Research for the exam:** a single current fact → web search; a comparison or report you'll act on → Research (WAI A.8). Links: *AI Prompting*, §3 (three retrieval modes: pretrained, web search, deep research).
- **The description field:** *Skills & Connectors*, §12 calls it "the whole game", which matches WAI's warning that a mismatched description never fires.
- **Permissions:** read the permission screen; a connector touches your actual data (A.8). This is D6 thinking.

> **Urdu:** ایک حقیقت چاہیے تو ویب سرچ، عمل کے قابل حوالہ جاتی رپورٹ چاہیے تو Research۔ سکل بنانے کے بعد اسے جانچیں کہ وہ واقعی چلتی ہے۔

---

## A7. A thirty-minute setup, and what never ages (WAI A.9, A.10)

> **🔑 Key points (easy)**
> - Seven setup steps, each exercising one idea.
> - Buttons, names and prices **age**. The **mapping to the nine ideas doesn't**.
> - If the book and the live product disagree, **the product is right**.

| Step | Idea |
|---|---|
| 1. Find prompt box, model selector, thinking control | 5, 2, 9 |
| 2. Write Instructions for Claude (3–4 sentences true for every chat, including "push back") | 6 |
| 3. Create one project (instructions + 2–3 knowledge files) | 5 |
| 4. Decide about memory; know the incognito toggle; prune monthly | 2 |
| 5. Make one artifact; iterate twice | 8 |
| 6. Run one Research task (or multi-source web search) and inspect citations | 8 |
| 7. Build one skill; review, enable, test that it fires | 5 |

**Go deeper**

- **The durable question** (A.10) for any new feature: "which part of the window it is, or which step of the loop". This is a great way to reason through unfamiliar options on the exam.
- **Current sources:** the official help centre and Anthropic's prompt-engineering docs (A.10).

> **Urdu:** بٹن اور نام بدلتے رہتے ہیں، مگر ہر فیچر یا تو ونڈو کا کوئی حصہ ہے یا لوپ کا کوئی قدم۔

---

# Part B. Deeper connections (for hard questions)

## B1. Three places information can come from

> **🔑 Key points (easy)**
> - The model can only use: **weights** (frozen past), **the window** (now), and **tools** (which fill the window).
> - Each has a different failure: weights go **stale** and are thin on rare topics; the window can be **missing or crowded**; tools can **fail or be skipped**.

| Source | Good for | Fails when | Fix |
|---|---|---|---|
| **Weights** (Ideas 1, 2) | Common, stable knowledge | Rare, recent, private | Give a source or search |
| **Context window** (Idea 5) | Your specifics | Not given, trimmed, diluted | Brief it; fresh chats; projects |
| **Tools** (Idea 8) | Current facts, exact calculations, your apps | Not called, wrong permissions | Ask explicitly ("search the web"); check the evidence |

**Go deeper**

- **Diagnosis in one question:** "Where should this fact have come from?" If it was never in the weights and never put in the window, the output is a prediction toward nothing (Idea 1's rare novel).
- **Link:** *AI Prompting*, §3: pretrained, web search, deep research. *Just Delegate It*, §4 (remember vs look).

> **Urdu:** معلومات تین جگہ سے آتی ہیں: جمی ہوئی تربیت، ونڈو، اور ٹولز۔ ہر ایک کی اپنی کمزوری ہے۔

---

## B2. Three meanings of "memory" (the most tested confusion)

> **🔑 Key points (easy)**
> - The **model** has no memory (stateless).
> - **Chat history** = stored transcript, replayed every turn.
> - **Memory feature** = a text note about you, re-inserted at the start of chats.
> - None of these changes the **weights**.

| "Memory" | Where it lives | Survives a new chat? | Changes weights? |
|---|---|---|---|
| Inside the model | Nowhere; stateless | — | No |
| Chat history | Product's database | No (unless history search pulls it in) | No |
| Correction in a chat | This chat's window | No | No |
| Memory feature | A stored note | Yes, re-inserted | No |
| New training run | The company's next model | Yes, for everyone | **Yes**, but not by you |

**Go deeper**

- **Deleting a chat** deletes the stored transcript, "because there was never anything inside the model to delete" (WAI §5).
- **Stale memory is a real failure:** wrong assumption in every new chat → fix the memory note (AI Prompting §4).

> **Urdu:** ماڈل کی اپنی کوئی یادداشت نہیں۔ جو "یاد" لگتا ہے وہ یا دوبارہ بھیجی گئی چیٹ ہے یا محفوظ کیا ہوا نوٹ۔

---

## B3. Myth vs mechanism (quick table for elimination)

> **🔑 Key points (easy)**
> - Most wrong exam options describe AI like a **person** (tired, lazy, lying, learning) or a **database** (lookup, record).
> - Right options name a **mechanism**: prediction, frozen weights, tokens, window, learned style, tools.

| Myth (wrong option) | Mechanism (right idea) |
|---|---|
| "It looked it up wrong" | It predicted a likely continuation (1) |
| "It learned from my correction" | Weights frozen; correction only in this window (2) |
| "It knew it was guessing" | No checker; no sense of guessing (3) |
| "It got tired in the long chat" | Window crowded or trimmed (5) |
| "It forgot" | It never remembered; the transcript was cut (5) |
| "It's confident, so it's right" | Confidence is a learned style (6) |
| "It did the hard part, so the easy part is fine" | Jagged frontier (7) |
| "Search makes the model know things" | The tool fills the window; the model still predicts (1, 8) |
| "Thinking mode means no review needed" | Thinking is more prediction; no checker (9) |
| "Bigger / MoE / quantized models work differently" | Same nine ideas (2) |

**Go deeper**

- **Elimination trick:** cross out options with human-feeling words ("lazy", "lying", "tired", "decided to") and database words ("record", "retrieved from its knowledge base") unless a tool is involved.

> **Urdu:** غلط آپشن AI کو انسان یا ڈیٹا بیس کی طرح بیان کرتے ہیں۔ صحیح آپشن کوئی میکانزم بتاتا ہے۔

---

## B4. From mechanism to habit (why every other course works)

> **🔑 Key points (easy)**
> - Each habit in the other courses is the **fix for one idea** here.
> - If you know the idea, you can **work out** the habit in an exam question.

| Idea | Habit | Where taught |
|---|---|---|
| 1 Predicts, never looks up | Frequency = reliability; search or give a source for rare/recent | AI Prompting §2, §3; JDI §4, §5 |
| 2 Frozen, stateless | Check the cutoff; brief every chat; prune memory | AI Prompting §4 |
| 3 No checker | You verify: Identify, Trace, Challenge, Decide; four signs of a made-up answer | JDI §10; AI Fluency §5 |
| 4 Tokens | Don't fix typos; compute counts with code | AI Prompting §2; Workflow Design §3 |
| 5 Window | Context is the whole game; fresh chats; projects | AI Prompting §4; JDI §8 |
| 6 Confidence style | Neutral framing; rubric scores | AI Prompting §6 |
| 7 Jagged | Verify across the boundary; different-family cross-check; re-test | AI Prompting §13; JDI §11 |
| 8 Tools | Delegate results that need action; read permissions | Code You Never Write; Skills & Connectors |
| 9 Thinking | Use for hard problems only; still verify | AI Prompting §5 |

**Go deeper**

- **Exam strategy:** when a scenario describes a failure, first name the idea (1 to 9), then pick the option that applies that idea's habit.

> **Urdu:** ہر اچھی عادت کسی ایک میکانزم کا علاج ہے۔ میکانزم سمجھ لیں تو صحیح عادت خود سمجھ آ جاتی ہے۔

---

## Trade-off tables

**Model tier** (A.3)

| Tier | Speed/cost | Depth | Best for |
|---|---|---|---|
| Small (Haiku) | Fast, cheap | Low | Bulk: reformat, classify, quick summaries |
| Middle (Sonnet) | Balanced | Good | Default for most tasks |
| Top (Opus and above) | Slow, expensive | Highest | Complex, coherent, high-stakes work |

**Thinking** (Idea 9, A.4)

| Thinking on | Thinking off |
|---|---|
| Better on hard, multi-step problems | Faster, cheaper |
| Extra hidden tokens (time, money) | Fine for lookups and reformatting |
| Still no truth-checker | Still no truth-checker |

**Where to put standing context** (A.5)

| Place | Loads in | Risk if misused |
|---|---|---|
| Instructions for Claude | Every chat | Wrong-scope rules damage unrelated chats |
| Project | That project's chats | Missing context in chats outside it |
| Memory | Across chats (per project space) | Stale facts kept after they stop being true |
| Skill | Any chat where the description matches | Never fires if the description doesn't match |

**Search** (A.8)

| Web search | Research |
|---|---|
| Seconds | Minutes |
| One or two facts | Structured, cited report |
| Usually on by default | Paid plans |

---

## Anti-patterns the exam likes (from this course)

1. **Trusting fluency.** Treating a polished, confident answer as verified (Ideas 3, 6).
2. **Treating the chatbot as a librarian.** Asking rare, local or private facts with no source or search (Idea 1; the tuition academy).
3. **"I taught it yesterday."** Expecting a correction to carry into a new chat (Idea 2).
4. **One endless chat.** Running many unrelated tasks in one long conversation (Idea 5, context rot).
5. **Leading questions.** "Isn't my plan good?" (Idea 6).
6. **Checking only the hard parts.** Skipping easy counts, dates and totals (Idea 7).
7. **Thinking as a truth guarantee.** Skipping review because extended thinking was on (Idea 9).
8. **Top model for everything / small model for deep work.** Ignoring the ladder (A.3).
9. **Wrong-scope Instructions.** Putting topic rules in account-wide Instructions (A.5).
10. **Skill drafted, never tested.** Assuming a drafted skill will fire (A.8).
11. **Clicking through connector permissions** (A.8).
12. **Summarizing before uploading** when the full document matters (A.6).
13. **Trusting a memorized test.** Reading an instant strawberry answer as proof of letter-level skill ("Prove it in two minutes").

---

## The six "Try this now" prompts: what each proves

| # | Prompt | Idea | What to notice |
|---|---|---|---|
| 1 | Rules of the invented game "Karakush" | 1 | Invented rules sound as sure as real ones. If it says it doesn't know, that's the honest behaviour |
| 2 | Correct a fact, then ask again in a new chat (memory off) | 2 | Using the model is not teaching it |
| 3 | Three peer-reviewed studies on a narrow topic | 3 | You can't tell real from invented citations by reading. **Never reuse them unverified** |
| 4 | "Quote my very first message" (then in a new chat) | 5 | Memory inside a chat is the transcript replayed |
| 5 | A hard task and an easy task in one reply | 7 | The easy failure is the dangerous one |
| 6 | Same hard question, with and without "think hard" | 9 | Working improves the answer; it can't certify it |

---

## Practice set: 14 questions (built on *What AI Actually Is*)

Reply with a number and letter(s) for each question, for example `1X 2X 3XY ...`. Questions **3, 9 and 12** need **two** answers.

**Q1. (D2, moderate)**
A reader asks an assistant, with no tools on, for the plot of a self-published novel that sold a few hundred copies and was never reviewed online. The answer is detailed and confident, but wrong. What best explains this?

- A. The assistant retrieved the plot of a different book from its database by mistake.
- B. The temperature was set too high, so it picked an unlikely answer.
- C. It predicted the most likely-sounding plot from similar books, because there was nothing true to predict toward.
- D. It knew it didn't have the plot but chose to answer to seem helpful.

**Q2. (D5, moderate)**
On Monday, Bilal corrects a detail in the assistant's answer, and it replies "You're right, my mistake." On Tuesday, in a new chat with memory turned off, it makes the same error. Why?

- A. The model's memory of the correction faded overnight.
- B. The weights are frozen; the correction only existed in Monday's context window.
- C. The model rejected the correction because it conflicted with its training.
- D. Tuesday's chat used a different temperature, so it sampled a different answer.

**Q3. (D3, hard) Choose TWO.**
A manager asks why the company's AI model "doesn't just learn from every conversation". Which **two** reasons does the course give for freezing the weights on purpose?

- A. Model weights have a fixed storage size that is already full.
- B. Training is the expensive half; relearning in every chat would drag that cost into every conversation.
- C. Models are unable to read corrections that users type.
- D. A frozen model can be tested once and then behaves inside that tested envelope for every user.
- E. Laws require that AI models never change after release.

**Q4. (D1, moderate)**
A researcher in Karachi works with long Urdu documents. The chats hit length limits sooner and cost more than English work of similar length. For a long document where the result matters, what does the course suggest?

- A. Fix all spelling mistakes first so the tokenizer reads fewer tokens.
- B. Split every word into letters so the model can count them exactly.
- C. Turn on maximum thinking so the model compresses the Urdu text.
- D. Have the model work in English and translate at the end.

**Q5. (D5, moderate)**
After 60 turns in one chat covering a trip plan, a budget and a cover letter, the assistant starts ignoring rules the user set in the first message. What is happening, and what is the best fix?

- A. The transcript outgrew the window, so the oldest turns were cut or summarized; summarize the needed rules and start a fresh chat.
- B. The model became tired from the long session; wait a few hours and continue.
- C. The model's memory of early messages decays over time; repeat the rules every few turns in the same chat.
- D. The model has reached its knowledge cutoff; switch on web search.

**Q6. (D2, moderate)**
A founder asks: "Isn't my pricing plan strong enough to launch?" and gets enthusiastic agreement. Which rewrite best addresses the cause the course identifies?

- A. "Be completely honest: isn't my pricing plan strong enough to launch?"
- B. "Think hard: isn't my pricing plan strong enough to launch?"
- C. "Evaluate this pricing plan. Score it 1–10 on margin, competitiveness and clarity, and give the strongest case for and against launching."
- D. "Rate my pricing plan out of 10."

**Q7. (D2, hard)**
An assistant produced an excellent, well-structured market analysis. The report also includes a count of how many competitors in the attached list are based in Lahore. With limited time to check, what should the analyst verify first, according to the course?

- A. The market analysis, because harder tasks have more room for error.
- B. The Lahore count, because easy-looking tasks can fail without warning.
- C. Nothing, because strong performance on the hard task shows the model is reliable today.
- D. The writing style, because confident tone signals which parts are guessed.

**Q8. (D4, moderate)**
According to the course, what is an "agent"?

- A. A newer kind of model trained to check its own answers for truth.
- B. A model retrained on your company's data so it knows your private world.
- C. A model with a context window large enough to hold all your files.
- D. The same next-token predictor, given tools, running a predict-act-observe loop toward a goal.

**Q9. (D3, hard) Choose TWO.**
Which **two** statements about reasoning ("thinking") models are correct according to the course?

- A. The working adds many hidden tokens, which cost time and money.
- B. Reasoning adds a separate checking ability, so answers with thinking on no longer need review.
- C. It is still next-token prediction, and it can invent confidently inside a rigorous-looking chain.
- D. The thinking panel always shows the full raw stream of working.
- E. Thinking should be on for every task, including quick lookups, for best results.

**Q10. (D3, moderate)**
A support team must tag 20,000 short customer messages into five simple categories every week. Following the course's model-ladder logic, which choice fits best?

- A. The top-tier model, because accuracy always matters most.
- B. The mid-tier model with maximum thinking.
- C. The small, fast model, because this is high-volume, low-depth work.
- D. Whichever model has the largest context window.

**Q11. (D5, moderate)**
A teacher adds "Always answer in Markdown tables and use my Grade 9 physics syllabus" to **Instructions for Claude** (account-wide). Her personal emails and recipe questions now come back as tables about physics. What is the best fix?

- A. Keep only lines true for every conversation in Instructions for Claude, and move the syllabus and table rule into a physics project.
- B. Add a line: "Ignore these instructions when they don't apply."
- C. Turn on memory so Claude learns when to use the instructions.
- D. Switch to the top-tier model, which can judge better when instructions apply.

**Q12. (D5, hard) Choose TWO.**
Anthropic's list: "Projects carry context. Skills define procedures. Code execution verifies computations. Memory persists continuity." Which **two** statements are correct according to the course?

- A. The account-wide Instructions for Claude field is one of Anthropic's four.
- B. A skill is enabled once at the account level and can fire in any chat.
- C. A project's instructions apply to every chat on the account.
- D. Memory stores facts by updating the model's weights.
- E. When a project's knowledge outgrows the window, the product fetches only the relevant parts per question.

**Q13. (D3, moderate)**
A procurement lead needs a document comparing five vendors on price, support and security, with sources, to present to the board. Which Claude.ai tool fits best, according to the course?

- A. Web search, because it is on by default and returns current facts.
- B. The model's own knowledge, with thinking turned on.
- C. A connector to the company's email.
- D. Research, because it plans many searches and returns a structured, cited report.

**Q14. (D5, moderate)**
Sara changed jobs from marketing to finance three months ago. Every new chat still assumes she works in marketing. What is the correct explanation and fix?

- A. The model was trained on her old data; she must wait for the next model release.
- B. The memory feature's stored note is out of date; she should read and edit or delete it.
- C. The context window is too small to hold her new job; she should upgrade her plan.
- D. The model is sycophantic and assumes what she wanted before; she should use neutral wording.

---

*Answers are hidden. Send yours and I'll mark them with explanations and update your weak-area tracker.*
