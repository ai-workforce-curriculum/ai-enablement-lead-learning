# Partnering with Finance on the Cost Model and ROI

> The ROI number is where enablement programs most often lose a CFO's trust. Not because the number is wrong — most published ROI numbers are *plausible* — but because the methodology is not defensible. The enablement lead who cannot explain where the numerator came from, what the denominator includes, and how AI-induced gain was separated from everything else moving in the organization is the enablement lead whose quarterly review will be challenged in the room and discounted after. This chapter is how the ROI narrative gets built with Finance, not in spite of Finance. Deep budget and build-vs-buy work lives in [mod-107](../mod-107-budget-roi-and-build-vs-buy-at-org-scope/README.md); this chapter treats the ROI *narrative on the scorecard* and the Finance partnership that makes it defensible.

## Why ROI gets reported badly

Three structural pressures push ROI narratives toward the indefensible.

- **Point estimates travel faster than ranges.** "This program delivers 3.2x ROI" is easier to put on a slide than "value realised is in the range of 1.5x–4.1x with 90% confidence." The travelling point estimate acquires authority it does not deserve.
- **Vendor ROI calculators exist and are convenient.** Most tool vendors publish ROI calculators. They are marketing instruments; their denominators exclude enablement program spend and FTE time, and their numerators extrapolate from favourable benchmark studies. Using them is faster than building the organization's own model. The output looks like ROI; it is not.
- **Enablement leads often skip Finance.** Finance is seen as an obstacle — slow, methodologically stringent, likely to dampen the headline number. The enablement lead who writes the ROI narrative alone produces a number that Finance will find later, in the quarterly review, in a room where the correction is public. Bring Finance in at the start; the public correction does not happen.

The role of this chapter is to make the Finance partnership the asset it should be, so that the ROI narrative in the quarterly review from [Chapter 02](02-authoring-the-executive-scorecard-weekly-monthly-quarterly.md) survives challenge.

## The ROI equation at this layer

ROI at the program level is:

```
ROI = (Value realised - Cost) / Cost
```

With *value realised* and *cost* each requiring their own defensible construction. The ratio is only as credible as the two components; a beautifully computed ratio over an indefensible numerator or denominator is still indefensible.

Every term in both the numerator and the denominator will be challenged. The partnership with Finance is what makes each challenge survivable.

## The numerator — value realised

### Three components, each separately defended

Value realised at program scope is the sum of three component types:

- **Time saved, converted to currency.** For each rollout: operator-hours saved per unit of work × units of work per period × currency conversion (usually fully-loaded cost of operator time). The conversion of time to currency is a Finance methodology decision, not an enablement decision; use the organization's standard rate, not a bespoke one.
- **Quality improvements, where measurable.** Defect avoidance, rework reduction, downstream error reduction. These are harder to convert to currency and often require Finance to make an organizational judgement call on the cost of a defect or a rework. Where the conversion is not defensible, carry the quality improvement as a separate narrative line rather than forcing it into the numerator.
- **New value, where it exists.** Revenue influenced, deals closed faster, customer retention delta, new capability created. The hardest to attribute but often the most important to the business story. Finance is where the attribution logic gets built; the enablement lead who tries to construct this alone is building a number Finance will not defend.

### The attribution discipline

The single hardest methodology problem in ROI reporting is attribution — *how much of the observed value is AI-induced*, as opposed to concurrent operational changes, workflow redesigns, training-program effects, or seasonal shifts.

Three attribution frames, in increasing rigour:

- **Attribution by fraction.** The enablement program claims a stated fraction of the value — for example, 40% of the outcome movement. The fraction is a methodology assumption, defended by the literature from [Chapter 04](04-reading-the-empirical-ai-productivity-literature-for-method-not-numbers.md) and the workflow interviews from [Chapter 01](01-the-measurement-stack-at-org-scope.md). Publish the fraction, the rationale, and the sensitivity — "at 40% attribution, value is $X; at 25% attribution, value is $Y."
- **Attribution by cohort comparison.** Compare a tool-using cohort to a matched non-using cohort inside the same business unit, at the same time. The difference is the AI-attributable value. Methodologically stronger; operationally harder because matched cohorts require deliberate design.
- **Attribution by staggered rollout.** Rollouts that go to different BUs at different times create a natural comparison. The difference-in-differences framework from the Brynjolfsson et al. study in [Chapter 04](04-reading-the-empirical-ai-productivity-literature-for-method-not-numbers.md) is the reference. Methodologically strongest; operationally hardest.

The enablement lead chooses the attribution frame with Finance before the quarterly review is written. The frame choice is itself a line on the methodology appendix — "attribution by fraction (40%, rationale: workflow-interview distribution across causal factors)" — so that a reviewer can see the choice and challenge it on method rather than on the number.

### What does not belong in the numerator

