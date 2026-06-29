---
title: PyTauri
type: concept
status: stable
created: 2026-06-10
updated: 2026-06-10
tags: [desktop-development, python, tauri, bindings]
---

# PyTauri

**Python bindings for the Tauri desktop application framework, allowing developers to write Tauri backends in Python.**

## Summary
PyTauri bridges the Tauri framework with Python, enabling developers to build desktop applications with modern web frontends and Python backends. It supports asynchronous execution, Pydantic model validation, and simple commands using pythonic annotations.

## Key points
- Provides Python bindings for Tauri and supports async Python workflows (from [[2026-06-10--ai-secure-browser-readme]], [[2026-06-10--ai-secure-browser-python-track]]).
- Recommends using `create-pytauri-app` as the starting point for new projects (from [[2026-06-10--ai-secure-browser-readme]]).
- Communication between the frontend and the Python backend is managed via `pyInvoke` (from [[2026-06-10--ai-secure-browser-readme]], [[2026-06-10--ai-secure-browser-architecture]]).
- Offers a pre-packaged workflow (`pytauri-wheel`) to build applications without writing Rust code manually (from [[2026-06-10--ai-secure-browser-readme]], [[2026-06-10--ai-secure-browser-python-track]]).

## Related
- [[tauri]] — the core Tauri framework.
- [[ai-secure-browser]] — browser shell utilizing PyTauri.

## Open questions
- None.

## Sources
- [[2026-06-10--ai-secure-browser-readme]]
- [[2026-06-10--ai-secure-browser-architecture]]
- [[2026-06-10--ai-secure-browser-python-track]]
