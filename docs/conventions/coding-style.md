# Coding Style

> Stable coding-style rules for the project. Enforced by linters / formatters where possible.

## Languages

<!-- Project-specific. List the primary languages and link each to its style guide. -->

* **Primary:** [language] — [link to style guide]
* **Secondary:** [language] — [link to style guide]

## Naming

* **Files:** lowercase, hyphen-separated (`order-repository.ts`).
* **Classes / types:** PascalCase.
* **Functions / methods:** camelCase (or snake_case — project decision).
* **Constants:** UPPER_SNAKE_CASE for top-level immutable values.
* **Bounded contexts:** match their directory names.
* **ADRs:** `NNNN-kebab-case-title.md`.
* **Tests:** mirror the file under test, suffixed with `.test` or `_test`.

## File Layout

* **One type per file** when the language supports it.
* **Imports:** organized by external → internal → relative.
* **Exports:** explicit, minimal.

## Formatting

* Enforced by [formatter name] — see `docs/conventions/tooling.md`.
* Run before commit (or rely on pre-commit hooks).

## Comments

* **Why, not what.**
* Public APIs are documented.
* Internal comments only where the code is non-obvious.

## Errors

* Errors carry enough context to debug.
* Error types are part of the public API where they cross boundaries.

## Related

* `docs/conventions/testing.md`
* `docs/conventions/tooling.md`
* `.cognition/developer/implementation_constraints.md`

---

> *Style is not art. Style is agreement.*