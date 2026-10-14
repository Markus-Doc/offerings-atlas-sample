---
type: "Registry"
title: "AWS source registry"
description: "Sources cited by the AWS column, with tiers and check dates."
classification: "C1"
owner: "agent:curator"
status: "draft"
review: "pending"
verification: "not applicable"
tags:
  - "cloud-platforms"
  - "sources"
sources:
  - id: "aws-audit"
    resource: "https://docs.aws.amazon.com/audit-manager/latest/userguide/concepts.html"
    locator: "registry entry"
    tier: 1
  - id: "aws-card"
    resource: "https://docs.aws.amazon.com/sagemaker/latest/dg/model-cards.html"
    locator: "registry entry"
    tier: 1
  - id: "aws-confirm"
    resource: "https://docs.aws.amazon.com/bedrock/latest/userguide/agents-userconfirmation.html"
    locator: "registry entry"
    tier: 1
  - id: "aws-data"
    resource: "https://docs.aws.amazon.com/bedrock-agentcore/latest/devguide/data-protection.html"
    locator: "registry entry"
    tier: 1
  - id: "aws-evals"
    resource: "https://docs.aws.amazon.com/bedrock-agentcore/latest/devguide/evaluations.html"
    locator: "registry entry"
    tier: 1
  - id: "aws-evaluation"
    resource: "https://docs.aws.amazon.com/bedrock/latest/userguide/evaluation.html"
    locator: "registry entry"
    tier: 1
  - id: "aws-gateway"
    resource: "https://docs.aws.amazon.com/bedrock-agentcore/latest/devguide/gateway.html"
    locator: "registry entry"
    tier: 1
  - id: "aws-guardduty"
    resource: "https://docs.aws.amazon.com/guardduty/latest/ug/runtime-monitoring.html"
    locator: "registry entry"
    tier: 1
  - id: "aws-guardrails"
    resource: "https://docs.aws.amazon.com/bedrock/latest/userguide/guardrails-how.html"
    locator: "registry entry"
    tier: 1
  - id: "aws-harness"
    resource: "https://docs.aws.amazon.com/bedrock-agentcore/latest/devguide/harness.html"
    locator: "registry entry"
    tier: 1
  - id: "aws-identity"
    resource: "https://docs.aws.amazon.com/bedrock-agentcore/latest/devguide/identity.html"
    locator: "registry entry"
    tier: 1
  - id: "aws-inspector"
    resource: "https://docs.aws.amazon.com/inspector/latest/user/scanning-ecr.html"
    locator: "registry entry"
    tier: 1
  - id: "aws-kb"
    resource: "https://docs.aws.amazon.com/bedrock/latest/userguide/knowledge-base.html"
    locator: "registry entry"
    tier: 1
  - id: "aws-memory"
    resource: "https://docs.aws.amazon.com/bedrock-agentcore/latest/devguide/memory.html"
    locator: "registry entry"
    tier: 1
  - id: "aws-model-registry"
    resource: "https://docs.aws.amazon.com/sagemaker/latest/dg/model-registry-models.html"
    locator: "registry entry"
    tier: 1
  - id: "aws-models"
    resource: "https://docs.aws.amazon.com/bedrock/latest/userguide/models-supported.html"
    locator: "registry entry"
    tier: 1
  - id: "aws-observe"
    resource: "https://docs.aws.amazon.com/bedrock-agentcore/latest/devguide/observability.html"
    locator: "registry entry"
    tier: 1
  - id: "aws-policy"
    resource: "https://docs.aws.amazon.com/bedrock-agentcore/latest/devguide/policy.html"
    locator: "registry entry"
    tier: 1
  - id: "aws-posture"
    resource: "https://docs.aws.amazon.com/securityhub/latest/userguide/bedrockagentcore-controls.html"
    locator: "registry entry"
    tier: 1
  - id: "aws-registry"
    resource: "https://docs.aws.amazon.com/bedrock-agentcore/latest/devguide/registry.html"
    locator: "registry entry"
    tier: 1
  - id: "aws-resource"
    resource: "https://docs.aws.amazon.com/bedrock-agentcore/latest/devguide/resource-based-policies.html"
    locator: "registry entry"
    tier: 1
  - id: "aws-return"
    resource: "https://docs.aws.amazon.com/bedrock/latest/userguide/agents-returncontrol.html"
    locator: "registry entry"
    tier: 1
  - id: "aws-runtime"
    resource: "https://docs.aws.amazon.com/bedrock-agentcore/latest/devguide/agents-tools-runtime.html"
    locator: "registry entry"
    tier: 1
  - id: "aws-security"
    resource: "https://docs.aws.amazon.com/bedrock-agentcore/latest/devguide/runtime-security-best-practices.html"
    locator: "registry entry"
    tier: 1
