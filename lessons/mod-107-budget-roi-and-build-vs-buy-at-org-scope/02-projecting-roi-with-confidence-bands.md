# Projecting ROI with Confidence Bands

> [mod-106 Chapter 05](../mod-106-outcome-measurement-and-executive-reporting/05-partnering-with-finance-on-cost-model-and-roi.md) treated *trailing* ROI — what the program has already produced — on the scorecard cadence. This chapter treats *projected* ROI on priority use cases: the number that lands in the annual budget ask, in a build-vs-buy case, and in a tool-stack-consolidation proposal. Projection is harder than trailing measurement because every term carries its own forward uncertainty, and because projections are what the budget conversation is actually priced on. The discipline here is the same discipline from [mod-106 Chapter 05](../mod-106-outcome-measurement-and-executive-reporting/05-partnering-with-finance-on-cost-model-and-roi.md) — refuse point estimates, defend methodology, co-author with Finance — applied forward.

## Why projected ROI is a different artifact than trailing ROI

Three things change when the ROI calculation points forward.

- **Every term is a forecast.** Trailing ROI uses measured outcomes against measured costs. Projected ROI uses modeled outcomes against modeled costs. Each modeled term needs its own uncertainty characterization; what trailing ROI reports as a single band becomes a layered band whose width is the composition of the terms.
- **Timing starts to matter.** Trailing ROI collapses to a period total. Projected ROI happens over time — a rollout that saves 15% of operator time by month twelve does not save 15% in month one. The projection is a curve, not a point, and the curve's shape (ramp slope, time to steady state, decay) is often more load-bearing than the steady-state value.
- **Attribution decays with time.** The further out you project, the harder attribution gets. A year-one projection can lean on the trailing-six-months attribution evidence; a year-three projection is projecting through a horizon in which the workflow may have been redesigned and the tool may have been swapped.

The role of this chapter is to make these three pressures explicit on the artifact so the reviewer sees the uncertainty in the projection, not under it.

## The value-realisation framework — four forward dimensions

Every projected value claim lives in a four-dimensional grid. If any dimension is missing from the writeup, the projection is incomplete.

- **Magnitude.** How much value the rollout produces at steady state. Hours saved per operator per period, converted to currency; quality-improvement value; new value where applicable. The three numerator components from [mod-106 Chapter 05](../mod-106-outcome-measurement-and-executive-reporting/05-partnering-with-finance-on-cost-model-and-roi.md) carry forward unchanged.
- **Timing.** When the value shows up. A J-curve is the default shape: negative in the ramp (adoption cost exceeds value realised), zero at the crossover, positive after. Model the ramp, the crossover month, the time to steady state, and any plateau. "Full value by month six" is a timing claim and is often wrong by a factor of two.
- **Attribution.** What fraction of the modeled value is actually AI-induced versus concurrent operational changes, training effects, workflow redesigns, seasonal shifts. The three attribution frames from [mod-106 Chapter 05](../mod-106-outcome-measurement-and-executive-reporting/05-partnering-with-finance-on-cost-model-and-roi.md) carry forward: attribution by fraction (baseline), by cohort comparison (stronger), by staggered rollout (strongest).
- **Confidence.** The uncertainty around each of the above. Point estimates travel; they also break. Every projected value number ships with a confidence band or it does not ship.

The four dimensions together are the shape of a defensible projection. A projection that names magnitude but is silent on timing is incomplete; a projection that quantifies magnitude and timing but hand-waves attribution is a vendor-grade model. The role of the four-dimensional discipline is to make partial projections unshippable.

## Modelling the J-curve

The default shape of a rollout's value curve is a J-curve, not a step function. Four regions structure the curve.

1. **Ramp (months 0 to T_cross).** Operator learning time (Family 6 in [Chapter 01](01-the-enablement-cost-model-at-org-scope.md)), workflow-redesign effort, support-load spike, policy-review effort. Net value is *negative* — the organization is paying to adopt the tool before any value shows up. The ramp depth and length are the J's left arm.
2. **Crossover (T_cross).** The month in which periodic value realised crosses periodic cost. The crossover month is a load-bearing number in any budget conversation; it is the month the rollout becomes net-positive on an operating basis. Typical crossover months for well-run coding-copilot and knowledge-work rollouts run 3-9 months; vendor claims of instant crossover ignore the ramp.
3. **Steady state (T_cross to T_plateau).** The region the magnitude claim lives in. Value per operator per period at steady state is the number most commonly quoted; the honest projection reports it with the ramp and the plateau it is bounded by.
4. **Plateau (T_plateau onward).** Value stops growing. Common plateau drivers: addressable-task saturation, workflow redesign reaching its limit, tool capability frontier hit. Projecting growth past the plateau is the compounding-ROI-forever pattern from [mod-106 Chapter 05](../mod-106-outcome-measurement-and-executive-reporting/05-partnering-with-finance-on-cost-model-and-roi.md).

A textual sketch of a two-year rollout curve:

