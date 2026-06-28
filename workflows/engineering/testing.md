# Workflow — Testing

## Goal

Verify that the system behaves correctly, that invariants are enforced, and that regressions are caught — **before** they reach production.

## Inputs

* The slice / feature spec / bug report under test.
* `.cognition/developer/implementation_constraints.md`.
* `.cognition/memory/permanent/invariants.md`.
* `.cognition/memory/permanent/business_rules.md`.
* The role prompt: `prompts/roles/developer.md`
* The task prompt: `prompts/tasks/testing.md`

## Outputs

* Test code in `tests/`.
* Updated `.cognition/memory/permanent/invariants.md` (when a new invariant is enforced).
* Coverage report or summary.
* Updated `.cognition/memory/working/current_context.md` (if testing reveals new state).

## Definition of Done

- [ ] Tests for the new behavior exist.
- [ ] All tests pass locally and in CI.
- [ ] Coverage targets met (project-defined).
- [ ] No flaky tests remain.
- [ ] Invariants have at least one test each.
- [ ] Business rules have at least one test each.

## Responsible Roles

* **Developer** (primary) — writes the tests.
* **Reviewer** — verifies test quality.

## Procedure

### Step 1 — Plan the Tests

1. Identify the behavior to test.
2. Choose the level (unit / property-based / integration / contract / e2e).
3. Write the test names first.

### Step 2 — Write the Tests (RED)

1. Write the test.
2. Run it; confirm it fails for the right reason.

### Step 3 — Make the Test Pass (GREEN)

1. Implement the minimum code.
2. Run the test; confirm it passes.

### Step 4 — Refactor (REFACTOR)

1. Clean up.
2. Re-run the test.

### Step 5 — Cover the Edges

1. Identify edge cases.
2. Add tests for them.

### Step 6 — Verify Invariants and Business Rules

For each invariant and business rule touched:

1. Verify a test exists.
2. Verify the test is meaningful (not just "call the function").

## Test Levels

| Level          | Speed     | Owned by       |
|----------------|-----------|----------------|
| Unit           | very fast | developer      |
| Property-based | fast      | developer      |
| Integration    | medium    | developer      |
| Contract       | medium    | developer / architect |
| End-to-end     | slow      | reviewer / QA  |

## Anti-Patterns (Refuse)

* Tests that pass by side effect.
* Tests that verify implementation, not behavior.
* Tests that require production data without a fixture.
* Skipping invariants.

---

> *Tests are how a project proves its invariants.*