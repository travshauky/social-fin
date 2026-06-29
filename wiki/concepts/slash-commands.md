---
title: Slash Commands
type: concept
status: active
created: 2026-05-19
updated: 2026-05-19
tags: [vault, commands, claude-code, vin]
---

# Slash Commands

**Reusable, named prompts stored in `.claude/commands/*.md` that Claude Code surfaces as `/<name>` in any session opened inside this vault.**

## Summary
A [[vindates|Vindate]] from [[internet-vin]]. Each command is a tightly-scoped prompt that knows the vault layout (`sources/`, `wiki/`, `daily/`, `attachments/`), the schema in [[CLAUDE]], and the vault's privacy boundaries. Commands codify Vin's reflective workflow into one-keystroke entry points.

## Installed commands (v1, 2026-05-19)

### Daily operations
- `/context` — load full vault context before working on anything.
- `/today` — morning review; prioritized plan for the day.
- `/close-day` — end-of-day processing; extract action items, surface connections, prompt confidence updates.

### Thinking tools
- `/ghost <question>` — answer in Shauky's voice using the vault as voice corpus; evaluate fidelity.
- `/challenge <belief>` — pressure-test a belief against the vault's own history.
- `/emerge` — surface ideas the vault implies but never states.
- `/drift` — compare stated intentions against actual behavior over 30–60 days.
- `/ideas` — deep 30-day cross-domain scan for actionable ideas.
- `/trace <topic>` — trace how an idea has evolved across the vault.
- `/connect <domain-a> <domain-b>` — bridge two domains via the link graph.

### Delegation helpers
- `/schedule <meeting>` — vault-aware recommendation on a proposed meeting.
- `/graduate` — promote daily-note ideas into standalone wiki pages.

## Authoring rules
- Commands live in `.claude/commands/<name>.md`.
- Frontmatter must include `description:`.
- Commands must honor the vault's privacy boundaries before any external send.
- Commands must respect the [[vindates|human-only-in-daily]] rule: never write to `daily/`.
- Commands SHOULD respect the karpathy rule for `wiki/`: write only after a clear synthesis is warranted, never speculative drafts.

## Related
- [[vindates]] — overall changeset
- [[internet-vin]] — source of the command set
- [[daily-notes]] — what most commands read
- [[obsidian-cli]] — what unlocks the graph awareness

## Open questions
- Build a `/lint` command to codify the existing schema lint workflow?
- Build a meta `/suggest-command` that recommends new commands based on vault patterns (Vin's "higher abstraction" trick)?

## Sources
- [[2026-05-19--internet-vin-obsidian-claude]]
