---
title: AI Secure Browser
type: project
status: active
created: 2026-06-10
updated: 2026-06-10
tags: [tauri, browser, project-setup]
---

# AI Secure Browser

**A local-first, security-first desktop browser shell built with Tauri 2 and a TypeScript frontend.**

## Summary
A personal learning project designed to build a custom browser shell rather than a rendering engine. It supports two possible backend architectures: a Tauri-native Rust backend and a PyTauri Python backend. The application design emphasizes a strict security posture with a default-deny command design and optional, non-foundational AI features.

## Key points
- Local-first application architecture working entirely without server-side requirements (from [[2026-06-10--ai-secure-browser-readme]], [[2026-06-10--ai-secure-browser-architecture]]).
- Security-first boundary treating remote content as untrusted and keeping backend commands minimal and explicitly configured (from [[2026-06-10--ai-secure-browser-security-rules]]).
- Supports Rust-native Tauri commands (`invoke`) or PyTauri Python commands (`pyInvoke`) for backend logic (from [[2026-06-10--ai-secure-browser-rust-track]], [[2026-06-10--ai-secure-browser-python-track]]).
- AI augmentation (e.g., using Gemini via `google-genai` SDK) is entirely optional and kept behind toggles/flags (from [[2026-06-10--ai-secure-browser-readme]], [[2026-06-10--ai-secure-browser-security-rules]]).

## Status
Phase 1 setup and scaffolding is being planned with two backend options.

## Next action
Decide between the Rust track (Tauri native) or the Python track (PyTauri) to scaffold the initial codebase.

## Related
- [[tauri]] — the core desktop app framework.
- [[pytauri]] — Python bindings for Tauri.
- [[browser-shell]] — the architectural concept behind this app.

## Open questions
- Which track is preferred for the primary implementation: Rust or Python?

## Sources
- [[2026-06-10--ai-secure-browser-readme]]
- [[2026-06-10--ai-secure-browser-architecture]]
- [[2026-06-10--ai-secure-browser-security-rules]]
- [[2026-06-10--ai-secure-browser-rust-track]]
- [[2026-06-10--ai-secure-browser-python-track]]
