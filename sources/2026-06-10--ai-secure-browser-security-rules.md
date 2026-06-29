---
title: AI Secure Browser - Security Rules
source_url: local
source_type: note
captured: 2026-06-10
tags: [tauri, browser, security, permissions, csp]
---

# Security Rules

## Security posture

The browser shell treats **remote content as untrusted** and keeps privileged backend logic behind a minimal command surface.

Tauri's official docs describe a trust boundary between code running in the webview and privileged code in the backend, with access controlled via capabilities and permissions. citeturn2search56turn2search54turn2search57

## Rules

### 1. Default deny

Do not expose backend commands to the frontend unless there is a clear reason.

Tauri's project structure docs say commands must be allowed via capability configuration to be used from JavaScript. citeturn4search72

### 2. Keep capabilities narrow

Use capability files to scope access to specific windows or contexts.

Tauri's capability documentation says capabilities define which permissions are granted to which windows or webviews, and warns that windows included in multiple capabilities effectively merge permissions. citeturn2search54

### 3. Keep permissions explicit

Only allow the commands needed for:

- navigation
- tab management
- local settings
- local history/bookmarks (when implemented)

Tauri's permissions documentation says permissions describe explicit privileges of commands and may allow or deny commands and define scopes. citeturn2search57turn2search59

### 4. Use a restrictive CSP for the app UI

Avoid remote scripts and keep the frontend self-contained.

Tauri's CSP documentation says CSP can reduce the impact of web-based vulnerabilities such as XSS and explicitly cautions against loading remote content such as CDN-hosted scripts because they introduce an attack vector. cite2search55

### 5. Do not make AI foundational

If AI is used, it must be optional and behind explicit settings or feature flags.

Google's Gemini docs say Gemini requires an API key, while the pricing docs say the Free tier is limited. This makes AI suitable as an optional augmentation, not a required part of the browser shell. citeturn4search74turn4search76turn4search79

### 6. Treat external pages as untrusted

This is a general rule for this project.

Electron's official security documentation explicitly warns that displaying arbitrary content from untrusted sources is a severe security risk in Electron. While this project is based on Tauri rather than Electron, the same defensive principle is useful here. citeturn2search60

## Practical checks before merging code

- Does this command really need to exist?
- Does the frontend truly need this capability?
- Can the feature work without cloud AI?
- Are we introducing a remote dependency into the critical path?
- Have we documented the new attack surface?

## Security checklist for Phase 1

- [ ] Restrictive capability set defined
- [ ] No unnecessary filesystem access
- [ ] No unnecessary shell/process access
- [ ] URL validation path documented
- [ ] Remote scripts avoided in the app UI
- [ ] AI integrations disabled by default

---
**Ingest notes (Claude-written, mutable):**
- Key claims: Core security posture treats remote content as untrusted, using default-deny command exposure, narrow capabilities, explicit permissions, restrictive CSP, and optional AI.
- Wiki touches: [[ai-secure-browser]], [[tauri]], [[browser-shell]]
