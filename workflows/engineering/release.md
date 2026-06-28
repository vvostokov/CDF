# Workflow — Release

## Goal

Ship a coherent, well-described, well-tested version of the system — with everything required to roll it forward or back.

## Inputs

* All merged PRs since the last release.
* `.cognition/identity/mission.md`, `vision.md`, `principles.md`.
* `.cognition/memory/roadmap/roadmap.md`.
* `.cognition/memory/history/decision_log.md`.
* Recent ADRs (`knowledge/architecture-decisions/`).
* `.cognition/curator/lessons_learned.md`.
* The role prompt: depends on the release type.
* The task prompt: `prompts/tasks/release.md`.

## Outputs

* Updated `CHANGELOG.md`.
* Release notes (in `docs/releases/` or GitHub Release).
* Updated `.cognition/memory/roadmap/roadmap.md` and `milestones.md`.
* Updated `.cognition/memory/history/project_timeline.md`.
* A tag (e.g. `git tag vX.Y.Z`).
* A note in `.cognition/memory/sessions/session_log.md`.

## Definition of Done

- [ ] All merged PRs since the last release are categorized.
- [ ] Version bump matches the nature of the changes (semver).
- [ ] Breaking changes are highlighted with a migration guide.
- [ ] Release notes are written for **users**.
- [ ] `CHANGELOG.md` is updated.
- [ ] `.cognition/memory/roadmap/roadmap.md` is updated.
- [ ] `.cognition/memory/history/project_timeline.md` is updated.
- [ ] Tag is created.
- [ ] GitHub Release is published.

## Responsible Roles

* **Planner** (primary) — owns the release schedule.
* **Developer** — produces release artifacts.
* **Reviewer** — verifies release readiness.
* **Curator** — updates cognitive layer.

## Procedure

### Step 1 — Collect

1. List all PRs merged since the last release.
2. Categorize: added / changed / fixed / removed / security / deprecated.

### Step 2 — Bump Version

| Change                | Bump        |
|-----------------------|-------------|
| Incompatible API      | MAJOR       |
| Backwards-compat new  | MINOR       |
| Backwards-compat fix  | PATCH       |

### Step 3 — Draft Release Notes

Use the template in `prompts/tasks/release.md`.

### Step 4 — Update Cognitive Layer

1. Update `CHANGELOG.md`.
2. Update `.cognition/memory/roadmap/roadmap.md`.
3. Update `.cognition/memory/roadmap/milestones.md` (close the relevant milestone).
4. Update `.cognition/memory/history/project_timeline.md`.

### Step 5 — Tag

`git tag -a vX.Y.Z -m "Release vX.Y.Z"`.

### Step 6 — Publish

Publish the GitHub Release with notes.

### Step 7 — Announce

Post in Discussions under **Announcements**.

## Anti-Patterns (Refuse)

* Releasing without updated changelog.
* Skipping migration guides for breaking changes.
* Major bumps without justification.

---

> *A release is a contract with users. The notes are the contract.*