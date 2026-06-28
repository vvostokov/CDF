# Workflow — Architecture Review (Periodic)

## Goal

Periodically (typically per milestone or quarter) verify that the project's architecture **still matches its mission, vision, principles, and constraints**, and identify drift before it becomes debt.

## Inputs

* `.cognition/identity/mission.md`, `vision.md`, `principles.md`, `constraints.md`, `non-goals.md`, `tradeoffs.md`
* `.cognition/architect/domain_model.md`
* `.cognition/architect/system_context.md`
* `.cognition/architect/architecture_notes.md`
* `knowledge/architecture-decisions/`
* `.cognition/memory/permanent/invariants.md`
* `.cognition/memory/permanent/business_rules.md`
* `.cognition/memory/roadmap/roadmap.md`
* `.cognition/reviewer/technical_debt.md`
* Recent retrospectives (`knowledge/retrospectives/`)

## Outputs

* Updated `.cognition/reviewer/architecture_review.md` (the report).
* Proposed ADRs for identified drift.
* Updated `.cognition/reviewer/technical_debt.md`.
* Updated `.cognition/memory/roadmap/roadmap.md` (if the architecture changes the roadmap).

## Definition of Done

- [ ] The review report is complete and saved with the current period.
- [ ] All findings are categorized (healthy / at-risk / broken).
- [ ] Drift inventory is filled.
- [ ] At least one recommended action exists for each at-risk or broken item.
- [ ] New ADRs (or ADR proposals) are linked from the report.

## Responsible Roles

* **Reviewer** (primary) — conducts the review.
* **Architect** — confirms findings.
* **Planner** — confirms impact on roadmap.

## Procedure

### Step 1 — Gather Inputs

1. Collect every ADR, every recent retrospective, every recent review report.
2. Re-read the mission and vision.

### Step 2 — Answer the Mandatory Questions

From the architecture review template:

1. Does the architecture still match the mission and vision?
2. Are the bounded contexts correctly carved?
3. Are there invariants we no longer enforce?
4. Where is debt accumulating fastest?
5. Are any ADRs obsolete or contradicted?
6. Where is drift most likely next?
7. Are non-functional requirements still met?

### Step 3 — Categorize Findings

* **Healthy:** things to keep doing.
* **At risk:** things to monitor.
* **Broken:** things to fix now.

### Step 4 — Propose ADRs

For each broken item, propose an ADR.

### Step 5 — Publish

1. Save the report.
2. Open a Discussion under **Architecture & Design**.
3. Link from the next milestone.

## Anti-Patterns (Refuse)

* Reviews that list only praise.
* Reviews that list only complaints.
* Reviews with no actions.

---

> *Architecture reviews catch drift before drift catches the team.*