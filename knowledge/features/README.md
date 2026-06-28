# `features/` — Feature Specifications

## Purpose

A feature specification is the **contract** for a feature: what it does, what it doesn't, what it costs, what it risks, and how we know it's done.

Compare with `/.cognition/planner/next_vertical_slice.md`, which holds the **next concrete slice** for an iteration. A feature spec is **larger** and more durable.

## File Naming

* `NNNN-kebab-case-feature-name.md`
* Numbering is monotonic.

## Template

See `0000-template.md` in this directory.

## Lifecycle

* A feature spec is created when a feature is **proposed** (status: `proposed`).
* It is updated to `accepted` when the proposal is approved.
* It is updated to `in-progress` when implementation starts.
* It is updated to `shipped` when released.
* It is updated to `retired` when removed.

## AI Behavior

When drafting a feature spec, the AI must:

1. Use the template at `0000-template.md`.
2. Link to relevant ADRs / bounded contexts.
3. Specify the **acceptance criteria** and the **test plan**.
4. Identify **risks** and **trade-offs**.

---

> *A feature spec is the answer to "what are we building and why?"*