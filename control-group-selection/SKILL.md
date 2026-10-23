---
name: control-group-selection
description: Select and assess comparison groups for observational causal studies of policies, programs, and business interventions. Evaluate exposure, contextual comparability, pretreatment data, and concurrent shocks for DID, DDD, event studies, matching, weighting, and synthetic controls.
---

# Control group selection

Build a defensible counterfactual for the user's causal question using four layers: treatment eligibility, contextual comparability, pretreatment outcomes and unit characteristics, and concurrent shocks. Adapt measures to the domain and observation unit. Do not select controls using favorable post-treatment estimates or significance.

## Define the comparison and design

Read study notes, data documentation, and code. Identify the estimand, target population, intervention, assignment and observation units, exposure mechanism, announcement and implementation dates, anticipation, outcomes, and window. Distinguish assignment from receipt, direct from spillover effects, and individual from aggregate effects. State unresolved assumptions.

Match evidence to the design:

- DID and event studies require credible untreated outcome changes under the relevant parallel-trends assumption; similar levels alone are insufficient.
- DDD requires a credible counterfactual for the difference between subgroup gaps across treatment groups and time.
- Matching and weighting under selection on observables require sufficient pretreatment confounder information, overlap, and conditional exchangeability. Balance cannot establish absence of unmeasured confounding.
- Synthetic control requires eligible donors, informative pretreatment history, adequate fit, and a defensible model for untreated outcomes. Fit alone does not establish identification.

If assignment follows a threshold, lottery, instrument, or other specific mechanism, consider whether that mechanism offers a better comparison than generic matching. Respect its design-specific requirements.

## 1. Treatment eligibility and exposure

Verify what changed, for whom, where, and when, including rollout and compliance. Prefer dated official records and contemporaneous evidence; current rules or interfaces cannot establish historical exposure.

Build a group-by-intervention timeline including competing treatments, organizational changes, eligibility changes, and other plausible confounders. Classify candidates as eligible, excluded, or unresolved with reasons and sources. For untreated comparisons, verify absence of treatment throughout the comparison window. Later-treated groups can contribute before treatment and relevant anticipation with an appropriate estimator; do not use already-treated units as untreated controls by default.

Assess interference through geography, networks, competition, displacement, shared organizations, and system-wide responses. A nominally untreated unit may experience spillovers. Explain how the exposure definition and estimand address contamination.

For DDD or active-comparator designs, establish the intended exposure contrast rather than requiring every comparator to receive no intervention. Verify treatment versions and the identifying assumption for that contrast.

## 2. Contextual and market comparability

Use pretreatment information for the actual populations and environments represented in the data. Keep geographic, organizational, and individual comparison units distinct. Do not substitute aggregate proxies without explaining their limitations.

Choose relevant dimensions rather than requiring every measure in every study:

| Dimension | Examples |
| --- | --- |
| Geography and operating environment | Population, density, urban/rural setting, climate, seasonality, commuting, institutional setting, jurisdiction, organizational scale |
| Overall activity or consumption | Household expenditure, total consumer spending, employment, production, or service use relevant to untreated outcomes |
| Domain-specific activity | Food spending and food-at-home/away-from-home shares in food studies; analogous demand, utilization, or participation in other sectors |
| Resources and socioeconomic conditions | Income distribution, purchasing power, poverty, employment, education, organizational resources, relevant prices |
| Treatment-related infrastructure and exposure | Platform penetration, technology access, provider networks, program availability, baseline participation, regulation, exposure intensity |
| Institutions and composition | Governance, baseline rules, industry structure, demographics, population needs, access constraints |

Separate overall from sector-specific consumption when both matter. Distinguish expenditures from quantities and visits, nominal from real measures, and totals from rates. Align dates, definitions, denominators, and coverage; label unavailable measures and proxies.

Select variables through a substantive account of treatment selection and untreated outcome evolution. Avoid indiscriminate matching, arbitrary composite scores, colliders, and treatment consequences. Explain which contextual differences threaten identification. Contextual similarity cannot repair contamination.

## 3. Pretreatment outcomes and unit-level information

Evaluate the actual estimation sample. Adapt unit characteristics: restaurant category and chain status, firm size and industry, patient baseline health, student prior attainment, household composition, or regional economic structure. Use information observed before treatment and relevant anticipation.

