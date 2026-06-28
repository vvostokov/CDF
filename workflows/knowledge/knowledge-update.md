# Workflow — Knowledge Update

## Goal

Promote durable findings into permanent knowledge without breaking consistency, and retire stale knowledge without losing history.

## Inputs

* The new / updated / retired knowledge.
* All of `.cognition/`.
* `knowledge/architecture-decisions/`.
* Recent sessions in `.cognition/memory/sessions/session_log.md`.
* Recent retrospectives.
* The role prompt: `prompts/roles/curator.md`.

## Outputs

* Updated `.cognition/memory/permanent/...` files.
* Updated `knowledge/architecture-decisions/` if affected.
* Entry in `.cognition/curator/knowledge_updates.md`.
* Entry in `.cognition/curator/glossary_updates.md` (if glossary changes).
* Entry in `.cognition/curator/lessons_learned.md` (if lesson).
* A note in `.cognition/memory/sessions/session_log.md`.

## Definition of Done

- [ ] The change is reviewed (architect or peer).
- [ ] The change is consistent with existing ADRs and invariants.
- [ ] Cross-references are updated.
- [ ] Index files are updated (e.g. `architectural_decisions.md`).
- [ ] Knowledge update log entry is added.

## Responsible Roles

* **Curator** (primary).
* **Architect** (review for architectural changes).
* **Reviewer** (general review).

## Procedure

### Step 1 — Identify the Knowledge

1. Identify what is **durable** (will be true for years).
2. Identify what is **stale** (no longer true).
3. Identify what is **missing** (should be true but isn't documented).

### Step 2 — Draft the Change

1. For an addition: write the new entry following the template.
2. For an update: write the diff.
3. For a retirement: mark the entry `deprecated` or `retired` (never delete).

### Step 3 — Review

1. Check for contradictions with existing ADRs and invariants.
2. Check cross-references.

### Step 4 — Apply

1. Apply the change to the file.
2. Update index files.
3. Update cross-references.

### Step 5 — Log

Append an entry to `.cognition/curator/knowledge_updates.md`.

## Anti-Patterns (Refuse)

* Silent changes (no log entry).
* Deleting history.
* Identity changes without an ADR.

---

> *Knowledge that ages gracefully is the project's only real asset.*