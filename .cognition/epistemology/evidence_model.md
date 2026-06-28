---
title: Evidence Model
status: experimental
last_updated: 2026-06-28
owner: epistemology
---

# Evidence Model

> What counts as evidence in this project, and what does not.

This document defines **what counts as evidence** when validating a claim. Without this definition, "evidence" becomes a vague word that can be used to support almost anything.

## The Purpose of Evidence

Evidence exists to:

1. **Promote a claim to a fact** by demonstrating it is consistent with reality.
2. **Demote a fact** when contradictory evidence appears.
3. **Calibrate confidence** in a model by comparing predictions to observations.

Evidence does **not** exist to:

* Prove a claim absolutely.
* Justify a pre-existing belief.
* End debate.

## Types of Evidence

CDF v1.1 accepts the following evidence types, ordered by strength.

### Direct Empirical Evidence

A recorded observation of the phenomenon the claim is about.

* **Example:** A test run that produces the result the claim predicts.
* **Strength:** Highest — the claim is directly observed in operation.
* **Requirement:** Reproducible. The observation must be reproducible by another actor under the same conditions.

### Indirect Empirical Evidence

An observation of a closely-related phenomenon that the claim implies.

* **Example:** A test of a sub-system that the claim depends on.
* **Strength:** High — strong support, but not the claim itself.
* **Requirement:** The relationship between the observation and the claim must be documented.

### Documentary Evidence

A reference to an external, authoritative source that states the claim.

* **Example:** An official specification, a published standard, a verified third-party document.
* **Strength:** Medium — depends on the reliability of the source.
* **Requirement:** The source must be cited, accessible, and verifiable.

### Logical Evidence

A derivation from other facts and rules of inference.

* **Example:** "Given that A and B are true, by modus ponens, C must be true."
* **Strength:** Medium — depends on the validity of the premises.
* **Requirement:** The derivation must be reproducible step by step.

### Expert Evidence

A statement by a recognized expert in the domain.

* **Example:** "According to the GAAP standard, this is treated as …"
* **Strength:** Low to medium — depends on the expert's track record in this project.
* **Requirement:** The expert's identity, credentials, and basis must be recorded.

### Consensus Evidence

Agreement among multiple team members that the claim is true.

* **Example:** "We all agreed this is how the system behaves."
* **Strength:** Lowest — measures agreement, not truth.
* **Requirement:** Consensus is logged but never used as the sole basis for promotion to fact.

## What Is Not Evidence

The following are explicitly **not** evidence under CDF:

* **Intuition.** A person's gut feeling, no matter how experienced.
* **Hearsay.** "Someone said …" without a verifiable source.
* **Frequency.** "This usually works" — frequency is a claim, not evidence.
* **Authority without source.** "The senior engineer said …" without explaining why.
* **Plausibility.** "It makes sense that …" — plausibility is not evidence.
* **Aesthetic appeal.** "It feels right" — see plausibility.

These can be **starting points** for investigation, but they cannot serve as evidence in a validation chain.

## Combining Evidence

A claim can be supported by multiple pieces of evidence. The combination follows these rules:

* **Independent sources count more.** Two pieces of evidence from independent sources are stronger than two from the same source.
* **Different types count more.** A claim supported by both empirical and documentary evidence is stronger than one supported by two of the same type.
* **Contradictory evidence cannot be ignored.** If even one piece of evidence contradicts a claim, the claim cannot be promoted to a fact until the contradiction is resolved.
* **Recent evidence counts more.** Older evidence may be stale.

## The Evidence Trail

Every fact in the project must have an **evidence trail** — a record of the evidence that supports it. The trail lives in:

* The fact's own document (under a "Evidence" section).
* The corresponding ADR (if the fact was decided architecturally).
* The decision log (`.cognition/memory/history/decision_log.md`) — for chronological traceability.

Removing the evidence trail is a **critical** issue: a fact without evidence is, by CDF's definition, not a fact.

## Related

* `knowledge_theory.md` — where evidence fits in the broader theory.
* `truth_criteria.md` — how evidence leads to truth.
* `confidence_framework.md` — how evidence translates to confidence.
* `validation_protocol.md` — how evidence is collected and recorded.