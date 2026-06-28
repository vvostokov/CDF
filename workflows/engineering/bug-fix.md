# Workflow — Bug Fix

## Goal

Diagnose a defect, find the **root cause**, fix it, and prevent it from recurring — without introducing regressions or architectural drift.

## Inputs

* The bug report (`.github/ISSUE_TEMPLATE/bug-report.md` filled in).
* `.cognition/identity/principles.md`.
* `.cognition/identity/constraints.md`.
* `.cognition/memory/permanent/invariants.md`.
* `.cognition/memory/permanent/business_rules.md`.
* Relevant ADRs.
* The role prompt: `prompts/roles/developer.md`.
* The task prompt: `prompts/tasks/bug-fix.md`.

## Outputs

* Root cause analysis (in the PR description).
* Minimal fix in `src/`.
* Regression test in `tests/`.
* Updated `.cognition/reviewer/technical_debt.md` (if bug is debt-related).
* Updated `.cognition/memory/permanent/invariants.md` (if a new invariant is introduced).
* A note in `.cognition/curator/lessons_learned.md` (if non-trivial).
* A retrospective in `knowledge/retrospectives/` (if severe).

## Definition of Done

- [ ] The bug is reproduced.
- [ ] The root cause is documented.
- [ ] The minimal fix is applied.
- [ ] A regression test fails without the fix and passes with it.
- [ ] The full test suite is green.
- [ ] No invariants are violated.
- [ ] No new technical debt is introduced.
- [ ] Lessons learned are recorded (if applicable).

## Responsible Roles

* **Developer** (primary) — fixes the bug.
* **Reviewer** — verifies the fix.
* **Curator** — updates permanent memory.
* **Architect** — involved if the fix touches the architecture.

## Procedure

### Step 1 — Reproduce

1. Read the bug report.
2. Reproduce locally.
3. Capture evidence (logs, screenshots, traces).

### Step 2 — Diagnose

1. Use the 5 Whys (or equivalent).
2. Identify the root cause.
3. Identify contributing factors.

### Step 3 — Write the Regression Test (RED)

1. Write a test that reproduces the bug.
2. Confirm it fails for the right reason.

### Step 4 — Fix (GREEN)

1. Apply the minimal fix.
2. Confirm the regression test passes.
3. Confirm the full test suite is green.

### Step 5 — Refactor (REFACTOR)

1. Clean up.
2. Re-run all tests.

### Step 6 — Update the Cognitive Layer

* If a new invariant is introduced: add it (with enforcement).
* If the fix addresses a known debt: update `technical_debt.md`.
* If the fix reveals a new lesson: add to `lessons_learned.md`.

### Step 7 — PR

Open a PR using the standard template.

### Step 8 — Post-Mortem (if severe)

Open a retrospective per `workflows/knowledge/retrospective.md`.

## Anti-Patterns (Refuse)

* "I'll patch the symptom and ship."
* "Tests pass; merging without understanding the cause."
* Fixes that hide the symptom (e.g. catching an exception that should bubble).

---

> *A bug fix without a regression test is a hope.*