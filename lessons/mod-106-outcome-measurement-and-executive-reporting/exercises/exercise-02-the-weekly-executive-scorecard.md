# Exercise 02 — The Weekly Executive Scorecard

**Estimated effort:** 3 hours
**Format:** one-page Markdown document styled as a weekly rollup, with a brief authoring note
**Grounding chapters:** [01 — The Measurement Stack at Org Scope](../01-the-measurement-stack-at-org-scope.md), [02 — Authoring the Executive Scorecard — Weekly, Monthly, Quarterly](../02-authoring-the-executive-scorecard-weekly-monthly-quarterly.md)

## Objective

Produce a real, usable weekly rollup — one page, five fixed sections in order — for a portfolio of four to six concurrent rollouts in your chosen organization. The weekly rollup is the operating artifact, not the executive artifact; the discipline of this exercise is to write it tightly enough that an operating circle can act on it on Monday, and to resist the temptation to pad it into monthly-deep-dive altitude.

## Prerequisites

- [Chapter 01](../01-the-measurement-stack-at-org-scope.md) read, with the three measurement layers in priority order.
- [Chapter 02](../02-authoring-the-executive-scorecard-weekly-monthly-quarterly.md) read, with the five-section weekly-rollup structure available for reference.
- Exercise 01 ideally completed on the same organization; if you did not do Exercise 01, sketch the portfolio briefly before starting (four to six rollouts, at least two task families, at least two business units) so the weekly rollup has real material to land on.

## Problem statement

You are the AI Enablement Lead at your chosen organization. It is Friday. You need to produce this week's rollup for Monday's operating meeting: the enablement lead, the governance analyst, the lead analyst, the L&D partner, two team managers, and an L50 governance architect. The audience allocates next week's attention based on what you put on this page. Last week's rollup is in the thread; this week's rollup picks up where last week's left off and adds the week's signal.

The scene is: the portfolio has run for roughly six months. Three of the rollouts are mature (live for 90+ days, outcome metrics running), two are in early rollout (30-60 days in, outcome metrics just starting to produce signal), and one is a pilot that is about to graduate. At least one outcome metric is missing its target this week; you have to decide how to write that up without turning the rollup into a crisis document.

## Requirements

Produce the one-page weekly rollup with the five sections from [Chapter 02](../02-authoring-the-executive-scorecard-weekly-monthly-quarterly.md), in order, with no re-ordering:

1. **Outcome movements this week.** For each live rollout, one line: outcome metric, directional move, baseline, current value. Missing-this-week values are stated as such with the next refresh date.
2. **Workflow-interview signals this week.** Three to five anonymized quotes or patterns from the week's interviews. If no interviews ran, write that; do not pad.
3. **Usage telemetry — floor check.** One line per rollout: *healthy / flat / declining*. No percentages as headlines.
4. **Risks and misses.** Every outcome below target *this week*, named, with a one-sentence reason. At least one miss must appear, honestly stated.
5. **Next week's attention allocation.** Three bullets at most. Specific operational commitments for the following week.

After the rollup, add a short authoring note (not part of the rollup itself) of three to five sentences:

- Which section was hardest to write honestly, and why.
- Which section is most likely to get skimmed, and what you did to keep the signal in it anyway.
- One editorial choice you made that you expect pushback on (ordering, framing, inclusion, exclusion), and the Chapter 01 or Chapter 02 principle you grounded that choice in.

## Starter guidance

- The weekly rollup is dense. A reader should be able to read the whole page in under two minutes and come out knowing what to do differently next week. If your draft is longer than one page, cut; if it reads thin, you have under-specified the portfolio.
- Outcome movements do not need to be dramatic to be reportable. "Flat against baseline, as expected during the training-propagation phase" is a credible line if it is honest; "exceeded target by 3%" when the measurement cycle does not support that precision is not.
- At least one workflow-interview signal should cut *against* the aggregate numbers. If all the qualitative signals confirm the dashboard, you are reading the transcripts for confirmation, not for signal. See the [Chapter 01](../01-the-measurement-stack-at-org-scope.md) qualitative ground-truth discipline.
- The miss needs to be named. Be specific — "Legal drafting rollout — median time-to-first-draft flat vs. target 20% reduction; new-matter workflow fit is suspected cause, investigation opens next week." Do not write "Legal rollout faced challenges."
- "Next week's attention allocation" is where this rollup converts into operating work. Each bullet names a rollout, an action, and an owner — not a vague priority.
- Keep adoption percentages off this page. If you catch yourself writing "73% active users," ask whether that number answers a decision the Monday meeting is making. It probably does not.

## Deliverables

- `weekly-rollup.md`: the one-page weekly rollup in the five-section structure.
- A short authoring note at the end of the same file, under the heading "Authoring note."

## Acceptance criteria

- The rollup fits on one page at normal font size (roughly 500-700 words in the rollup section; the authoring note is separate).
- All five sections appear in the specified order with the specified headings. Re-ordering the sections fails the exercise.
- Section 1 does not open with a usage percentage or an adoption number.
- Section 2 contains at least one qualitative signal that cuts against or sharpens a quantitative signal in section 1 (not just confirms it).
- Section 4 contains at least one *honest* miss. A rollup where every metric is on target is either lying or mis-specifying the targets.
- Section 5 is at most three bullets and each bullet names a rollout, an action, and an owner.
- No vendor-reported productivity numbers appear in the rollup.
- The authoring note names the hardest section honestly and cites a specific chapter principle for one editorial choice.

## Stretch goals

- Produce a second weekly rollup one week later (the imaginary "next week"). The second rollup must honour the "next week's attention allocation" from the first — the actions you committed to must appear as outcomes in the second rollup, succeeded or failed. This is where the weekly cadence stops being a writing exercise and starts being an operating discipline.
- Write a one-paragraph note to yourself as the enablement lead on which section of the rollup drifts first when calendar pressure rises. Most leads find that the workflow-interview section or the authoring-note discipline is where the compression lands. Naming your own drift pattern is how it stops being invisible.
- Draft the intake brief a new team manager would need to contribute their team's outcome line to next week's rollup — what they need to report, by when, in what format. This becomes a reusable interface artifact (consistent with the handoff cadence in [Chapter 06](../06-coordinating-with-the-analyst-and-the-team-manager.md)).

## Why this exercise matters

The weekly rollup is the smallest unit of scorecard credibility. A program that cannot produce an honest one-page weekly rollup is a program whose monthly deep-dive is already starting from a weaker base. The skill is picking the right six or seven lines of signal out of the dozens of things that happened this week, resisting the compression into vanity numbers, and keeping the miss section honest even when no one will read it. Done every week, the rollup becomes the paper trail that makes the quarterly review defensible; done inconsistently or dishonestly, the quarterly review is writing its own story from scratch.
