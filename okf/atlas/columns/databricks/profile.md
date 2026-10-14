---
type: "Platform profile"
title: "Databricks profile"
description: "Column profile for Databricks in the Data and AI platforms group."
classification: "C1"
owner: "agent:curator"
status: "draft"
review: "pending"
verification: "not applicable"
tags:
  - "data-ai-platforms"
  - "profile"
sources:
  - id: "atlas-catalogue"
    resource: "data/catalog.json"
    locator: "platforms, id databricks"
generated:
  by: "process:offerings-atlas-ingest"
  at: "2026-10-14T18:00:00+10:00"
---

Databricks Data Intelligence Platform AI features, covering Agent Bricks (Agent Bricks CLI, Agent Runtime, DurableAgentServer, managed memory and sessions, Databricks Sandbox), legacy Mosaic AI Agent Framework on Model Serving, Model Serving and Foundation Model APIs, Unity Gateway (formerly AI Gateway) with MCP services, service policies and skills, MLflow tracing and evaluation, AI Search (formerly Vector Search), and the Unity Catalog, identity, network and audit controls that apply to them, as documented for AWS with Azure and GCP differences noted where found.

Column group: Data and AI platforms. Facts are agent-run under atlas decision 0005. Cells listed as eligible are the only ones agents may retrieve.

## Verdicts and states

| Verdict | Cells |
| --- | --- |
| not-addressed | 5 |
| partial | 31 |
| supported | 8 |

| Verification state | Cells |
| --- | --- |
| unverified | 44 |

## Products

| Product | Party | Description |
| --- | --- | --- |
| Agent Bricks | 3p | Code-first agent developer platform with the Agent Bricks CLI, Agent Runtime on Databricks Apps, DurableAgentServer, managed memory and sessions, and Databricks Sandbox. |
| AI Search (formerly Vector Search) | 3p | Vector and hybrid search indexes governed in Unity Catalog. |
| Managed MLflow on Databricks | 3p | MLflow tracing, evaluation, production monitoring, human feedback, prompt registry, model registry in Unity Catalog and deployment jobs. |
| Mosaic AI Model Serving and Foundation Model APIs | 3p | Serverless serving of custom models, legacy agents, Databricks-hosted foundation models and governed external models. |
| Databricks platform security controls | 3p | Serverless egress control, audit and network system tables, compliance security profile, enhanced security monitoring, service principals and OAuth. |
| Unity Catalog | 3p | Governance layer for data and AI securables with grants, ABAC policies, governed tags, lineage, data classification and HTTP connections. |
| Unity Gateway (AI Gateway) | 3p | Gateway for model services, model provider services, MCP services and skills with rate limits, budgets, service policies, usage tables and inference tables. |

## Cells

| Control | Category | Verdict | State | Agent-eligible |
| --- | --- | --- | --- | --- |
| [Agent ID](c4-1.md) | Identity | partial | unverified | yes |
| [Credential Brokerage](c4-2.md) | Identity | partial | unverified | yes |
| [Delegation (OBO)](c4-3.md) | Identity | supported | unverified | yes |
| [A2A](c4-4.md) | Identity | partial | unverified | yes |
| [Agent Local Scopes](c1-1.md) | Authorisation | partial | unverified | yes |
| [Agent Remote Scopes](c1-2.md) | Authorisation | supported | unverified | yes |
| [Human Approval](c1-3.md) | Authorisation | partial | unverified | yes |
| [Agent Provisioning](c1-4.md) | Authorisation | partial | unverified | yes |
| [Agent Orchestration](c2-1.md) | Runtime | partial | unverified | yes |
| [Inference](c2-2.md) | Runtime | supported | unverified | yes |
| [Execution Environment](c2-3.md) | Runtime | partial | unverified | yes |
| [Agent In-Session Memory](c2-4.md) | Runtime | partial | unverified | yes |
| [Harness](c2-5.md) | Runtime | supported | unverified | yes |
| [Agent Persistent Memory](c2-6.md) | Runtime | partial | unverified | yes |
| [Model Gateway](c3-1.md) | Mediation / Policy Enforcement | supported | unverified | yes |
| [Tool Gateway](c3-2.md) | Mediation / Policy Enforcement | supported | unverified | yes |
| [Data Gateway](c3-3.md) | Mediation / Policy Enforcement | partial | unverified | yes |
| [A2A Gateway](c3-4.md) | Mediation / Policy Enforcement | partial | unverified | yes |
| [HITL](c5-1.md) | Observability & Explainability | supported | unverified | yes |
| [Behavioural](c5-2.md) | Observability & Explainability | partial | unverified | yes |
| [Cost & Yield](c5-3.md) | Observability & Explainability | partial | unverified | yes |
| [Infrastructure](c5-4.md) | Observability & Explainability | partial | unverified | yes |
| [Connectivity](c5-5.md) | Observability & Explainability | partial | unverified | yes |
| [Administrative Audit](c7-1.md) | Agentic MLSecOps | partial | unverified | yes |
| [SOC Telemetry](c7-2.md) | Agentic MLSecOps | partial | unverified | yes |
| [Model Assurance](c7-3.md) | Agentic MLSecOps | partial | unverified | yes |
| [Runtime Assurance](c7-4.md) | Agentic MLSecOps | partial | unverified | yes |
| [First-Party Tool Assurance](c7-5.md) | Agentic MLSecOps | partial | unverified | yes |
| [Third-Party Tool Assurance](c7-6.md) | Agentic MLSecOps | not-addressed | unverified | yes |
| [Data & Feature Stores](c7-8.md) | Agentic MLSecOps | supported | unverified | yes |
| [AI Discovery](c7-9.md) | Agentic MLSecOps | not-addressed | unverified | yes |
| [Automated AI Pen-Testing](c7-10.md) | Agentic MLSecOps | not-addressed | unverified | yes |
| [Asset Registries & Inventory](c6-1.md) | Governance | partial | unverified | yes |
| [Registration & Approval Workflows](c6-2.md) | Governance | partial | unverified | yes |
| [Posture & Reporting](c6-3.md) | Governance | partial | unverified | yes |
| [Policy Management](c6-4.md) | Governance | partial | unverified | yes |
| [AI Lifecycle Management](c6-5.md) | Governance | partial | unverified | yes |
| [Ownership & Accountability](c6-6.md) | Governance | partial | unverified | yes |
| [Risk Assessment & Classification](c6-7.md) | Governance | not-addressed | unverified | yes |
| [Change & Release Governance](c6-8.md) | Governance | partial | unverified | yes |
| [Exceptions & Risk Acceptance](c6-9.md) | Governance | not-addressed | unverified | yes |
| [Data Lifecycle Governance](c6-10.md) | Governance | partial | unverified | yes |
| [Assurance & Compliance Evidence](c6-11.md) | Governance | partial | unverified | yes |
| [Third-Party Governance](c6-12.md) | Governance | partial | unverified | yes |

Sources are in the [source registry](sources.md).
