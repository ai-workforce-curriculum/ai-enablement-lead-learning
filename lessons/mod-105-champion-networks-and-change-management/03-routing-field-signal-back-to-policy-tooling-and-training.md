# Routing Field Signal Back to Policy, Tooling, and Training

> The champion lifecycle produces signal. The question this chapter answers is *where that signal goes, in what shape, under what SLA, with what visible outcome*. Without an answer, the two-way loop collapses back into one-way broadcast — champions file reports, the reports pile up in a shared drive, and three cycles later no champion bothers filing because nothing ever came of the last five.

## The one-pipe-three-routes design

A healthy network runs a **single intake pipe** with **three downstream routes**. One pipe means champions do not have to guess which backlog their report belongs in; three routes means the signal reaches the right adjacent system without the CoE becoming a bottleneck.

- **Pipe (one):** a single field-report channel — a short form or Slack-slash-command the champion files into, with free-text and a small set of tags.
- **Routes (three):** policy ([mod-103](../mod-103-policy-co-authoring-with-governance/README.md)), tooling ([mod-102](../mod-102-selecting-and-rolling-out-ai-tools/README.md)), training ([mod-104](../mod-104-training-programs-and-ai-literacy-curriculum/README.md)). Every report is routed to at least one, sometimes two, rarely three.

The CoE's operations analyst owns the triage. The enablement lead reviews triage weekly. The champion sees the routing and the resolution on the report they filed — closing the loop at the record level is the single most important design decision in the chapter.

## The field-report form — minimum viable schema

A report is short, structured, and written at the speed of a champion between operator conversations. Longer than ten minutes of champion time and the field stops filing.

| Field | What goes in it |
|---|---|
| Date and function | Auto-filled from the champion's identity |
| Tool(s) involved | Which approved-tool envelope item(s), or "off-envelope" |
| Signal type | One of: use-case pattern, policy question, operator friction, incident-shaped observation, training gap, tool limitation |
| Narrative (2–4 sentences) | What happened, in operator language, with enough concreteness that the CoE does not have to interview the champion to triage |
| Operator identity | Whether the operator consents to being named; default is anonymous at the pipeline level |
| Recommended next step | The champion's own suggestion, which may be "I'm raising; no action proposed" |

Six fields. Not twenty. The schema is a working surface, not a compliance surface. The incident-shaped observation tag is the one that triggers the fast path to [Chapter 08](08-the-handoff-to-the-governance-incident-path.md); the rest route to the backlogs.

### Why operator anonymity, by default

An operator who worries that their name will appear on a governance ticket does not tell their champion the real story. Default-anonymous at intake, with opt-in to be named when the champion judges the report to benefit from attribution (e.g., a use-case spotlight). Two consequences:

- Champions file reports with fuller context, because they are not negotiating the attribution question in real time.
- The CoE handles the attribution decision at triage, not at the point of capture — which is the right place for it.

## The triage call — weekly, 30 minutes, same slot

The operations analyst runs a standing weekly triage. The enablement lead attends. Standing agenda:

1. New reports since last call. Routing decision for each — policy, tooling, training, or incident path. A report that lands in the incident queue follows the Chapter 08 path immediately; everything else waits for triage to assign it a route.
2. Cross-report patterns. Three reports from different functions about the same issue is a different signal than one report about one issue; patterns get a different disposition.
3. Open items from prior calls. What has moved; what has not; who owns it next.
4. Named-attribution queue. Any report where the operator opted in, now being reviewed for spotlight or scorecard surface.

A report leaves triage with:

- A route — one of policy, tooling, training, incident.
- A named ticket in the destination backlog, with the field report quoted (the quote is important; downstream owners work from the operator's language, not the CoE's paraphrase).
- A reply to the filing champion — one or two sentences, within 24 hours. "Routed to the policy backlog, ticket POL-247; I'll come back to you on the resolution."
- A date by which the champion will hear the outcome. Default: 30 days for policy and training; variable for tooling depending on rollout cycle.

Thirty minutes is a hard cap. If the weekly triage regularly overflows, the pipe volume has outstripped the CoE's triage capacity; the response is to adjust the intake friction up, not to extend the meeting.

## Route 1 — into the policy backlog (mod-103)

