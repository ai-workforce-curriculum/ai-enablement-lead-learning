# Failure Modes and the Pre-Mortem That Preempts Them

> Every rollout that quietly dies at six months died, in form, on day one. Someone in the room already knew. The pre-mortem is the artifact that makes them say it out loud, before the contract is signed and the comms go out.

A rollout almost never fails for a reason nobody could have seen. It fails along one of a short list of named patterns that the `ai-enablement-lead` at level 45 is paid to recognise on sight. This chapter catalogs the four that show up most often in the sampled role postings, and gives you the pre-mortem drill that forces each one into the open before launch.

If a candidate rollout cannot survive the pre-mortem, it should not get the pilot slot. That is the whole point of running the drill at the end of Stage 3 of selection (Chapter 01).

## The ghost-user rollout

**What it looks like.** Licences are provisioned for 4,000 people. SSO is live. The vendor dashboard shows 60 active users in week four. By week twelve the number is 45. The tool is "rolled out." Nobody opens it.

**Why it happens.** The rollout bought licences and shipped an email. It did not ship a reason to open the tool on Monday morning. There was no training package pinned to a pre-committed use case, no champion to answer the first awkward question, no launch comms that said *here is what to do with this tool before lunch today*.

**Pre-mortem prompt.** *"It is six months from now. 4,000 people have the licence. 50 are using it. Where did the first-week user drop out?"* If the answer is "we assumed curiosity would carry them," you do not have a rollout plan.

**Preempting artifact.** The launch artifact set from Chapter 03 — the training package, the named champion list, and the use-case-pinned launch comms — must exist *before* licences are turned on. The service-catalog entry for the tool names the first three use cases the champions have personally run. Launch comms point at those use cases, not at the tool's feature list.

## The metric-theatre pilot

**What it looks like.** The pilot report is beautiful. Daily active users up and to the right. Prompts-per-user up and to the right. NPS at 72. The executive scorecard is green. The underlying business outcome — cycle time, resolution rate, revenue per rep, defect escape rate — has not moved, or nobody knows because it was never measured.

**Why it happens.** Usage metrics are easy to pull from the vendor console. Outcome metrics are hard — they require instrumentation, a baseline, and a named owner in the business unit. Under deadline pressure the pilot ships with the easy numbers and quietly drops the hard ones. The scorecard becomes a story about the tool rather than a story about the work.

**Pre-mortem prompt.** *"It is six months from now. Adoption numbers are excellent and the sponsoring VP has cancelled the renewal. Why?"* The answer is almost always: because the thing the VP cares about did not change, and the adoption numbers never claimed it would.

**Preempting artifact.** The outcome metric is named in the pilot charter (Chapter 02) *before* the pilot starts, with a baseline value, a target delta, a measurement method, and a named BU owner who signs that they can produce the reading. The measurement layers from Chapter 04 — leading-indicator usage, lagging outcome, counterfactual where available — are wired in at provisioning, not retrofitted at month five.

<!-- needs-research: sampled postings' language on "outcome vs adoption metrics" — pull direct phrasings for the resources file. -->

## The champion-of-one

**What it looks like.** The rollout is going well. One person in the sponsoring BU is a force of nature — runs the office hours, answers every Slack question, builds the internal prompt library, demos at the town hall. Then they take a new role, go on leave, or burn out. Within a month, usage flatlines. Within a quarter, the tool is a line item nobody defends at renewal.

**Why it happens.** Champions are easy to acquire one at a time and hard to acquire in a network. The first volunteer absorbs all the load and the operating model never pushes back on that. There is no named second, no written playbook they could hand to a successor, no retention plan for the person carrying the program.

**Pre-mortem prompt.** *"It is six months from now. [Named champion] has moved to a new role. The rollout in their BU has collapsed. What did we not build?"*

**Preempting artifact.** A named champion list with strictly more than one champion per business unit or function at launch, each with a written remit, a time allocation their manager has signed, and a retention plan (recognition, role weight, promotion signal). Depth on *how* to build and run the network sits in mod-105; the pre-mortem contribution here is simply the hard gate: *no rollout clears Stage 3 with a champion list of one.*

## The policy-after-rollout retrofit

