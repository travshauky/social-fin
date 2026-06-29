---
title: Thinking-Partner Pattern
type: concept
status: active
created: 2026-05-19
updated: 2026-05-19
tags: [llm, workflow, reflection, vin]
---

# Thinking-Partner Pattern

**Treating the LLM primarily as a reflection and reasoning partner — not a builder of artifacts — anchored on a continuously-maintained personal vault.**

## Summary
A [[vindates|Vindate]] from [[internet-vin]]. The stance: most LLM value for an individual user comes from *the agent surfacing patterns in your own writing that you cannot see for yourself*, not from the agent producing artifacts on demand. Building is downstream of clear thinking. The vault is the substrate that makes the agent specific to *you*.

## Operating principles
- **Read-heavy, not write-heavy**. The agent reads the vault constantly; writes only when explicitly directed (or, in this vault, only inside `wiki/`).
- **Reflection commands beat task commands**. `/challenge`, `/emerge`, `/drift`, `/trace` are the high-leverage tools.
- **The vault as context fuel**. The reason these commands work is the depth of personal writing they pull from. Without sustained writing, the commands degrade fast.
- **Manage the vault, not the agent**. Instead of crafting better prompts, write more clearly in the vault — the agent's outputs improve automatically.

## When this pattern fails
- Sparse vault → shallow outputs. The commands are not a shortcut; they are an amplifier of accumulated writing.
- Voice mimicry (`/ghost`) only works once a meaningful corpus of first-person writing exists.
- Anti-pattern: asking the agent to produce a take and then back-filling the vault to match.

## Related
- [[internet-vin]] — source
- [[vindates]] — overall changeset
- [[daily-notes]] — the writing surface this pattern relies on
- [[slash-commands]] — the commands that operationalize the pattern
- [[llm-wiki-pattern]] — the karpathy substrate this layers on top of

## Open questions
- What writing cadence is the minimum for these commands to be useful — daily? 3×/week?

## Sources
- [[2026-05-19--internet-vin-obsidian-claude]]
