# Cognitive Development Framework (CDF)

> **Status: Experimental**
> **Version: 1.1**
> **Validation: 0 projects**
>
> CDF is published as an experimental GitHub Template. It evolves only through documented evidence — see [`cdf-improvement-log.md`](./cdf-improvement-log.md) for the journal that drives every structural change.
>
> See [`cdf.manifest.yaml`](./cdf.manifest.yaml) for the declarative description of v1.1.

---

## What CDF Is

The **Cognitive Development Framework (CDF)** is a **Cognitive Operating Framework** for software engineering. It is **not** an application and **not** a software framework. It is language-agnostic, technology-agnostic, and AI-friendly.

Its purpose is to help **humans and AI** collaborate on complex software projects over many years while preserving architectural knowledge, reasoning, decisions, and project memory.

## What CDF Is Not

To prevent misunderstanding, CDF is explicitly **not**:

* A runtime. It does not execute anything.
* A configuration format. `cdf.manifest.yaml` declares structure; it does not control behavior.
* An opinionated stack. It does not assume any language, framework, database, or deployment target.
* A finished product. It is experimental. It has been validated against **0** projects.
* A growing architecture. Its structure is frozen until a real project surfaces a structural problem.

## Why CDF Exists

Most repositories store code. Few store the *thinking* behind the code.

After a few months of development, the original context is lost:

* Why was this technology chosen?
* What problem does this module actually solve?
* Which constraints shaped this design?
* What was the previous AI assistant told?
* What invariants must never be broken?

CDF makes the **project's cognitive layer** part of the repository itself. The `.cognition/` directory is the **brain** of the project. The source code is only one organ.

If the entire team — humans and AI — disappears, a new team (or a new AI) should be able to **reconstruct the project** by reading the repository.

## How to Use CDF

### Option A — As a GitHub Template (Recommended)

1. Click **"Use this template"** on the GitHub repository page.
2. Name your project.
3. Clone the new repository.
4. Edit `.cognition/identity/mission.md` with your project's mission.
5. Walk through each identity document in order.
6. Open the first planning iteration in `.cognition/planner/`.
7. **When you encounter friction or surprises, log them in `cdf-improvement-log.md`.**

### Option B — Manual

1. Clone or copy this repository.
2. Rename the root directory.
3. Follow `workflows/lifecycle/01-start-new-project.md`.
4. Follow `workflows/lifecycle/02-repository-initialization.md`.

## Repository Structure

```
.
├── cdf.manifest.yaml         # Declarative description of this CDF installation
├── cdf-improvement-log.md    # Journal of issues that drive every structural change
├── .cognition/               # The cognitive layer (project's brain)
│   ├── identity/             # Who we are (knowledge)
│   ├── memory/               # What we know, remember, decide (knowledge)
│   │   └── permanent/reasoning/  # Saved chains of architectural thought (v1.1)
│   ├── epistemology/         # How we know (knowledge, v1.1)
│   ├── knowledge/            # Conceptual namespace — see README (v1.1)
│   ├── processes/            # Conceptual namespace — see README (v1.1)
│   ├── planner/              # Goals, iterations, slices (process)
│   ├── architect/            # Design, domain model, ADRs (process)
│   ├── developer/            # Implementation, tests (process)
│   ├── reviewer/             # Reviews, technical debt (process)
│   ├── curator/              # Knowledge maintenance (process)
│   ├── researcher/           # Research, experiments (process)
│   └── reflector/            # Reflection, patterns, lessons (process, v1.1)
├── .github/                  # GitHub templates (issues, PRs, discussions)
├── knowledge/                # Long-lived knowledge artifacts (ADRs, glossary, etc.)
├── architecture/             # Architectural artifacts (context, decisions, diagrams)
├── docs/                     # Guides, conventions, references
├── prompts/                  # Reusable AI prompts (roles + tasks)
├── workflows/                # End-to-end workflows
├── src/                      # Source code (language chosen by the project)
├── tests/                    # Tests
└── scripts/                  # Automation, utilities
```

Every directory contains a `README.md` explaining **purpose, structure, lifecycle, expected content, and relationship with AI**.

## What's New in v1.1

CDF v1.1 is an **evolutionary** update to v1.0. The existing directory layout is preserved to avoid disrupting 396 cross-references. New additions are:

* **`.cognition/epistemology/`** — six documents defining how the project knows: knowledge theory, evidence, truth, confidence, uncertainty, validation. *(Entry CDF-002.)*
* **`.cognition/memory/permanent/reasoning/`** — saved chains of architectural thought, separate from the decisions they produce. *(Entry CDF-004.)*
* **`.cognition/reflector/`** — reflection as a distinct role from curation, with a role prompt and four reflection artifacts. *(Entry CDF-007.)*
* **`.cognition/knowledge/` and `.cognition/processes/`** — conceptual namespaces separating static knowledge from dynamic processes. Files remain in their v1.0 locations; physical migration is deferred until evidence demands it. *(Entry CDF-001.)*

Three proposals were **deferred** rather than implemented:
* `knowledge/models/` (CDF-003) — the architect role already owns models.
* `processes/planner/capabilities/` (CDF-005) — slices remain the unit of development for now.
* `actors/` (CDF-006) — actor/role distinction is documented as a convention, not a structure.

See [`cdf-improvement-log.md`](./cdf-improvement-log.md) for the full journal including rejected proposals with their rationale.

## How CDF Evolves

CDF evolves **only** through documented, real-world experience.

* Every structural change must reference at least one entry in `cdf-improvement-log.md` that justifies the change.
* Speculative architecture — adding layers "just in case" — is explicitly rejected.
* See [`CONTRIBUTING.md`](./CONTRIBUTING.md) for the full rule.

This is the **first and most important rule** of CDF. If you are tempted to add a layer because it "would be useful someday", don't. Wait until the day arrives.

## Philosophical Commitments

* Architecture before implementation.
* Knowledge before code.
* Reasoning before optimization.
* Project memory before convenience.
* Explicit over implicit.
* Documented over assumed.

These are stated in full in `.cognition/identity/principles.md` and `.cognition/identity/philosophy.md`.

## License

MIT — see [`LICENSE`](./LICENSE).

---

> *"If your repository cannot be understood in five years by someone who has never seen it, your repository is not a project — it is a problem in waiting."*
>
> *CDF is published as experimental because it has not yet had the chance to prove that statement true. That proof is up to the projects that use it.*