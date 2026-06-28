# `reviewer/` — Review Role

## Purpose

The reviewer ensures **architectural integrity**, **quality**, and **alignment with identity**. The reviewer looks for:

* Architectural drift (changes that violate the model, ADRs, or invariants).
* Quality regressions (poor naming, missing tests, brittle code).
* Cognitive-layer inconsistencies (code that contradicts `.cognition/` or vice versa).
* Technical debt (and records it).

The reviewer is the **last line of defense** before knowledge is lost. The reviewer does not gate personality — they gate consistency.

## Files

```
reviewer/
├── README.md                # This file
├── review_report.md         # The latest consolidated review report
├── architecture_review.md   # Periodic architectural review
└── technical_debt.md        # Known, catalogued technical debt
```

## Lifecycle

| File                    | Lifecycle                                                |
|-------------------------|----------------------------------------------------------|
| `review_report.md`      | Replaced per PR (or appended to `knowledge/retrospectives/` for periodic reviews). |
| `architecture_review.md`| Updated periodically (per milestone).                    |
| `technical_debt.md`     | Append-only ledger of known debt with priority.         |

## Inputs

* The PR / change under review.
* Identity, principles, constraints (`.cognition/identity/`).
* ADRs (`knowledge/architecture-decisions/`).
* Domain model (`.cognition/architect/domain_model.md`).
* Invariants and business rules (`.cognition/memory/permanent/`).
* Implementation plan (`.cognition/developer/implementation_plan.md`).
* `prompts/tasks/code-review.md`.

## Outputs

* Inline comments on the PR.
* `review_report.md` summary for the PR.
* Updates to `technical_debt.md` for new debt.
* Proposals for new ADRs when design drift is detected.

## Relationship with AI

When acting as **Reviewer**, the AI must:

1. Read the PR diff, the linked slice, the relevant ADRs, and the cognitive layer artifacts.
2. Categorize findings by severity (blocker, major, minor, nit).
3. Distinguish **architectural** issues from **style** issues.
4. Propose fixes, not just complaints.
5. **Never** approve a change that contradicts identity without an explicit ADR.

## Quality Criteria

* Every blocker has a clear, actionable fix.
* Every major issue links to a principle, ADR, or invariant.
* Every finding is constructive.
* The review report fits in one screen.

---

> *A good review makes the author *want* to fix things.*