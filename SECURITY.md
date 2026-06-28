# Security Policy

The Cognitive Development Framework (CDF) is a **template repository** containing markdown content, prompts, workflows, and templates. It does not ship executable application code, so the traditional attack surface is small. Nevertheless, we take security seriously.

## Supported Versions

| Version | Supported          |
|---------|--------------------|
| 0.1.x   | ✅ Yes              |
| < 0.1   | ❌ No               |

## Reporting a Vulnerability

**Please do not open a public GitHub Issue for security vulnerabilities.**

Instead, report privately by emailing the maintainers at the address listed in the repository's commit history or by using GitHub's [private vulnerability reporting](https://docs.github.com/en/code-security/security-advisories/guidance-on-reporting-and-writing-information-about-vulnerabilities/privately-reporting-a-security-vulnerability) feature.

You should receive an acknowledgment within **72 hours**.

## What to Include

When reporting, please include:

* A clear description of the vulnerability.
* Steps to reproduce.
* Potential impact.
* Suggested mitigation (if you have one).

## What to Expect

* **Acknowledgment** within 72 hours.
* **Triage** within 7 days — confirmed, declined, or needs more info.
* **Fix** coordinated with you, with credit in the changelog (unless you prefer anonymity).
* **Disclosure** published after the fix lands.

## Scope

In-scope for security reports:

* Malicious content injected into CDF templates that could harm downstream projects (e.g. dangerous prompt-injection patterns, unsafe scripts).
* Vulnerabilities in `scripts/` utilities shipped with CDF.
* Privacy or credential leaks in any committed file.

Out-of-scope:

* Issues in third-party tools referenced by CDF documentation.
* Social-engineering attacks against maintainers.
* Theoretical concerns without a reproducible scenario.

## Safe Use of CDF

CDF encourages the use of AI assistants. When applying prompts from `prompts/`:

* Treat all AI output as **untrusted** until reviewed by a human.
* Do not paste secrets, credentials, or PII into prompts.
* Review prompt templates before using them in production contexts.

---

> Security is a property of the system, not an afterthought. The same is true of CDF.