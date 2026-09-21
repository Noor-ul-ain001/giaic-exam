# Skills & Connectors: Teach AI Once, Connect It to Your Apps
## Complete Explanation
> Source: [agentfactory.panaversity.org/docs/skills-connectors-crash-course](https://agentfactory.panaversity.org/docs/skills-connectors-crash-course)  
> Simplified & explained — all 14 concepts, every section, nothing skipped.

---

## The Problem This Solves

Most people use AI like a vending machine. They type a request, take what comes out, and walk away. Tomorrow they type the whole request again — same instructions, same context, same "no, our invoices look like *this*." The machine remembers none of it.

There is a better way — and in 2026 it requires no programming.

- You can **teach AI a task once** and have it do that task your way, every time. That is a **Skill**.
- You can **give AI safe access to the apps** where your work actually lives — your files, your email, your tracker. That is a **Connector**.

---

## The One Idea Under Everything

> **A chat message tells AI what to do *this once*.  
> A Skill teaches AI how to do something *every time*.  
> A Connector gives AI *hands* to reach your real apps and data.**

### The Kitchen Analogy

| Kitchen element | What it maps to |
|---|---|
| An order shouted across the counter ("make me a sandwich") | A one-time chat message — made once, forgotten |
| The kitchen itself — stove, knives, fridge, real ingredients | **Connectors** — the live apps where your real data lives |
| Recipe cards on the wall | **Skills** — step-by-step instructions for doing one task *your* way |

Give a cook a kitchen but no recipes → every dish is improvised.  
Give them recipes but no kitchen → they can read but cannot cook.  
Give them both → they produce your dish reliably, every time.

**Two places the analogy stops being exact:**
1. Your ingredients never move into AI's kitchen. AI reaches into your live app when you ask, and only as far as your own account already allows.
2. A real cook tastes and fixes. AI follows the card — so the tasting (review) always stays your job.

---

## The 14 Ideas in One Line Each

| # | Idea |
|---|---|
| 1 | From chat box to operating layer — the two kinds of work you keep redoing by hand |
| 2 | A Skill is a folder with a text file in it. No code from you. |
| 3 | A Connector is safe access to one app, with the permissions you already have |
| 4 | Skills, Connectors, Projects, and Custom Instructions — four features, one clean split |
| 5 | In Claude.ai, skills start on their own — you rarely need a slash command |
| 6 | Word, PowerPoint, Excel, and PDF skills come built in — one switch to turn them on |
| 7 | Connecting your apps takes about a minute; enable per chat |
| 8 | The real magic: Connector fetches data, Skill shapes the output, you review |
| 9 | Diagnose by the friction you feel — re-explaining vs. copy-pasting |
| 10 | Fastest path: describe the skill in plain English, AI writes it for you |
| 11 | A SKILL.md has two parts — one always loaded, one loaded only when matched |
| 12 | The description field decides whether your skill ever fires |
| 13 | Test what starts it, test the output, test the hard cases, then fix |
| 14 | One click saves it; Team plans can share it across an organization |

---

## Part 1: The Two Upgrades

### Concept 1 — From Chat Box to Operating Layer

**The two kinds of friction:**

**Friction 1 — Re-explaining how, every time:**
- An accountant pastes the same formatting rules into a new chat every month
- A doctor re-explains SOAP note format daily for consultation notes
- A marketer pastes brand-voice rules into every caption request
- An engineer pastes the same review checklist for every design

All four have the same shape: a **repeatable task done your specific way**, where only the input changes. A **Skill** is built for exactly this.

**Friction 2 — Fetching data from other apps, every time:**
- The accountant's numbers are in an Excel file and a month-old email
- The doctor's patient history is in a Google Drive folder
- The marketer's calendar is in a planning tool
- The engineer's open issues are in Jira or Linear

AI can reason about all of this — but only if the information reaches it. Copy-pasting is the cost of AI having no hands. A **Connector** gives it those hands.

**Put the two together** and the chat box becomes a colleague who knows your standards and can reach your files. This shift is called the **operating layer** — AI that acts on your real work, not just a box you type into.

---

### Concept 2 — What a Skill Actually Is

A Skill is almost embarrassingly simple:

> **A Skill = a folder with a text file in it.**

The required text file is called **`SKILL.md`** — named exactly that way, capital letters and all. It holds:
- A **name**
- A short **description** of when to use the skill
- The **instructions** you want AI to follow in plain English

That is all that is required. The accountant's first skill could be five sentences of formatting rules.

The folder can optionally also hold:
- Example files
- A template document
- Reference notes
- Small programs (which AI writes — you never write a line of code)

**Why you can install dozens of skills without slowing AI down:**

AI does not hold every skill in view at all times. It keeps only the short **description** of each skill loaded, and opens the full instructions only when your request matches. This is called **progressive disclosure**. The skill "sleeps" until needed, then wakes up exactly when relevant.

> The recipe card fits perfectly: a Skill is a card pinned to the kitchen wall. Every time that dish is ordered, the cook follows the card.

---

### Concept 3 — What a Connector Actually Is

A Connector is how AI safely reaches your apps. Connect Claude to:
- **Google Drive** → it can search your files
- **Gmail** → it can read mail and draft replies
- **Slack** → it can pull messages and act in channels
- **Linear, Asana, Notion** → it can read tickets, pages, and tasks

**MCP** (Model Context Protocol) is the open standard that all connectors run on. You never build or read the connector code. You click *Connect*. That is the deal: code you never write.

**Three facts that matter for using connectors safely:**

**1. AI inherits only the permissions you already have.**  
If your account cannot open a file, folder, or record — the connector cannot either. Connecting Google Drive does not hand AI your whole company's Drive.

**2. You choose how much AI may do.**
- **Read-only** = AI may look but not change ("search and summarize my email")
- **Write access** = AI may edit, create, send, or delete ("send this email")
- Always start read-only. Grant write access only once you trust how the tool behaves.

**3. You turn connectors on per conversation.**  
Connecting an app once makes it *available*. You still decide which connectors each chat may use, and you choose the **scope** (how much of the app AI may reach). One folder < whole drive. Smaller is safer.

**Types of connectors:**
- **Ready-made connectors** in the directory: Google Drive, Gmail, Slack, Notion, Figma, Linear, Atlassian, and more
- **Custom connectors**: ones you set up for any app that speaks MCP
- **Interactive connectors**: draw a live panel inside the chat, not just returning text

---

### Concept 4 — Skills vs Connectors vs Projects vs Custom Instructions

Four features that beginners often mix up:

| Feature | What it is | Best for | One-line test |
|---|---|---|---|
| **Skill** | Reusable *how-to* instructions AI loads only when relevant | A repeatable task done your specific way: formatting, voice, checklists | "I keep re-explaining *how* to do this." |
| **Connector** | Safe access to an outside app or data source | Reading files, email, messages, tickets — or acting in them | "I keep copy-pasting from another app." |
| **Project** | A workspace whose files and instructions load in every chat inside it | Standing context for a client, course, or ongoing body of work | "These same files and rules apply to *everything* here." |
| **Custom Instructions** | Preferences applied to *all* your chats | Global style: "be concise", "use metric units" | "I want this to be true everywhere, always." |

**Three lines people confuse:**

**Skill vs Project:**
- A Project loads its context the moment you open a chat inside it — always on within that workspace
- A Skill sleeps until a request matches it, then fires anywhere
- Standing knowledge → Project. A procedure you run on demand → Skill.

**Skill vs Connector:**
- A Connector is **access** (what AI can reach)
- A Skill is **expertise** (how AI should behave)
- They are partners, not alternatives.

**Skill vs Custom Instructions:**
- Custom instructions touch everything you ever do
- A Skill touches only one kind of task
- "Always reply in the language I write in" → Custom Instructions
- "When I ask for a board paper, use this eight-section structure" → Skill

---

### Concept 5 — Slash Command or Automatic?

**In Claude.ai (the web and mobile app), skills fire on their own.**

You describe your task in plain English. AI reads your request, checks it against the short description of every skill you have enabled, and loads the matching one. The word for this is **fire** — the skill activates without you naming it.

Ask for "a PowerPoint about Q3 results" → the PowerPoint skill fires automatically.

**Slash commands are for other tools and overrides:**
- In **Cowork** and **Microsoft 365 add-ins** (Claude inside Excel, Word, PowerPoint, Outlook): type `/` to browse and pick a skill
- In **Claude Code / OpenCode**: skills load automatically, or you can call one directly
- In **all tools including Claude.ai**: if automatic matching misses, name the skill: "use my brand-voice skill to draft this caption"

| You want to… | In Claude.ai | In Cowork / Office add-ins | In Claude Code / OpenCode |
|---|---|---|---|
| Let AI decide | Describe the task. Automatic. | Describe the task. Automatic. | Describe the task. Automatic. |
| Force a specific skill | Name it: "use my X skill" | Type `/` and pick it, or name it | Name it, or call it directly |

**Connectors work the same way.** Once an app is connected and enabled for the conversation, AI brings it in when your request calls for it. "Summarize the contract in my Drive" pulls from Drive with no extra clicking.

> You will spend about 90% of your time letting AI decide automatically.

---

## Part 2: Using What Already Exists (No Building Required)

### Concept 6 — The Skills That Come Built In

Anthropic maintains built-in skills that produce finished files. They all depend on one switch:

**Settings → Capabilities → "Code execution and file creation" → ON**

This one switch enables:
- **Word** → formatted `.docx` documents
- **PowerPoint** → full slide decks from a description
- **Excel** → real spreadsheets with working formulas (not a table pasted into chat)
- **PDF** → creating and filling PDFs

You just ask. Say *"prepare a slide deck introducing agentfactory.panaversity.org to a general audience"* and a finished deck comes back. No skill named. The skill fires automatically.

**Important:** These built-in document skills do NOT appear in your skills list. They live in the engine. Your skills list starts with only one item: **skill-creator** — an Anthropic skill whose entire job is to help you build your own skills.

**To install more skills:**  
Open **Customize → Skills → "+" → Browse skills** to open the directory of one-click installable skills, including partner skills from Notion, Figma, and Atlassian.

**Note on the wider ecosystem:** Skills became an open standard in late 2025, so community marketplaces with tens of thousands of skills appeared quickly. That is a gift and a hazard — see Part 5 on safety.

---

### Concept 7 — Connecting Your Apps

**Connecting an app takes about one minute.**

How to do it:
1. From a chat, click the `+` in the lower left (or type `/`)
2. Hover over Connectors → "Manage connectors" → click `+`
3. OR: Open **Customize → Connectors → "+"**
4. Pick a service, click Connect, sign in — the usual "allow this app to access your account" flow

**Four practical notes:**

1. **After connecting, enable the connector for a specific conversation.** Connecting once makes it available. You still switch it on per chat.

2. **Free plans include one custom connector.** Ready-made directory connectors (Drive, Gmail, Slack, etc.) are broadly available.

3. **Each connector brings a list of "actions" (the settings call them tools).** With ten or more connectors switched on, choose **load-on-demand** — loads an action only when a request needs it.

4. **Watch for the "Interactive" badge.** Those connectors draw live panels inside the chat, not just text responses.

**Worked example (on made-up data — always practice this way first):**

Step 1: Create a demo file  
*"Make a one-page Word doc of a fake patient intake form (call it DEMO-Okafor-2026-03, with three invented medications and one allergy) and save it to my Google Drive."*

Step 2: Read it back  
*"Find DEMO-Okafor-2026-03 in my Drive and summarize the medications into a SOAP-style note."*

Claude searches your Drive, pulls the file, and drafts the note. One connector, both directions (write and read), on data you invented.

> **Key rule:** When the data is real (healthcare, legal, student records), use only the accounts your organization has approved. Always practice on invented data first.

---

### Concept 8 — The Real Magic: Skills + Connectors Together

Each is useful alone. Together they eliminate the entire copy-paste-format cycle.

> **The Connector fetches. The Skill shapes. You review.**

**Example 1 — The Accountant's Monthly Close:**

With a "client-summary" skill built and Google Drive connected, the monthly ritual collapses to two messages:

Create the demo ledger:
```
Create a sample ledger spreadsheet for a made-up client called DEMO Trading:
a dozen March transactions across a few expense heads, two or three of them
deliberately above a typical withholding threshold. Save it to my Google
Drive as DEMO-ledger-March.
```

Then the monthly request is one sentence:
```
Prepare the March client summary for DEMO Trading from DEMO-ledger-March
in my Drive.
```

The Drive connector fetches the ledger. The skill formats every amount in the reporting currency, groups by expense head, flags withholding items, and lays it out in the firm's four-section template. A two-hour ritual → a two-minute review.

**Example 2 — The Marketer's Weekly Content Batch:**

A "brand-voice" skill holds the rules: no exclamation marks, question-hook openings, banned buzzwords, CTA format. A connector reaches the content calendar in Notion.

Request: *"Draft captions for this week's three scheduled posts in Notion, in our voice."*

The connector reads the calendar, the skill writes the captions on-brand, and the marketer edits instead of composes from scratch.

**The same template fits:**
- **Engineer**: "design-review" skill + Linear connector → review open `arch`-tagged issues, write findings by severity
- **Teacher**: "lesson-plan" skill + Drive connector → build next week's plan from the syllabus file

---

### Concept 9 — Which Problem Needs Which?

**Diagnose by the friction you feel:**

| The friction you feel | What it needs | Example |
|---|---|---|
| "I paste the same formatting, voice, or method rules every time." | **Skill** | Brand voice, SOAP notes, report template |
| "The output should always look a certain way." | **Skill** | Board-paper structure, invoice layout |
| "I keep copying data out of Drive / Gmail / Slack / a tracker." | **Connector** | Pulling a ledger, email thread, last week's tickets |
| "I want AI to *do* something in another app." | **Connector** (write access) | Create a Linear issue, draft an email, update a Notion page |
| "I fetch real data *and* it must come out my specific way." | **Both** | Monthly client close, weekly content batch, design review |
| "I just want a one-off answer right now." | **Neither** | A single question, a quick draft you will never repeat |

**Two honest cautions:**

1. **Not everything deserves a skill.** A task you do once is just a good prompt. A skill earns its place only when the task repeats — this is called the **market-of-one test**: a skill is worth making when it captures *your* specific repeated way, the thing no app does for you out of the box.

2. **A connector you don't need is a door left open.** Connect the apps a workflow requires, not every app you own. Scope is safety.

---

## Part 3: Building Your Own Skill (AI Builds It for You)

### Concept 10 — The Fastest Path: Let AI Write It

You do not write a skill. You describe it.

Anthropic provides a built-in skill called **skill-creator** whose entire job is to build skills for you. Just ask:

```
Use the skill-creator skill to help me build a skill.

The skill prepares a monthly client financial summary for my
accounting firm. Whenever I ask for a "client summary"
or "monthly close," it should:
- Format all amounts in our reporting currency with thousands separators.
- Group line items by expense head.
- Flag any payment above the tax-withholding reporting threshold.
- Output using my standard four-section report layout
  (Overview, Income, Expenses by Head, Flags & Notes).

Ask me anything you need, then build it.
```

skill-creator asks a few clarifying questions (threshold amount? what does the template look like?), then generates a complete, correctly formatted SKILL.md.

**This is "code you never write."**  
You described an outcome. AI produced the file — plus any code the skill needs — without you writing or reading a single line. You are the client, not the contractor. A good client does not lay bricks. They write a clear brief and check the result against things they can measure.

---

### Concept 11 — Anatomy of a SKILL.md

Every skill has the same structure. Here is a minimal example:

```markdown
---
name: client-monthly-summary
description: Prepares a monthly client financial summary for an
  accounting firm. Use when the user asks for a "client summary",
  "monthly close", or "month-end report". Formats amounts in the
  firm's reporting currency, groups by expense head, and flags
  tax-withholding items.
---

# Client Monthly Summary

## Settings (edit these to make it yours)

- Reporting currency: your currency (e.g., USD, EUR, PKR)
- Withholding threshold: the amount above which to flag a payment

## Instructions

When asked to prepare a client summary or monthly close:

1. Format every amount in the reporting currency, with thousands
   separators (e.g., "1,250,000").
2. Group all line items by expense head. Sort heads by total,
   largest first.
3. Flag any single payment above the withholding threshold
   with a "⚑ WITHHOLDING" note.
4. Produce the report in exactly four sections, in this order:
   Overview, Income, Expenses by Head, Flags & Notes.

## Example

User: "Prepare the March summary for DEMO Trading."
Result: A four-section report, currency-formatted, withholding lines flagged.
```

**The two-part structure:**

**Part 1 — Frontmatter** (the block between the `---` lines at the top):
- Contains the `name` and the `description`
- This is the **only part AI keeps loaded at all times**
- AI reads this to decide whether your request matches the skill
- This is **progressive disclosure Level 1**

**Part 2 — Body** (everything after the frontmatter):
- Contains the actual instructions, examples, settings
- Loaded **only when the description matches your request**
- This is **progressive disclosure Level 2**

**Optional folders for complex skills:**
- `references/` — detailed docs AI reads when needed (Level 3, load on demand)
- `assets/` — a template file to fill in
- `scripts/` — programs for steps that must be exact every time

**File rules (common upload errors):**
- File must be named exactly `SKILL.md` — capital S, capital M, capital D
- Folder name uses kebab-case: `client-monthly-summary` ✅, not `Client Monthly Summary` ❌
- No XML-style tags (angle brackets) in the name or description
- Do not put "claude" or "anthropic" in a skill name — those are reserved

---

### Concept 12 — The Description Field Is the Whole Game

**The description decides whether your skill ever fires.** AI does not read your instructions to judge relevance — it only reads the description. A vague description = a skill that never starts. A sharp description = a skill that starts exactly when it should.

**Formula: what it does + when to use it + the exact phrases you would say**

| Bad description | Why it fails | Better description |
|---|---|---|
| "Helps with reports." | Too vague — fires for everything or nothing | "Prepares a monthly client financial summary. Use when the user asks for a 'client summary', 'monthly close', or 'month-end report'." |
| "Handles patient documentation." | No trigger words a real user would say | "Converts consultation notes into SOAP-format clinical notes. Use when the user asks for a 'SOAP note', 'clinical note', or to 'write up' a consultation." |
| "Brand stuff for marketing." | No idea what or when | "Writes social captions in our brand voice (no exclamation marks, question-hook openings). Use when drafting Instagram, LinkedIn, or X captions." |

**Debugging trick:** Once a skill is installed, ask AI:
> *"When would you use my client-summary skill?"*

It says the description back in its own words. If the answer is narrower or wider than you intended, you found what to fix.

**Negative triggers:** A line that says when *not* to use the skill — helpful when a skill fires too eagerly.

Example: *"Do NOT use for one-off calculations or quick questions. Use only for full month-end reports."*

---

### Concept 13 — Test, Then Iterate

A skill is never done on the first draft. Test in this order:

**Step 1 — Describe and generate.** Let skill-creator write the first version.

**Step 2 — Read the draft before testing.** Ask one question of every instruction line: "Would two different colleagues who read this do the same thing?" 

- "Flag the big payments" → ❌ FAILS (what is "big"?)
- "Flag any single payment above the withholding threshold with a ⚑ WITHHOLDING note" → ✅ PASSES

A failing instruction shows no error message — the output just comes out differently each run.

**Step 3 — Test what starts the skill.**
- Try phrases that *should* start it (e.g., "prepare the client summary") → confirm it loads
- Try unrelated requests → confirm it does *not* fire

**Step 4 — Test the output.** Run the skill on a real or realistic input. Right currency? Grouped by head? Withholding flagged? All four sections present?

**Step 5 — Test the awkward cases.**
- A client with no income that month
- A payment exactly on the threshold
- A messy or incomplete ledger

**Step 6 — Bring failures back to skill-creator:**
*"This skill double-counted reversed entries. Update it to net out reversals before grouping."*

**Timing list — when did it go wrong? That points at the cause:**

| When it broke | What is wrong | Fix |
|---|---|---|
| Never starts | Description is too vague or missing your trigger words | Add the exact phrases you say |
| Starts on wrong things | Description too broad | Narrow it, or add a negative trigger |
| Starts but output is off | An instruction is loose | Write the rule you assumed it knew |
| Right at first, worse as chat grows | Chat got long — skill is fine | Start a fresh chat; don't edit the file |
| Same mistake every run even after rewording | Step needs to be exact (a sum, a threshold check) | Ask skill-creator to move it into a script |
| Used to work, now doesn't | Something around it changed (threshold, template, workflow) | Re-read the skill against how you work today — nothing warns you when a skill goes out of date |

---

### Concept 14 — Saving and Sharing Your Skill

**Saving:** When skill-creator finishes, it shows a "Save skill" button. One click puts it in your personal skills list — switched on and private to your account. No zip file, no upload.

**To share (Team or Enterprise plans):**
- Share with named colleagues
- Publish to your organization's directory
- Shared skills are **view-only** — recipients cannot edit the original
- When you improve the original, **all shared copies update automatically** → this is how a whole firm standardizes its document formats

**To install a skill from elsewhere:**  
Open **Customize → Skills → "+" → "Create skill" → upload the folder**

---

## Part 4: The Same Skill, Five Places

**In December 2025, Anthropic published the Agent Skills open standard** at agentskills.io. This is the format that lets many different tools read the same `SKILL.md` file. A skill you write once is portable across tools.

**The five tools:**

| Where you work | Who it's for | How to install a skill | How to connect an app | How to build your own |
|---|---|---|---|---|
| **Claude.ai** (web/mobile) | Everyone — your main tool | Click Install in directory, or upload a zip | `+` → Connectors → pick → sign in | skill-creator writes it, click Save |
| **Cowork / OpenWork** (desktop) | Knowledge workers, non-coders | Same directory; skills appear automatically | Same flow + files already on your computer | Describe it; agent saves to a folder |
| **Claude Code / OpenCode** (terminal) | People who work with code | Drop the skill folder into the `skills` directory | Set up once in a config file | Ask the agent to "create a skill for…" |

- **Cowork** is Anthropic's product; **OpenWork** is the open-source alternative
- **Claude Code** is Anthropic's product; **OpenCode** is the open-source alternative
- Both in each pair read the same `SKILL.md`

**Honest guidance for non-programmers:** Start and stay in Claude.ai. Move to Cowork/OpenWork when you want AI working directly on files on your computer. Use Claude Code/OpenCode only if you work with code.

### What About ChatGPT and Gemini?

**Two things are true at once, and the marketing blurs them:**

**On Skills — genuinely cross-vendor (via CLI tools):**
- OpenAI's **Codex CLI** and Google's **Gemini CLI** (command-line developer tools) read the same `SKILL.md` files
- VS Code and Cursor also support the standard
- A skill is the one piece of this course that is not locked to Claude

**On "teach it once" in consumer chat apps — each vendor is locked in:**

| Vendor | Their version | Portable? |
|---|---|---|
| Claude | Skills (SKILL.md open standard) | ✅ Yes — runs across many tools |
| ChatGPT | Custom GPTs (with knowledge files, distributed via GPT Store) | ❌ No — lives only inside ChatGPT |
| Gemini | Gems (saved assistants with instructions and knowledge files) | ❌ No — lives only inside Google's apps |

> **If your strategy spans more than one AI tool — Skills are the future-proof choice.**

**On Connectors — the principle is the same everywhere:**  
All three vendors support app connections running on MCP or equivalent. You grant access, AI inherits your permissions, start read-only. The principle is identical.

---

## Part 5: Use This Safely (The Part Most Tutorials Rush)

Nothing inside the model checks whether an action is safe or correct. **You are that check.**

> Treat a skill from a stranger like a contract you are about to sign. Treat a connector like a key you are about to hand over.

### The Two Real Risks

**Risk 1 — Malicious skills:**

A skill is a text file (and possibly programs). A bad actor can write one whose hidden instructions tell AI to leak data or contact a suspicious server.

Two named dangers:
- **Prompt injection**: hidden instructions that push AI into actions you did not intend
- **Data exfiltration**: the skill sending your information out in secret

> "I downloaded a free skill from social media" is a sentence that should make you pause.

**Risk 2 — Over-broad connector access:**

A connector can only reach what you can reach — but if you grant write access carelessly, AI can change things on your behalf. The risk is usually not dramatic: a wrong edit, a record in the wrong place, a deleted file with no easy undo.

**Also important:** A connector's reach has two halves — the permissions you set, AND the list of actions it was built to perform. The second half is not yours to configure. For example: the Drive connector can save a new file into your Drive but cannot edit an existing document in place. Before building a weekly habit on a connector, ask it:

> *"What can you actually do in my Drive through this connector, and what can't you do?"*

Shape the work around the answer. A limit like that is the shape of the tool, not a bug.

### The Safe-Use Checklist

| Rule | Why it matters |
|---|---|
| **Install skills from trusted sources** | Built-in Anthropic skills and the official directory are the safe default. A zip from a forum is not. |
| **Read a skill before enabling it** | Open the SKILL.md and bundled files, or ask AI: *"Read this skill and tell me exactly what it instructs you to do. Flag anything that contacts external servers or could leak my data."* Pay attention to programs and any instruction that reaches the internet. |
| **Start a new connector read-only** | Grant "search and summarize" before "send" or "delete." Move to write access only after you've watched the tool behave well. |
| **Scope to the smallest folder or app the task needs** | Don't grant whole-drive access for a one-folder job. |
| **Scope is a connector idea, not a Skill idea** | A connector has scopes you can narrow. A Skill runs with whatever access its chat already has — so reading the skill first is the control for Skills; starting read-only is the control for connectors. |
| **Check recovery before allowing edits** | Confirm how a connector handles version history and undo before letting AI edit, move, or delete files. Some write actions skip the recovery path you expect. Keep backups of anything you cannot afford to lose. |
| **On a team, route shared skills through your org's directory** | Where an owner has reviewed them — not by passing zip files around. |

> **The two controls summarized:**  
> Read a skill before enabling it — that is the protection against bad skills.  
> Start a connector read-only and keep its scope small — that is the protection against careless connectors.

---

## Quick Glossary

| Term | Simple definition |
|---|---|
| **Skill** | A saved set of instructions that teaches AI how to do one task your way |
| **Connector** | A safe link that lets AI reach one of your apps (files, email, etc.) |
| **SKILL.md** | The required text file inside every skill folder |
| **Frontmatter** | The block at the top of a SKILL.md (between `---` lines), holding name and description — always loaded |
| **Description** | The short line in a skill that tells AI when to use it — the most important thing you write |
| **Negative trigger** | A line in the description saying when NOT to use the skill |
| **Fire** | When AI starts a skill on its own because your request matched |
| **Progressive disclosure** | AI keeps only the description in view; opens full instructions only on a match |
| **Scope** | How much of an app you open to AI — one folder, or everything. Smaller is safer. |
| **Read-only** | AI may look but not change |
| **Write access** | AI may edit, create, send, or delete |
| **MCP** | Model Context Protocol — the open standard all connectors run on |
| **Custom connector** | One you add yourself, for any app that speaks MCP |
| **Interactive connector** | One that draws a live panel inside the chat |
| **Project** | A workspace whose files and instructions load in every chat inside it |
| **Custom instructions** | Preferences that apply to all your chats, everywhere |
| **skill-creator** | An Anthropic built-in skill whose job is to build skills for you |
| **Agent Skills open standard** | The format published in Dec 2025 that lets many tools read the same SKILL.md |
| **Operating layer** | AI that acts on your real work, not just a box you type into |
| **CLI** | Command-line interface — a tool you use by typing commands instead of clicking |
| **Tool access** | A setting controlling when a connector's actions load into a chat |
| **Prompt injection** | Hidden instructions in a skill that push AI into actions you did not intend |
| **Data exfiltration** | A skill secretly sending your information somewhere outside your account |
| **Market-of-one test** | A task earns a skill when it captures *your own* repeated specific way — the thing no app does for you |
| **Expense head** | A spending category (travel, rent, salaries) |
| **SOAP** | Standard four-part clinical note format: what the patient says, what the doctor sees, assessment, plan |

---

## The Complete Recap

| Idea | What to remember |
|---|---|
| **The core model** | A chat = this once. A Skill = how, every time. A Connector = hands to your apps. |
| **What a Skill is** | A folder with a SKILL.md. Name + description + plain-English instructions. No code from you. |
| **What a Connector is** | Safe, scoped access to an app running on MCP. AI inherits your permissions. |
| **How skills fire** | Automatically in Claude.ai when your prompt matches the description. Slash command / naming = override. |
| **The description is everything** | AI reads only the description to decide relevance — vague = never fires. |
| **Built-in skills** | Word, PowerPoint, Excel, PDF — one switch in Capabilities turns them all on. |
| **Diagnosis** | Re-explaining how = Skill. Copy-pasting from an app = Connector. Both = both. One-off = neither. |
| **Building** | Describe it to skill-creator. Test what starts it. Test the output. Fix. |
| **Portability** | Skills are an open standard — they travel across Claude.ai, Claude Code, OpenCode, Cowork, OpenWork, and even OpenAI/Google CLI tools. GPTs and Gems are locked to one vendor. |
| **Safety** | Read skills before enabling. Install from trusted sources. Start connectors read-only. Keep scope small. |

---

## Six Practice Prompts (Try These in Claude.ai)

**1. Start a built-in skill:**  
Turn on *Code execution and file creation* in Settings → Capabilities, then:
```
Turn this into a one-slide PowerPoint with a title and three bullet points:
[paste any three facts about your work].
```
Watch it fire on its own — you never named the skill.

**2. Connect one app, read-only:**  
Connect Drive or Gmail, enable it for the chat, then:
```
Find [a specific document] in my Drive and give me a three-sentence
summary plus the three numbers that matter most.
```
Notice: you never downloaded or pasted anything.

**3. Build your first skill:**  
Pick the most repetitive "I keep re-explaining how" task in your week:
```
Use the skill-creator skill to help me build a skill for [your task].
Here's exactly how I want it done every time: [list your rules,
your format, your must-dos and must-nots]. Ask me anything you
need, then build it.
```

**4. Pressure-test the description:**  
After the skill is built and installed:
```
When would you use the skill we just made? And when would you NOT use it?
```
If the answer is too wide or too narrow, tell it the fix.

**5. Audit a skill for safety:**  
For any skill you did not write:
```
Read this skill and tell me, in plain language, exactly what it
instructs you to do. Flag anything that contacts an external
server, handles credentials, or could send my data anywhere.
```

**6. Diagnose three tasks:**  
Write down three recurring annoyances from your work. For each one: is the friction re-explaining *how* (Skill), fetching from an app (Connector), or both? Those are your first three projects.

---

## Troubleshooting Quick Reference

| Problem | Do not do | Do this |
|---|---|---|
| Skill never fires | Guess at the problem | Ask AI "When would you use my [name] skill?" — the answer reveals what to fix |
| Skill fires on wrong things | Add more instructions | Narrow the description or add a negative trigger |
| Output is right at first, drifts later | Edit the skill file | Start a fresh chat — the skill is fine; the chat got long |
| Same mistake every run | Reword the instruction | Move the exact step into a script (ask skill-creator to do it) |
| Connector "can't find" a file | Assume it's broken | Confirm the connector is enabled *for this chat*, and that your account can open the file |
| AI answered from a glance instead of using connector | Accept the answer | Say: "Use my [app] connector to fetch the actual file before answering, and tell me which file you used." |
| Nervous about write access | Grant it anyway | Stay read-only; grant write only after the tool has behaved well |
| Chat is long and confused | Keep adding prompts | Start fresh — a tangled chat is cheaper to abandon than rescue |

---

*Source: [agentfactory.panaversity.org/docs/skills-connectors-crash-course](https://agentfactory.panaversity.org/docs/skills-connectors-crash-course)*  
*Part of the Panaversity Agent Factory Program — Foundations (Everyone) track.*