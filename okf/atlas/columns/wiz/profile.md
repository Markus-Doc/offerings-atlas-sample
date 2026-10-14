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
  at: "2026-10-14T18:00:00+10:00"
---

Cloud security platform, a Google company since March 2026, researched for its AI security offerings: AI-SPM and AI inventory, Wiz Defend with the Runtime Sensor on AI workloads, Wiz Code for AI code and coding agents, and the Red Agent, from public wiz.io product pages and blog posts (docs.wiz.io was not reachable for this run).

Column group: AI security. Facts are agent-run under atlas decision 0005. Cells listed as eligible are the only ones agents may retrieve.

## Verdicts and states

| Verdict | Cells |
| --- | --- |
| not-addressed | 21 |
| partial | 12 |
| supported | 6 |
| unresolved | 5 |

| Verification state | Cells |
| --- | --- |
| contested | 1 |
| unverified | 38 |
| verified | 5 |

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
| [Agent ID](c4-1.md) | Identity | partial | unverified | no |
| [Credential Brokerage](c4-2.md) | Identity | not-addressed | unverified | no |
| [Delegation (OBO)](c4-3.md) | Identity | not-addressed | unverified | no |
| [A2A](c4-4.md) | Identity | unresolved | unverified | no |
| [Agent Local Scopes](c1-1.md) | Authorisation | not-addressed | unverified | no |
| [Agent Remote Scopes](c1-2.md) | Authorisation | not-addressed | unverified | no |
| [Human Approval](c1-3.md) | Authorisation | unresolved | unverified | no |
| [Agent Provisioning](c1-4.md) | Authorisation | not-addressed | unverified | no |
| [Agent Orchestration](c2-1.md) | Runtime | not-addressed | unverified | no |
| [Inference](c2-2.md) | Runtime | not-addressed | unverified | no |
| [Execution Environment](c2-3.md) | Runtime | not-addressed | unverified | no |
| [Agent In-Session Memory](c2-4.md) | Runtime | not-addressed | unverified | no |
| [Harness](c2-5.md) | Runtime | not-addressed | unverified | no |
| [Agent Persistent Memory](c2-6.md) | Runtime | not-addressed | unverified | no |
| [Model Gateway](c3-1.md) | Mediation / Policy Enforcement | not-addressed | unverified | no |
| [Tool Gateway](c3-2.md) | Mediation / Policy Enforcement | not-addressed | unverified | no |
| [Data Gateway](c3-3.md) | Mediation / Policy Enforcement | not-addressed | unverified | no |
| [A2A Gateway](c3-4.md) | Mediation / Policy Enforcement | not-addressed | unverified | no |
| [HITL](c5-1.md) | Observability & Explainability | not-addressed | unverified | no |
| [Behavioural](c5-2.md) | Observability & Explainability | partial | unverified | no |
| [Cost & Yield](c5-3.md) | Observability & Explainability | not-addressed | unverified | no |
| [Infrastructure](c5-4.md) | Observability & Explainability | not-addressed | unverified | no |
| [Connectivity](c5-5.md) | Observability & Explainability | supported | unverified | no |
| [Administrative Audit](c7-1.md) | Agentic MLSecOps | partial | unverified | no |
| [SOC Telemetry](c7-2.md) | Agentic MLSecOps | supported | contested | no |
| [Model Assurance](c7-3.md) | Agentic MLSecOps | partial | verified | yes |
| [Runtime Assurance](c7-4.md) | Agentic MLSecOps | supported | unverified | no |
| [First-Party Tool Assurance](c7-5.md) | Agentic MLSecOps | partial | verified | yes |
| [Third-Party Tool Assurance](c7-6.md) | Agentic MLSecOps | partial | unverified | no |
| [Data & Feature Stores](c7-8.md) | Agentic MLSecOps | partial | unverified | no |
| [AI Discovery](c7-9.md) | Agentic MLSecOps | supported | unverified | no |
| [Automated AI Pen-Testing](c7-10.md) | Agentic MLSecOps | partial | verified | yes |
| [Asset Registries & Inventory](c6-1.md) | Governance | supported | verified | yes |
| [Registration & Approval Workflows](c6-2.md) | Governance | unresolved | unverified | no |
| [Posture & Reporting](c6-3.md) | Governance | supported | unverified | no |
| [Policy Management](c6-4.md) | Governance | partial | unverified | no |
| [AI Lifecycle Management](c6-5.md) | Governance | not-addressed | unverified | no |
| [Ownership & Accountability](c6-6.md) | Governance | partial | unverified | no |
| [Risk Assessment & Classification](c6-7.md) | Governance | partial | unverified | no |
| [Change & Release Governance](c6-8.md) | Governance | not-addressed | unverified | no |
| [Exceptions & Risk Acceptance](c6-9.md) | Governance | unresolved | unverified | yes |
| [Data Lifecycle Governance](c6-10.md) | Governance | unresolved | unverified | no |
| [Assurance & Compliance Evidence](c6-11.md) | Governance | partial | verified | yes |
| [Third-Party Governance](c6-12.md) | Governance | not-addressed | unverified | no |

Sources are in the [source registry](sources.md).
