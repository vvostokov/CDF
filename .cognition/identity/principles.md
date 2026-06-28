---
title: Principles
status: draft
last_updated: YYYY-MM-DD
---

# Core Principles

> Non-negotiable engineering principles. Every decision must be defensible against these.

These principles are **stable**. They define how the project thinks. Any deviation requires an explicit justification recorded in an ADR.

---

## 1. Architecture Before Implementation

We design before we code. We do not write code for which there is no architectural intent.

* We do not "fix it later".
* We do not assume implementation will reveal architecture.
* Every non-trivial change begins with an architectural consideration.

**Test:** Can you point to the architectural artifact (model, ADR, design note) that motivates this code?

## 2. Knowledge Before Code

We capture knowledge before, during, and after writing code. We do not commit code that we cannot explain.

* Code without explanation is technical debt by definition.
* Knowledge is a **first-class artifact**.

**Test:** Could a new engineer (or AI) understand this code in 2 years without the author present?

## 3. Reasoning Before Optimization

We optimize only after we have measured and reasoned. We do not optimize for hypothetical futures.

* Premature optimization is the enemy of clarity.
* Performance work follows an explicit benchmark.

**Test:** Is there a measured reason to optimize, or a stated hypothesis with a falsifiable prediction?

## 4. Project Memory Before Convenience

We preserve project memory even when it is inconvenient.

* Memory loss is unrecoverable. Refactoring is recoverable.
* We pay the cost of documentation now to avoid the cost of rediscovering later.

**Test:** If everyone left today, would the project survive?

## 5. Explicit Over Implicit

We choose explicit over implicit, even when implicit is faster.

* Implicit dependencies are bugs waiting to happen.
* Implicit assumptions are wrong assumptions waiting to be discovered.

**Test:** Could a stranger understand this code without asking the author a question?

## 6. Documented Over Assumed

If it is not documented, it does not exist.

* Tribal knowledge is a liability.
* Undocumented invariants are broken invariants.

**Test:** Is this behavior, decision, or constraint captured in a stable document?

## 7. Small Over Clever

We prefer small, boring, correct solutions over clever, compact, surprising ones.

* Cleverness ages poorly.
* Simplicity scales.

**Test:** Could a competent engineer read this without a cup of coffee?

## 8. Reversible Over Irreversible

When given a choice, we prefer reversible decisions.

* Reversible decisions can be made quickly.
* Irreversible decisions require care, ADRs, and review.

**Test:** If this decision turns out to be wrong, how expensive is the reversal?

## 9. Boundaries Are Sacred

We respect bounded contexts, module boundaries, and layering.

* Cross-cutting changes must be justified.
* "Just this once" is the first step toward spaghetti.

**Test:** Does this change respect the existing boundaries?

## 10. Trust Through Verification

We trust, but verify. Tests, reviews, and benchmarks are how we make trust durable.

* Code is correct because it is verified, not because it was written carefully.
* Reviews are conversations, not approvals.

**Test:** Is there a test or a check that proves this is correct?

---

## How to Use This Document

When proposing a change:

* Quote the relevant principle.
* Explain how the change aligns with it.
* If the change **violates** a principle, propose an ADR that explicitly accepts the violation.

When reviewing a change:

* Check each principle.
* If a principle is violated, ask for an explicit justification.

## Related

* `philosophy.md` — how we think about software.
* `constraints.md` — hard limits we cannot cross.
* `non-goals.md` — what we explicitly do not do.