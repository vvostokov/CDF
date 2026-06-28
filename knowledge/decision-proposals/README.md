# `decision-proposals/` — Decision Proposals

## Purpose

A **lighter** entry point than an ADR. Decision proposals (DPs) capture the question, the context, the proposed decision, and the rationale, before the full ADR is written.

If the proposal is **accepted**, it is promoted to an ADR (`knowledge/architecture-decisions/NNNN-*.md`) and the DP is marked `accepted` and linked.

If the proposal is **rejected**, it is archived with reasoning.

## File Naming

* `DP-NNN-short-name.md`
* Numbering is monotonic.

## Template

See `0000-template.md` in this directory.

## Lifecycle

| Status     | Meaning                                                  |
|------------|----------------------------------------------------------|
| `proposed` | Submitted for discussion.                                |
| `accepted` | Promoted to an ADR; link to that ADR.                    |
| `rejected` | Not adopted; reasoning recorded.                         |
| `superseded`| A newer proposal replaces this one.                      |

## AI Behavior

When drafting a proposal, the AI must:

1. Use the template.
2. Cite the relevant principles and constraints.
3. Identify alternatives explicitly.
4. **Refuse** to skip the alternatives section.

---

> *Proposals make decisions discussable. ADRs make decisions durable.*