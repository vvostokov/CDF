---
title: Knowledge — Conceptual Namespace
status: experimental
last_updated: 2026-06-28
---

# `knowledge/` — Conceptual Namespace

> Static knowledge: what the project **knows**.

This directory is a **conceptual namespace**. It does **not yet contain physical files** — those live in their existing locations and are listed below.

It exists because CDF v1.1 recognizes two fundamental kinds of content in the cognitive layer:

* **Knowledge** — relatively stable, declarative, durable. Answers "what is true".
* **Processes** — dynamic, transformative, evolving. Answers "what is being done".

This README makes the Knowledge side **explicit**. The actual files remain where they are in v1.1 to avoid an unnecessary blast radius across 396 cross-references.

## What Conceptually Belongs to Knowledge

The following existing directories contain **knowledge artifacts** (static content):

| Directory                                          | What it contains                                  |
|----------------------------------------------------|---------------------------------------------------|
| `.cognition/identity/`                             | Mission, vision, principles, constraints, values  |
| `.cognition/memory/`                               | Glossary, invariants, business rules, decisions, history, sessions, roadmap, **reasoning chains** |
| `.cognition/epistemology/`                         | How the project knows (new in v1.1)              |
| `.cognition/guides/`                               | Reading order, working-with-cognition (static)   |

## What Conceptually Belongs Elsewhere (Processes)

The following directories contain **processes** — they transform knowledge:

| Directory                                          | What it does                                      |
|----------------------------------------------------|---------------------------------------------------|
| `.cognition/planner/`                              | Transforms goals into iterations and slices       |
| `.cognition/architect/`                            | Transforms knowledge into design                  |
| `.cognition/developer/`                           | Transforms design into implementation             |
| `.cognition/reviewer/`                             | Transforms changes into integrity                |
| `.cognition/curator/`                              | Transforms knowledge into durable artifacts       |
| `.cognition/researcher/`                           | Transforms unknowns into findings                 |
| `.cognition/reflector/`                            | Transforms experience into lessons (new in v1.1) |

## Why No Physical Migration Yet

Physical migration would require:

* Moving ~30 directories.
* Updating ~396 cross-references across 77 files.
* Risking subtle breakage in paths that escape detection.

That work would consume effort disproportionate to its value **at this stage**. The conceptual separation, documented here and in `cdf.manifest.yaml`, achieves the **cognitive** benefit without the **filesystem** risk.

## When to Migrate Physically

A physical migration should be considered when:

* A real project (e.g. Zhamlik) demonstrates that the conceptual separation is **insufficient** — i.e., people keep confusing knowledge with processes despite the conceptual namespace.
* The number of cross-references has **grown** significantly (today's blast radius is contained; in a year it may be 1000+).
* Tooling is being built that depends on the directory structure.

Until one of these signals appears, the conceptual namespace is enough.

## Tracking

This decision is recorded in `cdf-improvement-log.md`:

* **CDF-001** — Knowledge and processes are mixed at the same conceptual level.
* **Status:** accepted as a conceptual separation.
* **Physical migration:** deferred until evidence demands it.

## Related

* `.cognition/processes/README.md` — the counterpart namespace.
* `cdf-improvement-log.md` — entry CDF-001.
* `cdf.manifest.yaml` — declarative description of CDF v1.1.