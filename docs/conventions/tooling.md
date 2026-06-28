# Tooling

> Which tools the project uses, at which versions, and why.

## Primary Stack

<!-- Project-specific. Replace with the chosen stack. -->

* **Language:** [e.g. TypeScript]
* **Runtime:** [e.g. Node.js 22 LTS]
* **Build:** [e.g. pnpm + tsc]
* **Lint:** [e.g. ESLint + Prettier]
* **Test:** [e.g. Vitest + Playwright]
* **CI:** [e.g. GitHub Actions]

## Versions

* Versions are pinned (exact, not ranges) for reproducibility.
* Upgrade cadence: per quarter (or as needed).

## Pre-commit

* A pre-commit hook runs the formatter and the linter.
* A separate hook (optional) runs unit tests.

## CI

* Lint
* Unit tests
* Integration tests
* Build
* Optional: smoke deploy

## How to Upgrade

1. Open an ADR if the upgrade is non-trivial.
2. Update `docs/conventions/tooling.md`.
3. Update CI.
4. Update developer docs.

## Related

* `.cognition/developer/implementation_constraints.md`
* `docs/conventions/coding-style.md`

---

> *Tooling is what keeps the project reproducible.*