# Lab 02 — Dry-run the "Is It a Model?" Intake Triage

**Duration:** 75–90 minutes
**Format:** guided solo simulation — triage three bank-flavoured candidate-tool intake submissions, produce the routing packet to Model Risk Management (MRM), and draft the operator-facing holding response
**Grounding chapters:** [04 — Finance Flavour — SR 11-7 and FINRA](../04-finance-flavour-sr-11-7-and-finra.md) (the "is it a model?" question and the three sub-questions; intake deltas), [07 — Enablement vs. Governance Responsibility Split](../07-enablement-vs-governance-responsibility-split.md) (the finance overlay and the three-lines-of-defense test), [08 — Partnering with Industry Counsel Without Opining](../08-partnering-with-industry-counsel-without-opining.md) (operator-surfaces-a-question posture)

## Objective

Run the single question Chapter 04 names as the one the bank enablement lead will be asked most often — **"is it a model under SR 11-7?"** — through three candidate-tool intake submissions, produce the routing packet to MRM, and draft the operator-facing holding response. Target outputs:

1. Three **triage-sheet rows** — one per candidate tool — with the Chapter 04 three sub-questions filled in and the routing decision (to MRM / to approved-use process / pause for clarification) stated with a one-sentence rationale per answer.
2. A **routing packet** to MRM for the submissions that need it — intake-questionnaire-shape, written to make the MRM-side determination possible without a two-week debate.
3. An **operator-facing holding response** for each submission — written in the Chapter 08 operator-surfaces-a-question posture, naming the pause duration and the escalation path.

The lab is the dry-run of the muscle Chapter 04 names: *the enablement lead carries the routing discipline; MRM makes the call*. You are not classifying tools. You are making classification *possible* and *fast* at the MRM end.

## Prerequisites

- Chapter 04 read end-to-end, especially *The "is it a model?" question* and *Intake questionnaire deltas*.
- Chapter 07 skimmed — the finance overlay, and the three-lines-of-defense test.
- Chapter 08 skimmed — the operator-surfaces-a-question posture and the sentence patterns that stay in scope.
- A chosen organization. For the lab's default, assume a 10,000-person US-headquartered bank with a national lending franchise, broker-dealer subsidiary, and a mature MRM function under SR 11-7. (You may adapt the three intake submissions to a different finance flavour — SEC-registered investment adviser, GSE-adjacent infrastructure — if that matches your target role better; keep the three-sub-question structure.)
- A single markdown file.
- A timer.

## Why a lab, not an exercise

Exercise 02 asks for a posting-reading memo + obligation map. Exercise 04 asks for the AUP + SOP + intake-questionnaire delta. Neither exercise simulates the recurring triage work that *runs the intake delta on live submissions* — the week-in-week-out activity that produces the evidence MRM grades the enablement intake on. This lab operates one layer below the exercises: three realistic intakes land on your desk; you triage them against the three sub-questions, route them, and reply to the operator — all within an hour-and-a-half.

Running the dry-run with a timer is the cheapest way to build the triage discipline before the first week in a bank-flavoured role, where the three-sub-question routine either becomes muscle quickly or becomes the drift Chapter 07 names (making classification calls on the fly because MRM is slow).

## The three intake submissions

Three realistic intake submissions, chosen to span the three sub-questions non-trivially. Do not read ahead; part of the lab is deciding the answers yourself.

### Submission A — Marketing Copy Drafter

*"I lead the retail-marketing content team. We would like approval to use `[approved coding assistant / chat tool in envelope]` to draft weekly email campaigns, blog posts, and landing-page copy. Our editorial team reviews every piece before send. Team of 11 content producers. Est. 40 drafts per week. Data input: product details, offer parameters, audience segments (no customer PII, no NPI). Output: marketing copy only; no reference to any specific customer; no price, rate, or term quotes. We already use the tool for internal comms — this is a workload-scale ask."*

### Submission B — Credit-Analyst Memo Assistant

*"I lead credit for middle-market commercial lending. We want to use `[approved coding assistant / chat tool in envelope]` to help analysts assemble the narrative section of credit memos — the qualitative part discussing borrower risk factors, industry trends, and our rationale for the recommendation. Analyst still writes the risk grade, the conclusion, and the recommendation. Memo is reviewed by senior credit, then the loan committee. 25 analysts. Est. 10 memos per week per analyst. Data input: borrower financials, industry data, our internal rating-system framework. Output drafted narrative; analyst edits and owns."*

### Submission C — Call-Center Transcript Summarizer

