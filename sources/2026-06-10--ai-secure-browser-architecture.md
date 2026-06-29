---
title: AI Secure Browser - Architecture
source_url: local
source_type: note
captured: 2026-06-10
tags: [tauri, browser, architecture, design-principles, python, rust]
---

# Architecture

## High-level architecture

This project uses a **shared frontend** with two possible backend tracks:

- **Rust track**: TypeScript frontend ↔ Tauri `invoke` ↔ Rust commands
- **Python track**: TypeScript frontend ↔ PyTauri `pyInvoke` ↔ Python commands

Tauri's documentation says a Tauri project is typically made up of a JavaScript project and a Rust project under `src-tauri/`, and that the `capabilities/` folder is where capability files live. citeturn4search72

## Core design principles

### 1. Browser shell, not browser engine

We are building a desktop **browser shell** with our own UI, navigation, storage, and security model. We are not building a rendering engine.

### 2. Local-first

The application should work without any required server component. Cloud features are optional.

### 3. Security-first

Backend commands should be minimal, explicit, and reviewed before exposure to the frontend.

### 4. AI optional

AI features may be added later, but the browser shell must remain fully usable without them.

## Suggested folder structure

```text
.
├── README.md
├── docs/
│   ├── architecture.md
│   ├── security-rules.md
│   ├── rust-track.md
│   └── python-track.md
├── index.html
├── package.json
├── src/
│   ├── main.ts
│   ├── components/
│   ├── features/
│   │   ├── navigation/
│   │   ├── tabs/
│   │   ├── history/
│   │   ├── bookmarks/
│   │   └── settings/
│   ├── stores/
│   ├── utils/
│   └── types/
└── src-tauri/
    ├── Cargo.toml
    ├── build.rs
    ├── tauri.conf.json
    ├── capabilities/
    └── src/
```

This aligns with Tauri's documented structure of a frontend at the top level and a `src-tauri/` project containing `Cargo.toml`, `build.rs`, `tauri.conf.json`, icons, capabilities, and Rust source files. citeturn4search72

## Backend choice

## Rust backend

Choose Rust if you want:

- the most direct Tauri-native path
- fewer runtime layers
- maximum alignment with the core Tauri model

Tauri's docs say backend logic can be written in Rust and that JavaScript can call into Rust using `invoke`. citeturn4search70turn4search72

## Python backend

Choose Python if you want:

- Pydantic models
- async Python workflows
- easier AI experimentation
- a Python-first backend experience

PyTauri's docs say PyTauri provides Python bindings for Tauri, supports async Python, and exposes command calls through `pyInvoke`. citeturn4search63

## Phase 1 target capabilities

Phase 1 should include:

- one desktop window
- address bar
- back/forward/reload
- basic tab state
- safe URL validation
- local history/bookmarks later in the phase

## Suggested application models

```ts
export type Tab = {
  id: string
  title: string
  url: string
  isLoading: boolean
  canGoBack: boolean
  canGoForward: boolean
  securityState: 'unknown' | 'safe' | 'warning' | 'blocked'
  createdAt: string
  updatedAt: string
}

export type Bookmark = {
  id: string
  title: string
  url: string
  createdAt: string
}

export type HistoryEntry = {
  id: string
  title: string
  url: string
  visitedAt: string
  visitCount: number
}
```

These models are design proposals for this project, not direct quotes from the source material.

---
**Ingest notes (Claude-written, mutable):**
- Key claims: Shared frontend with Tauri Rust and PyTauri Python backend options. Core design principles are browser shell vs engine, local-first, security-first, and AI optional.
- Wiki touches: [[ai-secure-browser]], [[tauri]], [[pytauri]], [[browser-shell]]
