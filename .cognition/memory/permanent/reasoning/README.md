---
title: Reasoning Memory — README
status: experimental
last_updated: 2026-06-28
---

# `memory/permanent/reasoning/` — Saved Chains of Thought

> Architectural reasoning, preserved independently of the decisions it produced.

This directory was added in CDF v1.1 in response to log entry CDF-004. The problem it solves: a future contributor could find the final architectural decision but not the **chain of reasoning** that produced it.

## Purpose

When an architect writes "we chose event sourcing because …", the conclusion is preserved in an ADR. The reasoning — the alternatives considered, the doubts raised, the predictions made, the trade-offs accepted — is often lost.

This directory preserves **chains of reasoning** as standalone artifacts, separate from the decisions they led to.

## What Lives Here

Each file is a **reasoning chain** — a saved line of thought that led (or could have led) to one or more decisions. Chains may be:

* **Closed** — the reasoning concluded and produced a decision.
* **Open** — the reasoning is still in progress.
* **Abandoned** — the reasoning concluded in a different direction than originally expected.

The directory is **append-mostly**. Chains are added; existing chains are not edited except for clarity.

## File Naming

* `YYYY-MM-DD-kebab-case-title.md`
* The date is when the chain began, not when it concluded.
* The title is short and descriptive.

## File Template

Each reasoning chain includes:

* **Title** — what was being reasoned about.
* **Date opened** — when the chain began.
* **Status** — `open` | `closed` | `abandoned`.
* **Context** — what triggered the reasoning.
* **Reasoning** — the actual chain of thought, step by step.
* **Alternatives considered** — what was rejected and why.
* **Decisions produced** — links to ADRs or decision log entries.
* **Confidence at the time** — what was the team's confidence in the conclusion.
* **What we did not know** — explicit list of unknowns.
* **Predictions** — what we expected to be true as a result.
* **Validation results** — later, when evidence comes in, what we actually found.

## When to Write a Reasoning Chain

Write one when:

* A non-trivial architectural decision is being considered.
* A trade-off has multiple defensible answers.
* The reasoning took more than a single conversation to converge.
* The decision may be revisited in the future.

Do not write one for:

* Trivial decisions.
* Decisions that are clearly mandated by constraints.
* Decisions whose reasoning is fully captured in an ADR.

## Relationship with ADRs

ADRs record **decisions**. Reasoning chains record **reasoning**. They are complementary:

* An ADR may reference a reasoning chain for full context.
* A reasoning chain may reference an ADR for the final outcome.
* The reasoning chain is preserved even after the ADR is superseded, because the reasoning itself may still be useful.

## Relationship with Architecture Notes

`processes/architect/architecture_notes.md` is the architect's **active scratchpad** — short notes, hypotheses, dead ends. Reasoning chains here are **finished or substantial** — long enough and structured enough to be referenced later.

Move content from architecture_notes.md to a reasoning chain when:

* The reasoning spans more than a few notes.
* The reasoning is expected to lead to a decision.
* The reasoning should survive the current iteration.

## Related

* `cdf-improvement-log.md` — entry CDF-004 (the original friction this directory addresses).
* `.cognition/processes/architect/architecture_notes.md` — active scratchpad.
* `.cognition/memory/history/decision_log.md` — chronological decision log.
* `knowledge/architecture-decisions/` — formal ADRs.