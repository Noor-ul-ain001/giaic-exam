# Deep Dive: *Just Delegate It* (complete)

The whole course, concept by concept, with related ideas from your other files. Everything is cited by file and section. "JDI" means *Just Delegate It A Crash Course.md*.

**Why this file matters for the exam.** It is the first Foundations course, and its questions table maps to **six of the seven exam domains** (JDI, "The questions this course answers"):

| JDI topic | Exam domain |
|---|---|
| Asking vs job (§1), outcome not clicks (§2), the brief (§3), deliverable (§6) | **D1 Prompting and Task Execution** |
| Verify before you accept (§10) | **D2 Output Evaluation and Validation** |
| Research (§4), the source (§5), same job different AI (§11) | **D3 Product and Model Selection** |
| The job again: Projects (§8) | **D5 Configuration and Knowledge Management** |
| Authority (§7), accountability (§10) | **D6 Governance, Risk, and Responsible Use** |
| Intervene (§9) | **D7 Troubleshooting and Optimization** |
| The Delegation Loop, the Delegation Record | Additive (not exam objectives, but they hold everything together) |

---

## ⚡ All key points on one page (for quick revision)

**Big picture**
- AI can do an hour of work in a minute.
- But AI **cannot tell you if its own result is right**. Only checking can.
- So the course gives you a rhythm (the loop), a work order (the brief) and a record.

**Delegation Loop**
- Six steps: **Define, Delegate, Observe, Intervene, Verify, Accept**.
- AI does the **middle** (the work).
- You own **both ends**: what the job is, and whether the result is good enough.

**Concept 1. From asking AI to giving AI the job**
- **Asking** = you get advice, and the work stays with you.
- **Delegating** = you ask for **a thing to exist** (a table, a list with links), so only checking is left.
- The difference is the **type of sentence**, not its length, and not a paid plan.

**Concept 2. Give AI the outcome, not the clicks**
- Say **what you want at the end**, not every click to get there.
- If you dictate steps, the result can **never be better than your plan**, and AI can't warn you.
- Steps are fine only when they are a **real requirement** (put them under Constraints).

