# Lab 02 — Walk the Combined-Signal Dashboard Read

**Duration:** 60–75 minutes
**Format:** guided hands-on — worked walk + independent reads + named-intervention drill
**Grounding chapters:** [07 — Measuring Change-Management Health](../07-measuring-change-management-health.md), [06 — AI-Specific Resistance Patterns](../06-ai-specific-resistance-patterns-adkar-and-kotter.md)

## Objective

Read a one-page four-quadrant health dashboard against the combined-signal reads from [Chapter 07](../07-measuring-change-management-health.md), diagnose which pattern each snapshot matches, and produce the **named concern + named intervention + named owner** that Chapter 07 says every off-baseline signal must carry. You will walk one dashboard as a worked example, then independently diagnose two more and draft the exec-sponsor-facing narrative the operations analyst would pass up with the next scorecard cycle.

## Prerequisites

- Chapter 07 read with particular attention to *The combined-signal reads that matter*.
- Chapter 06 read (the resistance patterns surface through the Signal 4 resistance survey; interventions reference Chapter 06 by name).
- A working file called `dashboard-reads.md` to capture each diagnosis.

## Why a lab, not an exercise

[Exercise 06](../exercises/exercise-06-change-management-health-dashboard.md) asks you to *design* the one-page four-quadrant dashboard for a specific organization — baselines, intervention triggers, the dashboard template. This lab operates below that: given a populated dashboard, walk the combined-signal read and produce the intervention. Chapter 07 is explicit that "combined-signal reads are the practice; single-signal reads are training wheels," and that "if a review produces no interventions, the dashboard is not being used." Those two sentences are what this lab trains on.

## Setup

Open `dashboard-reads.md` and paste this skeleton. You will reuse it three times — one for the worked example, one each for the two independent reads.

```markdown
# Dashboard Read — <snapshot-name>

## The snapshot

| Quadrant | Current value | Baseline | Delta from last period |
|---|---|---|---|
| Adoption curve shape | | | |
| Champion retention | | | |
| Communications reach | | | |
| Resistance survey | | | |

## Combined-signal diagnosis

Named read (from Ch 07): <one of the five combined reads, or "novel — explain">
Confidence: <low / medium / high>
Why: <2-3 sentences tying the specific values to the named read>

## Named interventions

| Quadrant | Named concern (one sentence) | Named intervention (one sentence) | Named owner |
|---|---|---|---|
| Adoption curve shape | | | |
| Champion retention | | | |
| Communications reach | | | |
| Resistance survey | | | |

## What goes into the exec scorecard this quarter

<2-3 sentences: which slice of the dashboard surfaces into the Chapter 04 scorecard, what the ask is, what stays internal.>
```

---

## Step 1 — Walk the worked example (20 min)

### The snapshot

The fictional organization: a 3,000-person US bank, the rollout is a six-month-old customer-service AI assistant for Tier 1 ticket handling, mandated for the 400 branch service reps (Shape B from [Chapter 05](../05-opt-in-vs-mandate.md)). The dashboard at the end of month six:

| Quadrant | Current value | Baseline (Ch 07) | Delta from last period |
|---|---|---|---|
| Adoption curve shape | **S-curve**, active-use at 78% of in-scope roster in a given week | ≥65% active-use by month six | +4pp |
| Champion retention | active-roster 15 of 15; retention 100% so far; function-coverage 100% | active = roster; retention ≥85%; coverage ≥90% | 0 |
| Communications reach | opens 48% (org baseline ~35%); Slot 4 click-through 9%; self-serve traffic rising with sends | opens above internal-comms baseline; click-through >5%; sustained self-serve | +1pp opens; +2pp clicks |
| Resistance survey | quality-skepticism free-text cluster is rising — in Q2 10% of responses mentioned "the tool gets the policy nuance wrong"; in Q3 that cluster is **27%** of responses, with repeated references to a specific exception-handling workflow | — (survey is pattern-detection not metric-chase) | +17pp cluster growth |

### Fill the skeleton

Copy the skeleton into `dashboard-reads.md` with the snapshot above transcribed. Now walk the diagnosis.

### The combined-signal diagnosis — walk Chapter 07's five named reads

Chapter 07 lists five combined reads:

1. Adoption up + resistance quality-skepticism up → silent-compliance risk forming.
2. Adoption flat + champion retention normal + comms reach normal → tool not finding workflow fit; route to mod-102.
3. Comms reach high + adoption flat + resistance anxiety high → role-threat narrative competing with vision; intervene in Slot 3.
4. Champion retention low + resistance survey "program should change X" cluster → field-signal interface failing *and* structural problem; investigate before continuing rollout.
5. All four signals healthy + business scorecard flat → change is working; scorecard may be mis-aligned.

Match the snapshot: adoption is up and healthy S-curve; resistance survey shows a sharp quality-skepticism signal rising in free-text. That is read #1 — **silent-compliance risk forming**.

