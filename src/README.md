# `src/` — Source Code

## Purpose

Source code lives here. The language, framework, and layout are **chosen by the project**, not by CDF.

CDF does **not** prescribe a stack. CDF prescribes **how the project thinks about the code**, not how the code is written.

## Structure

This directory is intentionally left for the project to populate. CDF recommends:

```
src/
├── README.md                # This file
├── bounded-contexts/        # One directory per bounded context (recommended)
│   ├── billing/
│   ├── identity/
│   └── ...
├── shared/                  # Cross-cutting code (logging, config, types)
└── main.*                   # Application entry point
```

The actual layout depends on the chosen language and framework.

## Conventions

* Source code is **language-specific**; conventions live in `docs/conventions/`.
* Each directory has a `README.md` explaining its purpose.
* Imports respect bounded-context boundaries (no leaking across).
* Public APIs are documented.

## Relationship with AI

When generating code, the AI must:

1. Use the developer role prompt (`prompts/roles/developer.md`).
2. Follow the implementation plan (`.cognition/developer/implementation_plan.md`).
3. Read the implementation constraints (`.cognition/developer/implementation_constraints.md`).
4. Follow the coding style (`docs/conventions/coding-style.md`).
5. Update the cognitive layer on architectural surprises (via ADR proposal).

## Lifecycle

* Code changes through PRs (per `workflows/engineering/code-review.md`).
* Code is documented as it is written.
* Code is tested as it is written.

---

> *Source code is the project's body. The cognitive layer is its mind. Both are necessary.*