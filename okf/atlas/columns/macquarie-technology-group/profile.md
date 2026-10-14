---
type: "Platform profile"
title: "Macquarie Technology Group (Macquarie Government and Cloud Services) profile"
description: "Column profile for Macquarie Technology Group (Macquarie Government and Cloud Services) in the Australian sovereign hosting group."
classification: "C1"
owner: "agent:curator"
status: "draft"
review: "pending"
verification: "not applicable"
tags:
  - "sovereign-hosting"
  - "profile"
sources:
  - id: "atlas-catalogue"
    resource: "data/catalog.json"
    locator: "platforms, id macquarie-technology-group"
generated:
  by: "process:offerings-atlas-ingest"
  at: "2026-10-14T18:00:00+10:00"
---

Australian data centre, secure cloud and cyber provider (ASX: MAQ). This research covers Launch AI, the Macquarie Cloud Services sovereign model-as-a-service platform on Red Hat OpenShift, the Macquarie Government secure cloud (VMware-based PROTECTED Cloud), the Macquarie Government Azure practice with Azure Local for private model hosting (launched July 2026), and the managed SOC. IRAP: Macquarie Government states its services are IRAP assessed against PROTECTED controls and that the PROTECTED Cloud platform was assessed by an IRAP assessor for data up to PROTECTED, with the report available on request. No assessor, date or service list is published, and no page places Launch AI or Azure Local in that scope. Hosting Certification Framework: Macquarie states it is the only provider DTA Certified Strategic for both its data centres and cloud, and lists itself as a Federal Government Certified Strategic Hosting Provider. No certificate, date or facility list is published on the pages read.

Column group: Australian sovereign hosting. Facts are agent-run under atlas decision 0005. Cells listed as eligible are the only ones agents may retrieve.

## Verdicts and states

| Verdict | Cells |
| --- | --- |
| not-addressed | 35 |
| partial | 9 |

| Verification state | Cells |
| --- | --- |
| unverified | 44 |

## Products

| Product | Party | Description |
| --- | --- | --- |
| Macquarie Government Azure practice (including Azure Local) | 3p | Co-managed Azure, Sentinel, XDR, Azure Local and Fabric services for agencies, with Azure Local positioned for private language model hosting. |
| Macquarie Data Centres | 3p | Sovereign colocation in Sydney and Canberra, including IC3 Super West built for AI and cloud workloads. |
| Launch AI | 3p | Sovereign model-as-a-service platform from Macquarie Cloud Services on Red Hat OpenShift, in shared and dedicated tiers with capacity pricing. |
| Macquarie Government SOCaaS and Macquarie Cloud Services Managed SOC | 3p | 24/7 onshore SOC and SIEM-as-a-Service with cleared staff. |
| Macquarie Government Secure Cloud (PROTECTED Cloud) | 3p | VMware-based government cloud in Canberra and Sydney, stated as IRAP assessed for data up to PROTECTED. |

## Cells

| Control | Category | Verdict | State | Agent-eligible |
| --- | --- | --- | --- | --- |
| [Agent ID](c4-1.md) | Identity | not-addressed | unverified | yes |
| [Credential Brokerage](c4-2.md) | Identity | not-addressed | unverified | yes |
| [Delegation (OBO)](c4-3.md) | Identity | not-addressed | unverified | yes |
| [A2A](c4-4.md) | Identity | not-addressed | unverified | yes |
| [Agent Local Scopes](c1-1.md) | Authorisation | not-addressed | unverified | yes |
| [Agent Remote Scopes](c1-2.md) | Authorisation | not-addressed | unverified | yes |
| [Human Approval](c1-3.md) | Authorisation | not-addressed | unverified | yes |
| [Agent Provisioning](c1-4.md) | Authorisation | not-addressed | unverified | yes |
| [Agent Orchestration](c2-1.md) | Runtime | not-addressed | unverified | yes |
| [Inference](c2-2.md) | Runtime | partial | unverified | yes |
| [Execution Environment](c2-3.md) | Runtime | partial | unverified | yes |
| [Agent In-Session Memory](c2-4.md) | Runtime | not-addressed | unverified | yes |
| [Harness](c2-5.md) | Runtime | not-addressed | unverified | yes |
| [Agent Persistent Memory](c2-6.md) | Runtime | not-addressed | unverified | yes |
| [Model Gateway](c3-1.md) | Mediation / Policy Enforcement | partial | unverified | yes |
| [Tool Gateway](c3-2.md) | Mediation / Policy Enforcement | not-addressed | unverified | yes |
| [Data Gateway](c3-3.md) | Mediation / Policy Enforcement | not-addressed | unverified | yes |
| [A2A Gateway](c3-4.md) | Mediation / Policy Enforcement | not-addressed | unverified | yes |
| [HITL](c5-1.md) | Observability & Explainability | not-addressed | unverified | yes |
| [Behavioural](c5-2.md) | Observability & Explainability | not-addressed | unverified | yes |
| [Cost & Yield](c5-3.md) | Observability & Explainability | not-addressed | unverified | yes |
| [Infrastructure](c5-4.md) | Observability & Explainability | partial | unverified | yes |
| [Connectivity](c5-5.md) | Observability & Explainability | not-addressed | unverified | yes |
| [Administrative Audit](c7-1.md) | Agentic MLSecOps | not-addressed | unverified | yes |
| [SOC Telemetry](c7-2.md) | Agentic MLSecOps | partial | unverified | yes |
| [Model Assurance](c7-3.md) | Agentic MLSecOps | not-addressed | unverified | yes |
| [Runtime Assurance](c7-4.md) | Agentic MLSecOps | partial | unverified | yes |
| [First-Party Tool Assurance](c7-5.md) | Agentic MLSecOps | not-addressed | unverified | yes |
| [Third-Party Tool Assurance](c7-6.md) | Agentic MLSecOps | not-addressed | unverified | yes |
| [Data & Feature Stores](c7-8.md) | Agentic MLSecOps | partial | unverified | yes |
| [AI Discovery](c7-9.md) | Agentic MLSecOps | not-addressed | unverified | yes |
| [Automated AI Pen-Testing](c7-10.md) | Agentic MLSecOps | not-addressed | unverified | yes |
| [Asset Registries & Inventory](c6-1.md) | Governance | not-addressed | unverified | yes |
| [Registration & Approval Workflows](c6-2.md) | Governance | not-addressed | unverified | yes |
| [Posture & Reporting](c6-3.md) | Governance | not-addressed | unverified | yes |
| [Policy Management](c6-4.md) | Governance | not-addressed | unverified | yes |
| [AI Lifecycle Management](c6-5.md) | Governance | not-addressed | unverified | yes |
| [Ownership & Accountability](c6-6.md) | Governance | not-addressed | unverified | yes |
| [Risk Assessment & Classification](c6-7.md) | Governance | not-addressed | unverified | no |
| [Change & Release Governance](c6-8.md) | Governance | not-addressed | unverified | yes |
| [Exceptions & Risk Acceptance](c6-9.md) | Governance | not-addressed | unverified | yes |
| [Data Lifecycle Governance](c6-10.md) | Governance | partial | unverified | yes |
| [Assurance & Compliance Evidence](c6-11.md) | Governance | partial | unverified | yes |
| [Third-Party Governance](c6-12.md) | Governance | not-addressed | unverified | yes |

Sources are in the [source registry](sources.md).
