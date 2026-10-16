# MTL-XF-022 — Data workspace

## Required sources and cohort

MHCLG Statutory Homelessness — England time series + detailed LA Jan–Mar 2026. Historical releases are maintained over many years.

Use the agreed England time-series ODS and detailed LA January–March 2026 ODS. National trends use matching quarters available in the frozen time series; LA comparisons use January–March 2026 only. Earlier LA quarters are an extension requiring separately registered official files.

[Source register and exact URLs](SOURCE_REGISTER.md)

**Current state:** specification only. No raw datasets have been downloaded or uploaded in this build. Expected size, row count and history statements from the earlier agreement require verification against the actual files. Do not mark the cohort frozen until the manifest and metadata are complete.

## Controlled acquisition and preparation

1. Read [SOURCE_REGISTER.md](SOURCE_REGISTER.md); use the exact agreed URLs and official publisher documentation.
2. Validate that the response is the expected CSV/ODS/XLSX/ZIP rather than an error page. Inspect archive contents and sheet names where relevant.
3. Record resolved URL, UTC retrieval, release, coverage, filename, bytes, SHA-256 and licence evidence. Log discrepancies before changing sources.
4. Preserve original bytes in an approved immutable snapshot; later upload only where instructed and redistribution is permitted.
5. Record source fields, types, valid values, suppression, units and publisher methodology in [metadata](metadata/README.md).
6. Implement the analytical grain below, verify keys/cardinality and account for excluded/quarantined records.
7. Reconcile at least five published measures and create curated outputs reproducibly in the team repository.

## Analytical grain

Maintain separate quarterly national/available-geography duty-flow facts and quarter-end LA temporary-accommodation stock facts; include table identifier, household category, duty and outcome dimensions. National trends do not create an LA historical panel.

## Required metric contract

| Metric | Required definition / calculation |
| --- | --- |
| Prevention duties owed | Published quarterly households owed a prevention duty. |
| Relief duties owed | Published quarterly households owed a relief duty; do not add duties to infer unique households. |
| Prevention accommodation outcome share | 100 × prevention duties ended with secured accommodation / relevant prevention duties ended, using the publisher's outcome categories. |
| Relief accommodation outcome share | 100 × relief duties ended with secured accommodation / relevant relief duties ended. |
| Temporary-accommodation stock | Households in temporary accommodation at the quarter-end reference date. |
| Family accommodation share | 100 × stock households with dependent children / total temporary-accommodation households, where supported. |
| National comparable-quarter change | 100 × (current count / same quarter previous year − 1); zero base produces unavailable. |
| Reporting completeness | Valid authority returns / expected authorities for the selected table and quarter. |

## Mandatory quality risks

- Stock, new placements and duty flows describe different things and must not be summed.
- The core files do not automatically establish costs, length of stay or prevention effectiveness.
- Outcome shares are administrative indicators, not causal estimates or same-cohort conversion rates.

1. Reconcile five national/LA published totals without double-counting table subtotals.
2. Test that quarter-end stock cannot be added to quarterly duty flows.
3. Test zero and missing duty-ended denominators.
4. Verify the LA page is labelled January–March 2026 and has no fabricated historical trend.

## Folder ownership

- [raw](raw/README.md): unmodified approved source snapshots; guidance only at present.
- [reference](reference/README.md): governed code lists, hierarchies and crosswalks.
- [metadata](metadata/README.md): source notices, schema, glossary, lineage and manifest evidence.

Curated data, processing code, logs and test results belong in the team delivery repository. Preserve a reproducible boundary between source inputs and generated products. Do not add personal, confidential or paid-source data.
