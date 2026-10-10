# Questionnaire answers: Client A (synthetic)

Answered 2026-10-10 from the OKF tree okf/atlas. Stack: Claude Code, AWS, Okta for AI Agents (with Auth0), Wiz, Microsoft Purview (DSPM for AI, Compliance Manager). Maturity: m2, measured pilots. 37 of 38 citations passed the knowledge base check, and 0 rest on agent-verified records.

Models: `claude-cli-haiku` routed the concerns, `claude-cli-sonnet` answered them, through the local gateway. 5 calls, 45409 tokens in, 9595 out.

## 1. How does agent-to-agent (A2A) authorisation work, and how do we stop one agent acting with another agent's permissions?

Controls: A2A, Delegation (OBO), A2A Gateway, Agent ID.

Your Okta agent identities from c4-1 are the strongest base, because Okta lets one agent call another under the target's identity with scoped tokens and enforces this at token issuance. Claude Code has no cryptographic agent authentication for agent-to-agent traffic, and Wiz and Purview do not address the channel, so nothing in your stack inspects messages on the wire. To stop one agent borrowing another's permissions, give every agent its own identity, restrict allowed callers per target, and add a gateway if you need message-path enforcement.

| Claim | Record | Basis | Check |
| --- | --- | --- | --- |
| Okta's Connect to another AI agent resource connection lets one agent call another under the target's identity through an authorisation server and audience with allowed scopes. This is the in-stack mechanism that keeps a caller from simply reusing the callee's permissions. [source](https://help.okta.com/oie/en-us/content/topics/ai-agents/ai-agent-connected-resource.htm) | `okta-ai-agents--c4-4` | owner-accepted | pass |
| Okta's agent-to-agent connections define which agents may call which, but enforcement happens at token issuance. There is no inline gateway for A2A traffic and no message schema enforcement described, so support is partial. [source](https://help.okta.com/oie/en-us/content/topics/ai-agents/ai-agent-connected-resource.htm) | `okta-ai-agents--c3-4` | owner-accepted | pass |
| Okta Agent Gateway exchanges the agent token for downstream tokens on behalf of the user, and a linked app restricts an agent to acting for users currently signed in. Downstream apps must implement the ID-JAG grant, and delegation chains beyond one hop are not described. [source](https://developer.okta.com/docs/concepts/agent-gateway) | `okta-ai-agents--c4-3` | owner-accepted | pass |
| Claude Code agent teams pass messages through local mailbox files between sessions of the same user on one machine. There is no cryptographic authentication of agents or trust boundary definition, and the feature is experimental and off by default, so support is partial. [source](https://code.claude.com/docs/en/agent-teams) | `claude-code--c4-4` | owner-accepted | pass |
| Claude Code's RFC 8693 act chain exists only in self-hosted environments, and Anthropic advises treating the session token as weaker than a direct login. Local sessions pass the developer's own credentials rather than a delegated, attenuated token. [source](https://code.claude.com/docs/en/self-hosted-environments-identity) | `claude-code--c4-3` | owner-accepted | pass |
| AWS AgentCore Runtime supports A2A communication, but the assessment notes that discovery and protocol interoperability do not confer authority. Peer endpoints should be pinned and caller identity verified. [source](https://docs.aws.amazon.com/bedrock-agentcore/latest/devguide/agents-tools-runtime.html) | `aws--c4-4` | owner-accepted | pass |
| AWS Gateway documents passthrough targets including A2A, but protocol support alone does not prove pairwise delegation restrictions. Peers need authenticating and unapproved agent pairs denying, and no deployed configuration was tested. [source](https://docs.aws.amazon.com/bedrock-agentcore/latest/devguide/gateway.html) | `aws--c3-4` | owner-accepted | pass |
| Alternative: Kong AI Gateway AI Agent entities enforce which consumers or groups may call each agent and detect A2A JSON-RPC bindings. It has no skill-level ACLs, does not validate payloads beyond envelope detection, and allowed pairs depend on each calling agent having its own consumer identity. [source](https://developer.konghq.com/ai-gateway/entities/ai-agent/) | `kong-ai-gateway--c3-4` (alternative) | owner-accepted | pass |
| Alternative: Microsoft Entra Agent ID uses Conditional Access scoped by agent identity or blueprint to decide which agents get tokens for a callee, and risk policies can block risky agents. Enforcement is at token issuance, not on the message path. [source](https://learn.microsoft.com/en-us/entra/identity/conditional-access/agent-id) | `microsoft-entra-agent-id--c3-4` (alternative) | owner-accepted | pass |
| Alternative: Ping Identity Agent Privilege places remote agents behind an AI gateway with policy on which operations agents can use, and AI Guard inspects agent-to-agent traffic. A broader allowed-pairs matrix is not described. [source](https://docs.pingidentity.com/privilege/agent-privilege/what-is-agent-privilege.md) | `ping-identity-ai--c3-4` (alternative) | owner-accepted | pass |

Next steps:

- Register each agent separately in Okta with its own workload principal and create agent-to-agent connections only for approved caller and callee pairs.
- Test a two-agent chain in Okta and confirm the System Log shows both identities, then test a caller with no connection is refused.
- Test multi-hop delegation explicitly, since Okta does not describe chains beyond one hop.
- Keep Claude Code agent teams disabled in managed settings unless needed, and decide whether cross-boundary agent traffic needs an external A2A gateway.

Not settled by the knowledge base:

- Whether Okta enforces anything on the message path, as only token issuance enforcement is documented.
- Whether Okta supports the A2A protocol itself or cross-organisation trust boundaries, which its records do not describe.
- How your AWS AgentCore deployment is configured, as no tenant or Region was tested.
- Whether Wiz and Purview add anything to A2A authorisation. Their records show no A2A authentication or authorisation, and Purview only audits interactions after the fact.
- Whether the Claude Code agent teams feature is currently enabled in your environment.

## 2. What gateway do we need in front of models and MCP tools?

Controls: Model Gateway, Tool Gateway.

The client's stack already has partial gateway coverage, but no single product covers both models and MCP tools. Claude Code's own gateway and AWS Gateway are the main model and tool candidates, while Okta covers MCP traffic only and Wiz and Purview do not act as gateways. Gaps remain in prompt injection screening, rate limits and schema validation, so the client needs a model gateway with fail-closed settings plus a content-aware tool gateway.

| Claim | Record | Basis | Check |
| --- | --- | --- | --- |
| Claude Code's self-hosted Claude apps gateway signs users in with the corporate IdP, enforces model access per IdP group, routes and fails over between Bedrock, Google Cloud, Foundry and the Anthropic API, and caps spend per user, group or organisation. [source](https://code.claude.com/docs/en/claude-apps-gateway) | `claude-code--c3-1` | owner-accepted | pass |
| The Claude apps gateway has no documented prompt injection screening, spend enforcement fails open by default if Postgres is unavailable, and caps are USD estimates rather than token rate limits. Setting enforcement.fail_closed_on_error is the suggested fix. [source](https://code.claude.com/docs/en/claude-apps-gateway-spend-limits) | `claude-code--c3-1` | owner-accepted | pass |
| AWS Gateway documents model-based routing across providers, but per-model quotas and failover semantics need verification on the selected route, and no deployed configuration was tested. [source](https://docs.aws.amazon.com/bedrock-agentcore/latest/devguide/gateway.html) | `aws--c3-1` | owner-accepted | pass |
| Claude Code enforces tool policy on the client side through permission rules, managed MCP allowlists, PreToolUse hooks and sandbox egress allowlists. This is not a separate gateway and has no tool quotas, rate limits or schema validation policy. [source](https://code.claude.com/docs/en/managed-mcp) | `claude-code--c3-2` | owner-accepted | pass |
| AWS Gateway exposes APIs and MCP tools with authentication, and policy checks tool calls. Unknown tools and alternate egress paths still need denial tests. [source](https://docs.aws.amazon.com/bedrock-agentcore/latest/devguide/policy.html) | `aws--c3-2` | owner-accepted | pass |
| Okta Agent Gateway sits between agents and remote MCP servers, validates tokens, exposes only admin-selected tools and injects downstream credentials. It documents no rate limits, schema validation or injection screening, covers MCP only, and GA was stated for Q3. [source](https://developer.okta.com/docs/concepts/agent-gateway) | `okta-ai-agents--c3-2` | owner-accepted | pass |
| Okta's gateway does not route, quota or screen model calls, so it does not serve as the model gateway. [source]() | `okta-ai-agents--c3-1` | owner-accepted | fail |
| Wiz has no model gateway. It checks that provider guardrails are enabled and flags AI endpoints not protected by Cloudflare, but enforcement at the edge is done by Cloudflare. [source](https://www.wiz.io/blog/wiz-cloudflare-ai-security-integration) | `wiz--c3-1` | owner-accepted | pass |
| Purview offers only partial coverage. It has no model routing, quota or rate limits, and its prompt blocking is in preview. [source](https://learn.microsoft.com/en-us/purview/dlp-microsoft365-copilot-location-learn-about) | `microsoft-purview--c3-1` | owner-accepted | pass |
| Purview covers web search and AI site egress only, with no per-agent tool allow lists, schema checks or rate limits for tools. [source](https://learn.microsoft.com/en-us/purview/dspm-for-ai) | `microsoft-purview--c3-2` | owner-accepted | pass |

Next steps:

- Set enforcement.fail_closed_on_error on the Claude apps gateway and confirm that spend caps return 429 when Postgres is unavailable.
- Route all inference through the configured AWS Gateway endpoint and test failover and per-model quotas.
- Run denial tests against AWS Gateway for unknown tools and alternate egress paths, and allow only reviewed schemas and destinations.
- Choose a content-aware MCP gateway for rate limits, schema validation and injection screening, and confirm Okta Agent Gateway GA status for the tenant.

Not settled by the knowledge base:

- Which model providers and MCP servers the client actually uses, which decides whether the Claude apps gateway or AWS Gateway is the better fit.
- Whether AWS Gateway screens prompts for injection, as the record does not say.
- Whether Okta Agent Gateway is generally available for the client's tenant.
- Whether any alternative content-aware MCP gateway or LLM gateway product is available, as no alternative records were supplied.
- The client's deployed configurations, as none of the records tested a live tenant.

## 3. Can prompts, outputs and agent memory stay in Australia?

Controls: Data Lifecycle Governance, Agent Persistent Memory, Agent In-Session Memory, Inference.

The records do not confirm that prompts, outputs and agent memory can stay in Australia. Claude Code says residency follows the chosen provider or a gateway routing inference through the customer's cloud, and AWS residency needs service-specific validation. Purview does not address residency, and Wiz and Okta do not cover it.

| Claim | Record | Basis | Check |
| --- | --- | --- | --- |
| Claude Code residency follows the chosen provider, or a gateway that routes inference through the customer's cloud. Support is partial and unverified, so the required region has to be selected and confirmed. [source](https://code.claude.com/docs/en/data-usage) | `claude-code--c6-10` | owner-accepted | pass |
| Claude Code auto memory has no documented retention limit, and feedback transcripts are kept for 5 years when users submit them. Both are gaps for a residency position unless disabled in managed settings. [source](https://code.claude.com/docs/en/sessions) | `claude-code--c6-10` | owner-accepted | pass |
| Claude Code auto memory is machine-local plaintext with no documented expiry. It can be disabled with CLAUDE_CODE_DISABLE_AUTO_MEMORY where retention must be controlled. [source](https://code.claude.com/docs/en/memory) | `claude-code--c2-6` | owner-accepted | pass |
| Claude Code local session transcripts sit under the user's home directory and are retained for 30 days by default. Cloud session transcripts are stored by Anthropic, so location of that copy is not settled by these records. [source](https://code.claude.com/docs/en/data-usage) | `claude-code--c2-4` | owner-accepted | pass |
| Claude Code allows restricting API providers with allowedProviders and pinning model IDs on Bedrock, Google Cloud and Foundry. This can be used to keep inference on a chosen cloud, but organisation-level server-side model controls do not reach third-party cloud providers. [source](https://code.claude.com/docs/en/model-config) | `claude-code--c2-2` | owner-accepted | pass |
| For AWS AgentCore memory, retention, downstream deletion and residency need service-specific validation. No Region or deployed configuration was tested, so Australian residency is not confirmed. [source](https://docs.aws.amazon.com/bedrock-agentcore/latest/devguide/data-protection.html) | `aws--c6-10` | owner-accepted | pass |
| AWS Bedrock model, feature and Region availability must be checked for the selected deployment. The exact model identifier and supported Region should be recorded. [source](https://docs.aws.amazon.com/bedrock/latest/userguide/models-supported.html) | `aws--c2-2` | owner-accepted | pass |
| Purview retention policies can retain or delete prompts and responses, but residency is not addressed on the reviewed pages. Deletion can take up to about 16 days. [source](https://learn.microsoft.com/en-us/purview/retention-policies-copilot) | `microsoft-purview--c6-10` | owner-accepted | pass |
| AWS AgentCore Memory persists events across sessions, which is the store where agent memory residency would need to be traced. Namespace access, correction and deletion should be tested. [source](https://docs.aws.amazon.com/bedrock-agentcore/latest/devguide/memory.html) | `aws--c2-6` | owner-accepted | pass |

Next steps:

- Confirm which inference provider and AWS Region Claude Code uses, and restrict it with allowedProviders and pinned model IDs in managed settings.
- Trace each copy of prompts, outputs and memory in AgentCore and verify Region selection and deletion in the Australian Region.
- Disable auto memory, feedback and nonessential traffic in Claude Code managed settings, and set cleanupPeriodDays.
- Ask Microsoft for written confirmation of where Purview-retained AI interaction copies are stored.

Not settled by the knowledge base:

- Whether the client's Claude Code deployment actually routes inference through an Australian Region.
- Whether AgentCore Memory and Bedrock models are available in an Australian Region for the models chosen.
- Where Anthropic stores cloud session transcripts and feedback transcripts geographically.
- Where Purview retained AI interaction copies are stored.
- Whether any of the in-stack controls have been tested, as all records are unverified.

## 4. How do we make a person approve an agent action before it runs, with evidence of who approved it?

Controls: Human Approval, HITL, Administrative Audit, Ownership & Accountability.

Your stack can force a human approval before an agent action, but it only partly proves who approved it. Claude Code and Auth0 CIBA are the strongest routes, and each decision can be logged with a user identity, though neither is documented as tamper-evident. The audit capability you already have (c7-1) is partial, so approval evidence would need to be exported to write-once storage and tested.

| Claim | Record | Basis | Check |
| --- | --- | --- | --- |
| Claude Code in Manual mode shows the exact command or edit and asks before running it. Unmatched commands fail closed to a prompt, and each decision is emitted as a tool_decision event with its source. [source](https://code.claude.com/docs/en/permissions) | `claude-code--c1-3` | owner-accepted | pass |
| Claude Code gaps: Auto mode, the default in recent versions, replaces most human prompts with a classifier, and always-allow grants persist per repository. The approver is the local user with no separate authorisation check, so approval is not tied to a named authorised approver. [source](https://code.claude.com/docs/en/permission-modes) | `claude-code--c1-3` | owner-accepted | pass |
| Auth0 for AI Agents offers CIBA with RAR, so an agent waits for a user to approve an action on a separate device with Guardian push showing the details. This is partial support, and CIBA needs an Auth0 Enterprise plan or add-on. [source](https://auth0.com/docs/get-started/authentication-and-authorization-flow/client-initiated-backchannel-authentication-flow) | `okta-ai-agents--c1-3` | owner-accepted | pass |
| Okta workforce approval routing applies to access requests for agent-linked apps, not individual agent actions. Binding message, expiry and replay handling are not described on the page read. [source](https://help.okta.com/oie/en-us/content/topics/ai-agents/ai-agent-govern.htm) | `okta-ai-agents--c1-3` | owner-accepted | pass |
| Bedrock action groups support user confirmation and returning control to the application. Approval identity, expiry and replay protection need application tests, and no deployed configuration was tested. [source](https://docs.aws.amazon.com/bedrock/latest/userguide/agents-userconfirmation.html) | `aws--c1-3` | owner-accepted | pass |
| Wiz has no approval step for actions an AI agent proposes. Its Workflows approval covers only Wiz's own containment actions, so it cannot supply this control. [source](https://www.wiz.io/blog/ai-threat-readiness-pillar-4) | `wiz--c1-3` | owner-accepted | pass |
| Claude Code telemetry carries tool decisions with session and user attributes, which can serve as approval evidence. There is no tamper-evident ledger and local transcripts are editable by the user. [source](https://code.claude.com/docs/en/monitoring-usage) | `claude-code--c7-1` | owner-accepted | pass |
| The Okta System Log records agent token exchanges and Agent Gateway logs every tool call. Tamper evidence, log schema and retention are not described on the pages read, and inputs and outputs are not captured. [source](https://help.okta.com/oie/en-us/content/topics/ai-agents/agent-gateway-activity.htm) | `okta-ai-agents--c7-1` | owner-accepted | pass |
| Alternative if tamper-evident approval records are required: Airia release notes describe an AI Gateway feed with tamper-evident receipts covering identity, session, tool call, policy decision and outcome. The audit documentation requires a login and was not read, and human approval is not described. [source](https://airia.ai/docs/release-notes/release-notes) | `airia--c7-1` (alternative) | owner-accepted | pass |

Next steps:

- Set permissions.defaultMode or disableAutoMode in Claude Code managed settings so a human prompt is retained where approval is required.
- Export Claude Code tool_decision events to write-once storage and confirm each carries the approving user's identity.
- Pilot Auth0 CIBA with RAR for one high-risk agent action and test denial, expiry and replay behaviour.
- Check with your Airia contact for the audit log schema and whether a receipt can be verified independently before considering it.

Not settled by the knowledge base:

- Whether Purview offers any approval step for customer agents, as its record cites no source and only states none was found.
- Whether your Claude Code deployment currently runs in Auto mode or Manual mode.
- Whether your Auth0 plan includes CIBA.
- How Auth0 CIBA handles binding message, expiry and replay.
- Whether any in-stack log is tamper-evident, as none is documented as such.
- Whether Airia can record a human approval event, as the record covers policy decisions only.

## Where this client sits: Measured pilot and go or stop evidence

A team tests one defined task with representative data and users. Planning focus: task selection, data preparation, fit-for-purpose evaluation and stop criteria.

Prerequisite: Representative authorised data, task owner, test environment and agreed acceptance criteria. Completion evidence: Baseline comparison includes failure cases, harms, review effort and documented release recommendation. Do not progress if: Material risk, permission or evidence gaps remain without accountable acceptance.

| Offering | Minimum deliverable | Stack covers | In part | Not covered |
| --- | --- | --- | --- | --- |
| AI opportunity and readiness | Task, owner, data and risk assessment with a bounded prototype choice | 5 | 2 | 0 |
| Agent workflow engineering | One bounded prototype with permitted actions and review gates | 9 | 0 | 0 |
| Evaluation and operating controls | Repeatable evaluation pack, operating owner and release checks | 6 | 4 | 0 |

Offerings are proposed, not accepted services. Verdicts describe documented capability, not a deployment test.
