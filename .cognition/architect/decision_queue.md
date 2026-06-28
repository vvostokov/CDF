---
title: Decision Queue
status: active
last_updated: YYYY-MM-DD
owner: architect
---

# Decision Queue

> A short-lived, prioritized list of pending architectural decisions awaiting an ADR.

This is the **front** of the queue. Long-lived decisions live in `knowledge/architecture-decisions/`.

## How This File Works

1. Anyone (human or AI) adds a question as a new entry.
2. The architect prioritizes the queue.
3. The next decision to be made becomes the subject of a proposed ADR.
4. When the ADR is **accepted**, the decision moves to `knowledge/architecture-decisions/`.
5. When the ADR is **rejected**, the queue entry is updated with the reason and closed.
6. Closed entries are archived at the bottom of this file.

## Pending Decisions

### DQ-001 — [Title]

* **Question:**
* **Context:**
* **Candidate options:**
  1. Option A — pros, cons
  2. Option B — pros, cons
  3. Option C — pros, cons
* **Recommended:** Option N — because …
* **Urgency:** `low` | `medium` | `high`
* **Blocks:** [issues / slices / ADRs]
* **Linked:** [discussion, prior notes]

### DQ-002 — [Title]

* **Question:**
* **Context:**
* **Candidate options:**
* **Recommended:**
* **Urgency:**
* **Blocks:**

<!-- Repeat as needed. -->

## Recently Closed

### DQ-000 — [Title] — closed YYYY-MM-DD

* **Outcome:** Accepted / Rejected
* **Reason:**
* **ADR (if accepted):** `knowledge/architecture-decisions/NNNN-*.md`

---

> *A decision queue is architecture's short-term memory. Don't let it grow.*