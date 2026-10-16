# MTL-XF-022 — Statutory Homelessness, Temporary Accommodation & Prevention Performance Intelligence

**Mettelo Project Studio** · Cross-Functional · Master project specification  
**Client:** Confidential Council Housing & Homelessness Partnership  
**Accountable simulated executive:** Director of Housing & Homelessness  
**Sector:** Housing / Local Government  
**Team:** 6–8 people · **Window:** 8 weeks  
**Status:** documentation revised; file acquisition and cohort freeze pending  
**Review cadence:** quarterly homelessness pathway and accommodation review

> This is a **simulated confidential-client engagement using official public/open data**. Client and stakeholder role labels describe a fictional engagement; do not claim a real external Mettelo customer, employment, endorsement or privileged data access. No raw data is uploaded by this specification update.

## Business problem

Housing Options and temporary-accommodation managers approach the same review with different measures: duties arising during a quarter, duties ending with an outcome and households accommodated at quarter end. Leadership cannot allocate investigation effort consistently when those measures are mixed or treated as a single pipeline of unique households. Local housing supply and case duration may matter, but their contribution cannot be established from headline counts alone.

## Commissioned decision

> Where should the partnership investigate prevention practice, relief pathways or temporary-accommodation supply, given distinct measures of demand, outcomes and accommodation stock?

## Practical use

The Director reviews the England demand trend, then switches to the January–March 2026 authority comparison. One authority may have a large accommodation stock while another has a weaker secured-accommodation outcome share. The first triggers a placement/supply evidence request; the second triggers a prevention-pathway review. Neither is automatically labelled ineffective, expensive or slow without supporting casework evidence.

The full [business context](project/BUSINESS_CONTEXT.md) names operational stakeholders, decisions, risks and proposed benefit measures.

## What must be delivered

1. Build a national demand/outcome trend and a separate LA January–March 2026 peer view; do not infer local historical changes.
2. Create an up-to-ten-authority investigation shortlist distinguishing prevention, relief and accommodation-stock signals.
3. Compare raw-stock and outcome-share prioritisation, stratify by authority type if defensible, and state where population or housing-market context is missing.

The complete D1–D12 pack includes discovery, source governance, ingestion/model, quality, metric catalogue, analysis, investigation scenarios, BI, assurance/UAT, independent handover, executive briefing and contribution evidence. A dashboard by itself does not satisfy the commission.

## Fixed core and optional work

**Core:** England quarterly national trend plus a January–March 2026 LA diagnostic snapshot. Keep prevention duties, relief duties, duty-ending outcomes and quarter-end accommodation in separate facts. Use source-published household-normalised rates only if the workbook supplies their exact denominator; otherwise label comparisons as unadjusted.

**Extensions:** LA longitudinal comparisons need additional official quarterly files. Costs, median stay, individual pathways and causal prevention effectiveness require additional evidence and are not core commitments. Published duration categories, if present, must not be converted into an invented mean stay.

Source support is checked at the Week 2 gate. A required output is blocked until its fields and cohort are verified; it cannot pass acceptance through a generic “data unavailable” disclaimer. An explicitly optional extension may remain unavailable with a reason. See [exact source URLs and verification evidence](data/SOURCE_REGISTER.md).

## Measurable project outcomes

1. Every LA card is visibly dated January–March 2026 and separates stock from quarterly flows.
2. Every outcome percentage identifies both duty and duty-ended denominator.
3. Each shortlisted case selects either pathway, placement/supply or data-quality investigation with the responsible service role.

All headline metrics require field lineage; five source values and five BI measures must reconcile. DT1–DT10 must be executed, a second member must reproduce the core outputs, and no critical/high defect may remain. These assess delivery quality; real-world savings or service improvement are not claimed.

## Investigation rules

Compare two investigation views: accommodation-stock burden and prevention/relief accommodation-outcome shares using valid duty-ended denominators. Show reporting completeness and peer context before ordering. Produce separate stock-pressure and pathway-review queues rather than combining incompatible units into an unexplained score.

- Stock, new placements and duty flows describe different things and must not be summed.
- The core files do not automatically establish costs, length of stay or prevention effectiveness.
- Outcome shares are administrative indicators, not causal estimates or same-cohort conversion rates.

## Team and stakeholder ownership

Director of Housing & Homelessness approves business scope and the investigation recommendation. The Business Analyst, Data Governance Analyst, Data Engineer and BI Developer work with the specialist roles in the [project brief](project/PROJECT_BRIEF.md). Assign individual owners at kickoff and record substantive work and independent reviews in `CONTRIBUTIONS.md`.

## Delivery plan

Weeks 1–2: decision requirements and verified cohort. Weeks 3–4: model, reconciliation and metric definitions. Weeks 5–6: analytical findings, alternative investigation scenarios and BI draft. Weeks 7–8: simulated UAT, independent rerun, executive briefing and handover.

## Start here

1. [Project brief](project/PROJECT_BRIEF.md) and [business context](project/BUSINESS_CONTEXT.md).
2. [D1–D12 deliverables and metric contracts](project/DELIVERABLES.md).
3. [AC1–AC12 and DT1–DT10 acceptance tests](project/ACCEPTANCE_CRITERIA.md).
4. [Governance and sign-off](project/GOVERNANCE.md).
5. [Data workspace](data/README.md), [source register](data/SOURCE_REGISTER.md), [raw](data/raw/README.md), [reference](data/reference/README.md) and [metadata](data/metadata/README.md) guidance.
6. [Team repository standard](submission/TEAM_REPOSITORY_STANDARD.md), [submission guide](submission/SUBMISSION_GUIDE.md) and [final template](submission/FINAL_SUBMISSION_TEMPLATE.md).

## Master and team repositories

This master repository holds the Mettelo-controlled specification. Create `MTL-XF-022-<team-name>` under the **Mettelo GitHub organisation** and add every member's individual account. Delivery analysis, code, tests, BI and contribution evidence belong in that team repository. Use issues, branches, meaningful commits, PRs and reviews where practical.

The required master areas are `project/`, `data/` (including raw/reference/metadata guidance) and `submission/`; [the documentation index](project/README.md) explains their authority and current revision.

**Mettelo — Built for What’s Next**
