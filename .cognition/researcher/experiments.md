---
title: Experiments
status: active
last_updated: YYYY-MM-DD
owner: researcher
---

# Experiments Log

> A log of spikes, prototypes, and benchmarks — anything we built temporarily to learn something.

Each experiment has a **verdict** and a **disposition** (keep / throw away / promote).

## Active Experiments

### E-001 — [Title]

* **Date opened:** YYYY-MM-DD
* **Goal:**
* **Hypothesis:**
* **Setup:**
* **Result so far:**
* **Status:** `running`
* **Owner:**

---

## Concluded Experiments

### E-000 — [Title]

* **Date opened:** YYYY-MM-DD
* **Date concluded:** YYYY-MM-DD
* **Goal:**
* **Hypothesis:**
* **Method:**
* **Measurements:**
* **Verdict:** `validated` | `rejected` | `inconclusive`
* **Disposition:** `thrown-away` | `promoted-to-feature` | `promoted-to-ADR` | `archived`
* **Linked:** [research note, ADR, issue]

---

## Notes

* Throw-away code is **expected**. Don't keep dead code in `src/`.
* Capture the **measurement**, not just the conclusion. Conclusions age; numbers re-evaluate.
* An inconclusive experiment is still valuable. Record the data and move on.

---

> *Every experiment should reduce uncertainty. If it didn't, ask why.*