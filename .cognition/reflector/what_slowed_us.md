---
title: What Slowed Us Down
status: active
last_updated: YYYY-MM-DD
owner: reflector
---

# What Slowed Us Down

> Specific things that made us slower than we could have been.

This file is **not** a complaint log. It is a record of **causes** — what specifically slowed the project, why it slowed it, and what can be done about it.

## What Goes Here

Each entry has:

* **Date** — when the slowdown was observed.
* **Context** — what the project was doing.
* **Slowdown** — what specifically took longer than expected.
* **Root cause** — why it happened.
* **Magnitude** — rough estimate of the cost (hours, days, iterations).
* **Fix** — what we did or should do.
* **Pattern?** — does this repeat?

## Entries

<!-- Newest at top. -->

### YYYY-MM-DD — [Title]

* **Context:**
* **Slowdown:**
* **Root cause:**
* **Magnitude:**
* **Fix:**
* **Pattern:** yes / no / unconfirmed
* **Linked:** [retrospective / ADR / lesson learned]

---

## What Does Not Go Here

* Generic complaints ("things were hard").
* Slowdowns with no clear cause.
* Personal performance issues (use private feedback, not the cognitive layer).

## How Entries Are Promoted

* A **pattern** (3+ repetitions) is promoted to `what_should_change.md` as a concrete action.
* A **root cause in CDF itself** is logged in `cdf-improvement-log.md`.
* A **lesson** for future projects is added to `curator/lessons_learned.md`.

---

> *Slowdowns are symptoms. Root causes are diagnoses. Diagnose, don't just record.*