# Workflow — Architecture Design

## Goal

Design the **structure** for the next vertical slice in a way that fits the domain model, respects invariants, and yields an ADR.

## Inputs

* `.cognition/planner/next_vertical_slice.md`
* `.cognition/architect/domain_model.md`
* `.cognition/architect/system_context.md`
* `.cognition/memory/permanent/invariants.md`
* `.cognition/memory/permanent/business_rules.md`
* `knowledge/features/NNNN-*.md` (the relevant feature spec)
* The role prompt: `prompts/roles/architect.md`

## Outputs

* Updated `.cognition/architect/domain_model.md` (if the slice adds entities, etc.).
* Updated `.cognition/architect/system_context.md` (if it changes processes / integrations).
* Updated `.cognition/architect/architecture_notes.md`.
* Updated `.cognition/architect/decision_queue.md`.
* A proposed ADR (`knowledge/architecture-decisions/NNNN-*.md`).
* A proposed decision proposal (`knowledge/decision-proposals/DP-NNN-*.md`) if needed.
- Updated `.cognition/memory/permanent/architectural_decisions.md` (when ADR accepted).
- Updated `.cognition/memory/history/decision_log.md`.

## Definition of Done

- [ ] At least two options were considered.
- [ ] The recommended option is justified against principles, constraints, and prior ADRs.
- [ ] New invariants have been proposed and added to `.cognition/memory/permanent/invariants.md`.
- [ ] New business rules have been proposed and added to `.cognition/memory/permanent/business_rules.md`.
- [ ] The domain model has been updated if entities / aggregates / contexts changed.
- [ ] The system context has been updated if deployment / integrations changed.
- [ ] An ADR is written and has the appropriate status (`proposed`).
- [ ] The slice is now ready for the developer.

## Responsible Roles

* **Architect** (primary).
* **Reviewer** (consulted).
* **Developer** (consulted for feasibility).

## Procedure

### Step 1 — Read the Inputs

1. Re-read the inputs.
2. Identify the design question.

### Step 2 — Explore the Options

1. Draft at least two designs.
2. For each: pros, cons, alignment with principles, alignment with constraints.

### Step 3 — Decide

1. Pick the recommended option.
2. State the rationale.

### Step 4 — Write the ADR

Use `knowledge/architecture-decisions/0000-template.md`.

### Step 5 — Update the Cognitive Layer

1. Update domain model / system context / invariants / business rules / glossary as needed.
2. Update the decision index (`/.cognition/memory/permanent/architectural_decisions.md`).
3. Append to `/.cognition/memory/history/decision_log.md`.

### Step 6 — Hand Off

Notify the developer that the slice is ready for implementation.

## Anti-Patterns (Refuse)

* "Just one option" (no alternatives = no design).
* Skipping the invariants.
* Designing in chat without writing anything down.

---

> *Design is the work of making the future small enough to fit on a page.*