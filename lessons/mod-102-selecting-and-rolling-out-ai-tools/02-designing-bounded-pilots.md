# Designing Bounded Pilots with Pre-Written Decision Criteria

> "The pilot went well" is not a sentence this role is allowed to say. If "well" wasn't written down before the pilot started, what you have is a feeling, not a decision.

## Why the pilot-charter artifact exists

A pilot without a written charter is a vibe. It will produce stories, screenshots, and a slide titled *Early Wins*, and six weeks after the timebox ends, nobody will be able to tell you whether to adopt the tool, extend the trial, or kill it. The charter is the artifact that forces that answer.

The charter has exactly five sections. Keep it to one page:

1. **Cohort** — who is in the pilot, and why they are representative.
2. **Duration** — a specific start date and end date.
3. **Baseline** — what was measured before the pilot started, and over what window.
4. **Decision criteria** — the pre-written thresholds for adopt, extend, and kill.
5. **Kill switch** — the specific condition under which the pilot ends early, and who pulls it.

If you cannot write a one-page charter, you are not ready to run the pilot. That is a feature of the artifact, not a defect.

## Cohort — representative, not friendly

The single most common cohort mistake at this level is piloting with champions who would succeed with a potato. If your cohort is five AI-curious engineers who already pay for a personal subscription to the tool, you have not learned anything about whether the broader organization will adopt it — you have learned that your friends like the tool.

A defensible pilot cohort looks like the population you intend to roll out to. That means:

- A mix of skill levels, not just the top quartile.
- At least one sceptic, ideally two. If every participant volunteered eagerly, the cohort is not representative.
- A workflow surface that touches more than one function, if the eventual rollout will.
- Named participants, not a mailing list. "The marketing team" is not a cohort; twelve named people are.

Cohort size is a trade-off. Big enough to generate signal — a cohort of three cannot distinguish a trend from a mood. Small enough to be reversible — a cohort of three hundred is not a pilot, it is a rollout you forgot to charter. A common working range sits somewhere between those extremes; the right number is the one where you can still pull the kill switch without a change-management campaign.

## Duration — the forcing function of a short timebox

Pilots need an end date for the same reason sprints do: without one, nothing produces a decision. Open-ended pilots silently become permanent. The tool stays in the environment, the contract auto-renews, the "we're still evaluating" line gets used for a second year, and the organization never actually chose anything.

A common working range for a bounded pilot is four to twelve weeks. Shorter than four and you will not clear the learning curve — participants are still fighting the UI, not using the tool. Longer than twelve and the timebox stops being a forcing function; the pilot becomes the default state.

Pick a date. Put it in the charter. Put it on the calendar invite for the decision meeting. The decision meeting exists before the pilot starts — that is the point.

## Baseline — measured before, not after

"We didn't baseline" is the single most common reason a pilot ends inconclusive. The pattern is familiar: the pilot runs, participants report feeling faster, someone pulls a vanity metric at the end, nobody can say whether the number is better or worse than before, and the meeting ends with "let's extend for another quarter."

Baseline measurement has two parts, and both matter:

- **What you measure.** Pick two or three metrics that will still mean something after the pilot ends. Time-to-complete on a defined task, defect rate on a defined artifact, throughput on a defined queue. If you cannot name the metric in one sentence without adjectives, it is not a metric yet.
- **The window you measure over.** A single week of baseline is weather, not climate. The baseline window should be long enough to absorb the normal variance of the work — often a window comparable to the pilot duration itself. A four-week pilot with a two-day baseline is not a comparison; it is a coincidence.

Baseline before the pilot starts. Not the week it starts. Before.

## Pre-written decision criteria — adopt, extend, kill

The anti-pattern here is universal and must be refused by name: writing success criteria *after* you see the results. Anyone can draw the target around the arrow. The charter exists so you cannot.

At the pilot-start meeting, write three thresholds into the charter. Each one must be concrete — a number, a range, or a specifically-worded condition that an outside reader could evaluate without asking you what you meant.

- **Adopt** — the condition under which the tool graduates into the approved-tool envelope and moves into a broader rollout. Example form: *measured metric moves by at least X% against baseline, with participant satisfaction above Y, and zero unresolved security findings.*
- **Extend** — the condition under which the pilot earns one more defined window (and only one). Extend is a narrow lane, not an escape hatch. Example form: *signal is directionally positive but under the adopt threshold, AND a specific hypothesis about why is testable in the extension.*
- **Kill** — the condition under which the tool exits the environment. Example form: *metric regresses against baseline, OR an unresolved security/compliance finding, OR participant abandonment above Z%.*

Write these at the start. Sign them at the start. Reread them at the decision meeting. If the data does not clearly fall into one of the three buckets, the charter was not specific enough — fix that next time and default to kill or extend-once, never to drift.

## The rule, stated plainly

If "well" is not a pre-written threshold, the pilot has produced vibes, not a decision. The AI Enablement Lead at level 45 does not forward vibes to the executive scorecard. The charter is what keeps that promise.

## A brief illustrative pilot charter

Generic, not a real organization. Shown to illustrate shape, not to be copied verbatim.

> **Tool:** Vendor X code-assistant, Team plan.
> **Cohort:** Twelve named engineers across three product squads — four senior, six mid, two junior; two self-identified sceptics included. Opt-out permitted; replacements drawn from the same mix.
> **Duration:** Eight weeks. Start: first Monday of the quarter. Decision meeting: the Thursday after the end date, on the calendar now.
> **Baseline:** Measured over the eight weeks prior to start. Metrics: median pull-request cycle time on the three squads' repos; escaped-defect rate on the same repos; weekly self-reported friction score on a four-item survey.
> **Adopt:** Median PR cycle time improves by at least 15% against baseline, escaped-defect rate does not regress, friction score median is 4 or better out of 5, zero unresolved findings from the security review.
> **Extend (once, for four weeks):** Cycle-time improvement is between 5% and 15% AND a named hypothesis explains the shortfall AND the security review is clean.
> **Kill:** Any of — cycle time regresses, escaped-defect rate regresses, friction score median below 3, an unresolved high-severity security finding, abandonment above 25% of the cohort.
> **Kill switch:** The AI Enablement Lead pulls the pilot early on any security finding rated high or above, or on abandonment crossing the kill threshold, without waiting for the decision meeting.

One page. Five sections. Signed by the Enablement Lead, the sponsoring function lead, and the security reviewer before the first login is provisioned.

## Summary

- The pilot-charter artifact has five sections — cohort, duration, baseline, decision criteria, kill switch — and fits on one page.
- Cohorts must be representative, not friendly; size them big enough for signal and small enough to reverse.
- Duration is a forcing function; a bounded timebox (commonly four to twelve weeks) is what turns a pilot into a decision instead of a drift.
- Baselines are measured before the pilot starts, over a window long enough to absorb normal variance, on metrics specific enough to still mean something at the end.
- Adopt / extend / kill thresholds are written at the start, not the end; "the pilot went well" is not a sentence this role is allowed to say.
