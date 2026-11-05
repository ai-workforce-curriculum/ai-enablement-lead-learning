# Exercise 06 — ROI Numerator and Denominator Defence

**Estimated effort:** 2 hours
**Format:** written ROI narrative plus a simulated Finance Q&A, Markdown
**Grounding chapters:** [05 — Partnering with Finance on the Cost Model and ROI](../05-partnering-with-finance-on-cost-model-and-roi.md), [04 — Reading the Empirical AI Productivity Literature for Method, Not Numbers](../04-reading-the-empirical-ai-productivity-literature-for-method-not-numbers.md), [06 — Coordinating with the Analyst and the Team Manager](../06-coordinating-with-the-analyst-and-the-team-manager.md)

## Objective

Produce the ROI narrative that would appear in Section 6 of the quarterly review for your portfolio, with a numerator and a denominator each separately defensible, a confidence band, a sensitivity analysis, and an explicit attribution frame. Then simulate the Finance partner's pushback — six specific challenges, each answered in two to three sentences — so the narrative you end up with is one that would survive the standing quarterly ROI review from [Chapter 05](../05-partnering-with-finance-on-cost-model-and-roi.md).

## Prerequisites

- [Chapter 05](../05-partnering-with-finance-on-cost-model-and-roi.md) read, with the numerator/denominator components, attribution frames, and theatre patterns close enough to cite without the chapter open.
- [Chapter 04](../04-reading-the-empirical-ai-productivity-literature-for-method-not-numbers.md) read; the methodology patterns are what back the attribution claims.
- [Chapter 06](../06-coordinating-with-the-analyst-and-the-team-manager.md) read; the handoff interfaces produce the inputs to the ROI calculation.
- A portfolio sketch (from Exercise 01 or newly constructed): at least four rollouts across at least two task families, at least two business units, running for at least six months at the quarter's end.
- One attribution frame chosen in advance (attribution by fraction, by cohort comparison, or by staggered rollout). The frame choice shapes the narrative; picking one before you start is the discipline.

## Problem statement

Your CoE's portfolio is nearing the end of its sixth quarter in production. The CFO's office, through the Finance partner embedded with enablement, has asked for a defensible ROI narrative for the next quarterly review. The current narrative in last quarter's review was a point estimate of 2.8x with no confidence band and a vendor-adjacent methodology footnote; the Finance partner has indicated that the narrative will not survive a second quarter in that form.

You have one week to produce the narrative, review it with Finance, and have it ready for Section 6 of the quarterly review. This exercise is the first draft and the Finance Q&A you expect to receive.

## Requirements

### Part A — the ROI narrative

Produce the Section 6 narrative, roughly 600-900 words. Structure:

- **Headline ROI.** The central estimate, the 90% confidence band, the sensitivity note. One to two sentences. Carries no vendor-reported numbers.
- **The numerator.** Walk through the three value-realised components: time saved, quality improvements, new value. For each component, name the rollouts that contributed, the magnitude, the conversion to currency, and the source of the input (team manager measurement, workflow interview, analyst analysis — the handoffs from [Chapter 06](../06-coordinating-with-the-analyst-and-the-team-manager.md)). Where a component is small or zero, say so; do not pad.
- **The denominator.** Walk through the four cost components: tool licenses, enablement program spend, embedded FTE time, downstream support cost. Each has a dollar figure and a source. The fully-loaded FTE multiplier is stated explicitly.
- **The attribution frame.** Which of the three Chapter 05 frames you chose (fraction, cohort comparison, staggered rollout), why, and what evidence supports the specific fraction / comparison / staggering choice. This is the single most-challenged paragraph; write it carefully.
- **The sensitivity analysis.** How ROI moves under plausible variations in the two or three most impactful assumptions — usually attribution fraction, time-to-currency conversion, and denominator scope.
- **The methodology footnote.** Two to three sentences citing [Chapter 04](../04-reading-the-empirical-ai-productivity-literature-for-method-not-numbers.md) papers whose *methods* you borrowed, along with the three to four [Chapter 04](../04-reading-the-empirical-ai-productivity-literature-for-method-not-numbers.md) threats to validity you are defending against.

The narrative is honest if it reads in a way that could lower the ROI number as well as raise it. A narrative that only supports a higher number is the reverse-engineered-ROI pattern from Chapter 05.

### Part B — the simulated Finance Q&A

Write six Finance-partner challenges you expect to receive at the standing quarterly ROI review, with your answer to each. The six challenges together should probe the full narrative; a Q&A that attacks only the numerator is incomplete.

Suggested coverage (pick at least five of these; the sixth can be a surprise challenge of your own design):

