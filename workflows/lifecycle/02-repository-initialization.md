# Workflow 02 — Repository Initialization

## Goal

Configure a fresh CDF repository for **immediate usability**: tooling, CI, dependencies, branch protection, and contributor ergonomics.

## Inputs

* A repository that has been bootstrapped using `01-start-new-project.md`.

## Outputs

* A working CI pipeline.
* Working linters / formatters.
* Working test runner.
* Branch protection rules.
* Recommended GitHub labels.
- Recommended GitHub Discussions categories.

## Definition of Done

- [ ] CI runs on PRs (lint, test, build).
- [ ] Linters and formatters are configured for the chosen language(s).
- [ ] Branch protection enabled on `main`.
- [ ] Labels created per `.github/LABELS.md`.
- [ ] Discussion categories created per `.github/DISCUSSIONS/RECOMMENDATIONS.md`.
- [ ] Issue templates verified.
- [ ] PR template verified.
- [ ] CONTRIBUTING.md verified.
- [ ] CODEOWNERS (optional) set for critical paths.

## Responsible Roles

* **Developer** — configures CI, lint, test.
* **Reviewer** — configures branch protection and review requirements.
* **Maintainer** — enables Discussions.

## Procedure

### Step 1 — Choose Tooling

1. Pick a primary language / stack.
2. Document the choice in `docs/conventions/tooling.md`.
3. Add the choice to `.cognition/identity/` (via ADR if it is architectural).

### Step 2 — Configure CI

1. Add a CI workflow (e.g. `.github/workflows/ci.yml`).
2. Run lint, test, build.
3. Cache dependencies.
4. Block merges if CI fails.

### Step 3 — Configure Branch Protection

On `main`:

* Require PRs.
* Require N reviews (default: 1).
* Require CI to pass.
* Disallow direct pushes.

### Step 4 — Configure Labels

Apply `.github/LABELS.md`.

### Step 5 — Configure Discussions

Apply `.github/DISCUSSIONS/RECOMMENDATIONS.md`.

### Step 6 — Verify Templates

Open an issue of each type and a test PR. Confirm the templates appear.

### Step 7 — Write the First `.cognition/memory/working/current_context.md`

It should now reflect the bootstrapped state.

## Common Pitfalls (Refuse)

* CI that runs only on `main` (too late — catch problems in PRs).
* Branch protection without required reviews (a single push can corrupt the project).
* Lint rules nobody agrees with.

---

> *A repository that builds itself is a repository that scales.*