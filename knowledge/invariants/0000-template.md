# Invariant — [Statement]

* **Invariant ID:** INV-NNN
* **Status:** `enforced` | `unenforced` | `retired`
* **Owner:**
* **Bounded context:**
* **Created:** YYYY-MM-DD
* **Last verified:** YYYY-MM-DD
* **Source:** [ADR / domain fact / business rule]

## Statement

<!-- A single sentence in plain English. -->

## Why This Invariant Exists

<!-- The reason this must always be true. -->

## Violation Scenarios

<!-- What would happen if this invariant is violated? -->

* …

## Enforcement

### Tests

* **Unit:** [paths]
* **Integration:** [paths]
* **Property-based:** [paths]
* **Contract:** [paths]

### Static

* **Type system:** [rule]
* **Linter:** [rule]
* **Static analyzer:** [rule]

### Runtime

* **Assertion:** [location]
* **Watchdog:** [location]

## How to Verify

<!-- Step-by-step: how do we know this invariant still holds? -->

1. …
2. …

## Verification Cadence

* Per-PR (CI):
* Per-release:
* Per-quarter:

## Exceptions and Edge Cases

<!-- Any well-known edge cases that touch the invariant. -->

* …

## Related

* ADRs: [list]
* Business rules: [list]
* Glossary: [list]

## Change Log

| Date       | Change                       | Author |
|------------|------------------------------|--------|
| YYYY-MM-DD | Initial scaffold             |        |

---

> *An invariant without a test is a wish.*