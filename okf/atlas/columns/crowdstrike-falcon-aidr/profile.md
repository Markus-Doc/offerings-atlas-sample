---
type: "Platform profile"
title: "CrowdStrike Falcon (AIDR, Next-Gen SIEM, Identity) profile"
description: "Column profile for CrowdStrike Falcon (AIDR, Next-Gen SIEM, Identity) in the Security operations (SIEM, XDR) group."
classification: "C1"
owner: "agent:curator"
status: "draft"
review: "pending"
verification: "not applicable"
tags:
  - "secops"
  - "profile"
sources:
  - id: "atlas-catalogue"
    resource: "data/catalog.json"
    locator: "platforms, id crowdstrike-falcon-aidr"
generated:
  by: "process:offerings-atlas-ingest"
  at: "2026-10-14T18:00:00+10:00"
---

CrowdStrike Falcon AI Detection and Response (Workforce and Agents subscriptions, GA December 2025) with Falcon Next-Gen SIEM, Falcon Next-Gen Identity Security agent identity features and AI Red Team Services. The AIDR docs state end of support on 30 November 2026 with capabilities continuing in Falcon Guardian, announced 1 September 2026, so both names belong to CrowdStrike and Guardian is the successor. Pangea origin not confirmed in pages read.

Column group: Security operations (SIEM, XDR). Facts are agent-run under atlas decision 0005. Cells listed as eligible are the only ones agents may retrieve.

## Verdicts and states

| Verdict | Cells |
| --- | --- |
| not-addressed | 20 |
| partial | 20 |
| supported | 2 |
| unresolved | 2 |

| Verification state | Cells |
| --- | --- |
| unverified | 44 |

## Products

| Product | Party | Description |
| --- | --- | --- |
| Falcon AIDR for Workforce and AIDR for Agents | 3p | Collectors for browsers, endpoints, apps, gateways, MCP, Claude Code, Copilot Studio, AWS and OTel that apply log, redact or block policies. |
| Falcon Guardian | 3p | Successor AIDR offering announced September 2026 with endpoint agent discovery, inventory and runtime enforcement. |
| Falcon Next-Gen Identity Security | 3p | Identity security with the announced Agentic Identity Provider and Continuous Identity for AI Agents. |
| Falcon Next-Gen SIEM | 3p | SIEM that receives AIDR events for search, dashboards and correlation. |
| CrowdStrike AI Red Team Services | 3p | Consulting service for AI application penetration testing and adversary emulation. |

## Cells

| Control | Category | Verdict | State | Agent-eligible |
| --- | --- | --- | --- | --- |
| [Agent ID](c4-1.md) | Identity | partial | unverified | yes |
| [Credential Brokerage](c4-2.md) | Identity | partial | unverified | yes |
| [Delegation (OBO)](c4-3.md) | Identity | unresolved | unverified | yes |
| [A2A](c4-4.md) | Identity | not-addressed | unverified | yes |
| [Agent Local Scopes](c1-1.md) | Authorisation | partial | unverified | yes |
| [Agent Remote Scopes](c1-2.md) | Authorisation | partial | unverified | yes |
| [Human Approval](c1-3.md) | Authorisation | not-addressed | unverified | yes |
| [Agent Provisioning](c1-4.md) | Authorisation | unresolved | unverified | yes |
| [Agent Orchestration](c2-1.md) | Runtime | not-addressed | unverified | yes |
| [Inference](c2-2.md) | Runtime | not-addressed | unverified | yes |
| [Execution Environment](c2-3.md) | Runtime | not-addressed | unverified | yes |
| [Agent In-Session Memory](c2-4.md) | Runtime | not-addressed | unverified | yes |
| [Harness](c2-5.md) | Runtime | not-addressed | unverified | yes |
| [Agent Persistent Memory](c2-6.md) | Runtime | not-addressed | unverified | yes |
| [Model Gateway](c3-1.md) | Mediation / Policy Enforcement | partial | unverified | yes |
| [Tool Gateway](c3-2.md) | Mediation / Policy Enforcement | partial | unverified | yes |
| [Data Gateway](c3-3.md) | Mediation / Policy Enforcement | partial | unverified | yes |
| [A2A Gateway](c3-4.md) | Mediation / Policy Enforcement | not-addressed | unverified | yes |
| [HITL](c5-1.md) | Observability & Explainability | not-addressed | unverified | yes |
| [Behavioural](c5-2.md) | Observability & Explainability | partial | unverified | yes |
| [Cost & Yield](c5-3.md) | Observability & Explainability | partial | unverified | yes |
| [Infrastructure](c5-4.md) | Observability & Explainability | not-addressed | unverified | yes |
| [Connectivity](c5-5.md) | Observability & Explainability | not-addressed | unverified | yes |
| [Administrative Audit](c7-1.md) | Agentic MLSecOps | partial | unverified | yes |
| [SOC Telemetry](c7-2.md) | Agentic MLSecOps | supported | unverified | yes |
| [Model Assurance](c7-3.md) | Agentic MLSecOps | not-addressed | unverified | yes |
| [Runtime Assurance](c7-4.md) | Agentic MLSecOps | partial | unverified | yes |
| [First-Party Tool Assurance](c7-5.md) | Agentic MLSecOps | partial | unverified | yes |
| [Third-Party Tool Assurance](c7-6.md) | Agentic MLSecOps | partial | unverified | yes |
| [Data & Feature Stores](c7-8.md) | Agentic MLSecOps | not-addressed | unverified | yes |
| [AI Discovery](c7-9.md) | Agentic MLSecOps | supported | unverified | yes |
| [Automated AI Pen-Testing](c7-10.md) | Agentic MLSecOps | partial | unverified | yes |
| [Asset Registries & Inventory](c6-1.md) | Governance | partial | unverified | yes |
| [Registration & Approval Workflows](c6-2.md) | Governance | not-addressed | unverified | yes |
| [Posture & Reporting](c6-3.md) | Governance | partial | unverified | yes |
| [Policy Management](c6-4.md) | Governance | partial | unverified | yes |
| [AI Lifecycle Management](c6-5.md) | Governance | not-addressed | unverified | yes |
| [Ownership & Accountability](c6-6.md) | Governance | partial | unverified | yes |
| [Risk Assessment & Classification](c6-7.md) | Governance | not-addressed | unverified | yes |
| [Change & Release Governance](c6-8.md) | Governance | not-addressed | unverified | yes |
| [Exceptions & Risk Acceptance](c6-9.md) | Governance | not-addressed | unverified | yes |
| [Data Lifecycle Governance](c6-10.md) | Governance | partial | unverified | yes |
| [Assurance & Compliance Evidence](c6-11.md) | Governance | not-addressed | unverified | yes |
| [Third-Party Governance](c6-12.md) | Governance | partial | unverified | yes |

Sources are in the [source registry](sources.md).
