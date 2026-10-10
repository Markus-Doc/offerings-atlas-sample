---
type: freshness-pull-request
pr_id: FRESH-2026-10-10-001
raised_by: agent:freshness (run fresh-demo-3), simulated enterprise gate
run_timestamp: 2026-10-10T04:24:34Z
target_document: knowledge/findings/aws/c2-2.md (sandbox)
target_version: d06e928ea0cadcce7ef5639d24dbba2004da7fde4b873c5e859a2aa745914713
evidence_cut_of_target: 2026-10-08
scan_window: 2026-10-08 to 2026-10-10
status: AWAITING HUMAN APPROVAL
---

# Freshness pull request FRESH-2026-10-10-001

**Simulation notice.** This is a demonstration of decision 0009, run on a sandbox copy of the KB with a synthetic page change. The freshness agent produced the detection, the affected findings, the evidence hashes and the queued evaluator jobs. The proposed wording was scripted for the demo in the role of the researcher agent, since this build makes no model calls. Decision 0005 keeps facts in this KB agent-run with no human gate. This document shows how an enterprise knowledge tree that keeps a human gate, as kb-hub decision 0002 does, would receive the same change. The approvers are synthetic roles, not people.

## Summary

One page change, two findings reached, one material change proposed. The central claim of the target, that Claude Sonnet 5.5 on Bedrock has no Australian Geo route, does not survive the scan.

| No. | Change | Section affected | Type | Materiality | Confidence |
| --- | --- | --- | --- | --- | --- |
| 1 | Claude Sonnet 5.5 gains an au. Geo inference route on Bedrock | Answer | Contradicted by source | High: residency and routing (high-risk under decision 0008) | Not set: confidence never sets a state |
| 2 | Same page change reaches knowledge/findings/anthropic/c2-2.md through the register `covers` list | Answer | Recheck only | Low: wording does not name the model | Not set |

## Change 1: knowledge/findings/aws/c2-2.md (sandbox)

Target section: Answer. Change type: contradicted by a tier 1 source.

Current text, quoted exactly:

> On Amazon Bedrock, Claude Sonnet 5.5 has no Australian Geo inference route. Its Geo inference IDs are listed for us. and eu. only, so from Sydney and Melbourne it is offered only through Global routing. Opus 5.5 and Haiku 5.5 have au. Geo routes that keep processing in Sydney or Melbourne.

What has changed in the world: the page's hashed sections changed. Units the freshness check reported:

- `Geo inference ID: au.anthropic.claude-sonnet-5-5 / ap-southeast-2 (Sydney)`: added
- `Geo inference ID: au.anthropic.claude-sonnet-5-5 / ap-southeast-4 (Melbourne)`: added
- `Programmatic Access / bedrock-runtime`: modified

Evidence:

| Field | Value |
| --- | --- |
| Source | SRC-AWS-CARD-SONNET-5-5 (tier 1) |
| URL | https://docs.aws.amazon.com/bedrock/latest/userguide/model-card-anthropic-claude-sonnet-5-5.html |
| Fetched | 2026-10-10T04:24:34Z, HTTP 200 |
| Raw body SHA-256 | `140c4c8037c17665ba1f4e4f554072ea69129436951e4723520cb1a91f94696c` |
| Normalised text SHA-256 | `52d66db49b68545fd174b2ba93adef909e09fda81ceebe47bee1d8cde034de32` |
| Section SHA-256, before and after | `fa85a1d4b26ed013a8a79661fd699d5297a4d44493a58da7dee55a3dd8c489ee` to `8917eb29374adb2f53eacc8f229ca7c48e7274c9d2379caad70904bb83a7b140` |
| Signal | `sig-20261010-be926726` |
| Evaluator job | `ej-39d7101e3caa3b03`, priority 0, families anthropic and openai |

Passage, verbatim from the fetched page (quote check: pass):

> Geo inference ID: `au.anthropic.claude-sonnet-5-5`

Proposed wording:

> On Amazon Bedrock, Claude Sonnet 5.5 lists an au. Geo inference ID, au.anthropic.claude-sonnet-5-5. From Sydney and Melbourne it routes to Sydney or Melbourne, as Opus 5.5 and Haiku 5.5 do. Global routing remains available and can send requests outside Australia.

**Judgement handed to the knowledge owner: whether client guidance that recommended Opus 5.5 or Haiku 5.5 for Australia-bounded processing should now include Sonnet 5.5.** That is advice, not a fact edit, and stays with a person in an enterprise tree.

## Scanned, no change proposed

| Thread checked | What was checked | Action |
| --- | --- | --- |
| knowledge/findings/anthropic/c2-2.md | Answer wording against the changed units. The text speaks of model catalogues generally and does not name Sonnet 5.5 or a region | Evaluator recheck queued (`ej-a77de43879f3024a`). No wording change proposed |
| Page sections outside Programmatic Access and Regional Availability | Not hashed by design | None. A footer date changed and raised nothing |

## Approval gate

Each approver signs in order. A rejection at any step stops the chain.

- [ ] **Knowledge owner, AI platforms** approves change 1. Approving commits this role to: the new wording is accurate and within the tree's scope.
- [ ] **Security reviewer** approves change 1. Approving commits this role to: the residency and routing statement is safe to give to a client.
- [ ] **Publisher** approves change 1. Approving commits this role to: the approved text replaces the old text in the published tree, with history kept.

Decision: accept all / accept with amendments / reject / defer. Reviewer roles and dates are recorded against each tick.

## Outcomes, simulated on copies of the sandbox

| Outcome | Finding state after | What else happens |
| --- | --- | --- |
| Approved by all three roles | `unverified` | The approved wording replaces the claim. Because the claimed text changed, the store sends it to unverified. The queued evaluator job now meets a new revision, so the curator requeues it to check the new wording against the new page. In the enterprise tree the published version moves to the new text with the old one kept in history. |
| Rejected at any step | `stale` | The original text stays, shown with its age. The evaluator job still runs. A contradicted verdict against the tier 1 page would invalidate the claim under decision 0005, so a rejection cannot keep a wrong fact verified. |

## Sources

- SRC-AWS-CARD-SONNET-5-5, fetched by the demo from a synthetic fixture standing in for https://docs.aws.amazon.com/bedrock/latest/userguide/model-card-anthropic-claude-sonnet-5-5.html
- Original claim: paraphrases the observed result of 2026-10-08 in research/source-decision-log-2026-10-08.md, decision 7 follow-up
