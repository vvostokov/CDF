# Bounded Contexts

## Purpose

One file per bounded context. Each file is a **deep dive** into a single context: aggregates, entities, value objects, events, ACLs, internal rules, and tests.

The summary domain model in `/.cognition/architect/domain_model.md` lists all contexts; this directory holds the details.

## File Naming

* `NNNN-context-name.md` (e.g. `0001-billing.md`).
* Numbering is monotonic per directory.

## Template

See `0000-template.md` in this directory.

## Lifecycle

* A bounded context is added when the system acquires a new responsibility.
* A bounded context is split when its internal complexity grows.
* A bounded context is merged (rarely) when two contexts prove to be one.
* All changes are linked to ADRs.

## Cross-References

* Each bounded-context file references its owning ADRs.
* Each bounded-context file references related invariants, business rules, and glossary terms.
* Sequence diagrams live in `/architecture/diagrams/`.

---

> *A bounded context is a bounded argument about the world.*