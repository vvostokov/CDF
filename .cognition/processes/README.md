---
title: Processes — Conceptual Namespace
status: experimental
last_updated: 2026-06-28
---

# `processes/` — Conceptual Namespace

> Dynamic processes: what the project **does**.

This directory is a **conceptual namespace**. It does **not yet contain physical files** — those live in their existing locations and are listed below.

It exists because CDF v1.1 distinguishes two fundamental kinds of content:

* **Knowledge** — relatively stable. Answers "what is true".
* **Processes** — dynamic, transformative, evolving. Answers "what is being done".

This README makes the Processes side **explicit**. The actual role directories remain where they are in v1.1 to avoid a filesystem-wide migration.

## What Conceptually Belongs to Processes

The following existing directories are **processes** — they transform knowledge:

| Directory                                          | What it does                                      |
|----------------------------------------------------|---------------------------------------------------|
| `.cognition/planner/`                              | Transforms goals into iterations and slices       |
| `.cognition/architect/`                            | Transforms knowledge into design                  |
| `.cognition/developer/`                           | Transforms design into implementation             |
| `.cognition/reviewer/`                             | Transforms changes into integrity                |
| `.cognition/curator/`                              | Transforms knowledge into durable artifacts       |
| `.cognition/researcher/`                           | Transforms unknowns into findings                 |
| `.cognition/reflector/`                            | Transforms experience into lessons (new in v1.1) |

## What Conceptually Belongs Elsewhere (Knowledge)

The following contain **knowledge artifacts**:

| Directory                                          | What it contains                                  |
|----------------------------------------------------|---------------------------------------------------|
| `.cognition/identity/`                             | Mission, vision, principles, constraints, values  |
| `.cognition/memory/`                               | Glossary, invariants, business rules, decisions, history, sessions, roadmap, reasoning chains |
| `.cognition/epistemology/`                         | How the project knows (new in v1.1)              |
| `.cognition/guides/`                               | Reading order, working-with-cognition (static)   |

## Process vs. Knowledge — The Distinction

A useful test:

> *"If this file disappeared, would the project still know what it knows?"*

* If **yes** — it is knowledge.
* If **no** — it is a process (the project's ability to do work depends on it).

A glossary disappearing is annoying but the project still knows its domain. The curator role disappearing means the project loses the ability to maintain its knowledge — but it doesn't lose the knowledge itself.

## Why No Physical Migration Yet

A physical migration would require moving 30+ directories and updating 396 cross-references. That risk is **not justified** at this stage by the conceptual benefit.

See `.cognition/knowledge/README.md` for the rationale.

## When to Migrate Physically

See `.cognition/knowledge/README.md`. The criteria are the same.

## The Actor / Role Distinction

Roles (this directory's contents) define **what to do**. Actors define **who does it**. The two are deliberately decoupled:

* **Roles:** planner, architect, developer, reviewer, curator, researcher, reflector.
* **Actors:** human, LLM (ChatGPT, Claude, Hermes, Gemini, OpenCode), automation, CI, future AI_OS.

A single actor may perform multiple roles. A single role may be performed by multiple actors. The role prompts in `prompts/roles/` are **actor-agnostic** — they specify responsibilities, not who carries them out.

This is logged in `cdf-improvement-log.md`:

* **CDF-006** — Actor and Role are different concepts.
* **Status:** deferred (a convention, not a structure).

## Related

* `.cognition/knowledge/README.md` — the counterpart namespace.
* `cdf-improvement-log.md` — entry CDF-001, CDF-006.
* `cdf.manifest.yaml` — declarative description of CDF v1.1.