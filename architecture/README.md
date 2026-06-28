# `architecture/` — Architectural Artifacts

## Purpose

This directory holds **rendered**, human-friendly versions of the architecture: context diagrams, container diagrams, deployment diagrams, sequence diagrams, and the C4 model in text form.

Compare with:

* `.cognition/architect/domain_model.md` — the **summary** model that lives in the cognitive layer.
* `.cognition/architect/system_context.md` — the **summary** system context.
* `knowledge/architecture-decisions/` — the **decisions** themselves (ADRs).

This directory is the **rendered output** — what you would show to a new engineer on day one.

## Structure

```
architecture/
├── README.md
├── context/                # Context-level diagrams and explanations
├── decisions/              # Visual / graphical companion to ADRs
└── diagrams/               # Source files for diagrams (PlantUML, Mermaid, etc.)
```

## Conventions

* Diagrams are stored as **source** (e.g. `.puml`, `.mmd`, `.drawio`) in `diagrams/`.
* Rendered diagrams may be committed as `.svg` / `.png` next to the source, or generated in CI.
* Every diagram has a companion `.md` file in `context/` or `decisions/` that explains what the diagram shows and what is *not* shown.

## AI Behavior

When generating diagrams, the AI must:

1. Use a standard notation (C4, UML, Mermaid).
2. Include a textual explanation in a `.md` file alongside the diagram.
3. Link the diagram to relevant ADRs.

---

> *A diagram is a hypothesis about structure, drawn so it can be questioned.*