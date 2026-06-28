---
task: release
version: 0.1.0
status: active
pairs_with: [developer, reviewer, curator]
---

# Task: Release

## Mission

Ship a coherent, well-described, well-tested version of the system — with everything required to roll it forward or back.

## Responsibilities

* Produce release notes.
* Update the changelog.
* Tag the release.
* Communicate breaking changes.
* Update the cognitive layer to reflect the released state.

## Inputs (must be read first)

1. The role prompt that scopes this task.
2. `.cognition/identity/mission.md` and `vision.md`.
3. `.cognition/memory/roadmap/roadmap.md`.
4. `.cognition/memory/history/decision_log.md`.
5. Recent ADRs (`knowledge/architecture-decisions/`).
6. `.cognition/curator/lessons_learned.md`.
7. All PRs merged since the last release.

## Outputs

* Updated `CHANGELOG.md`.
* Release notes (in `docs/releases/` or GitHub Release).
* Updated `.cognition/memory/roadmap/roadmap.md` and `milestones.md`.
* Updated `.cognition/memory/history/project_timeline.md`.
* Tag (e.g. via git).
* A note in `.cognition/memory/sessions/session_log.md`.

## Quality Criteria

* Every change since the last release is categorized (added / changed / fixed / removed / security / deprecated).
* Breaking changes are **highlighted** with a clear migration path.
* Versioning follows semantic versioning.
* The release notes are written for **users**, not just developers.
* The cognitive layer is updated to reflect the released state.

## Failure Conditions

You must stop and ask if:

* There are unreleased changes that have not been reviewed.
* The version bump does not match the nature of the changes.
* There are open incident reports that block the release.
* A migration path is missing for a breaking change.

## Procedure

1. Read the inputs.
2. Collect merged PRs since the last release.
3. Categorize each change.
4. Determine the version bump.
5. Draft release notes.
6. Update `CHANGELOG.md`.
7. Update `.cognition/memory/history/project_timeline.md` and `roadmap.md`.
8. Tag the release.
9. Announce (GitHub Release, internal channels).

## Versioning (Semantic Versioning)

| Change Type                    | Bump            | Example       |
|--------------------------------|-----------------|---------------|
| Incompatible API change        | `MAJOR`         | 1.x → 2.0     |
| Backwards-compatible feature   | `MINOR`         | 1.x → 1.5     |
| Backwards-compatible bug fix   | `PATCH`         | 1.4.x → 1.4.2 |
| Pre-release                    | `pre-release`   | 2.0.0-rc.1    |
| Build metadata                 | `build`         | 1.0.0+exp.sha |

## Release Notes Template

```markdown
# Release vX.Y.Z — YYYY-MM-DD

## Highlights

* …

## Added

* …

## Changed

* …

## Fixed

* …

## Removed

* …

## Security

* …

## Deprecated

* …

## Migration Guide

* (only for breaking changes)

## Acknowledgements

* (contributors)
```

## Examples of Good Behavior

* "I have released v1.4.0. The changelog highlights the new reporting API, lists two bug fixes, and includes a migration guide for the removed `legacy.billing.endpoint`."
* "I have updated `.cognition/memory/roadmap/roadmap.md` to reflect that milestone M-002 is now shipped."

## Examples of Bad Behavior (Refuse)

* Releasing without updated changelog.
* Skipping release notes.
* Bumping a major version without a migration guide.

---

> *A release is a contract with users. The notes are the contract.*