# `business-rules/` — Business Rule Specifications

## Purpose

Business rules captured as **standalone, reviewable artifacts**. The summary in `/.cognition/memory/permanent/business_rules.md` lists the rules; the files here describe each rule in depth.

## File Naming

* `BR-NNN-kebab-case-name.md`
* Numbers correspond to the BR-IDs in `/.cognition/memory/permanent/business_rules.md`.

## Template

See `0000-template.md`.

## Lifecycle

* Each rule file is created when the rule is introduced.
* Updates require a PR with rationale.
* Deprecations are noted in the file (not deleted).

## AI Behavior

When describing a business rule, the AI must:

1. State the rule in plain English.
2. Provide examples and counterexamples.
3. Identify the **trigger** and the **response on violation**.
4. Link to tests and code locations.

---

> *A business rule without examples is a misunderstanding waiting to happen.*