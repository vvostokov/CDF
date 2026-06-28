# Changelog

All notable changes to the Cognitive Development Framework (CDF) are documented in this file.

The format is based on [Keep a Changelog](https://keepachangelog.com/en/1.1.0/),
and this project adheres to [Semantic Versioning](https://semver.org/spec/v2.0.0.html).

## [Unreleased]

### Added
- Initial release of the Cognitive Development Framework template repository.
- `.cognition/` cognitive layer with identity, planner, architect, developer, reviewer, curator, researcher, memory, history, sessions, and roadmap sections.
- `knowledge/` templates: ADR, glossary, domain model, bounded context, invariants, feature specification, business rule, risk analysis, technical debt, retrospective, lessons learned, review report, decision proposal.
- `prompts/` for AI roles (Planner, Architect, Developer, Reviewer, Curator, Researcher) and tasks (Documentation, Testing, Bug Fix, Refactoring, Release, Prompt Improvement, Prompt Review).
- `workflows/` for the full project lifecycle, engineering, and knowledge operations.
- `.github/` templates: issue templates, pull request template, discussion recommendations, label recommendations.
- Top-level `README.md`, `LICENSE`, `CONTRIBUTING.md`, `SECURITY.md`, `CODE_OF_CONDUCT.md`, `.editorconfig`, `.gitignore`.

### Changed
- README: republished as **Experimental** with validation count `0`. Honest framing replaces earlier aspirational language.
- CONTRIBUTING: added Rule #1 — *CDF evolves only after practical experience*. Every structural change must reference an entry in `cdf-improvement-log.md`.

### Added (Freeze)
- `cdf.manifest.yaml` — declarative description of this CDF installation. Analogous to `package.json` / `Cargo.toml` / `pyproject.toml` but at the cognitive-architecture level.
- `cdf-improvement-log.md` — journal template for issues encountered while using CDF. The **only** basis for evolving the framework.

## [0.1.0] — 2026-06-28 — Freeze

### Changed
- **CDF is frozen at version 1.0.** No new layers, schemas, processes, or directories will be added until a real project surfaces a structural problem that requires them.
- The repository is published as **Experimental**, with `validation.projects_validated: 0` recorded in `cdf.manifest.yaml`.