# MTL-XF-022 — Project brief

## Engagement

This is a **simulated confidential-client engagement** using official public/open data. The client label is fictional and intentionally anonymous. Do not imply a real external Mettelo customer, employment by that client, privileged access or confidential source data. Public source statistics remain public; the engagement framing does not make them confidential.

**Simulated sponsor:** Confidential Council Housing & Homelessness Partnership. **Duration:** 8 weeks. **Team:** 6–8 members. **Track:** Cross-Functional. **Sector:** Housing / Local Government.

## Commission

Where should the partnership investigate prevention practice, relief pathways or temporary-accommodation supply, given distinct measures of demand, outcomes and accommodation stock?

**Statutory Homelessness, Temporary Accommodation & Prevention Performance Intelligence.** A council partnership is facing rising temporary-accommodation pressure but cannot clearly distinguish demand growth, weak prevention outcomes, relief-duty pressure and long stays. The project will support housing-service redesign and prevention planning.

## Outcomes and boundaries

- Build a national demand/outcome trend and a separate LA January–March 2026 peer view; do not infer local historical changes.
- Create an up-to-ten-authority investigation shortlist distinguishing prevention, relief and accommodation-stock signals.
- Compare raw-stock and outcome-share prioritisation, stratify by authority type if defensible, and state where population or housing-market context is missing.

Deliver evidence for a management investigation decision, with an auditable shortlist of up to ten cases and at least two alternative prioritisation scenarios. Do not manufacture a full shortlist where the data supports fewer cases. Findings may conclude that evidence is insufficient.

**Data boundary:** Use the agreed England time-series ODS and detailed LA January–March 2026 ODS. National trends use matching quarters available in the frozen time series; LA comparisons use January–March 2026 only. Earlier LA quarters are an extension requiring separately registered official files.

**Model boundary:** Maintain separate quarterly national/available-geography duty-flow facts and quarter-end LA temporary-accommodation stock facts; include table identifier, household category, duty and outcome dimensions. National trends do not create an LA historical panel.

**Out of scope:** real operational deployment, confidential case-level data, guaranteed savings/outcome improvements, paid-source dependencies and automatic allocation of services or funding. Optional modelling or enriched sources must not delay or replace the core D1–D12 pack.

## Users and acceptance owners

- Simulated sponsor/review panel: approves commissioned question, changes and final investigation recommendation.
- Domain service/planning user: checks whether diagnostic evidence supports the proposed review action.
- Data steward: verifies source/version, licence, definitions, quality and retention evidence.
- BI user: tests overview, drill-down, filters and limitations.
- Independent reviewer: verifies calculations, rerun and requirement-to-test traceability.

These are simulated stakeholder roles, not claims of access to a real organisation.

## Work allocation

| Accountable role | Project responsibility and evidence |
| --- | --- |
| Business Analyst / Delivery Lead | Own the commissioned decision for Confidential Council Housing & Homelessness Partnership; record at least eight prioritised requirements, each linked to a deliverable and test; maintain weekly scope and decision logs. |
| Data Governance Analyst | Register every 022 input and critical field; approve the frozen cohort, licence evidence, glossary and 100% headline-KPI lineage before analysis. |
| Data Engineer | Implement the stated 022 analytical grain, ingestion and exclusions; deliver a clean rerun with row-count/checksum evidence and no unexplained key duplicates. |
| BI Developer | Build executive, diagnostic and quality views for the commissioned decision; reconcile at least five 022 dashboard measures and test every visible filter. |
| Housing Pathway Analyst | Validate duty/end-reason mappings and interpret prevention, relief and stock separately across all eight metrics. |
| Housing Finance Analyst | Produce an evidence-gap register for costs and length of stay; label every financial scenario as an assumption. |
| Housing Policy & Evaluation Analyst | Own the up-to-ten-authority investigation plan and compare at least two prioritisation scenarios. |

At kickoff, replace role ownership with named team members and record review partners in `CONTRIBUTIONS.md`. Multiple roles per member are permitted, but critical calculations need a reviewer distinct from their author.

## Working stages

1. Week 1: agree at least eight requirements and define expected decisions.
2. Week 2: inspect actual file schemas, establish available coverage and approve cohort freeze.
3. Week 3: implement and reconcile analytical facts, keys and exclusions.
4. Week 4: approve the 8-measure KPI catalogue and denominator rules.
5. Week 5: complete five supported findings and domain comparisons.
6. Week 6: compare two decision scenarios, produce the investigation shortlist and BI draft.
7. Week 7: execute ten or more assurance/UAT scenarios, including project-specific edge cases.
8. Week 8: independent rerun, executive briefing, presentation and final handover.

## Sign-off

Follow [D1–D12](DELIVERABLES.md) and [AC1–AC12](ACCEPTANCE_CRITERIA.md). Approve only with reproducible evidence, no unresolved critical/high defects and transparent conditional-data limitations. A change in source availability must be logged; do not silently substitute a newer release.