*"I lead the retail call-center operations function. We want to use `[approved coding assistant / chat tool in envelope]` to generate a short structured summary of each inbound call once the agent completes the call — summary pushed to the CRM. Purpose: reduce after-call work by ~90 seconds per call. 1,800 agents. ~400,000 calls per week. Data input: call transcript (which contains customer PII and account details). Output: 200-word summary with structured tags (reason-for-call, resolution-status, follow-up-needed)."*

Set the timer and start. Each submission's full triage, routing, and holding-response pass is targeted at 20 minutes; the final ~20 minutes are for the summary routing packet and the debrief.

## Setup

Create `is-it-a-model-intake-triage.md` with this skeleton:

```markdown
# Intake Triage — "Is It a Model?" Dry-run

**Date of dry-run:** <today>
**Organization:** <bank, size, regulatory posture>
**Drafter:** AI Enablement Lead (me)
**SR 11-7 anchor:** Supervisory Guidance on Model Risk Management (Fed / OCC, 2011). Model defined as "a quantitative method, system, or approach that applies statistical, economic, financial, or mathematical theories, techniques, and assumptions to process input data into quantitative estimates."
**Three sub-questions per Chapter 04:**
1. Does the tool's output affect a decision, estimate, or quantitative judgment?
2. Does the output materially influence business or regulatory outcomes (credit, suitability, pricing, reserving, compliance)?
3. Is the output used in any way that would need to be defended to a regulator?
An honest "yes" to any one opens the model-risk routing.

---

## Triage sheet

| Submission | Q1 (decision/estimate/judgment) | Q2 (business/regulatory outcome) | Q3 (defend to regulator) | Routing decision | One-sentence rationale |
|------------|---------------------------------|----------------------------------|--------------------------|-------------------|-------------------------|
| A — Marketing | | | | | |
| B — Credit memo | | | | | |
| C — Call summary | | | | | |

---

## Routing packet to MRM (submissions that need it)

<entries>

---

## Operator-facing holding responses

<entries>

---

## Debrief

<entries>
```

---

## Step 1 — Minutes 0–20: triage Submission A (Marketing Copy Drafter)

Read Submission A once. Then fill its triage-sheet row with your honest answer to each sub-question. Not "probably no"; `yes` / `no` / `unsure`, with one sentence of rationale.

Anchor your reasoning in Chapter 04's three sub-questions. The chapter is explicit: "An honest 'yes' to any one opens the model-risk routing." The enablement lead is not *determining* model status; the enablement lead is *routing* based on honest answers to a structured question.

Then make the routing decision. Three options:

- **Route to MRM** (any honest "yes" or "unsure" on any sub-question).
- **Route to the approved-use process** (all three honest "no"s, and the use falls inside existing approved-use language).
- **Pause for clarification** (the submission is ambiguous enough on a load-bearing fact that MRM would bounce the packet back; clarify with the requestor before routing).

For Submission A, write the routing decision and the one-sentence rationale. Then draft the operator-facing holding response in the file's *Operator-facing holding responses* section.

The holding response is a Chapter 08 Posture 1 ("operator surfacing a question") move — the operator is you surfacing a question, but your audience is the business-line lead who filed the submission. Three features the response needs:

- **A clear decision-ask shape.** Name the pause. Name the decision maker.
- **Operational context.** Mirror back what the submission said so the requestor sees you read it.
- **A timing signal.** How long the pause is expected to last; what the delay cost is to the requestor; the escalation path if the delay runs over.

Template:

```markdown
### Submission A — holding response

To: <requestor role>
From: AI Enablement Lead
Subject: Intake A — [tool] for marketing copy drafting — held pending <next step>

Thanks for the submission. Summarizing what I have: you would like to use [tool] with your 11-person content team to draft ~40 marketing-copy pieces per week; editorial review is on the send side; data inputs are product/offer/segment, no customer PII and no NPI; outputs are marketing copy only with no price, rate, or term quotes.

My intake triage on the three SR 11-7 sub-questions reads as <answers>. On that basis, I am <routing to MRM | approving through the approved-use process | pausing for clarification on one point>.

<If routed to MRM: expected MRM response window is <X business days>; I will update you on <date>. Hard pause until then on any production use.>
<If approved through approved-use: specific approved-use language that governs is <link / line>; the SOP section on records-retention for marketing output applies.>
<If paused for clarification: the single clarifying question is <X>; I need the answer by <date> to route.>

The escalation path if this timing creates a business issue is <CRO / CCO / head of AI governance>. I will coordinate with compliance on any FINRA / SEC marketing-rule overlay that attaches.
```

