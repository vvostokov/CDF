---
title: System Context
status: draft
last_updated: YYYY-MM-DD
owner: architect
---

# System Context

> The system at the level of processes, containers, integrations, and deployment. The complement of `domain_model.md`.

`domain_model.md` describes **what** the system models. This document describes **how** it runs.

## System Overview

<!-- A short paragraph: what is the system, who uses it, how it is deployed. -->

## Containers / Processes

| Process           | Responsibility                           | Tech stack       | Lifecycle |
|-------------------|------------------------------------------|------------------|-----------|
| [process]         |                                          |                  |           |
| [process]         |                                          |                  |           |
| [process]         |                                          |                  |           |

## Deployment Topology

<!-- Where each process runs. -->

* **Production:**
* **Staging:**
* **Local development:**

## External Integrations

| System                | Direction | Protocol | Auth | Owner | Criticality |
|-----------------------|-----------|----------|------|-------|-------------|
| [External system]     | in/out    |          |      |       |             |

## Cross-Cutting Concerns

* **Authentication / Authorization:**
* **Observability (logs, metrics, traces):**
* **Configuration management:**
* **Secret management:**
* **Rate limiting / throttling:**
* **Data retention:**
* **Backup and recovery:**

## Data Stores

| Store            | Purpose         | Technology | Owner | Retention | Backup |
|------------------|-----------------|------------|-------|-----------|--------|
| [store]          |                 |            |       |           |        |

## Networking and Boundaries

* **DMZ / public-facing:**
* **Internal network:**
* **Trust boundaries:**

## Failure Modes and Recovery

| Failure                       | Detection          | Response            | RTO     | RPO     |
|-------------------------------|--------------------|---------------------|---------|---------|
| [failure mode]                |                    |                     |         |         |

## Compliance Surface

* **Data residency:**
* **PII handling:**
* **Audit logging:**
* **Encryption at rest / in transit:**

## Diagrams

<!-- Link or embed diagrams from `architecture/diagrams/`. -->

* [System context diagram (C4 L1)]
* [Container diagram (C4 L2)]
* [Deployment diagram (C4 L3)]

## Change Log

| Date       | Change                             | Author | ADR / Issue |
|------------|------------------------------------|--------|-------------|
| YYYY-MM-DD | Initial scaffold                   |        |             |

---

> *The system context is what an SRE or a new operator reads on day one.*