---
type: "Platform profile"
title: "Zscaler AI Security (with SPLX) profile"
description: "Column profile for Zscaler AI Security (with SPLX) in the AI usage control (SASE, browser, DLP) group."
classification: "C1"
owner: "agent:curator"
status: "draft"
review: "pending"
verification: "not applicable"
tags:
  - "ai-usage-control"
  - "profile"
sources:
  - id: "atlas-catalogue"
    resource: "data/catalog.json"
    locator: "platforms, id zscaler-ai-security"
generated:
  by: "process:offerings-atlas-ingest"
  at: "2026-10-14T18:00:00+10:00"
---

Zscaler AI security portfolio on the Zero Trust Exchange. This research covers AI Guard (users and apps), AI Asset Management, AI Red Teaming from the SPLX acquisition, AI Protect additions, and the AI Broker for Agents, Endpoint AI Security and AI Access Graph announced in June 2026.

Column group: AI usage control (SASE, browser, DLP). Facts are agent-run under atlas decision 0005. Cells listed as eligible are the only ones agents may retrieve.

## Verdicts and states

| Verdict | Cells |
| --- | --- |
| not-addressed | 16 |
| partial | 22 |
| supported | 4 |
| unresolved | 2 |

| Verification state | Cells |
| --- | --- |
| unverified | 44 |

## Products

| Product | Party | Description |
| --- | --- | --- |
| Zscaler AI Broker for Agents | 3p | Announced June 2026: MCP and A2A brokers with an integrated Agent Registry. |
| Zscaler AI Guard | 3p | Inline proxy and detection API that inspects prompts and responses with more than 18 detectors and applies user or group policies. |
| Zscaler AI Asset Management | 3p | Discovery and risk analysis of shadow AI, models, AI workflows, MCP servers and cloud agents. |
| Zscaler Endpoint AI Security | 3p | Announced June 2026: policy for AI in browsers, extensions, plugins and local AI tools. |
| Zscaler AI Red Teaming (SPLX) | 3p | Automated adversarial testing of AI applications, agents and MCP servers with remediation and compliance mapping. |

## Cells

| Control | Category | Verdict | State | Agent-eligible |
| --- | --- | --- | --- | --- |
| [Agent ID](c4-1.md) | Identity | unresolved | unverified | yes |
| [Credential Brokerage](c4-2.md) | Identity | not-addressed | unverified | yes |
| [Delegation (OBO)](c4-3.md) | Identity | not-addressed | unverified | yes |
| [A2A](c4-4.md) | Identity | unresolved | unverified | yes |
| [Agent Local Scopes](c1-1.md) | Authorisation | partial | unverified | yes |
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
| [Data Gateway](c3-3.md) | Mediation / Policy Enforcement | partial | unverified | yes |
| [A2A Gateway](c3-4.md) | Mediation / Policy Enforcement | partial | unverified | yes |
| [HITL](c5-1.md) | Observability & Explainability | not-addressed | unverified | yes |
| [Behavioural](c5-2.md) | Observability & Explainability | partial | unverified | yes |
| [Cost & Yield](c5-3.md) | Observability & Explainability | not-addressed | unverified | yes |
| [Infrastructure](c5-4.md) | Observability & Explainability | not-addressed | unverified | yes |
| [Connectivity](c5-5.md) | Observability & Explainability | partial | unverified | yes |
| [Administrative Audit](c7-1.md) | Agentic MLSecOps | partial | unverified | yes |
| [SOC Telemetry](c7-2.md) | Agentic MLSecOps | partial | unverified | yes |
| [Model Assurance](c7-3.md) | Agentic MLSecOps | partial | unverified | yes |
| [Runtime Assurance](c7-4.md) | Agentic MLSecOps | partial | unverified | yes |
| [First-Party Tool Assurance](c7-5.md) | Agentic MLSecOps | partial | unverified | yes |
| [Third-Party Tool Assurance](c7-6.md) | Agentic MLSecOps | partial | unverified | yes |
| [Data & Feature Stores](c7-8.md) | Agentic MLSecOps | partial | unverified | yes |
| [AI Discovery](c7-9.md) | Agentic MLSecOps | supported | unverified | yes |
| [Automated AI Pen-Testing](c7-10.md) | Agentic MLSecOps | supported | unverified | yes |
| [Asset Registries & Inventory](c6-1.md) | Governance | partial | unverified | yes |
| [Registration & Approval Workflows](c6-2.md) | Governance | partial | unverified | yes |
| [Posture & Reporting](c6-3.md) | Governance | supported | unverified | yes |
| [Policy Management](c6-4.md) | Governance | partial | unverified | yes |
| [AI Lifecycle Management](c6-5.md) | Governance | partial | unverified | yes |
| [Ownership & Accountability](c6-6.md) | Governance | not-addressed | unverified | yes |
| [Risk Assessment & Classification](c6-7.md) | Governance | partial | unverified | yes |
| [Change & Release Governance](c6-8.md) | Governance | not-addressed | unverified | yes |
| [Exceptions & Risk Acceptance](c6-9.md) | Governance | not-addressed | unverified | yes |
| [Data Lifecycle Governance](c6-10.md) | Governance | partial | unverified | yes |
| [Assurance & Compliance Evidence](c6-11.md) | Governance | supported | unverified | yes |
| [Third-Party Governance](c6-12.md) | Governance | partial | unverified | yes |

Sources are in the [source registry](sources.md).
