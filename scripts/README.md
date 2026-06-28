# `scripts/` — Automation and Utilities

## Purpose

Scripts for setup, build, lint, test, release, and any other repeatable task that does **not** belong in the application's runtime.

## Conventions

* Scripts are **idempotent** — running them twice has the same effect as once.
* Scripts accept `--help`.
* Scripts log what they are doing.
* Scripts fail fast and loud.
* Scripts are tested (at least manually).

## Suggested Files

* `setup.sh` / `setup.ps1` — first-time setup.
* `lint.sh` / `lint.ps1` — run linters.
* `test.sh` / `test.ps1` — run all tests.
* `build.sh` / `build.ps1` — build artifacts.
* `release.sh` / `release.ps1` — prepare a release.
* `render-diagrams.sh` — render architecture diagrams.
* `setup-labels.sh` — create the GitHub labels recommended in `.github/LABELS.md`.

## Relationship with AI

When generating scripts, the AI must:

1. Use POSIX shell when possible (cross-platform).
2. Include Windows variants when needed.
3. Document inputs and outputs in the file header.
4. Avoid hardcoded paths.

## Lifecycle

* Scripts are versioned with the project.
* Scripts can be replaced, but never silently.
* A broken script is a bug.

---

> *Scripts are how the project automates itself.*