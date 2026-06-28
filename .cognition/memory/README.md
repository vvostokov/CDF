# `memory/` — Project Memory

## Purpose

Project memory is everything the project knows about itself that is **not** in code or identity. It is split by lifetime:

* **Working memory** — short-lived. Reflects the current context.
* **Permanent memory** — long-lived. The project's accumulated knowledge.
* **History** — append-only. What happened, in order.
* **Sessions** — append-only. One entry per AI or human session.
* **Roadmap** — where we are going.

## Structure

```
memory/
├── README.md
├── working/         # Short-lived, frequently replaced
│   ├── current_context.md
│   ├── active_questions.md
│   └── temporary_notes.md
├── permanent/       # Long-lived, monotonically growing
│   ├── glossary.md
│   ├── invariants.md
│   ├── business_rules.md
│   ├── architectural_decisions.md
│   └── domain_knowledge.md
├── history/         # Append-only log
│   ├── decision_log.md
│   └── project_timeline.md
├── sessions/        # Session-by-session journal
│   └── session_log.md
└── roadmap/         # Roadmap and milestones
    ├── roadmap.md
    └── milestones.md
```

## Lifetime Discipline

| Bucket    | Lifetime                    | Replaced?                | Audited?            |
|-----------|-----------------------------|--------------------------|---------------------|
| Working   | Hours to days               | Yes, frequently          | At the end of every iteration |
| Permanent | Years                       | No, only amended via ADR | Quarterly           |
| History   | Forever                     | No                       | Never               |
| Sessions  | Forever                     | No                       | Never               |
| Roadmap   | Months to years             | Updated per milestone    | Per milestone       |

## Promotion Path

```
working/  ──►  permanent/   (via curator)
working/  ──►  history/decision_log.md  (via curator / architect)
sessions/ ──►  history/      (rarely)
working/  ──►  curator/lessons_learned.md  (after each iteration)
```

## AI Protocol

When an AI starts a session:

1. Read `memory/working/current_context.md`.
2. Read `memory/permanent/glossary.md` and `memory/permanent/invariants.md`.
3. Read the most recent `memory/sessions/session_log.md` entries.

When an AI ends a session:

1. Update `memory/working/current_context.md` if the context changed.
2. Append an entry to `memory/sessions/session_log.md`.
3. Promote any durable findings to `memory/permanent/` (proposal — curator approves).

## Recovery From a Cold Start

If everything in working memory is stale or empty, a fresh contributor (human or AI) should be able to recover the project by reading, in order:

1. `.cognition/identity/mission.md`
2. `memory/permanent/glossary.md`
3. `memory/permanent/invariants.md`
4. `memory/permanent/architectural_decisions.md` (or ADRs in `knowledge/architecture-decisions/`)
5. `memory/history/decision_log.md`
6. `memory/roadmap/roadmap.md`
7. `memory/working/current_context.md` (may be stale)
8. Recent `memory/sessions/session_log.md` entries

If those files are insufficient, the project has a knowledge gap. Log it in `curator/lessons_learned.md`.

---

> *Memory is what allows a project to outlive a contributor.*