- Audit outcome definitions, source coverage, measurement consistency, missingness, entry/exit, reporting changes, and composition. Investigate selection and survivorship artifacts.
- With longitudinal data, examine levels, changes, seasonality, and treated-control gaps across multiple pretreatment periods. Without outcome histories, explain which diagnostics are unavailable and which assumptions carry identification.
- Use design-appropriate matching, weighting, stratification, or donor construction. Avoid conditioning on treatment-induced participation, spending, survival, or mediators. Explain the target population after trimming or weighting.
- Use a documented, coherent selection rule across main outcomes. Do not choose a favorable comparator for each outcome; justify any outcome-specific population substantively.
- When history permits, construct weights on earlier pretreatment periods and validate on held-out later periods outside anticipation. Specify the split before examining treatment effects. Do not force a split with inadequate history or claim it eliminates confounding.
- Report relevant balance, overlap, outcome fit, weight concentration, effective sample size, and donor/group contributions. Define metrics and substantive decision criteria before using them to rank candidates.
- For trend-based designs, assess economically meaningful departures, confidence intervals, and event-study leads. Failure to reject pretrends does not prove parallel trends. Selecting controls solely by passing such tests can distort inference; fitted pretreatment similarity is not independent validation.

## 4. Concurrent shocks and COVID conditions

Identify shocks that could differentially affect groups: recessions, disasters, strikes, supply disruptions, elections, reforms, or public-health emergencies. Compare timing, intensity, responses, and plausible outcome pathways. Post-treatment context may diagnose competing explanations; do not tune weights to reproduce post-treatment outcomes.

When the window overlaps COVID-19:

- Compare epidemic waves, population-adjusted cases, hospitalizations/deaths where comparable, vaccination, and testing/reporting differences. Explain denominators, revisions, missingness, and geographic proxies.
- Document relevant closures, capacity limits, remote-work or school rules, travel restrictions, reopening dates, and other outcome-related restrictions.
- Examine mobility, labor supply, service availability, and recovery in overall and domain-specific consumption/activity. Distinguish mandated restrictions from voluntary behavior and actual recovery.
- Provide a dated treated-versus-candidate comparison covering pre- and post-treatment periods. Common national waves do not establish comparable local conditions.
- Consider justified covariates and lags, alternative windows, or excluding differential shocks as sensitivity checks. Explain whether adjustment variables could be treatment consequences. Adding COVID controls does not automatically repair identification.

State when COVID is inapplicable. For other shocks, use analogous evidence relevant to their mechanisms rather than imposing pandemic-specific measures.

## Choose and report the design

Separate hard exclusions from degrees of comparability. Recommend individual, pooled, or weighted controls according to evidence; pooling is not automatically superior. If no credible comparison exists, explain why and suggest a narrower estimand, different window, additional data, or alternative identification strategy.

Assess treated groups separately when contexts or effects differ materially and explain aggregation weights. Use individual-control, leave-one-group-out, alternative-window, or alternative-exposure checks where meaningful. For DDD, consider context-by-time fixed effects for common shocks and state the remaining differential-trend assumption. Consider sensitivity to plausible parallel-trend violations when warranted.

Match inference to assignment and dependence. Many observations in a few treated clusters do not create many independent assignments. Explain small-cluster limitations and justify assumptions for placebo, randomization, or resampling procedures rather than treating them as automatic remedies.

Deliver a concise recommendation supported by:

1. The estimand, treatment, timing, units, and design-specific assumptions.
2. A candidate table covering eligibility, contextual comparability, pretreatment evidence, shocks, and include/exclude/unresolved decisions.
3. A reproducible selection or weighting rule, overlap limitations, validation actually performed, and implied target population.
4. Remaining identification threats, sensitivity checks, and suitable inference.
5. Sources and data definitions separating verified facts, assumptions, proxies, and missing evidence.

Use local/connected evidence and authoritative historical sources; verify external claims when needed. Never fabricate exposure histories, covariates, diagnostics, or causal certainty. Without data, provide a selection protocol and provisional judgments. Preserve the user's scope: a design review does not authorize editing datasets or analysis code.
