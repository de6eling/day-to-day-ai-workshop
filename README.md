# Day-to-Day AI — Workshop Kit

Everything you need to follow along, in one place. Copy the prompts straight from this page into Claude.

Throughout the day you'll build **one ecommerce brand** and carry it through four blocks:

| Block | Where | You'll build |
|---|---|---|
| 1 — Prompting & Artifacts | Claude **Chat** | Your brand, captured as a one-page brief |
| 2 — Projects & Connectors | Claude **Chat** | A social-post machine that makes posts + Canva graphics |
| 3 — Routines & Tasks | Claude **Cowork** | A weekly competitor report that writes itself to a folder |
| 4 — Large Context & Skills | Claude **Code** | Your whole brand as a navigable wiki you open in a browser |

> **The one idea for the day:** an AI is like predicting the next line of a movie.
> *Context* = the movie · *Tokens* = the words · *Prompt* = everything before the next line · *Response* = the line that comes next.

---

## Block 1 — Prompting & Artifacts *(Chat)*

**Goal:** bring *your own* brand idea to life through conversation, then save it as a file.

**1. Start the strategist conversation** (paste, then fill in your idea):
```text
Act as a sharp brand strategist. I have a rough idea for a new ecommerce
brand, and I want you to help me refine it through conversation — not write
it for me.

My starting idea:
[one or two sentences — your rough brand idea]

How I want you to work with me:
- Ask me one focused question at a time — the kind a real brand strategist
  would ask to sharpen the idea (customer, problem, what makes it different, why me).
- Wait for my answer before moving to the next question.
- Push back when an answer is vague or generic — don't just agree.
- Build on what I give you; don't invent the brand for me.

Context: this is for a workshop demonstrating practical, day-to-day uses of AI.

Start by reflecting back what you understand about my idea, then ask your
first question.
```

Then just **answer its questions**.

**2. Capture it as your foundation file:**
```text
Summarize the brand we built into a one-page brand brief. Make it a file.
Include: brand name, one-sentence concept, target customer, problem we solve,
product line, brand voice, and 3 launch-message ideas.
```

**Go further:**
```text
Argue that this brand will fail. Give me your three strongest reasons.
```
…then make it defend the brand against its own attack.

**Keep this file — every later block builds on it.**

---

## Block 2 — Projects & Connectors *(Chat)*

**Goal:** build a project that turns any subject into on-brand Instagram posts **and** Canva graphics.

**Setup:** Create a new project → download your Block 1 brand brief from chat → upload it as **Project Knowledge** → connect **Canva**.

**Project Instructions** — this is your prompt-writing rep. Fill *every* blank using the ingredients from Block 1 (Role · Goal · Audience · Voice · Constraints). The richer your blanks, the more on-brand the machine:
```text
Act as a [role] for the brand in the project knowledge.

Audience: [who these posts are for]
Goal: [what you want the posts to achieve]
Brand voice: [your tone — a few words]
Visual style: [the look of the graphics]
Always avoid: [your hard rules — what it should never do]

When I give you a subject, write Instagram posts for it. For each post,
return as plain text:
- Post copy
- Visual direction
- Suggested CTA

Then use the Canva connector to create an Instagram graphic for each post,
following its visual direction and the visual style above. Keep everything
consistent with the brand and these settings every time.
```

**Run it:**
```text
This week's subject: [your subject]. Write 3 Instagram posts and create the graphics.
```

**Go further:**
```text
This week's subject: [a totally different subject]. Write 3 Instagram posts and create the graphics.
```
Does the voice and the look still hold? That's the real test of the machine.

---

## Block 3 — Routines & Tasks *(Cowork)*

**Goal:** a task that writes a weekly competitive analysis into your brand folder, on its own.

**Setup (go slow here):**
1. Make a folder on your computer called **`my-brand`**.
2. Download your **brand brief** (Block 1) and **social posts** (Block 2) from chat into it.
3. Cowork → **Schedules → New task → Create with Claude**.
4. **Add folder** (`my-brand`) — *do this before answering any questions.*
5. Turn on **auto-accept edits**.

**Describe the task** (then answer Claude's setup questions):
```text
Every Monday, research the main competitors of the brand in brand-brief.md
in this folder, and write a short competitive analysis to this folder:
- 3–5 key competitors
- What each does well and where they're weak
- Notable recent moves (products, campaigns, pricing)
- 2–3 opportunities for our brand
Save each week's file dated, and keep it skimmable.
```

**Then hit "trigger" / "run now"** to see the file appear — no need to wait a week.

**Go further:** create a *second* task on a different cadence — e.g. a daily industry-trend scan — also writing to the `my-brand` folder.

---

## Block 4 — Large Context & Skills *(Claude Code)*

**Goal:** turn your whole `my-brand` folder into a navigable wiki you open in your browser.

Open Claude Code **in your `my-brand` folder**.

**Step 0 — Install the skill** (no GitHub account or `git` needed — Claude Code just downloads one file):
```text
Download this file and save it to .claude/skills/brand-wiki/SKILL.md in this
project (create the folders if needed), then tell me to restart Claude Code:
https://raw.githubusercontent.com/de6eling/day-to-day-ai-workshop/main/skills/brand-wiki/SKILL.md
```
Then **restart the Claude Code session** so the skill is ready.

**Step 1 — Build the wiki:**
```text
Read every file in this folder and treat it all as raw source material
about my brand.

Decide the key topics yourself, then distill the material into one short note
per topic. For each note, note which other notes it relates to.

Then build a single self-contained file called brand-wiki.html in this
folder that I can open by double-clicking. It must:
- show an interactive graph: each note is a node, lines connect related notes
- let me click a node to open and read that note beside the graph
- use only plain inline JavaScript — no external libraries, no CDN, no
  internet — so it works fully offline

Keep each note short and skimmable.
```

**Step 2 — Double-click `brand-wiki.html`** and explore your brand's whole story as a graph.

**Step 3 — The level-up:** run the same thing in one word:
```text
/brand-wiki
```

**Go further:** open `.claude/skills/brand-wiki/SKILL.md`, change how it builds the wiki (a new note type, your brand colors, a different layout), and run `/brand-wiki` again. *A skill is just a file you own and can reshape.*

---

## What's in this repo

- `README.md` — this page (all the prompts).
- `skills/brand-wiki/` — the **Brand Wiki** skill used in Block 4.
