# Workflow — Documentation

## Goal

Produce or update documentation that is **correct**, **complete**, **consistent**, and **discoverable**.

## Inputs

* The artifact(s) being documented.
* `.cognition/identity/principles.md`.
* `.cognition/memory/permanent/glossary.md`.
* ADRs related to the artifact.
* The role prompt(s) of the author.
* The task prompt: `prompts/tasks/documentation.md`.

## Outputs

* New or updated Markdown in `docs/`.
* Updated README files.
* Updated `.cognition/` artifacts (if state has changed).
* Changelog entry (when user-visible).
* A note in `.cognition/memory/sessions/session_log.md`.

## Definition of Done

- [ ] The doc has a clear audience (newcomer / user / operator / contributor).
- [ ] Every claim is backed by code, an ADR, or an invariant.
- [ ] Every example compiles / runs (or is marked illustrative).
- [ ] Every term is in the glossary (or is added).
- [ ] The doc is linked from relevant READMEs.

## Responsible Roles

* Any role, depending on the audience.
* **Curator** (for cross-cutting consistency).

## Procedure

### Step 1 — Identify the Audience

| Audience       | Location                              |
|----------------|---------------------------------------|
| Newcomer       | Root `README.md` + `docs/getting-started.md` |
| User           | `docs/guides/`                        |
| Operator       | `docs/guides/operations/`             |
| Contributor    | `docs/guides/development/` + `CONTRIBUTING.md` |
| Architect      | `architecture/` + ADRs                |

### Step 2 — Identify the One Thing

A doc exists to convey **one** thing well. Identify it.

### Step 3 — Write

1. Use the appropriate template (if any).
2. Use the glossary.
3. Cite ADRs and invariants.
4. Verify examples.

### Step 4 — Cross-Link

1. Link from related READMEs.
2. Link to related `.cognition/` artifacts.

### Step 5 — Update the Cognitive Layer

If state has changed (a feature was added, an invariant was introduced), update the corresponding `.cognition/` artifact.

### Step 6 — Announce

Append a session note.

## Anti-Patterns (Refuse)

* Docs that lie.
* Docs that document future features as if shipped.
* Docs with no audience in mind.

---

> *Documentation is how a future contributor knows what was true.*