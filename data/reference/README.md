# MTL-XF-022 — Reference data and mappings

## Purpose

Maintain the code lists and crosswalks needed to implement this analytical grain:

Maintain separate quarterly national/available-geography duty-flow facts and quarter-end LA temporary-accommodation stock facts; include table identifier, household category, duty and outcome dimensions. National trends do not create an LA historical panel.

Potential references are the publisher's geography/entity identifiers, category hierarchies, period definitions, units, status codes and revision markers. Include only references actually needed by the model. Register any separately downloaded official file as an additional source.

## Required mapping evidence

Each reference needs source/version, licence, valid-from/to dates, key uniqueness, allowed values, business meaning, owner and transformation use. For each crosswalk record source key, target key, relationship cardinality, rationale and treatment of unmapped or changed entities. Quantify 100% of unmatched keys; do not silently drop them or infer a mapping from similar names.

Avoid multiplying facts when a reference is many-to-many. Keep parent totals distinct from child categories. Non-official analyst-created groupings must be labelled as project assumptions and sensitivity-tested where they affect the investigation shortlist.

## Domain constraints

- Stock, new placements and duty flows describe different things and must not be summed.
- The core files do not automatically establish costs, length of stay or prevention effectiveness.
- Outcome shares are administrative indicators, not causal estimates or same-cohort conversion rates.

The domain specialist approves category meaning and comparability. The Data Engineer supplies uniqueness, join-cardinality and coverage checks before the reference enters the curated model.
