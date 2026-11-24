# Lab 03 — Populate and Defend the Fluency Scorecard

**Duration:** 60–75 minutes
**Format:** guided hands-on — populate the scorecard with plausible numbers, draft the exec narrative, red-team against measurement failures
**Grounding chapters:** [07 — Measuring Fluency Growth](../07-measuring-fluency-growth.md), [02 — Audience Segmentation and Fluency Targets](../02-audience-segmentation-and-fluency-targets.md) (tier definitions the scorecard rows reflect)

## Objective

Take an **empty** fluency scorecard template, populate it with a plausible single-month snapshot, and draft the two-minute exec narrative you would use to walk the sponsor through it. Then red-team the artifact against Chapter 07's "common measurement failures" and revise.

This lab operates one layer below [Exercise 06](../exercises/exercise-06-fluency-growth-measurement-drill.md). Exercise 06 is explicit: "Scorecard numbers do not go in this exercise. The deliverable is the *template* — the thing the operations analyst fills every month." This lab is the complement: given the template, practice the fill and the read. The skill the lab trains is the exec-review move Chapter 07 names as the thing that defends budget year over year.

## Prerequisites

- Chapter 07 read, specifically *The measurement artifact — the fluency scorecard*, *Common measurement failures*, and *External benchmarks worth referencing (not citing as evidence)*. Chapter 02 skimmed (tier definitions).
- The scorecard template from [Exercise 06](../exercises/exercise-06-fluency-growth-measurement-drill.md) if you have done it; otherwise use the empty template in Setup below.
- A chosen organization — carry forward the one from earlier exercises if you have one.
- A blank markdown file.

## Why a lab, not an exercise

Exercise 06 ends with a template. A template is scaffolding; the skill is the exec read. Most literacy programs are cut not because the stack is unbuilt but because the enablement lead cannot walk the sponsor through it in two minutes without leading with attendance. Chapter 07 names five "common measurement failures" that reliably sink the exec review; a practiced fill and a rehearsed narrative are the cheapest version of that lesson.

## Setup

Open a file called `fluency-scorecard-populated.md` with this header and the empty scorecard below.

```markdown
# Fluency Scorecard — <organization>, <month>

**Owner:** operations analyst (per Chapter 07)
**Review cadence:** monthly CoE review; quarterly exec extract
**Scorecard version:** v0.1 (first populated cycle)
**Rubric versions referenced:** <list — Chapter 07 names rubric versioning as a scoring prerequisite>

| Segment | L1 completion | L2 knowledge avg | L3 rubric-meets % | L4 business-outcome delta | Open issues |
|---|---|---|---|---|---|
| **Leadership tier** | | | | | |
| **Operators tier** | | | | | |
| **Specialists tier** | | | | | |
| **Builders tier** | | | | | |
| Sales function | | | | | |
| Service function | | | | | |
| Operations function | | | | | |
| Finance function | | | | | |
| HR function | | | | | |
| Legal function | | | | | |

**Footer:** sources for L1 (LMS), L4 (function system of record), rubric version(s) scored against.
```

If your organization has fewer major functions in year one, trim rows. The scorecard is meant to be readable; a 20-row scorecard is an operational report, not an exec artifact.

---

## Step 1 — Populate with plausible numbers (20 min)

Fill the scorecard with a single-month snapshot. The numbers are plausible, not real — a mid-Y2 program at a mid-sized organization after the foundational curriculum has rolled out and two or three role-based playbooks are live.

Do not freestyle. Follow the four rules below so your numbers hang together.

### Rule 1 — L1 completion is high and plateauing

Chapter 07 names the L1 pass bar as "typically 80%" on the knowledge check, and treats L1 as the compliance layer. In a mid-Y2 program, completion against the in-scope roster has largely landed; 92–97% is a credible range. Variance across tiers typically reflects onboarding timing (leadership slower; operators faster because of cohort workshops; specialists often highest because of bootcamp).

- Pick a tier-level and function-level completion rate in the 85–98% band.
- Deliberately include **one row** with a visibly lower completion rate (e.g., 72%) — this is the lapsed-record or new-cohort row that becomes your Open-issues entry. A scorecard where every cell is green is not a believable scorecard.

### Rule 2 — L2 knowledge-check averages are close to the pass bar and relatively flat across tiers

Pass bar is 80%; average scores for a maintained item bank typically land in the 82–90% band. Variance across tiers is small; variance across functions is larger if item authoring is grounded in each function's policy artifacts. If a cell is wildly lower, mark it in Open issues as an item-bank audit trigger (Chapter 07: "audit for item bias (regional, functional) quarterly").

### Rule 3 — L3 rubric-meets percentage is the headline number and the one most likely to be sub-90%

