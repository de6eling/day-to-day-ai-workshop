# Day-to-Day AI — Workshop Kit

Everything you need to follow along, in one place. Copy the prompts straight from this page into Claude.

Throughout the day you'll build **one ecommerce brand** and carry it through four blocks:

| Block | Where | You'll build |
|---|---|---|
| 1 — Prompting & Artifacts | Claude **Chat** | Your brand, captured as a one-page brief |
| 2 — Projects & Connectors | Claude **Chat** | A social-post machine that makes posts + Canva graphics |
| 3 — Routines & Tasks | Claude **Cowork** | A weekly competitor report that writes itself to a folder |
| 4 — Live Artifacts & Connectors | Claude **Cowork** | A live dashboard that pulls real data from a connector you use |

*Blocks 1–3 build your brand; Block 4 finishes with a live dashboard from a connector you already use. The surface escalates Chat → Cowork — your presenter will point you to each. Anything in `[brackets]` is a fill-in-the-blank: replace it, brackets and all.*

> **The one idea for the day:** an AI is like predicting the next line of a movie.
> *Context* = the movie · *Tokens* = the words · *Prompt* = everything before the next line · *Response* = the line that comes next.

---

## Block 1 — Prompting & Artifacts *(Chat)*

**Goal:** bring *your own* brand idea to life through conversation, then save it as a file.

**1. Start the strategist conversation.** First, pick your starting idea. Below are a few to get you going — **keep the one you like and delete the rest**, or replace them all with a rough idea of your own:

```text
Starting ideas (keep one, delete the others — or write your own):
- Refillable home-cleaning products that ship as concentrated pods, so you buy the bottle once and never throw it away.
- A snack box for desk workers built around afternoon energy slumps — no sugar crash, portioned for one.
- Everyday basics (tees, socks, totes) made from deadstock fabric that would otherwise be thrown out.
- Starter kits for first-time houseplant owners — the plant, the right pot, and a simple care card that texts you reminders.
- Pet treats made from "ugly" produce and trimmings that grocery stores reject.
```

Then paste the prompt below, with your chosen idea filled in:
```text
Act as a brand strategist. I have a rough idea for a new ecommerce
brand, and I want you to help me refine it through conversation.

My starting idea:
[one or two sentences — your rough brand idea]

How I want you to work with me:
- Ask me one focused question at a time — the kind a real brand strategist
  would ask to sharpen the idea (customer, problem, what makes it different, why me).
- Wait for my answer before moving to the next question.
- We should get to a good brand definition within 8-12 questions.
- Define brand name, one-sentence concept, target customer, problem we solve, product line, brand voice, and 3 launch-message ideas
- Push back when an answer is vague or generic — don't just agree.
- Build on what I give you; don't invent the brand for me.

Context: this is for a workshop demonstrating practical, day-to-day uses of AI.

Start by reflecting back what you understand about my idea, then ask your
first question.
```

Then just **answer its questions**.

**2. Capture it as a file** — it opens in a side panel called an *artifact*:
```text
Summarize the brand we built into a one-page brand brief. Make it a markdown file.
Include: brand name, one-sentence concept, target customer, problem we solve,
product line, brand voice, and 3 launch-message ideas.
```

**3. Save it:** click the download icon on the artifact and save it as **`brand-brief.md`** (it lands in your **Downloads** folder). You'll reuse this exact file in every later block.

**Go further:**
```text
Argue that this brand will fail. Give me your three strongest reasons.
```
…then make it defend the brand against its own attack.

---

## Block 2 — Projects & Connectors *(Chat)*

**Goal:** build a project that turns any subject into on-brand Instagram posts **and** Canva graphics.

**Setup:** Create a new project → upload your **`brand-brief.md`** (from **Downloads**) as **Project Knowledge** → connect **Canva** *(needs a free Canva account; click Allow when it asks to connect)*.

**Project Instructions** — this is your prompt-writing rep. Fill *every* blank using the ingredients from Block 1 (Role · Goal · Audience · Voice · Constraints). The richer your blanks, the more on-brand the machine:
```text
Act as a [role] for the brand in the project knowledge.

Audience: [who these posts are for]
Goal: [what you want the posts to achieve]
Brand voice: [your tone — a few words]
Visual style: [the look of the graphics]
Always avoid: [your hard rules — what it should never do]

We make one Instagram post per chat, step by step. When I give you a subject:
1. Write only the post copy first  (caption + suggested CTA) in a markdown (.md) file -- no image yet.
2. Ask me whether to revise the copy, or if I'm ready for the image.
3. Once I approve, use the Canva connector to make one Instagram graphic
   that follows the copy and the visual style above.
4. Ask me whether to revise the image.
5. When I'm happy, tell me to start a new chat in this project for the next post.

Keep everything consistent with the brand and these settings every time.
```

