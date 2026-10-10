---
type: "Guide"
title: "Ingestion rules for the offerings atlas tree"
description: "How atlas records become pages in this tree, which pages agents may retrieve, and what the ingest refuses."
classification: "C1"
owner: "human:markus"
status: "stable"
review: "pending"
verification: "not applicable"
tags:
  - "rules"
sources:
  - id: "decision-0010"
    resource: "offerings-atlas decisions/0010-atlas-okf-business-kb.md"
    locator: "Proposed choice, items 1 to 8"
generated:
  by: "human:markus"
  at: "2026-10-10T18:00:00+10:00"
---

These rules govern every page in this tree. They are the only authored file here. `tools/okf_tree.py` in the offerings-atlas repository reads the block at the end of this file, builds the tree from the atlas store, and refuses to write if any page breaks a rule. Decision 0010 in the atlas sets the policy. This file states it in a form the ingest can check.

## Where the facts come from

The atlas store is the only source. Findings come from `knowledge/findings/`, sources from `data/sources.json` and `data/source-register.json`, products from `data/research/products/`, controls from `data/catalog.json` and column groups from `data/research-groups.json`. Never edit a page in this tree. Change the store and rerun the ingest. A rerun is deterministic for a given repository state and `--at` time.

## Type mapping

| Atlas record | Page | Type |
| --- | --- | --- |
| Finding, one matrix cell | `columns/<platform>/<control>.md` | Platform capability |
| Column | `columns/<platform>/profile.md` | Platform profile |
| Sources a column cites | `columns/<platform>/sources.md` | Registry |
| Control | `controls/<control>.md` | Control |
| Atlas offering proposals | `registers/offering-controls.md` | Registry |
| Rules and agent guide | `rules/ingestion.md`, `AGENTS.md` | Guide |

Offering and Decision pages are refused. Offerings live in the kb-hub business tree and only the owner accepts them. Claims and products are rendered inside their finding and profile pages.

## Frontmatter

Every page carries `type`, `title`, `description`, `classification`, `owner`, `status`, `review`, `verification`, `tags`, `sources` and `generated`. Finding pages add an `atlas` block (platform, control, group, verdict, eligibility and its reasons, high-risk tags, check date, and the origin file with its SHA-256), plus `stale_after` and OKF `verified` events when an evaluator has verified them. The `atlas` block also records `eligibility_basis`: `agent-verified`, `owner-accepted` or null.

`retrieval-index.json` lists every concept page with its path, platform, group, control, category, verdict, verification, eligibility basis, eligibility, sources (URL, locator, tier), chunk names and SHA-256, so a consumer can filter and fetch without parsing YAML.

- `classification` is C1 for the whole tree.
- `review` is always `pending`. Only the owner sets `approved`, and never in this tree.
- `verified` events are written only from evaluator runs, as `evaluator/<family>`. A `human:` verifier is never generated.
- `generated.by` is the ingest process. The finding's own author stays in `owner`.
- Each `sources` entry has `id`, `resource` (the registered URL), `locator` and `tier`.

## Tags

Finding pages get four tags, in order: the column group id, the control category as a slug, the researcher verdict and the verification state. Profiles and registries carry the group id, controls carry the category.

## Chunks

A finding page opens with one orientation paragraph, then six sections, each preceded by a `chunk` comment so a retriever can split and cite them: answer, products, gaps, options, evidence and sources. No chunk may exceed the word limit below.

## Eligibility

A verified finding is agent-eligible on evaluator evidence when all of these hold:

1. One evaluation is supported, passed the quote check, used a tier 1 or 2 source whose registered tier and URL match, and came from a different run than the one that drafted the finding.
2. A high-risk finding (decision 0008) has such evaluations from two model families.
3. No later evaluation is contradicted or outdated.
4. The verdict is not `not-addressed`. Absence checks are shown but never verify.
5. The classification is C1 and the page was not withheld.
6. The recheck date (`review_on`) is after the generation date. It becomes `eligible_until`.

A page that meets these rules has `eligibility_basis: agent-verified`.

### Proof-of-concept basis: owner acceptance

For this proof of concept only, the owner accepted every researched finding that no evaluator run has checked (`data/owner-acceptance.json`, 2026-10-10). Such a finding is agent-eligible with `eligibility_basis: owner-accepted` when it is unverified, has no evaluation and no absence check, and is C1 and not withheld. It has no `eligible_until` and no OKF `verified` event, because no agent or person has checked the page itself. An evaluator verdict replaces it: once a finding has any evaluation, only the agent-verified basis can make it eligible. Contested, invalidated, stale and provisional findings are never eligible on either basis. A real enterprise tree turns this basis off by setting `owner_acceptance.enabled` to false.

Eligible pages get `status: stable` and an entry in `agent-eligible.json` with their basis. Every other page is `status: draft`, shows its state and the reasons it is not eligible, and stays readable for people. Agents filter on `agent-eligible.json` before retrieval.

## Withholding

A finding whose text contains a money figure, an email address, a phone number, an IPv4 address or a match on the kb-hub redaction list is withheld whole and listed in `withheld.json`. It is never rewritten, because rewriting a quoted source passage changes the evidence. Every URL in the tree must be the registered URL of an atlas source, or the ingest stops.

## Rules block

<!-- rules:begin -->
```json
{
  "profile": "offerings-atlas-tree/1",
  "okf_version": "0.2",
  "tree_id": "offerings-atlas",
  "default_groups": "all",
  "generated_by": "process:offerings-atlas-ingest",
  "classification": ["C1"],
  "review": "pending",
  "status_when_eligible": "stable",
  "status_otherwise": "draft",
  "types": {
    "finding": "Platform capability",
    "column": "Platform profile",
    "sources": "Registry",
    "control": "Control",
    "offerings": "Registry",
    "guide": "Guide"
  },
  "forbidden_types": ["Offering", "Decision"],
  "required_frontmatter": ["type", "title", "description", "classification", "owner", "status", "review",
                           "verification", "tags", "sources", "generated"],
  "states": ["unverified", "provisional", "verified", "contested", "stale", "invalidated"],
  "tags": ["group", "category", "verdict", "state"],
  "finding_chunks": ["answer", "products", "gaps", "options", "evidence", "sources"],
  "max_chunk_words": 600,
  "eligibility_bases": ["agent-verified", "owner-accepted"],
  "owner_acceptance": {
    "enabled": true,
    "record": "data/owner-acceptance.json",
    "basis": "owner-accepted",
    "states": ["unverified"],
    "proof_of_concept_only": true
  },
  "eligibility": {
    "state": "verified",
    "outcome": "supported",
    "quote_check": "pass",
    "tiers": [1, 2],
    "high_risk_families": 2,
    "disagreeing_outcomes": ["contradicted", "outdated"],
    "never_eligible_verdicts": ["not-addressed"]
  },
  "withhold_patterns": {
    "money": "(?:US|AU)?\\$\\s?\\d|\\bAUD\\s?\\d",
    "email": "\\b[A-Za-z0-9._%+-]+@[A-Za-z0-9.-]+\\.[A-Za-z]{2,}\\b",
    "phone": "(?<!\\w)(?:\\+61[ -]?[2-478]|0[2-478])[ -]?\\d(?:[ -]?\\d){7}(?!\\w)",
    "ipv4": "\\b(?:25[0-5]|2[0-4]\\d|1?\\d?\\d)(?:\\.(?:25[0-5]|2[0-4]\\d|1?\\d?\\d)){3}\\b"
  }
}
```
<!-- rules:end -->
