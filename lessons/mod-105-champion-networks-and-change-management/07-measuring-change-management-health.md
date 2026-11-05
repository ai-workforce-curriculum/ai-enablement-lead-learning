# Measuring Change-Management Health

> A change-management program that cannot measure its own health runs blind until the exec sponsor loses patience. Four signals — *adoption curve shape, champion retention, communications reach, resistance survey* — read together give you enough resolution to catch problems before they are visible on the business scorecard. This chapter defines each signal, the specific intervention it triggers, and how the four combine into a health dashboard the operations analyst owns.

## Why four signals, not one

A single-metric change program always looks good or always looks bad; neither is usefully diagnostic. "Adoption rate" alone misses the silent-compliance pattern from [Chapter 06](06-ai-specific-resistance-patterns-adkar-and-kotter.md); "satisfaction score" alone misses the role-threat narrative; "training completion" alone misses the quality skepticism.

Four signals instrument four distinct aspects of health:

- **Adoption curve shape** — are operators actually adopting, and on what trajectory?
- **Champion retention** — is the two-way signal interface staying alive?
- **Communications reach** — is the cadence from [Chapter 04](04-the-rollout-communications-cadence.md) reaching the audience?
- **Resistance survey** — are the resistance patterns from [Chapter 06](06-ai-specific-resistance-patterns-adkar-and-kotter.md) building or releasing?

Each signal is cheap to instrument, actionable on its own, and more informative in combination. The combination is the dashboard; the dashboard is the operations analyst's primary surface.

## Distinguishing this dashboard from the business scorecard

The executive scorecard from [mod-106](../mod-106-outcome-measurement-and-executive-reporting/README.md) measures business outcomes — time saved, incidents avoided, revenue influenced. This dashboard measures the *health of the change effort* itself. They are related but not the same:

- A healthy change effort produces business outcomes eventually.
- Business outcomes can look good temporarily while the change effort is quietly deteriorating (silent compliance pattern).
- Business outcomes can look bad temporarily while the change effort is healthy (mid-way through a large behaviour-change rollout).

The dashboard is a *leading* indicator; the scorecard is a *trailing* indicator. The dashboard belongs to the enablement function and informs internal decisions. Slices of the dashboard surface into the scorecard where they tell a business story the exec sponsor needs; the rest stays internal.

## Signal 1 — Adoption curve shape

### What to measure

For each rollout, three curves over time:

- **Access curve** — the cumulative count of in-scope operators who have been provisioned.
- **First-use curve** — the cumulative count of provisioned operators who have made their first substantive use (not a login — an actual task completed).
- **Active-use curve** — the count of operators using the tool in a given week against the in-scope denominator.

Three curves because each stall point tells a different story. Access that stalls is an IT identity problem; first-use that stalls is a training or champion problem; active-use that stalls is a workflow-fit problem.

### The shape vocabulary

Four shapes recur; name them so the team can diagnose quickly.

- **S-curve.** The classic adoption shape — slow start, rising mid-adoption, plateau at a sustainable active-use level. Healthy.
- **Hockey stick.** Flat for the first quarter, then a sharp rise. Usually the result of a late champion activation or a compelling use-case spotlight landing after the initial launch. Lagged but healthy.
- **Shark fin.** Rapid first-month adoption, visible decline in months 2–4. Early activity was launch-driven; the tool did not find a workflow fit. Not healthy.
- **Flat line.** Access provisioned, first-use never rises, active use stays near zero. The ghost-user rollout from [mod-102 Chapter 03](../mod-102-selecting-and-rolling-out-ai-tools/03-the-rollout-artifact-set.md).

### Specific intervention per shape

| Shape | Primary intervention |
|---|---|
| S-curve | No intervention; protect the rhythms that are working |
| Hockey stick | Investigate why the delay; shorten it next rollout |
| Shark fin | Diagnose: workflow-fit problem? ([mod-102 Chapter 02](../mod-102-selecting-and-rolling-out-ai-tools/02-designing-bounded-pilots.md) pilot design was thin), or quality-skepticism pattern surfacing in month 2? ([Chapter 06](06-ai-specific-resistance-patterns-adkar-and-kotter.md)) |
| Flat line | Check first: did the training package tie to a real use case? Is the champion for the function active? Walk the ghost-user checklist from [mod-102 Chapter 03](../mod-102-selecting-and-rolling-out-ai-tools/03-the-rollout-artifact-set.md) |

### What the curve does not tell you

Adoption curves do not tell you whether operators are using the tool *correctly*. A flat line on active use is bad; an active-use curve that rises while verification habits collapse is worse. Pair the curve with the resistance survey (Signal 4) and with the incident path from [Chapter 08](08-the-handoff-to-the-governance-incident-path.md) to avoid optimising for the surface metric.

## Signal 2 — Champion retention

### What to measure

Four sub-metrics against the champion roster:

