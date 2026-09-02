# Bioinformatics Telegram Editor

A ChatGPT Skill that turns source-grounded bioinformatics intelligence into accurate Persian Telegram-ready drafts.

## Protocol

Version: 1.1.0

Preferred upstream input: `Telegram Handoff v1` from Bioinformatics Intelligence Radar.

## Core design

Radar owns broad discovery and Radar-level verification. Telegram Editor owns selected-story ranking, narrative construction, readability, and hype control. The Editor must not strengthen a scientific claim beyond the evidence supplied by Radar or independently verified from a primary source.

Version 1.1.0 adds a source-sufficiency gate and explicit routing boundaries. The Editor no longer behaves like a general news-discovery system, does not draft unsupported factual posts from model memory, and can optionally receive upstream paper analysis or downstream style transformation without making those Skills hard dependencies.

## Default output

- 2-3 selected Telegram drafts unless the user requests another number
- Persian prose
- Flash, Standard, or Deep format
- visible preprint/benchmark limitations when applicable
- source identification
- no automatic publishing

## Orchestrated execution

The Editor does not need to be installed as a separate Skill when an outer orchestrator can read this repository. The orchestrator can load `SKILL.md` plus the referenced policies and apply them directly to `Telegram Handoff v1`.

Related Skills remain optional. If a paper-understanding or writing-style workflow is used, the Editor keeps the final authority over scientific wording and reruns its fact/hype gate before release.
