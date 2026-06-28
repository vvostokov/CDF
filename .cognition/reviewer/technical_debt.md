---
title: Technical Debt Ledger
status: active
last_updated: YYYY-MM-DD
owner: reviewer
---

# Technical Debt Ledger

> A live, prioritized list of known technical debt. Updated continuously.

Debt is not a sin. Hidden debt is.

## How to Use This

* When you find debt, add an entry.
* When you fix debt, mark it resolved and link the PR.
* When you decide to live with debt forever, mark it `accepted` and explain why.
* Priority is `critical` | `high` | `medium` | `low`.

## Active Debt

### TD-001 — [Title]

* **Location:** `src/...` / `tests/...` / `knowledge/...`
* **Type:** `code` | `test` | `documentation` | `architecture` | `process`
* **Description:**
* **Why it is debt:**
* **Impact if not fixed:**
* **Estimated effort:** S / M / L / XL
* **Priority:** `low` | `medium` | `high` | `critical`
* **Owner:**
* **Linked issue / ADR:**
* **Created:** YYYY-MM-DD
* **Status:** `open` | `accepted` | `in-progress` | `resolved`

### TD-002 — [Title]

* (same shape)

<!-- Repeat. -->

## Recently Resolved

### TD-000 — [Title]

* **Resolved:** YYYY-MM-DD
* **Resolution PR:** #XXX
* **One-line summary of fix:**

## Accepted (Living With)

### TD-XXX — [Title]

* **Status:** `accepted`
* **Reason for accepting:**

---

> *Pay debt like taxes. Regular small payments, not a one-time lump sum.*