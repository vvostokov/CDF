---
task: prompt-review
version: 0.1.0
status: active
pairs_with: [reviewer, curator]
---

# Task: Prompt Review

## Mission

Critically review a prompt and recommend improvements — or refuse it as unsuitable for CDF.

## Responsibilities

* Read the prompt.
* Evaluate it against CDF's prompt criteria.
* Produce a structured review.
* Recommend edits or rejection.

## Inputs (must be read first)

1. The role prompt that scopes this task.
2. `.cognition/identity/principles.md`.
3. `.cognition/identity/philosophy.md`.
4. The prompt under review.
5. `prompts/README.md` and the relevant role/task README.

## Outputs

* A structured review (markdown file or PR comment).
* Recommended edits (concrete diffs).
* A verdict: `Accept` | `Request changes` | `Reject`.

## Quality Criteria

* The review is **specific** — not "this is unclear" but "the failure conditions do not cover X".
* The review is **constructive** — every issue has a suggested fix.
* The review is **principle-aligned** — issues are justified against CDF criteria.

## Review Criteria

A CDF prompt must:

1. **Be self-contained.** No reliance on chat history.
2. **Be stack-agnostic.** No language-specific or tool-specific instructions unless justified.
3. **Define role scope.** What the AI may and may not do.
4. **Define inputs.** Which artifacts to read first.
5. **Define outputs.** What to produce, in what location.
6. **Define quality criteria.** What "good" looks like.
7. **Define failure conditions.** When to stop and ask.
8. **Define procedure.** Step-by-step behavior.
9. **Give examples.** Good and bad behavior.

## Verdict Matrix

| Verdict          | When                                                  |
|------------------|-------------------------------------------------------|
| `Accept`         | All criteria met; no improvements needed.             |
| `Request changes`| One or more criteria unmet; fixable.                  |
| `Reject`         | Incompatible with CDF (e.g. proprietary, dangerous).  |

## Procedure

1. Read the inputs.
2. Evaluate each criterion above.
3. Write the review.
4. Recommend the verdict.
5. Submit as a PR comment or as a file under `knowledge/reviews/`.

## Examples of Good Behavior

* "The prompt does not list inputs. Recommendation: add a section 'Inputs (must be read first)' listing the role and task prompts."
* "The prompt includes 'Run pytest for Python tests'. This is stack-specific. Recommendation: replace with 'Run the project's test suite (see `docs/guides/development/testing.md`).'"

## Examples of Bad Behavior (Refuse)

* Approving a prompt without listing failure conditions.
* Rejecting a prompt because "I don't like the wording".

---

> *Prompt review is how the project maintains a high-quality interface with its AI.*