# MTL-XF-022 — Acceptance criteria and domain tests

**Business decision owner:** Director of Housing & Homelessness. **Decision:** Where should the partnership investigate prevention practice, relief pathways or temporary-accommodation supply, given distinct measures of demand, outcomes and accommodation stock?

## Delivery sign-off

| ID | Deliverables | Required pass evidence | Acceptance owner |
| --- | --- | --- | --- |
| AC1 | D1 | Eight user requirements cover the commissioned questions, named stakeholder actions and core/extension boundary. | Business Analyst / Director of Housing & Homelessness |
| AC2 | D2 | 100% of used source files have approved provenance, version/coverage, licence, retrieval UTC and SHA-256. Required fields and reference versions are checked. | Data Governance Analyst |
| AC3 | D3 | Every input row is accounted for; keys and all many-to-many/hierarchy effects have explicit checks and no unexplained duplication. | Data Engineer / independent reviewer |
| AC4 | D4 | Five source cells reconcile within a declared rounding tolerance; all material differences and non-additive totals are explained. | Domain specialist |
| AC5 | D5 | All 8 metric contracts are classified core/conditional and have tested definitions; no unsupported fields or fabricated unavailable values. | Data Governance Analyst / BI Developer |
| AC6 | D6 | Five findings cover all business questions or evidence gaps; period, eligible population, magnitude, comparison and limitation are visible. | Domain analyst |
| AC7 | D7 | The project-specific baseline and alternative below are implemented; eligibility, scenario changes, reason codes and evidence requests are visible. | Director of Housing & Homelessness |
| AC8 | D8 | Five BI measures reconcile to curated outputs; all filters/reset/export retain the scope, units and limitations. | BI Developer / operational UAT user |
| AC9 | D9 | DT1–DT10 have actual execution evidence and expected/actual outcomes; no unresolved critical/high defect. | Independent reviewer |
| AC10 | D10 | A distinct member's clean rerun reproduces equivalent core outputs with documented environment and checks. | Independent rerun reviewer |
| AC11 | D11 | Two-page maximum briefing and 15–20 minute presentation answer the decision and assign investigation owners without unsupported outcomes. | Director of Housing & Homelessness / Mettelo panel |
| AC12 | D12 | Every member links substantive authored and reviewed work, including handover or presentation contribution. | Delivery Lead |

## Project-specific business success

1. Every LA card is visibly dated January–March 2026 and separates stock from quarterly flows.
2. Every outcome percentage identifies both duty and duty-ended denominator.
3. Each shortlisted case selects either pathway, placement/supply or data-quality investigation with the responsible service role.

## Required prioritisation and sensitivity

Compare two investigation views: accommodation-stock burden and prevention/relief accommodation-outcome shares using valid duty-ended denominators. Show reporting completeness and peer context before ordering. Produce separate stock-pressure and pathway-review queues rather than combining incompatible units into an unexplained score.

Record each case's entity/segment, valid period, supporting measures, reason code, scenario position, missing evidence, responsible operational role, next review and manual-review trigger. Fewer than ten cases is valid; padding unsupported cases fails acceptance.

## DT1–DT10 — minimum executed domain tests

| Test | Input / action | Expected pass evidence |
| --- | --- | --- |
| DT1 | Reconcile five national/LA published totals without double-counting table subtotals. | Five selected published values reproduce within declared source precision, with explicit source coordinates and scope. |
| DT2 | Test that quarter-end stock cannot be added to quarterly duty flows. | The invalid comparison, join or denominator is rejected or flagged according to the documented rule; no silent fallback. |
| DT3 | Test zero and missing duty-ended denominators. | The edge case produces an explicit unavailable/exclusion result or a supported calculation, with affected rows quantified. |
| DT4 | Verify the LA page is labelled January–March 2026 and has no fabricated historical trend. | The domain boundary remains visible in the analytical output and BI product; no unsupported inference. |
| DT5 | 80 prevention duties end; 48 end with secured accommodation | Outcome share = 60%; do not divide by duties newly owed. |
| DT6 | 200 households in TA and 50 new duty cases | Do not report 250 unique homeless households. |
| DT7 | LA has a missing return in the target table | Show missing coverage; exclude from performance ordering. |
| DT8 | Two LA categories overlap or include a total row | Select one valid level; do not add aggregate and component values. |
| DT9 | No LA data for an earlier quarter in the approved inputs | No local trend is drawn; national context remains separately labelled. |
| DT10 | A case has stock pressure but no cost data | Recommendation requests placement/cost evidence; no expenditure saving is stated. |

Worked values are **synthetic test fixtures**, not claims about the public data or simulated client. For each test retain requirement ID, source/input or fixture, expected result, actual result, evidence link, tester, independent reviewer and date. DT1–DT4 additionally require the documented project-specific rule; their general evidence descriptions do not waive the named domain condition. Add dashboard/filter tests as needed beyond these ten.

## Scope gate and unresolved issues

**Mandatory core:** England quarterly national trend plus a January–March 2026 LA diagnostic snapshot. Keep prevention duties, relief duties, duty-ending outcomes and quarter-end accommodation in separate facts. Use source-published household-normalised rates only if the workbook supplies their exact denominator; otherwise label comparisons as unadjusted.

**Optional extensions:** LA longitudinal comparisons need additional official quarterly files. Costs, median stay, individual pathways and causal prevention effectiveness require additional evidence and are not core commitments. Published duration categories, if present, must not be converted into an invented mean stay.

A mandatory source/field gap blocks the affected deliverable and must be resolved by a registered official replacement or approved, versioned scope change. An explicitly optional result may be unavailable with a reason and a useful evidence request. Neither missing raw data nor unexecuted tests may be marked passed.

A critical/high defect materially changes a headline value, cohort, recommendation, provenance or reproducibility and blocks release. Lower-impact issues require a named acceptance owner and disclosed impact. All panel feedback and approvals must be recorded honestly as simulated where applicable.
