---
type: "Registry"
title: "GitHub Copilot source registry"
description: "Sources cited by the GitHub Copilot column, with tiers and check dates."
classification: "C1"
owner: "agent:curator"
status: "draft"
review: "pending"
verification: "not applicable"
tags:
  - "coding-agents"
  - "sources"
sources:
  - id: "gh-audit"
    resource: "https://docs.github.com/en/copilot/reference/enterprise-administrators/agentic-audit-log-events"
    locator: "registry entry"
    tier: 1
  - id: "gh-billing"
    resource: "https://docs.github.com/en/billing/concepts/product-billing/github-copilot-billing"
    locator: "registry entry"
    tier: 1
  - id: "gh-budgets"
    resource: "https://docs.github.com/en/copilot/concepts/billing-and-usage/organizations-and-enterprises/budgets"
    locator: "registry entry"
    tier: 1
  - id: "gh-cloud"
    resource: "https://docs.github.com/en/copilot/concepts/copilot-surfaces/copilot-on-github"
    locator: "registry entry"
    tier: 1
  - id: "gh-custom"
    resource: "https://docs.github.com/en/copilot/reference/custom-agents-configuration"
    locator: "registry entry"
    tier: 1
  - id: "gh-deploy-policy"
    resource: "https://docs.github.com/en/copilot/how-tos/administer-copilot/manage-for-enterprise/use-managed-settings/deploy-managed-settings"
    locator: "registry entry"
    tier: 1
  - id: "gh-firewall"
    resource: "https://docs.github.com/en/copilot/how-tos/copilot-on-github/customize-copilot/customize-the-firewall"
    locator: "registry entry"
    tier: 1
  - id: "gh-guardrails"
    resource: "https://docs.github.com/en/copilot/tutorials/cloud-agent/build-guardrails"
    locator: "registry entry"
    tier: 1
  - id: "gh-hooks"
    resource: "https://docs.github.com/en/copilot/reference/hooks-reference"
    locator: "registry entry"
    tier: 1
  - id: "gh-management"
    resource: "https://docs.github.com/en/copilot/concepts/enterprise/agent-management"
    locator: "registry entry"
    tier: 1
  - id: "gh-mcp"
    resource: "https://docs.github.com/en/copilot/concepts/agents/cloud-agent/mcp-and-cloud-agent"
    locator: "registry entry"
    tier: 1
  - id: "gh-memory"
    resource: "https://docs.github.com/en/copilot/concepts/agents/copilot-memory"
    locator: "registry entry"
    tier: 1
  - id: "gh-models"
    resource: "https://docs.github.com/en/copilot/reference/ai-models/supported-models"
    locator: "registry entry"
    tier: 1
  - id: "gh-otel"
    resource: "https://docs.github.com/en/copilot/concepts/enterprise/opentelemetry"
    locator: "registry entry"
    tier: 1
  - id: "gh-permissions"
    resource: "https://docs.github.com/en/copilot/how-tos/copilot-cli/use-copilot-cli/allowing-tools"
    locator: "registry entry"
    tier: 1
  - id: "gh-policy"
    resource: "https://docs.github.com/en/copilot/reference/enterprise-administrators/enterprise-managed-settings"
    locator: "registry entry"
    tier: 1
  - id: "gh-sandbox"
    resource: "https://docs.github.com/en/copilot/how-tos/cloud-and-local-sandboxes/configuring-local-sandbox-settings"
    locator: "registry entry"
    tier: 1
  - id: "gh-sdk"
    resource: "https://docs.github.com/en/copilot/how-tos/copilot-sdk"
    locator: "registry entry"
    tier: 1
  - id: "gh-secrets"
    resource: "https://docs.github.com/en/copilot/how-tos/copilot-on-github/customize-copilot/customize-cloud-agent/configure-secrets-and-variables"
    locator: "registry entry"
    tier: 1
  - id: "gh-security"
    resource: "https://docs.github.com/en/copilot/concepts/security-governance-and-network-settings/risks-and-mitigations"
    locator: "registry entry"
    tier: 1
  - id: "gh-sessions"
    resource: "https://docs.github.com/en/copilot/how-tos/copilot-on-github/use-copilot-agents/manage-and-track-agents"
    locator: "registry entry"
    tier: 1
  - id: "owasp"
    resource: "https://genai.owasp.org/llm-top-10/"
    locator: "registry entry"
    tier: 4
  - id: "self-redteam"
    resource: "https://www.promptfoo.dev/docs/red-team/"
    locator: "registry entry"
    tier: 4
