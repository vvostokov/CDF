---
task: bug-fix
version: 0.1.0
status: active
pairs_with: [developer, reviewer, researcher]
---

# Task: Bug Fix

## Mission

Diagnose a defect, find the **root cause**, fix it, and prevent it from recurring — without introducing regressions or architectural drift.

## Responsibilities

* Reproduce the bug.
* Diagnose the root cause.
* Propose a minimal fix.
* Add a regression test.
* Capture lessons learned (if non-trivial).

## Inputs (must be read first)

1. The role prompt that scopes this task.
2. The bug report (`.github/ISSUE_TEMPLATE/bug-report.md` filled in).
3. `.cognition/identity/principles.md`.
4. `.cognition/identity/constraints.md`.
5. `.cognition/memory/permanent/invariants.md`.
6. `.cognition/memory/permanent/business_rules.md`.
7. Relevant ADRs (`knowledge/architecture-decisions/`).
8. The related slice / implementation plan.

## Outputs

* Root cause analysis (in the PR description).
* Minimal fix in `src/`.
* Regression test in `tests/`.
* Updated `.cognition/reviewer/technical_debt.md` if the bug is debt-related.
* Updated `.cognition/memory/permanent/invariants.md` if a new invariant is introduced.
* A note in `.cognition/curator/lessons_learned.md` (if non-trivial).
* A retrospective in `knowledge/retrospectives/` (if severe).

## Quality Criteria

* The fix addresses the **root cause**, not the symptom.
* The fix is **minimal** (no unrelated changes).
* A regression test fails without the fix and passes with it.
* The fix does not violate invariants.
* The fix does not introduce new technical debt.

## Failure Conditions

You must stop and ask if:

* The "fix" requires an architectural change (route to architect — propose an ADR).
* The bug cannot be reproduced.
* Multiple distinct root causes are plausible; investigation has not converged.
* The fix would break an existing test.

## Procedure

1. Read the inputs.
2. Reproduce the bug.
3. Diagnose the root cause (5 Whys, or equivalent).
4. Write a failing regression test (RED).
5. Apply the minimal fix (GREEN).
6. Refactor (REFACTOR).
7. Run the full test suite.
8. Update the cognitive layer as needed.
9. Document the lesson.

## Severity Matrix

| Severity | Fix SLA   | Examples                                   |
|----------|-----------|--------------------------------------------|
| Critical | Hours     | Data loss, security breach, total outage   |
| High     | 1 day     | Major feature broken, partial outage       |
| Medium   | 1 week    | Minor feature broken, workaround exists    |
| Low      | Backlog   | Cosmetic, rare edge case                   |

## Examples of Good Behavior

* "Root cause: the cancellation handler did not check that the order was already in `Cancelled` state, violating INV-003. Fix: added the check + a regression test."
* "I have categorized this as `high` because it affects 5% of requests. I am scheduling the fix for the next iteration."

## Examples of Bad Behavior (Refuse)

* "I'll just patch the symptom and ship."
* "Tests pass; merging without understanding the cause."

---

> *A bug fix without a regression test is a hope.*