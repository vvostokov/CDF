# `tests/` — Tests

## Purpose

Tests live here. Like `src/`, the layout is **chosen by the project**.

CDF recommends a layout that **mirrors the bounded contexts in `src/`**:

```
tests/
├── README.md                # This file
├── unit/
│   ├── billing/
│   ├── identity/
│   └── ...
├── integration/
├── contract/
├── e2e/
├── fixtures/
└── helpers/
```

## Conventions

* Tests are deterministic, fast, and focused.
* Each test asserts **one** concept.
* Coverage targets are defined per project in `docs/conventions/testing.md`.
* Test names describe **behavior**, not implementation.
* New invariants require new tests (per `workflows/engineering/testing.md`).

## Relationship with AI

When generating tests, the AI must:

1. Use the testing task prompt (`prompts/tasks/testing.md`).
2. Follow the testing conventions (`docs/conventions/testing.md`).
3. Cover happy path, alt path, edge cases, failure modes.
4. Add property-based tests for invariants where possible.

## Lifecycle

* Tests are written **with** the code (RED-GREEN-REFACTOR).
* Tests are reviewed as part of PR review.
* Tests are refactored with the code.

---

> *Tests are how the project proves its claims.*