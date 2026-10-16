# MTL-XF-022 — Required deliverables

**Commissioned decision:** Where should the partnership investigate prevention practice, relief pathways or temporary-accommodation supply, given distinct measures of demand, outcomes and accommodation stock?

All locations below refer to the team's delivery repository. The master repository defines the requirements and contains no completed analysis. Owners are assigned from [the project roles](PROJECT_BRIEF.md).

## D1 — Discovery & decision requirements

**Due:** Week 1  
**Team artefact location:** `docs/01-discovery/`

Decision statement; stakeholder map; as-is reporting to investigation-review process; at least eight prioritised requirements. Answer these questions: Is national pressure rising because approaches/assessments, prevention duties or relief duties increased? Which authorities have high temporary-accommodation stock and family accommodation exposure in the agreed quarter? How do prevention and relief outcomes differ when each uses its own relevant denominator? Where do missing or non-comparable returns prevent a fair peer comparison? What cost, duration or casework evidence is still needed to diagnose local service pressure?

**Acceptance evidence:** All requirements have an owner, priority, deliverable and test ID; domain analyst approves scope.

## D2 — Governed sources & cohort

**Due:** Week 2  
**Team artefact location:** `docs/02-data-governance/; data/`

Use the agreed England time-series ODS and detailed LA January–March 2026 ODS. National trends use matching quarters available in the frozen time series; LA comparisons use January–March 2026 only. Earlier LA quarters are an extension requiring separately registered official files. Register exact files, metadata, licences, checksums, coverage and critical fields; record rejection of unavailable dimensions.

**Acceptance evidence:** 100% of inputs registered; no claimed freeze until acquisition evidence exists.

## D3 — Reproducible analytical model

**Due:** Week 3  
**Team artefact location:** `src/; sql/; docs/03-data-model/`

Maintain separate quarterly national/available-geography duty-flow facts and quarter-end LA temporary-accommodation stock facts; include table identifier, household category, duty and outcome dimensions. National trends do not create an LA historical panel. Deliver load, type checks, hierarchy handling, lineage, exclusions and environment instructions.

**Acceptance evidence:** A second member regenerates equivalent curated outputs from identical inputs; no unexplained duplicate analytical keys.

## D4 — Quality & reconciliation

**Due:** Week 3  
**Team artefact location:** `docs/04-data-quality/; tests/`

Profile missingness, suppression, valid values, keys and join coverage. Reconcile five national/LA published totals without double-counting table subtotals. Test that quarter-end stock cannot be added to quarterly duty flows. Test zero and missing duty-ended denominators. Verify the LA page is labelled January–March 2026 and has no fabricated historical trend.

**Acceptance evidence:** Every input row is accounted for as retained, excluded or quarantined; five published cells reconcile within declared rounding.

## D5 — KPI catalogue

**Due:** Week 4  
**Team artefact location:** `docs/05-kpi-catalogue/`

Define all 8 measures listed below with formula, grain, denominator, unit, source fields, exclusions, owner, refresh and limitations.

**Acceptance evidence:** 100% headline metrics trace to source fields and tested transformations; conditional unavailable measures are explicitly marked.

## D6 — Domain analytical assessment

**Due:** Week 5  
**Team artefact location:** `analysis/; docs/06-analysis/`

Build a national demand/outcome trend and a separate LA January–March 2026 peer view; do not infer local historical changes. Create an up-to-ten-authority investigation shortlist distinguishing prevention, relief and accommodation-stock signals.

**Acceptance evidence:** At least five evidence-backed findings state period, population, comparison, magnitude, uncertainty and limitation; negative findings count.

## D7 — Investigation decision framework

**Due:** Week 6  
**Team artefact location:** `docs/07-decision-framework/`

Compare raw-stock and outcome-share prioritisation, stratify by authority type if defensible, and state where population or housing-market context is missing. Record eligibility, thresholds, weights if used, reason codes and manual review triggers.

**Acceptance evidence:** Every shortlisted case has metrics, rationale, owner and evidence gaps; at least two scenarios compared; fewer than ten is valid where evidence is insufficient.

## D8 — BI decision-support product

**Due:** Draft Week 6; final Week 7  
**Team artefact location:** `dashboard/`

Executive overview answering 'Where should the partnership investigate prevention practice, relief pathways or temporary-accommodation supply, given distinct measures of demand, outcomes and accommodation stock?' plus diagnostic and data-quality views; visible periods, units, denominator notes, resettable filters and accessible labels.

**Acceptance evidence:** Five headline measures reconcile; every filter tested; export screenshots/PDF plus reproducible build or free access instructions.

## D9 — Independent assurance & UAT

**Due:** Week 7  
**Team artefact location:** `docs/08-assurance-uat/`

At least ten scenarios including the four project-specific tests below; requirement-to-test matrix, expected/actual evidence, defect log and simulated stakeholder feedback.

**Acceptance evidence:** No unresolved critical/high defect; accepted lower-severity limitations have a named reviewer and explicit impact.

## D10 — Technical & operational handover

**Due:** Week 8  
**Team artefact location:** `docs/09-technical-handover/`

Clean setup, architecture, frozen input manifest, run/refresh steps, output checks, troubleshooting and change-control process for Statutory Homelessness, Temporary Accommodation & Prevention Performance Intelligence.

**Acceptance evidence:** Another member reproduces the core outputs without undocumented edits and records environment, duration and discrepancies.

## D11 — Executive recommendation

**Due:** Week 8  
**Team artefact location:** `deliverables/`

Maximum two-page briefing and 15–20 minute presentation: commissioned decision, five findings, investigation shortlist, sensitivity, missing evidence, responsibilities and next review.

**Acceptance evidence:** Every quantitative claim links to an artefact/metric; no unsupported causal, policy or operational guarantee.

## D12 — Contribution & delivery record

**Due:** Weekly; final Week 8  
**Team artefact location:** `CONTRIBUTIONS.md; delivery issues/PRs`

Record who delivered and reviewed each MTL-XF-022 work package, including domain, governance, engineering, BI and assurance contributions.

**Acceptance evidence:** Every member links to substantive artefacts and review/presentation evidence; commit count alone is insufficient.

## Required KPI definitions

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

For every metric record business purpose, formula, source fields, grain, unit, numerator/denominator, exclusions, suppression, zero-base behaviour, owner, refresh and test evidence. Do not populate conditional metrics from invented fields.

## Mandatory domain scenarios

1. Reconcile five national/LA published totals without double-counting table subtotals.
2. Test that quarter-end stock cannot be added to quarterly duty flows.
3. Test zero and missing duty-ended denominators.
4. Verify the LA page is labelled January–March 2026 and has no fabricated historical trend.

## Review gates

Week 2: cohort and source approval. Week 4: model, DQ and metrics approval. Week 6: analytical and decision-framework review. Week 8: UAT, independent rerun and final panel review. Record reviewer, date, artefact version and decision at every gate.
