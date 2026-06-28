# `planner/` — Planning Role

## Purpose

The planner owns the **what** and **when**. It decides which goal the project pursues next, what the current iteration covers, what is in the backlog, and which vertical slice should be tackled first.

The planner does **not** decide **how**. Architecture is the architect's job. Implementation is the developer's job.

## Files

```
planner/
├── README.md                  # This file
├── current_goal.md            # The single most important goal right now
├── current_iteration.md       # The iteration currently in progress
├── backlog.md                 # Ordered list of everything not yet done
└── next_vertical_slice.md     # The smallest end-to-end slice to deliver next
```

## Lifecycle

| File                    | Lifecycle                                                  |
|-------------------------|------------------------------------------------------------|
| `current_goal.md`       | Replaced only when the current goal is achieved or retired. |
| `current_iteration.md`  | Replaced at the end of each iteration.                     |
| `backlog.md`            | Updated continuously. Append-mostly, ordered.              |
| `next_vertical_slice.md`| Replaced when the slice is completed or rescoped.          |

## Inputs

* Project identity (`.cognition/identity/`).
* Permanent memory (`.cognition/memory/permanent/`).
* Working memory (`.cognition/memory/working/current_context.md`).
* Roadmap (`.cognition/memory/roadmap/roadmap.md`).
* Lessons learned (`.cognition/curator/lessons_learned.md`).

## Outputs

* A clear `current_goal.md` that the rest of the project can read.
* A `backlog.md` ordered by value × risk.
* A `next_vertical_slice.md` small enough to deliver in days, not weeks.

## Relationship with AI

When acting as **Planner**, the AI must:

1. Read identity, working memory, and permanent memory first.
2. Read lessons learned for context on prior iterations.
3. Propose a goal, iteration, and slice **without** writing code or ADRs.
4. Cite the inputs that motivated the proposal.
5. Update `current_iteration.md` at the start of each iteration.

## Quality Criteria

* The current goal is **one** goal, not a list.
* The backlog is **ordered**, with the highest-value items first.
* The next vertical slice is **end-to-end** (cuts through the architecture) and **small** (deliverable in days).
* Every item has a clear Definition of Done.

---

> *The planner's job is to make the next decision obvious.*