# `reflector/` — Reflection Role

## Purpose

The reflector **analyzes completed work** to produce lessons, challenge assumptions, detect recurring patterns, and feed project memory.

The reflector is **about** knowledge. The curator is **of** knowledge. This is the key distinction (per `cdf-improvement-log.md` entry CDF-007):

* **Curator** maintains the cognitive layer — glossary, lessons learned, knowledge updates.
* **Reflector** examines how the cognitive layer was built — the reasoning behind decisions, the assumptions that turned out to be wrong, the patterns that recur across iterations.

## Files

```
reflector/
├── README.md                # This file
├── what_slowed_us.md        # What slowed us down
├── what_surprised_us.md     # What surprised us
├── wrong_assumptions.md     # Which assumptions turned out to be wrong
└── what_should_change.md    # What should change as a result
```

## Lifecycle

| File                    | Lifecycle                                            |
|-------------------------|------------------------------------------------------|
| `what_slowed_us.md`     | Append-mostly; reorganized periodically.             |
| `what_surprised_us.md`  | Append-mostly; reorganized periodically.             |
| `wrong_assumptions.md`  | Append-mostly; cross-referenced from identity.       |
| `what_should_change.md` | Append-mostly; promoted into concrete actions.       |

## Inputs

* Iteration retrospectives (per `workflows/knowledge/retrospective.md`).
* ADR history (`knowledge/architecture-decisions/`).
* Reasoning chains (`.cognition/memory/permanent/reasoning/`).
* Decision log (`.cognition/memory/history/decision_log.md`).
* Recent session logs.
* Lessons learned (`.cognition/curator/lessons_learned.md`).

## Outputs

* Entries in the four reflection files.
* Proposed changes to other roles' artifacts (the reflector proposes, the role decides).
* Updates to epistemics (per `.cognition/epistemology/`) when the reflection surfaces a calibration issue.
* **Proposals to `cdf-improvement-log.md`** when the reflection surfaces a structural issue with CDF itself.

## Relationship with the Curator

The reflector and curator are **complementary**:

* The reflector asks: "What does our work tell us about how we think?"
* The curator asks: "How should we record what we know?"

Reflection produces **observations**. Curation turns observations into **durable knowledge**.

## How the Reflector Is Different from a Retrospective

A retrospective captures one event (an iteration, milestone, incident). Reflection **connects events** — finding patterns that no single retrospective could reveal.

## Quality Criteria

* Every entry is **specific** — naming what, not just "things went slowly".
* Every entry is **actionable** — pointing to a change, not just an observation.
* Entries use **evidence** — references to retrospectives, ADRs, or reasoning chains.
* Patterns are only declared after appearing in **at least three** different events.

## AI Behavior

When acting as reflector, the AI must:

1. Read all recent retrospectives and reasoning chains.
2. Look for **patterns across** them — not just summaries of one.
3. Distinguish **what happened** from **what we think caused it**.
4. Refuse to draw conclusions without evidence.
5. Promote durable findings to:
   * `curator/lessons_learned.md` if they are actionable.
   * `cdf-improvement-log.md` if they affect CDF itself.
   * Epistemics if they affect calibration.

---

> *A project that never reflects is a project that makes the same mistakes with more confidence.*