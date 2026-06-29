---
title: Daily Notes
type: concept
status: active
created: 2026-05-19
updated: 2026-05-19
tags: [vault, schema, daily, vin]
---

# Daily Notes

**The `daily/` folder is the continuous, dated capture stream of this vault. One file per day, human-written-only.**

## Summary
A [[vindates|Vindate]] from [[internet-vin]]. Daily notes are where raw thought, observations, hypotheses, and inline delegations live. Unlike `wiki/` pages — which are Claude-maintained synthesis — `daily/` is the part of the vault that respects Vin's strict separation: the agent reads it but never writes to it.

## Conventions
- **Path**: `daily/YYYY-MM-DD.md` (one file per day).
- **Frontmatter**: `date`, optional `domain` (if "day per domain" is adopted), optional `tags`.
- **Visibility**: defaults to `public` per [[Hi Shauky]] v2; flip to `private` when needed.
- **Anatomy** (suggested, not enforced):
  - `## Capture` — raw thought, observations, links.
  - `## Hypotheses` — half-formed ideas with `confidence:` markers.
  - `## @delegate` — items for an agent to pick up (inline delegation pattern).
  - `## Reflect` — end-of-day pass written by Shauky after `/close-day`.

## How commands use daily notes
- `/today` reads the last 7 days of daily notes to build the morning plan.
- `/close-day` reads today's daily note, extracts action items, suggests confidence-marker updates, surfaces vault connections.
- `/drift` reads 30–60 days of daily notes and compares stated intent vs. actual behavior.
- `/graduate` scans recent daily notes for ideas worth promoting to standalone `wiki/` pages.
- `/trace` and `/emerge` cross-reference daily notes with wiki pages.

## Why daily ≠ wiki
- **Daily** is *the writing surface*. Cheap, dated, lossy. Most of it stays put.
- **Wiki** is *the synthesis surface*. Curated, named by concept, dense in links.
- The `/graduate` command is the bridge — promotes good daily-note material into wiki pages.

## Related
- [[vindates]] — overall changeset
- [[internet-vin]] — source person
- [[slash-commands]] — commands that read this folder
- [[thinking-partner-pattern]] — why this folder is human-only

## Open questions
- Adopt "day per domain"? (Monday = X, Tuesday = Y, etc.)
- Add a `meetings/` sub-convention for Granola/Gemini drops?

## Sources
- [[2026-05-19--internet-vin-obsidian-claude]]
