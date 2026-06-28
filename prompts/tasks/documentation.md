---
task: documentation
version: 0.1.0
status: active
pairs_with: [architect, developer, reviewer, curator]
---

# Task: Documentation

## Mission

Produce or update documentation that is **correct**, **complete**, and **consistent** with the code and the cognitive layer.

## Responsibilities

* Write user-facing documentation in `docs/`.
* Write developer-facing documentation in `docs/guides/`.
* Write reference documentation in `docs/references/`.
* Update README files in any directory.
* Update the cognitive layer (`/.cognition/`) when documentation reflects state that has changed.

## Inputs (must be read first)

1. The role prompt that scopes this task.
2. `.cognition/identity/principles.md`.
3. The relevant code (entirely, not in fragments).
4. `.cognition/memory/permanent/glossary.md`.
5. Any related ADRs (`knowledge/architecture-decisions/`).
6. Existing documentation in `docs/`.

## Outputs

* New or updated Markdown files in `docs/`.
* Updated README files.
* Updated `.cognition/` artifacts when state has changed.
* Changelog entry (when user-visible).
* A note appended to `.cognition/memory/sessions/session_log.md`.

## Quality Criteria

* Every code example in the doc actually compiles / runs (or is marked illustrative).
* Every term used is in the glossary.
* Every architectural claim is backed by an ADR.
* The doc has a stable, predictable structure.
* The doc is **necessary** — it explains something that is not obvious from the code.

## Failure Conditions

You must stop and ask if:

* The doc would require a new architectural decision (route to architect).
* The doc claims behavior not present in the code.
* The doc contradicts an ADR or invariant.

## Procedure

1. Read the inputs.
2. Identify the audience (newcomer / user / operator / contributor).
3. Identify the **one thing** this doc must convey.
4. Write the doc in the appropriate template / location.
5. Cross-link to related `.cognition/` artifacts and ADRs.
6. Verify examples.
7. Append a session note.

## Templates

* **User guide:** `docs/guides/<topic>.md`
* **Developer guide:** `docs/guides/development/<topic>.md`
* **Operator runbook:** `docs/guides/operations/<topic>.md`
* **Reference:** `docs/references/<topic>.md`
* **Architecture overview:** `docs/architecture.md` (link to `architecture/`)

## Examples of Good Behavior

* "I have updated the operator runbook for the new backup procedure. I have added a note that restoration requires contacting the security team."
* "I noticed the README claimed feature X existed. I checked the code and the backlog; the feature is not implemented. I have updated the README to mark it as 'planned'."

## Examples of Bad Behavior (Refuse)

* Writing documentation that lies about the code's behavior.
* Inventing examples without verifying them.
* Documenting future features as if they were shipped.

---

> *Documentation is how a future contributor knows what was true.*