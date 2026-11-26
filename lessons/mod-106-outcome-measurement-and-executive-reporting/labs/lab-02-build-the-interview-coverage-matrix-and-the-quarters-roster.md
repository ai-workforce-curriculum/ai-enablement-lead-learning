# Lab 02 — Build the Role × BU × Tool Interview Coverage Matrix and the Quarter's Interview Roster

**Duration:** 60–75 minutes
**Format:** guided hands-on — matrix construction + gap diagnosis + roster scheduling + red-team pass
**Grounding chapters:** [01 — The Measurement Stack at Org Scope](../01-the-measurement-stack-at-org-scope.md), [06 — Coordinating with the Analyst and the Team Manager](../06-coordinating-with-the-analyst-and-the-team-manager.md)

## Objective

Produce two operating artifacts for the Chapter 01 Layer 2 qualitative ground-truth discipline: the **role × BU × tool coverage matrix** (which rollout family in which business unit is on which interview cadence right now), and the **quarter's interview roster** (which operators in which rollouts will be interviewed, by whom, on what dates, against which four questions). Together they convert the "quarterly workflow interviews" line in your framework from an aspiration into a calendar with names on it. By the end of the lab, no rollout live for 90 days is sitting in a blank cell without a flagged risk, and the coming quarter has a signed roster the team-manager working group can commit to.

## Prerequisites

- [Chapter 01](../01-the-measurement-stack-at-org-scope.md) read, with the role × BU × tool coverage matrix, the four interview questions, and the three rules for keeping the qualitative layer honest (enablement lead reads transcripts personally; anonymize at ingest; quote in the scorecard carefully) available for reference.
- [Chapter 06](../06-coordinating-with-the-analyst-and-the-team-manager.md) read; the team-manager-interface section is where the BU-level coverage gets staffed.
- A sketched portfolio: four to eight rollouts across at least two task families and at least three business units. If you did Exercise 01 or Exercise 02, carry that portfolio forward.
- A blank working file — `interview-coverage.md`.

## Why a lab, not an exercise

The module's exercises assume that the qualitative-ground-truth layer is populated — [Exercise 02](../exercises/exercise-02-the-weekly-executive-scorecard.md) Section 2 reads "three to five anonymized quotes from this week's interviews," [Exercise 03](../exercises/exercise-03-quarterly-board-ready-review-outline.md) Section 5 carries "two or three pattern findings from the quarter's interviews," [Exercise 04](../exercises/exercise-04-metric-miss-narrative-drill.md) Vignette A's diagnosis is "confirmed in 6 of 8 interviews." None of them builds the matrix or the roster that *produces* those interviews. This lab is that layer. When a lead reaches Exercise 02 and realizes they do not know which operators were interviewed this quarter — or whether any were — this lab is where that gap gets closed.

## Setup

Open `interview-coverage.md` and paste this skeleton. You will fill it in as you walk Steps 1–5.

```markdown
# Interview Coverage Matrix and Q<N> Roster — v0.1 (draft)

**Owner:** AI Enablement Lead — <your-name>
**Analyst partner:** <analyst-name>
**Team-manager partners:** <list>
**Review cadence:** matrix refreshed monthly; roster locked at quarter-start.

## 1. Portfolio snapshot

## 2. The coverage matrix (current state)

## 3. Gap diagnosis

## 4. Q<N> interview roster

## 5. The four questions and the anonymization protocol

## 6. Red-team notes
```

---

## Step 1 — Portfolio snapshot (5 min)

In Section 1, list the rollouts the matrix will cover. For each rollout, one line:

- **Rollout name** (workflow, not tool — carry the Lab 01 discipline).
- **Task family** — one of: drafting, summarization, meeting-notes, support-ticket resolution, code review, retrieval, analyst research. Chapter 01 names these; use the vocabulary as-is for comparability across your own portfolio and against the literature from [Chapter 04](../04-reading-the-empirical-ai-productivity-literature-for-method-not-numbers.md).
- **Business units in scope** — the BU codes or names.
- **Days-since-GA** — a rough integer. Chapter 01's rule: a rollout live for 90 days without a cell on the matrix is a flagged risk.

The snapshot is the row-and-column source for Step 2's matrix; keep it short — seven to twelve lines total. If your portfolio has more than twelve rollouts, you are measuring at a scale that this lab's single matrix cannot carry; split by task-family region and run the lab twice.

### Checkpoint 1 — before Step 2

