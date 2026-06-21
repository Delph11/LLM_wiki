---
namespace: personal
type: [understanding]
date-created: 2026-06-19
source-file: meta
---

# LLM Wiki Usage Guide

How to use this wiki system with Claude — prompts, workflows, and rhythm.

---

## 1. Yes, you have to prompt Claude Code after every upload — but read Q5

There's no automatic trigger. Claude Code doesn't watch your folder in the background. But Q5 solves this — keep reading.

---

## 2. Case A vs Case B — and a general rule

**Case A — Treat each point separately:** Use this when the note is a **list of unrelated or loosely related observations.** Like "Thoughts 2" — each point is its own idea that could belong to different themes.

Prompt:

> "I've added raw/filename.md. Each numbered point is a separate observation — treat them individually, identify the theme of each, and file insights where they belong. Follow CLAUDE.md rules. Tell me your plan first."

**Case B — Treat as a whole:** Use this when the note is **one coherent piece** — a reflection on a single event, a journal entry about one day, notes from one class, a single article summary.

Prompt:

> "I've added raw/filename.md. This is a single coherent note — summarise the key ideas as a whole and create or update the relevant wiki page. Follow CLAUDE.md rules. Tell me your plan first."

**The general rule to decide:**

Ask yourself — _does this note have one topic or many?_

|Note type|Case|
|---|---|
|Numbered list of random thoughts|A|
|Journal entry about one day|B|
|Google Keep brain dump|A|
|MBA class notes on one topic|B|
|"Things I noticed this week"|A|
|A reflection on one relationship/event|B|

When genuinely unsure, **default to Case A**. Treating a unified note as separate points loses a little coherence. But treating a multi-point note as a whole loses individual insights — which is worse.

---

## 3. How the wiki builds and how you actually benefit from it

The wiki builds through **accumulation and cross-linking.** Each time Claude processes a note it either creates a new page or _adds to an existing one._ So "self-doubt" might appear as a point in Thoughts 2, then again in a journal entry, then again in a Keep note about confidence — and Claude keeps filing all of it into the same `wiki/self-doubt.md` page, which grows richer each time.

**How you get the benefit — three concrete ways:**

First, **querying.** This is the main one. Open Claude Code, open PrivateBrain, and just ask in plain English:

> "What patterns do I have around self-doubt? What have I noticed across all my notes?"

Claude reads the wiki (not all the raw files — just the structured wiki pages) and synthesises an answer from everything you've ever added. This is something no journal or Keep note can do.

Second, **before a hard conversation or decision.** Say you're nervous before a presentation:

> "What do I know about how I handle nerves and confidence? What has worked for me before?"

Claude pulls from everything relevant in your wiki and gives you _your own_ best thinking back to you.

Third, **monthly lint check.** The Routine you'll set up will surface things like: "You have three pages that all seem to be about fear of judgment — should I merge them?" That's when you see the real shape of your thinking.

The graph in Obsidian is just a visual — the real value is in Claude being able to answer questions using accumulated knowledge.

---

## 4. Adding new points to an existing raw file

Yes, you'd have to run Claude Code again — but here's the thing: **you don't have to do it immediately.** Just add the point and leave it. Batch it with everything else at end of day. Which leads to Q5.

---

## 5. Yes — end of day batch processing is the right approach

This is actually the _better_ way to run the system. Here's the prompt to save as a **Routine** in Claude Code so you don't have to type it every night:

> "Run an end-of-day processing pass on PrivateBrain.

**Step 1 — New files:** Check raw/ for any files that have no corresponding wiki page. Process each one: if it contains a numbered list of separate points treat each point individually; if it is a single coherent note treat it as a whole.

**Step 2 — Modified files:** Check raw/ for any files that were modified more recently than their corresponding wiki pages. For each one, re-read the raw file and compare it against the existing wiki page. Add anything new that isn't reflected yet. If points have been removed from the raw file, flag them to me before removing anything from the wiki — I may want to keep the insight even if I deleted the raw point.

**Step 3 — Bookkeeping:** Update index.md to reflect any new or changed pages. Append a single end-of-day entry to log.md summarising everything processed.

Show me a summary of what you found and what you did before closing."

Save this as a Routine called **"PrivateBrain Evening Update"** in the Claude Code sidebar. Then each night before bed, open Claude Code, run the Routine, glance at the summary, and close it. Morning you wake up to an updated wiki.

This also solves the usage limit concern — one batch at night is far more efficient than a prompt after every single file.

---

**The rhythm in practice:**

- Throughout the day — dump raw notes into Obsidian freely, don't think about structure
- Before bed — run the Evening Update Routine
- Once a month — run the Lint Routine
- Whenever you need insight — open Claude Code and ask a question