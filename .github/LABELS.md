# GitHub Labels Recommendation

CDF projects benefit from a **small, stable label taxonomy**. The set below is the recommended default for any project using this template. Adjust names to fit your existing repo, but try to keep semantics.

## Categories

### Type — *what is this?*

| Label            | Color     | Description                                    |
|------------------|-----------|------------------------------------------------|
| `bug`            | `#d73a4a` | Something is broken or behaves incorrectly.    |
| `feature`        | `#a2eeef` | New user-visible capability.                   |
| `enhancement`    | `#84b6eb` | Improvement to existing capability.            |
| `documentation`  | `#0075ca` | Docs, READMEs, knowledge updates.              |
| `refactor`       | `#fbca04` | Code change with no behavior change.           |
| `test`           | `#bfdadc` | Test-only change.                              |
| `ci`             | `#e4e669` | CI / tooling / automation.                     |
| `security`       | `#b60205` | Security issue or hardening.                   |
| `performance`    | `#f9a825` | Performance investigation or fix.              |

### Cognitive Layer — *where in the framework does it live?*

| Label               | Color     | Description                                       |
|---------------------|-----------|---------------------------------------------------|
| `architecture`      | `#5319e7` | Affects `.cognition/architect/` or architecture/. |
| `decision`          | `#1d76db` | Requires or references an ADR.                    |
| `knowledge`         | `#0e8a16` | Touches `.cognition/memory/`, `knowledge/`.       |
| `curation`          | `#c2e0c6` | Glossary, invariants, lessons learned updates.    |
| `research`          | `#d4c5f9` | Research, experiments, spikes.                    |
| `planning`          | `#fef2c0` | Planner artifacts (goal, iteration, backlog).      |
| `documentation-cog` | `#bfd4f2` | Documentation about the cognitive layer.          |

### Status — *where is it in the workflow?*

| Label                | Color     | Description                                       |
|----------------------|-----------|---------------------------------------------------|
| `needs-triage`       | `#ededed` | Awaiting first review.                            |
| `needs-review`       | `#fbca04` | Awaiting review (architect or technical).         |
| `blocked`            | `#b60205` | Cannot progress (waiting on something).           |
| `in-progress`        | `#0e8a16` | Actively being worked on.                         |
| `ready-for-release`  | `#006b75` | Approved and queued for the next release.         |
| `wontfix`            | `#ffffff` | Will not be addressed (closed without action).    |
| `duplicate`          | `#cfd3d7` | Duplicates an existing issue.                     |

### Priority — *how urgent?*

| Label       | Color     | Description                       |
|-------------|-----------|-----------------------------------|
| `priority/critical` | `#b60205` | Production down or data loss risk. |
| `priority/high`     | `#d93f0b` | Blocking, urgent.                |
| `priority/medium`   | `#fbca04` | Important but not urgent.        |
| `priority/low`      | `#0e8a16` | Nice to have.                    |

### Scope — *bounded context or area*

These are project-specific. Each project should define a small set (≤ 10) describing its main bounded contexts or subsystems, e.g. `scope/billing`, `scope/identity`, `scope/api`.

## Conventions

* Use **Type**, **Cognitive Layer**, and **Status** labels on every issue and PR.
* Use **Priority** labels sparingly — most issues should not be `priority/critical`.
* Use **Scope** labels to filter by area of the codebase.
* Keep the label set small. Quality over quantity.
* Avoid emoji in label names — they sort inconsistently.

## Suggested Setup

You can create these labels via `gh label create` or the GitHub UI. A script is provided in `scripts/setup-labels.sh` (optional, project authors may adapt).