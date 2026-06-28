# Workflow — Retrospective

## Goal

At the end of an **iteration, milestone, release, or incident**, capture what happened, what we learned, and what we will change.

## Inputs

* The slice / milestone / release / incident under review.
* `.cognition/identity/principles.md`.
* Recent sessions (`.cognition/memory/sessions/session_log.md`).
* The recent ADRs and PRs.
* The role prompt: depends on who is running it.

## Outputs

* A retrospective file in `knowledge/retrospectives/NNNN-*.md` (using `0000-template.md`).
* Updated `.cognition/curator/lessons_learned.md`.
* Updated `.cognition/reviewer/technical_debt.md` (if relevant).
* Updated `.cognition/memory/roadmap/roadmap.md` (if relevant).
- Updated `.cognition/memory/history/decision_log.md` (if a decision was made).
* A note in `.cognition/memory/sessions/session_log.md`.

## Definition of Done

- [ ] The retrospective covers the agreed scope.
- [ ] Each lesson learned is specific and actionable.
- [ ] Action items have owners and deadlines.
- [ ] Lessons are promoted to `.cognition/curator/lessons_learned.md`.
- [ ] Action items are added to the backlog if appropriate.
- [ ] The retrospective is filed under `knowledge/retrospectives/`.

## Responsible Roles

* Any role can call a retrospective.
* **Curator** ensures lessons are promoted.
* **Reviewer** ensures technical debt is logged.
* **Planner** ensures action items are scheduled.

## Procedure

### Step 1 — Schedule

1. Decide on a scope (iteration / milestone / release / incident).
2. Set a time-box (typical: 60–90 minutes).
3. Invite the relevant participants (human and AI roles).

### Step 2 — Gather Inputs

1. Pull the recent PRs, ADRs, sessions, bugs.
2. Pull recent lessons learned.

### Step 3 — Run the Retrospective

Use the four-lens structure:

* **What went well** — keep doing.
* **What hurt** — stop doing.
* **What surprised us** — investigate.
* **What we learned** — promote.

### Step 4 — Write the Retrospective

Use `knowledge/retrospectives/0000-template.md`.

### Step 5 — Promote Lessons

Promote durable lessons to `.cognition/curator/lessons_learned.md`.

### Step 6 — Schedule Action Items

1. Add action items to the backlog (with owners).
2. Update `.cognition/memory/roadmap/roadmap.md` if relevant.

### Step 7 — Log

Append a session note.

## Cadence

| Scope      | Cadence           |
|------------|-------------------|
| Iteration  | Every iteration   |
| Milestone  | Every milestone   |
| Release    | Every release     |
| Incident   | Within 1 week     |

## Anti-Patterns (Refuse)

* Retrospectives with no action items.
* Retrospectives without owners.
* Retrospectives that are blame sessions.

---

> *A retrospective without action items is a complaint with witnesses.*