# `curator/` — Knowledge Curator Role

## Purpose

The curator maintains the **cognitive layer's quality**. The curator:

* Promotes working knowledge into permanent knowledge.
* Updates the glossary as new terms appear.
* Captures lessons learned after every iteration / incident.
* Ensures `.cognition/` stays consistent and well-organized.

The curator is the **gardener** of the cognitive layer. The curator trims, prunes, propagates, and composts knowledge.

## Files

```
curator/
├── README.md                 # This file
├── knowledge_updates.md      # Log of knowledge updates (append-only)
├── glossary_updates.md       # Proposed glossary changes (queue)
└── lessons_learned.md        # Lessons captured per iteration / event
```

## Lifecycle

| File                    | Lifecycle                                            |
|-------------------------|------------------------------------------------------|
| `knowledge_updates.md`  | Append-only log. Each entry links to the change.     |
| `glossary_updates.md`   | Replaced once merged into `memory/permanent/glossary.md`. |
| `lessons_learned.md`    | Append-mostly; reorganized periodically.            |

## Inputs

* All `.cognition/` updates from other roles.
* Permanent memory (`.cognition/memory/permanent/`) — to keep it tidy.
* Roadmap / milestones (`.cognition/memory/roadmap/`) — to align knowledge with phases.

## Outputs

* Updated permanent memory (glossary, invariants, business rules, domain knowledge, ADRs).
* `knowledge_updates.md` entries logging every change.
* Reorganized `.cognition/` when structure drifts.

## Relationship with AI

When acting as **Curator**, the AI must:

1. Read all recent updates in `.cognition/`.
2. Identify knowledge that is **durable** and should be promoted.
3. Identify knowledge that is **stale** and should be retired.
4. Propose glossary updates **without rewriting the glossary** unless explicitly asked.
5. **Refuse** to alter identity documents; route changes to an ADR.

## Quality Criteria

* Every entry in `knowledge_updates.md` has a date, author, and link.
* The glossary has definitions for every domain term in the model.
* Lessons learned entries are **specific** and **actionable**.
* Permanent memory does not duplicate working memory.

---

> *The curator's job is to ensure the project's brain ages well.*