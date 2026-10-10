---
type: "Platform profile"
title: "Wiz profile"
description: "Column profile for Wiz in the AI security group."
classification: "C1"
owner: "agent:curator"
status: "draft"
review: "pending"
verification: "not applicable"
tags:
  - "ai-security"
  - "profile"
sources:
  - id: "atlas-catalogue"
    resource: "data/catalog.json"
    locator: "platforms, id wiz"
generated:
  by: "process:offerings-atlas-ingest"
  at: "2026-10-10T18:00:00+10:00"
---

Cloud security platform, a Google company since March 2026, researched for its AI security offerings: AI-SPM and AI inventory, Wiz Defend with the Runtime Sensor on AI workloads, Wiz Code for AI code and coding agents, and the Red Agent, from public wiz.io product pages and blog posts (docs.wiz.io was not reachable for this run).

Column group: AI security. Facts are agent-run under atlas decision 0005. Cells listed as eligible are the only ones agents may retrieve.

## Verdicts and states

| Verdict | Cells |
| --- | --- |
| not-addressed | 25 |
| partial | 12 |
| supported | 6 |
| unresolved | 1 |

| Verification state | Cells |
| --- | --- |
| unverified | 44 |

## Products

| Product | Party | Description |
| --- | --- | --- |
| Wiz AI Security (AI-SPM) | 3p | Agentless AI discovery, AI inventory and AI-BOM, agent and MCP mapping, AI misconfiguration rules, AI attack paths and DSPM for AI. |
| Wiz Code | 3p | Code security with SAST, AI code scans, IDE plugins, skills and git-boundary hooks for coding agents, and code-to-cloud mapping. |
| Wiz Defend | 3p | Cloud detection and response that ingests cloud, SaaS and AI invocation logs and sensor events, with Blue Agent investigation and Wiz Workflows response. |
| Wiz Red Agent | 3p | AI-driven continuous external penetration testing of exposed applications and APIs, linked to Wiz ASM and the Security Graph. |
| Wiz Runtime Sensor | 3p | eBPF workload sensor that detects and blocks runtime threats and attributes activity on AI workloads to agents, MCPs and models. |

## Cells

| Control | Category | Verdict | State | Agent-eligible |
| --- | --- | --- | --- | --- |
| [Agent ID](c4-1.md) | Identity | partial | unverified | yes |
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
| [HITL](c5-1.md) | Observability & Explainability | not-addressed | unverified | yes |
| [Behavioural](c5-2.md) | Observability & Explainability | partial | unverified | yes |
| [Cost & Yield](c5-3.md) | Observability & Explainability | not-addressed | unverified | yes |
| [Infrastructure](c5-4.md) | Observability & Explainability | not-addressed | unverified | yes |
| [Connectivity](c5-5.md) | Observability & Explainability | supported | unverified | yes |
| [Administrative Audit](c7-1.md) | Agentic MLSecOps | partial | unverified | yes |
| [SOC Telemetry](c7-2.md) | Agentic MLSecOps | supported | unverified | yes |
| [Model Assurance](c7-3.md) | Agentic MLSecOps | partial | unverified | yes |
| [Runtime Assurance](c7-4.md) | Agentic MLSecOps | supported | unverified | yes |
| [First-Party Tool Assurance](c7-5.md) | Agentic MLSecOps | partial | unverified | yes |
| [Third-Party Tool Assurance](c7-6.md) | Agentic MLSecOps | partial | unverified | yes |
| [Data & Feature Stores](c7-8.md) | Agentic MLSecOps | partial | unverified | yes |
| [AI Discovery](c7-9.md) | Agentic MLSecOps | supported | unverified | yes |
| [Automated AI Pen-Testing](c7-10.md) | Agentic MLSecOps | partial | unverified | yes |
| [Asset Registries & Inventory](c6-1.md) | Governance | supported | unverified | yes |
| [Registration & Approval Workflows](c6-2.md) | Governance | not-addressed | unverified | yes |
| [Posture & Reporting](c6-3.md) | Governance | supported | unverified | yes |
| [Policy Management](c6-4.md) | Governance | partial | unverified | yes |
| [AI Lifecycle Management](c6-5.md) | Governance | not-addressed | unverified | yes |
| [Ownership & Accountability](c6-6.md) | Governance | partial | unverified | yes |
| [Risk Assessment & Classification](c6-7.md) | Governance | partial | unverified | yes |
| [Change & Release Governance](c6-8.md) | Governance | not-addressed | unverified | yes |
| [Exceptions & Risk Acceptance](c6-9.md) | Governance | unresolved | unverified | yes |
| [Data Lifecycle Governance](c6-10.md) | Governance | not-addressed | unverified | yes |
| [Assurance & Compliance Evidence](c6-11.md) | Governance | partial | unverified | yes |
| [Third-Party Governance](c6-12.md) | Governance | not-addressed | unverified | yes |

Sources are in the [source registry](sources.md).