- [ ] Section 1 has one line per rollout, each line stating the four items above.
- [ ] Rollout names are workflows, not tool names.
- [ ] Every rollout has a days-since-GA number, even approximate.

---

## Step 2 — Draw the matrix (10 min)

In Section 2, draw the coverage matrix. Rows are **task-family groupings**, columns are **business units**, cells are the current **interview cadence** for that (task-family, BU) intersection.

The matrix shape from Chapter 01, extended across your portfolio:

```
                        | BU-A        | BU-B        | BU-C        | BU-D        |
------------------------+-------------+-------------+-------------+-------------+
Drafting                |             |             |             |             |
Summarization / notes   |             |             |             |             |
Support ticket          |             |             |             |             |
Code review             |             |             |             |             |
Retrieval / search      |             |             |             |             |
Analyst research        |             |             |             |             |
```

Add rows only for task families that appear in Section 1; drop the ones that do not. Add columns only for BUs that appear.

Fill the cells using one of five labels:

- **monthly** — the (task-family, BU) intersection has an interview running every month this quarter.
- **quarterly** — one interview wave in the quarter, typically weeks 4–8.
- **—** (em-dash) — no rollout live in this intersection; the cell is correctly blank.
- **GAP** — a rollout *is* live in this intersection *and* no interview is scheduled; this is what Chapter 01 names as a flagged risk, not a quiet success.
- **ad-hoc** — a non-standing cadence, e.g., investigation-driven. Chapter 01's qualitative discipline treats ad-hoc as a weaker-than-quarterly standing — allowed, but worth upgrading if the rollout matters at the scorecard altitude.

Honesty check: at least one cell on your matrix should be **GAP**. A matrix with every rollout on a monthly or quarterly cadence either describes an unusually mature program or (more likely) under-reports its gaps. Chapter 01 names blank cells as known gaps *to be published*, not quiet successes; the discipline is on the scorecard precisely because the under-reporting is the common failure.

### Checkpoint 2 — before Step 3

- [ ] Rows and columns match the portfolio snapshot — no orphan rows, no orphan columns.
- [ ] Every cell has one of the five labels; no cell is left genuinely blank.
- [ ] At least one cell is **GAP**; a matrix with zero gaps goes back to Step 2 for a more honest re-read.

---

## Step 3 — Gap diagnosis (10 min)

For every **GAP** cell in Section 2, write one short entry in Section 3:

- **Which rollout.** Name it; a cell labeled "drafting / BU-C" is not specific enough until you name the rollout within it.
- **Days-since-GA for the rollout.** From Section 1.
- **Why the gap exists.** One of: (a) no team manager assigned to the BU for this rollout; (b) champion network in the BU has gone quiet (per [mod-105 Chapter 07](../../mod-105-champion-networks-and-change-management/07-measuring-change-management-health.md)); (c) HR/Legal has not signed off on operator-level interviews in this BU; (d) analyst's qualitative-data pipeline for this BU is not yet instrumented ([Chapter 06](../06-coordinating-with-the-analyst-and-the-team-manager.md) data-governance surface); (e) the rollout is pre-GA and the gap is pre-timing, not under-investment.
- **Severity.** Chapter 01 says a rollout live for 90+ days with a GAP cell is a *flagged risk*. Mark severity as **flagged** (90+ days-since-GA) or **monitored** (<90 days).
- **Action.** The specific move that closes the gap this quarter — a named team manager, an HR sign-off ask, an analyst-pipeline build on Lab 01's priority-stack pattern.

Flagged gaps go into the monthly deep-dive's Section 5 (risks on the one-to-three-month horizon, from [Chapter 02](../02-authoring-the-executive-scorecard-weekly-monthly-quarterly.md)) — this is where the scorecard learns about them before they show up as misses in Section 2.

### Checkpoint 3 — before Step 4

- [ ] Every **GAP** cell in Section 2 has an entry in Section 3.
- [ ] Each entry carries rollout, days-since-GA, reason, severity, action.
- [ ] At least one entry is marked **flagged** or Step 2's gap-detection was too kind.

---

## Step 4 — The quarter's interview roster (20 min)

In Section 4, build the roster for the coming quarter. The roster is the signed calendar; the matrix is the diagnostic.

Produce a table with these columns:

| Week | Rollout | BU | Role(s) | Interviewer | Interviewees (count, not names) | Four-question prompt | Transcript owner |
|---|---|---|---|---|---|---|---|

One row per interview session. Chapter 01's rule is three interviewees per role × BU × tool cell as the minimum useful qualitative read; use three by default, more when the rollout is a flagged gap closing.

