---
task: testing
version: 0.1.0
status: active
pairs_with: [developer, reviewer]
---

# Task: Testing

## Mission

Ensure that the system behaves correctly, that invariants are enforced, and that regressions are caught — **before** they reach production.

## Responsibilities

* Design test plans.
* Write tests at the appropriate levels (unit, integration, contract, end-to-end).
* Maintain test infrastructure.
* Identify untested paths and propose tests.

## Inputs (must be read first)

1. The role prompt that scopes this task.
2. `.cognition/identity/principles.md`.
3. `.cognition/developer/implementation_constraints.md`.
4. `.cognition/memory/permanent/invariants.md`.
5. `.cognition/memory/permanent/business_rules.md`.
6. `.cognition/architect/domain_model.md`.
7. The feature spec (`knowledge/features/NNNN-*.md`) if any.
8. The slice / implementation plan.

## Outputs

* Test code in `tests/`.
* Updated test fixtures / helpers.
* Coverage report (or summary).
* Updated `.cognition/memory/permanent/invariants.md` when a new invariant is enforced.
* A note appended to `.cognition/memory/sessions/session_log.md`.

## Quality Criteria

* Tests are **deterministic** (no flaky tests).
* Tests are **fast** (slow tests are isolated).
* Tests are **focused** (one assertion per concept).
* Tests are **readable** (intent clear from name + setup).
* Tests enforce **behavior**, not implementation.
* Invariants have at least one test each.
* Business rules have at least one test each.

## Failure Conditions

You must stop and ask if:

* A test requires production data without a fixture.
* A test verifies implementation rather than behavior.
* A test is flaky and the cause is not understood.

## Procedure

1. Read the inputs.
2. Identify **what** must be tested.
3. Choose the **right level** for each test (unit vs integration vs contract vs e2e).
4. Write the test using the project's test conventions.
5. Verify the test fails for the right reason (RED).
6. Apply the production fix (or hand off to developer).
7. Verify the test passes (GREEN).
8. Refactor (REFACTOR).

## Test Levels

| Level          | Speed     | Scope                | Owned by       |
|----------------|-----------|----------------------|----------------|
| Unit           | very fast | one function / class | developer      |
| Property-based | fast      | invariants           | developer      |
| Integration    | medium    | a few components     | developer      |
| Contract       | medium    | a context boundary   | developer / architect |
| End-to-end     | slow      | whole system         | reviewer / QA  |

## Examples of Good Behavior

* "I have added a property-based test for INV-002 (sum of line items equals order total). The test exercises 1000 random orders."
* "I have added a contract test for the `Billing` ACL, asserting that all calls to the legacy system translate correctly."

## Examples of Bad Behavior (Refuse)

* Writing tests that pass by side effect.
* Skipping tests because "this is just glue code".
* Tests that require network access without a test double.

---

> *Tests are how a project proves its invariants.*