- **Vendor-reported productivity gains.** These are not value realised in your organization; they are marketing from the vendor. Chapter 04's reading discipline is what prevents this from migrating into the numerator.
- **Unused seats' hypothetical value.** If 60% of licensed seats are not actively used, the value from those seats is zero, not the extrapolation of the active-user value. The denominator carries those seat costs; the numerator does not reclaim them as value.
- **Time saved that has not been redeployed.** Ten minutes saved per operator per day is a different claim than ten minutes of productive capacity added. If the saved time goes to idle, the value is not realised. Finance will ask this question; prepare the answer — usually by scoping value claims to work that was *backfilled* by freed capacity (an additional task completed, a wait-time reduced in the customer-facing workflow, etc.).

## The denominator — cost

### Four cost components, each separately itemized

Cost at program scope has four components, each of which the enablement lead and Finance jointly maintain:

- **Tool licenses.** The direct cost of the AI tools in the portfolio — enterprise seats, per-seat per-month charges, usage-based charges, premium add-ons. The vendor invoice is the primary source. Include contracted-but-unused seats; those are a cost whether or not value is being extracted.
- **Enablement program spend.** The CoE's operating budget — enablement-team headcount (loaded), training production (internal and external), champion program operating cost, content and tooling for the enablement function itself, support infrastructure.
- **Embedded enablement partner FTE time.** Partners embedded in business units who spend a fraction of their time on enablement work. 20% of a senior engineer's time on champion duties is a cost; counting it is the discipline that prevents the denominator from understating.
- **Downstream support cost.** Help-desk tickets generated by AI-tool support, escalations into IT, security review time, legal review time on policy updates, incident-response time when a rollout surfaces harm (per [mod-109](../mod-109-ai-incident-response-and-enablement-side-rollback/README.md)). Often the hardest to measure; always the first to be challenged as missing.

The denominator discipline is the discipline of *not making the denominator smaller than it is*. The temptation is to count only tool licenses, because that is the invoice Finance already tracks. The honest denominator includes the three other components, and the quarterly review that makes this visible builds credibility over cycles.

### The fully-loaded FTE question

The single most common Finance methodology challenge on the denominator is whether FTE time is counted at *salary* or at *fully-loaded cost*. Finance will almost always want fully-loaded cost (salary + benefits + facilities + overhead allocation). The enablement lead's reflex is often to use salary because it produces a smaller denominator and a better-looking ROI. Fully-loaded cost is the correct answer; using it is also the move that makes Finance an ally rather than a late-stage auditor.

Use the organization's standard fully-loaded multiplier (usually 1.3x to 1.5x of salary). Do not invent one; Finance already has it.

### What does not belong in the denominator

- **One-time pilot costs, after the pilot has closed.** Pilot costs are costs during the pilot period. Once the rollout is live, the ongoing operating cost is the denominator going forward; the pilot cost belongs to the pilot's own economic story, not to the running ROI calculation.
- **Opportunity cost of not adopting a different tool.** This is a vendor-marketing argument. Opportunity cost is not a cost in the ROI denominator; it is a different calculation with its own methodology.
- **Costs the organization was already incurring.** Microsoft 365 licenses that existed before Copilot was added are not AI-program costs; the *incremental* Copilot license is. Separate the AI-incremental cost from the pre-existing baseline cost.

## The confidence-band discipline, at ROI altitude

ROI never ships as a point estimate. The quarterly review carries:

