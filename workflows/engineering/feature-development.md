# Workflow — Feature Development

## Goal

Take a feature from **idea** to **shipped**, with full cognitive-layer updates at every step.

## Inputs

* The feature request (issue / discussion).
* `.cognition/identity/mission.md`, `principles.md`, `non-goals.md`, `tradeoffs.md`.
* `.cognition/memory/roadmap/roadmap.md`.
* `.cognition/planner/backlog.md`.
* Existing ADRs.
* `.cognition/architect/domain_model.md`.
* `.cognition/architect/system_context.md`.

## Outputs

* A feature spec: `knowledge/features/F-NNN-*.md`.
* (Potentially) a decision proposal and an ADR.
* Implemented and tested code in `src/` and `tests/`.
* Updated `.cognition/` (domain model, glossary, invariants, business rules, decision log).
* Updated documentation.
* Updated roadmap and milestones.
* A retrospective (post-shipment).

## Definition of Done

- [ ] Feature spec is written and accepted.
- [ ] Architectural changes (if any) are ADR-ed.
- [ ] Domain model, glossary, invariants, and business rules are updated.
- [ ] Code is implemented and tested.
- [ ] Documentation is updated.
- [ ] Cognitive layer reflects the shipped state.
- [ ] Roadmap / milestone is updated.
- [ ] Retrospective is held (per `workflows/knowledge/retrospective.md`).

## Responsible Roles

* **Planner** — owns the feature's place in the backlog / iteration.
* **Architect** — owns the design.
* **Developer** — owns implementation.
* **Reviewer** — owns review.
* **Curator** — owns cognitive-layer updates.
* **Researcher** — owns spikes.

## Procedure

### Step 1 — Idea → Spec

1. Open an issue using `.github/ISSUE_TEMPLATE/feature-request.md`.
2. Discuss in **Ideas** (Discussions) if not yet clear.
3. Draft `knowledge/features/F-NNN-*.md` from `0000-template.md`.
4. Mark the spec `proposed`.

### Step 2 — Spec → Accepted

1. Review the spec against identity and the domain model.
2. Identify bounded contexts, aggregates, entities, invariants, business rules touched.
3. Identify risks.
4. Update the spec.
5. Mark the spec `accepted`.

### Step 3 — Accepted → Designed

1. Architect designs the change.
2. If architectural change needed: write ADR.
3. Update domain model / system context / invariants / business rules / glossary.

### Step 4 — Designed → Scheduled

1. Planner adds the slice to the iteration.
2. Update `next_vertical_slice.md`.

### Step 5 — Scheduled → Implemented

Per `workflows/engineering/implementation.md`.

### Step 6 — Implemented → Reviewed

Per `workflows/engineering/code-review.md`.

### Step 7 → Shipped

Per `workflows/engineering/release.md`.

### Step 8 → Reflected

Per `workflows/knowledge/retrospective.md`.

## Anti-Patterns (Refuse)

* Implementing without a spec.
* Skipping ADR for architectural change.
* Skipping cognitive-layer updates.

---

> *A feature is a promise to a user. The spec is the contract.*