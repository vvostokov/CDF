---
title: Business Rules
status: active
last_updated: YYYY-MM-DD
---

# Business Rules

> Rules the system must enforce because of the business domain (not because of technology).

Distinguished from **invariants**:

* Invariants are properties of the *system* (e.g. "money is never negative in memory").
* Business rules are properties of the *business* (e.g. "a refund cannot exceed the original charge").

## How to Use

* Each rule has a unique ID, a clear statement, a scope, and an owner.
* Rules can be violated; when they are, the system responds in a defined way (error, exception, compensation).
* Rules are reviewed when the business changes.

## Rules

### BR-001 — [Rule Statement]

* **ID:** BR-001
* **Statement:**
* **Scope:** bounded context
* **Trigger:** (event / action / condition)
* **Response on violation:** (exception / error code / compensation)
* **Owner:**
* **Source:** (issue / ADR / business decision)
* **Tests:** [paths]
* **Last reviewed:** YYYY-MM-DD

### BR-002 — [Rule Statement]

* (same shape)

---

## Recently Changed

* YYYY-MM-DD — BR-XXX — changed because: …

## Deprecated

* YYYY-MM-DD — BR-YYY — retired because: …

---

> *Business rules are how the system remembers the business.*