**Run it** — give a subject; the project walks you through copy → image, one post at a time:
```text
This week's subject: [your subject].
```
**Make 3 posts total** — start a **new chat in the project** for each one. Notice the project still knows your brand in every new chat.

**Save the posts:** in one chat, paste the copy from your finished posts and type *"put these in one markdown file, starting with a short header naming the brand and its voice"*, then download it as **`social-posts.md`** (you'll need it in Block 3).

**Go further:** start a new chat and give a *totally different* subject — does the voice and the look still hold? That's the real test of the machine.

---

## Block 3 — Routines & Tasks *(Cowork)*

**Goal:** a task that writes a weekly competitive analysis into your brand folder, on its own.

**Setup (go slow here):**
1. Make a folder on your **Desktop** called **`my-brand`**.
2. From your **Downloads** folder, move **`brand-brief.md`** and **`social-posts.md`** into it.
3. Cowork → **Schedules → New task → Create with Claude**.
4. **Add folder** (`my-brand`) — *before answering any questions* (this lets Claude read and write files there).
5. Turn on **auto-accept edits** (lets it save files without asking each time).

When you start, Claude asks what you want the task to do and offers a few ready-made options. **Don't pick one** — in that first question, type the task in your own words.

Then **just answer Claude's follow-up questions** as it walks you through the rest of the setup.

**Run it:** hit **"trigger" / "run now"** to see the file appear — no need to wait a week.

**Revise until it's right:** open the file Claude wrote. Not quite what you wanted — too long, wrong competitors, missing opportunities? Manually update the *task instructions*, and **run it again**. Repeat until the report looks the way you want.

**Go further:** create a *second* task on a different cadence — e.g. a daily industry-trend scan — also writing to the `my-brand` folder.

---

## Block 4 — Live Artifacts & Connectors *(Cowork)*

**Goal:** build a **live artifact** — a dashboard that pulls real data from a connector you use and renders it as something interactive you can keep open. The artifacts you made earlier were just *files* — a snapshot, frozen the moment you saved them. A **live artifact** is different: it connects to a live source, so it actually works and stays up to date.

**1. Pick a connector.** Below are a few dashboards you could build — **keep the one you want and delete the rest**, or pick another connector you already have:

```text
Connector ideas (keep one, delete the others — or use another you have):
- Shopify — a store dashboard: revenue, orders, average order value, top products, low stock
- Slack — a daily-update dashboard: highlights from your key channels, who needs a reply, action items
- Google Calendar — a week-ahead dashboard: meetings, focus blocks, scheduling conflicts
- Gmail — an inbox-triage dashboard: who's waiting on you, threads to reply to, newsletters to skip
- Linear / Notion — a project dashboard: what's in progress, what's blocked, what shipped this week
```

**Setup:** Cowork → **connect your chosen connector** *(click Allow when it asks).*

**2. Build the live artifact** — paste, filling in the blanks for the connector you picked:
```text
Create a live artifact: a dashboard that uses the [connector] connector to
pull real data and stay up to date.

It should show me at a glance:
- [the 3–5 things you most want to see — e.g. today's orders, unread highlights, this week's meetings]

Make it:
- one interactive artifact I can keep open
- visual — cards, big numbers, and simple charts, not walls of text
- built on the real data you pull from the connector right now; tell me the exact time range it covers
- organized so the single most important thing is at the top

Walk me through what you pulled, then render the dashboard.
```

**3. Refine it live** — the artifact updates in place as you ask:
```text
[a tweak — e.g. "add a bar chart of orders by day", "group these by status",
"highlight anything that needs my attention in red"]
```

**Go further:** ask it *"which one thing here should I act on first, and why?"* — let the dashboard not just show the data but tell you what to do about it.

---

## What's in this repo

- `README.md` — this page (all the prompts).
- `skills/brand-wiki/` — a bonus **Brand Wiki** skill for Claude Code: turn your `my-brand` folder into a navigable offline wiki. Optional, great to try after the workshop.
