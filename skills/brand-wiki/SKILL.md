---
name: brand-wiki
description: Turn a folder of brand documents into a single self-contained, offline HTML knowledge graph (brand-wiki.html) — an interactive node graph plus readable notes. Use when the user wants to distill a folder of files into one navigable wiki page they can open in a browser.
---

# Brand Wiki

Turn the files in the current folder into one self-contained `brand-wiki.html`.

## Steps

1. **Read everything.** Read every file in the current folder and treat it all as raw source material about the user's brand.
2. **Decide the topics yourself.** Identify the key topics from the material — do not ask the user to list them. Distill the material into one short, skimmable note per topic.
3. **Connect them.** For each note, determine which other notes it relates to (its links).
4. **Build `brand-wiki.html`** in the current folder. It must:
   - be **fully self-contained and work offline** — all HTML, CSS, and JavaScript inline, **no external libraries, no CDN links, no network requests of any kind**;
   - open correctly by **double-clicking** the file (a local `file://`, no server required);
   - show an **interactive force-directed graph** where each note is a node and lines connect related notes;
   - let the user **click a node to open and read that note's full content** in a readable panel beside the graph;
   - use plain, hand-written JavaScript for the graph (e.g. canvas or SVG) — do not rely on any library being available.
5. **Report back.** Tell the user the file is ready and to double-click `brand-wiki.html` to open it.

## Reliability requirements (do not skip — this must render on the first try)

- **Embed note content as data, never as code.** Put all notes and links in a single `<script type="application/json">` block and read them in JS. **Never** inject note text directly into JavaScript strings or HTML — brand docs often contain quotes, backticks, or `</script>`, which would break the page and render it blank.
- **Keep nodes on screen.** Give the canvas a fixed size, clamp every node inside the visible bounds, and use a collision radius so nodes and labels don't overlap.
- **Crisp on Retina.** Scale the canvas for high-DPI displays so it's sharp on a projector.
- **Clean light theme** with high-contrast, readable labels.

## Guidelines

- Keep each note short — favor clarity over completeness.
- Node labels are the topic names; keep the graph readable, not crowded.
- If the folder contains dated files (e.g. weekly reports), fold their content into the relevant topic notes rather than making a node per file.
