# `domain/` — Domain Knowledge

## Purpose

This directory holds **detailed** domain knowledge: the full domain model, full bounded contexts, the canonical glossary, and any long-form domain explanations.

Compare with `/.cognition/architect/domain_model.md`, which holds the **summary** that everyone reads first.

## Files

```
domain/
├── README.md                  # This file
├── domain-model.md            # Full domain model (canonical)
├── glossary.md                # Full glossary (canonical)
└── bounded-contexts/
    ├── README.md
    ├── 0000-template.md       # Template for a bounded context doc
    └── NNNN-context-name.md   # One file per bounded context
```

## Lifecycle

* The full domain model is updated when the summary model is insufficient.
* The full glossary is updated when the summary glossary is insufficient.
* Bounded contexts are added as the system grows.

## AI Behavior

When writing bounded-context docs, the AI must:

1. Reference the relevant ADRs.
2. Reference the relevant invariants and business rules.
3. Use the template at `bounded-contexts/0000-template.md`.

---

> *The domain is what the system serves. Everything else is plumbing.*