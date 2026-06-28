# Workflow — Refactoring

## Goal

Improve the **structure** of the code without changing **observable behavior**. Pay down debt without breaking invariants.

## Inputs

* `.cognition/reviewer/technical_debt.md`.
* `.cognition/developer/implementation_constraints.md`.
* `.cognition/memory/permanent/invariants.md`.
* `.cognition/memory/permanent/business_rules.md`.
* The role prompt: `prompts/roles/developer.md`.
* The task prompt: `prompts/tasks/refactoring.md`.

## Outputs

* Refactored code in `src/`.
* Updated tests in `tests/`.
* Updated `.cognition/reviewer/technical_debt.md`.
* A note in `.cognition/memory/sessions/session_log.md`.

## Definition of Done

- [ ] Tests pass before the refactor.
- [ ] Tests pass after each refactor step.
- [ ] No observable behavior changed.
- [ ] No new debt is introduced.
- [ ] No invariants are violated.
- [ ] The relevant debt item is closed (or marked `in-progress`).

## Responsible Roles

* **Developer** (primary).
* **Reviewer** (verifies behavior preservation).

## Procedure

### Step 1 — Pick the Debt

1. Read `.cognition/reviewer/technical_debt.md`.
2. Pick one item.
3. Confirm tests cover the behavior.

### Step 2 — Refactor in Small Steps

1. Apply **one** refactoring.
2. Run all tests.
3. Commit.
4. Repeat.

### Step 3 — Update the Ledger

Mark the debt item `resolved` (with PR link).

### Step 4 — Update Documentation

If the refactor changes a public API or a contract:

* Update `docs/`.
* Update the feature spec (`knowledge/features/`).

## Anti-Patterns (Refuse)

* Refactoring without tests covering the behavior.
* Mixing refactoring with bug fixes or features.
* "Big bang" rewrites.

---

> *Refactoring is the discipline of improving structure without changing behavior.*