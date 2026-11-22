# Lab 02 — Wire the Per-Rollout Measurement Plan v0.1

**Duration:** 60–75 minutes
**Format:** guided hands-on — three-layer measurement plan with capture mechanisms and named owners
**Grounding chapters:** [04 — Measuring Whether the Rollout Changed Anything](../04-measuring-whether-the-rollout-changed-anything.md), [02 — Designing Bounded Pilots](../02-designing-bounded-pilots.md)

## Objective

Build a **measurement plan v0.1** for one concrete rollout — the operational artifact that specifies, for each of Chapter 04's three layers, *what* you measure, *how* it is captured, *who* owns the reading, and *when*. The deliverable is not a scorecard and not a weekly report; it is the wiring diagram that both of those depend on.

If the inputs to the scorecard are theatre, the scorecard is theatre. This lab is where you refuse the theatre at the plumbing layer.

## Prerequisites

- Chapter 04 read, with the three-layer order (outcome → interviews → telemetry) held in your head.
- Chapter 02 skimmed; the baseline rules travel from pilot into rollout.
- A chosen organization and rollout. Carry forward from Exercises 01–04 if you have the pair. If not, pick one:
  - 3,000-person US bank rolling out a code assistant to a 180-engineer platform team; target task: **pull-request cycle time on tier-2 service repos**
  - 12,000-person global pharma rolling out a document-summarization tool to the 60-person medical-affairs writing team; target task: **time to first reviewable draft of a response letter**
  - 500-person SaaS company rolling out a meeting-notes tool to a 220-person go-to-market org; target task: **follow-up actions captured per customer meeting, logged in the CRM**
- A blank markdown file.

## Why a lab, not an exercise

Exercise 03 produces a one-page *weekly report*; Exercise 06 is a rewrite *drill*. Neither specifies the measurement plumbing underneath. This lab does — it names the fields that have to exist upstream of a readout so the readout has something true to say. Rollouts drift into metric theatre at this layer, not at the report layer.

## Setup

Create `measurement-plan-v0-1.md` with this skeleton:

```markdown
# Measurement Plan — <organization> / <rollout> / v0.1

**Rollout:** <tool> → <cohort>
**Target task (from the pilot charter):** <one sentence>
**Owner of this plan:** AI Enablement Lead
**Cadence of plan revision:** monthly through month 6, then quarterly

## Layer 1 — Outcome metrics on the target task

<entries>

## Layer 2 — Workflow interviews

<entries>

## Layer 3 — Usage telemetry — sanity check only

<entries>

## Readout rules

<entries>

## What this plan does not cover

<entries>
```

---

## Step 1 — Layer 1: outcome metrics on the target task (20 min)

Chapter 04 is unambiguous: Layer 1 is the only layer that answers the CFO's "what changed?" question. You will specify **one primary** outcome metric and **one secondary** outcome metric for your target task, using this field set:

```markdown
### Outcome metric — <primary / secondary>

- **Metric name:** <one phrase — "median PR cycle time on tier-2 service repos", not "developer productivity">
- **Measurement method:** <how the number is produced — SQL against ticketing system, timing study, sampled QA review, log scrape>
- **Data source (system of record):** <named system — Jira, ServiceNow, GitHub audit log, CRM>
- **Unit + direction of goodness:** <minutes, lower is better; actions-per-meeting, higher is better>
- **Comparable-work rule:** <what work shape is held constant; what annotations capture shifts in it>
- **Baseline value:** <number + capture window — or "to be measured in weeks <N>-<M> before pilot start">
- **Reading cadence:** <weekly / monthly — matched to the signal's natural noise floor>
- **Owner of the reading:** <role in the BU — not "the CoE">
- **First post-rollout reading target date:** <date or "week N of rollout">
```

Chapter 04 gives you the task-class shapes (drafting, summarization, retrieval, support-ticket, code review, meeting notes). Use your rollout's class to pick two shapes; do not invent a shape of your own on first draft.

