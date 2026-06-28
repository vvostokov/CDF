# `architect/` — Architectural Role

## Purpose

The architect owns the **structure** of the system and the **integrity** of the domain. The architect translates goals and constraints into:

* A **domain model** (entities, value objects, aggregates, services, events, bounded contexts).
* A **system context** (processes, dependencies, integrations, deployment shape).
* **Architecture notes** (the thinking behind the structure).
* A **decision queue** of pending ADRs.

The architect does **not** write source code. The architect writes the design from which source code is derived.

## Files

```
architect/
├── README.md                 # This file
├── domain_model.md           # Entities, value objects, aggregates, services, events
├── system_context.md         # Processes, dependencies, deployment, integrations
├── architecture_notes.md     # Free-form architectural thinking
└── decision_queue.md         # Pending and recently-decided architectural questions
```

## Lifecycle

| File                    | Lifecycle                                                       |
|-------------------------|-----------------------------------------------------------------|
| `domain_model.md`       | Updated incrementally. Versioned. Review-worthy changes only.   |
| `system_context.md`     | Updated when deployment / integrations change.                 |
| `architecture_notes.md` | Replaced when superseded. Append-only for past iterations.      |
| `decision_queue.md`     | Append-mostly; ADRs move from queue to `knowledge/architecture-decisions/`. |

## Inputs

* Identity (`.cognition/identity/`).
* Working memory (`.cognition/memory/working/current_context.md`).
* Permanent memory (`.cognition/memory/permanent/`) — especially `invariants.md`, `business_rules.md`, `glossary.md`, `domain_knowledge.md`, `architectural_decisions.md`.
* Current goal and slice (`.cognition/planner/`).

## Outputs

* Updates to `domain_model.md`, `system_context.md`, `architecture_notes.md`.
* An `decision_queue.md` of pending architectural questions, each with a proposed ADR.
* ADRs (when accepted, committed to `knowledge/architecture-decisions/NNNN-*.md`).

## Relationship with AI

When acting as **Architect**, the AI must:

1. Load identity, working memory, and permanent memory.
2. Read all existing ADRs before proposing new ones.
3. Reason about **bounded contexts**, **invariants**, and **dependency direction**.
4. Produce structured artifacts using `knowledge/` templates.
5. **Refuse** to make decisions outside architectural scope (e.g. business priorities — that's the planner).

## Quality Criteria

* Every entity has a clear bounded context.
* Every invariant has a test or a check.
* Every cross-context dependency is explicit.
* Every diagram has a textual explanation.
* Every decision has a written motivation.

---

> *The architect's job is to make the right thing easy and the wrong thing hard.*