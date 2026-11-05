# Exercise 03 — Quarterly Board-Ready Review Outline

**Estimated effort:** 3 hours
**Format:** outline document (section headings and content-shape bullets, not full prose), plus a fully-drafted one-page executive summary
**Grounding chapters:** [02 — Authoring the Executive Scorecard — Weekly, Monthly, Quarterly](../02-authoring-the-executive-scorecard-weekly-monthly-quarterly.md), [03 — Writing for Executives — Board Updates, LT Briefings, Strategic Memos](../03-writing-for-executives-board-updates-lt-briefings-strategic-memos.md)

## Objective

Produce the eight-section outline for a board-ready quarterly review of your organization's AI enablement program, plus the fully-drafted one-page executive summary that will be the first (and often only) page a board member reads. The outline is deliberately not full prose — authoring the full quarterly review is a quarter of operating work, not a single exercise — but the outline plus the executive summary must be specific enough that a reader can tell what the full review would say.

## Prerequisites

- [Chapter 02](../02-authoring-the-executive-scorecard-weekly-monthly-quarterly.md) read, with the eight-section quarterly structure close enough to work from without the chapter open.
- [Chapter 03](../03-writing-for-executives-board-updates-lt-briefings-strategic-memos.md) read, with the BLUF, misses-in-the-lead, and confidence-band structural moves available.
- One chosen organization with a sketched portfolio (ideally the same organization carried from Exercise 01 and 02). The portfolio should include at least five live rollouts across at least two task families.
- Decide, before writing, what the quarter's dominant story is: a quarter on plan, a quarter with significant misses, or a quarter with a mixed picture. The story shape changes what the review emphasizes; writing without picking is how reviews end up incoherent.

## Problem statement

You are the AI Enablement Lead. The quarterly board packet goes out in two weeks. Your CAIO is drafting the board narrative for the broader AI agenda; your six to ten pages on the enablement program are the data-and-narrative appendix that supports one of the CAIO's slides. You need to produce the outline of the review — all eight sections per [Chapter 02](../02-authoring-the-executive-scorecard-weekly-monthly-quarterly.md) — and the one-page executive summary that opens it.

The board will read the summary. Approximately half will read page 2 (portfolio-level outcomes). Three or four will read the hit list and the miss list. One or two will read the methodology appendix. The six to ten pages must survive each of these reading depths.

## Requirements

### Part A — the eight-section outline

For each of the eight sections from [Chapter 02](../02-authoring-the-executive-scorecard-weekly-monthly-quarterly.md), produce:

1. A section heading matching the Chapter 02 template.
2. Three to six content bullets that specify *what the section will contain* — concrete, with proposed numbers, metric names, rollout names, risk descriptions. Not prose; also not "TBD." A reader should be able to tell from the bullets whether the section will land.
3. One brief sentence per section naming the *editorial risk* for that section — the way this section could drift into theatre if the writing drifts. "Section 3 risk: the hit list becomes a vendor-feature celebration rather than an outcome narrative." Each editorial-risk sentence is one of the Chapter 01 or Chapter 03 named patterns.

The eight sections, per Chapter 02:

1. One-page executive summary (outlined in Part A; fully drafted in Part B).
2. Portfolio-level outcome rollups.
3. The hit list.
4. The miss list — and the quarter's lessons.
5. Qualitative ground truth at quarterly resolution.
6. ROI narrative.
7. Strategic risks on the one-to-three-quarter horizon.
8. Investment asks and strategic decisions requested.

