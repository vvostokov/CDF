# Workflow — Planning (Iteration Planning)

## Goal

Choose the next **vertical slice** to deliver, in a way that respects priorities, dependencies, and the project's current goal.

## Inputs

* `.cognition/planner/current_goal.md`
* `.cognition/planner/backlog.md`
* `.cognition/identity/mission.md`, `principles.md`, `non-goals.md`, `tradeoffs.md`
* `.cognition/memory/roadmap/roadmap.md`
* `.cognition/curator/lessons_learned.md`
* `.cognition/memory/working/current_context.md`

## Outputs

* Updated `.cognition/planner/current_iteration.md` (or new iteration)
* Updated `.cognition/planner/next_vertical_slice.md`
* Updated `.cognition/planner/backlog.md`
* Updated `.cognition/memory/working/current_context.md`

## Definition of Done

- [ ] The next vertical slice is selected and documented.
- [ ] The slice is **end-to-end** (cuts through all relevant layers).
- [ ] The slice is **small** (deliverable in days).
- [ ] The slice's acceptance criteria are documented.
- [ ] The slice has a Definition of Done.
- [ ] The slice is linked to the relevant feature spec / ADR / discussion.
- [ ] The backlog reflects the new ordering.

## Responsible Roles

* **Planner** (primary) — owns the slice.
* **Architect** — confirms the slice is consistent with the domain model.
* **Developer** — confirms the slice is implementable.

## Procedure

### Step 1 — Review

1. Re-read the inputs.
2. Re-read the lessons learned (what has hurt us before?).
3. Re-read the open questions (`.cognition/memory/working/active_questions.md`).

### Step 2 — Choose the Slice

1. Pick the highest-priority item from the backlog that is:
   * Unblocked.
   * End-to-end.
   * Sized for days, not weeks.
2. If none qualifies, **schedule research first**.

### Step 3 — Document the Slice

Write the slice in `.cognition/planner/next_vertical_slice.md` using the template there.

### Step 4 — Update the Backlog

Reorder the backlog to reflect the new state.

### Step 5 — Hand Off

1. Notify the architect that a new slice is ready for design review.
2. Update `.cognition/memory/working/current_context.md`.

## Anti-Patterns (Refuse)

* Slices that touch only one layer.
* Slices sized "as long as it takes".
* Slices without acceptance criteria.

---

> *A slice is a hypothesis about what should be built next. Make it falsifiable.*