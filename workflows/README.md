# `workflows/` — Workflows

## Purpose

`workflows/` holds the **end-to-end procedures** that combine roles, tasks, prompts, and templates into a coherent activity.

Every workflow defines:

* **Goal** — what this workflow achieves.
* **Inputs** — what must be available before starting.
* **Outputs** — what is produced.
* **Definition of Done** — a checklist that defines completion.
* **Responsible Roles** — who owns the workflow and who participates.
* **Procedure** — step-by-step instructions.
* **Anti-Patterns** — what to refuse.

## Structure

```
workflows/
├── README.md
├── lifecycle/            # Project-level lifecycle workflows
│   ├── 01-start-new-project.md
│   ├── 02-repository-initialization.md
│   ├── planning.md
│   ├── architecture-design.md
│   └── architecture-review.md
├── engineering/          # Day-to-day engineering workflows
│   ├── feature-development.md
│   ├── implementation.md
│   ├── code-review.md
│   ├── testing.md
│   ├── documentation.md
│   ├── refactoring.md
│   ├── bug-fix.md
│   ├── release.md
│   └── research.md
└── knowledge/            # Knowledge maintenance workflows
    ├── knowledge-update.md
    └── retrospective.md
```

## Naming

* Filenames use kebab-case.
* Lifecycle workflows use a numeric prefix (`01-`, `02-`, …) to preserve ordering.
* Engineering and knowledge workflows use descriptive names.

## How to Use

1. Find the workflow that matches the activity.
2. Read the Goal, Inputs, Outputs, and Definition of Done first.
3. Follow the Procedure.
4. Stop at the first sign of an anti-pattern.
5. If the workflow produces an artifact, file it in the right location (referenced in the workflow).

## How to Modify

* Workflows change via PR.
* Changes are reviewed by at least one maintainer.
* Workflow changes are announced under **Knowledge & Process** in Discussions.

---

> *Workflows are how the project converts intention into evidence.*