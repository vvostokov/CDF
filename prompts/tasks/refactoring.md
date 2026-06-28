---
task: refactoring
version: 0.1.0
status: active
pairs_with: [developer, reviewer]
---

# Task: Refactoring

## Mission

Improve the structure of existing code **without changing its observable behavior**. Pay down technical debt without breaking invariants.

## Responsibilities

* Identify refactoring opportunities.
* Refactor in small, behavior-preserving steps.
* Maintain test coverage throughout.
* Update `.cognition/reviewer/technical_debt.md` when debt is paid.

## Inputs (must be read first)

1. The role prompt that scopes this task.
2. `.cognition/identity/principles.md`.
3. `.cognition/developer/implementation_constraints.md`.
4. `.cognition/reviewer/technical_debt.md` (the debt ledger).
5. `.cognition/memory/permanent/invariants.md`.
6. `.cognition/memory/permanent/business_rules.md`.
7. The relevant ADRs.

## Outputs

* Refactored code in `src/`.
* Updated tests in `tests/` (if structure changed but behavior did not).
* Updated `.cognition/reviewer/technical_debt.md`.
* A note in `.cognition/memory/sessions/session_log.md`.

## Quality Criteria

* **No behavior change.** Every refactor step has passing tests before and after.
* **Small steps.** Each commit / change is a single coherent transformation.
* **Tests cover the path being refactored** before the change.
* **No new debt** is introduced.
* **No invariants** are violated, even temporarily (use branches / feature flags if needed).

## Failure Conditions

You must stop and ask if:

* The refactor requires an architectural decision (route to architect).
* Behavior change is necessary for the goal (that's a feature / bug fix, not a refactor).
* Test coverage is insufficient to prove the refactor is safe.

## Procedure

1. Read the inputs.
2. Identify a **specific** code smell or debt item.
3. Confirm tests cover the behavior.
4. Apply the refactor in **one** small step.
5. Run tests.
6. Repeat until the smell is gone.
7. Update the debt ledger.

## Common Refactorings (Apply, Don't Announce)

* Extract function / class
* Inline function / class
* Rename (let the IDE / linter do it consistently)
* Move function / class
* Replace conditional with polymorphism
* Introduce parameter object
* Replace magic number with named constant
* Replace inheritance with composition

## Examples of Good Behavior

* "I am extracting the duplicate billing calculation into `BillingCalculator`. I have added unit tests that capture the existing behavior. The refactor passes them unchanged."
* "I am closing TD-014 by introducing a value object for `Money`. All callers updated."

## Examples of Bad Behavior (Refuse)

* "I am rewriting the module because it is messy." (Too big; break it down.)
* "Behavior is approximately the same." (No. Behavior must be exactly the same.)

---

> *Refactoring is the deliberate improvement of structure with the deliberate preservation of behavior.*