**Concept 3. Write the Delegation Brief**
- A brief = **six lines**: Outcome, Context, Constraints, Authority, Deliverable, Verification.
- People forget **Authority** (what AI may decide alone) and **Verification** (what you'll check).
- Write Verification **before** the work, so reading becomes checking.

**Concept 4. Give AI something to research**
- AI either **remembers** (old training) or **looks** (search).
- For prices, dates, links and "does it still exist?", it must **look**.
- A looked-up fact comes **with a source**. A remembered one comes alone, and sounds just as sure.

**Concept 5. Give AI the source**
- When AI needs something only you have, **give it the source**.
- Two magic instructions: **"Use only the text below"** and **"Quote the sentence you used"**.
- Allow the answer **"not in the source"**, so AI doesn't fill gaps with guesses.

**Concept 6. Ask for the deliverable, not an answer**
- An **answer** talks to you. A **deliverable** can be handed to someone else.
- Name the **form**: table, document, file, columns.
- Tidy documents often **drop warnings**. Say: "Keep every 'unverified' mark."

**Concept 7. Decide how much of the job AI owns**
- Authority has two parts: **how** AI works, and **what** it may do without asking.
- Ask for the **plan first**, change one step, then say "go". Fixing a plan is the cheapest fix.
- Boundaries: **research not buy, draft not send, inspect not delete, choose but tell me**.

**Concept 8. Give AI the job again**
- Same job again? Results can differ because **the world changed** or **AI chose differently**.
- Retyping the same background a **third** time? Put it in a **Project**.
- Project **knowledge** = files AI may read. **Standing instructions** = rules AI must follow.

**Concept 9. Intervene when AI goes wrong**
- When AI goes wrong, send the **smallest message that fixes it**.
- Six moves: **stop, correct, redirect, change the requirement, escalate, take it back**.
- People forget **escalate**: a stronger model or thinking mode may be all it needs.

**Concept 10. Verify before you accept**
- Four steps: **Identify** what matters → **Trace** to the source → **Challenge** it → **Decide**.
- Four decisions: **Accept, Correct, Investigate, Reject**.
- Check more when **stakes, reversibility, audience or regulation** are high. One is enough.

**Concept 11. Same job, different AI**
- Run the **same brief, unchanged**, in another AI.
- If it works there too, your brief describes **the job, not the tool**.
- Two runs on one day are an **observation, not a ranking**.

**B1. Delegation is workflow design, not "giving work to AI"**
- Delegation = deciding **who does which part**, and **why**.
- Three awareness types: the **problem**, the **platform** (right AI), the **task split**.
- Business rules (limits, approvals, send vs draft) are **your** decisions, written in Authority.

**B2. Three modes: automation, augmentation, agency**
- **Automation** = do this task. **Augmentation** = think with me. **Agency** = pursue this goal for me.
- Agency = AI set up to do **future** tasks, possibly **for other people**, while you're not there.
- In agency, judgment must be **built in beforehand**, because nobody is watching.

**B3. Ownership per step: the three criteria**
- Classify every step: **AI-appropriate**, **human-retained**, or **collaborative**.
- Only three questions decide: **Can it be undone? What does a mistake cost? Is this the actual decision?**
- Not a score. **The strictest answer wins.**

**B4. How delegation goes wrong over time**
- Trust is earned **per step**, not across steps.
- **Halo delegation**: giving AI a new step because a different step went well.
- **Unstaffed gate**: the review still exists on paper but nobody really does it.

**B5. Authority, deeper: gates, ladders and thresholds**
- Safety is a **stack** of controls, not one approve button.
- **Action ladder** = what can this action do to the world? **Review thresholds** = must a person see the result?
- Pick the safety level **before** the run.

**B6. Before delegating at all: is this use case appropriate?**
- Before delegating, ask: **should AI do this at all?**
- Three answers: **fully appropriate**, **appropriate with review**, **inappropriate**.
- Name the **deciding factor** in one sentence.

**B7. Data before delegation: tiers and redaction**
- Data has three levels: **green** (OK), **yellow** (check first), **red** (not through unapproved tools).
- Ask: does the job need **who** it is, or only the **pattern**?
- Removing names isn't enough if other details still point to one person.

**B8. Diligence: the three kinds of responsibility**
- Three responsibilities: choose tool and data well, **be honest** about AI's role, **check before sending**.
- The more a result affects others, the stronger the case for telling them.
- Numbers a decision depends on must be **calculated, never guessed**.

**B9. The science under the brief: context engineering**
- AI only sees what's on its **"desk"** (the context window) right now.
- It remembers nothing between turns by itself (**stateless**).
- More files ≠ better. **Remove** what isn't needed.

**B10. Why we verify easy-looking things: the jagged frontier**
- AI can be brilliant at a hard task and fail an **easy** one next to it.
- Weak spots: letters, **very recent** facts, **your private** context, rare topics.
- So check the easy-looking claims too, especially prices, dates, links.

**B11. Intervene, deeper: diagnose by timing**
- Ask **when** the problem started.
- Wrong from the start → **missing information** in the prompt.
- Good, then worse → **chat too long**; summarise and restart.

**B12. From a job to a workflow to a worker**
- Others depend on your tool → it's now **infrastructure**; get engineering help.
- Same solution three times → it can become a **reusable worker/Skill**.
- The same 4Ds (Delegation, Description, Discernment, Diligence) scale up to full systems.

---

## 0. The big picture in one minute

> **🔑 Key points (easy)**
> - AI can do an hour of work in a minute.
> - But AI **cannot tell you if its own result is right**. Only checking can.
> - So the course gives you a rhythm (the loop), a work order (the brief) and a record.
> - Remember: **Give AI the job. Watch it work. Check what matters. Then decide.**

**The opener** (JDI, "See it in two minutes"). You ask AI to find three free courses in a table with links. Then you open one link and check it. One of three things happens: the page agrees, it disagrees on a detail (often price or language), or the link doesn't reach the course. **Nothing in the table told you which one you would get.**

> AI did an hour's work in a minute. The one thing it could not do was tell you whether to trust the result.

That is the whole course. The rest gives that moment a **rhythm** (the Delegation Loop), a **written form** (the Delegation Brief), and a **record** (the Delegation Record).

**The one sentence to remember** (JDI, "A short recap"):
> **Give AI the job. Watch it work. Check what matters. Then decide.**

**The book's thesis behind it** (JDI, "Where this leads"): "Humans define intent. Agents execute. Humans verify outcomes." This is the **10-80-10 Rule**: the first tenth is yours, the middle is the machine's, the last tenth is yours again.

**Go deeper**

- **Why this is the whole course.** In the opener, three outcomes are all "normal": the page agrees, differs on a detail, or the link is wrong. The table looks identical in all three cases. That is the core problem the rest of the course solves: **the output's appearance carries no information about its correctness** (see also *What AI Actually Is*, §3: no internal truth-checker).
- **10-80-10 in practice.** The first 10% (define and brief) and last 10% (verify and accept) are small in time but carry all the responsibility. Cutting them to save time is the most common way a delegated job fails.

> **Urdu:** AI کام تیزی سے کر دیتا ہے، مگر یہ نہیں بتا سکتا کہ نتیجے پر بھروسہ کیا جائے یا نہیں۔ یہ فیصلہ ہمیشہ آپ کا ہے۔

---

## 1. The Delegation Loop: six steps (JDI, Part 2 opener)

> **🔑 Key points (easy)**
> - Six steps: **Define, Delegate, Observe, Intervene, Verify, Accept**.
> - AI does the **middle** (the work).
> - You own **both ends**: what the job is, and whether the result is good enough.
> - AI can help you with the ends, but it can never take them.

| Step | What it means | Who owns it |
|---|---|---|
| 1. **Define** | Say what result you want | **You** |
| 2. **Delegate** | Give AI responsibility for producing it | **You** |
| 3. **Observe** | Let AI do routine work without directing every step | AI works, you watch |
| 4. **Intervene** | Correct, redirect, constrain or clarify when AI drifts | AI works, you step in |
| 5. **Verify** | Check the claims, numbers and actions that matter | **You** |
| 6. **Accept** | Decide if the result is fit for use, or send it back | **You** |

**Key rule:** AI owns the middle. **You own both ends.** AI can *help* with Define, Delegate, Verify and Accept, but it cannot *take* them, "because what the job is and whether the result is fit for use are decisions you answer for."

**Deep connection.** The same shape appears everywhere in your files:
- *General Agents on the Web*, §8: **brief, plan, approve, review** for work you won't watch.
- *AI Fluency*, §7: the **4Ds** (Delegation, Description, Discernment, Diligence) as an operating loop.
- *Workflow Design*, §9: the build loop **ideate, prototype, feedback, refine**.

The loop grows as the work leaves your sight, but the two human ends never disappear.

**Go deeper**

- **Why the ends can't be delegated.** Define decides *what the job is*; Accept decides *whether it is fit for use*. Both are judgments you answer for. AI may suggest a definition or a verdict, but adopting it is still your decision.
- **Observe and Intervene merge in a chat.** In a chat you read the reply and answer it in one act. In an agent that runs while you watch, they separate: you watch live and can press stop mid-run (JDI §9).
- **Common confusion:** Verify ≠ Accept. Verify gathers evidence (four steps). Accept is the decision made on that evidence (four decisions).

> **Urdu:** کام کی شروعات (کیا چاہیے) اور اختتام (کیا نتیجہ قابلِ قبول ہے) ہمیشہ انسان کے پاس رہتے ہیں۔ درمیان کا کام AI کرتا ہے۔

---

## Concept 1. From asking AI to giving AI the job (D1)

> **🔑 Key points (easy)**
> - **Asking** = you get advice, and the work stays with you.
> - **Delegating** = you ask for **a thing to exist** (a table, a list with links), so only checking is left.
> - The difference is the **type of sentence**, not its length, and not a paid plan.
> - Test: could I hand this result to someone else?

**The experiment.** In a fresh chat, ask "What are some good courses for learning AI agents?" Compare that answer with the opener's table.

| Asking | Giving a job |
|---|---|
| Gets an **answer** (a list, advice) | Gets a **result** (a table with links) |
| The next steps stay **yours**: open, compare, check, decide | AI did the first pass. Only **checking** is left for you |
| AI may **guess** what form you wanted | The job removes the guessing |

**The real difference is not length.** The job asked for **a thing to exist**: three courses, in a table, with links. To **delegate** means giving AI responsibility for producing the result. It depends on **what kind of sentence you type**, not on a paid plan or special model.

**Three tests** (JDI §1, "What to Notice"):
1. Which answer could you **hand to someone else**, and which is advice you still have to act on?
2. Did it separate **facts it found** from **advice it gave**?
3. Which one left you with something you could **check**?

**The running job.** From here, you carry one job through the whole course and add one line at each concept. By Concept 10 you've written a complete brief "without ever filling in a form".

**Exam trap.** An option that treats "asking a better question" and "delegating a job" as the same thing is wrong. The test is whether a checkable thing is asked to exist.

**Test yourself.** The course's own first assessment question: *Sana types "What are the best free tools for making a CV?", gets a good list, then opens each tool, compares them, and picks one. Which step did she keep that she could have delegated?* Answer: the comparison and recommendation. She asked instead of delegating, so the work stayed with her. (JDI, "Test Your Understanding", question 1; answer is my reasoning from §1.)

**Go deeper**

- **Hidden mechanism.** When you ask a question, AI must *guess* the form you want. When you name the thing (three courses, table, links), the guessing is gone, and you get something **checkable** item by item.
- **What to check first.** Did the answer **separate facts it found from advice it gave**? Mixed together, you can't tell which parts need verification.
- **Exam-style thinking:** If a scenario shows someone doing the comparing, collecting or formatting themselves after an AI answer, the fix is to delegate that result, not to "ask better".

> **Urdu:** سوال پوچھنے سے مشورہ ملتا ہے اور کام آپ ہی کو کرنا پڑتا ہے۔ کام سونپنے سے ایک تیار چیز ملتی ہے جسے آپ صرف جانچتے ہیں۔

---

## Concept 2. Give AI the outcome, not the clicks (D1)

> **🔑 Key points (easy)**
> - Say **what you want at the end**, not every click to get there.
> - If you dictate steps, the result can **never be better than your plan**, and AI can't warn you.
> - Steps are fine only when they are a **real requirement** (put them under Constraints).
> - Write the outcome as: "When this is done, I will have…"

**The experiment.** Give the same job as a **recipe**: "Look only at provider one and provider two, find the three highest-rated courses on each, copy name, price, length into a table, then tell me which is best."

**What goes wrong with a recipe:**
- AI follows your steps **even where a step is weak**, because the plan was yours.
- **Your plan becomes the limit.** If the two sites you named are not where the best courses are, the table is neat, the recommendation is poor, and **nothing in the result tells you so**.
- "Highest-rated": if the page shows no rating, **AI supplied one**.

**The outcome version** names what should exist when the work is done. AI chose where to look. You judge the result against the **outcome**, not against a plan you invented on the spot.

**When steps ARE right.** When a source or an order of work is **genuinely required**, that is a **constraint**, and it goes on the Constraints line. What you should not do is "write steps because you are nervous. That feeling belongs at the end, when you check, not at the start."

**Your Turn formula:** "When this is done, I will have…" plus two limits, one line each (for example "must be possible to start this week", "no more than five hours a week").

**Check:** Does my sentence describe a **result, not an action**? Could someone else read it and **know when the job is finished**? Did I **leave the method to AI**?

**Deep connection.** *Code You Never Write*, §5 says the same for code: **"Brief the problem, not the program."** *AI Fluency*, §4 splits Description into **product** (what you want), **process** (how to approach it) and **performance** (how AI should behave). Concept 2 says: lead with product, and add process only when it is a real requirement.

| Approach | Good when | Risk |
|---|---|---|
| Outcome only | You don't know the best method | You must check the result carefully |
| Outcome + required constraints | A source or order is truly required | None, if the constraint is real |
| Full recipe | Almost never for research jobs | Result limited by your plan; AI can't warn you |

**Go deeper**

- **Why a recipe is dangerous.** A recipe hides two failures: (1) AI follows a weak step obediently; (2) AI may **invent** data to fill a step ("highest-rated" when no rating exists). Both produce a neat result with no warning.
- **Nervousness goes at the end.** The course's rule: don't write steps "because you are nervous". Put that worry into the Verification line instead, where it actually protects you.
- **How to judge a good outcome sentence:** it describes a *result*, not an *action*, and a stranger could tell when the job is finished.

> **Urdu:** AI کو قدم بہ قدم ترکیب نہ دیں، بلکہ بتائیں کہ آخر میں کیا چیز تیار ہونی چاہیے۔ ترکیب دینے سے نتیجہ آپ کے منصوبے سے بہتر نہیں ہو سکتا۔

---

## Concept 3. Write the Delegation Brief (D1)

> **🔑 Key points (easy)**
> - A brief = **six lines**: Outcome, Context, Constraints, Authority, Deliverable, Verification.
> - People forget **Authority** (what AI may decide alone) and **Verification** (what you'll check).
> - Write Verification **before** the work, so reading becomes checking.
> - If a line doesn't apply, write **"none"**, don't delete it.
> - When a result disappoints, one of the six lines was missing.

**Six questions you answer before AI starts**, so you have something to check the result against.

| Line | Meaning | Example (JDI §3) |
|---|---|---|
| **Outcome** | What should exist when done | Three free courses on AI agents, compared, one recommended for a beginner |
| **Context** | What AI can't know unless you say it | I've never built an agent, can't program, have 5 hours a week |
| **Constraints** | Requirements and limits | Free to start; no programming needed; search for current info |
| **Authority** | What AI may decide **without asking** | Choose sources; if two are equal pick the shorter; **say clearly** if paid |
| **Deliverable** | The form of the result, so someone can use it | Table: provider, language, time, certificate cost, link; then 2-sentence recommendation |
| **Verification** | What you'll check, **written before the work starts** | Mark anything unconfirmed as "unverified" instead of guessing |

**The two lines people skip: Authority and Verification** (JDI, "Quick self-check", answer 4).

- **Authority exists even in a chat**, where AI can't send or buy anything. It covers **decisions**. "Pick the shorter one without asking me" is authority. "Say clearly if a course is paid" is a **limit on** authority. Without the line, **AI decides for you silently**, and you never learn a decision was made.
- **Verification written first** turns reading into checking. You name what matters enough to open a source for, while you still remember why it matters.

**It's a thinking tool, not a form.** Nobody fills in six boxes for a two-line job. But **"every time a result disappoints you, one of these six questions was unanswered, and now you can say which."** If a line doesn't apply, write **"none"** rather than deleting it, so you can see you decided.

**Which competency sits behind each line** (JDI §3, table):

| Brief line | *AI Fluency* competency |
|---|---|
| Outcome | Delegation + Description |
| Context | Description |
| Constraints | Description + Diligence |
| Authority | Delegation + Diligence |
| Deliverable | Description |
| Verification | Discernment + Diligence |

**How the brief grows later** (JDI, "Where this leads"):
- *General Agents*, §8: a brief for **unwatched** work adds allowed **sources**, a **destination** for the finished file, and a rule for **what should stop the run and come back to you**. Plus: "If the necessary evidence is missing, say what is missing and stop rather than inventing it."
- An **AI Worker (Digital FTE)** gets an outcome contract: trigger, evidence, acceptance criteria, a main number, guardrails, forbidden actions, a **named human with final authority**, and a record.

**Go deeper**

- **Authority exists even in a chat.** AI can't buy or send in a chat, but it still makes decisions: which sources, which course to recommend, what to do with ties. Without an Authority line these decisions are made **silently**.
- **"Say clearly if…" is a limit on authority.** It doesn't forbid a choice; it forces AI to make the choice **visible**, so you can review it.
- **Diagnostic use.** When a result disappoints, go line by line: which of the six was unanswered? This turns "AI is bad" into a specific, fixable gap.
- **Competency map** (JDI §3): Verification rests on **Discernment and Diligence**, Authority on **Delegation and Diligence**. The two lines people skip are exactly the two that carry responsibility.

> **Urdu:** بریف کی چھ لائنیں ہیں: نتیجہ، پس منظر، پابندیاں، اختیار، شکل، اور جانچ۔ لوگ عموماً "اختیار" اور "جانچ" بھول جاتے ہیں۔ جب نتیجہ خراب ہو تو دیکھیں کون سی لائن خالی تھی۔

---

## Part 2 rule: "Need first, then tool"

A control on the screen is learned **when a job needs it, not before** (JDI, Part 2 opener). This map is worth memorising:

| The job needs | So you | Concept |
|---|---|---|
| Current information | Ask for it; turn on web search if you see the switch | 4 |
| A source only you have | Paste it or attach the file | 5 |
| Something private | Take private parts out; use a temporary/incognito chat for the rest | 5 |
| A finished thing | Ask for the document, table or file itself | 6 |
| Room to choose its method | Say what it may decide alone and what it must ask | 7 |
| Same context every time | Project: sources as **knowledge**, rules as **standing instructions** | 8 |
| Same job on a clock | Scheduled task, if your plan has one | 8 (optional) |
| More capability than it showed | Turn on **thinking**, or a stronger model | 9 |
| A place for the result / a source in another app | A **connector** | 7 (optional), *Skills & Connectors* |

**Exam angle (D3 and D5).** Many questions are "which feature solves this need?" Match the **need** to the **tool**. For example: a repeated background → Project, not a longer prompt. A price that changes → search, not the model's memory. A hard multi-step comparison → thinking or a stronger model.

---

## Concept 4. Give AI something to research (D3)

> **🔑 Key points (easy)**
> - AI either **remembers** (old training) or **looks** (search).
> - For prices, dates, links and "does it still exist?", it must **look**.
> - A looked-up fact comes **with a source**. A remembered one comes alone, and sounds just as sure.
> - **A citation is not verification. Opening it and finding the sentence is.**
> - A source is not a date: check the page date yourself.

**Two ways AI knows things:**

| Remembering (pretrained) | Looking (search) |
|---|---|
| What it read when it was built. **Large and out of date** | Looks now. Needed for price, start date, link, "does it still exist?" |
| Fact **arrives alone**, and sounds just as sure | Fact should **arrive with a source you can open** |

**The line to add:** "For each course, say whether you found it by searching just now or already knew about it, and give the date of the page you used."

**Two cautions:**
1. If a current claim arrives **with no source**, do not assume AI looked, **whatever the answer says about itself**. The word "searched" is only a hint. The **source and its date are the evidence.**
2. **A source is not a date.** Pages go stale. Find the date on the page yourself.

**Search vs deep research.** Web search is for facts one search settles. **Deep research** takes minutes, reads many pages, and writes a report: use it when **the deliverable is the report**.

**The key sentence:**
> **A citation is not verification. Checking the citation is verification.**

Trace method: open the page, **find the sentence** that supports the fact, **check the date**. If the sentence isn't there, or the date is old, "the link was decoration."

**Deep connection.** *AI Prompting in 2026*, §3 names **three retrieval modes: pretrained, web search, deep research**. *What AI Actually Is*, §1–§2: the model predicts the next token and **"never looks anything up"** by itself; its learning **stopped** at training. Search is a **tool** added around the model (*What AI Actually Is*, §8).

**Go deeper**

- **Why AI sounds sure either way.** A remembered fact and a looked-up fact come out in the same confident voice (*What AI Actually Is*, §6: confidence is a learned style).
- **AI's self-report is weak evidence.** If the answer says "I searched" but gives no source, don't assume it looked. The course says: judge by the source and its date, not the words.
- **Research mode vs search.** Use deep research only when **the report is the deliverable**; one fact needs one search.
- **Why the answer may change between runs:** either the world changed, or the search did. That question returns in Concept 8.

> **Urdu:** AI کی یادداشت پرانی ہوتی ہے۔ تازہ معلومات کے لیے اسے سرچ کرنے کو کہیں، اور خود ماخذ کھول کر تاریخ اور جملہ دیکھیں۔ حوالہ دینا جانچ نہیں، حوالہ کھول کر دیکھنا جانچ ہے۔

---

## Concept 5. Give AI the source (D3, with privacy from D6)

> **🔑 Key points (easy)**
> - When AI needs something only you have, **give it the source**.
> - Two magic instructions: **"Use only the text below"** and **"Quote the sentence you used"**.
> - Allow the answer **"not in the source"**, so AI doesn't fill gaps with guesses.
> - Remove names and private details **before** pasting. A temporary chat does not erase what you paste.
> - Long chat getting confused? **Summary → fresh chat.**

Some jobs need something AI **cannot search for**: a syllabus, an office notice, a message thread, a policy page. You have it; you give it.

**Two instructions make pasted text a real source:**
1. **"Using only the text below"**
2. **"Quote the sentence you used"**

Plus: "If the text does not say, write **'not in the source'**."

Without them, AI **mixes what you gave with what it remembers**, and you can't tell which is which. With them, every answer points to a sentence you can find, and "not in the source" becomes a **good answer instead of a gap AI fills**.

**The check:** take one quoted sentence and find it in the original.

| What you find | Meaning |
|---|---|
| Word for word | Good |
| Close but not exact | AI **paraphrased and called it a quote** |
| Not there at all | AI **invented** it |

**Paste vs attach.** A page or two: paste. Longer: attach the file (plus or paperclip). Same job either way.

**Privacy rules** (JDI §5, "What you paste"):
- Before pasting anything real, **remove names, phone numbers, account numbers**, anything you wouldn't pin to a public notice board. "A free assistant is not your filing cabinet."
- A **temporary chat** (ChatGPT) / **incognito chat** (Claude) is not saved to history and does not add to memory. **But neither makes a paste disappear**: the provider still holds a copy for a time. So removing private data comes first.
- Whether data may go into AI **at all** is a governance question (*Governance*, §2 "The Data").

**When a long chat goes stale.** After an hour, a chat loses track of early decisions and starts contradicting itself. **Don't argue with it.** Ask for a short summary of what's decided and what remains, open a **fresh chat**, and paste it as the first message. "The summary is a source too."

**Deep connection.** *What AI Actually Is*, §5: **the context window is the only thing it can see.** *AI Fluency*, §5.1 gives the same three-line pattern: answer only from the attached files; say so if a file doesn't state it; quote the heading and sentence.

**Go deeper**

- **Three results when you check a quote:** word-for-word (good), close but not exact (AI **paraphrased and called it a quote**), missing (AI **invented** it). Each tells you something different about trust.
- **Why "not in the source" matters.** Models rarely admit gaps unless allowed. Giving permission turns a gap into a **visible mark** instead of a guess (also *AI Prompting*, §6).
- **Privacy depth.** A temporary/incognito chat only stops saving to history and memory; the provider still keeps a copy for a time. Whether data may go in **at all** is a governance question (Part B7).
- **Stale chat is a context problem, not a prompt problem.** Arguing adds more text to an overloaded conversation. A summary is itself a source you control.

> **Urdu:** اپنا ماخذ دیں اور کہیں "صرف اسی متن سے جواب دو اور جملہ نقل کرو"۔ پھر خود دیکھیں کہ وہ جملہ واقعی متن میں موجود ہے۔ نجی معلومات پہلے ہٹا دیں؛ عارضی چیٹ بھی ڈیٹا کو مکمل طور پر غائب نہیں کرتی۔

---

## Concept 6. Ask for the deliverable, not an answer (D1)

> **🔑 Key points (easy)**
> - An **answer** talks to you. A **deliverable** can be handed to someone else.
> - Name the **form**: table, document, file, columns.
> - Tidy documents often **drop warnings**. Say: "Keep every 'unverified' mark."
> - Check: count the warnings in the chat vs in the document.

**An answer replies to you. A deliverable can be handed on**: saved, sent, acted on. Examples: a table with named columns, a document, a spreadsheet, a file. "Most deliverables have to leave the chat to survive."

**Where it appears:** some assistants open a **separate panel** beside the chat (artifacts); some produce a **file to download**. Same idea: the **work product is separated from the conversation about the work product**. For data, ask for a **table or spreadsheet, not paragraphs**.

**The hidden danger: deliverables lose caveats.** An "unverified" mark that survived three chat replies **can vanish** when poured into a tidy document, "because tidy is what the document is for."

So add: **"Keep every 'unverified' mark exactly where it is."**

**The check:** count the caveats in the chat answer (every "unverified", "may", "check"). Count them in the document. If the second number is smaller, find what was dropped and put it back.

**Three questions:** Does it match the deliverable line column for column? Did every caveat survive? **Could someone read it without ever seeing the chat?**

**Deep connection.** *General Agents*, §5 takes this further: **three file tiers**. Tier 1 = temporary scratch space (wiped), Tier 2 = vendor platform storage (safe but in their custody), Tier 3 = your own system of record. **"Finished work exits the platform."**

**Go deeper**

- **Why caveats vanish.** A document's purpose is to look tidy. Turning chat into a document "cleans" hedges like "may" and "unverified". The course treats this as a predictable failure, so you prevent it in the instruction and **count** caveats after.
- **The work product is separated from the conversation.** Whether it appears in a side panel or as a download, the point is that it can be kept and passed on without the chat.
- **For data, ask for a table or spreadsheet**, not paragraphs, so each value is checkable.

> **Urdu:** جواب صرف آپ کے لیے ہوتا ہے، مگر ڈیلیوریبل ایسی چیز ہے جو کسی اور کو دی جا سکے۔ دستاویز بناتے وقت "غیر تصدیق شدہ" کے نشان اکثر غائب ہو جاتے ہیں، انہیں گن کر چیک کریں۔

---

## Concept 7. Decide how much of the job AI owns (D6)

> **🔑 Key points (easy)**
> - Authority has two parts: **how** AI works, and **what** it may do without asking.
> - Ask for the **plan first**, change one step, then say "go". Fixing a plan is the cheapest fix.
> - Boundaries: **research not buy, draft not send, inspect not delete, choose but tell me**.
> - The real failure is a **silent change**, not a change.
> - Trust grows slowly: read every step at first, only the plan later.

**Authority has two faces.**

### Face 1: how much of the **method** AI decides → **Plan-first**

Add: "Before you start, list the steps you plan to take, in order, and wait for my go-ahead. Do not begin until I say go." Then **change at least one step** (so you know the veto is real) and say "go".

- The **cheapest moment in any job is before it runs.** A plan costs a minute to read and a sentence to fix. The same mistake found after the run **costs the run**.
- Asking for the plan is how you **Observe** a job you can't watch. Redirecting it is **Intervene at its cheapest**.
- **An approved plan is not a cage.** AI may find a better route. What it may not do is **cross a line you drew** or **change something that matters without telling you**. "The failure is the silent change, not the change."
- If AI **starts before you say go**, that's "an authority failure in miniature."
- After the run, put the approved plan beside what AI did. **Every difference is one question to ask.**

### Face 2: what AI may **do** without asking → **Boundaries**

| Boundary | Why it exists |
|---|---|
| **Research, but do not purchase** | Money that moves is hard to move back |
| **Draft, but do not send** | Sending creates a promise someone else can see |
| **Inspect, but do not delete** | Deleting destroys the evidence you'd need to check the work |
| **Choose, but say when you chose** | A silent decision is one you cannot review |

In a chat these are about **decisions**. Write them anyway, because **the same lines become permissions the day AI can act.**

**Trust grows with a record.** First run: read the plan **and every step**. Fifth clean run of the same job: read **the plan**.

**Four questions before AI touches anything real** (when it reaches a system, not just a chat):
1. What may it **read**?
2. What may it **do**?
3. Do I **trust where its information comes from**?
4. Am I **allowed to give it this access at all**?

**Optional real action (Netlify).** AI builds a one-page website and must **show it and wait** before publishing. If it publishes before "go", you've seen the authority failure for real. Once public, you check it loads, has nothing private, and the contact works. Deleting the site stays with you: "Inspect, but do not delete."

**Deep connections:**
- *General Agents*, §7: the gate becomes **approval modes** (Manual, Auto, Skip in Cowork) and an **autonomy ladder**: read and summarise → draft but don't send → write to reversible records → send, publish, purchase, delete (**Manual**). "Choose the gate **before** the run."
- *General Agents*, §8 note: in Cowork, **Manual mode does not automatically make a plan**. If you want plan-first, **put it in the brief**.
- *General Agents*, §6: **read is not send, draft is not publish, view is not edit.** Grant the smallest scope.
- *Governance*, §3: treat extensions like software; "trusted tool, untrusted content."

**Go deeper**

- **Why the plan is the cheapest moment.** A plan costs a minute to read and one sentence to fix. The same mistake after the run costs the whole run.
- **An approved plan is not a cage.** A good agent may find a better route. The rule is: no crossing drawn lines, and no **silent** change to something that matters. Compare plan vs actions afterwards; every difference is a question.
- **Chat boundaries become permissions.** The same four lines you write for decisions today become system permissions the day AI can act. That's why you practise them now.
- **Four questions before AI touches a real system:** What may it read? What may it do? Do I trust where its information comes from? Am I allowed to give this access?

> **Urdu:** اختیار کے دو پہلو ہیں: طریقہ کار کون طے کرے (پہلے منصوبہ مانگیں اور منظوری دیں)، اور AI بغیر پوچھے کیا کر سکتا ہے (تحقیق کرے مگر خریدے نہیں، مسودہ بنائے مگر بھیجے نہیں، دیکھے مگر حذف نہ کرے)۔ اصل غلطی خاموش تبدیلی ہے۔

---

## Concept 8. Give AI the job again (D5)

> **🔑 Key points (easy)**
> - Same job again? Results can differ because **the world changed** or **AI chose differently**.
> - Retyping the same background a **third** time? Put it in a **Project**.
> - Project **knowledge** = files AI may read. **Standing instructions** = rules AI must follow.
> - Repeating **method** = Skill. Repeating **timing** = scheduled task.
> - Review what's stored (and memory) **monthly**. A wrong line spoils every result.

**The experiment.** Save your brief **outside the chat**, run it again unchanged in a fresh chat, and mark every difference.

**Nothing changed, but the result did.** Two kinds of difference:
- **The world** changed (a course closed, a price moved).
- **AI** chose differently (another source, another order).

Telling these apart is "the beginning of running a job rather than doing it once."

**Repetition asks for two things:**

**1. Context you keep retyping → a Project.**
- **Knowledge** = the files a Project holds: what AI **may read**, in every chat inside it.
- **Standing instructions** = rules written once: what AI **must do every time** (e.g. "mark anything you could not confirm as unverified").
- The rule: **instructions for rules that don't change, knowledge for sources that don't change, a Project for one stream of work, the chat for today's job.**
- **"The third time you paste the same background, put it somewhere AI reads by itself."**
- **Anthropic's three-question test**: Does the task come back? Is the background the same each time? Is the output shape the same each time? **Two yes answers out of three → the Project earns its place.**

**2. A clock → scheduled tasks** (paid-plan features on both assistants; details in *Quick Reference*). A scheduled ChatGPT task **does not see your Project's files**, so paste the whole brief. Apply Concept 10 to the first unwatched result: **"a job that ran is not the same as a job that worked."**

**Stored context is a responsibility.** What's in a Project shapes **every** answer inside it. Memory (if on) is separate: you can **read, edit and delete** it. **Once a month, review both** and remove what's no longer true. "A wrong line in a Project is a wrong line in every result the Project produces."

**Project vs Skill.** A Project holds **what AI should know**. If what repeats is **the method** (same steps, same order), that's a **Skill** (*Skills & Connectors*). When the job becomes a **team's**, it's a **workflow** (*Workflow Design & Diagnosis*).

| Repeats... | Put it in | Source |
|---|---|---|
| Background, files | Project **knowledge** | JDI §8 |
| Rules | Project **standing instructions** | JDI §8 |
| The method / steps | A **Skill** (`SKILL.md`) | JDI §8; *Skills & Connectors* §2, §4 |
| The timing | A **scheduled task** | JDI §8; *General Agents* §9 |
| Team involvement | A **workflow** | *Workflow Design* §1 |

**Deep connection.** *General Agents*, §4: persistence is a **stack**, not one thing called memory: session history, Project, semantic memory, standing instructions, your own portable file. Put each fact in **the narrowest layer that reliably applies**. Old sessions are not memory. A Project is not memory.

**Go deeper**

- **Anthropic's three-question test:** Does the task come back? Is the background the same? Is the output shape the same? **Two yes out of three → use a Project.**
- **Project vs memory.** A Project is what *you* stored for one stream of work. Memory is what the *assistant* learned about you. Review both monthly.
- **Scheduled runs have limits.** A ChatGPT scheduled task doesn't see Project files, so the whole brief must be pasted. And a run that happened is not proof it worked (Concept 10).
- **Why the monthly review matters:** stored context fails **silently** (Part B11, stale configuration).

> **Urdu:** جو پس منظر آپ بار بار لکھتے ہیں، اسے پروجیکٹ میں ڈال دیں: فائلیں "نالج" میں اور اصول "اسٹینڈنگ انسٹرکشنز" میں۔ اگر طریقہ کار بار بار دہرایا جاتا ہے تو وہ "اسکل" ہے۔ ہر مہینے محفوظ معلومات دیکھ کر پرانی باتیں ہٹا دیں۔

---

## Concept 9. Intervene when AI goes wrong (D7)

> **🔑 Key points (easy)**
> - When AI goes wrong, send the **smallest message that fixes it**.
> - Six moves: **stop, correct, redirect, change the requirement, escalate, take it back**.
> - People forget **escalate**: a stronger model or thinking mode may be all it needs.
> - Check the fix **in the result**, not in AI's words ("I fixed it" is just a sentence).
> - Write the lesson into the brief so it doesn't happen again.

**The experiment.** Delete the Constraints and Authority lines and run the brief. Watch it drift (paid courses, wrong language, wrong level, a decision you didn't delegate). Fix it with **the smallest message you can write**.

**Six moves, chosen by the symptom:**

| What you see | The move |
|---|---|
| It answered a **different question** | **Stop**, restate the outcome in one line |
| **One fact or line** is wrong | **Correct**: name the error and its replacement |
| **Heading the wrong way**, not wrong yet | **Redirect**: name the direction, not the whole job |
| **The job itself** was wrong | **Change the requirement**, and say you changed it |
| It **can't do a step** at the level needed | **Escalate**: turn on thinking or a stronger model, run again |
| It **keeps failing** after that | **Take the job back.** Some jobs are yours |

**Escalate is the move people miss.** Start fast. When the job has several steps, a careful comparison, a calculation, or must be right, **move up and run the same brief again**. On a free plan without a stronger model, **make the job smaller**: one step at a time, each checked. "Sometimes 'AI failed' means 'I used the wrong level'."

Two kinds of escalation are different:
- **Escalate (Concept 9)** = a **stronger machine**.
- **Reject to an expert (Concept 10)** = a **person who knows the field**.

**Check the fix in the result, not in AI's description.** "'I have corrected the table' is a sentence. Look at the table."

**Close the loop:** write the lesson into the brief as a **Constraint or Authority line**, rerun in a fresh chat, confirm the drift is gone.

**In a chat vs an agent.** In a chat, Observe and Intervene are one act (read the reply, answer it). In an agent working live, they're separate, and **stopping it mid-run is a real button**.

**Deep connections:**
- *AI Fluency*, §5: feedback shape **Problem → Why it matters → Direction**, not "Wrong. Try again."
- *AI Fluency*, §5.2 process discernment: if it repeats a mistake you corrected twice, or you're editing more than you'd write, **change the description, change the tool, or take the task back**.
- *Workflow Design*, §13–§14: turn a reaction into an instruction, and put the fix in the right home (**rule, reference or procedure**) so it lasts.
- *AI Prompting*, §12 and *Quick Reference*, §2: fast vs thinking modes; which model when.

**Go deeper**

- **Match the move to the symptom.** Wrong question → stop and restate. One wrong line → correct. Wrong direction → redirect. Job was wrong → change the requirement **and say so**. Can't do it → escalate. Still failing → take it back.
- **Two kinds of escalation.** Concept 9's escalate = a **stronger machine**. Concept 10's reject-to-expert = a **person who knows the field**. Don't confuse them.
- **Free plan without a stronger model?** Make the job smaller: one step at a time, each checked.
- **Feedback shape** (*AI Fluency*, §5): Problem → why it matters → direction. "Wrong, try again" gives AI nothing to act on.

> **Urdu:** جب AI راستے سے ہٹے تو سب سے چھوٹا پیغام بھیجیں جو مسئلہ حل کرے۔ کبھی مسئلہ پرامپٹ کا نہیں بلکہ کمزور ماڈل کا ہوتا ہے، تو "تھنکنگ" یا بہتر ماڈل استعمال کریں۔ پھر سبق کو بریف میں لکھ دیں۔

---

## Concept 10. Verify before you accept (D2 and D6)

> **🔑 Key points (easy)**
> - Four steps: **Identify** what matters → **Trace** to the source → **Challenge** it → **Decide**.
> - Four decisions: **Accept, Correct, Investigate, Reject**.
> - Check more when **stakes, reversibility, audience or regulation** are high. One is enough.
> - Four things always need a named person: client deliverables, important money figures, sensitive data, public/legal messages.
> - **AI doing the work never moves the responsibility to AI.**

"Check AI's work" is advice, not a method. **This is the method.**

### Four steps: Identify, Trace, Challenge, Decide

1. **Identify** the claims that matter: prices, dates, figures, calculations, quotations, legal or safety claims, the recommendation you'll act on, anything hard to reverse. **Not everything.** Spend checking where an error would cost you.
2. **Trace** one claim: open the source, find the **supporting sentence**, check the **date**, judge the source (the provider's own page beats a blog about it).
3. **Challenge**: how could it be wrong? Could it have changed? Is AI repeating a secondary source? Is an assumption stated as a fact? When credible sources disagree, **the primary one usually wins, unless it is the older one.**
4. **Decide** one of four:

| Decision | Meaning | *AI Fluency* name |
|---|---|---|
| **Accept** | Evidence is enough | Ready to use |
| **Correct** | A specific error can be fixed (this is Intervene) | Needs revision |
| **Investigate** | Evidence incomplete or contradictory; trace again | Needs revision |
| **Reject** | Not reliable enough; take the job back | Needs human override |

**Reject's hidden second form:** you've corrected the same result **three times, and each round helps less**. That's a sign about **the job, not your prompts**. The next move is **a person who knows the field**, not a better message.

### Four review thresholds (one crossed is enough)

| Threshold | Question |
|---|---|
| **Stakes** | What does a mistake cost? |
| **Reversibility** | Can it be undone? |
| **Audience** | Who sees it? A client or the public counts more than you alone |
| **Regulatory exposure** | Is the data or field regulated? |

The higher it sits, the more of the four steps the result gets.

**Deep connection:** *General Agents*, §7 keeps two sets apart. The **autonomy ladder** decides the gate on the **action** (what can it do to the world?). The **review thresholds** decide the review on the **result** (must a person look before it counts?). A rung-one summary still needs review if it goes to a client or uses regulated data.

### Four things that never go out without a named person reading them

1. **Final client deliverables**
2. **Audit-critical or financially material calculations**
3. Anything with **regulated, confidential or highly sensitive data**
4. **Public or legal communications** where a misstatement lasts

**The rule under all four:** **AI doing the work does not transfer accountability to AI. The name on the result is yours.**

**Safest first real delegation:** a job you already finished and trust. Brief AI, hold back your result, compare. Record what matched, what needed fixing, and what should stay with you. "A pass earns AI similar jobs. It never earns your name on the result."

**Deep connections** (full detail in `02-D2-output-evaluation.md`):
- *What AI Actually Is*, §3, §6: no internal truth-checker; confidence is a learned style.
- *AI Fluency*, §5: four signs of a made-up answer (too-exact specifics, confidence where an expert would hesitate, contradictions, claimed actions that never happened).
- *Governance*, §1.3: "a human will review it" is not a gate unless it names **who, what, when**.

**Go deeper**

- **Identify is about economics.** You can't check everything. Spend checking where an error would cost you: prices, dates, calculations, quotes, legal/safety claims, the recommendation, anything irreversible.
- **Challenge rules for conflicting sources:** the primary source usually wins, **unless it is the older one**.
- **Reject has a hidden form:** three corrections, each helping less, means the problem is the job, not your prompt. Next step is an expert.
- **Safest first delegation:** redo a job you already finished and trust, then compare. A pass earns AI *similar jobs*, never your name on the result.

> **Urdu:** جانچ کے چار قدم: اہم دعوے چنیں، ماخذ تک جائیں، سوچیں کہ غلط کیسے ہو سکتا ہے، پھر فیصلہ کریں۔ چار چیزیں کبھی انسان کے دیکھے بغیر باہر نہیں جاتیں۔ ذمہ داری کبھی AI کو منتقل نہیں ہوتی۔

---

## Concept 11. Same job, different AI (D3)

> **🔑 Key points (easy)**
> - Run the **same brief, unchanged**, in another AI.
> - If it works there too, your brief describes **the job, not the tool**.
> - Two runs on one day are an **observation, not a ranking**.
> - Verify the second result **the same way** as the first.
> - The job is yours. **The model is replaceable.**

**The experiment.** Paste your complete brief, **unchanged**, into a **second assistant**. Record five things: did it finish, how many messages, did it honour the **Authority** line, did it **mark anything unverified**, how did the deliverable compare? If you can't use a second assistant, rerun in the same one with a different model or setting, but **write down which test you ran**: that tests **run-to-run variation**, not whether the brief **travels**.

**The brief travelled because it describes the job, not the tool.** Nothing in six lines names a button. Buttons differ and get renamed; the discipline doesn't. Where controls live is **something you look up** (*Quick Reference*), not something you learn.

**What you recorded is two runs on one day, not a ranking.** Models change too fast; this course never asks you to rank assistants.

**Questions:** Did the brief need a change to run elsewhere? If so, which line, and was it a **brief problem or an assistant problem**? Where did the results differ: **facts, form, or only buttons**? Verify the second result **by the same method** as the first.

**Recap line:** "The job belongs to you. **The model is replaceable.**"

**Deep connection and an important distinction:**
- *AI Prompting*, §13: **models checking models** requires **different model families** (companies). Two Claude models checking each other is not cross-model checking. And the score is **a progress signal, not a truth signal**.
- *Code You Never Write*, §6: a cross-model check has one limit: **both programs read your brief, so a rule you left out is a mistake both can make and both agree on.**
- Concept 11's main purpose is **portability of the brief**; the §13 purpose is **catching blind spots**. Different goals.

**Go deeper**

- **What you're really testing.** A second assistant tests **portability** (does the brief travel?). A rerun in the same assistant tests **variation** (does it change run to run?). Write down which one you did.
- **Reading the difference:** did results differ in **facts**, **form**, or only **buttons**? Facts need verification; form points to the Deliverable line; buttons don't matter.
- **Not the same as cross-model checking** (*AI Prompting*, §13), whose purpose is catching blind spots with a rubric. Both use a second AI, for different reasons.

> **Urdu:** اچھا بریف کسی بھی AI میں بغیر تبدیلی کے چل جاتا ہے کیونکہ وہ کام بیان کرتا ہے، بٹن نہیں۔ دو نتائج کا موازنہ صرف ایک دن کا مشاہدہ ہے، کسی AI کی درجہ بندی نہیں۔

---

## The Delegation Record (JDI, "Your Delegation Record")

The **one-page record** of a job: **brief, run, check, decision**, plus the second run and what you'll save. **If a line is empty, that is a finding**: a step of the loop hasn't happened yet.

```
DELEGATION RECORD — Job / Date
THE BRIEF      Outcome, Context, Constraints, Authority, Deliverable, Verification
THE RUN        Assistant; messages needed; plan asked first?; plan changed by me?;
               where it drifted and the move that fixed it
THE CHECK      Claim 1 + source + finding; Claim 2 + source + finding;
               anything marked "unverified"
THE DECISION   Accept / Correct / Investigate / Reject + one sentence why
THE SECOND RUN Assistant; finished?; brief changed?; where results differed
WHAT I WILL SAVE ...
```

---

## Six practice jobs: what each one teaches (JDI, "Try this now")

| Job | The lesson hidden in it |
|---|---|
| 1. A purchase you'll make | **Prices are the claim most likely to be stale.** Trace one before trusting the recommendation. Dated prices, local currency |
| 2. A weekly summary | Sources from **last 7 days**; **say when sources disagree** instead of picking silently; mark **single-source** items. It's the job that comes back: after run two, save the brief and use a Project |
| 3. A document to reply to | **Authority: "none"** is a real line. AI stops at understanding and does not draft a reply. Quote each sentence; "not in the source" |
| 4. A letter to send | **"Draft, but do not send."** Don't invent facts; list assumptions. The day AI can send, this becomes a **permission** |
| 5. A plan for a week | The plan is a deliverable you'll **run**. Check every link **before day one**, not on day one. "Ask me before including anything paid" |
| 6. Your own subject, from scratch | Write the brief without looking. **The lines you forget are the lines you still need the course for** |

---

## Where the course sits: six steps of growing delegation (JDI, "Where this leads")

| Step | What you say to AI | Where taught |
|---|---|---|
| Prompt | Tell me something | *AI Prompting in 2026* |
| Collaboration | Help me do something | *AI Fluency* |
| **Delegated job** | **Here is the outcome. Do the work** | ***Just Delegate It*** |
| Workflow | This work happens again and again | *General Agents*, *Workflow Design* |
| AI Worker (Digital FTE) | Own this responsibility | Later courses |
| Agent Factory | Build and run workers as a method | Later courses |

**Deep connection.** *AI Fluency*, §2: three ways to work with AI: **automation** (AI does a defined task), **augmentation** (you and AI think together), **agency** (you configure AI to act independently on future tasks, including for others). Delegating a job is the bridge from augmentation toward agency.

---

## Trade-off table: how much to hand over

| Choice | Reliability | Your effort | Speed | Safety | When |
|---|---|---|---|---|---|
| Just ask a question | Low (unchecked advice) | High later (you do the work) | Fast | n/a | Curiosity only |
| One-sentence job | Medium | Low | Fast | Medium | Low-stakes jobs |
| Recipe (you dictate steps) | Capped by your plan | High | Medium | Medium | Only when steps are real constraints |
| Full six-line brief | High (checkable) | Medium | Medium | High | Anything that matters |
| Brief + plan-first | Highest before running | Medium | Slower start | Highest | New, costly or hard-to-reverse jobs |
| Brief in a Project + standing instructions | High and consistent | Lowest per run | Fastest per run | High, if reviewed monthly | Repeating jobs (2 of 3 test) |

---

## Anti-patterns the exam likes (from this course)

1. Treating asking and delegating as the same thing; judging by prompt length.
2. Dictating steps out of nervousness instead of naming the outcome.
3. Skipping the **Authority** and **Verification** lines.
4. Deleting a brief line instead of writing "none".
5. Assuming AI searched because it says so. Treating a **citation as verification**.
6. Pasting a source without "use only this" and "quote the sentence".
7. Believing a temporary/incognito chat makes pasted private data disappear.
8. Arguing with a stale long chat instead of summarising into a fresh one.
9. Accepting a tidy document without checking that caveats survived.
10. Letting AI start before approving the plan; accepting a **silent change**.
11. Giving send/buy/delete power when draft/research/inspect was enough.
12. Retyping the same background every time instead of using a Project; never reviewing stored context or memory.
13. Using a Project for a repeating **method** (that's a Skill).
14. Rewriting the whole job when a one-line correction would do; never escalating the model.
15. Trusting "I have corrected it" without looking at the result.
16. Endless correction rounds instead of taking it to an expert.
17. Believing accountability passes to AI.
18. Ranking assistants from one run each.

---

## Practice set: 8 questions (built on *Just Delegate It*)

Reply like `1A 2C 3BD 4A 5C 6D 7B 8AC`. Questions 3 and 8 need **two** answers.

**Q1. (D1, moderate)**
An office manager types: "What should I look for when choosing a new printer for our office?" The answer is a helpful list of features. The manager still has to find models, compare prices and choose. What change would best turn this into a delegated job?

- A. Ask for two or three printers available in their country under a stated budget, compared in a table with price, where sold and a link, with one recommended.
- B. Ask the same question with more detail about the office, so the list of features is more specific.
- C. Ask the assistant to explain each printer feature in more depth, so the manager can decide faster.
- D. Ask the same question in a stronger model with thinking turned on.

**Q2. (D1, hard)**
A student sends: "Go to Coursera and Udemy only, find the top three Excel courses on each by rating, copy name, price and length, then tell me the best." The table looks neat, but a friend points out that the best free Excel courses are on other sites. According to the course, what is the underlying problem?

- A. The student wrote a recipe, so the result could be no better than their own plan, and nothing in the result could warn them.
- B. The student forgot to turn on web search, so the assistant used out-of-date ratings.
- C. The student's prompt was too short. Adding more steps would have covered more sites.
- D. The assistant ignored the instructions. It should have searched all sites anyway.

**Q3. (D1, hard) Choose TWO.**
A team lead reviews a colleague's brief: Outcome, Context, Constraints and Deliverable are clear, but there are no Authority or Verification lines. The result arrived with one course chosen by the assistant and no marks on anything. Which **two** statements are correct according to the course?

- A. Without an Authority line, the assistant made decisions silently, and the colleague cannot know a decision was made.
- B. The missing lines only matter once the assistant can act in the world. In a chat window they add nothing.
- C. A Verification line written before the work starts turns reading the result into checking it.
- D. The lines were correctly left out, because a good brief includes only the lines that apply.
- E. The result is trustworthy, because nothing was marked as unverified.

**Q4. (D3, hard)**
An assistant returns a comparison of three accounting software plans, with monthly prices. Two prices come with links; one arrives without a source, and the assistant's message says "I searched for current prices." The owner will buy one plan this week. What should the owner do first?

- A. Treat the unsourced price as possibly remembered and check it first, then open the linked pages, find the sentence with each price, and check each page's date.
- B. Accept all three prices, because the assistant stated that it searched.
- C. Accept the two linked prices, since a citation confirms them, and check only the unsourced one.
- D. Ask the assistant to confirm that all three prices are current.

**Q5. (D3, hard)**
A teacher pastes a 2-page exam policy into a chat and asks, "What is the late-submission penalty?" The answer gives a precise penalty. The teacher cannot find it in the policy. Which change to the prompt best prevents this?

- A. Add "Using only the text below, answer the question, quote the sentence you used, and write 'not in the source' if the text does not say."
- B. Add "Be very accurate and do not make mistakes."
- C. Use a temporary chat so the assistant's memory does not affect the answer.
- D. Attach the policy as a file instead of pasting it.

**Q6. (D6, very hard) What should the user do FIRST?**
A user delegates: "Set up and publish a one-page site for my tutoring business on Netlify." The assistant publishes the site straight away. It includes the user's personal phone number, which was mentioned earlier in the chat. According to the course, what should the user fix first in how they delegate this kind of job?

- A. Write the Authority line to build the page and show it first, and not publish until they say go, and add the constraint "no phone number". Then check the live page for anything private.
- B. Switch to a more capable model, which would have known not to include a phone number.
- C. Stop using connectors for any task that can publish.
- D. Ask the assistant to be more careful with personal information next time.

**Q7. (D5, hard)**
A sales coordinator runs the same weekly competitor summary. Every week they paste the same background about the company, the same list of five competitors, and the same rule: "mark single-source claims". The output format is the same each week. What is the best setup according to the course?

- A. Save the brief as a note and paste it every week, since pasting keeps full control.
- B. Create a Project: put the company background and competitor list in as knowledge, write the rule as a standing instruction, and review the stored content monthly.
- C. Turn on memory and tell the assistant to remember everything about the job.
- D. Build a Skill, because anything that repeats should be a Skill.

**Q8. (D7 and D2, very hard) Choose TWO.**
A user asks an assistant to compare three savings accounts. The result has wrong interest rates. The user corrects it once; it improves. They correct it a second and third time, and each round improves less. The comparison will be sent to their elderly parents to make a decision. Which **two** actions follow the course?

- A. Recognise that repeated shrinking improvements are a signal about the job, and take it to a person who knows the field.
- B. Keep correcting until the rates are right, because each round still improves the result.
- C. Before any further run, try the escalate move: turn on thinking or a stronger model and rerun the same brief. If rates still fail, take the job back.
- D. Ask the assistant to state its confidence in each rate, and accept rates with high confidence.
- E. Run it once in a second assistant, and if both agree, send it without further checks.

---

*Answer keys are held back until you submit. Say "show answers" to reveal them.*

---
---

# PART B: Advanced layer — the deeper ideas behind *Just Delegate It*

*Just Delegate It* teaches the habit for **one job in one chat**. The exam writes its hardest questions one level up: **which steps** of a workflow AI should own, **why** a gate fails, **where** data may go, and **what** caused a bad output. Your other files teach that level. Each section below starts from a JDI idea and takes it deeper.

---

## B1. Delegation is workflow design, not "giving work to AI"

> **🔑 Key points (easy)**
> - Delegation = deciding **who does which part**, and **why**.
> - Three awareness types: the **problem**, the **platform** (right AI), the **task split**.
> - Business rules (limits, approvals, send vs draft) are **your** decisions, written in Authority.
> - Better question: not "Can AI do it?" but "Which parts should AI do?"

**JDI idea:** give AI the job (§1–§3).
**Deeper** (*AI Fluency*, §3): **Delegation** means deciding how the work is divided between human and AI. It has three parts:

| Part | Question | JDI line it feeds |
|---|---|---|
| **Problem awareness** | What is the goal? Who is it for? What does success look like? What could go wrong? Where is human judgment essential? | Outcome, Verification |
| **Platform awareness** | Which kind of AI fits: reasoning model, search-enabled assistant, coding agent, agent-capable system? | (JDI §4, §9, §11) |
| **Task delegation** | Which parts does AI do, which do I do, and **why**? | Authority |

**The invoice-agent example.** "Build me an invoice-chasing agent" leaves the real questions open: which customers, how many days late, what tone, **above what amount must a human approve**, what if the customer disputes, which system may it read, **may it send or only draft?** "These are not prompting questions. They are **business questions**. AI cannot decide your business policy unless you deliberately give it that authority, and in many cases you should not."

**Deep point for the exam:** a brief's **Authority line is where business policy lives.** A missing Authority line doesn't mean "no policy". It means AI invented one silently (JDI §3).

**The better question.** Not "Can AI do this?" but **"Which parts should AI do, which parts should I do, and why?"**

**Go deeper**

- **Why business questions can't be left to AI.** "Above what amount must a human approve?" is policy. If you don't state it, AI either invents one or never asks. Both are delegation failures, not prompt failures.
- **Worked split** (*AI Fluency*, §3.3): Human decides goals, verifies facts, adds lived experience, approves the final version. AI suggests structures, drafts, fixes grammar. Mixed: AI offers options, human chooses.

> **Urdu:** کام سونپنا صرف AI کو کام دینا نہیں، بلکہ یہ طے کرنا ہے کہ کون سا حصہ AI کرے گا اور کون سا انسان، اور کیوں۔ کاروباری اصول AI خود طے نہیں کر سکتا۔

---

## B2. Three modes: automation, augmentation, agency (*AI Fluency*, §2)

> **🔑 Key points (easy)**
> - **Automation** = do this task. **Augmentation** = think with me. **Agency** = pursue this goal for me.
> - Agency = AI set up to do **future** tasks, possibly **for other people**, while you're not there.
> - In agency, judgment must be **built in beforehand**, because nobody is watching.
> - One project can use all three modes.

| | Automation | Augmentation | Agency |
|---|---|---|---|
| You say | "Do this task" | "Help me think" | "Pursue this goal for me" |
| You provide | The task or steps | Back-and-forth thinking | **Goal and boundaries** |
| AI decides | Very little | Suggestions | **Many next steps** |
| Your role | Script writer | Thinking partner | Director (often not watching) |
| Common failure | A step done badly | Sycophantic partner | **Goal or boundary misunderstood** |

**The precise definition of agency** (a favourite exam trap): a human **configures** AI to independently perform **future** tasks, including **for others**, on their behalf.
- **Future** = you are not in the room.
- **For others** = the person served may not be you (your customer or student talks to it).

Because you can't supervise every decision, **"the judgment has to be built in beforehand."** That is why JDI's Authority and Verification lines grow into permissions, gates and evals later.

**Where JDI sits:** a delegated job in a chat is between automation and agency. You give an **outcome** (not steps), but you are still watching and you accept each result yourself. The same course question from *AI Fluency*'s assessment asks exactly which detail separates agency from automation most sharply: **future tasks, including for others**.

No mode is better. One project may use all three: automate extraction, augment thinking about exceptions, give an agent limited authority over routine cases.

**Go deeper**

- **Different failure types.** In automation a *step* goes wrong (easy to spot). In agency the *goal or boundary* is misunderstood (harder to spot, because every step can look right).
- **Where the exam hides it:** options that describe agency as "AI doing many tasks" or "AI being autonomous" miss the two defining words: **future** and **for others**.

> **Urdu:** ایجنسی کا مطلب ہے کہ آپ AI کو آئندہ کے کام خود سے کرنے کے لیے ترتیب دیں، دوسروں کے لیے بھی، جب آپ موجود نہ ہوں۔ اس لیے فیصلے کی حدیں پہلے سے طے کرنی پڑتی ہیں۔

---

## B3. Ownership per step: the three criteria (*Workflow Design*, §5–§6)

> **🔑 Key points (easy)**
> - Classify every step: **AI-appropriate**, **human-retained**, or **collaborative**.
> - Only three questions decide: **Can it be undone? What does a mistake cost? Is this the actual decision?**
> - Not a score. **The strictest answer wins.**
> - How well AI did in testing is **not** a reason.
> - A step can be given to AI only if **someone checks it afterwards** when stakes are high.

**JDI idea:** AI owns the middle of the loop; you own both ends.
**Deeper:** in a real workflow, decide ownership **step by step**. Classify each step:

- **AI-appropriate**: AI may own it.
- **Human-retained**: a person owns it outright.
- **Collaborative**: AI produces, **a named person judges**.

**Only three criteria decide it:**

| Criterion | Question | Example |
|---|---|---|
| **Reversibility** | Can the step be undone if AI is wrong? | A draft can be rewritten. A sent email cannot be unsent |
| **Stakes** | What does a mistake cost **in the bad case** (not on average)? | Misfiled label = a minute. Wrong penalty figure = the penalty |
| **Accountability** | Is this step **the decision** somebody answers for, or an **input** they judge before it acts? | An input can be handed over (accountability sits at the judging). The decision itself cannot |

**Rules that make this hard:**
1. **It's three questions, not a score.** Usually one criterion decides; **name it**, so others can check your call.
2. **Where they disagree, the strictest wins.** Reversible and cheap but still *the decision* → stays human.
3. **How well AI did in your test run is NOT a criterion.** (See B4.)
4. A **fourth criterion** (needs human creativity or empathy) answers a *different* question: whether the **whole use case** belongs with AI at all (eligibility), not who owns a step.
5. Accountability **never** moves onto the machine, "because the machine cannot be asked."

**Contract review map (the classic example):**

| Step | Owner | Deciding criterion |
|---|---|---|
| Extract clauses | AI | Reversible, low stakes |
| Flag departures from playbook | AI | Reversible; errors surface at the redline |
| Draft redline + rationale | **Collaborative** | High stakes, human judges each edit |
| Compute penalty exposure | AI (by **code execution**) | Reversible **and checked at the next gate** |
| Approve/reject each change | **Human** | This is the decision |
| Sign and send | **Human** | Irreversible, externally binding |

**Two subtle rows the exam loves:**
- **Penalty exposure:** being arithmetic does **not** make it low-stakes. It is safe to hand over only because a human gate sits at the next row. "Take that gate away and the step stops being AI-appropriate, even though the arithmetic has not changed." "Must be computed" is **how** it's carried, never **why** it's delegated.
- **Playbook flags:** AI-appropriate only because someone reads the flags next. Move the same step to a workflow where **nobody reads them after** (e.g. expenses vs travel policy) and it becomes **collaborative**. "The step did not change. What changed is whether anybody is standing after it."

**Go deeper**

- **The penalty-exposure lesson.** A computed figure is safe to delegate only because a human approves at the next step. Remove that gate and the same arithmetic becomes collaborative. **Ownership depends on what stands after the step.**
- **Input vs decision.** A step that produces an input someone judges can be delegated (accountability sits at the judging). A step that *is* the decision cannot.
- **Two maps, same pattern** (*Workflow Design*, §6): in contract review and onboarding, mechanical and draft steps went to AI; the confirming step and the irreversible step stayed human. The criteria decided, not taste.

> **Urdu:** ہر قدم کے لیے تین سوال: کیا یہ واپس ہو سکتا ہے؟ غلطی کی قیمت کیا ہے؟ کیا یہی اصل فیصلہ ہے؟ اگر جواب مختلف ہوں تو سب سے سخت جواب جیتتا ہے۔ AI نے ٹیسٹ میں کتنا اچھا کیا، یہ معیار نہیں ہے۔

---

## B4. How delegation goes wrong over time (*Workflow Design*, §7)

> **🔑 Key points (easy)**
> - Trust is earned **per step**, not across steps.
> - **Halo delegation**: giving AI a new step because a different step went well.
> - **Unstaffed gate**: the review still exists on paper but nobody really does it.
> - **A step can't give itself permission** to skip review.
> - Keep asking: are my review gates still staffed?

**JDI idea:** "Trust grows with a record" (§7): first run read everything, fifth clean run read the plan.
**Deeper and more careful:** trust is earned **per step**, not across steps. Four errors, all of which "look reasonable at the moment they happen":

| Error | What happens | Why it's tempting |
|---|---|---|
| **Over-delegation** | AI gets more than the step's risk allows | Good results week after week |
| **Halo delegation** | A step goes to AI **because the previous step went well** | The competence was real, just for a different step |
| **Unstaffed gate** | A collaborative step's review decays into a glance, then a click | Busy reviewer, long queue, good drafts for months. **The map still says "reviewed"** |
| **Mapping the tool, not the work** | The workflow grows a step shaped like a tool you like | The tool really is good; it just isn't the work |

> **"Drafting quality is evidence about the draft. It is not evidence about the decision."**
> **"Bad maps are built from true statements about the wrong step."**
> **"A step cannot give itself permission to skip the gate."** (If AI sets severity and then sends "low severity" replies unreviewed, the same system has approved itself.)

**Checking order:** map the work **with no tools in mind**; classify each step on its own; then ask of every collaborative step **who reviews, and when**. Keep asking: **"Are the gates I designed still being staffed?"**

**Connection to JDI §10:** a result that passes review **earns AI similar jobs; it never earns your name on the result.** Trust widens what AI may *try*, never who is *accountable*.

**Go deeper**

- **Why these errors feel reasonable.** Each one comes from true evidence about the wrong step. "Bad maps are built from true statements about the wrong step."
- **The maps don't show decay.** A map records what you designed, not what is running. Only a scheduled check reveals an unstaffed gate.
- **Worked diagnosis** (*Workflow Design*, §7): severity classification given to AI because summaries were good = halo; auto-sending "low severity" = over-delegation that approves itself; a template shaped by a favourite Skill = mapping the tool.

> **Urdu:** اگر AI ایک قدم پر اچھا کام کرے تو اس کا مطلب یہ نہیں کہ اگلا قدم بھی اسے دے دیا جائے۔ مسودہ اچھا ہونا فیصلے کے اچھا ہونے کا ثبوت نہیں۔ یہ بھی دیکھتے رہیں کہ جانچ کرنے والا واقعی جانچ رہا ہے یا نہیں۔

---

## B5. Authority, deeper: gates, ladders and thresholds

> **🔑 Key points (easy)**
> - Safety is a **stack** of controls, not one approve button.
> - **Action ladder** = what can this action do to the world? **Review thresholds** = must a person see the result?
> - Pick the safety level **before** the run.
> - Read ≠ send, draft ≠ publish, view ≠ edit. Give the **smallest** access.
> - Text inside a web page or email is **information, never an order**.

**JDI idea:** research not purchase; draft not send; inspect not delete; choose but say (§7).
**Deeper** (*General Agents*, §6–§8):

**1. A gate is a stack, not a button.** Several layers can apply at once: the connector's permission scope, organisation policy, the task's **approval mode**, safety screening, explicit approval for destructive actions, and escalation to your phone. The better questions are: **"What is allowed to happen without me? What mechanism stops or screens it before it counts?"**

**2. Two different "sets of four" — keep them apart:**

| | Autonomy ladder (the **action**) | Review thresholds (the **result**) |
|---|---|---|
| Asks | What can this action do to the world? | Must a person look at the output before it counts? |
| Items | 1 read/summarise → 2 draft, don't send → 3 write reversible records → 4 send, publish, purchase, delete, change critical data | Stakes, reversibility, audience, regulatory exposure |
| Decides | The **gate on the action** (e.g. Manual approval at rung 4) | The **review on the result** |

A rung-1 summary still needs review if it goes to a **client** or uses **regulated** data.

**3. Choose the gate before the run.** "If you decide autonomy when the prompt appears, you are designing the safety system too late." Test the escalation path once on purpose ("ring the gate"): "An untested escalation path is only an assumption."

**4. Plan-first is an instruction, not a mode.** In Cowork, **Manual mode does not automatically produce a plan** for approval. If you want JDI's plan-first, **write it in the brief**.

**5. Read is not send, draft is not publish, view is not edit.** Write access is a separate increase in **blast radius** (the worst damage a wrong action can do). Grant the smallest scope that completes the job.

**6. Outside content is evidence, never a new boss.** **Prompt injection** = hidden instructions in a page, email or document. Your brief is the authority. The danger peaks when an agent can **both** read untrusted content **and** take a consequential action.

**Go deeper**

- **Ring the gate on purpose.** Before trusting unattended work, create one harmless step that needs your input, walk away, and confirm the request actually reaches you. An untested escalation path is only an assumption (*General Agents*, §7).
- **Default ≠ recommendation.** A product may default to automatic approval. For unfamiliar tools, signed-in sites or high-consequence actions, switch to Manual while learning.
- **The risky combination:** the agent can read untrusted content **and** take a consequential action. That's when prompt injection matters most.

> **Urdu:** عمل کا خطرہ (کیا یہ دنیا میں کچھ بدل دے گا؟) اور نتیجے کی جانچ (کیا انسان کو دیکھنا لازمی ہے؟) دو الگ سوال ہیں۔ حفاظتی دروازہ کام شروع ہونے سے پہلے طے کریں، اور باہر کے مواد میں لکھی ہدایات کو کبھی حکم نہ سمجھیں۔

---

## B6. Before delegating at all: is this use case appropriate? (*Governance*, §1)

> **🔑 Key points (easy)**
> - Before delegating, ask: **should AI do this at all?**
> - Three answers: **fully appropriate**, **appropriate with review**, **inappropriate**.
> - Name the **deciding factor** in one sentence.
> - "Someone will check it" is not a control. A real one says **who, what, when**.

JDI starts from "give AI the job". Governance asks the question **before** that: **may AI do this work?**

**Three answers for any use case:**

| Answer | Meaning | Examples |
|---|---|---|
| **Fully appropriate** | Low consequence, reversible, easy to review as you go | Internal FAQ from approved sources, restructured notes |
| **Appropriate with review** | Useful, but a **specific human check** must happen before use | Billing reply to a customer, management summary from financials, a shortlist |
| **Inappropriate** | Stays human-owned; review can't repair the consequence | **Final** medical, legal or disciplinary determinations. AI may *support*, not decide |

**Find the deciding factor.** Ask: "If one answer changed, which change would move this into a different classification?" Say it as a checkable sentence: *"This is appropriate with review because the organisation stays accountable for the factual claim."* Not "this feels risky."

**"A human in the loop is not a gate."** A **defined gate** names:
- **Who** reviews (the role that holds responsibility)
- **What** they verify (the specific risk)
- **When** (before the output becomes hard to undo)

"Someone will check it" is an **intention**. "The account manager checks delivery facts against the dispatch record before the report is sent" is a **control**. "If you cannot write the gate in that form, the workflow is not ready to run."

**Consequence ≠ accountability.** A high-consequence task isn't automatically prohibited (a good gate may restore control). A low-consequence task may still need a human "because the relationship is the point" (a condolence message).

**Go deeper**

- **Consequence vs relationship.** A condolence message is easy to rewrite, yet may need a human because "the relationship is the point". A high-stakes task may still be delegable with a strong gate.
- **Don't add up the criteria.** Use them to explain why a case sits in one category, via the deciding factor.

> **Urdu:** کام سونپنے سے پہلے پوچھیں کہ کیا AI کو یہ کام کرنا بھی چاہیے۔ "کوئی دیکھ لے گا" کوئی کنٹرول نہیں۔ اصل کنٹرول بتاتا ہے کہ کون، کیا، اور کب جانچے گا۔

---

## B7. Data before delegation: tiers and redaction (*Governance*, §2; *AI Fluency*, §6.1)

> **🔑 Key points (easy)**
> - Data has three levels: **green** (OK), **yellow** (check first), **red** (not through unapproved tools).
> - Ask: does the job need **who** it is, or only the **pattern**?
> - Removing names isn't enough if other details still point to one person.
> - "Customer 17" with a list that maps back = **not anonymous**.
> - Clean data still needs an **approved tool**.

**JDI idea:** remove names and private details before pasting; temporary chat ≠ disappearance (§5).
**Deeper:**

**Three data tiers** (translate to your organisation's labels):

| Tier | Contents | Rule |
|---|---|---|
| **Green** | Public, aggregated, approved internal, **anonymized** data | Generally permitted |
| **Yellow** | Internal-only docs, contact details, customer/employee IDs, confidential drafts, unannounced deals | Check first or add a control |
| **Red** | Credentials, secrets, highly regulated data, privileged (e.g. lawyer–client), third-party confidential, licensed material that can't be copied | Not through an unapproved route |

Unsure between two? **Use the more sensitive one.**

**The key question (the "discriminator"):** **Does the task need the identifiers, or only the pattern?** Spending trends need the pattern. Reconciling one account needs the identifier.

**Redaction fails two ways:**
1. **Partial**: a rare job title, exact date, region or age can identify a person as surely as a name. ("The only student who missed the week 3 lab" names that student.)
2. **Task-breaking**: you removed what the task needs, so the result is safe and useless.

**Pseudonymized ≠ anonymized.** Replacing names with "Customer 17" while someone still holds the mapping list = **pseudonymized**, and the data **keeps its tier**. Your organisation's anonymization standard, not relabeling, is what lets the tier drop.

**Test for redaction** (*AI Fluency*, §6.1): could someone reading **only what you pasted** work out who it is about? And stripping data **does not answer the tool question**: is this tool approved at all?

**Go deeper**

- **Two redaction failures:** too little (a rare job title plus an exact date still identifies someone) and too much (the task becomes useless). The test: could someone reading only what you pasted work out who it is about?
- **When the tier really drops:** the mapping list is gone and the task needed only the pattern, judged by your organisation's anonymization standard, not by relabeling.

> **Urdu:** پہلے پوچھیں: کیا کام کو شناخت چاہیے یا صرف پیٹرن؟ نام ہٹانا کافی نہیں اگر باقی تفصیلات سے شخص پہچانا جا سکے۔ "کسٹمر 17" لکھنے سے ڈیٹا گمنام نہیں ہوتا اگر کسی کے پاس اصل فہرست موجود ہو۔

---

## B8. Diligence: the three kinds of responsibility (*AI Fluency*, §6)

> **🔑 Key points (easy)**
> - Three responsibilities: choose tool and data well, **be honest** about AI's role, **check before sending**.
> - The more a result affects others, the stronger the case for telling them.
> - Numbers a decision depends on must be **calculated, never guessed**.
> - Unsure if it's fair? Ask the four questions or **escalate**. Don't guess.
> - **AI can automate work, not accountability.**

JDI §10's rule ("accountability stays with you") is one part of **Diligence**, which has three:

| Kind | Question | JDI link |
|---|---|---|
| **Creation diligence** | Is it responsible to use *this tool* with *this data*? Approved? Personal or confidential data? Legal limits? | §5 privacy |
| **Transparency diligence** | Should people know AI helped? The more a result **affects others**, the stronger the case | (not in JDI) |
| **Deployment diligence** | Verify before it's published, sent, executed or used in a decision. More reach = more checking; irreversible = check **before** the act | §10 |

**The numbers rule:** any number a decision rests on must be **computed, never generated**. A model summarising a report "predicts a likely-looking total, so the total can be wrong while every line item is right." Then check the **inputs** (right rows? right rate?), not just the sum.

**Unclear cases** (e.g. an AI-ranked applicant shortlist that may favour two universities). Ask four questions: Who is affected (including people who'll never see it)? What could go wrong for them, and would they know? What would a fair outcome look like? What should be disclosed, and to whom? If you can't answer, **escalate to the decision owner**. "Guessing is the one option that turns an unclear case into your mistake."

**Policy friction:** if the approved tool needs a form and a week while the unapproved one is one click away, "the easy path is a policy flaw, not only a personal one." Tell the policy owner.

> **"AI can automate work. It cannot automate accountability."**

**Go deeper**

- **Checking scales with reach and reversibility** (*AI Fluency*, §6.3): a note to yourself gets a glance, a customer email a full read, a regulator report a second reviewer; anything irreversible is checked **before** the act.
- **Check inputs, not just the sum.** Right rows? Right rate? A model can produce a wrong total while every line item is right.
- **Policy friction is a design flaw.** If the approved tool is hard to reach, people use the easy unapproved one. Report where it was hard.

> **Urdu:** ذمہ داری کے تین پہلو ہیں: درست ٹول اور ڈیٹا چننا، جب لوگوں پر اثر ہو تو AI کے کردار کے بارے میں ایماندار ہونا، اور بھیجنے سے پہلے جانچنا۔ فیصلے والے نمبر ہمیشہ حساب سے نکالیں، اندازے سے نہیں۔

---

## B9. The science under the brief: context engineering

> **🔑 Key points (easy)**
> - AI only sees what's on its **"desk"** (the context window) right now.
> - It remembers nothing between turns by itself (**stateless**).
> - More files ≠ better. **Remove** what isn't needed.
> - Keep standing instructions **short** and prune them.
> - The brief is **context engineering** for one job.

**JDI ideas:** Context line (§3), give the source (§5), stale chat (§5), Projects and monthly review (§8).
**Deeper** (*AI Prompting in 2026*, §4; *What AI Actually Is*, §5; *AI Fluency*, §4):

- **The context window is a reading desk.** Everything the model can use for this answer is on the desk; anything not on it **does not exist** for this answer. The model is **stateless**: it keeps nothing between turns; the desk is rebuilt from stored text before every reply.
- **Six layers land on the desk:** the company's **system prompt**, **tool descriptions**, your **prompt**, **chat history**, **uploaded files**, and **memory** (notes the tool writes about you).
- **Recall drops as the window fills.** This is why JDI §5 says a long chat "loses track" and why the fix is **summary → fresh chat**, not arguing.
- **Curating means removing as well as adding.** "Every extra file is one more thing the model can misread." Drop unneeded attachments, remove near-duplicates, label what each file is for.
- **Standing instructions pile up.** Keep your own layer short; review every few months and delete any line whose removal wouldn't make the AI go wrong. (The file notes Anthropic deleted most of its own accumulated standing instructions in July 2026 with no quality loss.) This is the deeper reason for JDI §8's monthly review.
- **Prompt engineering vs context engineering** (*AI Fluency*, §4): prompt engineering asks how to phrase this message; context engineering asks **what information must be available** for AI to succeed. "A well-written prompt cannot rescue an agent that has the wrong data, missing rules, poor examples, or no access to the tools it needs." The Delegation Brief is context engineering for one job; a **system prompt** makes it permanent; a `SKILL.md` makes a process reusable.

**Go deeper**

- **Six layers on the desk:** system prompt, tool descriptions, your prompt, chat history, files, memory. Anything not on the desk doesn't exist for that answer.
- **Recall drops as the desk fills.** This is the mechanism behind JDI's "long chat goes stale" advice.
- **Prompt vs context engineering** (*AI Fluency*, §4): phrasing can't rescue an agent that lacks the right data, rules, examples or tools.

> **Urdu:** ماڈل صرف وہی دیکھ سکتا ہے جو اس کی "میز" (کانٹیکسٹ ونڈو) پر رکھا ہو۔ زیادہ مواد ہمیشہ بہتر نہیں؛ غیر ضروری فائلیں ہٹائیں۔ مستقل ہدایات کو مختصر رکھیں اور وقتاً فوقتاً صاف کریں۔

---

## B10. Why we verify easy-looking things: the jagged frontier (*What AI Actually Is*, §7)

> **🔑 Key points (easy)**
> - AI can be brilliant at a hard task and fail an **easy** one next to it.
> - Weak spots: letters, **very recent** facts, **your private** context, rare topics.
> - So check the easy-looking claims too, especially prices, dates, links.
> - Different models fail in different places; re-test from time to time.

**JDI idea:** verify the claims that matter (§10); run the brief in a second AI (§11).
**Deeper:** AI ability is **jagged**, superhuman on one task and "startlingly incompetent" on a neighbouring one that looks no harder (a legal clause vs counting letters in "strawberry"). Weak spots: individual letters, very recent events, **your private context**, rare topics.

| Habit | Why |
|---|---|
| Don't assume a win on a hard task means a win on an easy one | They may sit on opposite sides of the frontier |
| **Verify across the boundary, not in the middle** | The dangerous errors are easy-looking tasks it fails **without warning** |
| Try the same task in two or three models | Frontiers have different shapes; one catches what another drops |
| Re-test on a schedule | The frontier moves with each model release |

**Connection:** this is the deeper reason JDI §4 says the stale-price, date and link claims deserve checking first: they are **recent, specific, and private-context** facts, all on the weak side of the frontier.

**Go deeper**

- **Why the frontier is jagged:** strong where tasks appeared often and clearly in training text; weak on letters, recent events, private context, rare topics. It doesn't follow human ideas of "easy" and "hard".
- **Verify across the boundary, not in the middle:** the dangerous errors are the easy-looking tasks it fails without warning.

> **Urdu:** AI مشکل کام بہت اچھا کر سکتا ہے مگر کوئی آسان سا کام غلط کر دیتا ہے۔ اس لیے آسان نظر آنے والی چیزیں بھی جانچیں، خاص طور پر تازہ، مخصوص یا نجی معلومات۔

---

## B11. Intervene, deeper: diagnose by timing (*Workflow Design*, §11–§12)

> **🔑 Key points (easy)**
> - Ask **when** the problem started.
> - Wrong from the start → **missing information** in the prompt.
> - Good, then worse → **chat too long**; summarise and restart.
> - Same kind of mistake every time → **wrong tool or model**.
> - Used to work, now doesn't → **outdated settings/files**. Do the cheapest check first.

**JDI idea:** six Intervene moves chosen by symptom (§9).
**Deeper:** before choosing a move, ask **"When did the symptom first appear?"** Timing tells you **where to look first**, not the final cause.

| When it appeared | First hypothesis | Cheap check (under a minute) | Fix | Matching JDI move |
|---|---|---|---|---|
| Wrong from the **first answer** | **Under-specification** | Re-read the prompt: is the missing thing in it? | Add what was left out | Correct / add a Constraint line |
| Started fine, **then degraded** | **Context overload** | Restate the instruction in a fresh session. Does it hold? | Restart or summarise | JDI §5: summary → fresh chat |
| **One repeatable** error type | **Wrong feature or model (tier)** | Run once with the right feature or a stronger tier | Change feature/tier (e.g. code execution for numbers) | **Escalate** |
| **Used to work**, now doesn't | **Stale configuration** | Open the instruction/knowledge source and check its **date** | Maintain the config | JDI §8 monthly review |

- **Cheapest first.** Each check can come back negative. That's not wasted: you ruled out the likeliest cause.
- **Stale configuration fails silently**: no error, perfectly formatted output quoting last quarter's figures. It is "the twin of the unstaffed gate": a control set up correctly, decaying while everyone assumes it holds. **A scheduled review finds both.**
- When handing a problem to someone else, **name where the failure lives**: the prompt, the context, the feature choice, or the task itself.

**Go deeper**

- **Timing is free information** you already have. Each quick check can come back negative, which still helps by ruling out the likeliest cause.
- **Stale configuration and unstaffed gates are twins:** both are controls set up correctly that decay silently. A scheduled review finds both.
- **When handing over a problem,** name where it lives: prompt, context, feature choice, or the task itself.

> **Urdu:** مسئلہ کب شروع ہوا؟ پہلے جواب سے غلط ہو تو ہدایت نامکمل تھی؛ بعد میں خراب ہوا تو چیٹ بہت لمبی ہو گئی؛ ایک ہی قسم کی غلطی بار بار ہو تو غلط ماڈل یا فیچر؛ پہلے ٹھیک چلتا تھا اب نہیں تو پرانی سیٹنگ۔ سب سے سستی جانچ پہلے کریں۔

---

## B12. From a job to a workflow to a worker

> **🔑 Key points (easy)**
> - Others depend on your tool → it's now **infrastructure**; get engineering help.
> - Same solution three times → it can become a **reusable worker/Skill**.
> - The same 4Ds (Delegation, Description, Discernment, Diligence) scale up to full systems.
> - At scale, check **some successes too**, because systems can fail silently.

**JDI idea:** the brief grows as work leaves your sight; six steps from prompt to Agent Factory.
**Deeper:**

**Two signals that sound alike** (*Workflow Design*, §10):

| Signal | Meaning | Where it goes |
|---|---|---|
| **Other people now depend on this** (the **escalation signal**) | It is infrastructure: uptime, access control, someone to call, a guarantee it still works like in March | Developer/architect expertise. Escalating is a correct answer, not failure |
| **I've solved this the same way three times** | The method is stable and can be manufactured | Turn it into a reusable worker/Skill |

Compare JDI §8: **third paste of the same context → Project**; **same method each time → Skill**; **team relies on it → workflow**; **others depend on it as infrastructure → engineering**.

**The 4Ds at system scale** (*AI Fluency*, §7, bookkeeping Digital FTE):

| Competency | In a chat (JDI) | In a system |
|---|---|---|
| Delegation | Decide what to ask AI | Scope the worker: may match and flag and draft; **humans approve every journal adjustment and write-off**; high-value items escalate to a named person |
| Description | The brief | Chart of accounts, matching rules, past examples, report format, escalation rules, "never post a journal entry", "never contact a client" |
| Discernment | Verify the result | Test against **past reconciliations already trusted**; check correct matches, wrong matches that slip through, right escalations, **over-escalation**, drift over time; **review some apparent successes**, because "a system can look safe simply by failing without saying so" |
| Diligence | Own the result | Data stays in approved infrastructure; actions logged; disclosure where required; **a human partner signs** |

**10-80-10 and the 4Ds:** first 10% set direction (Delegation, Description); middle 80% orchestrate (Description, Discernment repeat); final 10% judge the truth (Discernment); Diligence surrounds all 100%.

**Go deeper**

- **Escalating is correct, not failure.** The real failure is running something by prompt after other people depend on it, "because nobody marked the moment it stopped being small."
- **Bookkeeping example lesson:** the agent may match, flag and draft; humans approve every adjustment and write-off; a partner signs. The personal habits from JDI became system rules.

> **Urdu:** جب دوسرے لوگ آپ کے بنائے ہوئے ٹول پر انحصار کرنے لگیں تو وہ انفراسٹرکچر بن جاتا ہے اور اسے ماہر انجینئر کی ضرورت ہے۔ بڑے نظام میں بھی وہی چار مہارتیں (4Ds) کام کرتی ہیں، صرف پیمانہ بڑا ہوتا ہے۔

---

## B13. Master map: each JDI concept and its deeper principle

| JDI concept | Deeper principle | Where |
|---|---|---|
| 1 Asking vs job | Delegation = dividing work deliberately; problem, platform, task awareness | *AI Fluency* §3 |
| 2 Outcome not clicks | Product vs process description; brief the problem, not the program | *AI Fluency* §4; *Code You Never Write* §5 |
| 3 Brief | Context engineering; Authority = business policy | *AI Fluency* §3–§4; *AI Prompting* §4 |
| 4 Research | Three retrieval modes; jagged frontier on recent facts | *AI Prompting* §3; *What AI* §7 |
| 5 Source | Context window is all it sees; data tiers; redaction; pseudonymized ≠ anonymized | *What AI* §5; *Governance* §2 |
| 6 Deliverable | File tiers: finished work exits the platform | *General Agents* §5 |
| 7 Authority | Gate stack; autonomy ladder vs review thresholds; blast radius; injection | *General Agents* §6–§8 |
| 8 Job again | State spine layers; prune standing instructions; stale config fails silently | *General Agents* §4; *AI Prompting* §4; *Workflow* §11 |
| 9 Intervene | Diagnose by timing, cheapest check first | *Workflow* §11–§12 |
| 10 Verify | Three criteria per step; defined gate; diligence; halo delegation; unstaffed gate | *Workflow* §5–§7; *Governance* §1; *AI Fluency* §6 |
| 11 Different AI | Cross-family checks; frontiers differ; progress signal not truth | *AI Prompting* §13; *What AI* §7 |

---

## B14. Advanced anti-patterns

1. Treating the Authority line as optional ("AI will figure out the policy").
2. Defining agency as "AI doing tasks" instead of configuring **future** tasks, including **for others**.
3. Using AI's test-run performance as the reason to delegate a step.
4. Adding up the three criteria like a score, or letting the most lenient one win.
5. Delegating a computed figure because "it's just arithmetic" when no gate follows it.
6. Halo delegation: giving the decision step to AI because the draft step went well.
7. Writing "a human will review" with no who, what, when; never checking the gate is still staffed.
8. Letting a step approve itself ("low severity only" where AI set the severity).
9. Confusing the autonomy ladder with the review thresholds.
10. Assuming Manual approval mode means plan-first.
11. Following instructions found inside an email or web page.
12. Calling pseudonymized data anonymous; redacting names but leaving a unique combination of details.
13. Thinking stripped data answers the "is this tool approved?" question.
14. Adding attachments or standing instructions forever instead of curating and pruning.
15. Treating a slow, silent quality drop as a prompt problem instead of stale configuration.
16. Keeping a tool on prompt-and-iterate after other teams depend on it.
17. Judging a system only by its visible failures, never sampling its apparent successes.

---

## B15. Advanced practice: 6 very hard questions

Reply like `9B 10AD 11C 12A 13BE 14D`. Questions 10 and 13 need **two** answers. (Numbered 9–14 so they follow the first set.)

**Q9. (D4, very hard)**
A legal team's workflow: (1) AI extracts clauses; (2) AI computes the financial exposure of each penalty clause using code execution; (3) the figures go straight into an automated weekly risk dashboard that executives use to decide which contracts to renegotiate. Nobody reviews step 2's output before it reaches the dashboard. The computation has been correct in every test. How should step 2 be classified?

- A. AI-appropriate, because it is computed by code execution rather than written, and it has been correct in every test.
- B. Not AI-appropriate as designed. It is safe to hand to AI only if a human gate reviews the figures before they drive decisions. Without that gate it should be collaborative.
- C. Human-retained, because any financial figure must always be calculated by a person.
- D. AI-appropriate, because accountability sits with the executives who make the final decision.

**Q10. (D4, very hard) Choose TWO.**
A support team's map says: "AI summarises each complaint (its summaries have been excellent for three months), so AI also classifies severity. Low-severity replies are drafted and sent by AI without review." Which **two** problems does this map contain?

- A. Halo delegation: severity classification was handed over because a different step, summarising, went well.
- B. Under-specification: the summarising prompt needs more detail.
- C. Context overload: three months of complaints have filled the context window.
- D. A step granting itself permission: the same system that sets severity then uses "low severity" to skip the review gate before an irreversible send.
- E. Mapping the tool instead of the work, because an AI summary is used at all.

**Q11. (D6, hard)**
A school wants to use an approved AI tool to find patterns in why students miss assignments. The dataset has names, student IDs, class, the exact date of each missed assignment and a free-text reason. The analysis only needs the patterns. What is the best first move?

- A. Replace each name with "Student 1, Student 2…" and keep a mapping list so staff can follow up. The data can then be treated as anonymous.
- B. Remove only the names, keep everything else, and run the analysis.
- C. Confirm the task needs only the pattern, then remove the identifiers the task doesn't need. Check that no remaining combination of details (such as a rare class plus an exact date) points to one student, and follow the school's standard for treating the data as anonymized.
- D. Don't use AI at all, because student data is always in the red tier.

**Q12. (D7, hard)**
For two months, a Project-based weekly market brief was accurate. This month it quotes last quarter's prices, perfectly formatted, with no error or warning. The brief, the model and the prompt haven't changed. What is the most likely cause and the cheapest first check?

- A. Stale configuration: open the Project's knowledge files and standing instructions and check their dates.
- B. Under-specification: rewrite the brief with more detailed constraints.
- C. Context overload: the chat is too long, so start a fresh chat.
- D. Wrong model: move to a stronger tier with thinking turned on.

**Q13. (D6 and D2, very hard) Choose TWO.**
A clinic uses AI to draft patient appointment-summary letters. The written process says "a staff member will review letters before they go out". An audit shows reviewers now approve about 200 letters an hour, and two letters with wrong medication names were sent. Which **two** actions best fix the control?

- A. Add "Double-check medication names carefully" to the drafting prompt.
- B. Redefine the gate with who reviews (a named clinical role), what they check (medication names and doses against the patient record), and when (before sending), and make sure the reviewer has capacity to do it.
- C. Switch to a more capable model, since review has been unreliable.
- D. Let AI send letters without review when its confidence is high, so reviewers can focus on the rest.
- E. Add a regular sample review of sent letters and a named owner who checks the gate is still being staffed, since the review decayed without anyone changing the map.

**Q14. (D4, very hard)**
An analyst built a dashboard artifact by prompting for their own team. Six months later three departments open it every Monday, and one copies its numbers into a board report. It still works. What does the course say is the right next step?

- A. Keep improving it with better prompts. It still works, so nothing needs to change.
- B. Turn it into a Skill, because it has been used many times.
- C. Add a line to the brief saying the dashboard is used by three departments.
- D. Treat dependency as the escalation signal: it has become infrastructure, with needs like uptime, access control, an owner to call and consistency over time, so bring in developer or architect expertise.

---

*Answer keys for Part B are also held back until you submit.*
