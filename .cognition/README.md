# `.cognition/` — The Cognitive Layer

> The brain of the project. The cognitive layer is **independent of any programming language** and is the **first thing** any human or AI reads when joining the project.

## Purpose

The `.cognition/` directory stores **how the project thinks**. It captures:

* What the project is, why it exists, and what it must not become (identity).
* What the project is currently doing and why (planning, working memory).
* What the project has decided architecturally (architecture, ADRs, decision log).
* What the project has learned, fixed, and forgotten (history, lessons).
* What the project must always honor (invariants, business rules, glossary).

It is **not** a place for source code. Source code lives in `src/`.

## Relationship with AI

The cognitive layer is **specifically designed for LLM consumption**. Every document here is:

* Self-contained (a fresh AI can read it without external context).
* Structured with stable headings.
* Free of code unless the code is illustrative.
* Updated whenever the project itself changes.

Before any AI takes an action, it must read:

1. `identity/` — to understand the project.
2. `memory/working/current_context.md` — to know the current state.
3. `memory/permanent/` — to know the durable rules.
4. The relevant **role prompt** in `prompts/roles/`.
5. The relevant **task prompt** in `prompts/tasks/`.

After taking an action, the AI must:

* Update `memory/working/` if context shifted.
* Propose updates to `memory/permanent/` if a durable rule emerged.
* Append a session note to `memory/sessions/session_log.md`.

## Structure

```
.cognition/
├── README.md                # This file
├── identity/                # Project identity (mission, vision, principles, ...)
├── planner/                 # Current goal, iteration, backlog, vertical slice
├── architect/               # Domain model, system context, notes, decision queue
├── developer/               # Implementation plan, current task, constraints
├── reviewer/                # Reviews, technical debt, architecture review
├── curator/                 # Knowledge updates, glossary updates, lessons learned
├── researcher/              # Research notes, experiments
└── memory/
    ├── working/             # Short-lived, frequently replaced
    ├── permanent/           # Long-lived, monotonically growing
    ├── history/             # Decision log, project timeline
    ├── sessions/            # Session log (one entry per AI or human session)
    └── roadmap/             # Roadmap, milestones
```

## Lifecycle

| Area                | Lifecycle                                                                 |
|---------------------|---------------------------------------------------------------------------|
| `identity/`         | Near-immutable. Changes require an ADR (`identity-change`).               |
| `planner/`          | Replaced each iteration.                                                 |
| `architect/`        | Updated incrementally; `decision_queue.md` is short-lived.                |
| `developer/`        | Updated as work progresses; `current_task.md` is replaced frequently.    |
| `reviewer/`         | Append-only (review history).                                             |
| `curator/`          | Append-only (knowledge updates log); see `knowledge/` for promoted items. |
| `researcher/`       | Append-only until findings are promoted to `knowledge/` or an ADR.        |
| `memory/working/`   | Replaced frequently. Keep small and current.                              |
| `memory/permanent/` | Append-mostly. Reviewed periodically. Hard to change by design.           |
| `memory/history/`   | Append-only. The project's autobiography.                                 |
| `memory/sessions/`  | Append-only.                                                               |
| `memory/roadmap/`   | Updated at the end of each milestone.                                     |

## Expected Content by Area

* **`identity/`** — Mission, vision, principles, constraints, philosophy, values, non-goals, trade-offs.
* **`planner/`** — One goal, one iteration, one backlog, one next vertical slice.
* **`architect/`** — The current model of the domain and the system, plus the queue of pending decisions.
* **`developer/`** — How the current task will be implemented.
* **`reviewer/`** — What reviewers concluded; what technical debt has been logged.
* **`curator/`** — Knowledge change logs.
* **`researcher/`** — Findings, experiments, and unresolved questions.
* **`memory/working/`** — The here-and-now.
* **`memory/permanent/`** — The forever-now.
* **`memory/history/`** — What happened and why.
* **`memory/sessions/`** — Session-by-session journal.
* **`memory/roadmap/`** — Where we are going.

## Conventions

* All filenames are lowercase, hyphen-separated, and stable.
* Every file in `.cognition/` must be valid Markdown.
* Sections use stable headings so AI can navigate.
* Use front-matter (YAML or simple `# Title`) at the top.
* Cross-references use relative paths: `[ADR-0001](../architecture-decisions/0001-title.md)`.

## Where to Look When …

| When you need to …                                | Look here                                          |
|---------------------------------------------------|----------------------------------------------------|
| Understand the project                            | `identity/mission.md`, `identity/vision.md`        |
| Make a decision                                   | `identity/principles.md`, `identity/constraints.md` |
| Know what's being worked on                       | `planner/current_goal.md`, `memory/working/current_context.md` |
| Understand the domain                              | `architect/domain_model.md`                        |
| Understand the system                              | `architect/system_context.md`                      |
| Look up a term                                    | `memory/permanent/glossary.md`                     |
| Check an invariant                                | `memory/permanent/invariants.md`                   |
| Check a business rule                             | `memory/permanent/business_rules.md`               |
| See why a decision was made                       | `knowledge/architecture-decisions/`                |
| See who decided what, when                        | `memory/history/decision_log.md`                   |
| Resume a project after a long pause               | `memory/working/current_context.md` + `planner/` + `memory/permanent/` |

## What `.cognition/` is **Not**

* It is **not** a wiki. It is curated, structured, versioned, and owned.
* It is **not** a journal for individuals. It is a journal for the **project**.
* It is **not** source code. Do not place code here except short illustrative fragments.
* It is **not** throwaway scratch space. Scratch lives in `memory/working/` and is **replaced**, not accumulated.

---

> *If `.cognition/` disappears, the project has not lost its code — it has lost its mind.*