# Diagram Sources

> Source files for diagrams. Rendered SVGs / PNGs live in `architecture/context/` or `architecture/decisions/`.

## Supported Formats

* **PlantUML** — `.puml` / `.plantuml`
* **Mermaid** — `.mmd` / `.mermaid`
* **draw.io** — `.drawio`
* **Structurizr** — `structurizr.json`

## Naming

* `NNNN-kebab-case-name.<ext>` — matches the rendered output.

## How to Render

Use a renderer of your choice (PlantUML CLI, Mermaid CLI, draw.io CLI). A `scripts/render-diagrams.sh` may be provided per project.

## How to Add

1. Create the source file.
2. Add the rendering command to CI (optional but recommended).
3. Reference the diagram from the matching `.md` file.

---

> *Diagrams age like fish; their sources age like wine.*