```
Monthly net value (illustrative only)

  +$X     *------- plateau -------*
          /
         /
        /
       /
  $0 -*------ crossover around month 7
      \
       \
        *----- deepest ramp cost around month 2

  month: 0   3   6   9   12  15  18  21  24
```

The curve is what to project; the integral of the curve across the projection horizon is the dollar value that goes into the ROI numerator. A projection that reports only the steady-state magnitude without the ramp understates ramp cost and overstates year-one ROI by typically 30-60%.

## Confidence bands — composing them across terms

Every term in the ROI projection carries its own band. The composed band is wider than any individual term; this is correct and should be visible on the artifact.

### Term 1 — magnitude band

The steady-state value per operator per period, with a band. Sources:

- **Trailing measurement, where it exists.** A prior rollout of the same tool in a comparable cohort is the gold standard; the trailing six-month distribution of value-per-operator gives you the band directly.
- **Evidence from the empirical literature, carefully transferred.** The Peng, Ziegler, Noy & Zhang, Brynjolfsson/Li/Raymond, and Dell'Acqua studies from [mod-106 Chapter 04](../mod-106-outcome-measurement-and-executive-reporting/04-reading-the-empirical-ai-productivity-literature-for-method-not-numbers.md) give published effect-size distributions for specific task families. The warning from that chapter is unchanged: transplant method, not numbers. If the literature gives a 20-55% productivity-gain distribution on a comparable task, your projected band is likely wider, not narrower, because your cohort is unobserved.
- **Vendor-reported ranges, with discount.** Vendor-published numbers are at the top of the plausible distribution for the task; use them as an upper bound, not a central estimate.

### Term 2 — timing band

The crossover month, with a band. The dominant uncertainty sources:

- **Adoption curve shape.** Fast adoption shortens the ramp; slow adoption lengthens it. The leading indicators from [mod-105 Chapter 07](../mod-105-champion-networks-and-change-management/07-measuring-change-management-health.md) are what you use to tune the timing band in-flight.
- **Workflow-fit lag.** How long the operator takes to integrate the tool into the workflow. Governed by training depth, champion density, and task complexity.
- **Change-management load.** Resistance patterns, manager coaching rhythm, communication cadence. Each of these shifts the crossover month.

### Term 3 — attribution band

The fraction of the observed value attributable to the AI tool, with a band. Forward attribution is harder than trailing attribution; be explicit about the method.

- **Attribution by fraction.** 40% ± 15% is a typical band for a rollout without a cohort comparison; the fraction is bounded by workflow-interview evidence on causal factors.
- **Attribution by cohort comparison.** The band is set by the uncertainty in the cohort match; typically narrower than attribution by fraction when the cohorts are well-matched.
- **Attribution by staggered rollout.** The band is the standard error of the difference-in-differences estimate; typically narrowest when the staggering is designed in rather than exploited post-hoc.

### Term 4 — cost band

The denominator carries its own uncertainty. The six families from [Chapter 01](01-the-enablement-cost-model-at-org-scope.md) contribute different band widths; Family 6 (downstream) is typically the widest because it is the most attested rather than invoiced.

### Composing the bands

Two composition approaches, both acceptable, chosen with Finance:

