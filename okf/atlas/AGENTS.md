---
type: "Guide"
title: "Agent guide to the offerings atlas tree"
description: "How agents read this tree, and why they never write to it."
classification: "C1"
owner: "human:markus"
status: "draft"
review: "pending"
verification: "not applicable"
tags:
  - "rules"
sources:
  - id: "decision-0010"
    resource: "offerings-atlas decisions/0010-atlas-okf-business-kb.md"
    locator: "Proposed choice"
generated:
  by: "process:offerings-atlas-ingest"
  at: "2026-10-10T18:00:00+10:00"
---

This tree is generated. Never edit it. Change the atlas store and rerun the ingest, under the [ingestion rules](rules/ingestion.md).

## Reading

1. Load `agent-eligible.json` (or `retrieval-index.json`) and drop entries whose `eligible_until` has passed.
   Each entry names its basis: `agent-verified` (an evaluator checked it) or `owner-accepted` (proof-of-concept only, unchecked research the owner accepted). Say which when you quote it.
2. Retrieve, index or summarise only the pages left in that list. Every other page is for people to read.
3. Quote a cell with its verdict, its state, its gaps and its sources. A positive answer alone drops qualifiers.

## What the states mean

| State | Meaning |
| --- | --- |
| verified | An evaluator found a tier 1 or 2 passage that supports the finding |
| provisional | Supported by a tier 3 source only, expires after 30 days |
| unverified | Researcher output, not yet checked |
| contested | Evaluators or sources disagree |
| stale | Was verified, recheck date passed |

## What this tree never holds

Business decisions, prices, accepted offerings or anything marked `review: approved`. Offerings live in the kb-hub business tree, decided by the owner.
