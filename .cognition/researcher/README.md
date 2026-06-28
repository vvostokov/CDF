# `researcher/` — Research Role

## Purpose

The researcher investigates **unknowns**. The researcher:

* Captures research questions and findings.
* Runs spikes and experiments to validate or reject hypotheses.
* Documents dead ends so they aren't repeated.
* Feeds research outputs into architectural decisions, backlog items, or lessons learned.

The researcher is the project's **scout**.

## Files

```
researcher/
├── README.md            # This file
├── research_notes.md    # Active and archived research notes
└── experiments.md       # Logs of experiments (spikes, benchmarks, prototypes)
```

## Lifecycle

| File                  | Lifecycle                                                |
|-----------------------|----------------------------------------------------------|
| `research_notes.md`   | Append-mostly; promoted to ADRs or retired.              |
| `experiments.md`      | Append-mostly; each entry has a clear verdict.           |

## Inputs

* Decision queue (`.cognition/architect/decision_queue.md`).
* Backlog items flagged for research.
* Open questions in working memory.

## Outputs

* Research notes (this directory).
* Proposed ADRs (when a research finding warrants a decision).
* Backlog updates (when a research finding should be deferred as a feature).
* Lessons learned (`.cognition/curator/lessons_learned.md`).

## Relationship with AI

When acting as **Researcher**, the AI must:

1. State the research question clearly.
2. State the hypothesis.
3. State the method.
4. Time-box the work.
5. Record findings in `research_notes.md` or `experiments.md`.
6. **Never** write production code during a research spike.

## Quality Criteria

* Every note has a status (`open` | `concluded` | `parked`).
* Every experiment has a verdict (`validated` | `rejected` | `inconclusive`).
* Conclusions reference evidence (links, measurements, logs).
* Findings are promoted to ADRs / backlog / lessons — never left dangling.

---

> *Research is how a project learns without paying the full price of failure.*