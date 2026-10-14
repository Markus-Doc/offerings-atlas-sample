---
type: "Platform profile"
title: "OneTrust AI Governance profile"
description: "Column profile for OneTrust AI Governance in the AI governance and risk group."
classification: "C1"
owner: "agent:curator"
status: "draft"
review: "pending"
verification: "not applicable"
tags:
  - "ai-governance"
  - "profile"
sources:
  - id: "atlas-catalogue"
    resource: "data/catalog.json"
    locator: "platforms, id onetrust"
generated:
  by: "process:offerings-atlas-ingest"
  at: "2026-10-14T18:00:00+10:00"
---

OneTrust's SaaS AI governance solution for AI inventory, risk assessment, policy and compliance automation, covering the AI Governance product, its runtime controls (AI Policy Engine, AI Guard SDK, CORIE) and the linked Third-Party Management module as documented on onetrust.com and developer.onetrust.com.

Column group: AI governance and risk. Facts are agent-run under atlas decision 0005. Cells listed as eligible are the only ones agents may retrieve.

## Verdicts and states

| Verdict | Cells |
| --- | --- |
| not-addressed | 18 |
| partial | 16 |
| supported | 9 |
| unresolved | 1 |

| Verification state | Cells |
| --- | --- |
| unverified | 44 |

## Products

| Product | Party | Description |
| --- | --- | --- |
| OneTrust AI Governance | 3p | AI registry, discovery, risk assessment, policy management, workflows and evidence for models, agents, datasets and AI vendors. |
| OneTrust AI Guard | 3p | Python SDK and Light Worker Node classification service that allows, redacts or blocks sensitive data in prompts and responses. |
| OneTrust CORIE and AI Control Plane | 3p | Platform intelligence layer announced September 2026 that enforces policy at agent tool calls and records decisions in an Evidence Ledger. |
| OneTrust Third-Party Management | 3p | Vendor intake, tiering, assessment and continuous monitoring module used alongside AI Governance for third-party AI. |

## Cells

| Control | Category | Verdict | State | Agent-eligible |
| --- | --- | --- | --- | --- |
| [Agent ID](c4-1.md) | Identity | partial | unverified | yes |
| [Credential Brokerage](c4-2.md) | Identity | not-addressed | unverified | yes |
| [Delegation (OBO)](c4-3.md) | Identity | not-addressed | unverified | yes |
| [A2A](c4-4.md) | Identity | not-addressed | unverified | yes |
| [Agent Local Scopes](c1-1.md) | Authorisation | not-addressed | unverified | yes |
| [Agent Remote Scopes](c1-2.md) | Authorisation | partial | unverified | yes |
| [Human Approval](c1-3.md) | Authorisation | partial | unverified | yes |
| [Agent Provisioning](c1-4.md) | Authorisation | partial | unverified | yes |
| [Agent Orchestration](c2-1.md) | Runtime | not-addressed | unverified | yes |
| [Inference](c2-2.md) | Runtime | not-addressed | unverified | yes |
| [Execution Environment](c2-3.md) | Runtime | not-addressed | unverified | yes |
| [Agent In-Session Memory](c2-4.md) | Runtime | not-addressed | unverified | yes |
| [Harness](c2-5.md) | Runtime | not-addressed | unverified | yes |
| [Agent Persistent Memory](c2-6.md) | Runtime | not-addressed | unverified | yes |
| [Model Gateway](c3-1.md) | Mediation / Policy Enforcement | not-addressed | unverified | yes |
| [Tool Gateway](c3-2.md) | Mediation / Policy Enforcement | partial | unverified | yes |
| [Data Gateway](c3-3.md) | Mediation / Policy Enforcement | partial | unverified | yes |
| [A2A Gateway](c3-4.md) | Mediation / Policy Enforcement | not-addressed | unverified | yes |
| [HITL](c5-1.md) | Observability & Explainability | partial | unverified | yes |
| [Behavioural](c5-2.md) | Observability & Explainability | partial | unverified | yes |
| [Cost & Yield](c5-3.md) | Observability & Explainability | partial | unverified | yes |
| [Infrastructure](c5-4.md) | Observability & Explainability | not-addressed | unverified | yes |
| [Connectivity](c5-5.md) | Observability & Explainability | partial | unverified | yes |
| [Administrative Audit](c7-1.md) | Agentic MLSecOps | partial | unverified | yes |
| [SOC Telemetry](c7-2.md) | Agentic MLSecOps | unresolved | unverified | yes |
| [Model Assurance](c7-3.md) | Agentic MLSecOps | partial | unverified | yes |
| [Runtime Assurance](c7-4.md) | Agentic MLSecOps | not-addressed | unverified | yes |
| [First-Party Tool Assurance](c7-5.md) | Agentic MLSecOps | not-addressed | unverified | yes |
| [Third-Party Tool Assurance](c7-6.md) | Agentic MLSecOps | not-addressed | unverified | yes |
| [Data & Feature Stores](c7-8.md) | Agentic MLSecOps | partial | unverified | yes |
| [AI Discovery](c7-9.md) | Agentic MLSecOps | supported | unverified | yes |
| [Automated AI Pen-Testing](c7-10.md) | Agentic MLSecOps | not-addressed | unverified | yes |
| [Asset Registries & Inventory](c6-1.md) | Governance | supported | unverified | yes |
| [Registration & Approval Workflows](c6-2.md) | Governance | supported | unverified | yes |
| [Posture & Reporting](c6-3.md) | Governance | supported | unverified | yes |
| [Policy Management](c6-4.md) | Governance | supported | unverified | yes |
| [AI Lifecycle Management](c6-5.md) | Governance | supported | unverified | yes |
| [Ownership & Accountability](c6-6.md) | Governance | supported | unverified | yes |
| [Risk Assessment & Classification](c6-7.md) | Governance | supported | unverified | yes |
| [Change & Release Governance](c6-8.md) | Governance | partial | unverified | yes |
| [Exceptions & Risk Acceptance](c6-9.md) | Governance | partial | unverified | yes |
| [Data Lifecycle Governance](c6-10.md) | Governance | not-addressed | unverified | yes |
| [Assurance & Compliance Evidence](c6-11.md) | Governance | supported | unverified | yes |
| [Third-Party Governance](c6-12.md) | Governance | partial | unverified | yes |

Sources are in the [source registry](sources.md).