Do not approve "to save MRM time." Do not write "I think this is not a model." Do not render a determination. If your honest Q1/Q2/Q3 reading is all "no" *and* the use fits existing approved-use language *and* there is no regulated-communication touch, the approved-use route is fine; if there is any honest "unsure," route to MRM.

**Checkpoint 1:**

- [ ] Triage-sheet row filled for Submission A with Q1/Q2/Q3 honestly answered (not pre-judged).
- [ ] Routing decision made with a one-sentence rationale.
- [ ] Holding response drafted in the operator-surfaces-a-question shape.
- [ ] You did not render a classification determination.

---

## Step 2 — Minutes 20–40: triage Submission B (Credit-Analyst Memo Assistant)

Same loop. Read; fill the triage-sheet row; decide; draft the holding response.

Two tells specific to Submission B that Chapter 04 gives you language for:

- **"The analyst still writes the risk grade, the conclusion, and the recommendation"** is the submission trying to pre-empt the Q1/Q2 reading. Compare Chapter 08's finance case walk: *"The enablement lead declares the use permitted because 'the output is still reviewed by the analyst and underwriter' and updates the AUP's approved uses to include it"* is the wrong move — it is the lead doing the classification on the fly. The right move is to route to MRM: the AI output is in the credit memo (an artifact the loan committee reads); the Q2 "materially influence business or regulatory outcomes — credit" sub-question is honestly a yes even if humans remain in the loop.
- **The regulated-decision touch** is live even if the decision is formally the analyst's. Chapter 04's intake deltas name "regulated-decision touch" as its own field, independent of model classification; both the model-classification field and the regulated-decision-touch field route independently.

Fill the triage row honestly. If the routing is to MRM, write the holding response.

Template:

```markdown
### Submission B — holding response

To: <head of middle-market commercial lending credit>
From: AI Enablement Lead
Subject: Intake B — [tool] for credit-memo narrative drafting — routing to Model Risk Management

Thanks for the submission. Summarizing: 25 middle-market credit analysts, ~250 memos/week, tool drafts the qualitative narrative section (borrower risk factors, industry trends, rationale); analyst writes the risk grade, the conclusion, and the recommendation; senior credit reviews, loan committee approves.

My intake triage reads <Q1 / Q2 / Q3 answers>. On that basis I am routing this to MRM for classification under SR 11-7, with a parallel compliance check on fair-lending reason-code implications under ECOA. The AI output is in the credit-memo artifact, which is part of a regulated-decision chain; Chapter 04 of the SR 11-7 reading at this bank is clear that MRM — not enablement — owns the classification determination even when the human remains in the loop.

Expected MRM response window is <X business days>. Hard pause on production use until then; pilot in a sandbox with synthetic or fully-anonymized financials is permitted under <existing policy section>.

If this timing creates a business issue — the quarter-end pipeline is dense — the escalation path is <CRO> with <head of AI governance> on the thread. I will surface MRM-queue latency as a scorecard signal if the response window slips.
```

**Checkpoint 2:**

- [ ] Triage-sheet row filled for Submission B with explicit honesty on Q2 — "credit" is one of the chapter's named regulatory outcomes.
- [ ] Routing decision is to MRM (an honest Q2 "no" on a tool producing content inside a credit memo is the drift Chapter 07 names).
- [ ] Holding response named the escalation path if MRM is slow — do not absorb MRM's capacity; surface it.
- [ ] You did not write "the output is reviewed by the analyst so this is not a model."

---

## Step 3 — Minutes 40–60: triage Submission C (Call-Center Transcript Summarizer)

Same loop. Read; triage; decide; respond.

Three tells specific to Submission C:

- **PCI / NPI data touch.** The transcript contains customer PII and account details; that engages the data-class side of the intake (NPI touch, possibly PCI touch) regardless of the model-classification answer. The intake has multiple fields firing — do not collapse them.
- **The structured output's tags** (reason-for-call, resolution-status, follow-up-needed) are plausibly quantitative signals that downstream analytics read. Q1 ("affects a decision/estimate/judgment") depends on whether those tags feed any downstream regulated flow (fair-lending analytics, UDAAP monitoring, FINRA-regulated communications). The honest answer may be *unsure* on first read — route unsure to MRM, do not resolve on the fly.
- **Scale alone is a signal.** ~400,000 calls/week is a regulatory evidence surface if anything about the summarization pattern matters to CFPB or FINRA. Chapter 04's exam-year posture names the approved-tool envelope as an exam-ready evidence surface; a 400k-calls/week deployment is read by the examiner more carefully than a small-scale one.