generated:
  by: "process:offerings-atlas-ingest"
  at: "2026-10-14T18:00:00+10:00"
---

Every source the AWS cells cite, with its tier from the atlas source register. Tier 1 and 2 sources can verify a claim within their subject. Tier 3 can only hold it as provisional.

### aws-audit

- Title: Audit Manager evidence
- URL: https://docs.aws.amazon.com/audit-manager/latest/userguide/concepts.html
- Tier: 1
- Checked: 2026-10-07
- Cited by: [c6-11](c6-11.md), [c6-9](c6-9.md)

### aws-card

- Title: SageMaker Model Cards
- URL: https://docs.aws.amazon.com/sagemaker/latest/dg/model-cards.html
- Tier: 1
- Checked: 2026-10-07
- Cited by: [c6-11](c6-11.md), [c6-6](c6-6.md), [c6-7](c6-7.md), [c7-3](c7-3.md)

### aws-confirm

- Title: Bedrock user confirmation
- URL: https://docs.aws.amazon.com/bedrock/latest/userguide/agents-userconfirmation.html
- Tier: 1
- Checked: 2026-10-07
- Cited by: [c1-3](c1-3.md)

### aws-data

- Title: AgentCore data protection
- URL: https://docs.aws.amazon.com/bedrock-agentcore/latest/devguide/data-protection.html
- Tier: 1
- Checked: 2026-10-07
- Cited by: [c6-10](c6-10.md), [c7-8](c7-8.md)

### aws-evals

- Title: AgentCore Evaluations
- URL: https://docs.aws.amazon.com/bedrock-agentcore/latest/devguide/evaluations.html
- Tier: 1
- Checked: 2026-10-07
- Cited by: [c5-2](c5-2.md), [c7-10](c7-10.md)

### aws-evaluation

- Title: Bedrock evaluations
- URL: https://docs.aws.amazon.com/bedrock/latest/userguide/evaluation.html
- Tier: 1
- Checked: 2026-10-07
- Cited by: [c5-1](c5-1.md)

### aws-gateway

- Title: AgentCore Gateway
- URL: https://docs.aws.amazon.com/bedrock-agentcore/latest/devguide/gateway.html
- Tier: 1
- Checked: 2026-10-07
- Cited by: [c3-1](c3-1.md), [c3-2](c3-2.md), [c3-4](c3-4.md), [c4-2](c4-2.md), [c5-5](c5-5.md)

### aws-guardduty

- Title: GuardDuty Runtime Monitoring
- URL: https://docs.aws.amazon.com/guardduty/latest/ug/runtime-monitoring.html
- Tier: 1
- Checked: 2026-10-07
- Cited by: [c7-2](c7-2.md), [c7-4](c7-4.md)

### aws-guardrails

- Title: Bedrock Guardrails
- URL: https://docs.aws.amazon.com/bedrock/latest/userguide/guardrails-how.html
- Tier: 1
- Checked: 2026-10-07
- Cited by: [c3-3](c3-3.md), [c7-10](c7-10.md)

### aws-harness

- Title: AgentCore Harness
- URL: https://docs.aws.amazon.com/bedrock-agentcore/latest/devguide/harness.html
- Tier: 1
- Checked: 2026-10-07
- Cited by: [c2-1](c2-1.md), [c2-5](c2-5.md)

### aws-identity

- Title: AgentCore Identity
- URL: https://docs.aws.amazon.com/bedrock-agentcore/latest/devguide/identity.html
- Tier: 1
- Checked: 2026-10-07
- Cited by: [c4-1](c4-1.md), [c4-2](c4-2.md), [c4-3](c4-3.md)

### aws-inspector

- Title: Inspector ECR scanning
- URL: https://docs.aws.amazon.com/inspector/latest/user/scanning-ecr.html
- Tier: 1
- Checked: 2026-10-07
- Cited by: [c6-12](c6-12.md), [c7-5](c7-5.md), [c7-6](c7-6.md)

