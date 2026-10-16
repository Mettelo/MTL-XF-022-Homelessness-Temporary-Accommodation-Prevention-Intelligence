# MTL-XF-022 — Project brief

This is a **simulated confidential-client engagement using official public/open data**. Client and stakeholder role labels describe a fictional engagement; do not claim a real external Mettelo customer, employment, endorsement or privileged data access. No raw data is uploaded by this specification update.

**Client:** Confidential Council Housing & Homelessness Partnership. **Decision owner:** Director of Housing & Homelessness. **Team:** 6–8. **Duration:** 8 weeks. **Review:** quarterly homelessness pathway and accommodation review.

## Business problem and commission

Housing Options and temporary-accommodation managers approach the same review with different measures: duties arising during a quarter, duties ending with an outcome and households accommodated at quarter end. Leadership cannot allocate investigation effort consistently when those measures are mixed or treated as a single pipeline of unique households. Local housing supply and case duration may matter, but their contribution cannot be established from headline counts alone.

> Where should the partnership investigate prevention practice, relief pathways or temporary-accommodation supply, given distinct measures of demand, outcomes and accommodation stock?

## Core deliverable boundary

England quarterly national trend plus a January–March 2026 LA diagnostic snapshot. Keep prevention duties, relief duties, duty-ending outcomes and quarter-end accommodation in separate facts. Use source-published household-normalised rates only if the workbook supplies their exact denominator; otherwise label comparisons as unadjusted.

**Optional / out of core:** LA longitudinal comparisons need additional official quarterly files. Costs, median stay, individual pathways and causal prevention effectiveness require additional evidence and are not core commitments. Published duration categories, if present, must not be converted into an invented mean stay.

File availability does not prove dimensional support. Before analytical build, the team completes the source→field→metric→deliverable matrix in [data guidance](../data/README.md). Missing mandatory support blocks the gate and requires an approved official replacement or scope decision.

## Analytical model

Maintain separate quarterly national/available-geography duty-flow facts and quarter-end LA temporary-accommodation stock facts; include table identifier, household category, duty and outcome dimensions. National trends do not create an LA historical panel.

The source contract above controls where a general grain description is conditional. Do not create dimensions absent from the approved input.

## Objectives

1. Every LA card is visibly dated January–March 2026 and separates stock from quarterly flows.
2. Every outcome percentage identifies both duty and duty-ended denominator.
3. Each shortlisted case selects either pathway, placement/supply or data-quality investigation with the responsible service role.

## Business questions

1. Is national pressure rising because approaches/assessments, prevention duties or relief duties increased?
2. Which authorities have high temporary-accommodation stock and family accommodation exposure in the agreed quarter?
3. How do prevention and relief outcomes differ when each uses its own relevant denominator?
4. Where do missing or non-comparable returns prevent a fair peer comparison?
5. What cost, duration or casework evidence is still needed to diagnose local service pressure?

## Cross-functional delivery model

| Delivery role | Required project contribution |
| --- | --- |
| Business Analyst / Delivery Lead | Map the quarterly homelessness pathway and accommodation review, document eight prioritised user requirements and maintain requirement→deliverable→test links; Director of Housing & Homelessness owns business approval. |
| Data Governance Analyst | Own the MTL-XF-022 source/metadata register, cohort decision, licence evidence and 100% headline-measure lineage; resolve the specific risk: Duty flows, ended-duty outcomes and quarter-end accommodation stocks have incompatible populations and reference dates. |
| Data Engineer | Implement the declared facts, keys, hierarchy and join controls; account for every source row and deliver a second-member reproducible run at the chosen MTL-XF-022 scope. |
| BI Developer | Implement the quarterly homelessness pathway and accommodation review overview, diagnostic and quality pages; reconcile five measures and ensure cohort/extension warnings survive filters and export. |
| Housing Pathway Analyst | Validate duty/end-reason mappings and interpret prevention, relief and stock separately across all eight metrics. |
| Housing Finance Analyst | Produce an evidence-gap register for costs and length of stay; label every financial scenario as an assumption. |
| Housing Policy & Evaluation Analyst | Own the up-to-ten-authority investigation plan and compare at least two prioritisation scenarios. |

Assign named team members and review partners at kickoff; roles may be combined, but a distinct member must review critical calculations and perform the final clean rerun. The executive and operational stakeholder roles are specified in [business context](BUSINESS_CONTEXT.md).

## Required investigation approach

Compare two investigation views: accommodation-stock burden and prevention/relief accommodation-outcome shares using valid duty-ended denominators. Show reporting completeness and peer context before ordering. Produce separate stock-pressure and pathway-review queues rather than combining incompatible units into an unexplained score.

## Milestones and acceptance

| Gate | Reviewers | Evidence / decision |
| --- | --- | --- |
| G1 — scope/source, end Week 2 | Business Analyst + Data Governance Analyst + domain specialist | Approve actual period, geography, grain, required input and field support in a source-to-deliverable matrix. Publication and workbook listings verified; internal sheet/field mappings, outcome categories, licences and frozen file identity pending. Unsupported mandatory outputs remain blocked, not quietly reclassified as completed. |
| G2 — model/metrics, end Week 4 | Data Engineer + domain specialist + independent reviewer | Approve row accounting, keys, hierarchy, join cardinality, five source reconciliations and all core metric definitions. |
| G3 — analytical decision review, end Week 6 | Director of Housing & Homelessness + operational stakeholders | Compare two investigation views: accommodation-stock burden and prevention/relief accommodation-outcome shares using valid duty-ended denominators. Show reporting completeness and peer context before ordering. Produce separate stock-pressure and pathway-review queues rather than combining incompatible units into an unexplained score. Retain an evidence-insufficient case and a manual review route. |
| G4 — release, end Week 8 | Simulated Mettelo panel + independent reviewer | Accept D1–D12 only after ten executed domain tests, five BI reconciliations, clean rerun evidence and resolution of all critical/high defects. |

D1–D12 are defined in [deliverables](DELIVERABLES.md). AC1–AC12 and DT1–DT10 are defined in [acceptance criteria](ACCEPTANCE_CRITERIA.md). No real production deployment, automatic funding/service allocation, private-client data or paid-source dependency is required.
