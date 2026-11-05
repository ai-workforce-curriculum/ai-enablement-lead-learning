# Exercise 05 — Tool Stack Consolidation Worked Example

**Estimated effort:** 2 hours
**Format:** stack inventory, consolidation economic case, and one-page executive-sponsor surfacing memo
**Grounding chapters:** [05 — Reconciling the Tool Stack Across BUs](../05-reconciling-the-tool-stack-across-bus.md), [01 — The Enablement Cost Model at Org Scope](../01-the-enablement-cost-model-at-org-scope.md), [02 — Projecting ROI with Confidence Bands](../02-projecting-roi-with-confidence-bands.md), [06 — The Vendor Vetting Rubric](../06-the-vendor-vetting-rubric.md)

## Objective

Build a complete stack-consolidation case for one chosen organization: the inventory grid, the overlap-pattern read, the consolidation economics (switching cost explicit), and the executive-sponsor surfacing memo that would carry the recommendation into leadership without stripping teams of working tools. The output is a decision-grade case that would land at the next stack-reconciliation cycle from [Chapter 05](../05-reconciling-the-tool-stack-across-bus.md).

## Prerequisites

- [Chapter 05](../05-reconciling-the-tool-stack-across-bus.md) read; the four structural causes of sprawl, the four overlap patterns, the consolidation economics, and the five surfacing principles close enough to cite without the chapter open.
- [Chapter 01](../01-the-enablement-cost-model-at-org-scope.md) read; the cost model is the ledger the consolidation case moves numbers on.
- [Chapter 02](../02-projecting-roi-with-confidence-bands.md) read; the consolidation case uses the ROI projection method applied to a consolidation move versus the status quo.
- [Chapter 06](../06-the-vendor-vetting-rubric.md) read; the vendor-concentration view keeps consolidation from becoming unmanaged concentration.
- One chosen organization — fictional-but-realistic is fine. The organization must have (a) at least three BUs running AI tools, (b) at least two overlapping tool deployments across BUs (for the consolidation case to have teeth), (c) at least one tool near a contract renewal. Carrying the organization from Exercises 01-03 produces a coherent bundle.

## Problem statement

Your annual stack inventory (the first cadence from [Chapter 05](../05-reconciling-the-tool-stack-across-bus.md)) has surfaced three overlap patterns that collectively represent an estimated 15-25% of total AI tool spend. The CFO has asked whether consolidation would produce material savings; the executive sponsor has asked you to surface a specific consolidation case at the next leadership review, with the caveat that any case must not strip BUs of tools they are actively depending on. Three BUs have independently signaled resistance to any "central team taking away our tool."

You have two hours (this exercise) to produce the consolidation case and the surfacing memo.

## Requirements

### Part A — the stack inventory grid

Produce a (task-category × BU × tool) grid for your chosen organization. At minimum:

- 5-8 task categories (drafting, summarization, meeting-notes, code assistance, retrieval/internal-search, support-ticket handling, sales-call intelligence, analyst/research, etc.).
- 3-6 BUs.
- Specific current-market tool names populated in each cell where a tool is live. Cells with no deployment are blank; cells with a pilot are marked with "(POC)".

The grid must exhibit at least three of the four overlap patterns from [Chapter 05](../05-reconciling-the-tool-stack-across-bus.md):

1. Platform add-on duplicates a standalone tool.
2. Same vendor across BUs with no shared contract.
3. Overlapping tools in the same category across BUs.
4. Pilot sprawl inside a single BU.

A short paragraph (3-5 sentences) names which patterns the grid exhibits and which cells they appear in.

### Part B — the consolidation economics for one chosen target

Pick one overlap to build the full consolidation case against. Typically Pattern 3 (overlapping tools in the same category across BUs) produces the richest case; Pattern 1 and Pattern 2 are often simpler. Pattern 4 is a Stage 3 decision from [mod-102 Chapter 01](../../mod-102-selecting-and-rolling-out-ai-tools/01-the-three-stage-selection-decision.md) rather than a consolidation case per se.

