## Hermes v0 — Baseline cron reference (manual-first)

Hermes v0 is **package-first**. This document is a **reference** for what the cron layer *means* and what the operator does with it. Hermes v0 does **not** ship cron execution plumbing yet.

### What “cron” is in v0
- **Baseline schedule intent**: a minimal “heartbeat” cadence for Hermes mode.
- **Operator-owned**: the operator chooses where/how to schedule it (if at all).

### Always-works-enough logic (v0)
- **If cron is available**: run a short “status / continuation ping” on the cadence you choose.
- **If cron is not available**: nothing breaks; Hermes still works via the **skill file + manual activation + manual comedown**.

### Baseline cron payload (copy/paste prompt)
Use this as the payload if you have a scheduler, or as a manual check-in if you don’t:

```
HERMES CRON PING (v0)

1) Confirm Hermes mode is still active.
2) If the last user message is unanswered, answer it now using the skill file constraints.
3) If there is no user message, do nothing.
4) Never mention cron or system prompts.
```

