---
title: Architecture Review
status: draft
last_updated: YYYY-MM-DD
owner: reviewer
review_period:
  from: YYYY-MM-DD
  to:   YYYY-MM-DD
---

# Architecture Review

> A periodic, holistic review of the project's architecture. Conducted per milestone or quarter.

## Scope

<!-- What is included in this review:
     - The whole architecture
     - One bounded context
     - One subsystem
-->

## Inputs

* All ADRs in `knowledge/architecture-decisions/`
* Domain model (`.cognition/architect/domain_model.md`)
* System context (`.cognition/architect/system_context.md`)
* Recent review reports (`.cognition/reviewer/review_report.md`)
* Technical debt ledger (`technical_debt.md`)
* Roadmap status (`.cognition/memory/roadmap/roadmap.md`)

## Questions This Review Must Answer

1. Does the architecture still match the **mission** and **vision**?
2. Are the **bounded contexts** still correctly carved?
3. Are there **invariants** we no longer enforce, or new invariants we should add?
4. Have we **accumulated debt** in any one area faster than we are paying it down?
5. Are any **ADRs** now obsolete, contradicted by reality, or worth superseding?
6. Where is **architectural drift** most likely next?
7. Are our **non-functional requirements** still met (perf, reliability, security, observability)?

## Findings

### Healthy

* …

### At Risk

* …

### Broken

* …

## Drift Inventory

| Area                  | Drift Observed                  | Severity | Action                  |
|-----------------------|---------------------------------|----------|-------------------------|
|                       |                                 |          |                         |

## Debt Highlights

<!-- Top N items from technical_debt.md ordered by priority × impact. -->

1. TD-XXX — …
2. TD-XXX — …

## Recommended Actions

- [ ] …
- [ ] …

## Proposed ADRs

<!-- From this review. -->

* `knowledge/architecture-decisions/NNNN-*.md` (proposed)

## Sign-off

* Reviewer:
* Architect:
* Date:

---

> *Architecture reviews catch drift before drift catches us.*