Plus a note on the appendix (per-rollout detail, methodology notes, delta vs. last quarter's commitments) — one paragraph on what the appendix contains.

### Part B — the fully-drafted executive summary

A single page (roughly 350-500 words) that opens the quarterly review. Structure it with the [Chapter 03](../03-writing-for-executives-board-updates-lt-briefings-strategic-memos.md) BLUF discipline:

- Opening paragraph: BLUF — the headline finding or recommendation, the ask, the confidence. Three sentences.
- Second paragraph: the quarter's dominant story. If misses dominate, lead with them per Chapter 03's misses-in-the-lead discipline. If hits dominate, acknowledge the dominant miss early.
- Third paragraph: the single most important forward-looking commitment for next quarter.
- Fourth paragraph (optional, usually a short one): the one strategic decision the board is being asked to make, with the decision-by date.

Carry a confidence band on the headline number. If you quote an ROI or productivity figure, it has a 90% CI and a sensitivity note in the same sentence.

### Part C — the editorial-risk reading

A short note at the end of the file (five to eight sentences) that identifies:

- Which two sections of the outline were hardest to make specific, and why.
- One editorial choice in the executive summary that you expect pushback on (the headline framing, a miss acknowledgement, an ask that is larger than last quarter's), and how you would defend it in the room.
- One Chapter 04 methodology pattern you drew on when constructing a portfolio-level outcome number, and why.

## Starter guidance

- The executive summary is written last, even though it appears first. Draft the outline first so the summary has material to summarize; then write the summary; then revise the outline to make sure the summary's claims are supported deeper in the document.
- The outline bullets are not full sentences; they are content commitments. "Portfolio productivity rollup across drafting workflows: 22% median reduction, 90% CI 14-29%, n=842 operators, 14 weeks post-rollout, methodology per Chapter 04 Pattern 3 longitudinal" is the right density. "Report productivity numbers" is not.
- The hit list and the miss list should carry *equal weight* in the outline. If your hit list has five entries and your miss list has one, the review will read as theatre regardless of whether the balance is accurate. Either expand the miss list or compress the hit list.
- The miss list's "learned" lines per Chapter 02 are the most important lines in the outline. If you cannot write a learned line for a miss, the miss has not been diagnosed yet — say so in the miss outline, and that becomes an ask in section 8.
- The ROI narrative in section 6 should cite the attribution frame explicitly (see [Chapter 05](../05-partnering-with-finance-on-cost-model-and-roi.md)). An ROI number without an attribution frame is a point estimate reader-pattern-matches as theatre.
- Section 7 strategic risks are forward-looking; the three to five you name are the risks that are not yet on the scorecard but likely will be. Vendor concentration, regulatory change, and workforce-impact patterns from quarterly interviews are common candidates.
- The one-page executive summary is a BLUF document, not a synopsis. "In Q3 we rolled out AI across the enterprise and saw adoption growth" is a synopsis. The BLUF version carries the outcome, the ask, and the confidence in three sentences.

## Deliverables

- `quarterly-review-outline.md` containing Parts A (eight-section outline plus appendix note), B (fully-drafted executive summary on one page), and C (editorial-risk reading).

## Acceptance criteria

- The outline contains all eight sections in the specified order plus the appendix note.
- Each section has three to six content bullets and exactly one editorial-risk sentence citing a named Chapter 01 or Chapter 03 pattern.
- The hit list (section 3) and miss list (section 4) have equivalent content weight (comparable number of rollouts named, comparable depth of bullets).
- Every miss in section 4 has a "learned" bullet, or an honest statement that diagnosis is in progress with a named owner and a date.
- The ROI narrative in section 6 states the attribution frame being used (fraction, cohort comparison, or staggered rollout per Chapter 05) and carries a confidence band on the central number.
- The executive summary fits on one page, opens with a BLUF paragraph, and if it quotes a quantitative headline, that headline carries a confidence band in the same sentence.
- The executive summary does not open with a usage percentage, an adoption number, or a vendor-supplied statistic.
- If the quarter had a dominant miss, the executive summary acknowledges it by the second paragraph. If the summary buries misses to the fourth paragraph or later, the exercise fails.
- The editorial-risk reading identifies two specific sections and one specific editorial choice; "all of it was hard" does not count.

## Stretch goals

- Produce a short "co-author with the CAIO" note — three sentences on which parts of the review you would expect the CAIO to redraft, and why. This is the sponsor-handoff discipline from [Chapter 03](../03-writing-for-executives-board-updates-lt-briefings-strategic-memos.md).
- Sketch the slide deck the CAIO will build on top of this document — four or five slide titles with the specific numbers they will carry. The slide deck exists as a derivative of the written review; drafting the slides from the review (rather than the reverse) is the editorial discipline.
- Write the one-page strategic memo (per [Chapter 03](../03-writing-for-executives-board-updates-lt-briefings-strategic-memos.md)) that the enablement lead would send to the CFO separately on the ROI section, before the board packet. The memo pre-negotiates the Finance review of the ROI number so the board room is not where the Finance challenge lands.

## Why this exercise matters

The quarterly review is the artifact that shapes next quarter's budget, next quarter's scope, and next year's strategic direction for the enablement program. It is the one artifact in the module whose failure cannot be absorbed by the weekly cadence — if the quarterly lands weakly, the program's funding and credibility shift. The outline-and-summary format of this exercise is deliberate: writing the full six to ten pages would exceed the effort budget, but the outline plus the executive summary is where the review's credibility is actually decided. Get those right and the rest is execution.