**What it looks like.** The tool is live. A sensitive-data leak, a hallucinated customer email, or a contract clause drafted against policy lands on the general counsel's desk. For the next two weeks, the `ai-enablement-lead` is writing the use policy, the data-handling guidance, and the escalation runbook under executive pressure, in public, with the tool still running.

**Why it happens.** Selection was run as a procurement exercise. The artifact set — approved-use policy, data-handling guidance, prompt hygiene guide, escalation path, kill-switch owner — was treated as something to "follow up on after launch." The approved-tool envelope (Chapter 01, Stage 2) was defined loosely enough that a tool without the artifact set could still clear the gate.

**Pre-mortem prompt.** *"It is six months from now. An incident has forced us to write the use policy in forty-eight hours. Which artifact did we skip at launch?"*

**Preempting artifact.** The artifact set from Chapter 03 exists, is linked from the service-catalog entry, and is referenced by the launch comms — *at launch, not after it*. Stage 2 of selection (Chapter 01) blocks any candidate that cannot yet fit the approved-tool envelope: no artifact set, no pilot. Incident-response operations and kill-switch mechanics themselves are mod-109; the pre-mortem's job here is only to make sure the artifacts are standing at t-zero.

## The pre-mortem as a one-page artifact

The pre-mortem is run once, at the end of Stage 3 of selection, immediately before the pilot-vs-rollout commit. It produces one page.

The prompt is a single sentence:

> *Imagine it is six months from now and this rollout has quietly failed. Write the three sentences that explain why.*

Three sentences, not a paragraph. Not "various adoption challenges." Specific. Named. If the three sentences are vague — "adoption was slower than expected," "the vendor underdelivered," "the business was not ready" — re-run the exercise. Vague pre-mortem sentences are the single most reliable leading indicator of a rollout that will fail for exactly the reason nobody could quite articulate in the room.

The output of a good pre-mortem is a specific failure mode mapped to one of the named patterns above (or a new one), a preempting artifact, and a named owner for that artifact. If the artifact does not exist yet, Stage 3 has not cleared.

## How to run the pre-mortem meeting in 45 minutes

The meeting is small and disciplined.

- **Attendees.** The `ai-enablement-lead`, the sponsoring BU owner, the champion lead for that BU, a governance representative (per the handoff map in mod-101), and one skeptic — someone known to have reservations about the rollout. Five to seven people. Not a town hall.
- **Minutes 0–5.** The lead reads the prompt. No discussion.
- **Minutes 5–20.** Everyone writes their three sentences *in silence*, individually. No whiteboard. No talking. Individual writing before group discussion is the whole technique — it is what keeps the quiet skeptic's view from being absorbed into the sponsor's optimism.
- **Minutes 20–40.** Each attendee reads their three sentences aloud. The lead captures them verbatim. Cluster by named failure mode as you go.
- **Minutes 40–45.** For every cluster, name the preempting artifact and its owner. If the artifact does not exist, the rollout does not clear Stage 3.

Write-up format: one page. Three sections — *what we think will kill it*, *the preempting artifacts and owners*, *the commit*. Sign it. File it next to the service-catalog entry.

## The feedback loop

Every real rollout that fails, or nearly fails, gets a post-mortem in the ordinary way. The non-ordinary part is this: every confirmed failure mode from a post-mortem folds back into the pre-mortem catalog for the next rollout. The four named patterns in this chapter are a starting set, not a closed list. An operating model that has been running for two years should have added at least two of its own.

That feedback loop — post-mortem out, pre-mortem catalog updated, next rollout screened against the new mode — is how the enablement operating model stops repeating the same failure with a different vendor logo on it.

## Summary

- Rollouts fail along a short list of named patterns: the ghost-user rollout, the metric-theatre pilot, the champion-of-one, the policy-after-rollout retrofit.
- Each mode has a preempting artifact that must exist at launch — training-and-champion-and-comms bundle, outcome-metric charter, >1-champion list with retention plan, approved-tool artifact set.
- The pre-mortem is a one-page drill run at the end of Stage 3: three specific sentences on why this rollout will have quietly failed in six months. Vague sentences mean re-run.
- Run the meeting in 45 minutes with five to seven people, individual writing before group discussion, and a named artifact owner per clustered failure mode.
- Fold every real post-mortem back into the pre-mortem catalog. The four named patterns are a starting set, not a closed list.
