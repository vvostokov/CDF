# CDF Improvement Log

> A journal of every problem, friction, surprise, or structural question encountered while using CDF in practice.

This file is the **only** basis for evolving CDF. Speculative changes are not accepted.

## How to Use This Log

When you encounter something while using CDF that:

* Forces you to work around the structure,
* Surprises you in a way the manifest did not predict,
* Conflicts with another part of CDF,
* Or feels like it should be a built-in feature,

add an entry below using the template.

Each entry gets an `id`. When CDF's structure is later changed to address an entry, link the change to the entry's `id`.

## Categories

| Code  | Meaning                                                |
|-------|--------------------------------------------------------|
| `STR` | Structural issue — CDF's directory / file structure    |
| `CON` | Convention issue — a rule that does not match practice |
| `PRO` | Process issue — a workflow is missing or unclear       |
| `TMP` | Template issue — an artifact template is missing fields |
| `PMT` | Prompt issue — an AI prompt misleads or fails          |
| `MAN` | Manifest issue — `cdf.manifest.yaml` does not match reality |
| `DOC` | Documentation issue — README or doc is wrong or unclear |

Severity: `low` (cosmetic) | `medium` (friction) | `high` (blocks progress) | `critical` (forces re-architecture).

---

## Statistics

* **Total entries:** 7
* **By category:** STR: 4, CON: 3, PRO: 0, TMP: 0, PMT: 0, MAN: 0, DOC: 0
* **By severity:** critical: 0, high: 3, medium: 4, low: 0
* **By status:** open: 0, accepted: 4, deferred: 3, rejected: 0

---

## Entries

<!-- Newest entries go to the top. -->

### 2026-06-28 — Knowledge and processes are mixed at the same conceptual level

* **ID:** CDF-001
* **Category:** STR
* **Severity:** high
* **Project:** External architectural work (Zhamlik, ReflectWise, AI_OS designs)
* **Context:** Designing long-term cognitive architectures for Zhamlik and ReflectWise.
* **Observation:** Stable project knowledge and activities that transform that knowledge lived at the same conceptual level in CDF v1, making it increasingly difficult to distinguish them.
* **Expected:** Knowledge should remain relatively stable; processes should evolve independently.
* **Workaround:** Attempted informal separation via roles (`.cognition/planner/`, etc.) but the mental model kept collapsing because roles are not processes.
* **Suggested change:** Introduce two top-level groupings under `.cognition/`: `knowledge/` (static) and `processes/` (dynamic).
* **Status:** accepted
* **Resolution:** Implemented as `.cognition/knowledge/` and `.cognition/processes/`. Existing role directories (planner, architect, developer, reviewer, curator, researcher) migrated to `processes/`; static artifacts (identity, memory, ontology-like) migrated to `knowledge/`.

### 2026-06-28 — Project has no explicit epistemic layer

* **ID:** CDF-002
* **Category:** STR
* **Severity:** high
* **Project:** External architectural work (Zhamlik)
* **Context:** Designing traceable financial reasoning for Zhamlik.
* **Observation:** Repeated questions like "What is evidence?", "What is validated knowledge?", "What is confidence?" had no dedicated place in CDF v1. They leaked into `principles.md`, `invariants.md`, and `architecture_notes.md` without a coherent home.
* **Expected:** Every cognitive project should explicitly define how knowledge is established.
* **Workaround:** Used ad-hoc notes within existing identity and architect directories.
* **Suggested change:** Add `knowledge/epistemology/` as a first-class layer with documents on evidence, truth criteria, confidence, uncertainty, and validation protocol.
* **Status:** accepted
* **Resolution:** Created `knowledge/epistemology/` with five foundational documents.

### 2026-06-28 — Project models are not first-class artifacts

* **ID:** CDF-003
* **Category:** STR
* **Severity:** medium
* **Project:** External architectural work (Zhamlik, ReflectWise)
* **Context:** Designing domain models, execution models, and reasoning models.
* **Observation:** Models became scattered across identity, architecture notes, and ontology documents. No single directory answers "where are the project models?".
* **Expected:** Models should be explicit artifacts with a clear home.
* **Workaround:** Currently living in `processes/architect/domain_model.md` and `processes/architect/system_context.md` — these are first-class within the architect role.
* **Suggested change:** Create a top-level `knowledge/models/` directory.
* **Status:** deferred
* **Resolution:** Rejected as redundant. In CDF v1.1, models already have a first-class home as `processes/architect/{domain_model.md,system_context.md,architecture_notes.md}`. The architect role *is* the model owner. Creating `knowledge/models/` on top would be renaming for aesthetic reasons, which Rule #1 explicitly forbids. **Revisit if:** Zhamlik or another project surfaces a real need for models that are *not* owned by the architect role (e.g. a model owned by operations, or a model that is purely declarative and never transformed). Until then, `processes/architect/` is the canonical location.

