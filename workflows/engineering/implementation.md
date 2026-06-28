# Workflow — Implementation

## Goal

Turn the architect's design into **working, tested, documented** code that meets the slice's Definition of Done.

## Inputs

* `.cognition/planner/next_vertical_slice.md`
* `.cognition/developer/implementation_plan.md`
* `.cognition/developer/current_task.md`
* `.cognition/developer/implementation_constraints.md`
* `.cognition/architect/domain_model.md`
* `.cognition/architect/system_context.md`
* The relevant ADR.
* The relevant feature spec.
* The role prompt: `prompts/roles/developer.md`

## Outputs

* Source code in `src/`.
* Tests in `tests/`.
* Updated `.cognition/developer/implementation_plan.md` (progress).
* Updated `.cognition/developer/current_task.md`.
* Updated `.cognition/memory/working/current_context.md`.
* PR opened using `.github/PULL_REQUEST_TEMPLATE/pull_request_template.md`.

## Definition of Done

- [ ] All code compiles / lints clean.
- [ ] All tests pass locally.
- [ ] All tests pass in CI.
- [ ] New tests cover the new behavior.
- [ ] New invariants are enforced by tests or static checks.
- [ ] Documentation updated.
- [ ] Cognitive layer updated (domain model, glossary, invariants, business rules as needed).
- [ ] PR opened with the standard template.
- [ ] PR reviewed and merged.
- [ ] `.cognition/memory/working/current_context.md` reflects the new state.

## Responsible Roles

* **Developer** (primary).
* **Reviewer** (code review).
* **Architect** (architectural review if the slice touched the architecture).

## Procedure

### Step 1 — Refresh the Plan

Update `.cognition/developer/implementation_plan.md` with the latest understanding.

### Step 2 — Set the Current Task

Update `.cognition/developer/current_task.md` to the smallest executable step.

### Step 3 — Red-Green-Refactor

For each step:

1. Write a failing test (RED).
2. Implement the minimum code (GREEN).
3. Refactor (REFACTOR).
4. Update `current_task.md`.

### Step 4 — Document as You Go

* Update inline docs.
* Update `docs/` if user-facing.
* Update `knowledge/...` if durable.

### Step 5 — Open the PR

Use the PR template. Tick all cognitive-layer checkboxes.

### Step 6 — Respond to Review

Address comments, update the plan, re-run tests.

### Step 7 — Merge

* Merge only after CI is green and reviews are approved.
* After merge, update `.cognition/memory/working/current_context.md`.

## Anti-Patterns (Refuse)

* "I'll add tests later."
* "I'll update docs later."
* "I'll merge now and refactor next week."
* Silent architectural changes.

---

> *Implementation is the discipline of turning intent into evidence.*