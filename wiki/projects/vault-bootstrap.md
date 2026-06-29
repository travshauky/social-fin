---
title: Vault Bootstrap
type: project
status: active
created: 2026-05-18
updated: 2026-05-18
tags: [meta, vault]
---

# Vault Bootstrap

**Standing up this Obsidian vault as a karpathy-style second brain.**

## Status
Bootstrapped 2026-05-18. Schema in [[CLAUDE]] is v1. Folder structure, [[index]], and [[log]] are live. First source ingested: [[2026-05-18--llm-wiki-gist]].

## Next action
Decide which categories matter most to Shauky and start the second real ingest. Candidates: a book in progress, a current work project, a recurring decision area.

## Key points
- Implements the [[llm-wiki-pattern]] from [[andrej-karpathy]].
- Folder layout: `sources/`, `wiki/{topics,people,concepts,projects}/`, `attachments/`.
- Every ingest must: save raw, touch wiki, update [[index]], append to [[log]].

## Related
- [[llm-wiki-pattern]] — the pattern being instantiated
- [[second-brain]] — the genre

## Open questions
- Tag taxonomy: free-form or controlled vocabulary?
- Lint cadence?
- Should `attachments/` mirror the `wiki/` subfolder structure?

## Sources
- [[2026-05-18--llm-wiki-gist]]
