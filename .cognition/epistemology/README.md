---
title: Epistemology — README
status: experimental
last_updated: 2026-06-28
---

# `epistemology/` — How This Project Knows

> The epistemic layer of CDF. Defines what counts as knowledge, evidence, truth, confidence, uncertainty, and validation.

This directory answers the question that `identity/` and `kernel/` cannot: **how does this project decide what is true?**

## Purpose

Without an explicit epistemic layer, a project treats all claims as equally valid. That is dangerous. Epistemology gives the project a **shared vocabulary** for talking about knowledge and a **shared procedure** for validating claims.

This is the layer that CDF v1.0 was missing. It was added in CDF v1.1 in response to log entry CDF-002.

## Structure

```
epistemology/
├── README.md               # This file
├── knowledge_theory.md     # What is knowledge (vs. data, documentation, belief)
├── evidence_model.md       # What counts as evidence (and what does not)
├── truth_criteria.md       # When is something "true enough" to act on
├── confidence_framework.md # How we assign and revise confidence (0.0–1.0)
├── uncertainty_handling.md # How we act under uncertainty
└── validation_protocol.md  # Operational validation procedure
```

## Lifecycle

The epistemology layer is **near-immutable**, similar to `kernel/`. Changes to any document here require:

1. A discussion under `Knowledge & Process` in GitHub Discussions.
2. An ADR (`knowledge/architecture-decisions/`) explaining the change.
3. Review by at least two maintainers.

The reason: epistemology defines how the project reasons. Changing it without ceremony is changing how every other decision is made.

## Conceptual Placement

This layer conceptually belongs to **Knowledge** in the Knowledge / Processes distinction. It is **static** — it does not transform itself; it provides the framework within which transformations happen.

## Relationship with Other Layers

| Layer                | Relationship                                              |
|----------------------|-----------------------------------------------------------|
| `kernel/`            | Kernel provides principles; epistemology operationalizes them. |
| `identity/`          | Identity answers "who we are"; epistemology answers "how we know". |
| `memory/`            | Memory stores knowledge artifacts; epistemology defines what counts. |
| `processes/`         | Processes transform knowledge; epistemology governs how those transformations are validated. |
| `reflector/`         | Reflector uses epistemology to audit its own reasoning. |

## How to Use

* When introducing a new claim, consult `evidence_model.md` and `truth_criteria.md`.
* When assigning confidence, use the bands in `confidence_framework.md`.
* When acting under uncertainty, follow the decision rules in `uncertainty_handling.md`.
* When validating a claim formally, follow the workflow in `validation_protocol.md`.

## Status

**Experimental.** This layer was added in CDF v1.1 based on the architectural work that produced Zhamlik, ReflectWise, and AI_OS designs. It has not yet been validated against a real CDF project in production. Improvements will be accepted only via `cdf-improvement-log.md` entries.

---

> *A project that does not know how it knows will eventually stop knowing what it knows.*