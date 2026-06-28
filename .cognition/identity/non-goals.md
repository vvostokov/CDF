---
title: Non-Goals
status: draft
last_updated: YYYY-MM-DD
---

# Non-Goals

> What we explicitly do **not** do — and why.

A non-goal is a **deliberate refusal**. It is not "we don't have time yet". It is "we have decided not to do this, even if we have time".

Non-goals are how a project protects its focus. They are not a list of weaknesses; they are a list of **disciplined abstentions**.

---

## How to Use This Document

* Every feature proposal must be checked against the non-goals.
* If a proposal falls under a non-goal, the answer is **no** unless an ADR explicitly accepts the scope expansion.
* This document is not exhaustive. The absence of something here does not mean it is in scope.

---

## Non-Goals

### NG-1 — [Name]

* **Statement:** We do not ….
* **Reason:** ….
* **Implication:** ….

### NG-2 — [Name]

* **Statement:** We do not ….
* **Reason:** ….
* **Implication:** ….

<!-- Repeat as needed. -->

---

## Common Patterns That Look Like Goals but Are Non-Goals

| Pattern                          | Why it is a non-goal                                       |
|----------------------------------|------------------------------------------------------------|
| Becoming a framework             | We are a product; we do not compete with frameworks.       |
| Supporting every platform        | We focus on platforms that meet constraints.               |
| Building a UI for every persona  | We optimize for primary personas; others can be served later. |
| Custom auth in the first year    | We use proven solutions until proven insufficient.         |
| Multi-tenancy from day one       | Not until we have a concrete second tenant.                |

---

## Related

* `mission.md` — why we exist.
* `tradeoffs.md` — what we give up.
* `principles.md` — what we always do.