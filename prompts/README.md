# `prompts/` — AI Prompts

## Purpose

`prompts/` holds the **reusable prompts** that AI assistants (human, hermes, chatgpt, claude, gemini, opencode, future agents) load before acting in a project that uses CDF.

Every prompt is:

* **Self-contained** — does not rely on chat history.
* **Structured** — explicit sections for inputs, outputs, quality criteria, failure conditions.
* **Role-aware** — defines what the AI may and may not do.
* **Stack-agnostic** — works regardless of the project's chosen language.

## Structure

```
prompts/
├── README.md
├── roles/                # Role prompts (who the AI is acting as)
│   ├── README.md
│   ├── planner.md
│   ├── architect.md
│   ├── developer.md
│   ├── reviewer.md
│   ├── curator.md
│   └── researcher.md
└── tasks/                # Task prompts (what the AI is doing)
    ├── README.md
    ├── documentation.md
    ├── testing.md
    ├── bug-fix.md
    ├── refactoring.md
    ├── release.md
    ├── prompt-improvement.md
    └── prompt-review.md
```

## How to Use

A typical prompt invocation combines **one role** with **one or more tasks**:

```
ROLE: prompts/roles/architect.md
TASKS:
  - prompts/tasks/documentation.md
  - prompts/tasks/refactoring.md
CONTEXT:
  - .cognition/identity/
  - .cognition/memory/working/current_context.md
  - .cognition/memory/permanent/
```

## Conventions

* Every prompt file begins with a YAML or `# Header` front-matter.
* Sections are stable and ordered: **Role**, **Inputs**, **Outputs**, **Quality Criteria**, **Failure Conditions**, **Procedure**, **Examples**.
* Prompts are kept in plain Markdown so they can be diffed, reviewed, and versioned.

## AI Behavior

When using these prompts:

1. **Load** the role prompt and the relevant task prompt(s).
2. **Read** the listed context artifacts first.
3. **Produce** outputs that match the template, in the location specified.
4. **Update** the project's `.cognition/memory/working/current_context.md` after working.
5. **Append** to `.cognition/memory/sessions/session_log.md`.

---

> *Prompts are how a project talks to its AI. Make them explicit.*