# Testing Conventions

> Stable rules for testing. Enforced by tooling where possible.

## Levels

| Level          | Speed     | Location       | Purpose                          |
|----------------|-----------|----------------|----------------------------------|
| Unit           | very fast | `tests/unit/`  | One function / class              |
| Property-based | fast      | `tests/unit/`  | Invariants across random inputs   |
| Integration    | medium    | `tests/integration/` | A few components together   |
| Contract       | medium    | `tests/contract/`    | A context boundary          |
| End-to-end     | slow      | `tests/e2e/`   | Whole system                      |

## Naming

* File under test: `src/foo/Bar.ts` → test: `tests/unit/foo/Bar.test.ts`.
* Test name: describes behavior, not implementation (`returns 0 when input is empty`).

## Coverage

* Coverage target: **defined per project**. A bare minimum is recommended.
* Coverage is a **warning**, not a goal. Untested code that should be tested is technical debt.

## Determinism

* No real network.
* No real time (inject a clock).
* No real randomness (inject a generator).
* No real filesystem (inject an abstraction).

## Test Fixtures

* Fixtures live in `tests/fixtures/`.
* Fixtures are deterministic and reviewed.

## Anti-Patterns (Refuse)

* Tests that pass by side effect.
* Tests that depend on other tests.
* Tests with sleeps.

## Related

* `.cognition/memory/permanent/invariants.md`
* `prompts/tasks/testing.md`
* `workflows/engineering/testing.md`

---

> *A test is not "given enough rope to pass". It is a contract.*