**Specific moves for your rollout:**

1. **Choose the primary metric.** If your target task is pull-request cycle time, your primary is likely *median PR cycle time on the target repos*. Not "developer satisfaction." Not "logins per day."
2. **Choose the secondary.** The secondary exists to catch a metric-theatre failure in the primary. Chapter 04 pairs cycle time with defects-caught-after-merge for code review; summarization time with disagreement rate between summary and source; drafting speed with acceptance rate from reviewer on first pass. Match the pairing to your task class.
3. **Name the baseline window.** Chapter 02: "A four-week pilot with a two-day baseline is not a comparison; it is a coincidence." The baseline window should be comparable to the pilot duration and long enough to absorb normal variance. If your pilot ran four to twelve weeks, your baseline window matches.
4. **Name the comparable-work rule.** This is the field learners skip and it is the field that saves the readout from "30% speedup on tickets that got simpler." Write the rule even when it is boring.
5. **Name an owner of the reading in the BU, not in the CoE.** If the only person who can produce the reading is you, Layer 1 will quietly collapse the first week you have a conflict — and the readout will slide to telemetry by default.

**Checkpoint 1:**

- [ ] Two outcome metrics specified — primary and secondary — with all nine fields each.
- [ ] The secondary metric is chosen to catch a specific metric-theatre failure in the primary (e.g., speed paired with a quality metric, throughput paired with an escape rate).
- [ ] The baseline value field either names a number *or* names a specific capture window before pilot start — not "TBD."
- [ ] The owner of the reading is named by BU role, not the CoE.
- [ ] No number is borrowed from a vendor's published case study or from the Chapter 04 literature section. Chapter 04: "Do not borrow a vendor's published number for your scorecard. You do not know what workflow produced it."

---

## Step 2 — Layer 2: workflow interviews (15 min)

Chapter 04's rule: "Minimum sample for an org-wide rollout: every role that touches the tool, every BU that adopted it." Numbers tell you *that* something moved; interviews tell you *why*, *for whom*, and *where the tool misbehaves in ways the dashboard will never surface*.

Build a short interview schedule using this field set:

```markdown
### Interview schedule

- **Cadence:** <monthly for flagship / quarterly for long-tail>
- **Target length per interview:** <20–40 minutes, Chapter 04 default>
- **Roles × BUs matrix:**
  | BU \ Role | <role 1> | <role 2> | <role 3> |
  |-----------|----------|----------|----------|
  | <BU 1>    | <N>      | <N>      | <N>      |
  | <BU 2>    | <N>      | <N>      | <N>      |

- **The four questions (verbatim, every time):**
  1. What did you use the tool for this week?
  2. What did it replace?
  3. What did it add that wasn't there before?
  4. Where did it misbehave or where did you stop trusting it?
- **Selection rule:** <how you pick the named user in each cell — not "the loudest champion">
- **Transcription + tagging path:** <where transcripts live, who tags, tag taxonomy source>
- **Aggregation rule:** <"patterns across users are the finding; a single quote is an anecdote" — verbatim from Chapter 04>
- **Owner of the schedule:** <role>
```

Specific moves:

1. **Build the roles × BUs matrix explicitly.** For your chosen rollout, list every role that touches the tool and every BU that adopted it. Put a target interview count in each cell. If your rollout goes into three BUs and three roles, the matrix is nine cells, and the minimum sample has coverage in each — not three interviews total. Chapter 04 is explicit on this.
2. **Write the selection rule as a refusal of loud-user bias.** Example: "In each cell, select one user from the top usage quartile and one from the bottom. Rotate quarterly. Named participants, not self-nominated volunteers."
3. **Copy the four questions verbatim.** Chapter 04's point is that the questions are stable over time so that patterns are legible across quarters — paraphrasing destroys the aggregation.
4. **Name a transcription path.** If the interviews are not transcribed and tagged, they are stories, not data. Specify where transcripts live and who maintains the tag taxonomy.