- A central estimate of ROI.
- A 90% confidence band (or the organization's standard uncertainty-reporting band).
- A sensitivity analysis showing how ROI changes under plausible variations in the two or three most impactful assumptions — usually attribution fraction, value-conversion rate (time to currency), and scope of the denominator.

A worked example (fictional) of how this reads:

> **Program ROI, Q3.** Central estimate: 2.1x. 90% confidence band: 1.4x–2.9x. Sensitivity: at 25% attribution fraction, central ROI falls to 1.3x; at 55% attribution fraction, central ROI rises to 2.9x. Attribution fraction is the most sensitive assumption; it is reviewed quarterly with Finance based on cohort-comparison updates.

A point-estimate ROI without a band is a number that will not survive its second quarter. The band is the methodological signal that the number was built with Finance, not around Finance.

## The Finance partnership contract

The partnership with Finance is a running one, not a one-time hand-off. A durable contract covers four interfaces:

### Interface 1 — standing quarterly ROI review

Thirty to sixty minutes, week 10 of each quarter, with the Finance partner assigned to enablement (CFO's office or FP&A depending on the organization). Agenda:

- Current-quarter ROI draft with numerator, denominator, attribution logic.
- Any methodology changes from the prior quarter.
- The sensitivity analysis; what Finance would challenge on.
- The one-page ROI narrative for the quarterly review; Finance's edits before it ships.

### Interface 2 — monthly invoice reconciliation

Fifteen to thirty minutes, monthly. Finance reconciles vendor invoices against the denominator; the enablement lead flags any new rollouts or tool additions that will land in the next quarter's denominator. The reconciliation is what keeps the denominator complete; a tool that joined the portfolio in month two of a quarter without Finance noticing is a denominator gap.

### Interface 3 — ad-hoc for vendor contracts

When a new vendor contract is in flight, Finance reviews the contract terms (license counts, usage-based charges, true-up provisions, renewal uplift). The enablement lead carries the use case and the pilot plan. The joint output is a cost projection that lands in the next quarterly denominator with provenance; this is also the interface where [mod-107](../mod-107-budget-roi-and-build-vs-buy-at-org-scope/README.md)'s cost-modeling depth lands in the running scorecard.

### Interface 4 — the FTE-time attribution working group

An annual or semi-annual working session. The enablement lead, Finance, and HR/Workforce Planning align on how embedded FTE time is accounted for across BUs. This is organizationally slow work; it is also the work that keeps the denominator defensible across staffing changes.

## What the enablement lead owns and what Finance owns

A durable split:

- **Enablement lead owns.** The outcome measurement (numerator inputs), the attribution logic (with Finance challenge), the workflow-interview evidence that supports attribution, the scope of the denominator (what rollouts are in the portfolio), the ROI narrative in the quarterly review.
- **Finance owns.** The time-to-currency conversion rate, the fully-loaded FTE multiplier, the methodology for vendor-invoice recognition, the standard uncertainty-reporting band, the sign-off on the ROI line on the board update.
- **Co-owned.** The attribution fraction (methodology plus organizational judgement), the confidence band (statistical plus organizational), the sensitivity analysis.

This split is the operating interface. The enablement lead who tries to own Finance's columns is building a ROI number that will not survive internal audit; the Finance partner who tries to own the enablement columns is building a ROI number disconnected from the operating reality of the rollouts. Each side holds its own.

## The role of ROI on each scorecard cadence

ROI appears on the three cadences from [Chapter 02](02-authoring-the-executive-scorecard-weekly-monthly-quarterly.md) at different resolutions:

- **Weekly rollup.** ROI does not appear. The weekly cadence is too short to produce a defensible ROI update; a weekly ROI number is theatre.
- **Monthly deep-dive.** ROI appears as a trajectory line against the quarterly plan, not as a point estimate. "On track against Q3 ROI projection" or "below Q3 ROI projection, driven by Y" is the honest shape.
- **Quarterly board-ready review.** The full ROI narrative — central estimate, confidence band, sensitivity analysis, attribution logic — lands in section 6 of the quarterly review. This is the artifact Finance co-signs.

Treat ROI as a quarterly product, not a weekly dashboard metric. The infrastructure to produce it credibly does not run at weekly cadence.

## Theatre to watch for in ROI reporting

Two named patterns to catch in your own work before a reviewer catches them:

- **The reverse-engineered ROI.** The target ROI number is chosen first (often "3x, to match the industry benchmark"), and the attribution fraction or the denominator scope is adjusted until the number lands there. The methodology appendix is written to support the predetermined number, not to produce it. Watch for this pattern in your own drafts; the tell is that the attribution fraction changes between quarters without a corresponding change in the evidence that would justify it.
- **The compounding-ROI-forever projection.** A quarterly ROI of 2.1x is projected forward as compounding — 4.2x year two, 8.4x year three — as if the gain scales linearly. In practice, gains plateau, costs grow, and the compounding projection is almost never defensible. Report trailing ROI; forward-looking ROI is a forecast with its own uncertainty, and the quarterly review treats it as such.

## Where this chapter feeds

- [Chapter 02](02-authoring-the-executive-scorecard-weekly-monthly-quarterly.md) section 6 of the quarterly review is where the ROI narrative lands.
- [Chapter 03](03-writing-for-executives-board-updates-lt-briefings-strategic-memos.md) treats how the ROI narrative becomes a board-ready paragraph.
- [Chapter 04](04-reading-the-empirical-ai-productivity-literature-for-method-not-numbers.md) grounds the attribution and uncertainty methodology.
- [mod-107](../mod-107-budget-roi-and-build-vs-buy-at-org-scope/README.md) is where the cost model and the build-vs-buy matrix live at depth; this chapter is the scorecard-facing slice.
- Exercise 06 walks the numerator/denominator defence against a simulated Finance challenge.

## Summary

- ROI = (Value realised - Cost) / Cost, with each component separately defended; the ratio is only as credible as its components.
- Numerator has three components (time saved, quality improvements, new value), each with its own attribution challenge; attribution-by-fraction is the baseline, attribution-by-cohort or by staggered rollout is stronger.
- Denominator has four components (tool licenses, enablement program spend, embedded FTE time, downstream support cost); honest denominators are not smaller than they are.
- Report ROI with a central estimate, a 90% confidence band, and a sensitivity analysis on the two or three most impactful assumptions; point-estimate ROI is a number that does not survive a second quarter.
- The Finance partnership is a running contract — standing quarterly ROI review, monthly invoice reconciliation, ad-hoc contract review, semi-annual FTE-attribution working group — with a durable split between enablement-owned and Finance-owned columns.
- ROI appears on the quarterly cadence only; weekly ROI is theatre and monthly ROI is a trajectory line against plan.
- Two named ROI theatre patterns — reverse-engineered ROI, compounding-ROI-forever — to catch in your own drafts before a reviewer does.