A report is routed to policy when it surfaces a gap or ambiguity in the acceptable-use policy ([mod-103 Chapter 04](../mod-103-policy-co-authoring-with-governance/04-the-one-page-acceptable-use-policy.md)), the data-handling SOP ([mod-103 Chapter 05](../mod-103-policy-co-authoring-with-governance/05-the-data-handling-sop.md)), or the intake questionnaire ([mod-103 Chapter 06](../mod-103-policy-co-authoring-with-governance/06-the-intake-questionnaire.md)).

What the CoE does with it:

- The ticket enters the **walking-redline backlog** that the enablement lead works with the `head-of-ai-governance` on a recurring cadence (from [mod-103 Chapter 01](../mod-103-policy-co-authoring-with-governance/01-the-co-author-posture-and-the-redline-log.md)).
- Field-report-sourced items get a "field" tag so the redline log shows the *provenance* of each change. This is the attribution surface the retirement artifact and the recognition program ([Chapter 02](02-the-four-phase-lifecycle-recruit-train-recognise-retire.md)) reference.
- Resolved items produce a specific change — a policy section revised, a new row in the data-class table, a new intake question — and the reporting champion is notified with the change and the ticket.

**The anti-pattern to avoid:** treating field reports as grievances to be acknowledged rather than as inputs to the backlog. "Thank you for the feedback, we've noted it" without a ticket, without a route, without a date — that is the shape that breaks the loop within two quarters.

## Route 2 — into the tooling backlog (mod-102)

A report is routed to tooling when it surfaces a gap in the approved-tool envelope ([mod-102 Chapter 01](../mod-102-selecting-and-rolling-out-ai-tools/01-the-three-stage-selection-decision.md)), an unmet workload that champions keep seeing operators try to solve off-envelope, or a limitation in an in-envelope tool.

What the CoE does with it:

- Off-envelope-use reports feed the **Stage 1 candidate intake** — the list of workloads the envelope needs to grow into. [mod-102 Chapter 02](../mod-102-selecting-and-rolling-out-ai-tools/02-designing-bounded-pilots.md) treats the pilot design these candidates feed.
- Tool-limitation reports route to the vendor through the vendor relationship manager; the CoE does not negotiate product features directly but does keep an aggregated record that becomes vendor-management leverage at renewal (see [mod-111](../mod-111-ai-coe-operations-vendor-management-and-cross-functional-leadership/README.md)).
- Workloads that cross multiple functions get escalated to the pilot backlog with higher priority than single-function workloads — a multi-function signal is already an organizational one.

The visible outcome the champion sees is slower here than policy — tool adoption and procurement cycles are quarters, not weeks — but the loop still closes: "pilot PIL-18 is now running on your reported workload; you are invited to the pilot cohort."

## Route 3 — into the training backlog (mod-104)

A report is routed to training when it surfaces a fluency gap — an operator pattern that the role-based playbook ([mod-104 Chapter 04](../mod-104-training-programs-and-ai-literacy-curriculum/04-role-based-playbooks-and-use-case-libraries.md)) does not yet cover, a use case that belongs in the use-case library, a prompt pattern that wants to go in the library, or a misunderstanding of the policy that keeps recurring.

What the CoE does with it:

- Use-case and prompt-library gaps route to the **playbook owner** for the function, who adds the material to the next quarterly playbook rev. The champion whose report sourced it is a named contributor to the update.
- Recurring misunderstandings of policy route to the training side *and* loop back to Route 1 — a misunderstood policy is sometimes a signal that the policy itself is unclear.
- A report that belongs in a spotlight ([mod-104 Chapter 05](../mod-104-training-programs-and-ai-literacy-curriculum/05-the-delivery-mix.md)) routes to internal comms for the production pipeline.

A gap in the training content is usually the fastest-closing route; the playbook rev cycle is quarterly and the use-case library is near-continuous.

## The cross-routing cases

Some reports hit two routes. A typical case: a champion reports that operators in their function keep asking whether they can paste customer data into a specific approved tool, the policy is unclear on it, and the training content does not demo the policy-compliant workflow. That report:

- Routes to policy for an AUP / SOP clarification.
- Routes to training for a playbook update that demos the clarified workflow.
- Does **not** route to tooling, because the tool itself is fine; the gap is in the artifacts around it.

The triage call explicitly names cross-routing and attaches both tickets to the source report. Downstream, the two owners coordinate — because the policy change and the training change *must ship together* ([mod-103 → mod-104](../mod-103-policy-co-authoring-with-governance/README.md) is the coupling chain). The common failure is that the policy ships and the training does not; operators then learn the new policy from the old training material, which is worse than no policy change at all.

