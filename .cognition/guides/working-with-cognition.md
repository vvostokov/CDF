# Working with the Cognitive Layer

> A guide for **humans and AI** on how to work with `.cognition/`.

## The 30-Second Tour

```
.cognition/
├── identity/                # Who we are
├── planner/                 # What we're doing now
├── architect/               # How it's structured
├── developer/               # What we're building
├── reviewer/                # What we're catching
├── curator/                 # What we're remembering
├── researcher/              # What we're investigating
└── memory/
    ├── working/             # The here-and-now
    ├── permanent/           # The forever-now
    ├── history/             # The past
    ├── sessions/            # Session-by-session log
    └── roadmap/             # Where we're going
```

## Reading Order for a New Contributor

1. `identity/mission.md` — why the project exists.
2. `identity/principles.md` — how it operates.
3. `identity/constraints.md` — what it cannot violate.
4. `memory/working/current_context.md` — what is happening now.
5. `memory/permanent/glossary.md` — what the words mean.
6. `memory/permanent/invariants.md` — what must always be true.
7. `memory/permanent/architectural_decisions.md` — what has been decided.

## Updating Order for a Working Session

1. Read what's there (working memory + relevant permanent memory).
2. Do the work.
3. Update `current_task.md` and / or the relevant role file.
4. Promote durable findings to permanent memory.
5. Append a session log entry.

## AI Workflow

When an AI starts a session:

1. Load the role prompt (`prompts/roles/<role>.md`).
2. Load the task prompt (`prompts/tasks/<task>.md`).
3. Read the listed inputs (identity, working memory, permanent memory, slice / plan).
4. Produce the output (per the role/task prompt's "Outputs" section).
5. Update `.cognition/memory/working/current_context.md`.
6. Append to `.cognition/memory/sessions/session_log.md`.

## Anti-Patterns

* Silently contradicting an invariant.
* Skipping the cognitive-layer update at the end of a session.
* Letting working memory grow past a page or two.

---

> *The cognitive layer is the project's biggest asset. Treat it with care.*