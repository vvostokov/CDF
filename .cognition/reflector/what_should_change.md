---
title: What Should Change
status: active
last_updated: YYYY-MM-DD
owner: reflector
---

# What Should Change

> Concrete actions that emerge from reflection.

Reflection without action is observation without consequence. This file turns observations from `what_slowed_us.md`, `what_surprised_us.md`, and `wrong_assumptions.md` into **proposed changes**.

## What Goes Here

Each entry has:

* **Date** — when the change was proposed.
* **Origin** — link to the reflection entry that surfaced the need.
* **Proposed change** — what should change, specifically.
* **Target** — where the change should be applied (which file, which role, which process).
* **Owner** — who will carry it out.
* **Priority** — high / medium / low.
* **Status** — proposed / accepted / in-progress / done / rejected.
* **Linked** — issue, ADR, or PR.

## Entries

<!-- Newest at top. -->

### YYYY-MM-DD — [Title]

* **Origin:**
* **Proposed change:**
* **Target:**
* **Owner:**
* **Priority:** high / medium / low
* **Status:** proposed / accepted / in-progress / done / rejected
* **Linked:**

---

## Categories of Change

Changes proposed here may target:

* **Identity** (mission, vision, principles, constraints) — requires an ADR.
* **Kernel** (principles) — requires an ADR.
* **Domain model** (architect role) — direct update by architect.
* **System context** (architect role) — direct update by architect.
* **Invariants / business rules** (memory/permanent) — direct update by curator with architect sign-off.
* **Glossary** (memory/permanent) — direct update by curator.
* **Prompts** (prompts/) — direct update by relevant role.
* **Workflows** (workflows/) — direct update by relevant role.
* **CDF itself** (cdf-improvement-log.md) — proposal to the framework.

## What Does Not Go Here

* Vague intentions ("we should do better").
* Personal process changes (use private feedback).
* Changes that contradict identity or kernel — those require an ADR first.

## From Proposal to Action

When an entry here is **accepted**:

1. The owner carries out the change.
2. The change is linked to its target file via PR.
3. The reflector closes the entry (`Status: done`).
4. The lesson is propagated to `curator/lessons_learned.md` if generally applicable.

---

> *Reflection without action is theatre. Reflection with action is learning.*