Fill the triage row; make the routing decision (expect that this is a MRM + CCO + fair-lending + CISO multi-party route); draft the holding response.

Template:

```markdown
### Submission C — holding response

To: <head of retail call-center operations>
From: AI Enablement Lead
Subject: Intake C — [tool] for call-transcript summarization — multi-party routing

Thanks for the submission. Summarizing: 1,800 agents, ~400,000 calls/week; tool generates a 200-word summary with structured tags once the agent completes the call; summary pushed to CRM; inputs include customer PII and account details (NPI).

Intake triage: <Q1/Q2/Q3 answers; expect at least one honest "unsure">. Data-class fields: NPI touch yes; PCI touch <yes/no depending on how account details are carried>; regulated-communication touch <answer>.

I am routing this to <MRM for SR 11-7 classification> + <CCO for FINRA / UDAAP review on the summarization pattern that downstream flows read> + <fair-lending officer if the structured tags feed any fair-lending analytics> + <CISO on the transcript-data handling at scale>. The intake-queue status for each counterpart is <status>; expected response windows are <table>.

Hard pause on production use until the routed determinations return. Pilot with synthetic transcripts in a non-prod CRM sandbox is permitted under <existing policy section>.

Escalation if timing creates a business issue: <CRO> and <head of AI governance> on the thread. I will surface any MRM / CCO / fair-lending / CISO queue latency as a scorecard signal.
```

**Checkpoint 3:**

- [ ] Triage-sheet row filled for Submission C with honest answers (unsure is a permitted answer; "no" because the use feels operational is not).
- [ ] Routing decision is multi-party — a single "to MRM" misses the fair-lending, UDAAP, and CISO surfaces.
- [ ] Holding response named each counterpart and the expected response windows.

---

## Step 4 — Minutes 60–75: assemble the routing packet to MRM (15 min)

For the submissions that routed to MRM (likely B and C — possibly A if your Q1/Q2/Q3 were honest and ambiguous), assemble a single routing packet that lets MRM determine classification in one read, without a two-week debate.

Chapter 04's intake-questionnaire deltas name the required fields; the packet carries them in a format MRM can process.

Template:

```markdown
## Routing Packet — MRM Classification Queue

**Submitter:** AI Enablement Lead (intake runner)
**Date:** <today>
**Submissions in packet:** B, C (also A if routed)

### Submission B — Credit-memo narrative drafting

| Field | Value |
|-------|-------|
| Tool | [approved coding assistant / chat tool in envelope] |
| Requestor role | Head of middle-market commercial lending credit |
| Operator population | 25 credit analysts |
| Volume | ~250 memos/week |
| Data classes touched | borrower financials (NPI), industry data, internal rating-system framework |
| Q1 (decision/estimate/judgment) | <yes/no/unsure + 1-sentence why> |
| Q2 (business/regulatory outcome) | <yes/no/unsure + 1-sentence why> |
| Q3 (defend to regulator) | <yes/no/unsure + 1-sentence why> |
| Regulated-decision touch | yes — credit-decision chain |
| Regulated-communication touch | <answer; memo is internal but loan-committee decision is on record> |
| MNPI touch | no |
| PCI touch | no |
| Current approved-use language that would govern if non-model | <link / line> |
| Operator-facing content already drafted | no — pending MRM determination |
| Requested MRM response window | <X business days> |

### Submission C — Call-transcript summarization

<same shape, filled>
```

This packet is the artifact MRM reads. Do not propose the classification; state the Q1/Q2/Q3 honestly with one-sentence rationale and let MRM decide.

**Checkpoint 4:**

- [ ] Routing packet carries the Chapter 04 intake-delta fields explicitly — not just "please review."
- [ ] Each Q1/Q2/Q3 answer has a one-sentence rationale in your words.
- [ ] No sentence in the packet renders a classification determination or proposes one.
- [ ] The packet includes the operator-facing content status so MRM knows nothing is already published.

---

## Step 5 — Minutes 75–90: debrief (15 min)

Write a short debrief answering these four prompts. One or two sentences each.

