---
type: "Platform profile"
title: "Langfuse profile"
description: "Column profile for Langfuse in the Observability and evaluation group."
classification: "C1"
owner: "agent:curator"
status: "draft"
review: "pending"
verification: "not applicable"
tags:
  - "observability"
  - "profile"
sources:
  - id: "atlas-catalogue"
    resource: "data/catalog.json"
    locator: "platforms, id langfuse"
generated:
  by: "process:offerings-atlas-ingest"
  at: "2026-10-14T18:00:00+10:00"
---

Langfuse is an open-source (MIT, except ee folders) LLM engineering platform for tracing, evaluation and prompt management, and this research covers Langfuse Cloud (Hobby, Core, Pro, Enterprise) and self-hosted OSS and Enterprise Edition.

Column group: Observability and evaluation. Facts are agent-run under atlas decision 0005. Cells listed as eligible are the only ones agents may retrieve.

## Verdicts and states

| Verdict | Cells |
| --- | --- |
| not-addressed | 33 |
| partial | 9 |
| supported | 2 |

| Verification state | Cells |
| --- | --- |
| unverified | 44 |

## Products

| Product | Party | Description |
| --- | --- | --- |
| Langfuse Cloud | 3p | Managed Langfuse service in US, EU, Japan and HIPAA regions on AWS. |
| Langfuse self-hosted | 3p | Self-hosted Langfuse web, worker, Postgres, ClickHouse, Redis and blob storage, with Enterprise Edition features behind a licence key. |

## Cells

| Control | Category | Verdict | State | Agent-eligible |
| --- | --- | --- | --- | --- |
| [Agent ID](c4-1.md) | Identity | not-addressed | unverified | yes |
| [Credential Brokerage](c4-2.md) | Identity | not-addressed | unverified | yes |
| [Delegation (OBO)](c4-3.md) | Identity | not-addressed | unverified | yes |
| [A2A](c4-4.md) | Identity | not-addressed | unverified | yes |
| [Agent Local Scopes](c1-1.md) | Authorisation | not-addressed | unverified | yes |
| [Agent Remote Scopes](c1-2.md) | Authorisation | not-addressed | unverified | yes |
| [Human Approval](c1-3.md) | Authorisation | not-addressed | unverified | yes |
| [Agent Provisioning](c1-4.md) | Authorisation | not-addressed | unverified | yes |
| [Agent Orchestration](c2-1.md) | Runtime | not-addressed | unverified | yes |
| [Inference](c2-2.md) | Runtime | not-addressed | unverified | yes |
| [Execution Environment](c2-3.md) | Runtime | not-addressed | unverified | yes |
| [Agent In-Session Memory](c2-4.md) | Runtime | not-addressed | unverified | yes |
| [Harness](c2-5.md) | Runtime | not-addressed | unverified | yes |
| [Agent Persistent Memory](c2-6.md) | Runtime | not-addressed | unverified | yes |
| [Model Gateway](c3-1.md) | Mediation / Policy Enforcement | not-addressed | unverified | yes |
| [Tool Gateway](c3-2.md) | Mediation / Policy Enforcement | not-addressed | unverified | yes |
| [Data Gateway](c3-3.md) | Mediation / Policy Enforcement | not-addressed | unverified | yes |
| [A2A Gateway](c3-4.md) | Mediation / Policy Enforcement | not-addressed | unverified | yes |
| [HITL](c5-1.md) | Observability & Explainability | supported | unverified | yes |
| [Behavioural](c5-2.md) | Observability & Explainability | supported | unverified | yes |
| [Cost & Yield](c5-3.md) | Observability & Explainability | partial | unverified | yes |
| [Infrastructure](c5-4.md) | Observability & Explainability | partial | unverified | yes |
| [Connectivity](c5-5.md) | Observability & Explainability | partial | unverified | yes |
| [Administrative Audit](c7-1.md) | Agentic MLSecOps | partial | unverified | yes |
| [SOC Telemetry](c7-2.md) | Agentic MLSecOps | partial | unverified | yes |
| [Model Assurance](c7-3.md) | Agentic MLSecOps | not-addressed | unverified | yes |
| [Runtime Assurance](c7-4.md) | Agentic MLSecOps | not-addressed | unverified | yes |
| [First-Party Tool Assurance](c7-5.md) | Agentic MLSecOps | not-addressed | unverified | yes |
| [Third-Party Tool Assurance](c7-6.md) | Agentic MLSecOps | not-addressed | unverified | yes |
| [Data & Feature Stores](c7-8.md) | Agentic MLSecOps | not-addressed | unverified | yes |
| [AI Discovery](c7-9.md) | Agentic MLSecOps | not-addressed | unverified | yes |
| [Automated AI Pen-Testing](c7-10.md) | Agentic MLSecOps | not-addressed | unverified | yes |
| [Asset Registries & Inventory](c6-1.md) | Governance | partial | unverified | yes |
| [Registration & Approval Workflows](c6-2.md) | Governance | not-addressed | unverified | yes |
| [Posture & Reporting](c6-3.md) | Governance | not-addressed | unverified | yes |
| [Policy Management](c6-4.md) | Governance | not-addressed | unverified | yes |
| [AI Lifecycle Management](c6-5.md) | Governance | partial | unverified | yes |
| [Ownership & Accountability](c6-6.md) | Governance | not-addressed | unverified | yes |
| [Risk Assessment & Classification](c6-7.md) | Governance | not-addressed | unverified | yes |
| [Change & Release Governance](c6-8.md) | Governance | partial | unverified | yes |
| [Exceptions & Risk Acceptance](c6-9.md) | Governance | not-addressed | unverified | yes |
| [Data Lifecycle Governance](c6-10.md) | Governance | partial | unverified | yes |
| [Assurance & Compliance Evidence](c6-11.md) | Governance | not-addressed | unverified | yes |
| [Third-Party Governance](c6-12.md) | Governance | not-addressed | unverified | yes |

Sources are in the [source registry](sources.md).
