---
title: Invariants
status: active
last_updated: YYYY-MM-DD
---

# Invariants

> Things that **must always be true**. Violating an invariant is a bug, not a refactor.

Each invariant has:

* **ID**
* **Statement** — the thing that must always be true.
* **Scope** — bounded context, module, system.
* **Enforcement** — test / type / runtime assertion / external check.
* **Owner** — who is responsible.
* **Source** — ADR / rule / domain fact.
* **Status** — `enforced` | `unenforced` | `retired`.

---

## INV-001 — [Statement]

* **ID:** INV-001
* **Statement:** [Plain-English sentence.]
* **Scope:**
* **Enforcement:**
  * Unit test: [path]
  * Integration test: [path]
  * Static check: [tool + rule]
  * Runtime assertion: [location]
* **Owner:**
* **Source:** [ADR / domain fact / rule]
* **Status:** `enforced` | `unenforced` | `retired`
* **Last verified:** YYYY-MM-DD

---

## INV-002 — [Statement]

* (same shape)

---

## Unenforced Invariants

<!-- Invariants we know about but do not yet enforce. Each must have a follow-up issue. -->

* **INV-XXX:** … — Follow-up: …

## Retired Invariants

* **INV-YYY:** … — Retired on YYYY-MM-DD because: …

---

> *An invariant without enforcement is a hope.*