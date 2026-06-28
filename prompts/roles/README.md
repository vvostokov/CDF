# Role Prompts

## Purpose

A **role prompt** defines who the AI is acting as. It constrains what the AI may decide, what artifacts it may produce, and what it must refuse to do.

## Available Roles

| Role         | Prompt                            | Owns                                                       |
|--------------|-----------------------------------|------------------------------------------------------------|
| Planner      | [`planner.md`](./planner.md)      | Goals, iterations, backlog, vertical slices                |
| Architect    | [`architect.md`](./architect.md)  | Domain model, system context, ADRs, decision queue         |
| Developer    | [`developer.md`](./developer.md)  | Implementation plan, current task, code                    |
| Reviewer     | [`reviewer.md`](./reviewer.md)    | Review reports, technical debt, architecture reviews      |
| Curator      | [`curator.md`](./curator.md)      | Glossary, knowledge updates, lessons learned               |
| Researcher   | [`researcher.md`](./researcher.md)| Research notes, experiments, dead ends                     |

## How to Use

1. Pick **one** role.
2. Pair it with **one or more** task prompts (`../tasks/`).
3. Provide the **context** (which `.cognition/` files to read).
4. Run.

## Multi-Role Sequences

When the work crosses roles:

1. **Plan** → planner + task: planning.
2. **Design** → architect + tasks: decision-proposal, ADR.
3. **Implement** → developer + tasks: implementation, testing.
4. **Review** → reviewer + task: code-review.
5. **Curate** → curator + tasks: knowledge-update.

Each transition updates `.cognition/memory/working/current_context.md`.

---

> *Roles are hats. Wear one at a time. Take it off cleanly.*