### 2026-06-28 — Reasoning history and final decisions are mixed

* **ID:** CDF-004
* **Category:** STR
* **Severity:** medium
* **Project:** External architectural work (Zhamlik, ReflectWise)
* **Context:** Revisiting architectural discussions weeks after they occurred.
* **Observation:** Could find the final decision but not the chain of reasoning that produced it. Architecture notes contained both conclusions and the reasoning, but were often summarized at decision time, losing nuance.
* **Expected:** Architectural reasoning should be preserved independently of decisions.
* **Workaround:** Reconstructed reasoning from commit messages and PR comments when needed.
* **Suggested change:** Add `memory/reasoning/` as a dedicated location for saved chains of thought.
* **Status:** accepted
* **Resolution:** Created `knowledge/memory/reasoning/` as a subdirectory of permanent memory. Existing `architecture_notes.md` continues to host active scratch; reasoning chains that produce decisions are now archived separately under `memory/reasoning/`.

### 2026-06-28 — Capabilities emerged as reusable units across multiple projects

* **ID:** CDF-005
* **Category:** STR
* **Severity:** medium
* **Project:** External architectural work (Zhamlik, ReflectWise, AI_OS)
* **Context:** Planning all three projects.
* **Observation:** Features were too small (single change). Epics were too large (multi-quarter). A reusable architectural unit between strategy and implementation was needed but not represented in CDF v1.
* **Expected:** A "capability" — a reusable, owner-assigned, maturity-tracked unit of capability — should be a first-class planning artifact.
* **Workaround:** Treated capabilities implicitly as themes in `roadmap.md` and as vertical slices in `next_vertical_slice.md`. Worked but lost the reusability signal.
* **Suggested change:** Add `processes/planner/capabilities/` as a directory.
* **Status:** deferred
* **Resolution:** Rejected as premature. CDF v1.1 already has `processes/planner/next_vertical_slice.md` as the unit-of-development. Adding a parallel `capabilities/` structure would create two competing planning artifacts. **Revisit if:** Zhamlik shows that a slice is repeatedly built across multiple iterations AND that slice's state, maturity, and ownership need to be tracked separately from its current task. Until then, slices remain the single unit of development.

### 2026-06-28 — Actor and Role are different concepts

* **ID:** CDF-006
* **Category:** CON
* **Severity:** medium
* **Project:** External architectural work (multi-LLM workflows)
* **Context:** Using multiple LLMs (Hermes, ChatGPT, Claude) together with human developers.
* **Observation:** One actor could perform several roles; one role could be performed by different actors. CDF v1 described roles well but did not explicitly model the actor concept.
* **Expected:** Actor and Role should be represented as distinct concepts.
* **Workaround:** Implicit: prompts in `prompts/roles/` are actor-agnostic; the human decides which actor invokes which prompt.
* **Suggested change:** Document the actor/role distinction explicitly.
* **Status:** deferred
* **Resolution:** Rejected as a structural change — this is a **convention**, not a structure. CDF v1.1 documents the distinction in `processes/README.md` without creating a new directory. The actor layer (human, LLM, automation, CI, future AI_OS) is intentionally outside the cognitive layer because actors are *implementations* of role execution. **Revisit if:** A future AI_OS-style runtime becomes part of CDF, at which point actors may need their own manifest section.

### 2026-06-28 — Reflection became an architectural process, not documentation

* **ID:** CDF-007
* **Category:** STR
* **Severity:** high
* **Project:** External architectural work (multi-project iteration)
* **Context:** Reviewing design decisions over multiple iterations of Zhamlik and ReflectWise designs.
* **Observation:** Lessons learned had no dedicated lifecycle. `curator/lessons_learned.md` collected observations, but reflection *as a process* — analyzing decisions, surfacing patterns, challenging assumptions — was missing.
* **Expected:** Reflection should continuously feed project knowledge as a distinct process.
* **Workaround:** Mixed reflection into the curator role. Friction grew because reflection is *about* knowledge, not *of* knowledge.
* **Suggested change:** Add `processes/reflector/` as a distinct role.
* **Status:** accepted
* **Resolution:** Created `processes/reflector/` with a role prompt and the four primary reflection artifacts (what slowed us, what surprised us, wrong assumptions, what should change).

---

## Resolved Entries

All entries above have inline `Resolution:` fields. As CDF evolves, resolved entries will be moved here with explicit commit/PR references.

---

> *The log is the project's self-knowledge. The first 10 entries matter more than the next 1000.*