Scheduling rules, from Chapter 06's handoff cadences:

- **Weeks 4 through 8** of the quarter is the standing window. Weeks 1–3 are too early for the quarter's outcome data to reconcile against; weeks 9–12 collide with the monthly and quarterly deep-dive drafting cycles.
- **One interviewer per session.** The interviewer is the enablement lead for high-signal rollouts, a team manager for BU-local rollouts, an analyst for measurement-validity-focused sessions (echoing the Ziegler et al. construct-validity work from [Chapter 04](../04-reading-the-empirical-ai-productivity-literature-for-method-not-numbers.md)). Chapter 01 is explicit that the enablement lead reads transcripts personally; the lead does not have to run every interview, but every transcript crosses the lead's desk.
- **Three interviewees per session, minimum.** Sampled across operator tenure where the rollout warrants it, following the heterogeneity finding from Brynjolfsson/Li/Raymond in Chapter 04.
- **Transcript owner** is the role that receives the transcript into the measurement warehouse. Usually the analyst; sometimes an HR partner if the DPA constraints from Chapter 06 require it.

At the end of the roster, add a two-item footer:

- **Previously flagged gaps closing this quarter.** For each row in Section 3 marked **flagged**, name the specific row in Section 4 that closes it. A flagged gap with no closing row in Section 4 is a flagged gap *staying open*, and the roster says so.
- **Interviews that will not happen this quarter.** Any role × BU × tool cell that stays uncovered despite being in the portfolio — with a one-sentence reason. Chapter 01's qualitative-discipline rules do not allow silent under-coverage; the roster publishes what it is not doing.

### Checkpoint 4 — before Step 5

- [ ] The roster has at least one session per rollout live for 90+ days.
- [ ] Every session has an interviewer named by role (enablement lead, team manager, analyst, HR partner).
- [ ] Every flagged gap from Section 3 either closes in Section 4 or appears in the "will not happen" footer with a reason.
- [ ] No row has more than one interviewer; multi-interviewer sessions compress operator speech.

---

## Step 5 — The four questions and the anonymization protocol (10 min)

In Section 5, carry two artifacts the roster depends on.

### 5.1 The four questions

Chapter 01 names four questions, carried from [mod-102 Chapter 04](../../mod-102-selecting-and-rolling-out-ai-tools/04-measuring-whether-the-rollout-changed-anything.md). Write them verbatim in your roster, in this order:

1. What did you use the tool for this week?
2. What did it replace?
3. What did it add that wasn't there before?
4. Where did it misbehave or where did you stop trusting it?

Chapter 01's longitudinal-comparability point: *quarterly aggregates of question 4 responses, read in sequence, show the shape of a workflow's trust curve — a signal the dashboard cannot generate.* Add one sentence of guidance to the interviewer specifically on question 4: *follow up until an operator names a concrete incident or situation; "it sometimes misbehaves" is not an answer, it is a politeness.*

### 5.2 The anonymization protocol

Chapter 01's second qualitative-discipline rule is *anonymize at ingest*. Write a short protocol — five bullets at most:

- **At the interview.** Operators are told, in the first thirty seconds, that their name will not appear on the transcript or in any scorecard artifact, and that quotes used in the scorecard will be further anonymized to role-and-BU altitude ("one senior associate in BU-A noted…").
- **At transcription.** Operator name is stripped before the transcript enters the measurement warehouse. The analyst's pipeline enforces this; the enablement lead does not receive named transcripts.
- **At aggregation.** When quoting in the monthly deep-dive or the quarterly review, the quote is checked against the Chapter 06 aggregation-threshold rule: team-level quotes do not appear below a cell size that would re-identify individuals.
- **At retention.** Transcripts are retained for the duration specified in the organization's data-handling policy stack ([mod-103](../../mod-103-policy-co-authoring-with-governance/README.md)); typically 24 months at operator-level, indefinite at aggregate.
- **At failure.** If a dashboard or deep-dive exposes a quote that re-identifies an operator, it is not a scorecard input problem; it is a governance incident and routes to [mod-109](../../mod-109-ai-incident-response-and-enablement-side-rollback/README.md).

### Checkpoint 5 — before Step 6

- [ ] Section 5.1 carries the four questions in order, verbatim.
- [ ] Section 5.2 has five bullets covering interview, transcription, aggregation, retention, failure.
- [ ] Every bullet in 5.2 names an owner or a system; "we will anonymize" without an owner is a commitment that will not land.

