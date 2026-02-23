---
"agent-browser": minor
---

- Added `keyboard` command for raw keyboard input -- type with real keystrokes, insert text, and press shortcuts at the currently focused element without needing a selector.
- Added `--color-scheme` flag and `AGENT_BROWSER_COLOR_SCHEME` env var for persistent dark/light mode preference across browser sessions.
- Fixed IPC EAGAIN errors (os error 35/11) by adding backpressure-aware socket writes, command serialization, and lowering the default Playwright timeout to 25s (configurable via `AGENT_BROWSER_DEFAULT_TIMEOUT`).
- Fixed remote debugging (CDP) reconnection.
- Fixed state load failing when no browser is running.
- Fixed `--annotate` flag warning appearing when not explicitly passed via CLI.
