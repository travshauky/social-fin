---
title: Obsidian CLI
type: concept
status: stub
created: 2026-05-19
updated: 2026-05-19
tags: [obsidian, tooling, claude-code]
---

# Obsidian CLI

**A command-line tool released by the Obsidian team that exposes the vault's *graph* — not just the files — to external agents like Claude Code.**

## Summary
A [[vindates|Vindate]] enabler. Without the Obsidian CLI, an agent sees a folder of markdown files. With it, the agent can query inter-relationships: which files link to which, orphans, dead-ends, resolved links, tag counts. This is what makes [[internet-vin]]'s pattern-detection commands feasible.

## What it gives the agent
- File contents (already possible without the CLI).
- **Graph edges** — `[[wikilinks]]` resolved into a navigable structure.
- **Orphans** — pages with no inbound links.
- **Dead ends** — pages that link out but nothing links back.
- **Tag inventory** and counts.

## How this vault uses it
Many of the [[slash-commands]] explicitly call CLI-derived structure: `/connect`, `/trace`, `/emerge`, `/ideas`, `/graduate` all benefit from graph awareness, not just full-text search.

## Related
- [[internet-vin]] — the demo where this surfaced
- [[vindates]] — overall changeset
- [[slash-commands]] — consumers of CLI-derived graph data
- [[llm-wiki-pattern]] — pattern this tool empowers

## Open questions
- Install/setup link? — capture once Shauky installs it.
- Are graph queries cached or live-read per command? Latency tradeoff.

## Sources
- [[2026-05-19--internet-vin-obsidian-claude]]
