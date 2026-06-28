# Workflow — Research

## Goal

Investigate an **unknown** that is blocking or might block the project. Produce findings that inform an ADR, a backlog item, or a lesson.

## Inputs

* `.cognition/architect/decision_queue.md`.
* `.cognition/memory/working/active_questions.md`.
* `.cognition/planner/backlog.md` (research-flagged items).
* `.cognition/identity/constraints.md`.
* The role prompt: `prompts/roles/researcher.md`.

## Outputs

* New entries in `.cognition/researcher/research_notes.md`.
* New entries in `.cognition/researcher/experiments.md`.
* Proposed ADR (when findings warrant a decision).
* Backlog updates (when findings should be deferred as features).
* Lessons learned (when findings change behavior).

## Definition of Done

- [ ] The research question is stated.
- [ ] The hypothesis (if any) is stated.
- [ ] The method is recorded.
- [ ] The time-box is set.
- [ ] Findings are recorded.
- [ ] A verdict is recorded: `validated` | `rejected` | `inconclusive`.
- [ ] Findings are promoted (or explicitly retired).
- [ ] Session log entry recorded.

## Responsible Roles

* **Researcher** (primary).
* **Architect** (consumes findings).
* **Planner** (consumes findings).

## Procedure

### Step 1 — Frame

1. State the research question.
2. State the hypothesis.
3. State the method (spike / benchmark / reading).
4. Set the time-box.

### Step 2 — Run

1. Run the experiment / spike.
2. Capture evidence (measurements, logs, references).

### Step 3 — Conclude

1. State findings.
2. State verdict.
3. State next step (ADR / backlog / lesson / retire).

### Step 4 — Promote

If the finding warrants it:

* Propose an ADR.
* Add a backlog item.
* Add a lesson learned.

### Step 5 — Record

Append a session note.

## Anti-Patterns (Refuse)

* Continuing past the time-box without a result.
* Reaching conclusions without measurement.
* Writing production code during research.

---

> *Research is how the project learns without paying the full price of failure.*