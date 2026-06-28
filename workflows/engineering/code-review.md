# Workflow — Code Review

## Goal

Catch drift, regressions, contradictions, and risks **before** code is merged — without slowing the team.

## Inputs

* The PR / change under review.
* `.cognition/identity/principles.md`
* `.cognition/identity/constraints.md`
* `.cognition/identity/non-goals.md`
* `.cognition/identity/tradeoffs.md`
* `.cognition/architect/domain_model.md`
* `.cognition/architect/system_context.md`
* `.cognition/developer/implementation_constraints.md`
* `.cognition/memory/permanent/invariants.md`
* `.cognition/memory/permanent/business_rules.md`
* `.cognition/memory/permanent/glossary.md`
* All ADRs.
* The role prompt: `prompts/roles/reviewer.md`
* The task prompt: `prompts/tasks/code-review.md` (if present) — otherwise this workflow.

## Outputs

* Inline review comments on the PR.
* A review report: `.cognition/reviewer/review_report.md`.
* (If needed) updated `.cognition/reviewer/technical_debt.md`.
* (If needed) proposed ADR / decision proposal.

## Definition of Done

- [ ] All findings are categorized (blocker / major / minor / nit).
- [ ] Every blocker has a concrete fix.
- [ ] Every major issue is linked to a principle, ADR, or invariant.
- [ ] Architectural drift (if any) has a proposed ADR.
- [ ] New debt (if any) is logged.
- [ ] A verdict is recorded (`Approve` | `Request changes` | `Reject`).

## Responsible Roles

* **Reviewer** (primary).
* **Architect** (consulted for architectural concerns).

## Procedure

### Step 1 — Read the PR Context

1. Read the PR description and linked slice / plan.
2. Read the relevant ADRs and feature spec.

### Step 2 — Read the Diff

1. Read the diff line by line.
2. For each file, check:
   * Naming consistency.
   * Boundary respect.
   * Test coverage.
   * Invariant enforcement.
   * Business rule enforcement.
   * Documentation.

### Step 3 — Categorize Findings

* **Blocker** — must be fixed before merge.
* **Major** — should be fixed; rare exceptions accepted with justification.
* **Minor** — nice to fix; not blocking.
* **Nit** — preference; not blocking.

### Step 4 — Write the Review Report

Use `.cognition/reviewer/review_report.md`.

### Step 5 — Communicate

Submit the report and inline comments.

### Step 6 — Track Outcomes

After the author addresses findings:

1. Re-review.
2. Update the report with the final verdict.
3. Update `technical_debt.md` if any debt was logged.

## Anti-Patterns (Refuse)

* "Looks good to me." (No review = no value.)
* Blocking on style preferences with no principle.
* Approving a change that contradicts identity.

---

> *Reviews are how the project learns in public.*