generated:
  by: "process:offerings-atlas-ingest"
  at: "2026-10-10T18:00:00+10:00"
---

Every source the GitHub Copilot cells cite, with its tier from the atlas source register. Tier 1 and 2 sources can verify a claim within their subject. Tier 3 can only hold it as provisional.

### gh-audit

- Title: Copilot agent audit events
- URL: https://docs.github.com/en/copilot/reference/enterprise-administrators/agentic-audit-log-events
- Tier: 1
- Checked: 2026-10-07
- Cited by: [c4-1](c4-1.md), [c6-11](c6-11.md), [c6-3](c6-3.md), [c7-1](c7-1.md), [c7-2](c7-2.md)

### gh-billing

- Title: Copilot billing
- URL: https://docs.github.com/en/billing/concepts/product-billing/github-copilot-billing
- Tier: 1
- Checked: 2026-10-07
- Cited by: [c5-3](c5-3.md)

### gh-budgets

- Title: Copilot budgets
- URL: https://docs.github.com/en/copilot/concepts/billing-and-usage/organizations-and-enterprises/budgets
- Tier: 1
- Checked: 2026-10-07
- Cited by: [c5-3](c5-3.md)

### gh-cloud

- Title: Copilot on GitHub.com
- URL: https://docs.github.com/en/copilot/concepts/copilot-surfaces/copilot-on-github
- Tier: 1
- Checked: 2026-10-07
- Cited by: [c2-1](c2-1.md), [c2-4](c2-4.md), [c6-10](c6-10.md)

### gh-custom

- Title: Copilot custom agent configuration
- URL: https://docs.github.com/en/copilot/reference/custom-agents-configuration
- Tier: 1
- Checked: 2026-10-07
- Cited by: [c2-1](c2-1.md), [c2-5](c2-5.md), [c3-2](c3-2.md), [c3-4](c3-4.md), [c4-4](c4-4.md), [c6-1](c6-1.md), [c6-2](c6-2.md), [c6-5](c6-5.md), [c6-8](c6-8.md)

### gh-deploy-policy

- Title: Copilot managed settings deployment
- URL: https://docs.github.com/en/copilot/how-tos/administer-copilot/manage-for-enterprise/use-managed-settings/deploy-managed-settings
- Tier: 1
- Checked: 2026-10-07
- Cited by: [c1-4](c1-4.md), [c6-4](c6-4.md)

### gh-firewall

- Title: Copilot firewall configuration
- URL: https://docs.github.com/en/copilot/how-tos/copilot-on-github/customize-copilot/customize-the-firewall
- Tier: 1
- Checked: 2026-10-07
- Cited by: [c5-5](c5-5.md), [c7-6](c7-6.md)

### gh-guardrails

- Title: Copilot cloud agent guardrails
- URL: https://docs.github.com/en/copilot/tutorials/cloud-agent/build-guardrails
- Tier: 1
- Checked: 2026-10-07
- Cited by: [c2-3](c2-3.md), [c5-4](c5-4.md), [c6-2](c6-2.md), [c6-7](c6-7.md), [c6-8](c6-8.md), [c7-4](c7-4.md)

### gh-hooks

- Title: Copilot hooks
- URL: https://docs.github.com/en/copilot/reference/hooks-reference
- Tier: 1
- Checked: 2026-10-07
- Cited by: [c7-5](c7-5.md)

### gh-management

- Title: Enterprise agent management
- URL: https://docs.github.com/en/copilot/concepts/enterprise/agent-management
- Tier: 1
- Checked: 2026-10-07
- Cited by: [c1-4](c1-4.md), [c6-1](c6-1.md), [c6-12](c6-12.md), [c6-3](c6-3.md), [c6-6](c6-6.md), [c7-1](c7-1.md), [c7-9](c7-9.md)

### gh-mcp

- Title: Copilot cloud agent MCP
- URL: https://docs.github.com/en/copilot/concepts/agents/cloud-agent/mcp-and-cloud-agent
- Tier: 1
- Checked: 2026-10-07
- Cited by: [c1-2](c1-2.md), [c3-2](c3-2.md), [c3-3](c3-3.md), [c4-3](c4-3.md), [c6-12](c6-12.md), [c7-6](c7-6.md)

