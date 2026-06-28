# Bounded Context — [Name]

* **Context ID:** BC-NNN
* **Strategic classification:** `core` | `supporting` | `generic`
* **Owners:**
* **Created:** YYYY-MM-DD
* **Related ADRs:** [list]
* **Related invariants:** [list of INV-IDs]
* **Related business rules:** [list of BR-IDs]

## Purpose

<!-- What is this context responsible for? What is it NOT responsible for? -->

## Ubiquitous Language

<!-- Terms specific to this context, with their short definitions. -->

* **[Term]** — definition.

## Strategic Relationships with Other Contexts

| Other Context | Pattern           | Notes                                |
|---------------|-------------------|--------------------------------------|
|               | `partnership` / `customer-supplier` / `conformist` / `ACL` / `shared kernel` / `OHS` |                                      |

## Aggregates

### Aggregate: [Name]

* **Root entity:**
* **Invariants:**
* **Lifecycle:**
* **Allowed operations (commands):**
* **Emitted events:**
* **Subscribed events:**
* **Tests:**

## Entities

* **[Entity Name]** — description.

## Value Objects

* **[VO Name]** — description.

## Domain Services

* **[Service Name]** — purpose, contract, side effects.

## Domain Events

* **[Event Name]** — schema, consumers.

## Anti-Corruption Layers

* **[ACL Name]** — what it protects against.

## Internal Rules

<!-- Rules that are not business rules but are internal to this context. -->

* …

## Open Modeling Questions

* …

## Change Log

| Date       | Change                       | Author | ADR |
|------------|------------------------------|--------|-----|
| YYYY-MM-DD | Initial scaffold             |        |     |

---

> *The bounded context is where model and code agree on what they are talking about.*