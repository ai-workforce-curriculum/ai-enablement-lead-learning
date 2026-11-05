# Measuring Whether the Rollout Changed Anything Real

> Nine months in, the CFO asks one question: "What changed?" If the answer is "92% of licensed users logged in last week," you have already lost the meeting. Logins are not change. The target task getting faster, better, cheaper, or less error-prone is change.

## The three measurement layers, in priority order

A rollout's measurement plan has three layers. The order matters. Most programs at this level get it backwards — they start with telemetry because the vendor admin panel hands it to them, and they never climb back to the outcome. Run it the other way.

1. **Outcome metrics on the target task.** Did the target task get faster, better, cheaper, or less error-prone? This is the only layer that answers the CFO's question.
2. **Workflow interviews.** Short structured conversations with named users about how they actually use the tool. Qualitative ground truth. The only layer that tells you *why* the outcome did or did not move.
3. **Usage telemetry.** Seats, logins, prompts per day, active users. A sanity check. Never an outcome.

If you can only invest in two of the three, drop telemetry. It is the cheapest layer to produce and the least defensible on its own.

## Layer 1 — outcome metrics on the target task

Every approved rollout went through pilot with a stated target task. (If it didn't, that is a Chapter 02 failure — go back and fix it.) The outcome metric is whatever measures that task directly, before the tool and after the tool, on comparable work.

Framed by task class:

- **Drafting** — time from blank page to accepted first draft; acceptance rate from reviewer on first pass; rework hours after review.
- **Summarization** — time to produce a summary a stakeholder acts on; disagreement rate between the summary and the source when spot-checked.
- **Retrieval / internal search** — time to find the right document; rate at which users escalate to a human because they could not find the answer.
- **Support-ticket resolution** — handle time; first-contact resolution rate; re-open rate within N days.
- **Code review** — time to first comment on a PR; rate of defects caught before merge; rate of defects caught after merge (the metric that actually matters).
- **Meeting notes** — time from end-of-meeting to notes shared; rate at which action items from notes are completed.

These are shapes, not numbers. <!-- needs-research: internal baselines for each task class, measured on comparable work before rollout --> Do not borrow a vendor's published number for your scorecard. You do not know what workflow produced it.

Two rules that keep this layer honest:

- **Measure before.** If there is no pre-rollout baseline for the target task, the post-rollout number is a vanity number. Build the baseline in pilot (Chapter 02) and carry it into rollout.
- **Measure comparable work.** A 30% speedup on tickets that got simpler is not a 30% speedup from the tool. Hold the work shape constant, or at minimum annotate shifts in it.

## Layer 2 — workflow interviews as qualitative ground truth

Numbers tell you *that* something moved. Interviews tell you *why*, *for whom*, and *where the tool misbehaves in ways the dashboard will never surface*. This is the layer the metric-only programs skip, and it is the one that saves you when the number is ambiguous.

Shape of the interview:

- 20–40 minutes, named user, scheduled on a cadence (monthly for a flagship rollout, quarterly for the long tail).
- Four questions, every time: *What did you use the tool for this week? What did it replace? What did it add that wasn't there before? Where did it misbehave or where did you stop trusting it?*
- Transcribed, tagged, and read in aggregate. Patterns across users are the finding; a single quote is an anecdote.

Minimum sample for an org-wide rollout: **every role that touches the tool, every BU that adopted it.** If the tool rolled into legal, sales, and engineering across three BUs, you need coverage in each of the nine cells, not three interviews total from the loudest users. Loud users bias toward wins; the signal is often in the quiet ones.

A sign the interviews are working: they surface problems the telemetry cannot see. Users rebuilding their own prompt libraries on the side. A workflow the tool was supposed to replace that is still happening in a shadow spreadsheet. A role that abandoned the tool in month two but keeps the license.

## Layer 3 — usage telemetry as sanity check only

Seats assigned, licenses active, logins per week, prompts per day, DAU/MAU. The vendor hands this to you. It is cheap, it is high-resolution, and it is dangerous when it is the only thing you report.

Use it for three things, and three things only:

- **Did the floor hold?** If DAU collapsed in week six, something broke — go find out what.
- **Where is the dark matter?** Which BUs have licenses but near-zero usage? That is a workflow-interview target, not a scorecard bullet.
- **Is the spend wasted?** Unused seats are a reclaim list, not a success metric.

Ninety-five percent of licensed users opening the tool daily means **nothing** if the target task did not move. A room full of people clicking around in a UI is not a productivity gain. State this out loud in every exec readout. If you don't, someone will quote the 95% back at you in six months as proof the program worked, and then the outcome metric will land and you will be explaining the gap on your heels.

## The metric-theatre pilot — the failure mode to name

The most common failure at this level has a name. **Metric theatre**: reporting adoption percentage and prompts-per-day because they moved, while the outcome metric on the target task either did not move, was never baselined, or was quietly dropped from the readout. It is easy to fall into because the telemetry is pre-wired and the outcome metric is work. It is the hardest thing to defend to a CFO who has seen this pattern before at other companies.

Signs you are in it:

- Your weekly readout opens with a usage chart.
- Your outcome metric is described in words instead of numbers.
- The pilot's baseline is not on the slide.
- Nobody on the call can state the target task in one sentence.

How to get out of it is the whole of Chapter 05 — the explicit kill, pause, or scale decision based on whether the outcome actually moved. This chapter is the measurement; Chapter 05 is what you do with it.

## Composing with mod-106

This chapter sets **what you measure per rollout**. [mod-106](../mod-106-outcome-measurement-and-executive-reporting/README.md) is where the per-rollout measurements get composed into a weekly executive page — which rollouts are on the page, how they are aggregated, which metrics the CAIO and CFO actually see. Do not design the exec scorecard here. Design the per-rollout measurement so that mod-106 has something true to aggregate. If the inputs to the scorecard are theatre, the scorecard is theatre.

Similarly, cost attribution and ROI math belong in [mod-107](../mod-107-budget-roi-and-build-vs-buy-at-org-scope/README.md). "Minutes saved per ticket" is an outcome metric. "Dollars of value per quarter" is a mod-107 calculation that sits on top of the outcome metric. Keep them separate; they fail in different ways.

## The literature to read for method, not numbers

There is a growing empirical literature on AI productivity gains. Read it for *how* credible measurement is constructed — control groups, baselines, task selection, selection bias — not for numbers to paste into your scorecard. The headline numbers are context-specific; the methods travel.

- Peng et al., "The Impact of AI on Developer Productivity" (arXiv:2302.06590).
- Noy & Zhang, "Experimental Evidence on the Productivity Effects of Generative Artificial Intelligence" (Science, 2023).
- Dell'Acqua et al., "Navigating the Jagged Technological Frontier" (HBS working paper).
- Brynjolfsson, Li, and Raymond, "Generative AI at Work" (NBER).

<!-- needs-research: current URLs, exact publication dates, and any updates / retractions across these four papers at time of module publication --> Cite them by title when you train your team on measurement method. Do not cite their numbers in your own program's scorecard — different tasks, different populations, different baselines.

## Summary

- Measure the rollout in three layers, in this order: outcome metrics on the target task, workflow interviews, usage telemetry as a sanity check.
- Outcome metrics require a pre-rollout baseline on comparable work. Without it, the post number is a vanity number.
- Workflow interviews cover every role and every BU, on a cadence, with the same four questions each time — they tell you *why* the number moved.
- Telemetry is a sanity check, not an outcome. Ninety-five percent login rate proves nothing about the target task.
- Metric theatre — adoption up, outcome flat or unbaselined — is the named failure mode at this level; compose this chapter's measurement into mod-106's exec scorecard and mod-107's ROI math, not the other way around.
