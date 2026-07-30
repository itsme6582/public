# Review: `revenue-generator` prompts (itsme6582/public)

Source: https://github.com/itsme6582/public/tree/main/revenue-generator
Files reviewed: 15 (`2026072901.md` – `2026072915.md`)
Note: `#1`/`#2` and `#7`/`#8` are byte-for-byte duplicates — 13 unique prompts total.

## Main goal, as a whole

This is a set of prompts defining an **autonomous AI agent system for generating revenue with minimal human input and minimal compute cost.** They split into two families:

- **Bootstrapped/organic monetization** (files 1–10): scrape data to sell, patch bugs for bounties, publish SEO/newsletter content, build tools from pain points people complain about online, package data feeds, write affiliate buyer's guides — plus a self-optimizing routine that reroutes cheap tasks to cheaper models.
- **B2G (business-to-government) sales funnel** (files 11–15): find state grants/funding, find state agencies wasting money that AI could save, monitor state RFPs, advise on legal funding models, and auto-generate outreach emails to agencies.

The throughline: **turn agent labor into cash — either directly (sell data/content/patches) or by winning government contracts/funding for an AI platform — while keeping token/compute spend below the expected payout.**

## Ranking 1 — Speed to actual cash (fastest → slowest)

1. **#1/#2** Lead/dataset sale — sells immediately, has hard cost cap
2. **#10** Affiliate buyer's guide — content converts to commission fast
3. **#3** Bug bounty PR — payout on acceptance, but gated on manual approval
4. **#6** SEO articles — needs to rank first (weeks/months)
5. **#4** Newsletter/blog — needs an audience for sponsorship revenue
6. **#7/#8** Tool from scraped complaints — needs to be built *and* sold
7. **#9** Data feed/dashboard — needs a pipeline built and customers found
8. **#15** Agency outreach emails — starts a sales cycle, not a sale
9. **#13** RFP/procurement monitor — surfaces opportunities, doesn't close them
10. **#11** Grant finder — funding, not revenue, and slow to land
11. **#12** ROI business case — pre-sales collateral
12. **#14** Funding-model advisor — pure planning
13. **#5** Cost-optimization daemon — saves money, generates none

## Ranking 2 — Structural complexity (most → least engineered)

1. **#1/#2, #3, #4, #5** — full `/goal /routines /constraints /loop` agent framework with explicit sub-steps, hard limits, and scheduling logic. Read like production agent specs.
2. **#7/#8, #9, #11, #13, #15** — single-paragraph prompts, but each implies a multi-step research/synthesis task.
3. **#6, #10, #12, #14** — simplest, closest to one-shot content-generation prompts.

## Ranking 3 — Legal/compliance risk (highest → lowest)

1. **#1/#2** — scraping and reselling lead/business data raises ToS and data-resale exposure
2. **#7/#8** — scraping Reddit/Twitter/forums for product ideas, similar ToS risk
3. **#3** — submitting security patches to real repos carries responsible-disclosure and liability concerns
4. **#9** — combining public datasets into a paid product; mild licensing risk depending on sources
5. **#6, #10** — SEO/affiliate content; low risk if claims are sourced and disclosed
6. **#11, #12, #13, #15** — government-facing, but explicitly scoped to *public* data (budgets, procurement portals) — lower legal exposure
7. **#14** — lowest risk by design; the one prompt explicitly built to check compliance and flag improper billing
8. **#4, #5** — internal content generation / internal cost optimization; essentially no external legal exposure

## Open item

`#1`/`#2` and `#7`/`#8` are exact duplicates in the repo — worth cleaning up.