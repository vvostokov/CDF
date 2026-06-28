---
title: Truth Criteria
status: experimental
last_updated: 2026-06-28
owner: epistemology
---

# Truth Criteria

> When is something "true enough" to act on?

This document answers the practical question that `knowledge_theory.md` leaves open: given a claim, supported by evidence, when do we treat it as true?

## The Problem with "Truth"

In a strict philosophical sense, no claim about the world is provably true. But software projects cannot operate under permanent skepticism — at some point, decisions must be made.

CDF v1.1 therefore distinguishes between:

* **Absolute truth** — unknowable in principle.
* **Operational truth** — a claim that has met the project's criteria for being acted upon.

This document defines **operational truth criteria**.

## The Criteria

A claim becomes operationally true when **all** of the following hold:

### 1. The Claim Is Well-Formed

The claim is stated in a way that is testable.

* **Pass:** "All transactions before 2026-06-01 are processed in batch."
* **Fail:** "Transactions are usually processed in batch."

A claim that cannot be tested cannot be validated.

### 2. The Evidence Threshold Is Met

The claim is supported by a sufficient body of evidence, according to `evidence_model.md`.

* **Default threshold:** At least two independent pieces of evidence, of at least two different types.
* **Higher-stakes claims** (architectural, security, financial): require at least three pieces of evidence, with at least one direct empirical.
* **Lower-stakes claims** (cosmetic, internal naming): require at least one piece of evidence.

### 3. No Active Contradictions

No piece of evidence currently in the project's knowledge base contradicts the claim.

* A contradiction is **active** until it is resolved (explained away, the contradicting evidence is found to be erroneous, or the claim is revised).
* A claim with an active contradiction cannot be promoted to operational truth, no matter how strong the supporting evidence.

### 4. The Source Is Attributed

Every piece of evidence has a source, and every source is identified.

* "We tested it" is not attribution. "We tested it on commit X by Y on date Z" is attribution.

### 5. The Time Horizon Is Acknowledged

Every claim has an implicit time horizon — the period during which it is expected to hold.

* A claim about the system's behaviour today is different from a claim about its behaviour over the next decade.
* Time horizons longer than the project's history must be marked **provisional** and reviewed periodically.

## What "Operationally True" Means

A claim that has met these criteria is **operationally true**. This means:

* It is treated as true for the purposes of decision-making.
* It is documented as such (with its evidence trail).
* It is **subject to revision** if new evidence emerges.

Operational truth is **not** an absolute commitment. It is a working assumption with an audit trail.

## When Truth Criteria Fail

A claim that fails any of the five criteria must be marked:

* **Hypothesis** — if it is plausible and worth investigating.
* **Speculation** — if it is interesting but not yet worth tracking.
* **Rejected** — if it has been considered and discarded.

These statuses are not failures — they are honest labels.

## Periodic Review

Operational truths are not eternal. CDF requires that every operational truth is reviewed periodically:

* **Architectural truths:** every architecture review (per `.cognition/processes/architect/`).
* **Domain truths:** every iteration, as part of the domain model update.
* **Code-level truths:** every PR review.

A truth that fails its review is **demoted** to a claim, with the new evidence recorded.

## Related

* `knowledge_theory.md` — the broader theory.
* `evidence_model.md` — what counts as evidence.
* `confidence_framework.md` — how confidence and truth relate.
* `validation_protocol.md` — the operational process for validating claims.