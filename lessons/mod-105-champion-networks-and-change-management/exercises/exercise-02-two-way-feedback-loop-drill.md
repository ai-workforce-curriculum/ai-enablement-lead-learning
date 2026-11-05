# Exercise 02 — Two-Way Feedback Loop Drill

**Estimated effort:** 2.5 hours
**Format:** one working artifact (table + short notes), 2–3 pages
**Grounding chapter:** [03 — Routing Field Signal Back to Policy, Tooling, and Training](../03-routing-field-signal-back-to-policy-tooling-and-training.md)

## Objective

Operate the one-pipe-three-routes design against a batch of realistic field reports. Produce the triage output, the routing decisions, the destination-ticket drafts, and the champion-facing replies as if you were running the weekly 30-minute triage. The exercise trains the specific judgment the role requires: routing quickly, reasoning cross-route couplings, preserving operator anonymity, and closing the loop at the record level.

## Prerequisites

- Chapter 03 read.
- Exercise 01 completed (or at minimum the champion-network design from it — the exercise assumes a network exists against which champions file reports).
- Familiarity with the acceptable-use policy stub from [mod-103 Exercise 01](../../mod-103-policy-co-authoring-with-governance/exercises/exercise-01-one-page-acceptable-use-policy-drill.md) and the approved-tool envelope from mod-102. Draft versions are fine.

## Problem statement

It is Monday morning. Six field reports have come into the pipe since last week's triage. Run the triage: produce the routed output, the destination tickets, the champion-facing replies. Flag the cross-routes, flag the attribution surface candidates, flag the one that should move to the incident path. Do this in the 30 minutes the standing meeting lasts.

## The six field reports

Treat these as the reports the champions filed. The reports are deliberately a mix — some need policy work, some tooling, some training, some are cross-routed, one is incident-shaped.

### Report A — Sales Operations, filed by Priya

> Three operators in enterprise sales asked this week whether they can paste prospect email threads into the approved writing assistant to draft follow-up emails faster. Our AUP says "no customer data" but these are *prospect* conversations before any contract exists — same tool, same workflow, unclear policy. I'm not sure what to tell them and I think the answer varies by jurisdiction.

### Report B — Legal Operations, filed by Marcus

> Operator reports that the approved contract-redline assistant produced a clause reading "shall not exceed" where the attorney's own draft said "shall not materially exceed." The operator submitted it to counsel unchanged; counsel caught it; the attorney is now skeptical of the tool. I verified the model's output on the same input and got the same error. The attorney's reasoning on the "materially" qualifier is a real distinction the tool is flattening.

### Report C — Customer Service, filed by Jenna

> Operators are using a personal ChatGPT account to draft responses to difficult tickets because the approved tool's turnaround is slower when the ticket is long. I know two operators who do this; there are probably more. One of them pasted a ticket containing the customer's full name and address last Wednesday.

### Report D — Supply Chain, filed by David

> Operators in logistics planning are trying to use AI for carrier-rate analysis. The approved envelope has nothing for this; they tried the general writing assistant and are getting useless results. I think there's a workload here that we don't have a tool for.

### Report E — Product Management, filed by Sana

> Our role-based playbook has four use cases for PMs. In the last month, I've had six different PMs ask about generating draft user-interview synthesis from raw notes — not in the playbook. All approved tools handle this well; we just don't have the use case written up, and PMs are reinventing the prompt pattern each time.

### Report F — Supply Chain, filed by David

> Second report from me. One of the planners mentioned they've been using the approved writing assistant to draft replies to supplier escalations, and that last month the tool "confidently invented" a contract clause number that doesn't exist, which the planner caught before sending. The planner shrugged it off; I don't think they realise how close that was to a real problem.

## Requirements

### 1. The triage table (the primary artifact)

| Report ID | Signal type | Primary route | Secondary route (if cross-routed) | Destination ticket ID | Attribution candidate? | Incident path? |
|---|---|---|---|---|---|---|
| A | | | | | | |
| ... | | | | | | |

