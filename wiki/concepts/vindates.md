---
title: Vindates
type: concept
status: active
created: 2026-05-19
updated: 2026-05-19
tags: [vault, schema, meta, vin]
---

# Vindates

**The set of updates layered onto the original karpathy-style schema of this vault, sourced from [[internet-vin]]'s Obsidian + Claude Code workflow. Each Vindate is a deliberate addition that does *not* duplicate something the [[llm-wiki-pattern]] already provides.**

## Why the name
Shauky's coinage — "Vindates" = "Vin's updates". Tracked separately so the karpathy substrate stays legible underneath. The full active set lives in [[CLAUDE]] §10.

## The Vindates (v1, 2026-05-19)

1. **`daily/` folder** — a new top-level folder for continuous, dated, human-written-only daily notes. See [[daily-notes]].
2. **Strict human/agent separation scoped to `daily/`** — Vin's rule that the agent doesn't write into the vault is honored *for daily notes only*. The wiki stays Claude-maintained per [[llm-wiki-pattern]]. This resolves the karpathy/Vin philosophical tension cleanly.
3. **Confidence markers** — wiki pages of `type: concept` or `type: project` may carry a `confidence:` frontmatter field (`high | medium | low | tentative`). Revisited periodically; surfaced by `/close-day`.
4. **Inline delegation pattern** — in a daily note, write `@delegate: <unit of work>` to mark an item an agent should pick up. New UX pattern, no automation built yet.
5. **Slash command set** — ~12 commands installed in `.claude/commands/` (see [[slash-commands]]).
6. **Thinking-partner-over-builder stance** — recorded as the vault's primary use mode. See [[thinking-partner-pattern]].

## What's deliberately NOT a Vindate

Vin proposes ideas this vault already implements via karpathy; these are not duplicated:
- Markdown as substrate, vault-as-second-brain
- Wiki interlinking / graph
- Source-of-truth context files passed to agents
- Lint-style orphan / dead-end detection (already in [[CLAUDE]] §3.3)
- Privacy weight of agent access (already in [[Hi Shauky]])

## Resolved tensions

| Topic | Karpathy | Vin | This vault |
|---|---|---|---|
| Who writes wiki pages? | LLM maintains | Human only | **LLM in `wiki/`, human in `daily/`** |
| Primary use mode | Compounding knowledge base | Thinking partner | **Both — wiki compounds, commands reflect** |
| Bookkeeping cost | LLM absorbs it | Human owns curation | **LLM does ingest bookkeeping; human owns daily notes** |

## Related
- [[internet-vin]] — source person
- [[llm-wiki-pattern]] — the substrate being extended
- [[daily-notes]] — the new folder convention
- [[slash-commands]] — the command set
- [[thinking-partner-pattern]] — the stance
- [[CLAUDE]] §10 — the binding schema entry

## Open questions
- Will more Vindates land as Shauky uses the commands? Likely.
- Should "day per domain" become Vindate #7?

## Sources
- [[2026-05-19--internet-vin-obsidian-claude]]
