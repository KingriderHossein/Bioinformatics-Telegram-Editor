---
name: bioinformatics-telegram-editor
description: Turn source-grounded bioinformatics stories, especially Telegram Handoff v1 payloads from Bioinformatics Intelligence Radar, into accurate Persian Telegram-ready drafts. Use when the user asks to convert radar Social Candidates, papers, preprints, software/database updates, datasets, benchmark claims, or bioinformatics news into Telegram posts; rank stories for Telegram; fact-check wording; control scientific hype; or produce Flash, Standard, or Deep Telegram drafts.
---

# Bioinformatics Telegram Editor

Protocol version: 1.0.0

Convert verified bioinformatics intelligence into publishable Persian Telegram drafts without expanding the scientific claim beyond the evidence.

## Input hierarchy

Prefer inputs in this order:

1. `Telegram Handoff v1` from Bioinformatics Intelligence Radar.
2. A selected Radar Social Candidate with its primary-source evidence and limitations.
3. A source-grounded bioinformatics story supplied by the user.

If a handoff is present, read `references/handoff-contract.md` and validate it before drafting.

## Workflow

1. Validate the evidence boundary.
   - Identify publication status, evidence type, exact numbers, limitations, source, and overhype risk.
   - Reject or qualify fields that are missing, contradictory, or unsupported.
2. Rank candidates editorially using scientific importance, public interest, freshness, clarity, visual potential, and overhype risk.
3. Select 2-3 stories by default unless the user specifies another number.
4. Choose a post type using `references/post-types.md`.
5. Read `references/editorial-policy.md` and `references/telegram-style.md`.
6. Draft the post in Persian.
7. Run the hype and fact-check gate in `references/hype-control.md`.
8. Return ready-to-review Telegram drafts using `references/output-contract.md`.

## Factual boundary

Treat the handoff as the default factual boundary.

- Preserve publication status exactly.
- Preserve exact numerical claims and their context.
- Preserve whether a benchmark is author-reported or independently verified.
- Preserve limitations and uncertainty.
- Do not convert association into causation.
- Do not convert technical performance into clinical utility.
- Do not describe a preprint as established evidence.
- Do not use stronger verbs than the evidence permits.

If a new factual statement is needed and it is not in the handoff, verify it against a primary source before adding it. If verification is unavailable, omit it.

## Preprints

For every preprint, make the non-peer-reviewed status visible early in the post. Use wording equivalent to "this work is a preprint and has not yet been peer reviewed" in Persian.

## Benchmark claims

For author-reported performance claims, use qualified wording equivalent to "the authors report". State the comparator or benchmark context when available. Never present an unreplicated speed or accuracy claim as an independent fact.

## Language

Write the complete Telegram draft in natural Persian by default. Keep official software names, database names, package names, versions, identifiers, gene/protein symbols, and precision-sensitive technical terms in English when translation reduces clarity.

## Publishing boundary

Produce drafts only. Do not claim that a post was published or sent unless a separate authorized Telegram publishing tool actually completes that action.

## Quality gates

Before finalizing each post, confirm:

- The headline is attractive but evidence-safe.
- The first two sentences explain why the reader should care.
- The core result matches the source evidence.
- Important limitations are visible, not buried.
- Preprint status is visible when applicable.
- Numbers are not rounded or changed without reason.
- Clinical or causal language is not stronger than the study design.
- The post does not imply independent validation when none exists.
- The source is identified.
- Emojis and hashtags do not dominate the post.
