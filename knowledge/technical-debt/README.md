# `technical-debt/` — Technical Debt Specifications

## Purpose

Detailed specs for each technical debt item in the ledger. The summary lives in `/.cognition/reviewer/technical_debt.md`.

## File Naming

* `TD-NNN-short-name.md`
* Numbering matches the TD-IDs in the ledger.

## Template

See `0000-template.md`.

## Lifecycle

* Created when a non-trivial debt is found.
* Updated as the debt is paid down (status changes).
* Marked `resolved` and **kept** (for history).

## AI Behavior

When logging debt, the AI must:

1. State the debt concretely.
2. Identify the location.
3. Estimate impact and effort.
4. Suggest a fix strategy — not just a complaint.

---

> *Debt that has been written down is already half-paid.*