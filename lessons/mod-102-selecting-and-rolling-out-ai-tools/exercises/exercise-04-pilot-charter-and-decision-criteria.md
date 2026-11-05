# Exercise 04 — Pilot Charter and Decision Criteria

**Estimated effort:** 3 hours
**Format:** one-page pilot charter, Markdown or docx
**Grounding chapters:** [02 — Designing Bounded Pilots](../02-designing-bounded-pilots.md)

## Objective

Write the one-page pilot charter you would sign *before* a pilot of a specific AI tool starts at a specific organization. The charter must be:

- *Bounded* — a named cohort, a named duration, a named baseline.
- *Pre-committed* — the adopt / extend / kill criteria written now, not after the data arrives.
- *Externally replayable* — concrete enough that a reasonable external reader could apply the criteria to the end-of-pilot data and reach the same conclusion you would.

## Prerequisites

- Chapter 02 read.
- A specific AI tool and a specific target task in mind. If you do not have one in front of you, pick one of:
  - a general-purpose coding assistant for a 40-engineer backend squad at a SaaS company
  - a drafting-grade summarization tool for the retail-banking contact-centre quality-assurance team at a 3,000-person bank
  - a research-brief tool for the medical-affairs writers at a 12,000-person pharma
- *Strongly recommended:* the organization you chose for [Exercise 01](../../mod-101-role-and-the-org-wide-enablement-operating-model/exercises/exercise-01-the-one-page-role-scope-contract.md). Carrying the same org through both exercises gives you a realistic picture of where the scope contract constrains the pilot design.

## Problem statement

Your governance partner has cleared the tool for a bounded pilot and the vendor contract is in draft. Your boss's boss wants "the one-pager that says who, how long, what you're measuring, and how you'll decide" before procurement is signed. The ask is deliberately pre-launch: the whole point is that the criteria are written *before* you see the data.

You have the weekend.

## Requirements

Deliver a single page with the five sections named in Chapter 02:

1. **Cohort** — the named roles and headcount, the selection rationale, and a representativeness argument (or an explicit statement of what the cohort is *not* representative of — if these are friendly users, name it).
2. **Duration** — a start date, an end date, and a named mid-pilot check date. If the duration is longer than eight weeks, justify it.
3. **Baseline** — what you are measuring before launch, how it is being captured, and the measurement window. Name the specific task, the specific metric, and the specific capture mechanism (survey, timing study, ticket volume, telemetry export, etc.).
4. **Decision criteria** — three criteria, written as triggers:
   - *adopt* — concrete conditions under which you expand to the next cohort.
   - *extend* — concrete conditions under which you continue the pilot without expanding, *with a named ceiling*. "Extend" is not open-ended; you cannot extend forever. Six weeks maximum is a reasonable cap.
   - *kill* — concrete conditions under which you stop and do not pursue adoption.
5. **Kill switch** — the named conditions under which the pilot is stopped *mid-flight*, not at the end. These are the "we abort now" triggers — security incidents, policy violations above a threshold, data-handling breaches, measured harm.

Append to the charter:

- A short **representativeness check** paragraph (3–5 sentences) explaining why this cohort is a reasonable proxy for the broader population you would roll out to next — or an explicit acknowledgement of where it is not, and what you are deferring to a later pilot to find out.
- A two-sentence **inconclusive-outcome plan** naming what you will do if the pilot ends without hitting any of the adopt / extend / kill triggers. Chapter 02 forbids the sentence "the pilot went well" as a conclusion; write the sentence that goes in its place.

## Starter guidance

- The adopt / extend / kill triggers are the hard part. Fight the instinct to write them in prose. A criterion should be legible as a single conditional: *if measured metric X crosses threshold Y in window Z, then decision D.* "Adopt if users like it" is not a criterion. "Adopt if the median time-to-first-draft on the target task falls by at least 20% in the pilot cohort versus baseline AND the use-policy-violation rate from the governance usage review is zero" is a criterion.
- Write the baseline *measurement mechanism* with the same seriousness as the metric itself. "We will measure time-to-first-draft via a two-week timing study of the current workflow, logged in the team's existing ticket tool, sampled across at least 30 instances per writer" is useful. "We will measure time-to-first-draft" is not.
- The kill switch is not the same as the kill criterion. The kill *criterion* fires at end of pilot. The kill *switch* fires mid-flight. Name both.
- The "extend" pathway is the most frequently abused one in real orgs. It is the comfortable answer when neither adopt nor kill is clean. Write its ceiling and its exit condition explicitly, so that at ceiling + 1 day you are forced back into adopt or kill.
- Your representativeness paragraph should pass a hostile reader. If the cohort is friendly early adopters, *say so*, and name what you are deferring to the next pilot (skeptics, regulated workflows, cross-functional handoffs, non-English users, whatever applies).
- Resist the urge to describe the *rollout* in this document. The charter is about the pilot. The rollout artifact set is [Exercise 05](exercise-05-rollout-artifact-set-dry-run.md).

## Deliverables

- `pilot-charter.md` (or `.docx`): one page, five sections above, plus the two appended paragraphs (representativeness check and inconclusive-outcome plan).
- A short appended note (no more than 3 sentences) naming the single criterion you expect to be most contested in the pre-pilot review, and why.

## Acceptance criteria

- The charter is one page at normal body-text size. If it spills onto two, you are writing a project plan — cut.
- All five required sections are present and named.
- Adopt, extend, and kill are each written as concrete triggers with named metrics, named thresholds, and a named measurement window. A reader who did not write the charter could take your end-of-pilot dataset and independently apply the criteria.
- Extend has a named ceiling.
- The kill switch is distinct from the kill criterion and names at least one mid-flight condition.
- The representativeness paragraph is honest about what the cohort is and is not.
- The inconclusive-outcome plan exists and is two sentences. The phrase "the pilot went well" does not appear in the document.
- Organization and tool specificity is visible. A reader who knows the chosen org should be able to tell you wrote this *for them*.

## Stretch goals

- Write a 100-word *opening paragraph* for the charter — the first thing your governance partner and your boss's boss read. One sentence on the tool and the task, one on the cohort and duration, one on the single most important decision criterion.
- Add a *pre-mortem bullet list*: three concrete ways this pilot could fail that are not already covered by the kill switch, and what early signal you would look for in each case. (This is the Chapter 05 move, pulled forward.)
- Draft the three-line executive summary you would send at the mid-pilot check date for each of the three outcomes (tracking-to-adopt, tracking-to-extend, tracking-to-kill), using only the metrics from your baseline section. If you cannot write all three with the metrics you chose, your baseline section is under-specified — go back and fix it.

## Why this exercise matters

The pilot charter is the artifact that stops "the pilot went well" from being a sentence anyone is allowed to say. Writing the criteria *before* the data arrives is the only honest way to do a pilot — once you have the numbers, it is almost impossible not to rationalize toward the decision you were already going to make. Doing this once as a dry run, with no real money on the line, gives you a template and a set of reflexes you can drop into a real pilot in week one of the role.