Write in the **Named read** row:

> Named read: #1 — adoption up + quality-skepticism rising → silent-compliance risk forming.
> Confidence: high.
> Why: adoption curve shape is on the S-curve baseline and ahead of target; three other quadrants are on baseline; the one deviation is a 17pp growth in a specific quality-skepticism free-text cluster, concentrated in a single workflow. The shape is "operators are using the tool, and trust in the tool is deteriorating in parallel" — Chapter 07's description of the silent-compliance precursor.

### Fill the four intervention rows

Follow Chapter 07's rule: every off-baseline signal gets a *named* concern, a *named* intervention, and a *named* owner. For the three quadrants on baseline, the named intervention is "protect the rhythms that are working" — do not over-intervene; Chapter 07 is explicit about this on the S-curve.

For the resistance-survey quadrant, the intervention has two moves (Chapter 07 → Chapter 06):

- Route the specific exception-handling workflow failure through the field-report pipeline for investigation (Chapter 03 Route 2/3, treating the skepticism as signal first, resistance second per [Chapter 06 Pattern 4](../06-ai-specific-resistance-patterns-adkar-and-kotter.md)).
- Reinforce verification habits in the specialist-tier content ([Chapter 06 Pattern 4 → interventions](../06-ai-specific-resistance-patterns-adkar-and-kotter.md)): the role-based playbook names the verification step for each use case; the champion for customer service runs a monthly "what are we doing differently now" check-in (silent-compliance intervention, Pattern 5).

Owner for both moves: operations analyst runs the field-report investigation; the customer-service champion runs the monthly check-in; the enablement lead sponsors the Chapter 06 reinforcement rev.

### What goes into the scorecard

Write the 2–3 sentences for the exec sponsor. The slice that surfaces: the quality-skepticism cluster growth, the specific workflow, the intervention plan with named owners, and the ask (what decision the sponsor needs to confirm — usually a time allocation for the ops analyst's investigation and a cadence Slot 3 line in next month's send that names the issue honestly, matching the dissent-slot discipline from [Chapter 04](../04-the-rollout-communications-cadence.md)). What stays internal: the specific operator-level free-text responses.

### Checkpoint 1 — before Step 2

- [ ] The named read in your diagnosis matches one of Chapter 07's five and your two-sentence *Why* ties specific values from the snapshot to the read.
- [ ] Every off-baseline quadrant has a named concern, a named intervention, and a named owner in complete sentences.
- [ ] On-baseline quadrants carry the "protect the rhythms that are working" note; you did not over-intervene on healthy signals.
- [ ] The scorecard paragraph names a specific ask the sponsor can decide — not a summary without a decision point.

---

## Step 2 — Independent read #1 (15 min)

Clear the skeleton and transcribe this snapshot. The organization: a 12,000-person global pharma, six months into an opt-in general-purpose AI writing assistant rollout (Shape A from Chapter 05), works-council consultations completed in European sites.

| Quadrant | Current value | Baseline | Delta from last period |
|---|---|---|---|
| Adoption curve shape | **Flat line** — access provisioned to 7,800 operators, first-use rose to 1,100 in month one, active-use has sat at ~900 (7.5% of in-scope) for three months | S-curve rising to a sustainable plateau | 0 |
| Champion retention | active-roster 48 of 52; retention 96% of year-to-date; renewal rate running ~60%; function-coverage 98% | active = roster; retention ≥85%; renewal 40-70%; coverage ≥90% | -4 active |
| Communications reach | opens 52%; Slot 4 click-through 11%; self-serve traffic rising with sends | above baselines | +2pp clicks |
| Resistance survey | AI-anxiety signal flat; "ChatGPT at home" cluster flat; quality-skepticism flat; silent-compliance survey question responses skewing "my workflow has not changed in the last 60 days" at 72% | — | +4pp "not changed" |

Diagnose. Do not peek at the worked example above; this is the drill. Prompts, not spoilers:

- Three quadrants are on baseline. One quadrant is very off. Which combined read matches the pattern "adoption flat, three adjacent quadrants healthy"?
- The resistance survey response "my workflow has not changed" is worth interpreting — in the context of an opt-in, is it consistent with the adoption flat-line, or does it contradict it?
- What does Chapter 07 say the specific intervention is when the three adjacent systems are healthy and the tool is the issue?

Fill the skeleton. Hard rule: **you may not use the phrase "more communications" or "more training" as the intervention.** Both are present at baseline; neither is the gap.

### Checkpoint 2

- [ ] Named read references Chapter 07's combined read #2 (tool not finding workflow fit → route to mod-102 selection re-examination).
- [ ] Named owner on the intervention is the enablement lead working with mod-102's pilot pipeline, not "the CoE" generically.
- [ ] The scorecard paragraph does not frame the flat line as a comms or training failure; it frames it as a selection/workflow-fit question the exec sponsor needs to decide on.
- [ ] The on-baseline quadrants do not get interventions.

