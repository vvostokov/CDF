---
title: Implementation Constraints
status: draft
last_updated: YYYY-MM-DD
owner: developer
---

# Implementation Constraints

> Hard and soft rules that govern how code is written in this project. Violations require an explicit justification.

## Hard Constraints (Will Be Rejected in Review)

### IC-H-1 — [Constraint]

* **Statement:**
* **Why it is hard:**
* **How it is enforced:** linter / CI / convention

### IC-H-2 — [Constraint]

* (Same shape)

## Soft Constraints (Strong Defaults)

### IC-S-1 — [Constraint]

* **Statement:**
* **Why it is the default:**
* **When to deviate:** …

### IC-S-2 — [Constraint]

* (Same shape)

## Categories to Cover

Use these as headings when filling out this document.

* **Naming conventions**
* **File / module structure**
* **Error handling**
* **Logging**
* **Testing requirements** (per change type)
* **Documentation requirements** (per change type)
* **Dependency rules** (who can import what)
* **Concurrency / threading**
* **I/O and resource handling**
* **Security defaults**
* **Performance budgets**
* **Backwards compatibility**
* **API design**
* **Database access**
* **Configuration**
* **Observability**

## How to Change This Document

* Changes are PRs with rationale.
* Breaking changes require an ADR.
* Reviewer is the architect.

---

> *Constraints free us. They remove decisions we shouldn't have to make each day.*