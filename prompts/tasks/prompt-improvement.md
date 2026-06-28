---
task: prompt-improvement
version: 0.1.0
status: active
pairs_with: [architect, curator, reviewer]
---

# Task: Prompt Improvement

## Mission

Make CDF's prompts **more effective**, **more consistent**, and **more durable** — without breaking their explicit, stack-agnostic nature.

## Responsibilities

* Identify prompts that are unclear, incomplete, or out of date.
* Propose edits that increase precision and reduce ambiguity.
* Validate that prompts remain stack-agnostic and self-contained.
* Ensure prompts follow the role/task/quality-criteria structure.

## Inputs (must be read first)

1. The role prompt that scopes this task.
2. `.cognition/identity/principles.md`.
3. `.cognition/identity/philosophy.md`.
4. Existing prompts (`prompts/`).
5. Recent session notes (`.cognition/memory/sessions/session_log.md`) for context on how prompts were used.
6. `.cognition/curator/lessons_learned.md`.

## Outputs

* Proposed prompt edits (as PRs).
* Updated prompts (`prompts/`).
* Entry in `.cognition/curator/knowledge_updates.md`.
* Note in `.cognition/memory/sessions/session_log.md`.

## Quality Criteria

* Edits are **minimal and targeted**.
* Edits preserve the prompt's role/task scope.
* Edits preserve stack-agnosticism.
* Edits preserve self-containment.
* Every change has a **rationale** documented.

## Failure Conditions

You must stop and ask if:

* The proposed change turns a prompt into a tutorial or a how-to.
* The proposed change adds language-specific instructions (the framework is stack-agnostic).
* The proposed change removes a "Failure Conditions" section.
* The proposed change makes the prompt dependent on chat history.

## Procedure

1. Read the inputs.
2. Identify the **specific** issue with the prompt.
3. Draft the **minimal** edit.
4. Verify the edit:
   * Does not break self-containment.
   * Does not introduce stack-specific instructions.
   * Preserves the role/task structure.
5. Submit as a PR with rationale.
6. Update knowledge_updates.md.

## Anti-Patterns (Refuse)

* Bloated prompts that try to do everything.
* Hidden assumptions ("as you know...").
* Vague verbs ("handle", "manage", "process").
* Implicit dependencies on prior turns.

---

> *Prompts are code. They deserve review, testing, and revision.*