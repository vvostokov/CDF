# `memory/permanent/` — Permanent Memory

## Purpose

Permanent memory holds the **durable** knowledge of the project: the things that should still be true in five years.

Permanent memory is hard to change on purpose. Changes happen through curator activity, ADRs, and explicit review.

## Files

```
permanent/
├── README.md                     # This file
├── glossary.md                   # Domain terms with stable definitions
├── invariants.md                 # Things that must always be true
├── business_rules.md             # Business logic encoded as rules
├── architectural_decisions.md    # Summary index of architectural decisions (with links to ADRs)
└── domain_knowledge.md           # Stable facts about the domain the system models
```

## Lifecycle

| File                          | Lifecycle                                          |
|-------------------------------|----------------------------------------------------|
| `glossary.md`                 | Updated via curator process. Rare additions/removals. |
| `invariants.md`               | Updated via ADR when a new invariant is introduced. |
| `business_rules.md`           | Updated as rules are added / changed; tied to ADRs / features. |
| `architectural_decisions.md`  | Updated whenever a new ADR is accepted.             |
| `domain_knowledge.md`         | Updated as the system's understanding of its domain grows. |

## Editing Discipline

* **Glossary** — additions, edits, removals flow through `.cognition/curator/glossary_updates.md`.
* **Invariants** — every new invariant must be tied to a test or a check. An invariant without enforcement is a wish.
* **Business rules** — every rule has an owner (usually a bounded context) and a status.
* **Architectural decisions** — this is an **index**; the full text lives in `knowledge/architecture-decisions/NNNN-*.md`.
* **Domain knowledge** — entries are dated; old entries are not deleted but marked `retired`.

## Invariant Enforcement

Every invariant should be enforced by at least one of:

* A unit test
* An integration test
* A property-based test
* A static check (type, linter, formal)
* A contract test at a context boundary
* A run-time assertion (only when necessary)

If an invariant has **no** enforcement, mark it as `unenforced` and link to a follow-up issue.

## AI Behavior

When acting in any role, the AI must:

1. Read the relevant permanent-memory file before producing artifacts.
2. **Refuse** to silently contradict any invariant, glossary term, business rule, or accepted ADR.
3. When a contradiction seems necessary, **propose an ADR** rather than violate the rule.

---

> *Permanent memory is the project's spine. Bend it only with ceremony.*