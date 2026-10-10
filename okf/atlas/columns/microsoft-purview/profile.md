---
type: "Platform profile"
title: "Microsoft Purview (DSPM for AI, Compliance Manager) profile"
description: "Column profile for Microsoft Purview (DSPM for AI, Compliance Manager) in the Data security for AI group."
classification: "C1"
owner: "agent:curator"
status: "draft"
review: "pending"
verification: "not applicable"
tags:
  - "data-security"
  - "profile"
sources:
  - id: "atlas-catalogue"
    resource: "data/catalog.json"
    locator: "platforms, id microsoft-purview"
generated:
  by: "process:offerings-atlas-ingest"
  at: "2026-10-10T18:00:00+10:00"
---

Microsoft's data security and compliance suite as it applies to Copilot, Agent 365, Copilot Studio, Foundry, Fabric data agents and third-party AI apps, covering Data Security Posture Management (current and DSPM for AI classic), Compliance Manager, Audit, DLP, Insider Risk Management, Communication Compliance, eDiscovery, Data Lifecycle Management, the Purview APIs and SDK, and Unified Catalog as documented on Microsoft Learn.

Column group: Data security for AI. Facts are agent-run under atlas decision 0005. Cells listed as eligible are the only ones agents may retrieve.

## Verdicts and states

| Verdict | Cells |
| --- | --- |
| not-addressed | 24 |
| partial | 15 |
| supported | 5 |

| Verification state | Cells |
| --- | --- |
| unverified | 44 |

## Products

| Product | Party | Description |
| --- | --- | --- |
| Microsoft Purview APIs in Microsoft Graph and Purview SDK | 3p | processContent and protection scope APIs and Agent Framework middleware that bring Purview policies into custom AI apps. |
| Microsoft Purview Audit (Standard and Premium) | 3p | Unified audit log capturing Copilot and AI app interactions with retention policies and API export. |
| Microsoft Purview Compliance Manager | 3p | Regulatory assessments including EU AI Act, ISO/IEC 42001, ISO/IEC 23894 and NIST AI RMF templates, improvement actions, evidence and Foundry evaluation sync. |
| Microsoft Purview Communication Compliance, eDiscovery and Data Lifecycle Management | 3p | Review, search, hold, retention and deletion of AI prompts and responses. |
| Microsoft Purview Data Loss Prevention | 3p | DLP policies for the Microsoft 365 Copilot location, endpoints, network and agent instances, plus sensitivity labels. |
| Microsoft Purview Data Security Posture Management (including DSPM for AI classic) | 3p | Posture dashboard, AI observability inventory, activity explorer, data risk assessments and one-click policies for AI apps and agents. |
| Microsoft Purview Insider Risk Management | 3p | Risk scoring policies including the Risky AI usage and Risky Agents templates. |
| Microsoft Purview Unified Catalog | 3p | Data governance catalog with governance domains, data products, access policies and data quality. |

## Cells

| Control | Category | Verdict | State | Agent-eligible |
| --- | --- | --- | --- | --- |
| [Agent ID](c4-1.md) | Identity | not-addressed | unverified | yes |
| [Credential Brokerage](c4-2.md) | Identity | not-addressed | unverified | yes |
| [Delegation (OBO)](c4-3.md) | Identity | not-addressed | unverified | yes |
| [A2A](c4-4.md) | Identity | not-addressed | unverified | yes |
| [Agent Local Scopes](c1-1.md) | Authorisation | not-addressed | unverified | yes |
| [Agent Remote Scopes](c1-2.md) | Authorisation | partial | unverified | yes |
| [Human Approval](c1-3.md) | Authorisation | not-addressed | unverified | yes |
| [Agent Provisioning](c1-4.md) | Authorisation | not-addressed | unverified | yes |
| [Agent Orchestration](c2-1.md) | Runtime | not-addressed | unverified | yes |
| [Inference](c2-2.md) | Runtime | not-addressed | unverified | yes |
| [Execution Environment](c2-3.md) | Runtime | not-addressed | unverified | yes |
| [Agent In-Session Memory](c2-4.md) | Runtime | not-addressed | unverified | yes |
| [Harness](c2-5.md) | Runtime | not-addressed | unverified | yes |
| [Agent Persistent Memory](c2-6.md) | Runtime | not-addressed | unverified | yes |
| [Model Gateway](c3-1.md) | Mediation / Policy Enforcement | partial | unverified | yes |
| [Tool Gateway](c3-2.md) | Mediation / Policy Enforcement | partial | unverified | yes |
| [Data Gateway](c3-3.md) | Mediation / Policy Enforcement | supported | unverified | yes |
| [A2A Gateway](c3-4.md) | Mediation / Policy Enforcement | not-addressed | unverified | yes |
| [HITL](c5-1.md) | Observability & Explainability | partial | unverified | yes |
| [Behavioural](c5-2.md) | Observability & Explainability | partial | unverified | yes |
| [Cost & Yield](c5-3.md) | Observability & Explainability | not-addressed | unverified | yes |
| [Infrastructure](c5-4.md) | Observability & Explainability | not-addressed | unverified | yes |
| [Connectivity](c5-5.md) | Observability & Explainability | partial | unverified | yes |
| [Administrative Audit](c7-1.md) | Agentic MLSecOps | partial | unverified | yes |
| [SOC Telemetry](c7-2.md) | Agentic MLSecOps | partial | unverified | yes |
| [Model Assurance](c7-3.md) | Agentic MLSecOps | not-addressed | unverified | yes |
| [Runtime Assurance](c7-4.md) | Agentic MLSecOps | not-addressed | unverified | yes |
| [First-Party Tool Assurance](c7-5.md) | Agentic MLSecOps | not-addressed | unverified | yes |
| [Third-Party Tool Assurance](c7-6.md) | Agentic MLSecOps | not-addressed | unverified | yes |
| [Data & Feature Stores](c7-8.md) | Agentic MLSecOps | partial | unverified | yes |
| [AI Discovery](c7-9.md) | Agentic MLSecOps | supported | unverified | yes |
| [Automated AI Pen-Testing](c7-10.md) | Agentic MLSecOps | not-addressed | unverified | yes |
| [Asset Registries & Inventory](c6-1.md) | Governance | partial | unverified | yes |
| [Registration & Approval Workflows](c6-2.md) | Governance | not-addressed | unverified | yes |
| [Posture & Reporting](c6-3.md) | Governance | supported | unverified | yes |
| [Policy Management](c6-4.md) | Governance | partial | unverified | yes |
| [AI Lifecycle Management](c6-5.md) | Governance | not-addressed | unverified | yes |
| [Ownership & Accountability](c6-6.md) | Governance | partial | unverified | yes |
| [Risk Assessment & Classification](c6-7.md) | Governance | partial | unverified | yes |
| [Change & Release Governance](c6-8.md) | Governance | not-addressed | unverified | yes |
| [Exceptions & Risk Acceptance](c6-9.md) | Governance | partial | unverified | yes |
| [Data Lifecycle Governance](c6-10.md) | Governance | supported | unverified | yes |
| [Assurance & Compliance Evidence](c6-11.md) | Governance | supported | unverified | yes |
| [Third-Party Governance](c6-12.md) | Governance | partial | unverified | yes |

Sources are in the [source registry](sources.md).
