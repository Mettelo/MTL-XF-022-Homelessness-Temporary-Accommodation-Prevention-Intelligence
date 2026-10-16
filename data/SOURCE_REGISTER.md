# MTL-XF-022 — Source register and verification record

**Project:** Statutory Homelessness, Temporary Accommodation & Prevention Performance Intelligence  
**Documentation review:** 16 October 2026  
**State:** official documentation checked; acquired-file validation and freeze approval pending.  
**Steward:** Data Governance Analyst, with the project domain specialist.

## Source/cohort decision

England quarterly national trend plus a January–March 2026 LA diagnostic snapshot. Keep prevention duties, relief duties, duty-ending outcomes and quarter-end accommodation in separate facts. Use source-published household-normalised rates only if the workbook supplies their exact denominator; otherwise label comparisons as unadjusted.

**Outside core:** LA longitudinal comparisons need additional official quarterly files. Costs, median stay, individual pathways and causal prevention effectiveness require additional evidence and are not core commitments. Published duration categories, if present, must not be converted into an invented mean stay.

## Official publication and methodology references

| Official reference | URL |
| --- | --- |
| Official tables and archived releases | https://www.gov.uk/government/statistical-data-sets/live-tables-on-homelessness |

References above were inspected for this revision. They establish only the evidence described below; they are not a completed file acquisition, licence clearance or signed freeze.

## Verification findings

The official live-tables page lists the January–March 2026 detailed LA workbook and an England time series. Its update history records revisions, including corrections to prevention/relief and accommodation tables. A valid freeze must record the actual workbook version rather than only the quarter in its name.

**Field/reference mapping and acquisition instructions:** Inspect workbook contents and notes to map authority code, table identifier, quarter/reference date, duties owed, duty-ended outcomes, temporary-accommodation households and family categories. Do not invent column or sheet names from the business labels.

**Remaining status:** Publication and workbook listings verified; internal sheet/field mappings, outcome categories, licences and frozen file identity pending.

## Exact copyable file URLs

Original agreed URLs are retained. Entries labelled required supplement/reference or fallback are explicit changes from the initial pack. Do not silently replace an input with a newer release.

### S1 — Agreed core input 1

```text
https://assets.publishing.service.gov.uk/media/6a82eee63bd75b81e2329a7b/Statutory_Homelessness_England_Time_Series_202603.ods
```

**Acquisition:** pending; no source bytes uploaded. Record actual version, coverage, schema and licence before approving use. Core source reference; actual file identity remains to be verified.

### S2 — Agreed core input 2

```text
https://assets.publishing.service.gov.uk/media/6a82eeb83bd75b81e2329a7a/Statutory_Homelessness_Detailed_Local_Authority_Data_202603.ods
```

**Acquisition:** pending; no source bytes uploaded. Record actual version, coverage, schema and licence before approving use. Core source reference; actual file identity remains to be verified.

## File validation and licence record

For every actually used input record:

`source_id, role_core_reference_fallback_extension, original_url, resolved_url, retrieved_utc, actual_release, filename, bytes, sha256, format, sheets_or_members, rows, geography, period_start, period_end, grain, schema_version, methodology_evidence, licence_notice, attribution, redistribution_conditions, approved_by, approval_date`

Retain the relevant publication/file notices, including exceptions and third-party conditions. Do not assume all publishers use the same licence. A stated publication licence does not remove the need to check file-specific terms. Keep unverified values pending; never invent a hash or approval.

## Support and freeze decision

Complete the [source-to-deliverable matrix](README.md). The domain specialist verifies actual grain, units, period comparability and supported metrics; the steward verifies identity and reuse terms. Required missing fields block dependent core outputs. Every activated extension is separately registered. Where a fallback is used, record why, which original it replaces, overlap handling and impact on outputs.

If an agreed URL fails, seek the same official archived release and record evidence. A browser format limitation does not prove a file is unavailable, and a successful page fetch does not prove payload integrity. Preserve the frozen version and metadata in the approved location so future website changes do not silently alter the cohort.
