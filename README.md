# Bioinformatics Telegram Editor

A ChatGPT Skill that turns source-grounded bioinformatics intelligence into accurate Persian Telegram-ready drafts.

## Protocol

Version: 1.0.1

Preferred upstream input: `Telegram Handoff v1` from Bioinformatics Intelligence Radar.

## Core design

Radar owns discovery and verification. Telegram Editor owns story selection, narrative, readability, and hype control. The editor must not strengthen a scientific claim beyond the evidence supplied by Radar or independently verified from a primary source.

## Default output

- 2-3 selected Telegram drafts
- Persian prose
- Flash, Standard, or Deep format
- visible preprint/benchmark limitations
- source identification
- no automatic publishing

## Orchestrated execution

The Editor does not need to be installed as a separate Skill when an outer orchestrator can read this repository. The orchestrator can load `SKILL.md` plus the referenced policies and apply them directly to Telegram Handoff v1.
