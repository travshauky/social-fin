---
title: Tauri
type: concept
status: stable
created: 2026-06-10
updated: 2026-06-10
tags: [desktop-development, rust, typescript, framework]
---

# Tauri

**A framework for building tiny, fast, secure desktop and mobile applications using web technologies for the frontend and Rust for the backend.**

## Summary
Tauri is a modern desktop app framework that allows developers to design user interfaces using HTML, CSS, and JavaScript, while binding system operations to a Rust backend. Unlike Electron, Tauri uses the operating system's native web view engine instead of bundling Chromium, significantly reducing executable sizes and memory footprint.

## Key points
- Designed for small, fast, cross-platform applications using system webviews (from [[2026-06-10--ai-secure-browser-readme]]).
- Implements a strict security model with a trust boundary between the webview and backend code, controlled via capabilities and permissions (from [[2026-06-10--ai-secure-browser-security-rules]]).
- Supports backend commands invoked from JavaScript through `invoke` (from [[2026-06-10--ai-secure-browser-architecture]]).
- Project structure separates the frontend UI and the backend Rust code (in `src-tauri/`) (from [[2026-06-10--ai-secure-browser-architecture]]).

## Related
- [[pytauri]] — Python bindings for Tauri.
- [[ai-secure-browser]] — browser shell built using Tauri.

## Open questions
- None.

## Sources
- [[2026-06-10--ai-secure-browser-readme]]
- [[2026-06-10--ai-secure-browser-architecture]]
- [[2026-06-10--ai-secure-browser-security-rules]]
- [[2026-06-10--ai-secure-browser-rust-track]]
