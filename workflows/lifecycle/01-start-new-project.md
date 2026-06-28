# Workflow 01 — Start a New Project

## Goal

Bring a new project from "blank repo" to "ready to plan its first iteration" while populating the cognitive layer with identity.

## Inputs

* A blank (or near-blank) repository.
* The CDF template (this repository).
* The team's initial intent for the project.

## Outputs

* Populated `.cognition/identity/` (mission, vision, principles, etc.).
* An initial roadmap entry in `.cognition/memory/roadmap/roadmap.md`.
* A first backlog entry in `.cognition/planner/backlog.md`.
* A first entry in `.cognition/memory/sessions/session_log.md`.

## Definition of Done

- [ ] Mission, vision, principles, constraints, philosophy, values, non-goals, and trade-offs are filled in (or marked explicitly `TBD` with a date for completion).
- [ ] The project has a one-sentence description in the root `README.md`.
- [ ] The root `README.md` references `.cognition/identity/`.
- [ ] An initial roadmap theme is recorded.
- [ ] At least one backlog item is recorded.
- [ ] A session log entry records that the project was initialized.

## Responsible Roles

* **Planner** — populates the first backlog and roadmap entry.
* **Architect** — reviews the principles for consistency.
* **Curator** — ensures permanent memory is consistent.
* **Human** — owns the mission and vision.

## Procedure

### Step 1 — Initialize the Repository

1. Click **"Use this template"** on the CDF GitHub repository page (or clone / copy).
2. Rename to the new project's name.
3. Update the root `README.md` with the project name and a one-paragraph description.

### Step 2 — Fill in Identity (in order)

1. `mission.md` — one sentence and a paragraph.
2. `vision.md` — 5- and 10-year views.
3. `principles.md` — adopt CDF's defaults; modify if needed (rare).
4. `constraints.md` — list every hard constraint.
5. `philosophy.md` — adopt CDF's defaults; personalize if needed.
6. `values.md` — adopt CDF's defaults; personalize.
7. `non-goals.md` — list at least 3 explicit non-goals.
8. `tradeoffs.md` — list at least 2 accepted and 2 refused trade-offs.

### Step 3 — Open the First Discussion

Open a GitHub Discussion under **Architecture & Design** titled "Project bootstrap — review identity documents".

### Step 4 — Seed the Roadmap

1. Write the first theme in `.cognition/memory/roadmap/roadmap.md`.
2. Add the first milestone in `.cognition/memory/roadmap/milestones.md`.
3. Add at least one backlog item to `.cognition/planner/backlog.md`.

### Step 5 — Log the Session

Add an entry to `.cognition/memory/sessions/session_log.md` describing the bootstrap.

### Step 6 — Announce

Create a Discussion under **Announcements** titled "Project started" with a link to `.cognition/identity/`.

## Common Pitfalls (Refuse)

* Skipping identity — you will regret it within a month.
* Filling in identity without a real conversation.
* Promising too much in the vision.

---

> *A project without identity is a project without a spine.*