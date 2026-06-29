---
title: AI Secure Browser - Project Readme
source_url: local
source_type: note
captured: 2026-06-10
tags: [tauri, browser, project-setup, local-first, python, rust]
---

# AI Secure Browser

A local-first, security-first browser shell built with **Tauri 2** and a **TypeScript frontend**, with a choice of backend:

- **Rust backend** using Tauri `invoke`
- **Python backend** using **PyTauri** and `pyInvoke`

This project is designed as a learning vehicle for becoming a better programmer while building something real: a desktop browser shell focused on privacy, security, and optional AI augmentation.

## Why this stack

Tauri's official documentation says Tauri is designed for small, fast, cross-platform applications, works with multiple frontend frameworks, and uses the system webview rather than bundling a browser engine. The official starter utility is `create-tauri-app`. citeturn4search68turn4search69turn4search70turn4search72

PyTauri's documentation says PyTauri provides Python bindings for Tauri, supports async Python, and recommends `create-pytauri-app` as the starting point for new projects. It also documents `pyInvoke` as the frontend/backend bridge and notes that `pytauri-wheel` can be used when you want to work in Python without manually writing Rust code. citeturn4search62turn4search63

## Project goals

- Build a **browser shell**, not a browser engine
- Keep the app **local-first** by default
- Keep the architecture **security-first**
- Make AI **optional**, not foundational
- Ensure the project remains usable even without paid AI tools

Microsoft Learn says GitHub Copilot Free in Visual Studio has limited access and monthly usage limits, so Copilot should be treated as a helper rather than a hard dependency for this project. citeturn4search86turn4search87

## Suggested repo layout

```text
ai-secure-browser/
  README.md
  docs/
    architecture.md
    security-rules.md
    rust-track.md
    python-track.md
  src/
  src-tauri/
```

## Reading order

1. [`docs/architecture.md`](docs/architecture.md)
2. [`docs/security-rules.md`](docs/security-rules.md)
3. Choose one track:
   - [`docs/rust-track.md`](docs/rust-track.md)
   - [`docs/python-track.md`](docs/python-track.md)

## First milestone

A local desktop app launches and shows a basic browser shell with:

- address bar
- navigation controls
- tab state
- safe URL validation
- backend/frontend communication

## Notes on AI

If you choose to add Gemini later, Google's official docs say you need an API key from Google AI Studio and can use the official `google-genai` SDK. The pricing docs also say a Free tier exists but is limited, so AI should remain optional. citeturn4search74turn4search75turn4search76turn4search78turn4search79

---
**Ingest notes (Claude-written, mutable):**
- Key claims: AI Secure Browser is built with Tauri 2 and TypeScript, supporting either a Rust or Python backend. Focuses on privacy, security, and optional AI.
- Wiki touches: [[ai-secure-browser]], [[tauri]], [[pytauri]], [[browser-shell]]
