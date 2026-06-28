# `identity/` — Project Identity

## Purpose

Project identity defines **what the project is and what it must never become**. Every architectural decision, every feature proposal, every line of code should be defensible against these documents.

If you cannot justify an action against the identity documents, the action is probably wrong.

## Structure

```
identity/
├── mission.md         # Why we exist. The single sentence and the paragraph.
├── vision.md          # What success looks like in 5–10 years.
├── principles.md      # Non-negotiable engineering principles.
├── constraints.md     # Hard constraints (regulatory, technical, organizational).
├── philosophy.md      # How we think about software, knowledge, and collaboration.
├── values.md          # Cultural and ethical commitments.
├── non-goals.md       # What we explicitly do NOT do.
└── tradeoffs.md       # Trade-offs we accept and trade-offs we refuse.
```

## Lifecycle

* Identity documents are **near-immutable**.
* Changes require:
  1. A discussion in GitHub Discussions under **Architecture & Design**.
  2. A `meta/` ADR documenting the change (proposed, accepted).
  3. Review by at least two maintainers.
* The latest version always wins. Old versions live in git history.

## Expected Content

Each document answers one question:

| File               | Question                                                                |
|--------------------|-------------------------------------------------------------------------|
| `mission.md`       | Why does this project exist?                                            |
| `vision.md`        | What does success look like in 5–10 years?                              |
| `principles.md`    | Which engineering principles are non-negotiable?                        |
| `constraints.md`   | What constraints (technical, regulatory, organizational) are fixed?     |
| `philosophy.md`    | How do we think about software, knowledge, and collaboration?           |
| `values.md`        | What do we value as a team and a project?                               |
| `non-goals.md`     | What do we explicitly NOT do?                                           |
| `tradeoffs.md`     | Which trade-offs do we accept? Which do we refuse?                      |

## Relationship with AI

The AI must:

1. Load **all** identity documents before making any non-trivial proposal.
2. **Quote** the relevant principle or constraint when justifying a proposal.
3. **Refuse** to propose anything that contradicts the identity.
4. **Flag** contradictions in proposals by linking to identity documents.

---

> *Identity is what the project defends when under pressure.*