---

## Step 6 — Red-team against the three qualitative-ground-truth rules and the three Chapter 06 governance surfaces (10 min)

Read the full document and check it against six risks. For each check that fails, add a `<!-- fix: ... -->` note inline and fix before the roster is signed.

Three Chapter 01 qualitative-discipline rules:

1. **Does the enablement lead read the transcripts personally?** Chapter 01: "This is not delegable to the analyst. An aggregated interview summary loses the texture that makes the qualitative layer diagnostic." Section 4's transcript-owner column names a system; Section 1 implicitly commits the lead to reading. If the roster has more than roughly fifteen sessions in a quarter, the reading commitment may not be realistic; cut sessions rather than delegate reading.
2. **Does the protocol in Section 5.2 anonymize at *ingest*?** Not at publication — at ingest. If the analyst or the enablement lead ever receives a named transcript, the floor has been breached and HR will stop supporting the cadence.
3. **Are quotes planned for careful use?** Chapter 01: "An anonymized operator quote that cuts against the aggregate number is more credible than ten quotes that confirm it. Use quotes to show the role is reading its own transcripts, not to decorate the deck." Section 4 does not need to plan quotes in advance, but Section 5 does need to carry the discipline so the interviewer knows which responses are worth flagging for the scorecard author.

Three Chapter 06 data-governance surfaces:

4. **Personal data and operator identification.** Do the Section 5.2 bullets name the aggregation threshold and the retention rule? If not, the protocol is partial.
5. **Cross-BU access.** Do the transcripts flow to a single warehouse where a BU-A VP could read BU-B's interviews? If permission scoping is undefined, the first flag will be a political event. Name the scoping in the protocol.
6. **Vendor telemetry in the transcripts.** If interviews cover a vendor tool whose DPA constrains downstream use of interaction data, does Section 5.2 account for it? If not, route through the [mod-103](../../mod-103-policy-co-authoring-with-governance/README.md) governance partnership before the interviews start.

Fix each `<!-- fix: ... -->` before the roster is signed.

### Checkpoint 6 — before shipping

- [ ] All six checks pass or carry a fix note.
- [ ] The reading commitment implied by Section 4 is one the enablement lead can honour at the session count scheduled.
- [ ] The governance surfaces are addressed in Section 5.2 rather than deferred.

---

## Step 7 — Version and route (5 min)

Add a versioned footer to `interview-coverage.md`:

```
Version: v0.1 — draft for team-manager working group review.
Matrix refresh cadence: monthly (first week).
Roster lock: first week of quarter; mid-quarter changes logged below with reason.

## Change log

- v0.1 (YYYY-MM-DD) — <your-name> — initial matrix and Q<N> roster.
```

Route the file to the team-manager working group (per [Chapter 06](../06-coordinating-with-the-analyst-and-the-team-manager.md)'s quarterly two-to-three-hour working session) and to the analyst (for transcript-pipeline confirmation). The deliverable is the matrix plus roster, not a write-up about them.

## Deliverables

- `interview-coverage.md` — Sections 1 through 6 filled, the matrix in Section 2, the roster in Section 4, the four questions and anonymization protocol in Section 5, red-team fixes applied, versioned footer and change log.

## Checkpoint — self-evaluation

- [ ] The matrix in Section 2 covers every (task-family, BU) intersection implied by the portfolio snapshot; blanks are labeled **—** or **GAP** explicitly.
- [ ] Every **GAP** cell has an entry in Section 3 with rollout name, severity, and action.
- [ ] The roster in Section 4 has one row per planned interview, with interviewer by role, interviewee count, four-question prompt, and transcript owner.
- [ ] Section 5.1 carries the four Chapter 01 questions verbatim; Section 5.2 anonymizes at ingest with a named owner.
- [ ] The document publishes what the quarter will *not* cover, not only what it will.

## What this lab prepares you for

Exercise 02's Section 2 (workflow-interview signals this week) and Exercise 03's Section 5 (qualitative ground truth at quarterly resolution) read from the roster this lab produces; without the roster, those sections are either padded with generalities or omitted. The matrix is the artifact the monthly deep-dive's Section 5 (risks on the one-to-three-month horizon) draws from when a flagged gap is about to become a scorecard miss. The lab also exercises two Chapter 06 interfaces simultaneously — the analyst (transcript pipeline, anonymization enforcement, permission scoping) and the team-manager group (BU-level interviewers, cross-BU pattern finding) — which are the interfaces that produce the qualitative layer at scale.
