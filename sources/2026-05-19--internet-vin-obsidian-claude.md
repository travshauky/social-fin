---
title: "Internet Vin on Obsidian + Claude Code (Greg Eisenberg podcast)"
source_url: https://www.youtube.com/watch?v=6MBq1paspVU
source_type: video
author: [Internet Vin, Greg Eisenberg]
published: 2026
captured: 2026-05-19
description: Vin walks through using Obsidian as a second brain paired with Claude Code via the Obsidian CLI, including a custom slash-command set for reflection, idea generation, and personal context delegation.
tags: [ai, obsidian, claude-code, second-brain, knowledge-management, vin, podcast]
---

# Internet Vin on Obsidian + Claude Code

(Transcript provided in conversation; full text omitted here for brevity but the source URL above is canonical.)

## Headline ideas (Claude's structured extract)

### What Obsidian gives you that a folder doesn't
- **Inter-relationships between files** via `[[wikilinks]]`. The graph, not the folder, is the artifact.
- **Visualizable graph** of links per file (local graph view).

### Obsidian CLI
- An Obsidian-released tool that lets Claude Code read both vault files *and* their inter-relationships — not just text, but structure.
- This is what makes "pattern detection across the vault" feasible from the CLI.

### Vin's core workflow philosophies
1. **LLM as thinking partner over LLM as builder.** Reflection > automation in his stack.
2. **Strict separation**: the agent does **not** write files into the vault. It writes outputs in the side pane; Vin decides what becomes a note. He wants to know that patterns the agent surfaces are about *his* writing, not the agent's own previous writing.
3. **Context-on-demand**: he passes context to the agent via a single command (`/context demo`) rather than re-explaining each session.
4. **Higher-level prompting**: instead of asking the LLM to do X, ask it to suggest commands that would take him from his current skill level to a higher one.

### Vin's custom slash commands (the heart of the video)

**Daily operations:**
- `/context` — load full context about life, work, current state. Reads context files, daily notes, follows back-links to build a complete picture.
- `/today` — morning review. Pulls calendar, tasks, iMessages, last week of daily notes → prioritized plan for the day.
- `/close-day` — end of day processing. Extracts action items, surfaces vault connections, checks confidence markers.

**Thinking tools:**
- `/ghost` — answers a question the way *Vin* would. Builds a voice profile from the vault, writes in that voice, then evaluates fidelity.
- `/challenge <topic>` — pressure-tests current beliefs using the vault's own history. Finds contradictions, counter-evidence, shifts in thinking.
- `/emerge` — surfaces ideas the vault implies but never states. Conclusions from scattered premises, unnamed patterns, unarticulated directions.
- `/drift` — compares stated intentions against actual behavior over 30–60 days. Surfaces what's being avoided.
- `/ideas` — deep 30-day vault scan with cross-domain pattern detection and graph analysis. Generates actionable ideas across all domains.
- `/trace <topic>` — tracks how an idea has evolved over time across the vault.
- `/connect <domain-a> <domain-b>` — bridges two domains using the vault's link graph.
- `/schedule <meeting>` — reads vault + calendar to give a recommendation on whether to take a proposed meeting.
- `/graduate` — daily-note idea extractor. Scans recent daily notes, identifies ideas (tagged or not), prompts to promote, merge, or dismiss.

### Notable structural patterns
- **Confidence markers** on hypotheses — Vin tags ideas with a confidence rating and revisits them.
- **"Day per domain"** structure — each day of the week gets a specific focus.
- **Inline delegation** — write a unit of work directly in a daily note (e.g. "schedule a call with X about Y") and an agent can pick it up later. New UX pattern.
- **Granola/Gemini meeting notes** drop straight into the vault under a `meetings/` structure.

### Where Vin's model differs from karpathy
- Karpathy says: *the LLM maintains the wiki*. Vin says: *the LLM doesn't write into the vault — the human does, the LLM reads*.
- Resolution in our model: wiki stays Claude-maintained (karpathy); daily notes are human-only (Vin). Sources are clipper/human-captured immutables. See [[CLAUDE]] §10 for the synthesized rule.

### Memorable quotes
- Greg: "the whole game is feeding the beast good context."
- Vin: "the quality of information that the agent has entirely determines what it can do for you."
- Greg: "a file is essentially perfect memory."
- Greg: "people think tokens are the oxygen — but they're not. The markdown files are the memories."
- Vin: "I want a response from LLMs that is very contextual to the things I'm writing about."

### Tension worth flagging
- Vin acknowledges the privacy weight: giving an autonomous agent access to your full vault is real exposure. We already encode this via [[Hi Shauky]].

---
**Ingest notes (Claude-written, mutable):**
- **Wiki touches**: [[internet-vin]], [[vindates]], [[obsidian-cli]], [[daily-notes]], [[thinking-partner-pattern]], [[slash-commands]]
- **Schema changes triggered**: CLAUDE.md §10 (Vindates) added; daily/ folder created; confidence markers in frontmatter; inline delegation pattern documented; .claude/commands/ slash command set built.
- **Hi Shauky check**: source is a public podcast on YouTube. All derived wiki pages default to public per [[Hi Shauky]] v2. No private topic triggers.
- **Open questions**:
  - Day-per-domain structure — does Shauky want to adopt this? Which days, which domains?
  - Granola/meeting integration — does Shauky want a `meetings/` folder convention?
  - The `/ghost` and `/drift` commands degrade in usefulness when daily notes are sparse — defer real testing until daily/ has 30+ days of content.
