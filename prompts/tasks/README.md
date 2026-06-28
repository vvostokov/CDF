# Task Prompts

## Purpose

A **task prompt** defines what the AI is doing. It pairs with a role prompt to produce specific artifacts.

## Available Tasks

| Task               | Prompt                                          | Produces                                              |
|--------------------|-------------------------------------------------|-------------------------------------------------------|
| Documentation      | [`documentation.md`](./documentation.md)        | Docs in `docs/`, updates to `/.cognition/`            |
| Testing            | [`testing.md`](./testing.md)                    | Test plans, test code, coverage assessments           |
| Bug Fix            | [`bug-fix.md`](./bug-fix.md)                    | Root-cause analysis, regression tests, fix            |
| Refactoring        | [`refactoring.md`](./refactoring.md)            | Behavior-preserving code changes, debt payment        |
| Release            | [`release.md`](./release.md)                    | Release notes, version bumps, changelog               |
| Prompt Improvement | [`prompt-improvement.md`](./prompt-improvement.md) | Edits to `prompts/`                                |
| Prompt Review      | [`prompt-review.md`](./prompt-review.md)        | Critical review of an existing prompt                 |

## How to Use

Pick one or more tasks; pair with a role prompt. Each task prompt assumes:

* The role prompt has already been loaded.
* The context artifacts have been read.

## Refusing a Task

If a task is **outside the role's mandate**, the AI must:

1. State the conflict.
2. Recommend the correct role.
3. Stop.

---

> *Tasks are what gets done. Roles are who does it.*