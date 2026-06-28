---
title: Architectural Decisions (Index)
status: active
last_updated: YYYY-MM-DD
---

# Architectural Decisions — Index

> A chronological index of every accepted architectural decision. Full text lives in `knowledge/architecture-decisions/`.

## How This Works

* Every accepted decision lives in `knowledge/architecture-decisions/NNNN-title.md`.
* This file is the **table of contents**.
* Each row links to the ADR and summarizes it in one line.
* When an ADR supersedes another, the row links both.

## Index

| Number | Title                                          | Status          | Date         | Supersedes | Superseded by |
|--------|------------------------------------------------|-----------------|--------------|------------|---------------|
| 0000   | [Adopt CDF as the project's cognitive layer]   | `accepted`      | YYYY-MM-DD   | —          | —             |
|        |                                                |                 |              |            |               |

<!-- Newest at the top of the table for readability; or oldest at the top if chronological order is preferred. -->

## Recently Accepted

* `ADR-NNNN` — title — accepted YYYY-MM-DD

## Recently Proposed (Awaiting Decision)

* `ADR-NNNN` — title — proposed YYYY-MM-DD by …

## Recently Superseded

* `ADR-NNNN` — superseded by `ADR-MMMM` on YYYY-MM-DD

## Recently Rejected

* `ADR-NNNN` — rejected on YYYY-MM-DD — reason: …

---

## Conventions

* ADR numbers are zero-padded to 4 digits (`0001`, `0002`, …) and never reused.
* Filenames use kebab-case: `0001-adopt-cdf.md`.
* The full text uses the ADR template in `knowledge/architecture-decisions/` or `knowledge/architecture-decisions/README.md`.

---

> *Decisions made without writing them down aren't decisions — they're habits.*