Fill one row per report. Keep ticket IDs lightweight (POL-01, TOOL-01, TRAIN-01, INC-01). Attribution candidates are reports that would show up in the quarterly attribution surface for recognition.

### 2. Destination ticket drafts (two sentences each)

For each unique destination ticket, draft the two-sentence content: what the operator-language signal is, what the requested action is, and which champion sourced it. The two sentences become the body of the ticket in the adjacent-system backlog.

### 3. Champion replies (one sentence each)

For each of the six champions, draft the one-sentence reply that goes back to them inside 24 hours. Include the routing, the ticket IDs, and the target resolution date.

### 4. Cross-routing notes (short paragraph)

For reports that cross-routed, write a short paragraph on the specific coupling. What must ship together? Who coordinates between the two owners?

### 5. The incident flag (short paragraph)

Which report is incident-shaped? What makes it so? Which named owner on the governance side does it go to in the 30 minutes after the triage? (Use the handoff sequence from [Chapter 08](../08-the-handoff-to-the-governance-incident-path.md).)

### 6. Anonymity decisions

For each report, is the operator anonymised at the triage level, or is attribution appropriate? Default is anonymous; opt-in only where the operator consented and the report is a candidate for a use-case spotlight.

## Starter guidance

- Resist the urge to triage based on the champion's suggested next step. The champion suggests; the triage decides. Reports B and C in particular have different right routes than the champion's own reading might suggest.
- Cross-routes are common; the cost of recognising one late is high. Scan for the "the policy is unclear *and* the training doesn't demo the right workflow" pattern before finalising single-route decisions.
- The incident-shaped signal in this batch is the one where the data and the behaviour combined are already on the wrong side of policy. The champion did not tag it; one of your jobs is to recognise it anyway.
- The two reports from the same champion (D and F) are a modeling choice; they show that a healthy network has a steady filing rhythm, not a single annual report per champion. In the triage, the two reports are evaluated independently.
- Timing is a real constraint. The 30-minute triage is the forcing function. If your triage output takes an hour to produce, the design is wrong for the real cadence.

## Deliverables

- `triage-output.md`: the five sections above, in order.
- A short **meta-note** (3–5 sentences) at the bottom reflecting on what the drill surfaced about your own triage judgment — where you hesitated, which cross-route was non-obvious, which ticket draft felt too generic.

## Acceptance criteria

- All six reports routed; no report left without a primary route.
- At least one cross-routed report, with the coupling written out.
- Report C is recognised as incident-shaped and routed through the handoff sequence from [Chapter 08](../08-the-handoff-to-the-governance-incident-path.md).
- Each champion receives a one-sentence reply inside 24 hours (modelled, not actually sent).
- Each destination ticket draft is operator-language, not CoE-paraphrase.
- Anonymity default is applied; any attribution decisions are justified in one line.

## Stretch goals

- Simulate the loop closure. Three weeks later, two of the destination tickets have shipped. Write the champion-facing update that posts back to the source reports — the record-level close-the-loop artifact from [Chapter 03](../03-routing-field-signal-back-to-policy-tooling-and-training.md).
- Author the **quarterly attribution surface** that would include these six reports' contributions. One page, named champions, specific changes shipped. This is the artifact that appears in the exec scorecard and in the champion recognition surface.
- Run the drill again with a peer acting as one of the champions filing the reports. Interview them for 10 minutes after the triage: did your reply feel like a routing confirmation, or like a cold acknowledgment? Adjust your reply template based on the response.

## Why this exercise matters

The two-way feedback loop is the single most load-bearing operating surface of the champion network. [Chapter 01](../01-the-champion-network-as-a-change-management-asset.md) names the social-club, evangelist, and crickets failures — all three originate in a broken or absent triage. Doing the triage drill against realistic reports surfaces the judgment moves that chapter can only describe. Repeat this exercise with different report batches twice a quarter in a new role and your triage judgment will hold under pressure.