L3 is the task-level proficiency rubric from Chapter 07. It is scored by the operator's manager or a specialist-tier contributor (not the trainer). In a mid-Y2 program, rubric-meets rates typically land in the 55–80% band — materially lower than L1 and L2 because actually meeting the rubric on named tasks is harder than passing the quiz. This is the number the exec review hinges on.

- Set tier-level and function-level L3 rates in the 55–80% band.
- Include at least one function clearly above 75% (the one with the oldest role-based playbook, most mature coaching cadence) and at least one clearly below 65% (a newer rollout).
- The leadership tier's L3 cell is often marked N/A — Chapter 07 names rubrics as unsuited to tasks where the output is a decision, a conversation, or a non-artifact. Leadership tier's fluency reads through L4 behavioral indicators, not through a rubric. If you mark N/A, state the Chapter-07 reason in the footer.

### Rule 4 — L4 business-outcome delta is a single number with the caveat baked in

Chapter 07 is explicit: L4 reads are claims, not direct measurements. Use a function-system-sourced delta (CRM for sales, service platform for service, financial system for finance) with the baseline window and the comparison window named.

- For each function with a live playbook, name one metric and the delta (e.g., "service: first-response time -18% vs. pre-playbook baseline, 90-day rolling window"; "sales: discovery-note production time -27%, same window").
- For functions without a live playbook, mark the cell "pending (no playbook live)." A scorecard that fakes L4 numbers for a function with no playbook is a scorecard that will fail the first time the exec asks about the baseline.
- Chapter 07 names the incident delta as a cluster that reads *both ways* — a trained population surfaces more small-case incidents because operators now recognize them. If your organization's incident rate is up, name it as a signal the training is working, not a signal it is failing; the open-issues column is where the nuance goes.

### Rule 5 — Open issues are specific, dated, and name the owner

Chapter 07's scorecard column reads "Open issues: lapsed records, failed rubric cohorts, incident signals." Specific example entries:

- "28 operators in Service lapsed on refresh after the acceptable-use policy update; HR partnership running the chase; target closed-out by `<date>`."
- "Sales function L3 rubric-meets dropped from 72% to 61% after the Q2 playbook revision; coaching clinic cadence doubled to biweekly; next read in 30 days."
- "Three Module-6 escalation signals from Service were not on the current list; added to v2 of the escalation roster; Module 6 refresh triggered."

An Open-issues column with "none" in every row is not a credible scorecard.

**Checkpoint 1 — do not proceed until all five are true:**

- [ ] Every cell is populated (or marked N/A with the Chapter-07 reason).
- [ ] L3 is visibly lower than L1 and L2 somewhere; the scorecard is not uniformly green.
- [ ] At least one function has L4 pending because the playbook is not yet live, and the scorecard says so.
- [ ] Rubric versions referenced are named in the header — Chapter 07 is explicit that rubric drift breaks pre/post comparability.
- [ ] Open issues are specific (named owner, date, closed-out trigger) on at least three rows.

---

## Step 2 — Draft the two-minute exec narrative (15 min)

The exec sponsor sees the scorecard for 90–120 seconds. You lead with the story they need to make the resource decision, not with the row at the top.

Write the narrative as a short block (160–220 words). Structure:

1. **The headline number** — the single L3 or L4 number that captures program impact this month. Not completion. Not satisfaction.
2. **The move** — what the number represents and against what baseline. One sentence.
3. **The two bright spots** — one tier and one function whose L3 or L4 moved materially. Name the specific delta and the specific move that produced it (role-workshop rollout, coaching clinic cadence, playbook revision).
4. **The one concern** — the row that moved the wrong direction and what the program is doing about it. Chapter 07 names this as the "one thing that moved the wrong direction" slot; hiding it is a credibility loss.
5. **The ask** — zero to one sentence, only if it is load-bearing this cycle.

Then write the **two questions you anticipate** the sponsor asking. Your scorecard should be answerable for both. If one is not, flag the row; the next month's priority is the gap.

**Checkpoint 2 — do not proceed until all three are true:**

- [ ] The headline is L3 or L4; completion appears only as context, if at all.
- [ ] The narrative names at least one wrong-direction row and the move being taken.
- [ ] You can read the narrative aloud in under 90 seconds; a longer narrative will not survive the exec meeting's compressed time.

---

## Step 3 — Red-team against Chapter 07's five failure modes (15 min)

Read the scorecard and the narrative aloud against Chapter 07's "common measurement failures." Any row or sentence that fails one of the five gets a `<!-- fix: ... -->` comment appended — do not silently paper over.

