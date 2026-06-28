# `risks/` — Risk Analyses

## Purpose

A risk analysis captures **a specific risk**, its likelihood, its impact, its mitigation, and its owner.

Risks differ from technical debt: debt is known, accepted, and on the books. Risks are unknown-but-foreseeable.

## File Naming

* `NNNN-kebab-case-risk-title.md`
* Numbering is monotonic.

## Template

See `0000-template.md`.

## Lifecycle

* `open` — risk identified, mitigation in progress.
* `mitigated` — controls in place.
* `accepted` — risk is acknowledged; mitigation is "live with it".
* `realized` — risk happened; a retrospective was created.
* `closed` — risk no longer relevant.

## AI Behavior

When proposing a risk analysis, the AI must:

1. State the risk concretely.
2. Estimate likelihood and impact separately.
3. Distinguish **inherent** vs **residual** risk.
4. Tie mitigation to actions and owners.

---

> *A risk written down is half-mitigated.*