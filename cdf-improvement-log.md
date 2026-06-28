# CDF Improvement Log

> A journal of every problem, friction, surprise, or structural question encountered while using CDF in practice.

This file is the **only** basis for evolving CDF. Speculative changes are not accepted.

## How to Use This Log

When you encounter something while using CDF that:

* Forces you to work around the structure,
* Surprises you in a way the manifest did not predict,
* Conflicts with another part of CDF,
* Or feels like it should be a built-in feature,

add an entry below using the template.

Each entry gets an `id`. When CDF's structure is later changed to address an entry, link the change to the entry's `id`.

## Categories

| Code  | Meaning                                                |
|-------|--------------------------------------------------------|
| `STR` | Structural issue — CDF's directory / file structure    |
| `CON` | Convention issue — a rule that does not match practice |
| `PRO` | Process issue — a workflow is missing or unclear       |
| `TMP` | Template issue — an artifact template is missing fields |
| `PMT` | Prompt issue — an AI prompt misleads or fails          |
| `MAN` | Manifest issue — `cdf.manifest.yaml` does not match reality |
| `DOC` | Documentation issue — README or doc is wrong or unclear |

Severity: `low` (cosmetic) | `medium` (friction) | `high` (blocks progress) | `critical` (forces re-architecture).

---

## Entries

<!-- Newest entries go to the top. Use the template below. -->

### YYYY-MM-DD — [Title]

* **ID:** CDF-000
* **Category:** STR | CON | PRO | TMP | PMT | MAN | DOC
* **Severity:** low | medium | high | critical
* **Project:** [project using CDF]
* **Context:** [what you were doing when you encountered this]
* **Observation:** [what went wrong]
* **Expected:** [what the manifest or docs led you to expect]
* **Workaround:** [how you worked around it]
* **Suggested change:** [what should change in CDF — be specific]
* **Status:** open | accepted | deferred | rejected
* **Linked:** [issue, PR, ADR]

---

## Resolved Entries

### CDF-XXX — [Title]

* **Resolved on:** YYYY-MM-DD
* **Resolution:** [what was changed]
* **By:** [PR / commit / discussion link]

---

## Statistics

* **Total entries:** 0
* **By category:** STR: 0, CON: 0, PRO: 0, TMP: 0, PMT: 0, MAN: 0, DOC: 0
* **By severity:** critical: 0, high: 0, medium: 0, low: 0
* **By status:** open: 0, accepted: 0, deferred: 0, rejected: 0

---

> *The log is the project's self-knowledge. The first 10 entries matter more than the next 1000.*