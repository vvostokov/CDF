# `docs/` — Documentation

## Purpose

User-facing and developer-facing documentation. Built to be readable by **humans first**, by **AI second** (but always parseable by both).

## Structure

```
docs/
├── README.md
├── getting-started.md        # First-time setup
├── architecture.md           # Top-level architecture overview (links to architecture/)
├── guides/                   # How-to guides
│   ├── user/                 # For users of the system
│   ├── development/          # For contributors
│   └── operations/           # For operators / SREs
├── conventions/              # Project conventions
│   ├── coding-style.md
│   ├── testing.md
│   ├── commits.md
│   └── tooling.md
└── references/               # Reference documentation
    ├── api.md                # (placeholder; project populates)
    └── ...
```

## Audience Map

| Audience       | Where to look                                              |
|----------------|------------------------------------------------------------|
| Newcomer       | `docs/getting-started.md`, `README.md`                     |
| User           | `docs/guides/user/`                                        |
| Operator       | `docs/guides/operations/`                                  |
| Contributor    | `docs/guides/development/`, `docs/conventions/`, `CONTRIBUTING.md` |
| Architect      | `docs/architecture.md`, `architecture/`, `knowledge/`      |

## Conventions

* Markdown only.
* Cross-link liberally.
* Cite ADRs and invariants.
* Verify every example.

## AI Behavior

When writing or updating docs, the AI must:

1. Use `prompts/tasks/documentation.md`.
2. Match the audience of the doc.
3. Cite ADRs and invariants.
4. Verify code examples.

---

> *Good docs are the cheapest insurance against future chaos.*