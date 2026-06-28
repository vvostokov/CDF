# `architecture-decisions/` — ADRs

## Purpose

This directory holds the **full text** of every Architectural Decision Record (ADR).

`/.cognition/memory/permanent/architectural_decisions.md` is the index. The files here are the substance.

## Format

* File naming: `NNNN-kebab-case-title.md`
* Numbering is monotonic; numbers are never reused.
* Status is one of: `proposed` | `accepted` | `rejected` | `superseded`.

## Lifecycle of an ADR

1. **Proposed** — written as `NNNN-*.md` with status `proposed`.
2. **Discussed** — in Discussions / PR.
3. **Accepted** or **Rejected** — status updated; the file stays for history.
4. **Superseded** — a new ADR references the old one in its `supersedes` field.

## Template

See `0000-template.md` in this directory.

---

> *The list of decisions is the architecture. The motivation for each decision is its soul.*