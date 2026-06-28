# `reviews/` — Review Reports

## Purpose

Detailed review reports for PRs, design changes, and significant artifacts. The summary lives in `/.cognition/reviewer/review_report.md`; the detailed version lives here.

## File Naming

* `REV-NNN-short-name.md`
* Numbering is monotonic.

## Template

See `0000-template.md`.

## Lifecycle

* Created per PR / change.
* Marked `final` when approved (or merged).
* Not deleted — kept for history.

## AI Behavior

When drafting a review, the AI must:

1. Use the template.
2. Categorize findings by severity.
3. Distinguish **architectural** issues from **style** issues.
4. Propose fixes, not just complaints.

---

> *Reviews are how the project learns in public.*