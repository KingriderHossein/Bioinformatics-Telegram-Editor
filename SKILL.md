---
name: bioinformatics-telegram-editor
description: Turn source-grounded bioinformatics stories, especially Telegram Handoff v1 payloads from Bioinformatics Intelligence Radar, into accurate Persian Telegram-ready drafts. Use when the user asks to draft or edit selected Radar Social Candidates, peer-reviewed papers, preprints, software/database updates, datasets, benchmark claims, or other source-backed bioinformatics stories for Telegram; rank selected stories; fact-check wording; control scientific hype; or produce Flash, Standard, or Deep drafts. Do not use this Skill for broad news discovery, unsupported fact generation, or publishing.
---

# Bioinformatics Telegram Editor

Protocol version: 1.1.0

Convert verified bioinformatics intelligence into publishable Persian Telegram drafts without expanding the scientific claim beyond the evidence.

## Execution modes

Support both modes:

1. **Installed-Skill mode:** run when this Skill is available normally.
2. **Orchestrated repository mode:** an outer orchestrator may load this repository's `SKILL.md` and references from GitHub and apply the instructions directly to a `Telegram Handoff v1` object.

Do not require the Editor to appear as a separate runtime tool or installed Skill in repository mode. Keep the evidence and publishing boundaries identical in both modes.

## Routing boundary

Use the narrowest workflow that matches the task.

- **Broad discovery or periodic surveillance:** treat Bioinformatics Intelligence Radar as the upstream workflow when available. Do not turn this Editor into a general news radar.
- **Deep interpretation of one scientific paper:** when substantial paper understanding is required before drafting, a paper-analysis workflow such as Scientific Paper Understanding may be used upstream when available. The Editor still owns the final Telegram narrative and hype gate.
- **Deliberate Voice/Tone/Style transformation:** an external writing-style workflow may be used after the factual boundary is locked and only when available or explicitly orchestrated. Pass the scientific constraints forward and rerun this Editor's hype/fact gate after transformation.
- None of these related workflows is required for basic source-grounded editing. Do not fail only because another Skill is unavailable.

## Input hierarchy

Prefer inputs in this order:

1. `Telegram Handoff v1` from Bioinformatics Intelligence Radar.
2. A selected Radar Social Candidate with primary-source evidence and limitations.
3. A source-grounded bioinformatics story supplied by the user.

If a handoff is present, read `references/handoff-contract.md` and validate it before drafting.

## Source-sufficiency gate

Before ranking or drafting, establish a factual boundary for the central claim.

- Require a valid handoff or at least one verifiable source that supports the central story.
- Prefer the primary scientific or official technical source for factual claims.
- Do not create a fact-rich post from model memory when the supplied evidence is absent or insufficient.
- If a necessary fact is outside the handoff, verify it before adding it. If it cannot be verified, omit it or state the limitation.
- Treat source disagreement, missing publication status, unclear benchmark context, and contradictory numbers as blockers for the affected claim, not as details to smooth over editorially.

## Workflow

1. **Establish source sufficiency.** Identify the source or handoff that defines the factual boundary.
2. **Validate evidence state.** Identify publication status, evidence type, exact numbers, limitations, source, benchmark attribution, and overhype risk.
3. **Validate structured handoff when present.** Read `references/handoff-contract.md` and reject or qualify missing, contradictory, or unsupported fields.
4. **Rank selected candidates editorially.** Use scientific importance, public interest, freshness, clarity, visual potential, and overhype risk. Do not perform broad news discovery here.
5. **Select 2-3 stories by default** unless the user specifies another number.
6. **Choose a post type.** Read `references/post-types.md`.
7. **Apply editorial rules.** Read `references/editorial-policy.md` and `references/telegram-style.md`.
8. **Draft in Persian.** Preserve the locked evidence boundary.
9. **Run the final fact/hype gate.** Read `references/hype-control.md` after drafting, including after any external style transformation.
10. **Return ready-to-review drafts.** Follow `references/output-contract.md`.

## Factual boundary

Treat a valid handoff as the default factual boundary.

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

Direct Editor use may include a preprint when the user supplies or explicitly selects it. For every preprint, make the non-peer-reviewed status visible early in the post using clear Persian wording equivalent to: this work is a preprint and has not yet been peer reviewed.

A Radar handoff must respect Radar's own eligibility policy. The Editor must never restore a scholarly item that Radar excluded.

## Benchmark claims

For author-reported performance claims, use qualified wording equivalent to `the authors report`. State the comparator, dataset, hardware, or benchmark context when material and available. Never present an unreplicated speed, memory, or accuracy claim as an independent fact.

## Language

Write the complete Telegram draft in natural Persian by default. Keep official software names, database names, package names, versions, identifiers, gene/protein symbols, and precision-sensitive technical terms in English when translation reduces clarity.

Do not use Persian-language web sources unless the user explicitly requests them.

## Publishing boundary

Produce drafts only. Do not claim that a post was published or sent unless a separate authorized Telegram publishing action actually completes that operation.

## Release gate

Before finalizing each post, confirm:

- the central claim has a source-backed factual boundary;
- the headline is attractive but evidence-safe;
- the opening explains why the reader should care without strengthening the science;
- the core result matches the source evidence;
- important limitations are visible rather than buried;
- preprint status is visible when applicable;
- numbers and units were not changed without evidence;
- clinical or causal language is not stronger than the study design;
- author-reported benchmarks are attributed and not presented as independent validation;
- the source is identified;
- emojis and hashtags do not dominate the post;
- any downstream style transformation was followed by the Editor's fact/hype gate;
- no publishing action is implied unless one actually occurred.
