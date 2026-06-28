# `knowledge/` — Long-Lived Knowledge Artifacts

## Purpose

`knowledge/` stores **canonical, versioned, durable** knowledge. These are the documents a new contributor (human or AI) reads to understand what the project knows.

While `.cognition/memory/permanent/` holds **summary** knowledge (glossary, invariants, decisions index), `knowledge/` holds **detailed** knowledge: full ADRs, full bounded contexts, full feature specs, full retrospectives.

## Structure

```
knowledge/
├── README.md                          # This file
├── architecture-decisions/            # ADRs (NNNN-title.md)
│   └── README.md
├── domain/                            # Domain knowledge artifacts
│   ├── bounded-contexts/              # One file per bounded context
│   ├── domain-model.md                # Full domain model
│   ├── glossary.md                    # Full glossary (vs. summary in .cognition/)
│   └── README.md
├── features/                          # Feature specifications
│   └── README.md
├── risks/                             # Risk analyses
│   └── README.md
├── retrospectives/                    # Post-mortems, iteration retros, incident reviews
│   └── README.md
└── business-rules/                    # Business rule specifications
    └── README.md
```

## Templates Available

* **ADR** — `architecture-decisions/0000-template.md`
* **Bounded Context** — `domain/bounded-contexts/0000-template.md`
* **Feature Specification** — `features/0000-template.md`
* **Risk Analysis** — `risks/0000-template.md`
* **Retrospective** — `retrospectives/0000-template.md`
* **Business Rule** — `business-rules/0000-template.md`

The same templates exist as `.md` files alongside this README in each subdirectory.

## Lifecycle

| Subdirectory                | Lifecycle                                                  |
|-----------------------------|------------------------------------------------------------|
| `architecture-decisions/`   | Append-only. New ADRs get the next available number.       |
| `domain/`                   | Updated as the model evolves. Versions retained in git.    |
| `features/`                 | Append-only. Each feature gets a number.                   |
| `risks/`                    | Append-mostly. Risks move from `open` to `mitigated` to `accepted`. |
| `retrospectives/`           | Append-only. Each retrospective gets a number.             |
| `business-rules/`           | Updated as business changes; old versions in git history.  |

## Conventions

* Files use kebab-case (`bounded-context-billing.md`).
* Numbered prefixes (`0001-`, `0002-`) preserve chronological order.
* Front-matter (title, status, date, owner) is required.
* Cross-references use relative paths.

## AI Behavior

When generating knowledge artifacts, the AI must:

1. Use the appropriate template from `knowledge/.../0000-template.md`.
2. Number sequentially with zero-padding.
3. Link back to relevant `.cognition/` artifacts.
4. Propose the artifact as a **draft**, not as final — humans curate.

---

> *Knowledge lives here because it deserves its own room.*