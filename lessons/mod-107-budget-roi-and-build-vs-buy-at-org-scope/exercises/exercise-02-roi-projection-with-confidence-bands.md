# Exercise 02 — ROI Projection with Confidence Bands

**Estimated effort:** 3 hours
**Format:** projection worksheet (Markdown table or spreadsheet) plus a written narrative with sensitivity analysis
**Grounding chapters:** [02 — Projecting ROI with Confidence Bands](../02-projecting-roi-with-confidence-bands.md), [01 — The Enablement Cost Model at Org Scope](../01-the-enablement-cost-model-at-org-scope.md), [mod-106 Chapter 04](../../mod-106-outcome-measurement-and-executive-reporting/04-reading-the-empirical-ai-productivity-literature-for-method-not-numbers.md), [mod-106 Chapter 05](../../mod-106-outcome-measurement-and-executive-reporting/05-partnering-with-finance-on-cost-model-and-roi.md)

## Objective

Project ROI on one priority use case over a three-year horizon, using the four-dimensional value-realisation framework (magnitude, timing, attribution, confidence) from [Chapter 02](../02-projecting-roi-with-confidence-bands.md). Model the J-curve explicitly, compose confidence bands across the four terms, run a sensitivity analysis on the two or three most impactful assumptions, and conclude with a prioritisation-frame statement. The output is the first draft of a projection that would land in the next annual budget ask.

## Prerequisites

- [Chapter 02](../02-projecting-roi-with-confidence-bands.md) read; the four dimensions, the J-curve regions, and the three theatre patterns close enough to cite without the chapter open.
- [Chapter 01](../01-the-enablement-cost-model-at-org-scope.md) read; the denominator in the projection uses the six-family cost model from Exercise 01.
- [mod-106 Chapter 04](../../mod-106-outcome-measurement-and-executive-reporting/04-reading-the-empirical-ai-productivity-literature-for-method-not-numbers.md) read; the literature method is what grounds the attribution and magnitude bands.
- [mod-106 Chapter 05](../../mod-106-outcome-measurement-and-executive-reporting/05-partnering-with-finance-on-cost-model-and-roi.md) read; the three attribution frames carry forward unchanged.
- One priority use case — a rollout in your chosen organization that has either (a) recent trailing data from a pilot, (b) a comparable prior rollout to benchmark against, or (c) sufficient literature grounding to project credibly. Candidates include a coding-copilot rollout in engineering, a knowledge-work copilot rollout in a knowledge-work function, or a support-copilot rollout in a service function.

## Problem statement

The CFO has requested a three-year ROI projection for the priority rollout to anchor next year's enablement budget ask. The previous year's budget cycle included a single point-estimate ROI (3.1x, no band) that the CFO's office discounted in-flight. The expectation for this cycle is a projection with:

- A magnitude estimate with an explicit distribution.
- A timing model (ramp, crossover, steady state, plateau).
- An attribution frame chosen and defended.
- A composed confidence band on the central ROI.
- A sensitivity analysis on the most impactful assumptions.
- A prioritisation-frame statement — expected value, risk-adjusted, or portfolio frame — explaining where this rollout falls in next year's portfolio.

You have three hours (this exercise) to produce the projection draft before taking it into the Finance working session.

## Requirements

### Part A — the projection worksheet

Produce a worksheet with:

- **The target rollout.** One or two sentences naming the Stage 1 problem ([mod-102 Chapter 01](../../mod-102-selecting-and-rolling-out-ai-tools/01-the-three-stage-selection-decision.md) shape), the cohort, the task, and the current baseline.
- **The J-curve, monthly, over 36 months.** Four columns:
  1. Monthly realised value (gross, before attribution).
  2. Monthly cost (from the Family 1-6 cost model, allocated monthly).
  3. Monthly net value (realised - cost).
  4. Cumulative net value.
  The curve should clearly show (a) a negative ramp period, (b) a crossover month, (c) a steady-state region, (d) a plateau.
