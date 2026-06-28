# Commit Messages

> How the project writes commit messages. Enforced via convention (and sometimes tooling).

## Format

```
<type>(<scope>): <short summary>  (max 72 chars)

<body — wrapped at 72 chars>

<footer — references, breaks, notes>
```

## Types

| Type     | When                                                  |
|----------|-------------------------------------------------------|
| feat     | A new feature                                          |
| fix      | A bug fix                                              |
| docs     | Documentation only                                     |
| refactor | Code change that neither fixes a bug nor adds a feature |
| perf     | Performance change                                     |
| test     | Adding or correcting tests                             |
| ci       | CI / tooling                                            |
| chore    | Maintenance tasks                                      |
| revert   | Reverting a previous change                            |

## Scope

The scope identifies the bounded context or subsystem touched (e.g. `billing`, `identity`, `cognition`, `docs`, `ci`).

## Subject

* Imperative mood ("add", not "added").
* No trailing period.
* Lowercase.

## Body

* Explain **why**, not **what**.
* Wrap at 72 chars.
* Reference ADRs, issues, discussions.

## Footer

* `Refs: #123`
* `Closes #123`
* `BREAKING CHANGE: <description>`

## Examples

```
feat(billing): add order total invariant

Refs: INV-007, ADR-0014
```

```
fix(identity): prevent duplicate user creation under race

Refs: #1234
```

```
docs(cognition): update glossary with new bounded-context terms

Refs: G-002, G-007
```

---

> *A commit message is a letter to the future.*