For the chosen target:

**Numerator — value of consolidation.**

- License-cost reduction: delta between fragmented list price and consolidated contract price, net of complexities (true-ups, mid-term uplifts). Quantify.
- Operating-cost reduction: Family 2, 3, 4, 5, 6 lines from [Chapter 01](../01-the-enablement-cost-model-at-org-scope.md) that reduce. Estimate with a band; be explicit that these are harder to quantify than license savings.
- Standardization benefits: qualitative, with specific instances where attributable.

**Denominator — cost of consolidation.**

- Switching cost: operator relearning, workflow redesign, data migration, integration rebuild, lost-productivity dip during transition. Model as a one-time cost over 3-6 months.
- Reduced optionality: priced as expected cost of vendor-swap-under-duress × probability of needing to swap.
- Local-optimum sacrifice: if a BU was on a tool that genuinely fit its workflow better, the workflow-fit delta is a real cost. Measure or state the measurement plan ([mod-106 Chapter 01](../../mod-106-outcome-measurement-and-executive-reporting/01-the-measurement-stack-at-org-scope.md)).

**Crossover.** The horizon at which net value exceeds switching cost. Two years is the honest default; shorter horizons require explicit defence.

**Bands and sensitivity.** The consolidation case ROI with a composed band (per [Chapter 02](../02-projecting-roi-with-confidence-bands.md)) and a sensitivity analysis on the two most impactful assumptions (typically the per-seat price improvement and the lost-productivity dip during transition).

### Part C — the vendor-concentration check

A short paragraph (3-5 sentences) running the consolidation target through the vendor-concentration lens from [Chapter 06](../06-the-vendor-vetting-rubric.md). After the consolidation lands:

- How many vendors would be in the portfolio?
- How much spend would be on the top one / three / five vendors?
- How many tools would be single-sourced?
- Does the consolidation shift the portfolio into concentration risk?

If consolidation would increase concentration beyond the organization's comfort, name the trade and justify.

### Part D — the executive-sponsor surfacing memo

A one-page memo (roughly 400-600 words) that would carry the recommendation to the executive sponsor. Structure:

- **BLUF.** The consolidation move, the net value with band, the crossover horizon. One or two sentences.
- **What is being consolidated.** The specific tools, the specific BUs. Name the tools.
- **What the move preserves.** The local-optimum sacrifice, the exceptions the writeup permits, the champions carried forward. This is the section that keeps the memo from reading as a mass tool removal.
- **The economics.** Numerator, denominator, crossover, sensitivity. Two to three sentences.
- **The transition timeline.** 6-12 months is typical; longer for complex tools. Name the specific steps.
- **The decision requested.** What the sponsor is being asked to approve; what the alternative (status quo) looks like.
- **The dependencies.** What has to be true for the move to succeed — specific Procurement renewal timing, specific IT support bandwidth, specific communication investment.

### Part E — the five-principle self-check

A short paragraph (3-5 sentences) stating whether the memo and the economic case satisfy each of the five surfacing principles from [Chapter 05](../05-reconciling-the-tool-stack-across-bus.md):

1. Surface to leadership, not to operators first. (Is the memo for the sponsor, with operator-level communication a downstream artifact?)
2. Carry the local-optimum sacrifice on the writeup. (Is the sacrifice named, not hidden?)
3. Timeline the transition deliberately. (Is a 6-12 month plan specified?)
4. Protect the champion network across the transition. (Are the champions re-skilled and carried forward?)
5. Leave exceptions where they are earned. (Are documented exceptions permitted, not denied?)

For any principle not satisfied, revise before finalizing.

## Starter guidance

