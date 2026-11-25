# Lab 03 — Dry-Run the Incident-Path Handoff on Four Live Signals

**Duration:** 60–75 minutes
**Format:** guided hands-on — worked walk + three independent handoffs + boundary-failure red-team
**Grounding chapters:** [08 — The Handoff to the Governance-Owned Incident Path](../08-the-handoff-to-the-governance-incident-path.md), [03 — Routing Field Signal Back to Policy, Tooling, and Training](../03-routing-field-signal-back-to-policy-tooling-and-training.md)

## Objective

Run the four-step handoff sequence — **preserve, notify, transfer the facts, enter supporting mode** — against four short incident-shaped signals the enablement lead's surface actually produces. For each, you will produce the 30-minute operating artifact: the preservation note, the notification message to the named governance-side owner, the facts-transfer memo, and the supporting-mode worklist. The lab is where Chapter 08 moves from reading material to a muscle you can run cold at 4:40 pm on a Friday.

## Prerequisites

- Chapter 08 read with particular attention to the four-step sequence and the three boundary-failure modes.
- Chapter 03 read (two of the four signals come in as `incident-shaped` field reports via the pipe this lab's [Lab 01](lab-01-build-the-field-report-form-and-reply-macros.md) wires up).
- The escalation ladder from your organization's rollout artifact set. If you don't have one, use the stub below:
  - `head-of-ai-governance` — Priya Shah (primary) / Marcus Chen (backup)
  - `ai-risk-engineer` L25 — David Ortiz (primary) / Jenna Park (backup)
  - Security Operations Center — soc-oncall@org.internal, paged via PagerDuty
  - Privacy — Sana Patel (primary) / privacy-oncall@org.internal
- A working file called `handoff-dryrun.md` for the four sequences.

## Why a lab, not an exercise

Chapter 08 is deliberately short — the full incident response treatment lives in mod-109. None of the module's exercises walk you through the handoff itself; Exercise 06's dashboard touches the incident-signal surface but does not drill the four-step sequence. This lab fills the gap. The chapter is explicit that "handoff is a specific sequence, not a notification" and that "it is a procedure, not an email template" — those two sentences are what this lab trains.

## Setup

Open `handoff-dryrun.md` and paste this skeleton. You will reuse it four times.

```markdown
# Handoff Dry-Run — <signal-name>

## The signal (one paragraph, verbatim from the source surface)

<the field report text / the dashboard combined-signal read / the external message>

## Step 1 — Preserve

| Preservation artifact | Captured where | Captured when | By whom |
|---|---|---|---|
| | | | |

## Step 2 — Notify

- Primary named owner: <name + role>
- Secondary / parallel: <name + role, if applicable>
- Channel: <phone / Slack DM / email + "hey, see Slack" nudge / page>
- Message body (<120 words):

> <the message you send>

## Step 3 — Transfer the facts

Three-part memo to the governance-side owner:

- **The signal in full.** <ref>
- **The context.** <tool, function, rollout version, champion name, affected operator (if known)>
- **The enablement-side provisional read.** <flagged as provisional — one paragraph>
- **The access.** <rollout artifact set link, champion contact, operator path via champion>

## Step 4 — Enter supporting mode

Three worklist items for the first 48 hours:

1. Champion-network coordination: <specific action>
2. Kill-switch / rollback readiness: <specific posture>
3. Communications cadence: <specific hold or specific send, coordinated with internal comms>

Three things you explicitly will **not** do (Ch 08 Step 3 inversions):

- <e.g., interview the operator about incident substance>
- <e.g., brief the exec sponsor on substance ahead of governance>
- <e.g., issue a cadence send about the incident ahead of governance-approved communications>
```

---

## Step 1 — Walk the worked example (15 min)

### The signal

A field report lands in the Monday pipe with the `incident-shaped` tag. The filer is Jenna, the customer-service function's champion.

> Operators are using a personal ChatGPT account to draft responses to difficult tickets because the approved tool's turnaround is slower when the ticket is long. I know two operators who do this; there are probably more. One of them pasted a ticket containing the customer's full name and address last Wednesday.

### Walk the four steps

Copy the skeleton into `handoff-dryrun.md`. The signal paragraph is the field report above, verbatim.

**Step 1 — Preserve.** Four artifacts:
- The field report with its ID, in the intake system (captured at the moment Jenna filed).
- A timestamped snapshot of the report (in the ops analyst's preservation folder, within 10 minutes of Jenna's filing).
- Any related reports in the last 60 days tagged customer-service or off-envelope (joined in a short preservation note).
- The approved-tool envelope snapshot for the tool Jenna names (so a later investigator can reconstruct what "approved" meant on this date).

Captured by: the operations analyst, immediately on receiving the tag.

**Step 2 — Notify.** The signal shape matches two rows of Chapter 08's decision table — the `incident-shaped` field report row *and* the "operator pasted customer data into off-envelope tool" row. Notify in parallel:
- `head-of-ai-governance` (Priya Shah) — primary. Phone first, then a Slack DM with the field-report ID, since this is a live data-handling incident.
- SOC — paged via PagerDuty, standard data-exfiltration process.
- Privacy — Sana Patel — since the data pasted is PII (full name + address).
- `ai-risk-engineer` L25 (David Ortiz) — informational for now; may escalate to primary if root-cause work develops.

Message body under 120 words — short, factual, no speculation:

> Priya — incident-shaped field report FR-0247 from Jenna (customer-service champion). Operators appear to be pasting customer tickets into personal ChatGPT accounts; at least one incident last Wednesday involved full-name + address. Preserved in ops system; SOC and Sana paged in parallel. I am entering supporting mode. Need your decision on comms posture and whether we pull kill-switch on the approved tool's slow-turnaround queue to remove the trigger. — <you>

**Step 3 — Transfer the facts.** The memo:

- The signal in full — field report FR-0247 text, Jenna's name as filer, the three-report preservation pack.
- The context — the approved tool is <name>, the rollout went GA four months ago, Jenna is the standing customer-service champion, the operator involved last Wednesday is known to Jenna by name but is operator-anonymous in the report per the Chapter 03 default.
- The provisional read — this reads as a *data-handling incident caused by a workflow-friction trigger*: the approved tool's slow turnaround on long tickets is driving the off-envelope behaviour. Flagged provisional — the governance side runs the forensic. One paragraph, no more.
- The access — rollout artifact set link, Jenna's contact, operator path through Jenna (the governance side decides when and how to engage the operator directly).

**Step 4 — Enter supporting mode.** The first 48 hours:

1. Champion-network coordination: brief Jenna with the specific guidance Priya approves — in particular what Jenna should and should not say when other operators ask her about the incident. If a function-wide pause on the off-envelope workaround is needed, Jenna carries it. If organization-wide: all champions briefed with the same approved language.
2. Kill-switch / rollback readiness: the enablement lead prepares — *not pulls, prepares* — the kill-switch on the slow-turnaround queue so Priya can authorise it if the incident requires it. The mod-102 artifact names *who authorises* (CoE decides on kill-switch per Ch 01 and the mod-101 decision-rights table); you execute, but in this case the incident posture may route the authorisation to governance. Confirm with Priya in Step 2's reply.
3. Communications cadence: the next scheduled send *holds* pending guidance. No cadence content about this incident goes out before the governance-approved line. Internal comms is in the room; the standing cadence other than incident content continues on schedule unless Priya says otherwise.

Three things you will **not** do (verbatim from Chapter 08 Step 3):

- Interview the three operators directly to establish what happened.
- Brief the exec sponsor on substance ahead of the governance-side briefing. Informational notification is fine ("we have an incident in handoff with Priya"); substantive briefing is not.
- Issue a cadence send about the incident before Priya approves the language.

### Checkpoint 1 — before Step 2

- [ ] All four Step headings are populated.
- [ ] Step 2 has a named primary human (not a role title), a channel, and a message under 120 words.
- [ ] Step 4's "will not do" list has at least three items, each a verbatim Chapter 08 inversion.
- [ ] You can state in one sentence why the kill-switch posture is "prepared, not pulled" in this particular incident.

---

## Step 2 — Independent handoff #1: the dashboard combined-signal read (12 min)

### The signal

From the ops analyst's weekly dashboard review:

> Adoption curve shape on the sales-ops AI tool: healthy S-curve through month 4, now shark fin — month 5 active-use dropped 18pp from month 4. The quarterly resistance survey's quality-skepticism cluster rose 22pp with repeated references to "the tool is confidently inventing contract clause numbers." A specific example: one planner caught an invented clause number before sending a supplier escalation last week; two others filed friction reports that read similarly.

Walk the four steps. This is subtler than Lab 03's Step 1 — nothing has reached incident-surface yet, but the combined read matches Chapter 07's silent-compliance precursor *and* the dashboard snapshot is on an engineered-root-cause shape (model confidently inventing citations). Chapter 08's decision table row: "Dashboard adoption-up / skepticism-rising → `ai-risk-engineer` L25 as a watch-item; `head-of-ai-governance` informational."

Prompts:

- Who gets notified first in this signal shape — governance or risk-engineer? Chapter 08's table is specific.
- Preservation is lighter because nothing has hit incident-surface — but the dashboard snapshot still needs saving with a timestamp. Why?
- Supporting mode here is different from Lab 03 Step 1 — the incident has not fully formed. What is the enablement side doing while the risk-engineer investigates the engineered root cause?

Fill the skeleton. The rule: **you may not preemptively pull the kill-switch**; you may prepare it. The Chapter 08 Step 3 inversion applies — the enablement lead does not run the investigation.

### Checkpoint 2

- [ ] Step 2 names `ai-risk-engineer` L25 as primary (the dashboard watch-item row of Chapter 08's table) and `head-of-ai-governance` as informational.
- [ ] Step 4 names a specific champion-coordination action — the sales-ops function's champion is briefed with the watch-item status and asked to continue surfacing specific failure cases through the field-report pipe.
- [ ] Your "will not do" list names "do not issue a cadence send framing this as a confirmed tool defect ahead of the risk-engineer's finding."

---

## Step 3 — Independent handoff #2: the external surface (12 min)

### The signal

An email arrives at the enablement lead's inbox on Thursday morning, from your organization's customer-success team:

> Hi — flagging something that came in via our enterprise-support queue overnight. One of our customers' legal counsel sent us a note saying they received a contract redline from our contract specialist that contained language they flagged as possibly generated by an AI tool, and are formally requesting information about whether AI was involved in drafting any document shared with them under our MSA. They cited a specific clause and asked for a response within 72 hours. Looping you in since I know the legal-ops AI tool went GA last quarter.

Walk the four steps. The signal shape is Chapter 08's **external surface** row — customer complaint / regulator-adjacent query / legal exposure. The decision-table row: `head-of-ai-governance` (always), legal (usually), SOC (if data-shaped). This one is clearly legal territory.

Preservation rule: Chapter 08 Step 1 is explicit that external surfaces get preserved with timestamps — the email itself, any reply chain, headers. The 72-hour clock the customer named is a trigger for a different route (legal response) but the enablement-side preserve-and-notify still runs first.

Prompts:

- Who is the primary named owner? Secondary?
- Does the enablement lead reply to the customer-success team's email? What about to the customer's counsel? Chapter 08's Step 3 inversion applies to both.
- Step 4 has a specific communications element: the organization-wide cadence must *not* send anything that could complicate the legal response, but internal champions in legal ops may need a holding statement so they don't improvise answers to operators who hear about it.

Fill the skeleton.

### Checkpoint 3

- [ ] Step 2 names `head-of-ai-governance` and the organization's legal counsel (both notified on the first move), plus the customer-success team lead informed of the handoff path.
- [ ] Step 3's provisional read is one paragraph and explicitly flagged as provisional — the forensic question "did AI generate this language in a reviewable way" is not yours to answer.
- [ ] Step 4 names the holding posture on the cadence and a specific champion-network briefing for legal-ops champions on what they may and may not say pending guidance.
- [ ] The customer's counsel is **not** replied to by the enablement lead. The chapter is explicit: "do not respond externally until governance approves."

---

## Step 4 — Independent handoff #3: the ambiguous signal (10 min)

### The signal

A champion files a report with the `incident-shaped` tag, but the narrative is thin:

> Something feels off with the writing assistant on PII handling. Had a conversation with an operator today and they said something that worried me but I'm not sure it was a real incident. Flagging it just in case.

Walk the four steps. This is the case Chapter 08's prevention for boundary-failure-mode #1 ("the enablement lead holds the incident") is written against — the chapter's rule is that the `incident-shaped` tag is *the champion's call*, biased toward escalation, and the enablement lead's filter is biased toward escalation, not toward containment.

Prompts:

- Do you treat the thin narrative as "not actually incident-shaped" and route to the normal field-report pipe? Chapter 08 is explicit on the bias direction. What is your answer?
- Who is notified? With what caveat?
- How is Step 3 different when the facts are thin? What do you ask the champion for before the memo is complete, and how does that interact with the Chapter 08 Step 3 discipline ("transfer facts, not ownership")?
- Step 4: the supporting-mode worklist is lighter, but one specific thing happens — a short follow-up conversation with the champion (ops-analyst-run, not enablement-lead-run, because the enablement lead must stay out of the investigation) to help them articulate what concerned them. This is not an investigation; it is preservation of the champion's own recollection before it fades.

Fill the skeleton.

### Checkpoint 4

- [ ] You do not re-tag the report as non-incident; the escalation bias held.
- [ ] Notification goes out to `head-of-ai-governance` (informational / watch-item) with the honest flag that the signal is thin but the champion chose the tag.
- [ ] Step 3 is explicit that the facts set is partial and a follow-up conversation with the champion is scheduled — by the ops analyst, with a specific time inside 24 hours.
- [ ] Your "will not do" list includes "do not interview the operator the champion referenced."

---

## Step 5 — Red-team against the three boundary-failure modes (8 min)

Read all four of your sequences against Chapter 08's three boundary failures. Any sequence that fails a check gets a `<!-- fix: ... -->` comment.

1. **The enablement lead holds the incident.** Does any sequence have the enablement lead investigating, interviewing operators, or issuing fixes before governance has the signal? The handoff should be fast and the `incident-shaped` tag should route out, not contain. Check especially the ambiguous-signal sequence in Step 4 — did you quietly decide the signal was too thin to escalate?
2. **The handoff is a notification, not a transfer.** Does Step 2 (notify) in any sequence read like an email-and-move-on — no preservation attached, no Step 3 memo, no Step 4 supporting-mode worklist? The sequence after the notification is where this failure mode hides.
3. **The enablement side becomes mute.** Does any sequence have Step 4 that reads "wait for governance guidance" with no champion-network coordination, no kill-switch readiness posture, and no communications cadence hold? Chapter 08 is explicit that silence is a boundary failure — the enablement side continues to run its standing operations, with content governed by the incident owner.

Fix any `<!-- fix: ... -->` items.

---

## Deliverables

- `handoff-dryrun.md` — four completed handoff sequences, each with the full skeleton populated and the red-team check applied.

## Checkpoint — self-evaluation

- [ ] All four signals walked through all four steps; no step skipped in any sequence.
- [ ] Each Step 2 names a human by first name, not a role title; each uses the escalation ladder from the stub (or the real one if you had it).
- [ ] Each Step 3 flags the provisional read as provisional and names the access without claiming investigation ownership.
- [ ] Each Step 4 names three specific supporting-mode actions AND three specific things the enablement lead will not do, with at least one of the "will not" items coming directly from Chapter 08's Step 3 inversion list.
- [ ] Red-team check applied; any flagged items fixed.

## What this lab prepares you for

Chapter 08 is the module's hand-off to mod-109. When mod-109 is read, this lab is the running-start — the four sequences you built here are the operating muscle the full incident-response module assumes. The muscle also pays off in Chapter 07's dashboard reviews: the adoption-up / skepticism-rising combined read is explicitly named in Chapter 08's decision table as a `ai-risk-engineer` watch-item trigger, which means any ops-analyst dashboard review may surface a handoff. A first-time enablement lead who has never walked the sequence under exercise conditions will walk it poorly on the day a real signal arrives; a lab-practised one walks it cleanly enough that the governance side starts warm instead of cold. The latency difference is the regulator-notification clock, and that clock is counted in hours.
