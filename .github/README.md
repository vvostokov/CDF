# `.github/` — GitHub Configuration

## Purpose

Holds everything GitHub-specific: issue templates, PR templates, label recommendations, discussion recommendations, and (optionally) GitHub Actions workflows.

## Structure

```
.github/
├── README.md                # This file
├── LABELS.md                # Recommended label taxonomy
├── ISSUE_TEMPLATE/
│   ├── config.yml
│   ├── bug-report.md
│   ├── feature-request.md
│   ├── architecture-decision.md
│   ├── knowledge-update.md
│   ├── research.md
│   └── question.md
├── PULL_REQUEST_TEMPLATE/
│   └── pull_request_template.md
└── DISCUSSIONS/
    └── RECOMMENDATIONS.md   # Recommended discussion categories
```

## How to Use

1. Enable Discussions in repository settings.
2. Create the recommended categories per `DISCUSSIONS/RECOMMENDATIONS.md`.
3. Create the recommended labels per `LABELS.md` (or run `scripts/setup-labels.sh`).
4. Verify issue templates by opening a test issue of each type.
5. Verify the PR template by opening a test PR.

## Relationship with AI

The AI does **not** interact with GitHub directly through this directory; it works with the artifacts (issues, PRs, discussions) the templates produce. The templates guide both humans and AI on **what information to provide**.

---

> *Configuration is part of the project. Treat it as such.*