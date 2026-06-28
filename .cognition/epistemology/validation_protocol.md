---
title: Validation Protocol
status: experimental
last_updated: 2026-06-28
owner: epistemology
---

# Validation Protocol

> How we validate claims — operationally.

This document is the **operational companion** to `evidence_model.md` and `truth_criteria.md`. It defines who does what, when, and how, when a claim is validated.

## When Validation Happens

Validation is triggered by one of the following events:

* A new claim is introduced into the project.
* An existing claim is challenged (contradiction appears).
* A periodic review cycle reaches a claim (per `truth_criteria.md`).
* A claim is involved in a decision and must be re-checked.
* An explicit request by any actor (including AI assistants).

## Who Validates

Validation is the responsibility of the **architect** role by default, but it can be delegated.

| Claim Type                       | Default Owner        | May Be Delegated To        |
|----------------------------------|----------------------|----------------------------|
| Architectural claim               | Architect            | Reviewer (with architect sign-off) |
| Domain claim                     | Architect or Domain Expert | Reviewer or Curator       |
| Code-level claim                 | Developer            | Reviewer                   |
| Operational claim                | Curator              | Anyone with relevant evidence |
| Epistemic claim (about knowledge) | Curator              | Reflector                  |

When in doubt, the architect decides.

## The Validation Workflow

### Step 1 — Identify the Claim

State the claim precisely. If the claim is ambiguous, return to the proposer and ask for clarification. **Validation cannot proceed on an ambiguous claim.**

### Step 2 — Identify the Evidence

List the evidence currently supporting the claim, with sources. Compare to `evidence_model.md` to ensure the evidence is appropriate.

If evidence is missing, the validation **pauses** until evidence is gathered.

### Step 3 — Check for Contradictions

Search the project knowledge for any evidence that contradicts the claim.

* If contradictions exist, the claim is marked **contested**, and validation cannot proceed until the contradiction is resolved.
* Resolution may involve:
  * Gathering more evidence.
  * Re-interpreting the claim.
  * Retiring the claim.

### Step 4 — Apply the Truth Criteria

Apply the five criteria from `truth_criteria.md`:

1. Well-formed claim.
2. Evidence threshold met.
3. No active contradictions.
4. Sources attributed.
5. Time horizon acknowledged.

If any criterion fails, the claim is **not validated** and is returned to the proposer with notes.

### Step 5 — Assign or Revise Confidence

Assign a confidence score (per `confidence_framework.md`), or revise the existing one.

The score is recorded along with the validation event.

### Step 6 — Record the Validation Event

Append to `.cognition/memory/history/decision_log.md` (since validation is a kind of decision):

```
YYYY-MM-DD — Validated claim: <claim statement>
- Actor: <who>
- Confidence: <new score>
- Evidence: <list of sources>
- Contradictions: <none or list>
- Time horizon: <period>
```

### Step 7 — Update the Claim's Home

Update the document where the claim lives to reflect:

* The new confidence.
* The evidence trail.
* The validation date.
* The next review date.

## Validation of Architectural Claims

Architectural claims (e.g., "we will use event sourcing for the audit log") are validated through **ADRs**, not through this protocol directly.

The protocol applies when:

* An ADR's premise needs validation (e.g., "event sourcing provides strong audit guarantees" — is this claim supported by evidence?).
* An ADR's consequences are being reviewed.

In those cases, the validation is recorded in the ADR's "Validation" section.

## Validation of Domain Claims

Domain claims (e.g., "all transactions before 2026-06-01 are processed in batch") are validated against:

* Observations in the project's data.
* Documentation from authoritative sources.
* Expert evidence from domain specialists.

If a domain claim is found to be false, the domain model (`.cognition/processes/architect/domain_model.md`) must be updated.

## Validation of Operational Truths

Operational truths (per `truth_criteria.md`) are subject to **periodic review**. The cadence:

* **Architectural truths:** at every architecture review (per `.cognition/processes/architect/`).
* **Domain truths:** at every domain model update.
* **Code-level truths:** at every PR review.

A truth that fails review is **demoted** to a claim, with the new evidence recorded.

## The Reflector's View

The reflector (per `.cognition/reflector/`) reviews the **history of validation events** periodically:

* Which claims were validated correctly (the confidence was justified)?
* Which claims were validated incorrectly (the confidence was over- or under-stated)?
* Are there patterns in the failures that suggest systematic issues?

This feeds the calibration discussion in `confidence_framework.md`.

## Anti-Patterns

The following are explicitly rejected:

* **Validation by assertion.** "We've always done it this way" is not validation.
* **Validation by silence.** "Nobody objected" is not validation.
* **Validation by majority.** "Most of the team thinks this is true" is not validation.
* **Validation by authority.** "The senior engineer says so" is not validation.
* **Skipping the contradictions check.** "We didn't find any" without an explicit search is not validation.

## Related

* `knowledge_theory.md` — categories of knowledge.
* `evidence_model.md` — what counts as evidence.
* `truth_criteria.md` — operational truth criteria.
* `confidence_framework.md` — confidence scores.
* `uncertainty_handling.md` — acting under uncertainty.
* `.cognition/memory/history/decision_log.md` — where validation events are recorded.