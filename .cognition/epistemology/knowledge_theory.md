---
title: Knowledge Theory
status: experimental
last_updated: 2026-06-28
owner: epistemology
---

# Knowledge Theory

> What does it mean to "know" something in this project?

This document establishes the project's **theory of knowledge**. It is not a philosophical exercise — it is a working contract that every other artifact in the cognitive layer is expected to honour.

## Why This Document Exists

CDF treats knowledge as a first-class artifact. But "knowledge" can mean many things:

* A fact observed once and never tested.
* An inference derived from past data.
* A model that fits the world as far as we can tell.
* A belief shared by the team without explicit evidence.

Without an explicit theory of knowledge, **all of these are treated as equally valid**. That is dangerous: a fact and a belief collapse into the same category, and decisions are made on unstable ground.

This document fixes the categories.

## Categories of Knowledge

CDF v1.1 distinguishes four categories of knowledge, ordered by strength:

### Observation

A record of something that happened, captured at the time it happened or shortly after.

* **Example:** A bank statement showing a transaction on 2026-06-15.
* **Counter-example:** A summary written three months later that says "there was a transaction in June".

Observations are **time-stamped, source-attributed, and immutable**. Once recorded, an observation cannot be edited — only annotated or superseded by another observation.

### Claim

A statement asserted to be true, supported by one or more observations but not yet validated.

* **Example:** "All transactions before 2026-06-01 were processed in batch."
* **Counter-example:** "I think transactions are usually processed in batch."

Claims are **hypotheses waiting for validation**. They can be promoted to facts or retired.

### Fact

A claim that has been validated against enough independent evidence to be treated as the project's working assumption of truth.

* **Example:** "All transactions before 2026-06-01 are processed in batch" — after three independent observations confirm this and no counter-evidence emerges.
* **Counter-example:** A claim that has only been confirmed by a single source.

Facts are **provisional**. They can be revised if contradictory evidence emerges. The label "fact" describes the **current epistemic status**, not an absolute guarantee.

### Model

A structured abstraction that explains observations and predicts new ones. Models contain many facts and claims linked by relations.

* **Example:** The domain model of a financial ledger.
* **Counter-example:** A list of unrelated facts.

Models are **the highest-level knowledge artifact**. They are also the most fragile — a single falsifying observation may force a model revision.

## What Knowledge Is Not

This is equally important.

* **Knowledge is not data.** Data is the raw substrate; knowledge is what survives after validation, context, and meaning are attached.
* **Knowledge is not documentation.** Documentation may contain knowledge, but it may also contain instructions, references, or examples that are not knowledge claims.
* **Knowledge is not consensus.** A team agreeing on something does not make it true.
* **Knowledge is not expertise.** An expert's intuition is a claim, not a fact, until validated.

## How Knowledge Is Created

Every knowledge artifact in this project is created through one of three paths:

1. **Direct observation.** Someone or something observed an event and recorded it.
2. **Inference.** A reasoning chain produced a new claim or model from existing knowledge.
3. **External import.** Knowledge was obtained from a source outside the project (documentation, research, expert input).

Each path has different **confidence defaults** and different **validation requirements**. See `evidence_model.md` and `confidence_framework.md`.

## How Knowledge Decays

Knowledge is not immortal. It decays when:

* The underlying reality changes (a fact is no longer true).
* The source becomes unreliable (an observation is contradicted).
* A better explanation emerges (a model is superseded).
* The artifact becomes orphaned (no longer referenced, no longer maintained).

Decayed knowledge is not deleted — it is **retired** and moved to history. See `memory/history/`.

## Related

* `evidence_model.md` — what counts as evidence.
* `truth_criteria.md` — when is something "true enough" to act on.
* `confidence_framework.md` — how we assign and revise confidence.
* `uncertainty_handling.md` — how we act under uncertainty.
* `validation_protocol.md` — how we validate claims.
* `kernel/principles.md` — the principles this theory of knowledge must satisfy.