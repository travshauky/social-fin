---
title: LLM Wiki Pattern
source_url: https://gist.githubusercontent.com/karpathy/442a6bf555914893e9891c11519de94f/raw/ac46de1ad27f92b28ac95459c782c07f6b8c964a/llm-wiki.md
source_type: gist
captured: 2026-05-18
tags: [llm, knowledge-management, second-brain, karpathy]
---

# LLM Wiki Pattern

_Author: Andrej Karpathy. The canonical text lives at the source_url above; this file captures the extracted structure and key claims. The gist is intentionally abstract — meant to be instantiated by each user with their LLM._

## Main concept

Build persistent, structured knowledge bases where LLMs incrementally maintain markdown wikis rather than simply retrieving from raw documents. The wiki is a **persistent, compounding artifact** that grows richer with each source and question.

## Three-layer architecture

1. **Raw sources** — immutable documents the LLM reads.
2. **The wiki** — LLM-generated markdown files the LLM maintains.
3. **The schema** — configuration document defining structure and workflows.

## Key operations

- **Ingest** — process new sources, update relevant pages, maintain cross-references.
- **Query** — search wiki pages, synthesize answers with citations, file valuable results back.
- **Lint** — health-check for contradictions, orphaned pages, and gaps.

## Navigation

- **index.md** — content catalog organized by category.
- **log.md** — append-only chronological record with parseable timestamps.

## Core insight (quoted)

> "The tedious part of maintaining a knowledge base is not the reading or the thinking — it's the bookkeeping."

LLMs handle the maintenance burden that typically causes humans to abandon wikis; humans focus on curation, direction, and analysis.

## Supporting tools (suggested, optional)

Obsidian (IDE), qmd search engine, Dataview plugin, Marp for presentations, Web Clipper for source capture.

---
**Ingest notes (Claude-written, mutable):**
- Key claims: three-layer split; LLM does bookkeeping; wiki compounds.
- Wiki touches: [[andrej-karpathy]], [[llm-wiki-pattern]], [[second-brain]], [[vault-bootstrap]]
- Open question for the user: which categories matter most to you (work projects, reading notes, people, decisions)?
