# MTL-XF-022 — Data workspace and support gate

## Core contract

England quarterly national trend plus a January–March 2026 LA diagnostic snapshot. Keep prevention duties, relief duties, duty-ending outcomes and quarter-end accommodation in separate facts. Use source-published household-normalised rates only if the workbook supplies their exact denominator; otherwise label comparisons as unadjusted.

## Optional work

LA longitudinal comparisons need additional official quarterly files. Costs, median stay, individual pathways and causal prevention effectiveness require additional evidence and are not core commitments. Published duration categories, if present, must not be converted into an invented mean stay.

## Acquisition state

No raw data is uploaded by this update. Official documentation checks are recorded in [SOURCE_REGISTER.md](SOURCE_REGISTER.md). File payloads, full schemas, bytes/checksums and final reuse/freeze approvals remain pending where stated. Keep publication-level evidence distinct from acquired-file evidence.

## Required source-to-deliverable matrix

Before analysis, create a row per headline measure/required comparison:

`requirement_id | deliverable_id | metric | core_or_extension | source_id | actual_field_or_sheet | valid_grain | coverage | unit_denominator | metadata_evidence | support_status | owner | decision`

Allowed support statuses: documentation-supported; payload-verified; unsupported; optional-not-activated. “Documentation-supported” alone is insufficient for a completed data freeze. If a mandatory field is absent, block its output and resolve the source or approved scope; do not fabricate values or silently waive the requirement.

## Controlled preparation

1. Use registered exact URLs and inspect actual content type, archive members or sheets.
2. Record version, resolved URL, separate retrieval timestamps, bytes, SHA-256 and licence evidence.
3. Approve the actual cohort and scope matrix at G1.
4. Preserve original bytes; transform into curated facts with documented types, keys, hierarchies and joins.
5. Account for retained/excluded/quarantined rows and quantify all mapping gaps.
6. Reconcile five source values and execute [DT1–DT10](../project/ACCEPTANCE_CRITERIA.md).

## Model and measures

Maintain separate quarterly national/available-geography duty-flow facts and quarter-end LA temporary-accommodation stock facts; include table identifier, household category, duty and outcome dimensions. National trends do not create an LA historical panel.

The core contract above controls conditional dimensions. Metric formulas have one authoritative home: [DELIVERABLES.md](../project/DELIVERABLES.md). Do not create another incompatible formula copy in the data README.

## Data areas

- [Raw snapshots](raw/README.md): unmodified source bytes only when later authorised and permitted.
- [Reference data](reference/README.md): category/entity/period mappings with version and cardinality.
- [Metadata](metadata/README.md): manifest, dictionary, methodology, lineage and support/freeze decisions.

**Specific control:** Duty flows, ended-duty outcomes and quarter-end accommodation stocks have incompatible populations and reference dates.