- **Active-roster count** — champions who filed at least one field report in the last 60 days *and* hosted at least one office hour. A champion who has done neither is not active.
- **Retention rate** — champions who completed the current year's term relative to the start-of-year roster.
- **Renewal rate** — eligible champions renewing for a second term.
- **Function-coverage ratio** — functions with at least one active champion as a percentage of in-scope functions.

### Healthy baselines

Reasonable starting baselines, though your organization's shape will differ:

- Active-roster count should equal the roster count. Drift over 10% is a signal.
- Retention rate above 85% at year-end.
- Renewal rate between 40% and 70% — too low means the role is draining people; too high means the recruitment pipeline is not producing new candidates.
- Function-coverage ratio at 90%+ by the end of the first full year; any un-championed in-scope function is a known gap on the health dashboard.

### Specific intervention per deviation

- **Active-roster < roster count.** Walk the specific champions who have gone quiet. Is it workload (manager-release failing in practice)? Function change? Burnout? Each has a different intervention and a different implication for the lifecycle from [Chapter 02](02-the-four-phase-lifecycle-recruit-train-recognise-retire.md).
- **Retention < 85%.** Something in the role is harder than the design — the time commitment is wrong, the recognition is thin, the role scope has expanded informally, or the recruitment criteria missed. Debrief exiting champions; adjust the lifecycle.
- **Renewal too low.** The role is not building a career surface; the recognition channel 2 (visibility into the champion's own career) from [Chapter 02](02-the-four-phase-lifecycle-recruit-train-recognise-retire.md) is not working.
- **Renewal too high.** The recruitment pipeline is not producing candidates; a stuck cohort is forming. Open seats deliberately.
- **Function-coverage gap.** Named functions with no champion lose field-signal connection; treat each as a priority recruit in the next cycle.

## Signal 3 — Communications reach

### What to measure

Four sub-metrics:

- **Open / view rate** by communication surface (monthly update, quarterly brief, launch comms). Not vanity — actual open rate over a baseline.
- **Click-through on Slot 4 call-to-action.** The specific action each send calls for — registered, joined, read, attended. Measure against the target population for each action.
- **Self-serve traffic** on the pages the communications link to. A send that drives nothing to the self-serve layer is a send that did not land.
- **Reach breadth** — percentage of in-scope operators who have read at least one cadence send in the last 90 days.

### Healthy baselines

- Open rate meaningfully above the organization's internal-communications baseline (the partnership with internal comms from [mod-104 Chapter 08](../mod-104-training-programs-and-ai-literacy-curriculum/08-partnering-with-hr-ld-and-internal-comms.md) will tell you the baseline).
- Click-through on Slot 4 above 5% of the targeted operators. Below that, either the action is too ambitious for the slot or the content around it did not build enough pull.
- Self-serve traffic rising with cadence sends and sustained between them. A spike-and-crash pattern is the cadence producing attention without durable landing.
- Reach breadth at 60%+ for monthly, 80%+ for launch comms.

### Specific intervention per deviation

- **Open rate low.** The send is being filtered as noise; the problem is the subject line, the sender's identity, or the frequency. Partner with internal comms to debug.
- **Click-through low with high opens.** The content read fine; Slot 4 was wrong. Either the action was too big or too small for the audience. Usually too big.
- **Self-serve traffic low.** The link between the cadence and the self-serve layer is thin; sends should surface specific self-serve pages, not drive to a landing page that requires more navigation.
- **Reach breadth low.** A part of the in-scope population is not on the channel. Partner with internal comms to find the gap; often it is a sub-population (field operators, shift workers, offshore teams) that the standard channels miss.

## Signal 4 — Resistance survey

### What to measure

A short recurring instrument — six to eight questions, run quarterly, sampled across functions. The point is not to generate a satisfaction number; the point is to detect the resistance patterns from [Chapter 06](06-ai-specific-resistance-patterns-adkar-and-kotter.md) before they consolidate.

Specific questions, by pattern:

- **AI anxiety.** "How confident do you feel about your role's direction given the current AI rollout?" with a free-text follow-up.
- **Role-threat narrative.** "What are you hearing from peers about what the AI rollout means for your function?" (The question surfaces narratives without validating them.)
- **"ChatGPT at home."** "How does your personal use of AI tools outside of work compare to your use inside work? What, if anything, do you wish were different?"
- **Quality skepticism.** "When the AI tool produces output for your workflow, how often is the output usable without substantial edit? Describe a recent case."
- **Silent compliance.** "How has your actual daily workflow changed in the last 60 days as a result of the AI rollout?" with a prompt asking for specific examples.
- **Open slot.** "What is the one thing the enablement program should start, stop, or change?"

Keep the instrument to one page. Longer surveys drop the response rate and the response quality. Repeat the same instrument quarterly so you can read deltas; add one or two time-sensitive questions per quarter without displacing the standing ones.

### Reading the responses

The quantitative movement matters less than the free-text. Each response is a candidate field report; champions can be sent summary briefs of the responses from their function and asked to walk the specific issues with named operators (anonymised). This is the one case where the survey is a direct input to the field-report pipeline from [Chapter 03](03-routing-field-signal-back-to-policy-tooling-and-training.md).

### Specific intervention per pattern signal

Map each surveyed pattern back to the intervention from [Chapter 06](06-ai-specific-resistance-patterns-adkar-and-kotter.md):

- Anxiety signal rising → Kotter step-3 and step-5 interventions.
- Role-threat narrative surfacing → explicit Slot 1 / Slot 3 counter-narrative; champion-carried spotlights.
- ChatGPT-at-home signal → training-frame revision and specialist-tier routing.
- Quality skepticism signal → field-report investigation of the specific failure case; verification habits reinforced.
- Silent compliance signal → long-cadence reinforcement; champion-led retrospectives.

The survey closes the loop with the operator: the next quarter's cadence Slot 3 references the change made in response to the previous survey. "You told us the acceptable-use policy was unclear on section 4; we updated it; here is what changed." Visible attribution of survey → change is how the survey keeps its response rate.

## The dashboard

The four signals combine into a one-page dashboard the operations analyst maintains. The dashboard has four quadrants:

```
+----------------------------+-----------------------------+
| Adoption curve shape       | Champion retention          |
| per active rollout         | roster, retention, renewal, |
|                            | coverage                    |
+----------------------------+-----------------------------+
| Communications reach       | Resistance survey           |
| opens, clicks, self-serve, | pattern signals and         |
| breadth                    | deltas                      |
+----------------------------+-----------------------------+
```

Each quadrant has:

- Current value against the baseline.
- Delta from last period.
- Named concern (a sentence) if the signal is off baseline.
- Named intervention (a sentence) owned by a named person on the CoE team.

The dashboard is reviewed weekly by the ops analyst, monthly by the enablement lead, quarterly by the exec sponsor (a slice of it, inside the scorecard). The named interventions are the operating output of the dashboard — if a review produces no interventions, the dashboard is not being used to drive work.

## The combined-signal reads that matter

Two or more signals move together in ways that are more diagnostic than any single signal.

- **Adoption up, resistance survey quality-skepticism up.** The silent-compliance risk is forming. Operators are using the tool but not trusting it. Intervene before the trust gap closes toward "I'll use it badly and move on."
- **Adoption flat, champion retention normal, comms reach normal.** The tool is not finding workflow fit. The adjacent systems are healthy; the tool is the issue. Route to [mod-102](../mod-102-selecting-and-rolling-out-ai-tools/README.md) for a selection re-examination.
- **Comms reach high, adoption flat, resistance anxiety high.** The communications are landing but the resistance is holding. Likely a role-threat-narrative pattern competing with the organizational vision. Intervene in Slot 3, not Slot 1.
- **Champion retention low, resistance survey "program should change X" cluster.** The field-signal interface is failing *and* operators are surfacing structural problems directly. Both signals are pointing at a specific program issue; investigate before continuing the rollout.
- **All four signals healthy, business scorecard flat.** The change is working; the business measurement may be mis-aligned, or the behaviour change has not yet produced the business outcome. Hold the rhythms; adjust the scorecard. (See [mod-106](../mod-106-outcome-measurement-and-executive-reporting/README.md).)

The combined reads are the practice. Reading each signal alone is the training wheels; reading them together is how the role is actually done.

## What this chapter does not try to measure

Intentionally out of scope:

- **Business outcomes.** [mod-106](../mod-106-outcome-measurement-and-executive-reporting/README.md) treats these. The dashboard is a leading indicator, not a replacement.
- **Individual operator sentiment.** The survey samples; it does not track specific operators. Operator-level sentiment work belongs to HR / L&D and to the function manager, not to the CoE dashboard.
- **Vendor performance.** Vendor benchmarks and SLAs are vendor-management territory ([mod-111](../mod-111-ai-coe-operations-vendor-management-and-cross-functional-leadership/README.md)).

The dashboard is the health of the change effort. Keep it there; resist the pressure to let it eat adjacent surfaces.

## Where this chapter feeds

- [Chapter 08](08-the-handoff-to-the-governance-incident-path.md) uses dashboard signals (particularly adoption-and-skepticism combinations) as one of several triggers for the incident-path handoff.
- [mod-106](../mod-106-outcome-measurement-and-executive-reporting/README.md) treats the slice of the dashboard that appears in the executive scorecard.
- Exercise 06 asks you to design the dashboard for a specific organization and walk a combined-signal read.

## Summary

- Four signals — adoption curve shape, champion retention, communications reach, resistance survey — each cheap to instrument, each actionable on its own, more informative in combination.
- Name the adoption curve shape (S-curve, hockey stick, shark fin, flat line) to speed diagnosis; each shape has a specific intervention.
- Champion retention has four sub-metrics with specific baselines; off-baseline readings point to specific lifecycle phases needing adjustment.
- The resistance survey is short, quarterly, and attributionally referenced in the next cadence — visible response to responses is how the survey retains its response rate.
- The dashboard is one page, four quadrants, with named interventions owned by named humans. If a review produces no interventions, the dashboard is not being used.
- Combined-signal reads are the practice; single-signal reads are training wheels.
