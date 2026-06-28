---
title: Domain Model
status: draft
last_updated: YYYY-MM-DD
owner: architect
---

# Domain Model

> The current model of the project's domain. Bounded contexts, aggregates, entities, value objects, domain services, and domain events.

## How to Read This

* The model is expressed in **bounded contexts**.
* Each bounded context owns its own aggregates, entities, value objects, and events.
* Cross-context communication happens through **published contracts** (events, APIs) — never through shared databases or shared entities.

## Bounded Context Map

<!-- A short summary of contexts and their relationships.
     Use the strategic patterns:
     - Partnership
     - Customer–Supplier
     - Conformist
     - Anti-Corruption Layer
     - Shared Kernel
     - Open-Host Service
-->

```
[Context A] ─── partnership ───> [Context B]
[Context C] ─── conformist ───> [Context D]
[Context E] ─── ACL ───> [External System F]
```

## Bounded Contexts

### Context: [Name]

* **Purpose:**
* **Owners:**
* **Strategic classification:** `core` | `supporting` | `generic`
* **Communication style:** `REST` | `events` | `RPC` | `shared-nothing`

#### Aggregates

##### Aggregate: [Name]

* **Root entity:**
* **Invariants enforced:**
* **Lifecycle:**
* **Allowed operations:**

##### Aggregate: [Name]

* **Root entity:**
* **Invariants enforced:**
* **Lifecycle:**
* **Allowed operations:**

#### Entities

* **[Entity Name]** — description
* **[Entity Name]** — description

#### Value Objects

* **[VO Name]** — description (immutable, equality by value)
* **[VO Name]** — description

#### Domain Services

* **[Service Name]** — purpose, inputs, outputs, side effects

#### Domain Events

* **[Event Name]** — emitted by: …, consumed by: …
* **[Event Name]** — emitted by: …, consumed by: …

#### Business Rules

* See: [`../../memory/permanent/business_rules.md`](../../memory/permanent/business_rules.md)
* Context-specific rules:

#### Invariants

* See: [`../../memory/permanent/invariants.md`](../../memory/permanent/invariants.md)
* Context-specific invariants:

#### Anti-Corruption Layers

* ACL protecting this context from: …

### Context: [Name]

* **Purpose:**
* (Same structure as above.)

---

## Glossary

* See: [`../../memory/permanent/glossary.md`](../../memory/permanent/glossary.md)

## Change Log

| Date       | Change                                          | Author | ADR / Issue |
|------------|-------------------------------------------------|--------|-------------|
| YYYY-MM-DD | Initial scaffold                                |        |             |
|            |                                                 |        |             |

---

> *The domain model is a hypothesis. Update it when reality contradicts it.*