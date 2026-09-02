# Changelog

## 1.1.0 - 2026-09-02

- Added a source-sufficiency gate before ranking and drafting.
- Prevented unsupported fact-rich Telegram posts from being generated from model memory when evidence is absent or insufficient.
- Clarified routing boundaries: broad discovery belongs upstream, while the Editor owns selected-story narrative and hype control.
- Added optional interoperability with paper-understanding and writing-style workflows without creating hard Skill dependencies.
- Required the Editor fact/hype gate to run again after any external style transformation.
- Clarified that direct Editor use may handle an explicitly supplied preprint while Radar handoffs must preserve Radar's stricter eligibility policy.
- Added `default_prompt` to `agents/openai.yaml`.
- Refined the frontmatter trigger to exclude broad news discovery, unsupported fact generation, and publishing.

## 1.0.1 - 2026-08-24

- Added orchestrated repository mode so the Editor can be applied from canonical GitHub instructions without being installed as a runtime Skill.
- Clarified that missing Skill discovery is not an error when an outer orchestrator has loaded the Editor repository.
- Preserved the same evidence, hype-control, and publishing boundaries in both execution modes.

## 1.0.0 - 2026-08-24

- Added Telegram Handoff v1 as the preferred input contract.
- Added Persian Telegram editorial workflow.
- Added Flash, Standard, and Deep post types.
- Added scientific hype-control and fact-check gates.
- Added explicit preprint and author-reported benchmark handling.
- Added source-grounded editorial ranking and ready-to-review drafts.
