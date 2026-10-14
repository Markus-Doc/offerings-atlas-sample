---
type: "Platform profile"
title: "Anthropic profile"
description: "Column profile for Anthropic in the Frontier AI providers group."
classification: "C1"
owner: "agent:curator"
status: "draft"
review: "pending"
verification: "not applicable"
tags:
  - "frontier-ai"
  - "profile"
sources:
  - id: "atlas-catalogue"
    resource: "data/catalog.json"
    locator: "platforms, id anthropic"
generated:
  by: "process:offerings-atlas-ingest"
  at: "2026-10-14T18:00:00+10:00"
---

Claude APIs, Agent SDK, Claude Code and Managed Agents beta. Hosted and self-hosted responsibilities are assessed separately.

Column group: Frontier AI providers. Facts are agent-run under atlas decision 0005. Cells listed as eligible are the only ones agents may retrieve.

## Verdicts and states

| Verdict | Cells |
| --- | --- |
| partial | 37 |
| supported | 5 |
| unresolved | 2 |

| Verification state | Cells |
| --- | --- |
| unverified | 40 |
| verified | 4 |

## Products

| Product | Party | Description |
| --- | --- | --- |
| Claude Code | 1p | Named scope from research/platforms/anthropic.md, checked in that research on 2026-10-07. Product-specific capability assessment and route availability remain unverified. |
| Managed Agents | 1p | Named scope from research/platforms/anthropic.md, checked in that research on 2026-10-07. Product-specific capability assessment and route availability remain unverified. |

## Cells

| Control | Category | Verdict | State | Agent-eligible |
| --- | --- | --- | --- | --- |
| [Agent ID](c4-1.md) | Identity | partial | unverified | yes |
| [Credential Brokerage](c4-2.md) | Identity | partial | unverified | yes |
| [Delegation (OBO)](c4-3.md) | Identity | partial | unverified | yes |
| [A2A](c4-4.md) | Identity | partial | unverified | yes |
| [Agent Local Scopes](c1-1.md) | Authorisation | partial | verified | yes |
| [Agent Remote Scopes](c1-2.md) | Authorisation | partial | verified | yes |
| [Human Approval](c1-3.md) | Authorisation | supported | verified | yes |
| [Agent Provisioning](c1-4.md) | Authorisation | partial | unverified | no |
| [Agent Orchestration](c2-1.md) | Runtime | supported | unverified | no |
| [Inference](c2-2.md) | Runtime | supported | unverified | no |
| [Execution Environment](c2-3.md) | Runtime | partial | verified | yes |
| [Agent In-Session Memory](c2-4.md) | Runtime | supported | unverified | no |
| [Harness](c2-5.md) | Runtime | supported | unverified | yes |
| [Agent Persistent Memory](c2-6.md) | Runtime | partial | unverified | yes |
| [Model Gateway](c3-1.md) | Mediation / Policy Enforcement | partial | unverified | yes |
| [Tool Gateway](c3-2.md) | Mediation / Policy Enforcement | partial | unverified | yes |
| [Data Gateway](c3-3.md) | Mediation / Policy Enforcement | partial | unverified | yes |
| [A2A Gateway](c3-4.md) | Mediation / Policy Enforcement | unresolved | unverified | yes |
| [HITL](c5-1.md) | Observability & Explainability | partial | unverified | yes |
| [Behavioural](c5-2.md) | Observability & Explainability | partial | unverified | yes |
| [Cost & Yield](c5-3.md) | Observability & Explainability | partial | unverified | yes |
| [Infrastructure](c5-4.md) | Observability & Explainability | partial | unverified | yes |
| [Connectivity](c5-5.md) | Observability & Explainability | partial | unverified | yes |
| [Administrative Audit](c7-1.md) | Agentic MLSecOps | partial | unverified | yes |
| [SOC Telemetry](c7-2.md) | Agentic MLSecOps | partial | unverified | yes |
| [Model Assurance](c7-3.md) | Agentic MLSecOps | partial | unverified | yes |
| [Runtime Assurance](c7-4.md) | Agentic MLSecOps | partial | unverified | yes |
| [First-Party Tool Assurance](c7-5.md) | Agentic MLSecOps | partial | unverified | yes |
| [Third-Party Tool Assurance](c7-6.md) | Agentic MLSecOps | partial | unverified | yes |
| [Data & Feature Stores](c7-8.md) | Agentic MLSecOps | partial | unverified | yes |
| [AI Discovery](c7-9.md) | Agentic MLSecOps | partial | unverified | yes |
| [Automated AI Pen-Testing](c7-10.md) | Agentic MLSecOps | unresolved | unverified | yes |
| [Asset Registries & Inventory](c6-1.md) | Governance | partial | unverified | yes |
| [Registration & Approval Workflows](c6-2.md) | Governance | partial | unverified | yes |
| [Posture & Reporting](c6-3.md) | Governance | partial | unverified | yes |
| [Policy Management](c6-4.md) | Governance | partial | unverified | yes |
| [AI Lifecycle Management](c6-5.md) | Governance | partial | unverified | yes |
| [Ownership & Accountability](c6-6.md) | Governance | partial | unverified | yes |
| [Risk Assessment & Classification](c6-7.md) | Governance | partial | unverified | yes |
| [Change & Release Governance](c6-8.md) | Governance | partial | unverified | yes |
| [Exceptions & Risk Acceptance](c6-9.md) | Governance | partial | unverified | yes |
| [Data Lifecycle Governance](c6-10.md) | Governance | partial | unverified | no |
| [Assurance & Compliance Evidence](c6-11.md) | Governance | partial | unverified | no |
| [Third-Party Governance](c6-12.md) | Governance | partial | unverified | yes |

Sources are in the [source registry](sources.md).
