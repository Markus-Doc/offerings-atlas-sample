---
type: "Platform profile"
title: "ServiceNow profile"
description: "Column profile for ServiceNow in the Enterprise and workplace agents group."
classification: "C1"
owner: "agent:curator"
status: "draft"
review: "pending"
verification: "not applicable"
tags:
  - "enterprise-agents"
  - "profile"
sources:
  - id: "atlas-catalogue"
    resource: "data/catalog.json"
    locator: "platforms, id servicenow"
generated:
  by: "process:offerings-atlas-ingest"
  at: "2026-10-14T18:00:00+10:00"
---

ServiceNow AI Platform agent and governance features, covering AI Agent Studio, AI Control Tower, AI Gateway, AI Guardian, MCP and A2A support and ServiceNow Cowork, mainly as documented for the Brazil release with some Zurich pages.

Column group: Enterprise and workplace agents. Facts are agent-run under atlas decision 0005. Cells listed as eligible are the only ones agents may retrieve.

## Verdicts and states

| Verdict | Cells |
| --- | --- |
| not-addressed | 2 |
| partial | 28 |
| supported | 13 |
| unresolved | 1 |

| Verification state | Cells |
| --- | --- |
| unverified | 44 |

## Products

| Product | Party | Description |
| --- | --- | --- |
| AI Agent Studio and AI Agents | 1p | Builds and runs AI agents and agentic workflows on the instance, with Now LLM Service or third-party models. |
| AI Control Tower | 3p | AI asset inventory, lifecycle, approvals, risk, security posture, monitoring and value measurement. |
| AI Gateway and MCP Server Console | 3p | Mediates and scans MCP server traffic and exposes instance tools as MCP servers. |
| AI Guardian (Now Assist Guardian) | 3p | Offensiveness, prompt injection and sensitive topic guardrails with logs and custom guardians. |
| ServiceNow Cowork | 3p | Desktop agent client with sandbox, central policies and action approvals governed from the instance. |

## Cells

| Control | Category | Verdict | State | Agent-eligible |
| --- | --- | --- | --- | --- |
| [Agent ID](c4-1.md) | Identity | partial | unverified | yes |
| [Credential Brokerage](c4-2.md) | Identity | partial | unverified | yes |
| [Delegation (OBO)](c4-3.md) | Identity | partial | unverified | yes |
| [A2A](c4-4.md) | Identity | partial | unverified | yes |
| [Agent Local Scopes](c1-1.md) | Authorisation | supported | unverified | yes |
| [Agent Remote Scopes](c1-2.md) | Authorisation | partial | unverified | yes |
| [Human Approval](c1-3.md) | Authorisation | partial | unverified | yes |
| [Agent Provisioning](c1-4.md) | Authorisation | supported | unverified | yes |
| [Agent Orchestration](c2-1.md) | Runtime | partial | unverified | yes |
| [Inference](c2-2.md) | Runtime | supported | unverified | yes |
| [Execution Environment](c2-3.md) | Runtime | partial | unverified | yes |
| [Agent In-Session Memory](c2-4.md) | Runtime | unresolved | unverified | yes |
| [Harness](c2-5.md) | Runtime | supported | unverified | yes |
| [Agent Persistent Memory](c2-6.md) | Runtime | supported | unverified | yes |
| [Model Gateway](c3-1.md) | Mediation / Policy Enforcement | partial | unverified | yes |
| [Tool Gateway](c3-2.md) | Mediation / Policy Enforcement | partial | unverified | yes |
| [Data Gateway](c3-3.md) | Mediation / Policy Enforcement | partial | unverified | yes |
| [A2A Gateway](c3-4.md) | Mediation / Policy Enforcement | not-addressed | unverified | yes |
| [HITL](c5-1.md) | Observability & Explainability | partial | unverified | yes |
| [Behavioural](c5-2.md) | Observability & Explainability | partial | unverified | yes |
| [Cost & Yield](c5-3.md) | Observability & Explainability | supported | unverified | yes |
| [Infrastructure](c5-4.md) | Observability & Explainability | supported | unverified | yes |
| [Connectivity](c5-5.md) | Observability & Explainability | partial | unverified | yes |
| [Administrative Audit](c7-1.md) | Agentic MLSecOps | partial | unverified | yes |
| [SOC Telemetry](c7-2.md) | Agentic MLSecOps | partial | unverified | yes |
| [Model Assurance](c7-3.md) | Agentic MLSecOps | partial | unverified | yes |
| [Runtime Assurance](c7-4.md) | Agentic MLSecOps | partial | unverified | yes |
| [First-Party Tool Assurance](c7-5.md) | Agentic MLSecOps | partial | unverified | yes |
| [Third-Party Tool Assurance](c7-6.md) | Agentic MLSecOps | partial | unverified | yes |
| [Data & Feature Stores](c7-8.md) | Agentic MLSecOps | partial | unverified | yes |
| [AI Discovery](c7-9.md) | Agentic MLSecOps | partial | unverified | yes |
| [Automated AI Pen-Testing](c7-10.md) | Agentic MLSecOps | not-addressed | unverified | yes |
| [Asset Registries & Inventory](c6-1.md) | Governance | supported | unverified | yes |
| [Registration & Approval Workflows](c6-2.md) | Governance | supported | unverified | yes |
| [Posture & Reporting](c6-3.md) | Governance | supported | unverified | yes |
| [Policy Management](c6-4.md) | Governance | partial | unverified | yes |
| [AI Lifecycle Management](c6-5.md) | Governance | supported | unverified | yes |
| [Ownership & Accountability](c6-6.md) | Governance | supported | unverified | yes |
| [Risk Assessment & Classification](c6-7.md) | Governance | supported | unverified | yes |
| [Change & Release Governance](c6-8.md) | Governance | partial | unverified | yes |
| [Exceptions & Risk Acceptance](c6-9.md) | Governance | partial | unverified | yes |
| [Data Lifecycle Governance](c6-10.md) | Governance | partial | unverified | yes |
| [Assurance & Compliance Evidence](c6-11.md) | Governance | partial | unverified | yes |
| [Third-Party Governance](c6-12.md) | Governance | partial | unverified | yes |

Sources are in the [source registry](sources.md).
