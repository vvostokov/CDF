# Changelog

All notable changes to the Cognitive Development Framework (CDF) are documented in this file.

The format is based on [Keep a Changelog](https://keepachangelog.com/en/1.1.0/),
and this project adheres to [Semantic Versioning](https://semver.org/spec/v2.0.0.html).

## [Unreleased]

## [1.1.0] — 2026-06-28 — Evolutionary Update

### Added
- `.cognition/epistemology/` — six documents: knowledge theory, evidence model, truth criteria, confidence framework, uncertainty handling, validation protocol. *(Log entry CDF-002.)*
- `.cognition/memory/permanent/reasoning/` — saved chains of architectural thought. *(Log entry CDF-004.)*
- `.cognition/reflector/` — reflection as a distinct role from curation, with role prompt and four artifacts (what slowed us, what surprised us, wrong assumptions, what should change). *(Log entry CDF-007.)*
- `.cognition/knowledge/README.md` and `.cognition/processes/README.md` — conceptual namespaces separating static knowledge from dynamic processes. **No physical migration**; existing v1.0 directory layout is preserved. *(Log entry CDF-001.)*

### Changed
- `cdf.manifest.yaml` updated to v1.1.0 reflecting the new conceptual namespaces, three new layers (epistemology, reasoning, reflector), and explicit references to the seven improvement log entries that justify every change.
- `README.md` updated with the v1.1 changelog above and a structured map of the cognitive layer showing which directories belong to knowledge vs. processes conceptually.
- `cdf-improvement-log.md` populated with seven entries (CDF-001 through CDF-007) drawn from external architectural work on Zhamlik, ReflectWise, and AI_OS designs.

### Preserved
- All 396 cross-references in v1.0 files. No existing file was renamed or moved. Blast radius of v1.1 is bounded to **newly created files only**.

### Deferred
- `knowledge/models/` (CDF-003) — architect role already owns models; no separate namespace needed yet.
- `processes/planner/capabilities/` (CDF-005) — slices remain the unit of development; capability as a separate artifact is a future possibility.
- `actors/` top-level namespace (CDF-006) — actor/role distinction is documented in `processes/README.md` as a convention; structure deferred until an actor-runtime emerges.

## [0.1.0] — 2026-06-28 — Initial Template (Freeze)

### Added
- Initial release of the Cognitive Development Framework template repository.
- `.cognition/` cognitive layer with identity, planner, architect, developer, reviewer, curator, researcher, memory, history, sessions, and roadmap sections.
- `knowledge/` templates: ADR, glossary, domain model, bounded context, invariants, feature specification, business rule, risk analysis, technical debt, retrospective, lessons learned, review report, decision proposal.
- `prompts/` for AI roles (Planner, Architect, Developer, Reviewer, Curator, Researcher) and tasks (Documentation, Testing, Bug Fix, Refactoring, Release, Prompt Improvement, Prompt Review).
- `workflows/` for the full project lifecycle, engineering, and knowledge operations.
- `.github/` templates: issue templates, pull request template, discussion recommendations, label recommendations.
- Top-level `README.md`, `LICENSE`, `CONTRIBUTING.md`, `SECURITY.md`, `CODE_OF_CONDUCT.md`, `.editorconfig`, `.gitignore`.

### Changed
- README: published as **Experimental** with validation count `0`. Honest framing replaces earlier aspirational language.
- CONTRIBUTING: added **Rule #1** — *CDF evolves only after practical experience*. Every structural change must reference an entry in `cdf-improvement-log.md`.

### Added (Freeze)
- `cdf.manifest.yaml` — declarative description of this CDF installation. Analogous to `package.json` / `Cargo.toml` / `pyproject.toml` but at the cognitive-architecture level.
- `cdf-improvement-log.md` — journal template for issues encountered while using CDF. The **only** basis for evolving the framework.

### Frozen
- **CDF is frozen at version 1.0.** No new layers, schemas, processes, or directories will be added until a real project surfaces a structural problem that requires them.
- The repository is published as **Experimental**, with `validation.projects_validated: 0` recorded in `cdf.manifest.yaml`.