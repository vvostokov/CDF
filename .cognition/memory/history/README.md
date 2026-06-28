# `memory/history/` — History

## Purpose

History is the project's **autobiography**. It is append-only. Nothing is deleted — only annotated.

## Files

```
history/
├── README.md                # This file
├── decision_log.md          # Chronological log of significant decisions
└── project_timeline.md      # Chronological narrative of project events
```

## What Goes Here

* Major decisions (with link to ADR when applicable).
* Releases (with link to release notes).
* Significant incidents and their resolutions.
* Personnel / scope / mission changes.
* Architectural shifts.

## What Does **Not** Go Here

* Routine code changes (use git log).
* Session-level details (use `memory/sessions/`).
* Speculation or opinion.

## Editing Discipline

* New entries go to the **top**.
* Old entries are **never** edited except to fix typos or link to a follow-up.
* Each entry has a date, an actor (human, role, or "automated"), and a one-paragraph description.

## AI Behavior

When recording a decision in history, the AI must:

1. Reference the source (ADR, issue, discussion).
2. Use neutral, factual language.
3. State the decision, the context, and the consequence.

---

> *History is not a place for narrative. It is a place for facts.*