- **The magnitude band.** The steady-state monthly realised value with a 10th-percentile and 90th-percentile, grounded in (a) trailing measurement if available, (b) literature-informed distributions (Peng, Ziegler, Noy & Zhang, Brynjolfsson et al., Dell'Acqua et al.) if not, cited per [mod-106 Chapter 04](../../mod-106-outcome-measurement-and-executive-reporting/04-reading-the-empirical-ai-productivity-literature-for-method-not-numbers.md). State which.
- **The timing band.** The crossover month with a 10th-percentile and 90th-percentile. State the dominant uncertainty sources (adoption curve shape, workflow-fit lag, change-management load).
- **The attribution frame.** Which of the three Chapter 05 frames (fraction, cohort comparison, staggered rollout). The fraction or cohort structure with its own band. State the evidence source.
- **The cost band.** From the Family 1-6 model; the Family 6 line usually carries the widest band because it is the most attested.
- **The composed ROI band.** Central estimate and 10th/90th percentile over year one, over year two, and over the three-year horizon. State the composition method (analytical propagation or Monte Carlo). If Monte Carlo, state the sample count.

### Part B — the written narrative

A 400-600 word narrative that the enablement lead would carry into the Finance working session. Structure:

- **Headline projection.** Central three-year ROI and composed band. One sentence.
- **The J-curve read.** Where the crossover month lands, the ramp depth, the steady-state magnitude, the plateau. Two to three sentences.
- **The attribution frame.** Which frame chosen, why, what evidence supports the specific fraction / comparison / staggering. The most-challenged paragraph; write it carefully.
- **The sensitivity analysis.** Named: the two or three most impactful assumptions, how ROI moves under plausible variations. Quantified: "at the 10th percentile of attribution, central three-year ROI falls to X; at the 90th percentile, it rises to Y."
- **The prioritisation frame.** Expected value, risk-adjusted, or portfolio frame. Where does this rollout fall in the year's portfolio? Why.
- **The methodology footnote.** Two sentences citing [mod-106 Chapter 04](../../mod-106-outcome-measurement-and-executive-reporting/04-reading-the-empirical-ai-productivity-literature-for-method-not-numbers.md) papers whose methods you used; naming the threats to validity this projection carries.

### Part C — the theatre-pattern self-check

A short checklist (3-5 sentences total) stating whether each of the three projection-specific theatre patterns from [Chapter 02](../02-projecting-roi-with-confidence-bands.md) appears in your projection:

1. Hockey-stick (no ramp, steady-state in month one, year-three per-year ROI ≈ year-one per-year ROI).
2. Walking band (summary slide narrower than methodology appendix band).
3. Attribution by assertion (attribution fraction without an evidence source).

For any pattern that is present, revise before finalizing.

## Starter guidance

- The three-year horizon is standard; some organizations use two or five. Pick three for this exercise so the output composes with Exercise 03's build-vs-buy matrix.
- If trailing data is available, use it. Published literature is a second-best; a trailing-six-months measurement on a comparable rollout is tighter than any published distribution. Vendor-published numbers are the upper bound, never the central estimate.
- The ramp is the single most-undermodelled region. If your crossover month is in month 1 or month 2, re-check — most knowledge-work rollouts have crossover months in the 3-9 range once operator learning time (Family 6), ramp-period support load (Family 2), and workflow-redesign effort are honestly counted.
- Realistic three-year central ROI for enablement portfolios tends to land in the 1.5-2.5x range on priority use cases, wider on exploratory ones. If your central is above 3x, re-check the magnitude distribution, the attribution fraction, and the ramp depth — one of them is likely optimistic.
- The attribution frame is the single most load-bearing choice. Attribution-by-fraction at 40% is a defensible baseline when workflow-interview evidence distributes causal factors across AI, training, and operational changes; cohort-comparison is stronger when matched cohorts can be constructed; staggered rollout is strongest when the rollout wave structure is deliberate. Pick the frame for the evidence you actually have.
- The composed-band width is almost always wider than feels comfortable. A 10th-to-90th-percentile ROI range spanning 50% of the central estimate is normal; a tight band is usually the summary-slide failure where the methodology band was wider than reported.
- The prioritisation frame is where the projection connects to the portfolio. Expected-value is simplest; risk-adjusted is more conservative; portfolio-frame is the most honest at enterprise scale. Name the frame on the narrative so the reviewer can see the portfolio shape.

## Deliverables

- `roi-projection-worksheet.md` (or `.xlsx`) containing Part A's monthly J-curve table and the composed ROI band.
- `roi-projection-narrative.md` containing Part B's written narrative and Part C's theatre-pattern self-check.

## Acceptance criteria

- The J-curve is modelled monthly for 36 months with the four regions (ramp, crossover, steady state, plateau) clearly visible.
- The magnitude band carries a 10th-percentile and 90th-percentile with the grounding source named (trailing data or specific literature reference).
- The timing band includes a crossover month with uncertainty; the crossover month is not in month 1 unless the rationale is explicit.
- The attribution frame is named as one of the three Chapter 05 frames, with the evidence source for the specific fraction / comparison / staggering.
- The composed ROI band uses a stated composition method (analytical or Monte Carlo); if Monte Carlo, the sample count is stated.
- The sensitivity analysis quantifies ROI shift under at least two plausible variations of the most impactful assumptions.
- The methodology footnote cites at least two [mod-106 Chapter 04](../../mod-106-outcome-measurement-and-executive-reporting/04-reading-the-empirical-ai-productivity-literature-for-method-not-numbers.md) papers by title and names at least two threats to validity.
- The prioritisation-frame statement names the frame and places this rollout in a portfolio context.
- The theatre-pattern self-check addresses each of the three patterns from [Chapter 02](../02-projecting-roi-with-confidence-bands.md); where any pattern is present, the projection has been revised.
- The three-year central ROI is defended; if above 3x, the rationale for the high central is in the narrative.

## Stretch goals

- Run the projection under three scenarios — base, aggressive adoption, slow adoption — with the J-curve shifting across the three. The scenario slate is what a Finance scenario-modelling session consumes.
- Produce the forward-looking commitment paragraph: what the organization is committing to deliver next year from this rollout, with its own confidence band. Forward-looking commitments carry more reputational weight than trailing reports; resisting the compounding-ROI-forever pattern from [mod-106 Chapter 05](../../mod-106-outcome-measurement-and-executive-reporting/05-partnering-with-finance-on-cost-model-and-roi.md) is the discipline.
- Draft the three-sentence email you would send to the CFO ahead of the Finance working session. Lead with the composed band, not the central estimate; the band is what Finance will want to probe.

## Why this exercise matters

ROI projections are where enablement budgets are decided. A point-estimate projection with no band is a number that will be revised downward in the budget review and remembered as unreliable in the one after. A J-curve projection with a composed band, a stated attribution frame, and a sensitivity analysis is the artifact a CFO can sign off on even when the band is wide — because the band *is* the methodology signal. This exercise is the first draft of the artifact that will anchor your next annual budget ask.
