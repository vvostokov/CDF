# GitHub Discussions — Recommended Categories

CDF projects use GitHub Discussions for **open-ended, pre-decision conversations**. Issues are for well-defined work; Discussions are for thinking out loud.

## Recommended Categories

### 📣 Announcements
* **Purpose:** Maintainer-only announcements: releases, breaking changes, roadmap shifts.
* **Who posts:** Maintainers.
* **Examples:** "v1.0 released", "CFP for the next major version".

### 🏛️ Architecture & Design
* **Purpose:** Propose and debate architectural changes before they become ADRs.
* **Who posts:** Anyone.
* **Lifecycle:** A discussion may be promoted to an ADR via PR once consensus emerges.
* **Examples:** "Should we move to event sourcing?", "Trade-offs between monolith and modular monolith".

### 💡 Ideas
* **Purpose:** Propose new features, enhancements, or experiments that are not yet ready for an issue.
* **Who posts:** Anyone.
* **Examples:** "It would be cool if …", "Could we add a CLI for …".

### 🙏 Q&A
* **Purpose:** Questions about how to use the project, framework, or specific subsystems.
* **Who posts:** Anyone.
* **Examples:** "How do I add a new bounded context?", "What does this ADR mean?".

### 📚 Show and Tell
* **Purpose:** Share what you have built, learned, or discovered using the project.
* **Who posts:** Anyone.
* **Examples:** "I used CDF to bootstrap a 10-year-old legacy rewrite", "Lessons from running CDF in a team of 50".

### 🧠 Knowledge & Process
* **Purpose:** Discuss the cognitive layer itself — prompts, workflows, templates.
* **Who posts:** Anyone.
* **Examples:** "Should the curator role merge with reviewer?", "Best way to capture architectural drift".

### 🗳️ Polls
* **Purpose:** Lightweight votes on small decisions.
* **Who posts:** Anyone.
* **Examples:** "Which prompt format do you prefer?", "Vote on next quarter's priorities".

## How a Discussion Becomes a Decision

```
Discussion (open-ended, exploratory)
       │
       ▼  consensus forms
Decision Proposal (Issue or PR with ADR template)
       │
       ▼  accepted
ADR (`knowledge/architecture-decisions/NNNN-*.md`)
       │
       ▼  implementation
Code + Tests + Updated `.cognition/`
```

## Rules of Engagement

* **Be specific.** "This is bad" is not a discussion.
* **Cite artifacts.** Link to ADRs, issues, code, or external references.
* **Stay on topic.** Off-topic branches should split into new discussions.
* **Disagree gracefully.** Disagreement is welcome; disrespect is not.
* **Close loops.** When a discussion results in a decision, link to the resulting artifact.

---

> Discussions are the project's water-cooler, courtroom, and architecture review board — all in one. Use them well.