1. A challenge on the denominator's completeness — "did you include downstream support cost, and if so, how?"
2. A challenge on the time-to-currency conversion rate — "why that rate, not the organization's standard fully-loaded multiplier?"
3. A challenge on the attribution frame — "how do we know the 40% isn't actually 20%?"
4. A challenge on the confidence-band methodology — "what did you bootstrap over, and does the band include the attribution uncertainty?"
5. A challenge on a specific value-realised component — "the new-value number for the sales rollout: is the attribution to the AI tool or to the compensation change that landed concurrently?"
6. A challenge on last quarter's narrative — "what changed in the methodology from last quarter to this one, and why should we believe the new number more?"

Each answer is two to three sentences. "Good question, we'll look into it" is a failed answer; so is any answer longer than three sentences, which signals you are over-explaining. The answers should either respond substantively or acknowledge, specifically, that this is an area where the methodology needs further work — with a committed timeline.

## Starter guidance

- Pick a portfolio ROI in the range of 1.5x to 2.5x. Numbers above 3x almost always fail the second-quarter test; this exercise is about defending a believable number, not an impressive one.
- The confidence band on the central estimate should be wide — somewhere around 60-80% of the central estimate at the low end and 110-140% at the high end for most portfolios at this stage of maturity. A tight band (e.g., 2.1x ±0.1) is implausible; Finance will know.
- The attribution frame is the single most load-bearing choice. If you pick attribution-by-fraction, the fraction has to be defended by an evidence source — usually workflow-interview distribution across causal factors. If you pick cohort comparison, you need to describe the matched cohort construction. If you pick staggered rollout, you need to describe the difference-in-differences logic.
- The Finance Q&A is a simulation, not a transcript. Write the challenges as a Finance partner who knows methodology well would write them — pointed, specific, and sometimes uncomfortable. Writing softball challenges is self-defeating; the point is to find the holes in the narrative before Finance does.
- The sixth "surprise" challenge is often the most instructive. Candidates: a challenge on a rollout that is missing its outcome ("why is it still in the numerator?"), a challenge on the comparison to the organization's non-AI investments ("what's the ROI on the training budget?"), a challenge on forward-looking commitments ("you're projecting 3x next year — show me the math").
- Avoid the Chapter 05 reverse-engineered-ROI pattern. If your narrative would have landed on the same number regardless of the attribution analysis, the attribution analysis is decorative. Write a narrative where the attribution genuinely bounded the number, even if the bound is not favourable.

## Deliverables

- `roi-narrative-and-defence.md` containing Part A (the ROI narrative) and Part B (six simulated Finance challenges with answers).

## Acceptance criteria

- The headline ROI carries a 90% confidence band and a sensitivity note in the same sentence or the immediately following sentence.
- The numerator walk covers all three value-realised components; components that are small or zero are stated as such, not padded.
- The denominator walk covers all four cost components, each with a dollar figure and a source. The fully-loaded FTE multiplier is stated explicitly.
- The attribution frame is one of the three Chapter 05 frames, named, with evidence supporting the specific fraction or comparison.
- The sensitivity analysis names the two or three most impactful assumptions and quantifies how ROI shifts under plausible variations.
- The methodology footnote cites at least two Chapter 04 papers by title, and names at least two Chapter 04 threats to validity.
- The six Finance challenges together cover numerator, denominator, attribution, confidence, and methodology-change-over-time dimensions.
- No answer in Part B is longer than three sentences; no answer is a deflection ("we'll look into it"); where methodology work is incomplete, the answer acknowledges this with a specific timeline.

## Stretch goals

- Write the one-page strategic memo (per [Chapter 03](../03-writing-for-executives-board-updates-lt-briefings-strategic-memos.md)) you would send to the CFO *before* the standing quarterly review, pre-negotiating the ROI methodology. This moves the Finance challenge out of the board room and into a working session, which is where it belongs.
- Produce the next-quarter forward-looking ROI commitment: a projected ROI range for the next quarter with its own confidence band and the three assumptions it is most sensitive to. Forward-looking ROI is harder than trailing ROI; the exercise is in resisting the compounding-ROI-forever pattern from [Chapter 05](../05-partnering-with-finance-on-cost-model-and-roi.md).
- Draft the one-paragraph note the Finance partner would include in their co-signoff on the ROI line in the board update. The note is the Finance partner's framing of the methodology; writing it from the Finance partner's perspective is how you test whether the narrative actually earns their co-sign.

## Why this exercise matters

The ROI number is the single most-quoted number from the enablement program. If it is quoted without a confidence band, without an attribution frame, or against an invisible denominator, it becomes the number that undermines the rest of the scorecard the quarter it is challenged. The CFO who watches a program's ROI number survive two quarters of scrutiny starts treating the program as a serious counterparty; the CFO who catches a reverse-engineered or vendor-adjacent ROI starts treating every other number from the program the same way. This exercise is the preparation that makes the running Finance partnership from Chapter 05 pay.
