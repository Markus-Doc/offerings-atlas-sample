---
type: "Platform profile"
title: "Snowflake profile"
description: "Column profile for Snowflake in the Data and AI platforms group."
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
    locator: "platforms, id snowflake"
generated:
  by: "process:offerings-atlas-ingest"
  at: "2026-10-14T18:00:00+10:00"
---

Snowflake Cortex AI (Cortex Agents, Cortex Analyst, Cortex Search, AI functions and Snowflake CoWork, formerly Snowflake Intelligence), the Snowflake-managed MCP server, and the Horizon governance, RBAC, network, access history and Trust Center controls that apply to them.

Column group: Data and AI platforms. Facts are agent-run under atlas decision 0005. Cells listed as eligible are the only ones agents may retrieve.

## Verdicts and states

| Verdict | Cells |
| --- | --- |
| not-addressed | 7 |
| partial | 27 |
| supported | 10 |

| Verification state | Cells |
| --- | --- |
| unverified | 44 |

## Products

| Product | Party | Description |
| --- | --- | --- |
| Cortex AI Functions | 3p | SQL functions such as AI_COMPLETE and AI_REDACT that call hosted LLMs, with model RBAC and cross-region inference settings. |
| Cortex Agents | 3p | Managed agent objects that plan, call Cortex Analyst, Cortex Search, custom, MCP, web search and code execution tools, with threads, versioning and monitoring. |
| Cortex Analyst | 3p | Natural language to SQL over semantic views, executed under the caller's role. |
| Cortex Search | 3p | Managed hybrid search service over Snowflake data, run with owner's rights. |
| Snowflake CoWork (formerly Snowflake Intelligence) | 3p | Conversational application over Cortex Agents with curated agent lists, user memory and file upload. |
| Snowflake Horizon governance | 3p | RBAC, sensitive data classification, masking and row access policies, access history and contacts. |
| Snowflake-managed MCP server | 3p | Hosted MCP endpoint exposing agents, search, Analyst, SQL and UDF tools to external MCP clients. |
| Trust Center | 3p | Account security scanner packages, including an AI Security package, with violations, detections and notifications. |

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
| [Agent Provisioning](c1-4.md) | Authorisation | supported | unverified | yes |
| [Agent Orchestration](c2-1.md) | Runtime | partial | unverified | yes |
| [Inference](c2-2.md) | Runtime | supported | unverified | yes |
| [Execution Environment](c2-3.md) | Runtime | supported | unverified | yes |
| [Agent In-Session Memory](c2-4.md) | Runtime | partial | unverified | yes |
| [Harness](c2-5.md) | Runtime | supported | unverified | yes |
| [Agent Persistent Memory](c2-6.md) | Runtime | partial | unverified | yes |
| [Model Gateway](c3-1.md) | Mediation / Policy Enforcement | supported | unverified | yes |
| [Tool Gateway](c3-2.md) | Mediation / Policy Enforcement | partial | unverified | yes |
| [Data Gateway](c3-3.md) | Mediation / Policy Enforcement | supported | unverified | yes |
| [A2A Gateway](c3-4.md) | Mediation / Policy Enforcement | not-addressed | unverified | yes |
| [HITL](c5-1.md) | Observability & Explainability | partial | unverified | yes |
| [Behavioural](c5-2.md) | Observability & Explainability | partial | unverified | yes |
| [Cost & Yield](c5-3.md) | Observability & Explainability | partial | unverified | yes |
| [Infrastructure](c5-4.md) | Observability & Explainability | partial | unverified | yes |
| [Connectivity](c5-5.md) | Observability & Explainability | partial | unverified | yes |
| [Administrative Audit](c7-1.md) | Agentic MLSecOps | partial | unverified | yes |
| [SOC Telemetry](c7-2.md) | Agentic MLSecOps | partial | unverified | yes |
| [Model Assurance](c7-3.md) | Agentic MLSecOps | partial | unverified | yes |
| [Runtime Assurance](c7-4.md) | Agentic MLSecOps | partial | unverified | yes |
| [First-Party Tool Assurance](c7-5.md) | Agentic MLSecOps | not-addressed | unverified | yes |
| [Third-Party Tool Assurance](c7-6.md) | Agentic MLSecOps | not-addressed | unverified | yes |
| [Data & Feature Stores](c7-8.md) | Agentic MLSecOps | supported | unverified | yes |
| [AI Discovery](c7-9.md) | Agentic MLSecOps | partial | unverified | yes |
| [Automated AI Pen-Testing](c7-10.md) | Agentic MLSecOps | not-addressed | unverified | yes |
| [Asset Registries & Inventory](c6-1.md) | Governance | partial | unverified | yes |
| [Registration & Approval Workflows](c6-2.md) | Governance | partial | unverified | yes |
| [Posture & Reporting](c6-3.md) | Governance | supported | unverified | yes |
| [Policy Management](c6-4.md) | Governance | not-addressed | unverified | yes |
| [AI Lifecycle Management](c6-5.md) | Governance | partial | unverified | yes |
| [Ownership & Accountability](c6-6.md) | Governance | partial | unverified | yes |
| [Risk Assessment & Classification](c6-7.md) | Governance | not-addressed | unverified | yes |
| [Change & Release Governance](c6-8.md) | Governance | partial | unverified | yes |
| [Exceptions & Risk Acceptance](c6-9.md) | Governance | not-addressed | unverified | yes |
| [Data Lifecycle Governance](c6-10.md) | Governance | partial | unverified | yes |
| [Assurance & Compliance Evidence](c6-11.md) | Governance | partial | unverified | yes |
| [Third-Party Governance](c6-12.md) | Governance | partial | unverified | yes |

Sources are in the [source registry](sources.md).
