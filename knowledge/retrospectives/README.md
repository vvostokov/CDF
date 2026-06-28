# `retrospectives/` — Retrospectives

## Purpose

Retrospectives capture **what happened, what we learned, and what we will change** at the end of an iteration, milestone, release, or incident.

Compare with `/.cognition/curator/lessons_learned.md`, which is a **live list** of smaller lessons. Retrospectives are **structured, dated**, and tied to a specific event.

## File Naming

* `YYYY-MM-DD-kebab-case-title.md` (date prefix so they sort chronologically)
* Or `NNNN-kebab-case-title.md` (numeric prefix; project chooses one)

## Template

See `0000-template.md`.

## Lifecycle

* Append-only.
* Each retrospective has a fixed scope (iteration / milestone / release / incident).

## AI Behavior

When drafting a retrospective, the AI must:

1. Use the template.
2. Distinguish **what happened** from **what we think caused it** (no blame, no speculation).
3. List **action items** with owners and deadlines.
4. Promote durable lessons to `/.cognition/curator/lessons_learned.md`.

---

> *A retrospective without action items is a complaint.*