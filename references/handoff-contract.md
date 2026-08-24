# Telegram Handoff v1

Use this schema as the preferred machine-readable contract between Bioinformatics Intelligence Radar and Bioinformatics Telegram Editor.

## Top-level fields

- `handoff_version`: must be `1.0`.
- `radar_version`: Radar protocol version.
- `radar_date`: ISO date.
- `reporting_window`: object with `start` and `end` ISO dates/times when available.
- `candidate_count`: number of candidate objects.
- `candidates`: array of 3-5 selected stories on normal days.

## Candidate fields

Required:

- `id`: stable ID such as `BIR-20260824-01`.
- `topic`: concise technical topic.
- `scientific_title`: original paper/release/resource title when available.
- `suggested_social_title_fa`: evidence-safe Persian title suggestion.
- `hook_fa`: one-sentence Persian hook.
- `summary_fa`: concise Persian factual summary.
- `why_it_matters_fa`: Persian public-interest explanation.
- `content_type`: one of `peer_reviewed`, `preprint`, `software_release`, `database_update`, `dataset`, `service_change`, `other`.
- `publication_status`: exact evidence status.
- `priority`: `CRITICAL`, `HIGH`, `MEDIUM`, or `WATCH`.
- `social_score`: integer 0-30.
- `overhype_risk`: `LOW`, `MEDIUM`, or `HIGH`.
- `claim_status`: concise statement such as `peer-reviewed finding`, `author-reported benchmark`, `independent experimental challenge`, or `official service change`.
- `key_facts`: array of factual statements. Preserve exact numbers and qualifiers.
- `limitations_fa`: array of limitations or uncertainty notes in Persian.
- `do_not_say_fa`: array of tempting but unsupported claims the editor must not make.
- `source`: object containing `primary_name`, `primary_url` when available, and durable identifiers such as DOI/PMID/release tag when available.

Recommended:

- `benchmark_claims`: array with claim, comparator, dataset/hardware context, and independent verification state.
- `repository`: project/repository metadata verified by Radar.
- `recommended_post_type`: `FLASH`, `STANDARD`, or `DEEP`.
- `recommended_formats`: array such as `Telegram`, `Instagram carousel`, `X thread`.
- `editorial_angle_fa`: suggested story angle in Persian.

## Validation rules

- `candidate_count` must equal the array length.
- Do not infer missing scientific facts from the headline.
- Primary-source evidence outranks the suggested social title.
- A `preprint` content type must not have a peer-reviewed publication status.
- `author-reported benchmark` must not be rewritten as independently verified.
- If `primary_url` is absent, use available DOI/PMID/release identifiers and do not invent a URL.

## Orchestrated mode

This contract does not require direct Skill-to-Skill invocation. An outer orchestrator may construct the handoff after Radar, keep it in the same execution context, load this repository's instructions, and apply the Editor workflow directly. Missing installed-Skill discovery is not an error in orchestrated repository mode.