- **Analytical composition.** Treat the four bands as independent (they usually aren't quite — magnitude and attribution covary), compose by standard error propagation. Usable when the bands are roughly symmetric and not too wide.
- **Monte Carlo composition.** Draw samples from each term's distribution, compute ROI per draw, report the distribution's 10th and 90th percentiles (or your organization's standard band). Usable for wider bands or when term distributions are visibly asymmetric. A thousand-draw Monte Carlo runs in under a second in a spreadsheet or a short notebook; the mechanics are not the hard part.

Report both the central ROI and the composed band. Sensitivity analysis on the two or three most impactful assumptions ([mod-106 Chapter 05](../mod-106-outcome-measurement-and-executive-reporting/05-partnering-with-finance-on-cost-model-and-roi.md)) shows how ROI moves inside that band and which assumption the ROI is most load-bearing on.

## Refusing the point estimate — what to say instead

The pressure to ship a point estimate is persistent. Three forms the request takes and the response that preserves the methodology.

- **"I just need one number for the slide."** The one number is the central estimate; the slide carries the central estimate and the band in the same visual. If the slide designer removes the band, write it back in; a slide that shows "ROI = 2.1x" with no band is an editorial failure the enablement lead owns.
- **"Make it a range I can actually plan against."** The planning range *is* the confidence band. A range that is "1.4x–2.9x" is a defensible plan; a range that is "2.0x–2.2x" is a point estimate wearing a narrow band for cover.
- **"The CFO's finance team said no bands — just the midpoint."** The CFO's finance team is almost always wrong about this when it is said; the enablement lead's Finance partner is where the organizational standard on uncertainty reporting is resolved. See the Finance-partnership contract in [Chapter 04](04-partnering-with-procurement-finance-and-it.md).

The language on the artifact is: *"The point estimate is 2.1x. The 90% band is 1.4x–2.9x. The band is wide because the attribution fraction and the ramp length carry the largest uncertainty; a cohort-comparison update at the end of the first operating quarter will narrow the band."* Three sentences; the point estimate is quoted; the band and the narrowing plan are both on the page.

## Timing for the enablement budget ask

The ROI projection lands into three documents at different horizons; the band and the horizon are coupled.

- **The next-quarter projection.** 90-day horizon. Narrow band — most terms are grounded in recent trailing data. Appears in the quarterly review ([mod-106 Chapter 02](../mod-106-outcome-measurement-and-executive-reporting/02-authoring-the-executive-scorecard-weekly-monthly-quarterly.md)).
- **The annual budget projection.** 12-month horizon. Wider band — ramp and adoption shape have more room to vary. Lands into the annual budget ask with Finance.
- **The 2–3-year strategic projection.** 24-36-month horizon. Widest band — plateau timing, tool-market evolution, workflow-redesign effects are the dominant uncertainties. Lands into the board strategic memo ([mod-106 Chapter 03](../mod-106-outcome-measurement-and-executive-reporting/03-writing-for-executives-board-updates-lt-briefings-strategic-memos.md)) and build-vs-buy cases ([Chapter 03](03-the-build-vs-buy-matrix-at-enterprise-scope.md)).

A projection without a stated horizon is incomplete. A projection without a band whose width is appropriate to the horizon is theatre.

## Prioritising use cases on projected ROI

The role projects ROI to decide where enablement spend goes. Three prioritisation frames.

- **Expected value against the central estimate.** Rank use cases by central-estimate ROI × probability of successful execution. The simplest frame; usable when the bands are roughly comparable across candidates.
- **Risk-adjusted ranking.** Rank by the lower-bound (10th percentile) of the band. Favours robust, predictable rollouts over high-variance long-shots. Appropriate when the program has a credibility budget to protect — early CoE years, post-incident periods ([mod-109](../mod-109-ai-incident-response-and-enablement-side-rollback/README.md)).
- **Portfolio frame.** Distribute enablement spend across a portfolio with a target distribution — 60% high-confidence trailing-grounded projections, 30% medium-confidence new rollouts, 10% exploratory. Prevents the program from being either all-safe (no learning) or all-bet (reputationally brittle).

The prioritisation frame itself is a methodology choice co-authored with Finance and the executive sponsor; name the frame on the budget ask so the reviewer can see the shape of the portfolio.

## Theatre to watch for in projected ROI

Three patterns specific to projections (adding to the two trailing patterns from [mod-106 Chapter 05](../mod-106-outcome-measurement-and-executive-reporting/05-partnering-with-finance-on-cost-model-and-roi.md)).

- **The hockey-stick projection.** Steady-state value starts in month one and compounds. No ramp, no crossover, no plateau. Reverse-engineered from the target ROI number. Tell: a one-year ROI that is nearly identical to the three-year ROI on a per-year basis.
- **The band that walks.** The band widens in the methodology discussion and narrows in the summary slide. The summary ROI reads as a near-point estimate while the methodology appendix says the band is wide. Editorial failure; read your own summary against your own appendix before shipping.
- **The attribution by assertion.** The attribution fraction is quoted without an evidence source. "We estimate 60% attribution" with no cohort comparison, no workflow-interview distribution, no literature reference. The fraction is a number the enablement lead invented; the reviewer will call it.

## Where this chapter feeds

- [Chapter 03](03-the-build-vs-buy-matrix-at-enterprise-scope.md) uses projected ROI on the build and the buy candidate as the central comparison inputs.
- [Chapter 04](04-partnering-with-procurement-finance-and-it.md) is where the projection methodology becomes a co-signed artifact with Finance.
- [Chapter 05](05-reconciling-the-tool-stack-across-bus.md) uses projected ROI on the consolidation case versus the status quo.
- [Chapter 06](06-the-vendor-vetting-rubric.md) uses the projection band to price vendor-specific risks.
- Trails into [mod-106 Chapter 05](../mod-106-outcome-measurement-and-executive-reporting/05-partnering-with-finance-on-cost-model-and-roi.md) when the projection becomes trailing ROI and is reported against the original projection.

## Summary

- Projected ROI is a different artifact than trailing ROI because every term is a forecast with its own uncertainty, timing starts to matter, and attribution decays with horizon.
- Value realisation projects along four dimensions: magnitude, timing, attribution, confidence. A projection silent on any dimension is incomplete.
- The default rollout-value shape is a J-curve: ramp, crossover, steady state, plateau. Model the four regions; the integral is the numerator over the horizon.
- Compose confidence bands across magnitude, timing, attribution, and cost either analytically or via Monte Carlo — choose with Finance; report both central estimate and composed band.
- Refuse point estimates; the pressure to ship them comes in three recurring forms, and the band is a planning tool, not a hedge.
- Prioritise use cases on expected value, risk-adjusted lower bound, or portfolio frame — name the frame on the budget ask.
- Three projection-specific theatre patterns to catch before the reviewer does: hockey-stick, walking band, attribution by assertion.
