---
title: Constraints
status: draft
last_updated: YYYY-MM-DD
---

# Constraints

> Hard constraints — technical, regulatory, organizational, financial — that the project must respect without exception.

Constraints are **fixed** inputs. Unlike principles (which we choose), constraints are imposed by reality. We do not negotiate with constraints; we design around them.

## Categories

* **Regulatory** — laws, standards, certifications.
* **Technical** — platform limits, performance budgets, language limits.
* **Organizational** — team size, skills, on-call capacity.
* **Financial** — budget, vendor lock-in, licensing.
* **Temporal** — deadlines, SLAs, lifecycles.
* **Legal** — IP, data residency, contractual obligations.

## Constraints

<!-- List each constraint with:
     - ID (e.g. C-001)
     - Category
     - Statement
     - Source
     - Verification: how we check it
     - Effect: how it shapes design
-->

| ID    | Category       | Constraint                          | Source                  | Effect                                  |
|-------|----------------|-------------------------------------|-------------------------|-----------------------------------------|
| C-001 |                |                                     |                         |                                         |
| C-002 |                |                                     |                         |                                         |
| C-003 |                |                                     |                         |                                         |

## Detailed Constraint Statements

### C-001 — [Title]

* **Category:**
* **Statement:**
* **Source:**
* **Owner:**
* **Verification:**
* **Design implication:**
* **Related ADRs / docs:**

### C-002 — [Title]

* **Category:**
* **Statement:**
* **Source:**
* **Owner:**
* **Verification:**
* **Design implication:**
* **Related ADRs / docs:**

<!-- Repeat as needed. -->

## How Constraints Interact with Identity

* A **constraint violation** is not a discussion. It is a bug.
* A **principle violation** can be discussed. An ADR can accept the violation.
* A **constraint** can never be violated by an ADR. The constraint wins.

## Related

* `principles.md` — how we choose to operate.
* `philosophy.md` — how we think.
* `knowledge/risks/` — risks that *could* become constraints.