---
title: LLM Wiki Pattern
type: concept
status: active
created: 2026-05-18
updated: 2026-05-18
tags: [knowledge-management, llm, second-brain]
---

# LLM Wiki Pattern

**A three-layer architecture for personal knowledge bases where an LLM continuously maintains a markdown wiki on top of immutable raw sources, guided by a schema document.**

## Summary
Proposed by [[andrej-karpathy]] (from [[2026-05-18--llm-wiki-gist]]). The wiki is a persistent, compounding artifact that grows richer with each source and question. The LLM owns the bookkeeping; the human owns curation, direction, and analysis. This vault's [[CLAUDE]] is a concrete instantiation of the pattern.

## Key points
- **Three layers**: raw sources (immutable), wiki (mutable, LLM-maintained), schema (the rules).
- **Three operations**: ingest, query, lint.
- **Two navigation files**: `index.md` (catalog) and `log.md` (append-only history).
- The wiki itself is the artifact — not embeddings, not a vector store, just readable markdown.

## Why this works
- Markdown is durable, diffable, portable across tools.
- The LLM removes the maintenance friction that kills most personal wikis.
- Cross-linking makes the graph dense over time — the more you put in, the more useful each query becomes.

## Related
- [[second-brain]] — broader category
- [[andrej-karpathy]] — author
- [[vault-bootstrap]] — this vault's instantiation of the pattern

## Open questions
- What's the right lint cadence — weekly? after N ingests?
- When should a wiki page split into two vs. stay one long page?

## Sources
- [[2026-05-18--llm-wiki-gist]]
