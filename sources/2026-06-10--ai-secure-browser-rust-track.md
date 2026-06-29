---
title: AI Secure Browser - Rust Track
source_url: local
source_type: note
captured: 2026-06-10
tags: [tauri, browser, rust, project-setup]
---

# Rust Track

## Overview

Choose this track if you want the cleanest Tauri-native setup and a backend written in Rust.

Tauri's official docs say `create-tauri-app` is the recommended way to create a new project and that JavaScript can communicate with Rust using `invoke`. citeturn4search68turn4search70turn4search72

## Week 1 — Setup and scaffolding

### Install prerequisites

Install Tauri prerequisites for your operating system. Tauri's prerequisites page says development requires Rust plus system dependencies, and on Windows specifically requires Microsoft C++ Build Tools and Microsoft Edge WebView2. citeturn4search73

### Scaffold the project

Use an official Tauri starter:

```bash
npm create tauri-app@latest
```

Tauri's docs say `create-tauri-app` will prompt for project name, frontend language, package manager, and UI template. The docs recommend starting with **Vanilla** if you are unsure. citeturn4search68

### Recommended choices

- Frontend language: TypeScript / JavaScript
- Package manager: pnpm
- UI template: Vanilla
- UI flavour: TypeScript

These choices mirror the example path shown in Tauri's official create-project documentation. citeturn4search68

## Week 2 — Browser shell core

### Build the frontend shell

Create:

- address bar
- back button
- forward button
- reload button
- new tab button
- tab strip
- page/status area

This UI plan is a project design choice.

### Add Rust commands

Suggested Rust commands:

- `validate_url`
- `normalise_url`
- `open_tab`
- `close_tab`
- `list_tabs`

Tauri's docs say the Rust backend lives in `src-tauri/` and that JavaScript can call Rust using `invoke`. citeturn4search70turn4search72

## Week 3 — Optional AI

Keep AI optional. If you add Gemini, Google's docs say you need an API key from Google AI Studio and can use the official SDK examples. Google's pricing docs say the Free tier exists but is limited. citeturn4search74turn4search75turn4search76turn4search78turn4search79

In the Rust track, use Rust primarily for orchestration and keep API usage behind a feature flag or settings toggle.

## Week 4 — Packaging and hardening

Review the command surface and capability configuration before packaging. Tauri's project structure docs say capabilities are configured under `src-tauri/capabilities/`. citeturn4search72

## Minimal milestone checklist

- [ ] App launches locally
- [ ] Address bar accepts input
- [ ] URL validation runs through Rust
- [ ] Tab state exists in the frontend
- [ ] Backend command surface is documented
- [ ] Capability configuration is minimal

---
**Ingest notes (Claude-written, mutable):**
- Key claims: Rust track uses official Tauri native setup with `create-tauri-app` and `invoke` backend communications.
- Wiki touches: [[ai-secure-browser]], [[tauri]], [[browser-shell]]