---

## Step 3 — Independent read #2 (15 min)

Clear the skeleton again. The organization: a 500-person SaaS company, nine months into a three-tool rollout (coding assistant for engineering, AI sales-ops assistant, general writing assistant), all three were run as opt-in with a mandatory literacy module stacked ahead.

| Quadrant | Current value | Baseline | Delta from last period |
|---|---|---|---|
| Adoption curve shape | engineering coding assistant active-use 85% (healthy S-curve); sales-ops assistant active-use 42% (shark fin — rose to 68% in month two, declining since); general writing assistant active-use 51% (hockey stick — flat for 4 months, rising recently) | — | sales-ops −14pp; writing +9pp |
| Champion retention | active-roster 6 of 9; retention 67%; two champions retired mid-term citing workload; function-coverage 75% (sales-ops uncovered since champion A's retirement) | active = roster; retention ≥85%; coverage ≥90% | -3 active, -11pp retention |
| Communications reach | opens 38% (below org baseline of ~50% for a tech company); Slot 4 click-through 3%; self-serve traffic spiking on send days then crashing | above org baseline | −6pp opens, −2pp clicks |
| Resistance survey | "program should start/stop/change X" open-slot responses cluster around two themes: "cadence feels pointless, nothing changes" (21%) and "I don't know who my function's champion is" (28%) | — | both clusters new this quarter |

Diagnose. This snapshot matches Chapter 07's combined read #4 — champion retention low *and* resistance-survey structural-problem cluster. The adoption-curve quadrant also shows three different shapes, each needing its own named intervention from Chapter 07's shape-vocabulary table (shark fin → quality-skepticism investigation or workflow-fit; hockey stick → investigate the delay and shorten it next rollout).

Fill the skeleton, and note two specific things:

- The named interventions this quarter are *not* a new tool rollout. Chapter 07 is explicit: "both signals are pointing at a specific program issue; investigate before continuing the rollout." Name that pause in the scorecard paragraph.
- The sales-ops shark fin + the sales-ops champion retirement + the 28% "don't know who my champion is" cluster all point at the same function. One function, three deltas. The named intervention should recognise the cluster, not treat each quadrant's delta as independent.

### Checkpoint 3

- [ ] Your diagnosis names combined read #4 (or #4 plus a per-tool adoption-shape overlay) and the *Why* ties the three independent deltas to the same function.
- [ ] The scorecard paragraph names a program pause — the next rollout holds pending the investigation — and names the ask (the sponsor confirms the pause and allocates investigator time).
- [ ] At least one intervention references the Chapter 02 lifecycle — the champion retirements are a recruit-phase trigger as well as a retention signal.

---

## Step 4 — The anti-pattern check (5 min)

Read all three of your `dashboard-reads.md` entries aloud and check each against the three common failures Chapter 07 warns about.

1. **The single-signal read.** Did you diagnose from one quadrant's value instead of the combination? If one of your reads uses only one quadrant's data, mark it `<!-- fix: single-signal read -->` and rework.
2. **The interventionless review.** Did any read produce "no action — continue monitoring" across the board when the combined signal was actually off? Chapter 07: "if a review produces no interventions, the dashboard is not being used."
3. **The over-intervention.** Did you add interventions on quadrants that were on baseline? Chapter 07's S-curve guidance is explicit — no intervention; protect the rhythms that are working. An over-intervening analyst burns credibility with the exec sponsor the first time they are asked to justify a change that fixed something that was not broken.

---

## Deliverables

- `dashboard-reads.md` — three completed entries (the worked example, two independent reads), each with the full skeleton populated.

## Checkpoint — self-evaluation

- [ ] Three dashboard snapshots, three named combined-signal reads (matched to Chapter 07's list by number, or named "novel" with a specific reasoning paragraph).
- [ ] Every off-baseline quadrant across all three reads has a named concern, named intervention, and named owner in complete sentences.
- [ ] No read uses the phrase "more communications" or "more training" as the intervention.
- [ ] Each read's scorecard paragraph names an ask the exec sponsor can decide on, not a summary.
- [ ] Anti-pattern check applied; any `<!-- fix: -->` markers resolved.

## What this lab prepares you for

Exercise 06 designs the dashboard template and baselines. This lab's reads are what the dashboard produces every week in the ops analyst's review and every quarter in the exec sponsor's scorecard slice. The muscle this lab trains — resisting single-signal reads, producing named interventions on the off-baseline quadrants, and not over-intervening on healthy ones — is the specific judgment Chapter 07's closing sentence names ("combined-signal reads are the practice; single-signal reads are training wheels"). The lab is also the fastest route to catching the silent-compliance pattern from Chapter 06 before it appears on the business scorecard as a plateau.
