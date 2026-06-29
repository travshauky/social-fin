---
title: Browser Shell
type: concept
status: stable
created: 2026-06-10
updated: 2026-06-10
tags: [architecture, browser, design-principles]
---

# Browser Shell

**An application architecture that implements a custom browser UI, security posture, and backend logic, but delegates actual HTML rendering to a pre-existing system engine.**

## Summary
A browser shell focuses on providing the shell around the web content—such as tabs, history, settings, and navigation controls—without rebuilding the underlying rendering engine (like WebKit or Blink). By decoupling the UI and orchestration from the rendering layer, developers can implement targeted security policies, custom features, and specialized backend APIs while maintaining lightweight applications.

## Key points
- Focuses on UI, navigation, storage, and security rules rather than building a rendering engine (from [[2026-06-10--ai-secure-browser-readme]], [[2026-06-10--ai-secure-browser-architecture]]).
- Leverages pre-existing OS-native webview runtimes (e.g. system webview in Tauri, Edge WebView2 on Windows) to minimize resource usage (from [[2026-06-10--ai-secure-browser-readme]]).
- Implements defensive design (e.g. default-deny, restricted CSPs, URL validation) to keep the desktop shell secure when displaying untrusted remote content (from [[2026-06-10--ai-secure-browser-security-rules]]).

## Related
- [[tauri]] — the framework enabling system webview communication.
- [[ai-secure-browser]] — a specific project utilizing the browser shell design.

## Open questions
- None.

## Sources
- [[2026-06-10--ai-secure-browser-readme]]
- [[2026-06-10--ai-secure-browser-architecture]]
- [[2026-06-10--ai-secure-browser-security-rules]]
