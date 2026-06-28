---
title: Review Report
status: draft
last_updated: YYYY-MM-DD
owner: reviewer
pr_or_change: #000
---

# Review Report

> The reviewer's report for a single PR or change. Replaced per review.

## Summary

<!-- A 1–3 sentence summary of the review. -->

**Verdict:** ✅ Approve | 🔄 Request changes | ⛔ Reject

## Context

* **PR / Change:** #XXX — [title]
* **Author:**
* **Slice:** [link]
* **Architecture notes:** [link]

## Findings

### Blockers

* **B-1** — [File:Line] — [Description]
  * **Why it blocks:** …
  * **Suggested fix:** …

### Major

* **M-1** — [File:Line] — [Description]
  * **Principle / ADR / invariant violated:** …
  * **Suggested fix:** …

### Minor

* **m-1** — [File:Line] — [Description]
* **m-2** — …

### Nits

* **n-1** — [File:Line] — [Description]

## Architectural Drift?

* **Yes / No.** If yes, propose an ADR.

## New Technical Debt?

* Logged in `technical_debt.md`?  ☐ Yes — ID TD-XXX ☐ No (justify below).

## Cognitive Layer Impact

* Files updated: ☐ Domain model ☐ System context ☐ Glossary ☐ Invariants ☐ Business rules ☐ ADRs ☐ None

## Test Coverage Assessment

* Lines covered: …%
* Critical paths covered: ☐ Yes ☐ Partial ☐ No

## Security Review

* ☐ N/A
* ☐ Reviewed — no issues
* ☐ Reviewed — issues filed

## Verdict Justification

<!-- Why this verdict. -->

---

> *Reviews protect the project. They also teach.*