**Checkpoint 2:**

- [ ] The roles × BUs matrix exists and has a target count in each cell — not "we'll interview a few people."
- [ ] The four questions are copied verbatim from Chapter 04.
- [ ] The selection rule explicitly refuses loud-user bias (top quartile and bottom quartile, or similar).
- [ ] An owner of the schedule is named.

---

## Step 3 — Layer 3: usage telemetry as sanity check only (10 min)

Chapter 04's three permitted uses of telemetry: *did the floor hold?*, *where is the dark matter?*, *is the spend wasted?* Nothing else.

Build a short telemetry section using this field set:

```markdown
### Telemetry sanity-check panel

- **Metrics in panel (three at most):**
  1. <WAU / licensed — floor-holding check>
  2. <BUs with licenses but near-zero usage — dark-matter targeting for Layer 2>
  3. <unused seats for the quarter — reclaim list>
- **Thresholds that trigger action:**
  - Floor-held threshold: <value> — breach triggers <action>
  - Dark-matter threshold: <value> — breach triggers <Layer 2 interview target>
  - Reclaim threshold: <value> — breach triggers <seat reclaim workflow>
- **Cadence:** <weekly, from vendor admin console>
- **Where telemetry appears in the readout:** <"late in the paragraph, one line, demoted — never the headline">
- **Explicit prohibition:** <"a high login rate is never cited as evidence the target task moved" — verbatim promise>
- **Owner of the panel:** <role>
```

Specific moves:

1. **Cap the panel at three metrics.** More metrics = more temptation to lead with telemetry. Chapter 04 lists exactly three legitimate uses; the panel has one line per use.
2. **Write the thresholds as triggers.** Telemetry's job in this plan is to cause the next move — a Layer 2 interview target, a seat reclaim, an incident check — not to decorate a slide.
3. **Write the explicit prohibition.** This is the line you will reread before every readout: "a high login rate is never cited as evidence the target task moved." Put it in the plan so that future-you cannot drift.

**Checkpoint 3:**

- [ ] The telemetry panel has at most three metrics, each mapped to one of Chapter 04's three permitted uses.
- [ ] Each metric has a threshold that triggers a specific action, not a passive dashboard tile.
- [ ] The explicit prohibition sentence is in the plan.

---

## Step 4 — Readout rules (10 min)

Chapter 04 and Chapter 05 both describe metric theatre as a readout failure, not a measurement failure. Lock the readout rules into the plan so the measurement cannot be re-staged at report time.

Add a section:

```markdown
## Readout rules

- **Order of layers in every readout:** outcome → interviews → telemetry. Non-negotiable.
- **Headline rule:** the headline is the primary outcome metric, even when it is flat. Chapter 04: "If the outcome did not move, say so plainly."
- **Telemetry share of the page:** at most one quarter of the readout. Not the headline, not the closer.
- **Vanity-number refusal:** no reading is published without a baseline on comparable work. "Post-rollout number without a pre-rollout baseline" is a vanity number and is kept out of readouts — Chapter 04's rule, not a stylistic preference.
- **Metric-theatre check (run before every readout):**
  1. Does the readout open with the outcome? If not, re-order.
  2. Is the outcome stated as a number, not as words? If not, replace the adjectives.
  3. Is the pilot baseline on the page? If not, pull it up.
  4. Can everyone on the call state the target task in one sentence? If not, add a one-line target-task banner.
- **Composition into mod-106:** this plan's Layer 1 and Layer 2 outputs are what mod-106 aggregates. Cost attribution and ROI math belong to mod-107, not here.
```

**Checkpoint 4:**

- [ ] The order of layers in the readout is written as non-negotiable.
- [ ] The metric-theatre check is a short list a facilitator can run in two minutes before a steering committee.
- [ ] The plan explicitly disavows cost attribution / ROI math — those compose into mod-107, not this plan.

---

## Step 5 — "What this plan does not cover" (5 min)

Add a short closing section naming the adjacent concerns this plan explicitly does not do:

