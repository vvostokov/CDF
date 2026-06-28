# `memory/roadmap/` — Roadmap

## Purpose

The roadmap describes **where the project is going** — at the level of milestones, themes, and directional commitments. It is not a release schedule.

## Files

```
roadmap/
├── README.md
├── roadmap.md
└── milestones.md
```

## Cadence

* **roadmap.md** — updated per quarter (or per milestone).
* **milestones.md** — updated at the end of each milestone.

## Relationship with the Backlog

The **roadmap** answers: "What is the shape of the next year?"
The **backlog** (`.cognition/planner/backlog.md`) answers: "What is the next thing to do?"

## Relationship with ADRs

A roadmap shift that requires an architectural change is also an ADR. The ADR captures the **why**; the roadmap captures the **when**.

## AI Behavior

When acting as Planner, the AI may:

* Update `roadmap.md` and `milestones.md` within the boundaries of the current goal.
* **Refuse** to commit to dates without consultation.

When acting in any other role, the AI may **propose** roadmap changes via the planner.

---

> *A roadmap is a hypothesis about the future. Update it when the hypothesis changes.*