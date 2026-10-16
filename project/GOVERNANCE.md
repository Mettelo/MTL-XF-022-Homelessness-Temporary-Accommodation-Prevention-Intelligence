# MTL-XF-022 — Governance

## Engagement representation

This is a **simulated confidential-client engagement** using official public/open data. The client label is fictional and intentionally anonymous. Do not imply a real external Mettelo customer, employment by that client, privileged access or confidential source data. Public source statistics remain public; the engagement framing does not make them confidential.

Accurately describe verified Mettelo Project Studio participation and individual contribution. Do not claim real-client endorsement or production adoption.

## Accountability

The simulated sponsor/review panel owns scope and decision acceptance. The Business Analyst owns requirements and changes. The Data Governance Analyst owns source evidence, glossary, critical fields, licences and freeze records. The Data Engineer owns transformations and reproducibility. The BI Developer owns presentation and measure implementation. Domain specialists own interpretation; independent assurance owns test evidence. Assign named team owners at kickoff.

| Domain role | Required control |
| --- | --- |
| Housing Pathway Analyst | Validate duty/end-reason mappings and interpret prevention, relief and stock separately across all eight metrics. |
| Housing Finance Analyst | Produce an evidence-gap register for costs and length of stay; label every financial scenario as an assumption. |
| Housing Policy & Evaluation Analyst | Own the up-to-ten-authority investigation plan and compare at least two prioritisation scenarios. |

## Source and retention control

Use the agreed England time-series ODS and detailed LA January–March 2026 ODS. National trends use matching quarters available in the frozen time series; LA comparisons use January–March 2026 only. Earlier LA quarters are an extension requiring separately registered official files.

Before analysis, inspect each official source, record the actual version and coverage, document licence/attribution/redistribution terms and approve an immutable manifest. Source-register URLs are agreed references, not proof of successful acquisition. Do not invent a checksum, licence, retrieval date or schema. No raw data is uploaded in this master-pack build. Later redistribution requires the verified terms; where it is not permitted, retain provenance, checksums and authorised access instructions.

Preserve frozen inputs and metadata for reproducibility in the approved location. Never overwrite an approved snapshot. New versions require a new manifest, a change decision and an impact comparison. If a URL stops working, locate the same official archived release first and document resolution; do not silently switch cohorts.

## Analytical controls

**Required grain:** Maintain separate quarterly national/available-geography duty-flow facts and quarter-end LA temporary-accommodation stock facts; include table identifier, household category, duty and outcome dimensions. National trends do not create an LA historical panel.

- Stock, new placements and duty flows describe different things and must not be summed.
- The core files do not automatically establish costs, length of stay or prevention effectiveness.
- Outcome shares are administrative indicators, not causal estimates or same-cohort conversion rates.

Maintain field-level lineage, critical-data-element definitions, missing/suppression rules, denominator logic, hierarchy mappings, join cardinality and reconciliation evidence. Every adjustment or exclusion records affected rows/values and reason. All headline outputs must expose period, units, eligible coverage and limits.

## Decision/model governance

Compare raw-stock and outcome-share prioritisation, stratify by authority type if defensible, and state where population or housing-market context is missing.

Thresholds and weights are review hypotheses, not statutory standards unless explicitly supported by an official definition. Expose each component, compare at least two scenarios and retain manual-review triggers. Document evidence that would reverse or invalidate a recommendation. Optional forecasts/models require a baseline, time-appropriate holdout, leakage checks, uncertainty, error metrics, limitations and a named reviewer; core delivery must remain complete without them. Any generated text/code must be verified by the team.

## Repository and information controls

Use a Mettelo organisation team repository and individual member accounts. Never commit secrets, credentials, private correspondence or unnecessary personal details. Preserve source suppression; do not infer concealed identities. Check publication suitability of all screenshots and exports. Use issues, reviewed changes and a contribution log; make evidence accessible to the review panel without paid-only dependencies.

## Change and review record

Each change entry records date, requester, old/new requirement or source, reason, affected metrics/artefacts/tests, owner, reviewer and disposition. Review gates occur in Weeks 2, 4, 6 and 8. Keep a risk log with likelihood, impact, mitigation, owner and status. Only the review panel can accept final scope changes; no real regulatory or professional certification is implied.