- The grid is the readability instrument. Populate it with specific current-market tools (Gong, Chorus, M365 Copilot, GitHub Copilot, Cursor, Claude, Glean, Harvey — whatever is in-scope for your task families). The grid must be readable in seconds; abstract "Tool A, Tool B" labels defeat the exercise.
- Choose a consolidation target with real teeth but not infinite scope. Consolidating two tools across three BUs is a tractable case; consolidating the entire stack is a career-defining move that will not fit in this exercise.
- License-cost reduction is the easy numerator; operating-cost reduction is harder and often undervalued. Running the Family 2-6 lines from Exercise 01 through the consolidation lens produces numbers the writeup should carry. Operating-cost reduction from retired tools is often 20-40% of the license-cost reduction.
- Switching cost is routinely undervalued in consolidation writeups. 3-6 months of productivity dip for operators learning the new tool at fully-loaded cost across the affected cohort is typically the largest single line in the denominator. Honest switching cost makes the case harder to win but more credible.
- The local-optimum sacrifice section is where the memo wins or loses. A BU that is genuinely on a better-fitting tool and is being asked to move will push back; the writeup that names this and either permits an exception or justifies the sacrifice is more durable than the writeup that pretends the sacrifice does not exist.
- The transition timeline is where credibility sits. A 6-12 month timeline looks slow in the writeup but is realistic. A "consolidation effective next quarter" timeline is a change-management failure in slow motion; the memo should carry the honest timeline.
- The champion-carry language in the surfacing memo is small-footprint but load-bearing. Champions who became expert on the retired tool are the first to feel undermined; the memo should name that they are re-skilled on the consolidation target, not released.
- The vendor-concentration check is the discipline that keeps consolidation from producing unmanaged concentration. A consolidation that collapses three vendors into one in a single category is correct in isolation but may be concentration risk in portfolio context. Name the trade.

## Deliverables

- `stack-inventory.md` containing Parts A and the pattern-read paragraph.
- `consolidation-case.md` containing Parts B, C, and E.
- `sponsor-memo.md` containing Part D.

## Acceptance criteria

- The inventory grid has at least 5 task categories, 3 BUs, and specific current-market tool names populated.
- The pattern-read paragraph names at least three overlap patterns and the cells where they appear.
- The consolidation economics case carries all three numerator components, all three denominator components, a crossover horizon, and a sensitivity analysis.
- The ROI band on the consolidation case is composed per [Chapter 02](../02-projecting-roi-with-confidence-bands.md) and is not a point estimate.
- The vendor-concentration check names portfolio-level concentration before and after consolidation.
- The surfacing memo fits on one page and includes all seven required sections.
- The memo explicitly names the local-optimum sacrifice, the champion-carry language, and the transition timeline.
- The five-principle self-check addresses each principle; where any principle is not satisfied, the case has been revised.
- The memo is in a form the executive sponsor could reasonably sign off on for next-quarter action.

## Stretch goals

- Produce a second version of the surfacing memo rewritten from the perspective of the BU whose tool is being retired. The exercise is in reading your own memo from the losing side; if the retired-tool BU would reject the memo on fairness grounds, the memo is not ready.
- Draft the operator-level communication that would roll out six weeks before the consolidation takes effect. This is the artifact that converts the sponsor's approval into an executable change. Structure: what is changing, why, what is preserved, what to do by when, who to contact.
- Run the consolidation case against a second overlap pattern from the grid to produce a two-case bundle for the sponsor. Sponsors typically prefer a slate of consolidation moves to choose from over a single all-or-nothing proposal; the bundle shape is more realistic to how these decisions land.

## Why this exercise matters

Stack consolidation is the place where enablement leaders most often lose the room. A consolidation case that is economically correct but surfacing-naive produces operator resistance that stalls the move for quarters. A consolidation case that is surfacing-smart but economically weak produces a case the CFO will not sign. The exercise is in holding both at once: the economics rigorous, the surfacing careful, the local-optimum sacrifice named, the champions carried, the exceptions permitted. This is the artifact that converts "the central team is funding five overlapping copilots" from a quiet problem into a managed one.
