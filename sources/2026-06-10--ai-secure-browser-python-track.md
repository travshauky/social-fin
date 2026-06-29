---
title: AI Secure Browser - Python Track
source_url: local
source_type: note
captured: 2026-06-10
tags: [tauri, browser, python, pytauri, project-setup]
---

# Python Track

## Overview

Choose this track if you want a Python-first backend using **PyTauri**.

PyTauri's documentation says PyTauri provides Python bindings for Tauri, supports async Python, and exposes frontend/backend calls with `pyInvoke`. It also says `create-pytauri-app` is the recommended way to start a new project. citeturn4search62turn4search63

## Week 1 — Setup and scaffolding

### Install prerequisites

Install Tauri prerequisites for your operating system. Tauri's prerequisites page says Rust and system dependencies are required for Tauri development. citeturn4search73

Install Python and `uv`. PyTauri's tutorial documents a `uv`-based workflow and shows Python living under `src-tauri/python/...` for the Python backend path. citeturn4search67

### Scaffold the project

Use the recommended PyTauri scaffolding command:

```bash
uvx copier copy https://github.com/pytauri/create-pytauri-app .
```

PyTauri's docs explicitly say `create-pytauri-app` is the recommended way to start a new PyTauri project. citeturn4search62

### Python-first note

PyTauri's homepage says you can also choose `pytauri-wheel` if you want a workflow where everything can be done in Python without manually writing Rust code. citeturn4search63

## Week 2 — Browser shell core

### Build the frontend shell

Create:

- address bar
- navigation buttons
- tab strip
- page/status area

### Add Python commands

PyTauri's docs show a Python command style using `@commands.command()` and frontend calls using `pyInvoke`. citeturn4search63

Suggested Python commands:

- `validate_url`
- `normalise_url`
- `open_tab`
- `close_tab`
- `list_tabs`

### Use models for state

Python is a good fit for tab models, validation models, and optional AI logic.

## Week 3 — Optional AI

Python is the more natural route if you want to experiment with:

- page summarisation
- structured outputs
- content extraction pipelines
- model orchestration

If you add Gemini, Google's official docs say you need an API key from Google AI Studio and can use the `google-genai` SDK quickstart patterns. Google's pricing docs say the Free tier exists but is limited. citeturn4search74turn4search75turn4search76turn4search78turn4search79

## Week 4 — Packaging and standalone build

PyTauri's standalone build guide says PyTauri can be compiled into a standalone executable and documents bundling an embedded Python distribution under `src-tauri/pyembed`. It also documents configuring Tauri bundle resources so the embedded Python runtime is packaged with the app. citeturn4search80

## Minimal milestone checklist

- [ ] App launches locally
- [ ] Address bar accepts input
- [ ] URL validation runs through Python
- [ ] `pyInvoke` path is working
- [ ] Optional AI remains behind settings
- [ ] Packaging plan for embedded Python is documented

---
**Ingest notes (Claude-written, mutable):**
- Key claims: Python track uses PyTauri with `create-pytauri-app` scaffolding, using `uv` for package management and embedding Python using `src-tauri/pyembed`.
- Wiki touches: [[ai-secure-browser]], [[tauri]], [[pytauri]], [[browser-shell]]
