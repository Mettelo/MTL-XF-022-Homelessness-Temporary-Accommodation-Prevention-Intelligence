# MTL-XF-022 — Metadata, lineage and freeze evidence

Metadata makes statutory homelessness, temporary accommodation & prevention performance intelligence reproducible. This folder currently contains guidance; no acquisition manifest or source sign-off is claimed.

## Required records after acquisition

- Source manifest: source ID, exact/resolved URL, retrieval UTC, actual release, filename, bytes, SHA-256, archive members/sheets and coverage.
- Publisher methodology and licence/attribution evidence with provenance and retrieval date.
- Schema and field dictionary: name, type, meaning, units, key role, missing/suppression markers and valid values.
- Business glossary and critical data elements, with named steward and approved definitions.
- Grain, hierarchy and join-cardinality documentation.
- Field-level lineage from raw fields through transformations to each headline metric/dashboard measure.
- Quality profile, row-accounting reconciliation, exclusions, unresolved exceptions and their decision impact.
- Freeze approval, change log and later revision comparisons.

## Model contract

Maintain separate quarterly national/available-geography duty-flow facts and quarter-end LA temporary-accommodation stock facts; include table identifier, household category, duty and outcome dimensions. National trends do not create an LA historical panel.

## Metric definition coverage

- Prevention duties owed: Published quarterly households owed a prevention duty.
- Relief duties owed: Published quarterly households owed a relief duty; do not add duties to infer unique households.
- Prevention accommodation outcome share: 100 × prevention duties ended with secured accommodation / relevant prevention duties ended, using the publisher's outcome categories.
- Relief accommodation outcome share: 100 × relief duties ended with secured accommodation / relevant relief duties ended.
- Temporary-accommodation stock: Households in temporary accommodation at the quarter-end reference date.
- Family accommodation share: 100 × stock households with dependent children / total temporary-accommodation households, where supported.
- National comparable-quarter change: 100 × (current count / same quarter previous year − 1); zero base produces unavailable.
- Reporting completeness: Valid authority returns / expected authorities for the selected table and quarter.

Every listed metric needs source fields, transformation/formula, valid grain, unit, numerator/denominator, exclusions, zero/missing behaviour, refresh expectation, owner and test reference. Mark conditional metrics unavailable if the actual source cannot support them.

Store actual evidence only; never invent publisher schema, a completed licence review, a checksum or a stakeholder approval. See [source register](../SOURCE_REGISTER.md) and [acceptance criteria](../../project/ACCEPTANCE_CRITERIA.md).
