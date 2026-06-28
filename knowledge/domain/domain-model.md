# Domain Model (Full)

> The full, canonical domain model. Detailed version of `/.cognition/architect/domain_model.md`.

This file is intended for **deep reading**. The summary in `.cognition/` is for orientation; the file here is for understanding.

## Sections

1. **Strategic Overview** — bounded context map, classification, strategic patterns.
2. **Per-Context Detail** — for each context, a full description of aggregates, entities, value objects, services, events, ACLs.
3. **Cross-Context Flows** — sequence diagrams or step-by-step narratives for major flows.
4. **Cross-Context Invariants** — invariants that span multiple contexts.
5. **Glossary** — pointer to `glossary.md`.
6. **Open Modeling Questions** — unresolved modeling problems.

## How to Update

* Update `.cognition/architect/domain_model.md` (summary) and this file (detail) together.
* Every model change is linked to an ADR.
* Every new entity / aggregate has at least one test.

---

> *The full model is long. That is fine. It is meant to be referenced, not memorized.*