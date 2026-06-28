# `memory/working/` — Working Memory

## Purpose

Working memory holds the **here-and-now** of the project. It is small, current, and frequently replaced.

If working memory grows past a few pages per file, knowledge is leaking from permanent memory into working memory. Promote it.

## Files

```
working/
├── README.md                  # This file
├── current_context.md         # What is happening right now
├── active_questions.md        # Questions currently in flight
└── temporary_notes.md         # Scratchpad, replaced often
```

## Lifecycle

| File                    | Lifecycle                                                  |
|-------------------------|------------------------------------------------------------|
| `current_context.md`    | Replaced whenever context materially shifts. Reviewed at end of each iteration. |
| `active_questions.md`   | Updated continuously; resolved questions move out.         |
| `temporary_notes.md`    | Replaced at end of each session or iteration.              |

## When to Update

| File                    | Update trigger                                             |
|-------------------------|------------------------------------------------------------|
| `current_context.md`    | Iteration boundary, blocker encountered, scope changed, role handoff. |
| `active_questions.md`   | New question, question answered, question promoted to ADR. |
| `temporary_notes.md`    | When you need to think out loud.                           |

## When to Promote (Out of Working Memory)

* A fact becomes **durable** (will be true for years) → promote to `permanent/`.
* A decision is **made** → promote to `history/decision_log.md` and (if architectural) to `knowledge/architecture-decisions/`.
* A **lesson** is learned → promote to `curator/lessons_learned.md`.
* A **research finding** is conclusive → promote to `architect/architecture_notes.md` or an ADR.

## AI Behavior

When acting in any role, the AI should:

1. Read `current_context.md` at the start of every session.
2. Update `current_context.md` before ending a session.
3. **Refuse** to let working memory become a dumping ground.

## Cold Start

If `current_context.md` is empty or out-of-date, treat the project as cold-started and read permanent memory first.

---

> *Working memory is a whiteboard. Permanent memory is the library.*