# AI Fluency: A Crash Course — Complete Explanation
> Source: [agentfactory.panaversity.org/docs/ai-fluency-crash-course](https://agentfactory.panaversity.org/docs/ai-fluency-crash-course)  
> Framework by Prof. Rick Dakan & Prof. Joseph Feller (produced with Anthropic)  
> Explained simply — every concept, every sub-concept, nothing skipped.

---

## The Opening Scenario — Why This Matters

Imagine a talented new colleague joins your team. On her first morning you say:

> "Prepare a course outline on AI agents."

A few hours later she returns with a polished outline — written for PhD researchers, assumes a full semester, almost no hands-on practice.

She was not incapable. **You never told her the audience, the time available, the teaching style, or what students should be able to do at the end.**

Working with AI is the same — with one key difference. A human colleague learns and remembers you. AI does not. Every new chat opens with a colleague who has never met you. What you would tell a person once, you must say again every time — or put it somewhere the AI reads it automatically (like a Project's instructions or memory).

Even then: **a complete brief does not guarantee a correct answer.** AI can invent facts, sound confident, and still be wrong. Better instructions improve your odds — but checking the work is always a separate, necessary skill.

> **AI fluency = knowing what to give AI, how to guide it, how to judge its work, and when not to use it.**

---

## What Is AI Fluency?

**AI fluency** means working with AI in a way that is:

| Quality | What it means |
|---|---|
| **Effective** | You actually reach the goal |
| **Efficient** | You don't waste time, effort, or tokens (the small units of text AI reads/writes — what you pay for) |
| **Ethical** | You use AI fairly and openly |
| **Safe** | You protect people, privacy, security, and important information |

This is not about memorizing "magic prompts" or knowing how a model is built. It is about making **good human decisions** around AI.

---

## The 4Ds Framework — One Sentence Each

The AI Fluency Framework has **four human competencies** — called the **4Ds**:

| D | One-word summary | Plain-English question |
|---|---|---|
| **Delegation** | Decide | What should AI do, and what should stay with me? |
| **Description** | Explain | What does AI need to know to do the work well? |
| **Discernment** | Check | Is the result actually good and trustworthy? |
| **Diligence** | Own | Is this a responsible way to use AI, and am I ready to own the result? |

---

## The Eight Core Ideas (One Line Each)

1. Everyone has the same AI. Fluency is what you do with it — effectively, efficiently, ethically, and safely.
2. There are three ways to work with AI: automation, augmentation, and agency.
3. Delegation decides which work belongs to you and which to AI — before you type anything.
4. Description gives AI what it needs, in three kinds: product, process, and performance.
5. Discernment judges what comes back — because a confident answer can still be wrong.
6. Diligence uses AI responsibly, in three kinds: creation, transparency, and deployment.
7. The four skills run as one loop, and they scale into full engineering systems.
8. Four beginner mistakes are common — each one misses a different skill.

---

## Three Facts to Never Forget (from "What AI Actually Is")

Before the 4Ds, anchor these three truths:

1. **Sounding right ≠ being correct.** AI can produce a confident, polished, completely wrong answer. This is called a **hallucination** — a confident output built on invented information.
2. **The same prompt may give a different answer next time.** AI output is not deterministic.
3. **AI only works with the information in front of it.** If something important is missing, it guesses — and a reasonable-sounding guess can still be wrong.

> Treat AI output like work from a capable colleague — useful, but always worth reviewing. Unlike a real colleague, AI keeps the same confident tone whether it is sure or making something up.

---

## Part 1: The Big Picture

### The "See It in Three Minutes" Demo

Open any AI assistant. Paste this:

```
Write a welcome email for new members.
```

You get something competent, grammatical, and completely generic. Now try this:

```
Write a welcome email for new members of a small women's cycling club
in Karachi. Most are nervous beginners who have never ridden in traffic.
Warm and a bit funny, under 150 words, no exclamation marks. End by
telling them the Saturday 6am ride is slow on purpose and nobody gets dropped.
```

Same model. Same task. Same three seconds for the machine.

**The second email is better because you provided what the first left out:**
- Who the people are
- What they fear
- How it should sound
- How long
- What the point is

Two things happened:
1. The gap between the two results came from **you**, not from the model.
2. You could only tell the second was better because **you knew enough about the subject to judge it.**

The first is **Description**. The second is **Discernment**. That is the whole course in a demonstration.

---

### The Three Ways to Work with AI

Humans work with AI in three modes, differing by how much freedom the AI has to decide what to do next:

```
Low AI Autonomy ←————————————————→ High AI Autonomy
   Automation        Augmentation        Agency
  (Script writer)    (Co-creator)       (Director)
```

#### 1. Automation — "Do this task"

You tell AI exactly what to do. AI runs it.

**Examples:**
- "Summarize this report in five bullets."
- "Translate this email into Urdu."
- "Extract the invoice number, date, and total from this PDF."

**You are the script writer.** You define the task; AI runs it. Best for work that is clear and repeatable.

**Common failure:** A step is done badly.

#### 2. Augmentation — "Help me think"

You and AI work together as thinking partners. You go back and forth — you ask, it responds, you challenge, it revises.

**Examples:**
- Brainstorming a business idea
- Reviewing a software architecture
- Improving a lesson plan
- Comparing two strategies
- Exploring a question where you don't yet know the answer

**You are the co-creator.** AI is not following a script — it acts more like a colleague thinking alongside you.

**Common failure:** The AI becomes agreeable and stops being useful.

#### 3. Agency — "Pursue this goal for me"

You give AI a **goal and boundaries**, then let it decide many of the steps. Instead of:
> "Read these five emails and summarize them."

You say:
> "Keep my inbox manageable. Reply to routine messages, flag important ones, and ask me before doing anything you are unsure about."

Now AI must decide: which message is routine? Which is important? When to ask you?

**You are the director.** But unlike a director who watches every take, you often will not be watching.

**Two critical words — future and for others:**
- **Future** — you configured the AI on Monday; it handles Thursday's work while you sleep.
- **For others** — the person the AI serves may not be you. You set it up; your customer, student, or colleague talks to it.

**Common failure:** The goal or boundary is misunderstood.

#### Automation vs Agency — The Key Difference

| | Automation | Agency |
|---|---|---|
| You provide | The task or steps | The goal and boundaries |
| AI decides | Very little | Many next steps |
| Your role | Script writer | Director |
| Common failure | A step is done badly | The goal or boundary is misunderstood |

> No mode is automatically better. One project may use all three — automate data extraction, use augmentation to think through exceptions, then give an agent limited authority over routine cases.

---

## Part 2: The Four Competencies

### D1 — Delegation: Decide Who Should Do What

**The most common beginner mistake happens before the first prompt.** People start typing without deciding:
- What they want
- What a good result looks like
- Which parts AI should do
- Which decisions should never leave their hands

**Delegation = deciding how work is divided between you and the AI. It is workflow design, not task offloading.**

Delegation has **three parts**:

#### 1. Problem Awareness — Know What You Are Trying to Accomplish

Before asking AI anything, ask yourself:
- What is the goal?
- Who is this for?
- What does success look like?
- What could go wrong?
- Where is human judgment essential?

**Example — invoice-chasing agent:**

A beginner types: *"Build me an invoice-chasing agent."*

The AI produces something. But the real questions are still unanswered:
- Which customers should it contact?
- How many days late must an invoice be?
- What tone should it use?
- Above what amount must a human approve the message?
- What if the customer disputes the invoice?
- Which accounting system may the agent read?
- May it send messages, or only draft them?

**These are not prompting questions. They are business questions.** AI cannot decide your policy unless you deliberately give it that authority — and in many cases you should not.

#### 2. Platform Awareness — Choose the Right Kind of AI

No AI is equally good at everything. The right tool depends on the job:

| Task type | Best tool type |
|---|---|
| Hard multi-step problem | Reasoning model (thinks through steps before answering) |
| Current information needed | Search-enabled assistant (looks things up in real time) |
| Software work | Coding agent (reads and changes project files) |
| Multi-step automated work | Agent-capable system (uses tools, keeps going without a new instruction each time) |

You do not need to memorize model names — the market changes too quickly. The habit is simply: **"Is this the right tool for this job?"**

#### 3. Task Delegation — Divide the Work Deliberately

Once you understand the problem and the platform, explicitly split the job.

**Example — creating a course:**

| Task | Best owner | Why |
|---|---|---|
| Decide audience and learning goals | Human | Requires purpose and judgment |
| Suggest possible course structures | AI + human | AI gives breadth, human chooses |
| Draft sections from agreed outline | AI | Fast at first drafts |
| Verify factual claims | Human | Accountability stays with author |
| Add lived experience and local examples | Human | AI does not have your experience |
| Improve grammar and consistency | AI | Good fit for mechanical review |
| Approve the final course | Human | Your name and reputation are attached |

> The right question is not "Can AI do this?" It is: **"Which parts should AI do, which parts should I do, and why?"**

**Remember:** Domain expert first. AI delegator second. Some decisions should never leave your hands.

---

### D2 — Description: Give AI What It Needs

Think back to the colleague whose outline was wrong. She was not incapable — she was missing information.

AI has the same problem, more strongly. If you leave something important out, it guesses — and a reasonable-sounding guess can still be wrong.

**Description = giving AI the information and guidance it needs to do the work well.**

At full scale, this becomes **context engineering** — designing all the information an AI needs: instructions, documents, tools, memory, and policies.

Description has **three parts**:

> **Memory aid: What → How → How to work with me**

#### 1. Product Description — Define the Result

**What do you want back?**

Include:
- Type of output
- Audience
- Format
- Length
- Tone
- Important topics to cover
- Anything to leave out

**Vague:**
> "Summarize this report."

**Clear:**
> "Summarize this quarterly financial report for senior executives who have ten minutes to read. Focus on revenue trends, major risks, and recommended actions. Use short bullet points, keep it to one page. Highlight any figure that changed significantly from last quarter. Avoid unnecessary accounting jargon."

**Completeness matters more than clever wording.** The second request is not more intelligent — it is more complete.

#### 2. Process Description — Define the Approach

**How should AI do the work?**

Specify:
- Steps to follow
- Order of work
- Method to use
- Examples to imitate
- Checks to run before finishing

**Example:**
> "Review this code for correctness first, security second, and style last. Do not spend time on naming issues until you have checked whether the code actually works."

**Why order matters — the vendor proposal example:**

If you have three proposals and written criteria, you could paste everything and ask for a recommendation. But then you can only check the ending. Instead, split it by step:

**Step 1 — Extract:** Pull the same facts from every proposal into one table: price, contract length, exit terms, support hours. *Check: open each proposal and confirm a few cells.*

**Step 2 — Compare:** Compare vendors on your criteria, using only that table. *Check: does every difference named actually appear in the table?*

**Step 3 — Score:** Score each vendor using your weightings. *Check: do the scores follow your criteria, or did AI add one you never asked for?*

**Step 4 — Draft:** Write the recommendation. *Check: does it claim only what steps 1–3 support?*

> Put the step where a mistake spreads farthest **first**, and check it before continuing. A wrong price in step 1 carries through every later step and looks fine at the end.

**Prompt for step 1 only:**
```
Do only step 1 for now. Put the price, contract length, exit terms,
and support hours from each proposal into one table, then stop.
```

#### 3. Performance Description — Define How It Behaves

**How should this AI behave, and for whom?**

At the personal level (just you):
- Concise or detailed?
- Supportive or challenging?
- Ask questions first or make reasonable assumptions?
- Flag uncertainty or give best answer?

**Example performance description:**
> "Challenge my assumptions when they are weak. Flag uncertainty. Do not agree with me just to be polite. If my argument is stronger, explain why. If yours is stronger, hold your position and explain it."

This turns AI from a polite answer machine into a thinking partner.

At the system level (when you build AI for other people), performance description is even more critical. A tutoring agent might have a rule: *"Never give the answer before the student has tried the problem."* Same kind of instruction — written once, applied thousands of times.

> In a chat, a bad performance description annoys you for ten minutes. In a deployed agent, it is the product.

#### From Prompt Engineering to Context Engineering

**Prompt engineering** asks: "How should I phrase this message?"

**Context engineering** asks: "What information must be available for the AI to succeed?" — including documents, examples, memory, conversation history, policies, tools, database records, definitions, and instructions.

> A well-written prompt cannot rescue an agent that has the wrong data, missing rules, poor examples, or no access to the tools it needs.

---

### D3 — Discernment: Don't Confuse Confidence with Correctness

AI often sounds confident. A wrong answer does not come with a warning label — it can look polished, detailed, and certain.

**Discernment = judging the quality of what AI gives you.** Description asks whether you explained the job clearly. Discernment asks whether the AI actually did the job well.

**Automation bias** is the human tendency to trust automated output too easily, especially when it looks professional. It is one of the biggest risks of working with AI.

#### Four Signs That an Answer May Be Invented

| Sign | What it looks like | What to do |
|---|---|---|
| **Specifics that are too exact** | A precise figure, date, or citation that came from nothing you gave it | Open the source and verify before repeating it |
| **Confidence where an expert would hesitate** | A flat "yes" to something a specialist would answer with "it depends" | Ask what would change the answer |
| **Contradiction across a long output** | Page 2 says flat fee; Page 6 calculates from a per-user fee | Read the ending against the beginning |
| **A claimed action that never happened** | "I have sent the email" / "I checked the source" | Unless the tool shows proof, treat it as a sentence, not an event |

**When accuracy matters — verify.** Verify.

Discernment has the **same three parts as Description**, pointed at the same three things:

#### 1. Product Discernment — Is the Result Good?

Ask:
- Is it factually correct?
- Did it follow every important requirement?
- Is anything missing?
- Is it internally consistent?
- Would an expert find it credible?
- Would I put my name on it?

These six questions check the answer against three references: what you asked for, the source material, and your field's standards. An answer can pass two and fail the one that matters.

**Domain knowledge matters here.** An accountant spots a bad accounting assumption. A programmer notices a subtle bug. A teacher sees an explanation that will confuse beginners. AI speeds up expert work — it does not remove the need for expertise.

**Also judge the case made for the answer, not just the answer itself.** A right conclusion resting on a wrong assumption will not stay right.

**Useful things to ask AI to show you:**
> "Before recommending one option, list your assumptions, the evidence supporting them, and the criteria you are using to decide. Then give the recommendation."

**When answers should come from documents you provided:**
```
Answer only from the three proposals I attached, not from anything
you know about these vendors. If a proposal does not state its exit
terms, say so instead of guessing. For every term you report, quote
the proposal's section heading and the sentence it came from.
```

- The first line stops the model from filling gaps with training data (where Vendor A's imaginary feature came from).
- The second gives it permission to say "the proposal does not say" — which it rarely does unless you allow it.
- The third gives you something you can verify in a minute.

#### 2. Process Discernment — Is This Way of Working Paying Off?

Step back and judge the session itself — not just the last message:

- Is the AI adapting to my feedback, or drifting back?
- Is it repeating a mistake I corrected twice?
- Has it become agreeable to the point of uselessness?
- Am I spending every turn fixing the same formatting problem?
- Am I editing the draft more heavily than I would have written it myself?

Answer the last one directly. **Twenty minutes of steering that saves an hour is a win. Twenty minutes that saves fifteen is a loss you have been counting as a win because it felt productive.**

When the process is not working, three escalating moves exist:
1. Change the performance description
2. Change the tool
3. Take the task back

All three are fluency. Only the third feels like defeat — but sometimes it is the right answer.

#### 3. Performance Discernment — Is AI Serving People Well When You Are Not Watching?

This only matters once you have used Agency. The question is: does AI's independent behavior produce **good outcomes** for the people meeting it?

**Example:** An AI tutor might answer every question accurately and still be a bad tutor — because it gives solutions the moment a student hesitates, so nobody learns anything.

You cannot see this from inside a single chat window. It shows up across many cases: what users do next, what they complain about, the cases that go wrong the same way every time.

> Nobody can read a thousand conversations by hand. At system scale, performance discernment turns into infrastructure — evals, monitoring, sampling — that watches for you.

#### The Description–Discernment Loop

These two Ds form a continuous loop:

```
1. Describe what you want
2. AI produces something
3. Discern — inspect it
4. Refine — give specific feedback
5. AI tries again
→ Repeat until the result is right
```

**The first response is usually a draft, not the finish line.**

**How to give good feedback — Problem → Why it matters → Direction:**

Weak: *"Wrong. Try again."*

Better: *"The second section assumes enterprise customers. Our audience is solo founders, so the advice is too expensive. Rewrite that section for a one-person business with a limited budget."*

**Every review ends in one of three ways:**
1. Work goes out as-is
2. Work goes back with specific feedback
3. You take the task back — because the fix needs something only you know

Naming which one prevents the "one more small change" loop that eats an afternoon.

---

### D4 — Diligence: Use AI Responsibly and Own the Result

The first three Ds help you get better results. Diligence asks a different question:

**Should I use AI this way at all?**

**The lecturer example:** He used AI to draft end-of-term student feedback. The writing was excellent. But he pasted student names, grades, and disciplinary notes into a consumer AI service the university never approved. The students were not told AI helped write comments that would become part of their academic record.

*The output was good. The use of AI was still irresponsible.*

**Diligence = taking responsibility for how AI is used and for what happens to its output.**

Diligence has **three parts**, across three moments in time:

```
BEFORE          →        DURING         →        AFTER
Creation        →     Transparency      →     Deployment
Diligence       →      Diligence        →      Diligence
```

#### 1. Creation Diligence — Choose Tools and Data Responsibly

Before you share information with an AI system, ask:
- Does this contain personal data?
- Does it contain confidential company information?
- Am I allowed to put this into this tool?
- Who can access or keep the data?
- Is this service approved by my organization?
- Are there legal, contractual, or professional restrictions?

**The easy path is not always the responsible one.**

Often the fix is not to drop the task — it is to **strip the data.**

**Redaction** = removing identifying details before giving data to AI, while keeping the pattern the task needs.

The lecturer could have removed every student name and ID, kept the grade range and the one behavior worth commenting on, and drafted from that. **AI needs the pattern, not the person.**

**Redaction fails in two directions:**
- Too much removed → task cannot be done (feedback with no grade and no behavior is not feedback)
- Too little removed → a combination of details still identifies someone ("the only student who missed the week 3 lab" names that student as surely as a name does)

> **The test:** Could someone reading only what you pasted work out who it is about? If yes, strip more.

#### 2. Transparency Diligence — Be Honest About AI's Role

Not every AI-assisted task needs an announcement. But when AI materially affects other people, **disclosure may matter.**

Examples where transparency is important:
- Academic work
- Hiring decisions
- Customer communications
- Medical or financial advice
- Professional reports
- Anything presented as original human work

> **The more an AI-assisted result affects other people, the stronger the case for transparency.**

Transparency does not mean publishing every detail of your workflow. It means **not misleading people about AI's role when that role matters.**

#### 3. Deployment Diligence — Verify Before It Leaves Your Hands

Before AI-assisted work is published, sent, executed, or used in a decision — **check it.**

The more people the result reaches, the more checking it needs. A step that cannot be undone deserves a deeper check than one you can retract.

- A note to yourself → a quick glance
- A welcome email → a full read
- A report to a regulator → a second reviewer
- An irreversible action (payment sent, folder deleted) → check before the act, not after

Checking may mean:
- Verify facts
- Confirm sources actually exist
- Check calculations
- Review for bias or unfair outcomes
- Confirm permissions and rights
- Follow organization policy
- Get human approval for high-impact actions

**The Numbers Rule:**

> Any number a decision rests on — a total, a percentage — must be **computed**, never generated.

When you ask AI to summarize a financial report, it does not add up the column like a spreadsheet. It **predicts a likely-looking total** — which can be wrong while every individual line item looks correct.

Get numbers from a spreadsheet, a calculator, or code the AI ran and showed you. Then check the inputs, not just the sum. Did it use the right rows and the right rate?

**The one question that covers everything:**

> **"Would I confidently put my name on this?"**

If no → the work is not ready.

**When the case is unclear (not plainly wrong):**

Ask four questions:
1. Who is affected — including people who will never see the result?
2. What could go wrong for them, and would they be able to tell?
3. What would a fair outcome look like?
4. What should be disclosed, and to whom?

If you can answer all four, decide and write the answers down. If you cannot, escalate. **Guessing is the one option that turns an unclear case into your mistake.**

> **AI can automate work. It cannot automate accountability.** If an AI-assisted system makes a harmful decision, the organization operating it is still responsible.

---

## Part 3: The 4Ds as One Loop

### The 4D Operating Loop

The four competencies are not separate steps — they run as one continuous loop:

```
Delegate → Describe → Discern → Be Diligent → Repeat
```

In a chat, this loop is something you do manually. In an AI system you build for other people, each step becomes engineering:

| Competency | In a chat | In the Agent Factory (system scale) |
|---|---|---|
| **Delegation** | Decide what to ask AI to do | Scope the Digital FTE and human/AI boundary |
| **Description** | Give instructions and context | System prompts, skills, context engineering, Systems of Record |
| **Discernment** | Review the answer | Evals, monitoring, sampling, trusting the checker |
| **Diligence** | Protect data and own the result | Governance, permissions, audit, disclosure, human review |

### Worked Example: A Bookkeeping Digital FTE

Ayesha is a Forward Deployed Engineer helping a small accounting practice in Karachi build a bookkeeping AI worker. The first job: monthly bank reconciliation (checking the firm's records against the bank statement).

#### Step 1 — Delegation

Ayesha does NOT start by typing "build a reconciliation agent." She maps the job with the accounting partners first. They decide:

**AI may:**
- Match bank transactions to ledger entries
- Flag unmatched items
- Draft a reconciliation report

**Humans keep:**
- Every journal adjustment (manual correction) — humans approve
- Every write-off decision (recording money no longer expected to be collected)
- Anything affecting a client's tax position
- High-value unmatched items (escalate to a named person)

#### Step 2 — Description

Ayesha gives the system what it needs:
- The firm's chart of accounts (the list of categories for sorting transactions)
- Matching rules
- Examples of past reconciliations
- The report format the partners already use
- Escalation rules
- Definitions of duplicate payments and stale cheques (too old for the bank to pay)
- A rule: **never post a journal entry itself**
- A rule: **never contact a client directly**

#### Step 3 — Discernment

Ayesha doesn't assume it works because a demo looks good. She tests against past reconciliations the firm already trusts. The team checks:
- How many matches are correct?
- How many incorrect matches slip through?
- Do the right cases escalate?
- Does it escalate too much?
- Does performance change over time?

An accountant also reviews some matches that **appear to have succeeded** — not only the failures. A system can look safe simply by failing silently.

#### Step 4 — Diligence

- Client financial data stays inside approved infrastructure
- Agent actions are logged
- Where required, clients are told reconciliation is AI-assisted
- A human partner still signs the reconciliation and remains accountable

**The personal skill has become a system property.**

---

## The 4Ds and the 10-80-10 Rule

The book's **10-80-10 Rule** describes how human effort is distributed in AI-era work:

| Phase | % of effort | 4Ds strongest here |
|---|---|---|
| **First 10%** — Set direction | 10% | Delegation + Description (plan the work) |
| **Middle 80%** — Run the work with AI | 80% | Description + Discernment (iterate, check, steer) |
| **Final 10%** — Judge the truth | 10% | Discernment (critical review before anything ships) |
| **All 100%** — Act responsibly | 100% | Diligence (never a final checkbox — surrounds the whole workflow) |

---

## Part 4: Four Common Beginner Mistakes

Each mistake is one missing D:

| Mistake | Missing skill | Fix |
|---|---|---|
| **Prompting before defining the problem** — you start typing before deciding what success looks like | Delegation | Define the goal, audience, constraints, and human/AI split first |
| **Treating the first answer as the final answer** — one weak response and you decide AI is useless | Description + Discernment loop | Inspect the result, give specific feedback, try again |
| **Trusting a polished answer because it sounds professional** — you mistake fluency for accuracy | Discernment | Verify important facts, assumptions, calculations, and sources |
| **Thinking about privacy or accountability only after something goes wrong** | Diligence | Decide data, disclosure, approval, and accountability rules before you deploy |

---

## The Beginner Checklist

Run this before any important AI task:

| Stage | Ask yourself |
|---|---|
| **Delegate** | What is the goal? What should AI do? What stays with me? |
| **Describe** | What output, context, method, and behavior does AI need? |
| **Discern** | How will I know the answer is correct, complete, and useful? |
| **Be Diligent** | Is the data safe? Does AI's role need disclosure? Who approves and owns the result? |

---

## Six Practice Prompts (Try These Now)

### Prompt 1 — Build a 4D Plan for a Real Task
```
I need to do this: [describe your task].

Before we start, walk me through the four Ds of AI fluency:
delegation, description, discernment, diligence. Ask me one question
at a time, skip any that obviously don't apply, and give me the plan
as a short table at the end.
```
*Notice: most of the plan comes from your answers, not AI's. Delegation and Diligence are decisions only you can make.*

---

### Prompt 2 — Use Discernment on Something You Know
```
Let's discuss [topic I know well].

Talk to me like a knowledgeable colleague, not a lecturer.
As we go, I will watch for three things:
- where you improve my thinking,
- where I need to correct you,
- where my own experience makes me reject your suggestion.

Start by asking which part of the topic I want to discuss.
```
*Notice: how cheap discernment is when you know the subject. That ease is your expertise — and what you will not have in a topic you don't know.*

---

### Prompt 3 — Feel What It Is Like to Be a Non-Expert
```
Teach me the basics of [topic I know little about].
Explain it for a complete beginner and use concrete examples.

At the end, identify the claims in your explanation that I should
verify with a reliable source, and explain why they deserve checking.
```
*Notice: how differently the same quality of output lands. Nothing felt wrong — because you had nothing to check it against. Every user of an AI you build will feel this.*

---

### Prompt 4 — Write a Performance Description
Use this at the start of any serious session:
```
During this conversation:
- challenge weak assumptions,
- flag uncertainty on factual claims,
- do not agree with me just to be polite,
- ask a clarifying question when an ambiguity would materially change the answer,
- change your recommendation when new evidence supports it,
- explain why when you disagree with me.
```
*Notice: how few turns before the difference is obvious — and how quickly it fades if you forget to set it in the next chat. That is why a deployed agent keeps this in a system prompt, not in someone's memory.*

---

### Prompt 5 — Inspect the Justification Before Accepting a Recommendation
```
Before making a recommendation, list:
1. the important assumptions,
2. the evidence supporting them,
3. the criteria you are using to compare the options,
4. the major uncertainties.

Then make the recommendation.
I want a justification I can review, not just a conclusion.
```
*Notice: whether any assumption is one you would have accepted without seeing. That is the one worth checking — and it is invisible when you get only the conclusion.*

---

### Prompt 6 — Run a Small Project Through the Full 4D Loop
```
I want to complete this project using the 4D AI Fluency framework:
[describe the project].

First, help me decide the human/AI division of work.
Then, before each AI-owned task, ask what product, process,
and performance I want.

After each important output, stop so I can evaluate it.
At the end, run a diligence check covering facts, sensitive data,
disclosure, approvals, and anything I should verify before using the work.
```
*When done, ask: "Which D required the most effort from me?" That is the competency to practice most.*

---

## Quick Self-Check — 10 Questions from Memory

1. What four qualities define AI fluency?
2. What is the difference between automation, augmentation, and agency?
3. What are the three parts of Delegation?
4. What are the three parts of Description?
5. Why can a confident AI answer still require verification?
6. What are the three parts of Discernment?
7. What are the three parts of Diligence?
8. What question can you ask before shipping AI-assisted work?
9. In one sentence, what is the 4D loop?
10. How does Discernment become an engineering practice at scale?

**Answers:**

1. Effective, efficient, ethical, and safe.
2. Automation runs a defined task; augmentation works with you as a thinking partner; agency acts toward a goal with more freedom to choose the steps.
3. Problem awareness, platform awareness, and task delegation.
4. Product description, process description, and performance description.
5. Because sounding right is not the same as being correct. Fluent wording does not verify facts, assumptions, or reasoning.
6. Product discernment, process discernment, and performance discernment.
7. Creation diligence, transparency diligence, and deployment diligence.
8. "Would I confidently put my name on this?"
9. Decide what AI should do, describe the work, evaluate what comes back, and take responsibility for the whole process.
10. It becomes evals (repeatable tests), monitoring, sampling, and review gates that test whether an AI system performs well enough.

---

## Complete Glossary of Terms

| Term | Definition |
|---|---|
| **AI fluency** | Working with AI effectively, efficiently, ethically, and safely |
| **The 4Ds** | Delegation, Description, Discernment, and Diligence |
| **Automation** | AI performs a specific task you specify |
| **Augmentation** | Human and AI work together as thinking partners |
| **Agency** | AI works toward a goal you set and chooses many steps — often for other people, when you are not present |
| **Delegation** | Deciding what AI does and what humans keep |
| **Problem awareness** | Knowing the goal, the work, the risks, and what success means |
| **Platform awareness** | Knowing which AI system or tool fits the task |
| **Task delegation** | Assigning each part of the work to a human or to AI |
| **Description** | Giving AI the information and guidance the work needs |
| **Product description** | Defining the output you want (what) |
| **Process description** | Defining how the AI should approach the work (how) |
| **Performance description** | Defining how an AI behaves — with you (chat) or with its users (deployed agent) |
| **Discernment** | Judging whether AI's output, justification, and behavior are good enough |
| **Product discernment** | Judging the result itself |
| **Process discernment** | Judging whether your way of working with AI is paying off |
| **Performance discernment** | Judging whether an AI's independent behavior serves its users well |
| **Diligence** | Taking responsibility for how AI is used and for its output |
| **Creation diligence** | Choosing tools and data responsibly before and during the work |
| **Transparency diligence** | Being honest about AI's role when it affects people |
| **Deployment diligence** | Checking AI-assisted work before it is used or sent |
| **Context engineering** | Designing all the information an AI needs: instructions, documents, tools, memory, and policies |
| **Automation bias** | The human tendency to trust automated output too easily |
| **Hallucination** | A confident AI output that sounds right but is invented or incorrect |
| **Redaction** | Removing identifying details before giving data to AI, while keeping the pattern the task needs |
| **Digital FTE** | An AI worker set up to do a defined job for other people. FTE = full-time equivalent |
| **Tokens** | The small pieces of text an AI reads and writes — what you pay for |
| **System of Record** | The trusted store of a business's official data and rules |
| **System prompt** | A standing instruction an AI reads at the start of every conversation |
| **Eval suites** | Repeatable tests that score what an AI system produces |

---

## Where This Leads in the Agent Factory Program

| Competency | What it becomes at system scale |
|---|---|
| **Delegation** | Spec-Driven Development — Delegation + Description become an engineering method |
| **Description** | System prompts, SKILL.md files, System of Record, context engineering |
| **Discernment** | Eval-Driven Development, Trusting the Checker — manual review becomes infrastructure |
| **Diligence** | System of Record and Governance — data rules, access control, audit logs, human review gates |

> Practice in a chat window is rehearsal for building and governing AI systems.

---

## One Sentence to Remember

**Decide what AI should do. Describe the work clearly. Check what comes back. Own what happens next.**

---

*Source: [agentfactory.panaversity.org/docs/ai-fluency-crash-course](https://agentfactory.panaversity.org/docs/ai-fluency-crash-course)*  
*Framework by Rick Dakan & Joseph Feller, produced with Anthropic. Licensed CC BY-NC-SA 4.0.*  
*Part of the Panaversity Agent Factory Program — Foundations (Everyone) track.*