- The **executive scorecard** (mod-106) — this plan produces inputs; it does not render the scorecard.
- The **ROI calculation** (mod-107) — this plan produces outcome metrics in native units (minutes saved, defects caught); the dollar translation sits downstream.
- The **incident response path** (mod-109) — sanity-check breaches that look like incidents escalate out of this plan into incident runbooks.
- The **training package** (Chapter 03 artifact 4, deepened in mod-104) — some Layer 2 signal will feed training revisions; the training package is authored elsewhere.

This section is small and important. Chapter 04's closing move is to compose with mod-106 and mod-107 "not the other way around" — writing the boundary down keeps the plan from quietly growing into those modules' scope.

**Checkpoint 5:**

- [ ] The "what this plan does not cover" section names at least mod-106, mod-107, and mod-109 by module, not by vague gesture.

---

## Deliverable

- `measurement-plan-v0-1.md` — three layer sections (Layer 1 with primary + secondary metric, Layer 2 with the roles × BUs matrix, Layer 3 with the three-metric panel), the readout rules, and the "what this plan does not cover" section.

## Expected output shape

Roughly 2–3 pages of markdown. Layer 1 is the largest section; Layer 3 is the smallest. The roles × BUs matrix is visible. The four interview questions are verbatim. The explicit telemetry prohibition sentence is present. The metric-theatre check is a short, actionable list.

## Checkpoint — self-evaluation

- [ ] Layer 1 has a named primary and secondary outcome metric, each with all nine fields populated — or the baseline value field names a specific capture window before pilot start, not "TBD."
- [ ] The secondary metric is chosen to catch a specific quality or regression failure in the primary (speed paired with a quality metric, throughput paired with an escape rate).
- [ ] The roles × BUs matrix has a target interview count in each cell, matching Chapter 04's "every role × every BU" minimum sample rule.
- [ ] The four interview questions are verbatim from Chapter 04.
- [ ] The telemetry panel is capped at three metrics and the explicit prohibition sentence is present.
- [ ] The readout rules name the order of layers, the headline rule, the telemetry page share, and the metric-theatre check.
- [ ] The "what this plan does not cover" section names mod-106, mod-107, and mod-109 at minimum.
- [ ] No borrowed numbers from vendor case studies or literature. Chapter 04: method travels, numbers do not.

## Common failure modes

- **Primary metric is a satisfaction score.** Chapter 04 lists satisfaction under telemetry-adjacent signals, not outcome. A satisfaction score is not an answer to "did the target task get faster, better, cheaper?" Replace it.
- **The secondary metric is a flavor of the primary.** "Median cycle time" and "mean cycle time" are the same metric with two statistics; they will not catch a metric-theatre failure in each other. Pair different *dimensions* — a speed metric with a quality metric, a throughput metric with a defect-escape metric.
- **Interview matrix listed as "we'll do a few interviews per quarter."** This is not a sample; it is a prayer. Chapter 04's minimum is coverage in every role × BU cell; write the count per cell.
- **Owner of every reading is the CoE.** The plan will collapse the first week the CoE has a scheduling conflict. BU-side owners for BU-side readings.
- **A telemetry metric labeled as an outcome.** DAU/MAU, prompts-per-user, licenses-active are all telemetry. Chapter 04 names this directly. If you see any of them in Layer 1, move them to Layer 3.
- **No explicit prohibition sentence.** Six months in, someone will quote the 95% login rate at you as proof the rollout worked. The sentence in the plan is what lets you say no with evidence, not with vibes.

## What this prepares you for

This plan is the input to mod-106's org-wide scorecard and the baseline on which mod-107's ROI math rests. Writing it carefully once, before the first readout, is how you keep the rollout from drifting into metric theatre at month three — the point at which the drift is already visible to the CFO and expensive to reverse. In the real role, you will produce one of these per rollout, every time, and revise v0.1 after the first pilot readout. The lab is where you learn what v0.1 has to contain.
