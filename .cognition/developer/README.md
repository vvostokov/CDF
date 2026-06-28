# `developer/` — Development Role

## Purpose

The developer owns the **how** of getting work done: implementation plan, current task, and implementation constraints.

The developer translates the architect's design into code, tests, and documentation. The developer also enforces the constraints that come from the architect and identity.

The developer does **not** decide what to build (planner) or whether the design is sound (architect / reviewer).

## Files

```
developer/
├── README.md                       # This file
├── implementation_plan.md          # The plan for the current slice / feature
├── current_task.md                 # The smallest unit of work in progress right now
└── implementation_constraints.md   # Hard and soft implementation rules
```

## Lifecycle

| File                              | Lifecycle                                          |
|-----------------------------------|----------------------------------------------------|
| `implementation_plan.md`          | Created per slice; updated as work progresses; archived when done. |
| `current_task.md`                 | Replaced frequently (every few hours of work).    |
| `implementation_constraints.md`   | Rarely changed; changes via PR with rationale.     |

## Inputs

* `planner/next_vertical_slice.md` — what we're building.
* `architect/domain_model.md` — what it looks like in the domain.
* `architect/system_context.md` — what it looks like at runtime.
* `architect/architecture_notes.md` — how the architect thinks about it.
* `memory/permanent/invariants.md` and `business_rules.md` — what must never break.
* `prompts/tasks/implementation.md` — how the developer thinks.
* `workflows/engineering/implementation.md` — the Definition of Done.

## Outputs

* Source code (`src/`).
* Tests (`tests/`).
* Implementation plan (`implementation_plan.md`).
* Updates to `current_task.md` as the work progresses.
* Proposed ADR if an architectural surprise emerges.

## Relationship with AI

When acting as **Developer**, the AI must:

1. Load the implementation plan, the relevant architecture artifacts, and the implementation constraints.
2. Work in **small, verifiable increments** (write a test, then make it pass).
3. Update `current_task.md` at the start and end of each session.
4. **Refuse** to make architectural changes silently — propose an ADR instead.

## Quality Criteria

* The plan is **executable**: someone else could follow it.
* The current task is **small** (single session).
* The constraints are **enforced**: a CI check, a linter, or a code-review convention.
* The work has **tests** for each non-trivial path.

---

> *Developers turn architecture into a running system, one verifiable step at a time.*