1. **Attendance as the headline check.** Does the narrative lead with attendance or completion? If yes, rewrite to lead with L3 or L4. Attendance is a cost metric; reporting it as the headline trains the sponsor to think of the program as an event series.
2. **Smile-sheets as the proxy for effectiveness check.** Does any row or sentence rely on satisfaction scores to defend a tier or function? If yes, remove — session satisfaction correlates weakly with behavior change per Chapter 07.
3. **No pre-assessment check.** Does the narrative name a *delta* or only a *level*? Deltas presuppose pre-assessments. If your scorecard reports only post-levels, add a note that the pre/post delta read lands next cycle and name the window.
4. **Rubrics scored by the trainer check.** For each L3 cell, name who scored the rubric. If any cell is scored by the trainer, the grader is motivated to score charitably — the row's credibility is compromised. Chapter 07: the operator's manager or a peer in the specialist tier is a more reliable grader.
5. **Benchmarks weaponized check.** Is Josh Bersin AI-in-L&D or Microsoft Work Trend Index data cited as a *target* anywhere on the scorecard? If yes, remove. Chapter 07: the denominators are not comparable. Reference them as context in the narrative, not as a scorecard row.

**Expected output of Step 3:** a short list — two to five items — of edits before this scorecard goes to the exec review. These are the real revisions the artifact needs to defend the program for another cycle.

---

## Step 4 — Freshness and handoff (5 min)

Add three short lines at the bottom of your file:

1. **Next-cycle changes.** Which open issues you expect to be closed out by the next monthly read; which metrics you expect to shift.
2. **Scorecard ownership transition.** Chapter 07 is explicit: the operations analyst maintains the scorecard; the enablement lead reviews it monthly; the exec sponsor sees the one-page extract quarterly. If your organization's ownership is different, name the divergence and the reason.
3. **Audit-walkthrough one-liner.** A single sentence summarizing how this month's scorecard answers the audit question "show me the program is proportionate and working" — the Article 4 proportionality defense per [mod-101 Chapter 05](../../mod-101-role-and-the-org-wide-enablement-operating-model/05-eu-ai-act-article-4-and-the-literacy-floor.md).

---

## Deliverable

- `fluency-scorecard-populated.md` — the populated scorecard, the two-minute narrative, the red-team comments, the three closing lines (next cycle, ownership, audit one-liner).

## Expected output shape

Roughly 2 pages at normal body-text size. One page is the table and the narrative; one page is the red-team comments and the closing lines. If your artifact is one page, the narrative is thin or the red-team pass has not surfaced edits yet; expand. If your artifact runs beyond three pages, you have drifted into writing a quarterly deck — the scorecard is a one-page artifact.

## Checkpoint — self-evaluation

- [ ] Every scorecard cell is populated or marked N/A with a Chapter-07 reason.
- [ ] L3 is visibly lower than L1 and L2 somewhere; L4 is "pending" for at least one function with no live playbook.
- [ ] Open issues are specific — named owner, named date, closed-out trigger — on at least three rows.
- [ ] The narrative is 160–220 words, leads with L3 or L4, and names one wrong-direction row.
- [ ] Red-team Step 3 produced at least two edits before this scorecard goes to the exec review — a scorecard that passes red-team on first draft either is unusually complete or has not been red-teamed hard enough.
- [ ] The audit one-liner names the Article 4 proportionality defense without weaponizing an external benchmark.

## Common failure modes

- **Uniform-green scorecard.** Every cell is above the bar. A credible scorecard surfaces a wrong-direction row and the move being taken on it. Chapter 07 is explicit that hiding the one bad row is a credibility loss.
- **L4 numbers invented for functions without a live playbook.** The exec will ask for the baseline; the scorecard will not have one. Mark "pending" instead.
- **Rubric version not named.** Chapter 07 is explicit that historical scores are reported against the version they were scored under. An un-named rubric version breaks pre/post comparability.
- **Narrative leads with completion.** Trains the sponsor to think of the program as an attendance operation. Lead with L3 or L4.
- **Bersin or Microsoft Work Trend Index cited as a target.** Chapter 07 permits "our shape is consistent with what Bersin / Microsoft identifies as high-performing" as context; "we beat the Microsoft benchmark" is not a defensible framing because the denominators are different.

## What this lab prepares you for

The fluency scorecard is the artifact that defends the program's budget year over year. Chapter 07 is explicit that programs measuring only L1 and L2 are the ones that get cut; programs that measure through L4 compound budget. Rehearsing the fill and the narrative builds the reflex the exec review runs on. The output of this lab also feeds [mod-106](../../mod-106-outcome-measurement-and-executive-reporting/README.md), where the fluency scorecard flows up into the executive scorecard the CFO reads; the narrative shape rehearsed here is the input shape that module expects.
