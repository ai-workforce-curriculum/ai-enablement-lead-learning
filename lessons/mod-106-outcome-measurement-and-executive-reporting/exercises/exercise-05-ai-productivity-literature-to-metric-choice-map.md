# Exercise 05 — AI Productivity Literature to Metric Choice Map

**Estimated effort:** 3 hours
**Format:** mapping table plus short per-paper methodology notes, Markdown
**Grounding chapters:** [04 — Reading the Empirical AI Productivity Literature for Method, Not Numbers](../04-reading-the-empirical-ai-productivity-literature-for-method-not-numbers.md), [01 — The Measurement Stack at Org Scope](../01-the-measurement-stack-at-org-scope.md)

## Objective

Read the empirical AI productivity literature as a working methodology toolkit for your own scorecard — not as a source of numbers to transplant. Produce the mapping table from each paper to the specific methodology moves you will use in your portfolio's measurement, and write a short defence of each choice. The output is the methodology appendix that sits behind your quarterly review from [Chapter 02](../02-authoring-the-executive-scorecard-weekly-monthly-quarterly.md) section 6.

## Prerequisites

- [Chapter 04](../04-reading-the-empirical-ai-productivity-literature-for-method-not-numbers.md) read, with the five transferable methodology patterns and the five threats to validity close enough to cite without the chapter open.
- At least the abstract and method sections of each of the five primary papers read (full-read on at least one). Links in [resources.md](../resources.md).
- A sketched portfolio of at least four rollouts across at least two task families (see Exercise 01). The portfolio is what the methodology choices will be made against.

## Problem statement

Your CFO has pushed back on the ROI number in last quarter's review. The pushback is not that the number is wrong; the pushback is that the methodology appendix was thin and "could have been written by the vendor." You have been asked to produce a serious methodology section — citing published work and defending your methodological choices on their merits — for the current quarter's review.

The expectation from the CAIO is: by the end of the current quarter, every portfolio-level measurement choice in the scorecard is traceable to a published method, with the choice defensible on its own.

## Requirements

### Part A — the mapping table

Produce a table with these columns:

| Paper | Published task / context | Transferable methodology move | Where it lands in your scorecard | Choice confidence |

One row per paper, five rows total:

- **Peng et al. 2023** — "The Impact of AI on Developer Productivity: Evidence from GitHub Copilot" (arXiv:2302.06590).
- **Ziegler et al.** — "Measuring GitHub Copilot's Impact on Productivity" (Communications of the ACM).
- **Noy & Zhang 2023** — "Experimental Evidence on the Productivity Effects of Generative Artificial Intelligence" (Science).
- **Brynjolfsson, Li, Raymond** — "Generative AI at Work" (NBER working paper 31161).
- **Dell'Acqua et al.** — "Navigating the Jagged Technological Frontier" (HBS working paper 24-013).

The "transferable methodology move" is a specific move — not "measure productivity" but "pre-register the primary outcome metric with a secondary quality metric, following Noy & Zhang's two-dimensional structure." The "where it lands in your scorecard" is a specific slot — not "general methodology" but "Section 2 drafting-workflow rollup, which carries a quality outcome alongside time-per-draft because of this pattern."

Choice confidence is one of: *strong fit, partial fit, aspirational*. A strong fit means your portfolio can execute the move today; a partial fit means you can do most of it but not all; aspirational means the move is a next-quarter commitment, not a current one.

### Part B — per-paper methodology notes

For each paper, 100-200 words of written notes covering:

- The one method-level move you are borrowing.
- One concrete difference between the paper's context and your portfolio, and why the move still transfers across the difference.
- One concrete threat to validity from [Chapter 04](../04-reading-the-empirical-ai-productivity-literature-for-method-not-numbers.md) that this move helps you defend against.
- A one-sentence editorial note: how you would cite this move in the quarterly review's methodology appendix.

### Part C — the five-pattern inventory

A short section at the end of the file listing all five Chapter 04 methodology patterns (pre-registered outcome, two-dimensional, longitudinal, decomposition by sub-population, field over lab) with a one-sentence note on whether each is being executed in your portfolio today, and if not, which quarterly review you commit to introducing it.

## Starter guidance

- The mapping is not a literature review. It is a working appendix. Keep each cell concrete and portfolio-specific; a cell that could be in anyone's appendix is a cell that has not been thought through.
- The Peng-Ziegler pair is one entry in the mapping and two rows in the table. Peng is the primary study; Ziegler is the measurement-validity companion that sharpens Peng's claims. If your rollouts include a coding assistant, both rows should land in the scorecard; if not, both can still inform the general discipline of measurement validity.
- Resist the move to borrow published effect sizes. If your table has a cell that says "target 55% reduction (per Peng)," you have fallen into the vendor-number-headline pattern from [Chapter 01](../01-the-measurement-stack-at-org-scope.md). Published effect sizes inform your choice of *target range* at most, not your target number.
- Dell'Acqua's jagged-frontier finding often maps to the decomposition-by-sub-population pattern — your portfolio-level outcome rollup should decompose by task type where the data allows, and the mapping table is where you commit to doing so.
- The Brynjolfsson longitudinal pattern is the hardest to execute today; many portfolios have not been live long enough to have a six-month trajectory. Marking it *aspirational* is honest; marking it *strong fit* when you have three months of data is theatre.
- Noy & Zhang's heterogeneous-effects-by-skill finding deserves a specific slot in your scorecard. If your portfolio has not decomposed by skill or tenure, this is the exercise where you commit to adding the decomposition.

## Deliverables

- `literature-to-metric-map.md` containing:
  - Part A — the mapping table.
  - Part B — five sets of per-paper methodology notes.
  - Part C — the five-pattern inventory with commitments by quarter.

## Acceptance criteria

- The mapping table has five rows and five columns, with every cell populated (no "N/A," no blank cells; use "aspirational" with a committed quarter if the move is not current).
- Each "transferable methodology move" is specific (names the pattern or structure being borrowed, not just a topic).
- Each "where it lands in your scorecard" names a specific slot in a specific section of the scorecard (e.g., "Section 2 drafting-workflow rollup," not "methodology appendix").
- Each per-paper note names at least one threat to validity the move defends against, drawn from the Chapter 04 list.
- No published effect size is transplanted as a target in your portfolio.
- The five-pattern inventory states the current status (executed today / partial / aspirational) honestly. Marking all five as "executed today" is almost certainly dishonest for most portfolios at this stage.
- Each aspirational pattern has a committed quarter for introduction; "someday" does not count.

## Stretch goals

- Expand the mapping table to include Ziegler as a separate row from Peng, specifically addressing measurement-validity work (the Chapter 04 Pattern 1 discipline). The Ziegler methodology — construct validity for proxy measures — is the single most under-cited move in enablement-program methodology appendices.
- Write the *methodology appendix* section of the quarterly review (two to three pages) that this mapping produces. The appendix is the artifact your CFO will actually read on the pushback; the mapping is the private tool that makes the appendix defensible.
- Draft a one-page memo to your sponsor on which of the five Chapter 04 patterns is the most expensive to introduce (usually the longitudinal pattern, requiring six-month trajectories) and what capability investment the enablement function needs to execute it next year.

## Why this exercise matters

Every executive who has run a budget meeting with a data-driven function has seen the pattern of program leaders citing published studies as evidence while borrowing none of the method. The AI productivity literature is especially vulnerable to this failure because the headline numbers are large and the method sections are not. Doing this exercise is doing the work the methodology appendix *should* make visible: showing which published methods you are actually using, honestly, with the gaps named as commitments rather than hidden. This is what moves a scorecard from being a performative artifact to being a credible one.