### gh-memory

- Title: Copilot Memory
- URL: https://docs.github.com/en/copilot/concepts/agents/copilot-memory
- Tier: 1
- Checked: 2026-10-07
- Cited by: [c2-6](c2-6.md), [c3-3](c3-3.md), [c6-10](c6-10.md), [c7-8](c7-8.md)

### gh-models

- Title: Copilot supported models
- URL: https://docs.github.com/en/copilot/reference/ai-models/supported-models
- Tier: 1
- Checked: 2026-10-07
- Cited by: [c2-2](c2-2.md), [c3-1](c3-1.md), [c7-3](c7-3.md)

### gh-otel

- Title: Copilot OpenTelemetry
- URL: https://docs.github.com/en/copilot/concepts/enterprise/opentelemetry
- Tier: 1
- Checked: 2026-10-07
- Cited by: [c5-2](c5-2.md), [c5-4](c5-4.md), [c6-10](c6-10.md), [c7-2](c7-2.md)

### gh-permissions

- Title: Copilot CLI tool permissions
- URL: https://docs.github.com/en/copilot/how-tos/copilot-cli/use-copilot-cli/allowing-tools
- Tier: 1
- Checked: 2026-10-07
- Cited by: [c1-1](c1-1.md), [c1-3](c1-3.md), [c7-5](c7-5.md)

### gh-policy

- Title: Copilot enterprise managed settings
- URL: https://docs.github.com/en/copilot/reference/enterprise-administrators/enterprise-managed-settings
- Tier: 1
- Checked: 2026-10-07
- Cited by: [c1-2](c1-2.md), [c3-1](c3-1.md), [c6-4](c6-4.md), [c6-9](c6-9.md)

### gh-sandbox

- Title: Copilot local sandbox settings
- URL: https://docs.github.com/en/copilot/how-tos/cloud-and-local-sandboxes/configuring-local-sandbox-settings
- Tier: 1
- Checked: 2026-10-07
- Cited by: [c1-1](c1-1.md), [c2-3](c2-3.md), [c4-2](c4-2.md), [c6-9](c6-9.md), [c7-4](c7-4.md)

### gh-sdk

- Title: Copilot SDK
- URL: https://docs.github.com/en/copilot/how-tos/copilot-sdk
- Tier: 1
- Checked: 2026-10-07
- Cited by: [c2-5](c2-5.md), [c3-4](c3-4.md), [c4-4](c4-4.md), [c7-10](c7-10.md)

### gh-secrets

- Title: Copilot cloud agent secrets
- URL: https://docs.github.com/en/copilot/how-tos/copilot-on-github/customize-copilot/customize-cloud-agent/configure-secrets-and-variables
- Tier: 1
- Checked: 2026-10-07
- Cited by: [c4-2](c4-2.md), [c7-8](c7-8.md)

### gh-security

- Title: Copilot cloud agent risks and mitigations
- URL: https://docs.github.com/en/copilot/concepts/security-governance-and-network-settings/risks-and-mitigations
- Tier: 1
- Checked: 2026-10-07
- Cited by: [c1-3](c1-3.md), [c4-1](c4-1.md), [c5-1](c5-1.md), [c6-6](c6-6.md)

### gh-sessions

- Title: Managing Copilot agent sessions
- URL: https://docs.github.com/en/copilot/how-tos/copilot-on-github/use-copilot-agents/manage-and-track-agents
- Tier: 1
- Checked: 2026-10-07
- Cited by: [c2-4](c2-4.md), [c5-1](c5-1.md), [c5-2](c5-2.md), [c6-11](c6-11.md), [c6-5](c6-5.md)

### owasp

- Title: OWASP GenAI risks
- URL: https://genai.owasp.org/llm-top-10/
- Tier: 4
- Checked: 2026-10-07
- Cited by: [c6-7](c6-7.md), [c7-3](c7-3.md)

### self-redteam

- Title: Promptfoo red team guide
- URL: https://www.promptfoo.dev/docs/red-team/
- Tier: 4
- Checked: 2026-10-07
- Cited by: [c7-10](c7-10.md)