## Closing the loop at the record level

The phrase "closing the loop" is overused. Here it has a specific meaning: **the filing champion sees, in the record of the report they filed, the resolution** — the ticket number, the destination backlog, the final disposition, and (where applicable) the shipped artifact. One screen, one scroll.

The alternative — an acknowledgment that trails off into the shared drive — is what produces the evangelist and crickets failure modes from [Chapter 01](01-the-champion-network-as-a-change-management-asset.md). Champions file as long as filing *produces something they can see*. Remove the visibility and filings dry up within one quarterly cycle.

Two operational commitments make this real:

- **Each field report has a unique ID**, visible to the champion, referenced in the destination ticket.
- **Resolution updates to the destination ticket post back to the source report**, so the champion does not have to click through to another system to see the outcome.

The analyst who builds this is the same operations analyst from [mod-101 Chapter 03](../mod-101-role-and-the-org-wide-enablement-operating-model/03-authoring-the-enablement-operating-model.md). It is a thin piece of infrastructure — a spreadsheet, a Notion database, a lightweight workflow in the existing ticketing tool — and it is worth building properly.

## The attribution surface

Every quarterly recognition cycle produces a field-report attribution report:

- Which policy changes shipped this quarter sourced from field reports.
- Which playbook updates shipped from field reports.
- Which pilots were triggered by field reports.
- Named champions whose reports contributed.

The report is short — one page. It appears in the quarterly executive scorecard inputs ([mod-106](../mod-106-outcome-measurement-and-executive-reporting/README.md)) *and* in the recognition surface from [Chapter 02](02-the-four-phase-lifecycle-recruit-train-recognise-retire.md). Two audiences see the same artifact: the exec sees the field-signal engine is producing changes; the champion sees their own name attached to a change.

## What *not* to route

Not every piece of signal belongs in the pipe. Three categories route elsewhere on purpose:

- **Grievances about a named colleague.** These belong in HR, not in the field-report pipe. A champion who files one gets a conversation with the CoE about the routing, not a ticket.
- **Confidential business signal.** A champion who hears executive-level restructuring in their function should not be reporting it through the champion pipe. The CoE is not the right recipient; the champion's own management chain is.
- **Vendor marketing requests.** A vendor who has asked a champion to surface their new feature is a vendor-management conversation, not a tooling-backlog ticket.

Each of these filters exists because the pipe's trust and signal-to-noise ratio depend on it carrying actual field signal.

## Instrumenting the loop

Three measurements, surfaced in the health dashboard from [Chapter 07](07-measuring-change-management-health.md):

- **Filings per champion per quarter.** A healthy active champion files roughly two to six times per quarter. Zero is a crickets signal; above ten is either a social-club pattern or a function with a real surge the centre needs to engage with.
- **Time-to-first-response.** The 24-hour reply commitment is a hard target. Weekly aggregate time-to-first-response tells you whether the triage is holding.
- **Time-to-resolution by route.** Policy, tooling, training each have their own expected cycle time; drift from the baseline on any route signals a specific adjacent-system bottleneck.

The three together are the operational health of the loop. They are different from the network health metrics in Chapter 07 — those measure the asset; these measure the routing.

## Where this chapter feeds

- [Chapter 04](04-the-rollout-communications-cadence.md) uses the attribution surface as content for the "what is working" slot of the quarterly cadence.
- [Chapter 07](07-measuring-change-management-health.md) treats the three loop metrics as part of the health dashboard.
- [Chapter 08](08-the-handoff-to-the-governance-incident-path.md) treats the incident-shaped tag as the trigger for the fast path.
- Exercise 02 walks you through a two-way feedback-loop drill grounded in this chapter.

## Summary

- One intake pipe, three downstream routes — policy, tooling, training — plus a fast path to the incident queue for incident-shaped signal.
- The field-report form has six fields, not twenty. Default-anonymous at the operator level; opt-in to attribution.
- The weekly 30-minute triage produces a route, a destination ticket, a reply to the filing champion inside 24 hours, and a target resolution date.
- The three routes each have their own cycle time and failure mode; cross-routed reports require coordinated shipping between policy and training.
- Closing the loop means the champion sees, in their own report record, the resolution. If this breaks, the pipe dries up inside a quarter.
- The quarterly attribution surface is the artifact that both the exec scorecard and the champion recognition program read from.
- Three operational measurements — filings per champion, time-to-first-response, time-to-resolution by route — are the loop's health signals.