```markdown
## Debrief — what the triage taught me

1. **Which submission was hardest to keep an honest "unsure" on — and what pulled you toward a classification determination?** (Scale pressure? Submission framing that pre-emptively argued "no"? Operator relationship?)
   <answer>

2. **Which sentence in your holding responses came closest to the Chapter 08 drifted-starting-sentence patterns** ("Under [rule], the correct approach is…" / "Legally, this is permitted…" / "The regulatory requirement is Z")? Rewrite it here.
   <answer>

3. **If MRM comes back on Submission B in six weeks instead of the requested window, what is the specific scorecard signal you would surface — and to whom?**
   <answer>

4. **In a real intake week, where is this dry-run likely to break first?** (Common answers: triage-row Q1/Q2/Q3 collapse to the shortcut "no"; routing becomes "to MRM" and the fair-lending / CISO / CCO surfaces get missed; the holding response drifts into interpretation; the scorecard signal on MRM latency is never actually surfaced.)
   <answer>
```

**Checkpoint 5:**

- [ ] All four debrief prompts answered.
- [ ] Prompt 2 names a specific sentence from your own response and rewrites it to Chapter 08 posture.

---

## Deliverable

- `is-it-a-model-intake-triage.md` with:
  - The three-row triage sheet with Q1/Q2/Q3 answered and routing decisions.
  - The routing packet to MRM (for submissions that routed there).
  - The three operator-facing holding responses, each in Chapter 08 Posture 1 shape.
  - The four-prompt debrief.

## Expected output shape

Roughly 2–3 pages of markdown. Triage sheet is a table; routing packet is a structured per-submission table; holding responses are short memos (6–10 sentences each). Debrief is one short section.

## Checkpoint — self-evaluation

- [ ] Every triage row has an honest Q1/Q2/Q3 answer and a one-sentence rationale per answer.
- [ ] Not every submission routed to MRM — Submission A plausibly routed to approved-use *if* every Q answer honestly landed "no"; a routing of 3/3 to MRM is a sign you did not actually read the submissions.
- [ ] Not every submission routed to approved-use — Submission B's honest reading on Q2 ("credit — materially influences business outcomes") is a yes; a routing of 3/3 to approved-use is the drift Chapter 07 names.
- [ ] The routing packet to MRM carries structured fields, not a prose summary.
- [ ] The holding responses do not render classification determinations ("I think this is not a model") or legal conclusions ("Under SR 11-7 the correct approach is…").
- [ ] Each holding response named the escalation path and (where relevant) the scorecard signal on counterpart latency.
- [ ] The debrief rewrote one drifted sentence from your own response.

## Common failure modes

- **Collapsing to shortcut "no" on Q2.** The Q2 pull is "does the output *materially* influence…" — and the operator's framing often reads as "the human still decides." Chapter 04 is explicit that human-in-the-loop does not make the output non-material; the credit-memo narrative that goes to the loan committee is material to the credit decision even when the analyst owns the recommendation. Fix: answer Q2 against the chapter's definition, not the submitter's framing.
- **Classifying on the fly to "save MRM time."** The specific drift Chapter 07 names in the finance overlay. The lead writes "this is clearly not a model" to clear the queue. The organization accumulates deployed tools that have not been through MRM. Fix: when MRM is slow, the scorecard signal to CRO is the move — not the enablement lead's classification call.
- **Writing the holding response in legal voice.** "Under SR 11-7 the correct approach is…" is Chapter 08's named drift. Fix: operator-surfaces-a-question posture — operational context, specific decision ask, timing signal, escalation path. Compliance's position is compliance's.
- **Treating "to MRM" as one routing decision.** Submission C has fair-lending, UDAAP, and CISO surfaces on top of the model-classification question. A single-recipient routing misses them. Fix: Chapter 04's intake deltas carry multiple independent fields; each field routes independently.
- **Promising MRM-queue-latency escalation and never actually building the scorecard signal.** The intervention Chapter 07 names is the scorecard signal on MRM-queue latency; a holding response that mentions it but is not wired to a real scorecard metric is theatre. Fix: name the specific metric (MRM response window compliance %, oldest-queued-item age) you would commit to publishing — and verify the metric exists before writing the holding response in production.

## What this lab prepares you for

The "is it a model?" routine is the single recurring motion of the bank-flavoured enablement intake. In production, you run it 10–40 times a week depending on the organization's AI adoption curve. The first time you run it against a real submission that has executive momentum behind it, the pressure to collapse the honest-unsure to a "no" is real. Running the three-submission dry-run cold, with a timer, before that pressure arrives is the cheapest way to build the muscle. The lab also produces the operator-facing holding-response template that reads as professional (Chapter 08 Posture 1) rather than as a bureaucratic block — and in production, the quality of those holding responses is how business-line leads form their opinion of the enablement function. A second-order output: this lab's artifacts are a direct feed into Exercise 04's intake-questionnaire delta — the triage rows you produced show which fields and routing rules are load-bearing in your industry's intake schema.
