# Contributing to the Cognitive Development Framework

Thank you for considering a contribution to CDF. CDF is itself a project that follows its own framework. Contributions therefore follow the same rigor we ask of any project: **architecture before code, knowledge before change, reasoning before optimization.**

## Rule #1 — CDF Evolves Only After Practical Experience

> **Every structural change to CDF must reference a real problem encountered during software development.**
>
> **No speculative architecture.**

This rule is the **first and most important** rule of CDF. It exists to prevent the framework from accumulating layers that "would be useful someday" but never earn their place.

### What this means concretely

* A pull request that adds a new directory, layer, schema, or process to CDF **must** link to at least one entry in [`cdf-improvement-log.md`](./cdf-improvement-log.md) that justifies the change.
* "I think it would be useful" is **not** sufficient justification.
* "Another framework has it" is **not** sufficient justification.
* The exception is the **first** set of structural elements, which were bootstrapped at version 1.0 and documented in `cdf.manifest.yaml`.

### How to propose a change

1. **First**, if you have not already, use CDF on a real project.
2. When you encounter friction, log an entry in `cdf-improvement-log.md` using the template there.
3. If the friction is structural (it cannot be solved within CDF's current structure), open a discussion linking the log entry.
4. Once there is consensus that a structural change is justified, open a pull request that:
   * Links to the log entry.
   * Describes the smallest change that resolves the issue.
   * Updates `cdf.manifest.yaml` if structure changes.
   * Updates `cdf-improvement-log.md` to mark the entry as resolved.

### What CDF will not accept

* Speculative layers added "just in case".
* Renaming of stable paths purely for aesthetic reasons.
* New mandatory dependencies (RDF parsers, graph databases, async runtimes, etc.) inside CDF itself.
* Anything that violates the invariants in `cdf.manifest.yaml`.

## Code of Conduct

This project follows the [`CODE_OF_CONDUCT.md`](./CODE_OF_CONDUCT.md). By participating, you agree to uphold it.

## How to Contribute

There are many ways to contribute:

* **Propose improvements** to the framework via a Discussion.
* **Submit changes** to identity, principles, prompts, workflows, or templates via a Pull Request.
* **Report bugs** or unclear instructions via an Issue.
* **Improve documentation** in `docs/`.
* **Add new templates** to `knowledge/` that have proven useful in your projects.

## Workflow

1. **Open a Discussion** for any non-trivial change. Identity, principles, prompts, and workflows are architectural — they need a conversation, not just a PR.
2. **Open an Issue** for concrete, well-scoped changes (a typo, a missing section, a new example).
3. **Fork the repository** and create a branch.
4. **Follow** the relevant workflow in `workflows/`:
   * `workflows/lifecycle/01-start-new-project.md` for major structural changes
   * `workflows/engineering/code-review.md` for documentation changes
   * `workflows/knowledge/knowledge-update.md` for changes to `knowledge/`
5. **Update** the relevant artifact in `.cognition/` if your change affects framework identity, principles, or roles.
6. **Submit a Pull Request** using the provided template.
7. **Pass** the review checklist (architecture review + technical review).

## Contribution Principles

* **Explain why**, not only what.
* **Reference** the relevant template or ADR when relevant.
* **Keep changes atomic** — one concern per PR.
* **Preserve backward compatibility** unless the change is explicitly breaking.
* **Update memory** — if your change makes existing knowledge stale, update it in the same PR.

## Style

* Markdown is preferred for all narrative content.
* Filenames use lowercase, hyphens, and short, descriptive names (`bounded-context.md`, not `BoundedContextDoc.md`).
* All directories must contain a `README.md`.
* Identity files are immutable except via an ADR-style change proposal.

## Reviewers

Pull requests require:

* One architecture review from a maintainer (for changes to `.cognition/`, `prompts/`, `workflows/`, `knowledge/`).
* One technical review from any contributor.
* A passing CI / linter run (when applicable).

## Reporting Security Issues

Please **do not** open a public issue for security vulnerabilities. See [`SECURITY.md`](./SECURITY.md) for the private reporting process.

## Recognition

Contributors are listed in `CONTRIBUTORS.md` (created when the first non-trivial contribution lands). All contributors retain copyright of their contributions under the MIT License.

---

> CDF is a framework for thinking. Contributing to it is itself an exercise of that framework.