### aws-kb

- Title: Bedrock Knowledge Bases
- URL: https://docs.aws.amazon.com/bedrock/latest/userguide/knowledge-base.html
- Tier: 1
- Checked: 2026-10-07
- Cited by: [c3-3](c3-3.md), [c7-8](c7-8.md)

### aws-memory

- Title: AgentCore Memory
- URL: https://docs.aws.amazon.com/bedrock-agentcore/latest/devguide/memory.html
- Tier: 1
- Checked: 2026-10-07
- Cited by: [c2-4](c2-4.md), [c2-6](c2-6.md), [c6-10](c6-10.md), [c7-8](c7-8.md)

### aws-model-registry

- Title: SageMaker Model Registry
- URL: https://docs.aws.amazon.com/sagemaker/latest/dg/model-registry-models.html
- Tier: 1
- Checked: 2026-10-07
- Cited by: [c6-1](c6-1.md), [c6-5](c6-5.md), [c6-8](c6-8.md), [c7-3](c7-3.md)

### aws-models

- Title: Bedrock supported models
- URL: https://docs.aws.amazon.com/bedrock/latest/userguide/models-supported.html
- Tier: 1
- Checked: 2026-10-07
- Cited by: [c2-2](c2-2.md)

### aws-observe

- Title: AgentCore Observability
- URL: https://docs.aws.amazon.com/bedrock-agentcore/latest/devguide/observability.html
- Tier: 1
- Checked: 2026-10-07
- Cited by: [c5-3](c5-3.md), [c5-4](c5-4.md), [c5-5](c5-5.md), [c6-3](c6-3.md), [c7-1](c7-1.md), [c7-2](c7-2.md)

### aws-policy

- Title: AgentCore Policy
- URL: https://docs.aws.amazon.com/bedrock-agentcore/latest/devguide/policy.html
- Tier: 1
- Checked: 2026-10-07
- Cited by: [c1-2](c1-2.md), [c3-2](c3-2.md), [c6-4](c6-4.md), [c6-9](c6-9.md)

### aws-posture

- Title: Security Hub AgentCore controls
- URL: https://docs.aws.amazon.com/securityhub/latest/userguide/bedrockagentcore-controls.html
- Tier: 1
- Checked: 2026-10-07
- Cited by: [c6-3](c6-3.md), [c7-9](c7-9.md)

### aws-registry

- Title: AWS Agent Registry
- URL: https://docs.aws.amazon.com/bedrock-agentcore/latest/devguide/registry.html
- Tier: 1
- Checked: 2026-10-07
- Cited by: [c1-4](c1-4.md), [c6-1](c6-1.md), [c6-12](c6-12.md), [c6-2](c6-2.md), [c6-5](c6-5.md), [c6-6](c6-6.md), [c6-8](c6-8.md), [c7-6](c7-6.md), [c7-9](c7-9.md)

### aws-resource

- Title: AgentCore resource policies
- URL: https://docs.aws.amazon.com/bedrock-agentcore/latest/devguide/resource-based-policies.html
- Tier: 1
- Checked: 2026-10-07
- Cited by: [c1-2](c1-2.md), [c2-6](c2-6.md)

### aws-return

- Title: Bedrock return control
- URL: https://docs.aws.amazon.com/bedrock/latest/userguide/agents-returncontrol.html
- Tier: 1
- Checked: 2026-10-07
- Cited by: [c1-3](c1-3.md), [c5-1](c5-1.md)

### aws-runtime

- Title: AgentCore Runtime
- URL: https://docs.aws.amazon.com/bedrock-agentcore/latest/devguide/agents-tools-runtime.html
- Tier: 1
- Checked: 2026-10-07
- Cited by: [c1-1](c1-1.md), [c1-4](c1-4.md), [c2-3](c2-3.md), [c3-4](c3-4.md), [c4-4](c4-4.md), [c7-4](c7-4.md)

### aws-security

- Title: AgentCore Runtime security
- URL: https://docs.aws.amazon.com/bedrock-agentcore/latest/devguide/runtime-security-best-practices.html
- Tier: 1
- Checked: 2026-10-07
- Cited by: [c1-1](c1-1.md), [c7-1](c7-1.md), [c7-4](c7-4.md), [c7-5](c7-5.md)
