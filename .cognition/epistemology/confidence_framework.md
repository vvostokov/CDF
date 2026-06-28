---
title: Confidence Framework
status: experimental
last_updated: 2026-06-28
owner: epistemology
---

# Confidence Framework

> How we assign and revise confidence in claims.

This document gives every claim a **numeric confidence score** in [0.0, 1.0]. It defines what each score means, how it is assigned, and how it changes.

## Why a Numeric Scale

A binary "true / false" label is insufficient for real projects. Most claims live somewhere between "definitely true" and "definitely false". The confidence score makes this explicit and **comparable**: across many claims, you can prioritize verification effort based on which claims are least confident and most consequential.

## The Scale

CDF uses a 0.0–1.0 scale with the following bands.

### 0.95 – 1.00 — Verified Fact

* **Meaning:** Operational truth, validated to the standards in `truth_criteria.md`.
* **Action:** Treat as a basis for decisions.
* **Review:** Periodic.

### 0.80 – 0.94 — High Confidence

* **Meaning:** Strongly supported by evidence; no active contradictions; meets most but not all criteria for operational truth (e.g., only one source type instead of two).
* **Action:** Treat as a basis for decisions, but be ready to revise.
* **Review:** Before the next major decision that depends on this claim.

### 0.60 – 0.79 — Moderate Confidence

* **Meaning:** Plausible and supported by some evidence, but not enough to act on for high-stakes decisions.
* **Action:** Use as a working assumption for low-stakes decisions; flag for additional evidence before high-stakes use.
* **Review:** Within the current iteration.

### 0.40 – 0.59 — Low Confidence

* **Meaning:** Hypothesis with limited evidence. May be true; may not be.
* **Action:** Do not base decisions on this claim. Use only as a starting point for investigation.
* **Review:** As part of any retrospective.

### 0.20 – 0.39 — Speculation

* **Meaning:** An idea worth recording, but without meaningful supporting evidence.
* **Action:** Note it; do not act on it.
* **Review:** When the project encounters a context where the speculation may be relevant.

### 0.00 – 0.19 — Rejected

* **Meaning:** Considered and discarded, or so weakly supported that tracking it adds noise.
* **Action:** Move to history if it had any impact; otherwise delete from active consideration.
* **Review:** None.

## How Confidence Is Assigned

Confidence is assigned by the actor who first introduces a claim, based on:

1. **The strength of available evidence** (per `evidence_model.md`).
2. **The type of claim** (architectural > domain > code-level in terms of required confidence).
3. **The actor's own calibration** (see below).

The assignment is recorded with the claim. It is not a private judgment.

## Calibration

A confidence score is meaningful only if the actor assigning it is calibrated — i.e., claims given high confidence are actually correct most of the time, and claims given low confidence are rarely correct.

CDF v1.1 does not enforce calibration formally, but it requires that:

* Every actor reflect on their calibration periodically (per `.cognition/reflector/`).
* Claims that turn out to be wrong have their pre-revision confidence and post-revision confidence recorded, so calibration can be measured.

This is the basis for "trust through verification" in `kernel/principles.md`.

## How Confidence Is Revised

Confidence in a claim can change in either direction.

### Upward Revisions

* New evidence of a stronger type appears.
* An active contradiction is resolved in favour of the claim.
* An independent review confirms the claim.

### Downward Revisions

* Contradictory evidence appears.
* The original source becomes unreliable.
* The claim ages past its time horizon.
* The actor reflects that they were over-confident.

### The Process

Every confidence revision is recorded:

* **Date** of revision.
* **From** (old confidence).
* **To** (new confidence).
* **Reason** — what evidence or reasoning caused the change.
* **Actor** — who initiated the revision.

This record lives with the claim and feeds the periodic review.

## Confidence and Decisions

When making a decision, the relevant question is not "is this claim true?" but "**is the confidence in this claim high enough to justify the cost of acting on it being wrong?**"

A claim with confidence 0.9 may be insufficient for a million-dollar decision; a claim with confidence 0.7 may be sufficient for a cosmetic choice. **Decision-cost matters as much as claim-confidence.**

## Related

* `knowledge_theory.md` — claim as an epistemic category.
* `evidence_model.md` — what evidence supports a claim.
* `truth_criteria.md` — when a claim becomes operationally true.
* `uncertainty_handling.md` — how to act when confidence is low.
* `validation_protocol.md` — the operational process for confidence changes.