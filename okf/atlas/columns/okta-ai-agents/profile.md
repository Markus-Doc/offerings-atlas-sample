---
type: "Platform profile"
title: "Okta for AI Agents (with Auth0) profile"
description: "Column profile for Okta for AI Agents (with Auth0) in the Identity, access and secrets group."
classification: "C1"
owner: "agent:curator"
status: "draft"
review: "pending"
verification: "not applicable"
tags:
  - "identity"
  - "profile"
sources:
  - id: "atlas-catalogue"
    resource: "data/catalog.json"
    locator: "platforms, id okta-ai-agents"
generated:
  by: "process:offerings-atlas-ingest"
  at: "2026-10-14T18:00:00+10:00"
---

Okta workforce identity features for AI agents (Universal Directory agent registration, Agent SSO with Cross App Access, resource connections, Agent Gateway, ISPM agent discovery, Okta Identity Governance for agents and the kill switch), plus Auth0 for AI Agents and the acquired Permiso Security detection platform.

Column group: Identity, access and secrets. Facts are agent-run under atlas decision 0005. Cells listed as eligible are the only ones agents may retrieve.

## Verdicts and states

| Verdict | Cells |
| --- | --- |
| not-addressed | 20 |
| partial | 15 |
| supported | 9 |

| Verification state | Cells |
| --- | --- |
| unverified | 44 |

## Products

| Product | Party | Description |
| --- | --- | --- |
| Okta Agent Gateway | 3p | Okta-hosted MCP proxy that validates agent tokens, filters tools, injects downstream credentials by token exchange and logs tool calls. |
| Okta Agent SSO and Cross App Access (XAA) | 3p | Included in core Okta SSO plans from August 2026, registers XAA-capable agents and issues short-lived ID-JAG based tokens under admin policy. |
| Auth0 for AI Agents | 3p | Customer identity features for agent builders: user authentication, Token Vault, asynchronous authorization with CIBA and RAR, and Auth0 FGA for RAG. |
| Okta Identity Security Posture Management (ISPM) agent discovery | 3p | Discovery and risk assessment of shadow agents, OAuth grants and MCP servers from browser, endpoint and builder platform sources. |
| Okta Identity Governance for AI agents | 3p | Access requests and access certification campaigns covering agent-linked apps and agent resource connections. |
| Permiso Security (acquired August 2026) | 3p | Identity threat detection platform for human, non-human and agent identities, being integrated into Okta ITDR. |
| Okta for AI Agents | 3p | Separate subscription, GA since May 2026, for registering agents in Universal Directory with owners, resource connections, agent-to-agent connections and governance. |

## Cells

| Control | Category | Verdict | State | Agent-eligible |
| --- | --- | --- | --- | --- |
| [Agent ID](c4-1.md) | Identity | supported | unverified | yes |
| [Credential Brokerage](c4-2.md) | Identity | supported | unverified | yes |
| [Delegation (OBO)](c4-3.md) | Identity | supported | unverified | yes |
| [A2A](c4-4.md) | Identity | supported | unverified | yes |
| [Agent Local Scopes](c1-1.md) | Authorisation | not-addressed | unverified | yes |
| [Agent Remote Scopes](c1-2.md) | Authorisation | supported | unverified | yes |
| [Human Approval](c1-3.md) | Authorisation | partial | unverified | yes |
| [Agent Provisioning](c1-4.md) | Authorisation | supported | unverified | yes |
| [Agent Orchestration](c2-1.md) | Runtime | not-addressed | unverified | yes |
| [Inference](c2-2.md) | Runtime | not-addressed | unverified | yes |
| [Execution Environment](c2-3.md) | Runtime | not-addressed | unverified | yes |
| [Agent In-Session Memory](c2-4.md) | Runtime | not-addressed | unverified | yes |
| [Harness](c2-5.md) | Runtime | not-addressed | unverified | yes |
| [Agent Persistent Memory](c2-6.md) | Runtime | not-addressed | unverified | yes |
| [Model Gateway](c3-1.md) | Mediation / Policy Enforcement | not-addressed | unverified | yes |
| [Tool Gateway](c3-2.md) | Mediation / Policy Enforcement | partial | unverified | yes |
| [Data Gateway](c3-3.md) | Mediation / Policy Enforcement | partial | unverified | yes |
| [A2A Gateway](c3-4.md) | Mediation / Policy Enforcement | partial | unverified | yes |
| [HITL](c5-1.md) | Observability & Explainability | not-addressed | unverified | yes |
| [Behavioural](c5-2.md) | Observability & Explainability | partial | unverified | yes |
| [Cost & Yield](c5-3.md) | Observability & Explainability | not-addressed | unverified | yes |
| [Infrastructure](c5-4.md) | Observability & Explainability | not-addressed | unverified | yes |
| [Connectivity](c5-5.md) | Observability & Explainability | supported | unverified | yes |
| [Administrative Audit](c7-1.md) | Agentic MLSecOps | partial | unverified | yes |
| [SOC Telemetry](c7-2.md) | Agentic MLSecOps | partial | unverified | yes |
| [Model Assurance](c7-3.md) | Agentic MLSecOps | not-addressed | unverified | yes |
| [Runtime Assurance](c7-4.md) | Agentic MLSecOps | not-addressed | unverified | yes |
| [First-Party Tool Assurance](c7-5.md) | Agentic MLSecOps | not-addressed | unverified | yes |
| [Third-Party Tool Assurance](c7-6.md) | Agentic MLSecOps | partial | unverified | yes |
| [Data & Feature Stores](c7-8.md) | Agentic MLSecOps | not-addressed | unverified | yes |
| [AI Discovery](c7-9.md) | Agentic MLSecOps | supported | unverified | yes |
| [Automated AI Pen-Testing](c7-10.md) | Agentic MLSecOps | not-addressed | unverified | yes |
| [Asset Registries & Inventory](c6-1.md) | Governance | partial | unverified | yes |
| [Registration & Approval Workflows](c6-2.md) | Governance | partial | unverified | yes |
| [Posture & Reporting](c6-3.md) | Governance | partial | unverified | yes |
| [Policy Management](c6-4.md) | Governance | not-addressed | unverified | yes |
| [AI Lifecycle Management](c6-5.md) | Governance | partial | unverified | yes |
| [Ownership & Accountability](c6-6.md) | Governance | supported | unverified | yes |
| [Risk Assessment & Classification](c6-7.md) | Governance | partial | unverified | yes |
| [Change & Release Governance](c6-8.md) | Governance | not-addressed | unverified | yes |
| [Exceptions & Risk Acceptance](c6-9.md) | Governance | not-addressed | unverified | yes |
| [Data Lifecycle Governance](c6-10.md) | Governance | not-addressed | unverified | yes |
| [Assurance & Compliance Evidence](c6-11.md) | Governance | partial | unverified | yes |
| [Third-Party Governance](c6-12.md) | Governance | partial | unverified | yes |

Sources are in the [source registry](sources.md).
