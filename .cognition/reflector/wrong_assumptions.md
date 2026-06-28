---
title: Wrong Assumptions
status: active
last_updated: YYYY-MM-DD
owner: reflector
---

# Wrong Assumptions

> Assumptions we held that turned out to be incorrect.

Assumptions are **invisible** until they break. When they break, we record them here so future contributors can see what we once believed and why we revised it.

## What Goes Here

Each entry has:

* **Date** — when the assumption was found to be wrong.
* **Assumption** — what we believed.
* **Source** — where the assumption came from (a document, an ADR, a domain expert, a common belief).
* **What broke** — what event or evidence proved it wrong.
* **What we did** — how we responded.
* **Revised assumption** — what we believe now.
* **Lesson** — what we should do differently.

## Entries

<!-- Newest at top. -->

### YYYY-MM-DD — [Title]

* **Assumption:**
* **Source:**
* **What broke:**
* **What we did:**
* **Revised assumption:**
* **Lesson:**
* **Linked:** [ADR / decision / reasoning chain]

---

## Relationship with Identity

Wrong assumptions may force revisions to:

* `.cognition/identity/assumptions.md` (if it exists in the project)
* `.cognition/processes/architect/domain_model.md`
* `.cognition/processes/architect/system_context.md`
* `.cognition/memory/permanent/invariants.md`
* `.cognition/memory/permanent/business_rules.md`

Each revision must follow the relevant update workflow.

## Why This File Matters

A list of wrong assumptions is **embarrassing** — and therefore valuable. It is hard to maintain because it requires admitting mistakes. But it is one of the most useful files in the cognitive layer: it shows future contributors that the project has actually **learned**, not just **recorded**.

## Calibration

If a wrong assumption was held with high confidence for a long time, this is a strong signal of miscalibration. Reflect on:

* Why was the assumption trusted?
* What evidence was missing?
* How did we miss it?

Record the reflection in `cdf-improvement-log.md` if it suggests a structural improvement.

---

> *The list of wrong assumptions is the most honest document the project produces.*