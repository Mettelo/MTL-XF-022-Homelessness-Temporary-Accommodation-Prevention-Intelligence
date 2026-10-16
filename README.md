# MTL-XF-022 — Statutory Homelessness, Temporary Accommodation & Prevention Performance Intelligence

**Mettelo Project Studio** · Cross-Functional · Master specification  
**Client:** Confidential Council Housing & Homelessness Partnership  
**Sector:** Housing / Local Government  
**Status:** Pre-launch; documentation ready, data acquisition/freeze pending  
**Recommended team:** 6–8 people · **Delivery window:** 8 weeks  
**Master repository:** `Mettelo/MTL-XF-022-Homelessness-Temporary-Accommodation-Prevention-Intelligence`

> This is a **simulated confidential-client engagement** using official public/open data. The client label is fictional and intentionally anonymous. Do not imply a real external Mettelo customer, employment by that client, privileged access or confidential source data. Public source statistics remain public; the engagement framing does not make them confidential.

## Business challenge

**Statutory Homelessness, Temporary Accommodation & Prevention Performance Intelligence.** A council partnership is facing rising temporary-accommodation pressure but cannot clearly distinguish demand growth, weak prevention outcomes, relief-duty pressure and long stays. The project will support housing-service redesign and prevention planning.

Current reporting fragments the evidence needed for a repeatable management review. The team must explain which signals are reliable, which comparisons are valid and where further investigation is needed. No budget, operational failure or improvement outcome is asserted as an observed client fact.

## Commissioned decision

> Where should the partnership investigate prevention practice, relief pathways or temporary-accommodation supply, given distinct measures of demand, outcomes and accommodation stock?

The product supports a simulated stakeholder review. A dashboard alone is insufficient: the recommendation must be traceable to governed definitions, a reproducible model, reconciled analysis and a transparent investigation framework.

## Business questions

- Is national pressure rising because approaches/assessments, prevention duties or relief duties increased?
- Which authorities have high temporary-accommodation stock and family accommodation exposure in the agreed quarter?
- How do prevention and relief outcomes differ when each uses its own relevant denominator?
- Where do missing or non-comparable returns prevent a fair peer comparison?
- What cost, duration or casework evidence is still needed to diagnose local service pressure?

## Approved data and cohort

MHCLG Statutory Homelessness — England time series + detailed LA Jan–Mar 2026. Historical releases are maintained over many years.

Use the agreed England time-series ODS and detailed LA January–March 2026 ODS. National trends use matching quarters available in the frozen time series; LA comparisons use January–March 2026 only. Earlier LA quarters are an extension requiring separately registered official files.

Exact copyable URLs and acquisition gates are in [SOURCE_REGISTER.md](data/SOURCE_REGISTER.md). No raw data is uploaded by this build. Source coverage and size statements inherited from the agreement are expected values until controlled acquisition verifies them; current URLs are not a substitute for a frozen file manifest.

## What the team must build

1. Build a national demand/outcome trend and a separate LA January–March 2026 peer view; do not infer local historical changes.
2. Create an up-to-ten-authority investigation shortlist distinguishing prevention, relief and accommodation-stock signals.
3. Compare raw-stock and outcome-share prioritisation, stratify by authority type if defensible, and state where population or housing-market context is missing.

Produce the full D1–D12 delivery pack: discovery, governance, ingestion/model, quality, KPI catalogue, analysis, decision framework, BI, assurance/UAT, handover, executive briefing and contribution record. [Deliverables](project/DELIVERABLES.md) defines locations, dates and evidence for each.

## Core measures

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

## Cross-functional ownership

