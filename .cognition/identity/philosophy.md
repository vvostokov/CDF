---
title: Philosophy
status: draft
last_updated: YYYY-MM-DD
---

# Philosophy

> How we think about software, knowledge, and collaboration.

This document is **opinionated and reflective**. It does not state rules; it states beliefs. The rules live in `principles.md` and `constraints.md`.

---

## Software Is a Conversation Across Time

Software is not a static artifact. It is a conversation between past authors, present maintainers, future contributors, and the people it serves.

When we write code, we are speaking to people we may never meet. The least we can do is be clear.

## Knowledge Is the Project's Most Valuable Asset

Source code without knowledge is a corpse. Knowledge without code is a dream. Both decay without care.

We treat knowledge as a **first-class artifact** — versioned, reviewed, and preserved with the same rigor as production code.

## Architecture Is a Hypothesis

No architecture is permanently correct. All architectures are hypotheses tested by time and change.

We design architectures knowing they will be questioned, extended, and sometimes replaced. The architecture's job is to make those changes safe, intentional, and traceable.

## Reasoning Is Mandatory

We do not make decisions without explaining them. We do not change code without recording why.

The **why** is at least as important as the **what**.

## Complexity Must Earn Its Place

We pay the price of complexity in maintainability. Complexity is allowed only when it earns its place — when simpler alternatives have been considered and rejected with reasons.

> "There are two ways of constructing a software design: One way is to make it so simple that there are obviously no deficiencies, and the other way is to make it so complicated that there are no obvious deficiencies." — C.A.R. Hoare (attrib.)

## Boundaries Are for Thinking

Modules, bounded contexts, and layers are not bureaucratic overhead. They are **cognitive scaffolding**. They let us think about one thing at a time.

## Humans and AI Collaborate

We treat AI as a **collaborator**, not a tool and not an oracle.

* AI must follow the same principles and constraints as humans.
* AI must leave the project **better than it found it**: updated memory, captured knowledge, recorded decisions.
* Humans remain accountable.

## The Project Survives Its Contributors

The goal is not to produce code that depends on its authors. The goal is to produce a project that **continues** — that outlives its current maintainers, that can be read by future engineers (and AIs) without their needing to ask, "why was this done this way?"

## Process Over Heroism

A project that requires heroes to maintain is fragile. We prefer **process over heroism** — explicit roles, documented decisions, repeatable workflows.

## Documentation Is Not Optional

Documentation is not a final step. It is a **continuous practice**, integrated into the work.

If the work is not documented, the work is not done.

---

## Related

* `mission.md` — why we exist.
* `principles.md` — how we operate.
* `values.md` — what we hold dear.
* `non-goals.md` — what we refuse to do.