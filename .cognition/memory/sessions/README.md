# `memory/sessions/` — Session Log

## Purpose

One entry per session — a session being a single continuous unit of work by a human or AI. Sessions are short-lived but **logged forever** to enable reconstruction of how work happened.

## Files

```
sessions/
├── README.md
└── session_log.md
```

## What a Session Entry Looks Like

Each entry has:

* **Session ID** — YYYY-MM-DD-HH-MM (or a stable slug).
* **Actor** — role (planner / architect / developer / reviewer / curator / researcher / human / AI / hybrid).
* **Goal** — what the session tried to accomplish.
* **Outcome** — what actually happened.
* **Decisions made** — links to ADRs / decision log entries.
* **Artifacts touched** — file paths.
* **Memory updates** — what was promoted to permanent memory.
* **Lessons learned** — anything new.
* **Next step** — what the next session should pick up.

## How to Add an Entry

1. Append at the top of the log.
2. Use stable IDs (filename-safe).
3. Be honest about outcome — partial wins count.

## When Sessions Become Many

If session_log.md becomes hard to navigate, **do not split** by year. Instead, use clear IDs and let search tools do the work.

---

> *Sessions are how the project remembers how it actually got built.*