| Accountable role | Project responsibility and evidence |
| --- | --- |
| Business Analyst / Delivery Lead | Own the commissioned decision for Confidential Council Housing & Homelessness Partnership; record at least eight prioritised requirements, each linked to a deliverable and test; maintain weekly scope and decision logs. |
| Data Governance Analyst | Register every 022 input and critical field; approve the frozen cohort, licence evidence, glossary and 100% headline-KPI lineage before analysis. |
| Data Engineer | Implement the stated 022 analytical grain, ingestion and exclusions; deliver a clean rerun with row-count/checksum evidence and no unexplained key duplicates. |
| BI Developer | Build executive, diagnostic and quality views for the commissioned decision; reconcile at least five 022 dashboard measures and test every visible filter. |
| Housing Pathway Analyst | Validate duty/end-reason mappings and interpret prevention, relief and stock separately across all eight metrics. |
| Housing Finance Analyst | Produce an evidence-gap register for costs and length of stay; label every financial scenario as an assumption. |
| Housing Policy & Evaluation Analyst | Own the up-to-ten-authority investigation plan and compare at least two prioritisation scenarios. |

Roles may be combined by a smaller team, but each responsibility needs a named owner. A different member reviews critical calculations and final evidence wherever practical.

## Interpretation rules

- Stock, new placements and duty flows describe different things and must not be summed.
- The core files do not automatically establish costs, length of stay or prevention effectiveness.
- Outcome shares are administrative indicators, not causal estimates or same-cohort conversion rates.

## Measurable success

- All source files and transformations have provenance and licence evidence; approved inputs have SHA-256 manifests.
- All headline metrics have tested definitions and source-field lineage.
- At least five published values and five dashboard measures reconcile with declared source rounding.
- At least five findings address the business questions and quantify materiality.
- Up to ten investigation cases have evidence, reason codes, owners and limitations; at least two priority scenarios are compared.
- At least ten UAT scenarios pass or have explicitly accepted low-impact limitations; no critical/high defect remains.
- A second member reproduces the core outputs from the same frozen inputs.

These are delivery acceptance thresholds, not promises of real-world service improvement. See [acceptance criteria](project/ACCEPTANCE_CRITERIA.md).

## Delivery sequence

Weeks 1–2: decision requirements, source inspection and freeze approval. Weeks 3–4: model, reconciliation and KPI definitions. Weeks 5–6: analysis, investigation framework and BI draft. Weeks 7–8: UAT, independent rerun, briefing and handover.

## Start here

1. Read the [project brief](project/PROJECT_BRIEF.md) and [business context](project/BUSINESS_CONTEXT.md).
2. Review [deliverables](project/DELIVERABLES.md), [acceptance criteria](project/ACCEPTANCE_CRITERIA.md) and [governance](project/GOVERNANCE.md).
3. Inspect the [data workspace](data/README.md), [source register](data/SOURCE_REGISTER.md), [raw guidance](data/raw/README.md), [reference guidance](data/reference/README.md) and [metadata guidance](data/metadata/README.md).
4. Create `MTL-XF-022-<team-name>` under the **Mettelo GitHub organisation**, add each member's individual account and follow the [team repository standard](submission/TEAM_REPOSITORY_STANDARD.md).
5. Use the [submission guide](submission/SUBMISSION_GUIDE.md) and [final submission template](submission/FINAL_SUBMISSION_TEMPLATE.md).

## Master and team repositories

This master holds the challenge specification. Teams deliver their analysis and artefacts in their own Mettelo organisation repository. Do not submit team work by replacing this master specification. Use issues, branches, meaningful commits, PRs and reviews to demonstrate actual collaboration.

## Specification map

```text
README.md
project/README.md
project/PROJECT_BRIEF.md
project/BUSINESS_CONTEXT.md
project/DELIVERABLES.md
project/ACCEPTANCE_CRITERIA.md
project/GOVERNANCE.md
data/README.md
data/SOURCE_REGISTER.md
data/raw/README.md
data/reference/README.md
data/metadata/README.md
submission/README.md
submission/TEAM_REPOSITORY_STANDARD.md
submission/SUBMISSION_GUIDE.md
submission/FINAL_SUBMISSION_TEMPLATE.md
```

**Mettelo — Built for What’s Next**
