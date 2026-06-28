---
title: Uncertainty Handling
status: experimental
last_updated: 2026-06-28
owner: epistemology
---

# Uncertainty Handling

> How we act under uncertainty.

This document answers the question every project faces: **when we don't know, what do we do?**

## The Honest Position

All projects operate under uncertainty. The question is not whether uncertainty exists — it is whether we acknowledge it and plan for it.

CDF v1.1 requires that uncertainty is **explicit**:

* Every claim has a confidence score (per `confidence_framework.md`).
* Every decision references the claims it depends on.
* Every decision records what would make it wrong.

This is the opposite of "we'll figure it out as we go" — which is uncertainty denied, not uncertainty handled.

## Categories of Uncertainty

CDF v1.1 distinguishes four categories of uncertainty.

### Known Unknowns

Things we know we don't know.

* **Example:** "We don't know how the system behaves under load > 10x baseline."
* **Treatment:** Tracked explicitly, assigned an owner, scheduled for investigation.
* **Location:** `.cognition/memory/working/active_questions.md` and `knowledge/risks/`.

### Unknown Unknowns

Things we don't know we don't know.

* **Example:** The system fails in a scenario the team never imagined.
* **Treatment:** Cannot be prevented by process. Mitigated by:
  * Diversity of perspectives (multiple actors, multiple reviewers).
  * Periodic reflection (per `.cognition/reflector/`).
  * Small, reversible decisions.
  * Strong monitoring.

### Acknowledged Uncertainty

A claim or decision whose confidence is below the threshold for high-stakes action.

* **Example:** "We are 70% confident that this scaling approach will work."
* **Treatment:** Decision can proceed **only** if:
  * The cost of being wrong is bounded.
  * A rollback path exists.
  * The claim is re-checked within a defined period.

### Hidden Uncertainty

A claim that is treated as certain but is, in fact, not.

* **Example:** "The system always does X" — but the team has never tested it under condition Y.
* **Treatment:** This is the most dangerous category. CDF v1.1 mitigates it through:
  * Mandatory evidence trails for every claim (per `evidence_model.md`).
  * Periodic reviews (per `truth_criteria.md`).
  * A culture that rewards admitting uncertainty over projecting confidence.

## Decision Rules Under Uncertainty

When a decision must be made under acknowledged uncertainty, the following rules apply.

### Rule 1: Prefer Reversible Decisions

If two options are roughly equivalent in expected value, prefer the one that is easier to reverse.

This rule is from `kernel/principles.md` and applies especially under uncertainty.

### Rule 2: Bound the Cost of Being Wrong

If the cost of being wrong is unbounded (data loss, security breach, regulatory violation), do not proceed under acknowledged uncertainty.

If the cost of being wrong is bounded and the expected value of acting is positive, proceed with monitoring.

### Rule 3: Document the Uncertainty

Every decision made under uncertainty must record:

* The claim being acted on and its confidence.
* The cost of being wrong.
* The reversal path.
* The signal that would indicate the decision was wrong.

This is logged in the decision log: `.cognition/memory/history/decision_log.md`.

### Rule 4: Re-Check on Schedule

A decision made under acknowledged uncertainty must be re-checked at a defined interval, even if no problem has emerged.

The interval depends on the stakes:

* **High stakes:** weekly for the first month, then monthly.
* **Medium stakes:** monthly.
* **Low stakes:** at the next retrospective.

### Rule 5: Upgrade Confidence Through Action

Some uncertainty can be reduced only by acting. In that case:

* The action is explicitly framed as a **probe**, not a commitment.
* Success criteria are defined in advance.
* The result is recorded as evidence in the relevant claim's trail.

## The Reflector's Role

Uncertainty handling is not a one-time activity. The reflector (per `.cognition/reflector/`) periodically reviews:

* Which decisions were made under high uncertainty.
* Which of those decisions proved right or wrong.
* Whether the team's calibration improved or worsened.

This feeds back into the team's collective sense of what they know and don't know.

## Related

* `knowledge_theory.md` — categories of knowledge.
* `confidence_framework.md` — assigning confidence to claims.
* `truth_criteria.md` — when to act on a claim.
* `validation_protocol.md` — how to validate claims.
* `kernel/principles.md` — foundational principles including reversibility.
* `.cognition/reflector/` — periodic review of uncertainty handling.