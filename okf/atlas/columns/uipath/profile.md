---
type: "Platform profile"
title: "UiPath Agentic Automation profile"
description: "Column profile for UiPath Agentic Automation in the Workflow automation and RPA group."
classification: "C1"
owner: "agent:curator"
status: "draft"
review: "pending"
verification: "not applicable"
tags:
  - "workflow-automation"
  - "profile"
sources:
  - id: "atlas-catalogue"
    resource: "data/catalog.json"
    locator: "platforms, id uipath"
generated:
  by: "process:offerings-atlas-ingest"
  at: "2026-10-14T18:00:00+10:00"
---

UiPath Automation Cloud agentic platform covering Agents (Agent Builder in Studio Web), Maestro orchestration, AI Trust Layer, Automation Ops governance, Orchestrator, Action Center, Automation Hub and the Delegate desktop agent.

Column group: Workflow automation and RPA. Facts are agent-run under atlas decision 0005. Cells listed as eligible are the only ones agents may retrieve.

## Verdicts and states

| Verdict | Cells |
| --- | --- |
| not-addressed | 5 |
| partial | 34 |
| supported | 5 |

| Verification state | Cells |
| --- | --- |
| unverified | 44 |

## Products

| Product | Party | Description |
| --- | --- | --- |
| Action Center | 3p | Human task and escalation handling for agents and processes. |
| UiPath Agents | 3p | Low-code and coded agents built in Studio Web Agent Builder and run on Serverless robots. |
| AI Trust Layer | 3p | LLM gateway with model governance, guardrails, PII masking, audit log and usage summary. |
| Automation Hub | 3p | Idea submission, assessment and decision pipeline, including an Agentic AI idea flow. |
| Automation Ops | 3p | Governance policies for AI Trust Layer, Studio Web, Studio, Robot and Assistant deployed to tenants, groups and users. |
| UiPath Delegate | 3p | Desktop agent that acts with the user's access on Windows, governed through Automation Ops and the AI Trust Layer. |
| UiPath Maestro | 3p | BPMN and flow orchestration of agents, robots and people with instance management. |
| Orchestrator | 3p | Folders, roles, robot accounts, credential stores, audit, Agent Gateway and MCP servers. |

## Cells

| Control | Category | Verdict | State | Agent-eligible |
| --- | --- | --- | --- | --- |
| [Agent ID](c4-1.md) | Identity | partial | unverified | yes |
| [Credential Brokerage](c4-2.md) | Identity | partial | unverified | yes |
| [Delegation (OBO)](c4-3.md) | Identity | partial | unverified | yes |
| [A2A](c4-4.md) | Identity | partial | unverified | yes |
| [Agent Local Scopes](c1-1.md) | Authorisation | partial | unverified | yes |
| [Agent Remote Scopes](c1-2.md) | Authorisation | supported | unverified | yes |
| [Human Approval](c1-3.md) | Authorisation | partial | unverified | yes |
| [Agent Provisioning](c1-4.md) | Authorisation | partial | unverified | yes |
| [Agent Orchestration](c2-1.md) | Runtime | supported | unverified | yes |
| [Inference](c2-2.md) | Runtime | supported | unverified | yes |
| [Execution Environment](c2-3.md) | Runtime | partial | unverified | yes |
| [Agent In-Session Memory](c2-4.md) | Runtime | partial | unverified | yes |
| [Harness](c2-5.md) | Runtime | supported | unverified | yes |
| [Agent Persistent Memory](c2-6.md) | Runtime | partial | unverified | yes |
| [Model Gateway](c3-1.md) | Mediation / Policy Enforcement | partial | unverified | yes |
| [Tool Gateway](c3-2.md) | Mediation / Policy Enforcement | partial | unverified | yes |
| [Data Gateway](c3-3.md) | Mediation / Policy Enforcement | partial | unverified | yes |
| [A2A Gateway](c3-4.md) | Mediation / Policy Enforcement | partial | unverified | yes |
| [HITL](c5-1.md) | Observability & Explainability | supported | unverified | yes |
| [Behavioural](c5-2.md) | Observability & Explainability | partial | unverified | yes |
| [Cost & Yield](c5-3.md) | Observability & Explainability | partial | unverified | yes |
| [Infrastructure](c5-4.md) | Observability & Explainability | partial | unverified | yes |
| [Connectivity](c5-5.md) | Observability & Explainability | not-addressed | unverified | yes |
| [Administrative Audit](c7-1.md) | Agentic MLSecOps | partial | unverified | yes |
| [SOC Telemetry](c7-2.md) | Agentic MLSecOps | partial | unverified | yes |
| [Model Assurance](c7-3.md) | Agentic MLSecOps | partial | unverified | yes |
| [Runtime Assurance](c7-4.md) | Agentic MLSecOps | partial | unverified | yes |
| [First-Party Tool Assurance](c7-5.md) | Agentic MLSecOps | partial | unverified | yes |
| [Third-Party Tool Assurance](c7-6.md) | Agentic MLSecOps | not-addressed | unverified | yes |
| [Data & Feature Stores](c7-8.md) | Agentic MLSecOps | partial | unverified | yes |
| [AI Discovery](c7-9.md) | Agentic MLSecOps | not-addressed | unverified | yes |
| [Automated AI Pen-Testing](c7-10.md) | Agentic MLSecOps | not-addressed | unverified | yes |
| [Asset Registries & Inventory](c6-1.md) | Governance | partial | unverified | yes |
| [Registration & Approval Workflows](c6-2.md) | Governance | partial | unverified | yes |
| [Posture & Reporting](c6-3.md) | Governance | partial | unverified | yes |
| [Policy Management](c6-4.md) | Governance | partial | unverified | yes |
| [AI Lifecycle Management](c6-5.md) | Governance | partial | unverified | yes |
| [Ownership & Accountability](c6-6.md) | Governance | partial | unverified | yes |
| [Risk Assessment & Classification](c6-7.md) | Governance | partial | unverified | yes |
| [Change & Release Governance](c6-8.md) | Governance | partial | unverified | yes |
| [Exceptions & Risk Acceptance](c6-9.md) | Governance | not-addressed | unverified | yes |
| [Data Lifecycle Governance](c6-10.md) | Governance | partial | unverified | yes |
| [Assurance & Compliance Evidence](c6-11.md) | Governance | partial | unverified | yes |
| [Third-Party Governance](c6-12.md) | Governance | partial | unverified | yes |

Sources are in the [source registry](sources.md).
