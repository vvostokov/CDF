# `invariants/` — Invariant Specifications

## Purpose

Each invariant has its **own file** with full detail: statement, rationale, violation scenarios, and **enforcement strategy**.

The summary in `/.cognition/memory/permanent/invariants.md` is for orientation. The files here are for verification.

## File Naming

* `INV-NNN-short-name.md`
* Numbering matches the INV-IDs in the summary.

## Template

See `0000-template.md` in this directory.

## Lifecycle

* Created when an invariant is introduced (typically tied to an ADR).
* Updated when enforcement strategy changes.
* Marked `retired` (not deleted) when no longer needed.

## AI Behavior

When creating or reviewing an invariant file, the AI must:

1. State the invariant in one sentence.
2. Identify the enforcement mechanism.
3. Link to the tests that prove it.
4. Distinguish **enforced** from **unenforced** status.

---

> *An invariant is a law. It deserves its own courtroom.*