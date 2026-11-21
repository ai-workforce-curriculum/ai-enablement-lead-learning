# Lab 03 — Dry-Run the Weekly Intake Triage

**Duration:** 45–60 minutes
**Format:** guided simulation — six pre-written tickets routed through the three intake queues
**Grounding chapters:** [03 — Authoring the Enablement Operating Model](../03-authoring-the-enablement-operating-model.md), [04 — Handoffs with Adjacent Roles](../04-handoffs-with-adjacent-roles.md)

## Objective

Run a **mock weekly intake triage** against six pre-written tickets and produce, for each, a routing decision, a named owner, the next concrete step, and — where relevant — a flagged handoff. The deliverable is a **triage log** that looks like what you would file after a real week-9 triage per Chapter 06's 90-day plan.

This lab is not Exercise 03 (handoff map, static diagram). It runs the plumbing against synthetic traffic, which is a different muscle.

## Prerequisites

- Chapter 03 read, especially *Intake path* (three queues: long-tail employee, new-use-case pilot, incident fast lane).
- Chapter 04 read, especially the four load-bearing handoffs.
- The decision-rights table from Lab 01, if you did it (optional but useful — you will reference rows).
- A blank file.

## Setup

Create `triage-log-week-9.md` with this skeleton:

```markdown
# Weekly Intake Triage — Week 9, <date>

**Attendees:** AI Enablement Lead (me), AI governance analyst (level 15) via async, security partner (optional).
**Agenda:** six tickets, 10 minutes each, 60-minute cap.

## Ticket log

| # | Intake queue | Ticket | Routing decision | Owner | Next step | Handoff flagged |
|---|---|---|---|---|---|---|
```

You will fill in six rows, one per ticket.

The three intake queues (one must be picked per ticket):

- **L** — long-tail employee intake (one of: self-serve, office hours, training, champion routing, open as new-use-case ticket).
- **P** — new-use-case pilot pipeline (heavier; moves to governance / security review per decision-rights row 1 from Lab 01).
- **I** — incident fast lane (same-day triage, kill-switch authority on you, parallel notification).

---

## Step 1 — Read the six tickets (5 min)

### Ticket #1 — "Help, Claude keeps making up citations in my brief"

> From: senior associate, litigation group. "I used an approved tool to help draft a motion and it invented two case citations. I caught them before filing but my partner is furious. Can someone teach me the right way to use this tool?"

### Ticket #2 — "New-use-case proposal: customer-service copilot in the EU call center"

> From: VP of customer service, Germany. "We want to pilot a vendor copilot for tier-1 reps in our Munich call center. 40 agents. Calls include EU customer personal data. Need to be live by end of quarter."

### Ticket #3 — "Shadow-AI incident: HR shared salary data with ChatGPT"

> From: anonymous via ethics hotline, forwarded this morning. "An HR coordinator pasted a salary-benchmarking spreadsheet with ~400 rows including named employees into a personal ChatGPT account. The spreadsheet has salary band, role, and manager chain. Coordinator thought it was fine because 'it's not confidential, it's just internal.'"

### Ticket #4 — "Can you write our acceptable-use policy for us?"

> From: BU head, retail division. "Our legal team is bogged down and we want to roll out Copilot to 2,000 people in Q1. Can the CoE just draft the acceptable-use policy and we'll run with it?"

### Ticket #5 — "Prompt-coaching clinic request for finance team"

> From: controller, 45-person finance team. "My team's using the approved assistant but they're getting mediocre results. Any way to get a session to level them up? Would 60-90 minutes work?"

### Ticket #6 — "Red-team evidence request on vendor copilot before rollout"

> From: you — a self-ticket from last week's rollout pre-check. "We're one week from go/no-go on the vendor copilot pilot. We have no red-team evidence on prompt-injection robustness or data-exfiltration-shaped behaviors. Governance will ask."

---

## Step 2 — Route each ticket (20 min)

For each ticket, fill the row. Use this scoring order:

1. **Which queue?** L, P, or I. If you cannot tell, re-read Chapter 03's queue definitions — a ticket's queue is determined by the shape of harm and SLA, not by who sent it.
2. **Routing decision inside the queue.** For L, pick one of self-serve / office hours / training / champion routing / escalate-to-P. For P, pick next pilot-pipeline step (problem framing / governance intake questionnaire / security review / pilot design). For I, invoke the incident fast lane and name kill-switch readiness.
3. **Owner.** Named CoE role or named adjacent role from Chapter 04. If the owner is not you, the handoff column must name the role.
4. **Next step.** One concrete action with a time horizon (same-day, 48h, by Thursday triage).
5. **Handoff flagged.** Which of the four load-bearing handoffs from Chapter 04 does this ticket touch? Mark as `L15 (gov-analyst)`, `L25 (risk-eng)`, `L60 (head-of-gov)`, `L40 (team-mgr)`, or `—` if none.

Worked example — routing for Ticket #1:

| # | Queue | Ticket | Routing decision | Owner | Next step | Handoff flagged |
|---|---|---|---|---|---|---|
| 1 | L | Senior associate: hallucinated citations | Training (role-based playbook for legal) + office-hours pairing | Training & Curriculum Lead (or you, Q1) | Pair with associate at Thursday office hours; add "checking citations" to the legal role-based playbook v0.2 | L40 (team-manager for litigation group, if they have one) |

**Rationale:** this is textbook long-tail employee traffic. The harm is low (caught before filing); the pattern is coachable; it should resolve at training + office hours and never become an intake ticket. If the same question arrives again next week, that is signal to update the role-based playbook, not to open another ticket.

Now do the remaining five on your own.

**Guidance per ticket — but no routing decisions; you decide:**

- **#2** is clearly P (new-use-case pilot) *and* has Article 4 and GDPR implications because of EU customer personal data in a call-center use case. Chapter 05's "deployer-side obligations" and the decision-rights row 1 from Lab 01 (`CoE=D, BU=C, Gov=A, Sec=A`) both apply. Name the governance questionnaire as the next step; name a realistic SLA to governance. Do not promise end-of-quarter.
- **#3** is the incident fast lane (queue I). Same-day triage; kill-switch authority on you (Lab 01, row 3). Who do you notify in parallel? Who owns the recovery? Chapter 03 says "parallel notification to governance and security."
- **#4** is where the scope contract from Chapter 01 gets tested. You co-author policy with governance; you do not own it. Rewrite the BU head's request: name what you *can* do (draft, consult) and what the BU needs to route to governance for ratification. Do not ship a policy the BU runs with as if it were yours.
- **#5** is a clean match for a catalog service (prompt-coaching clinic from Lab 02). Confirm you have that in the catalog; if not, this ticket is what justifies adding it.
- **#6** is the self-ticket on the rollout decision. Route to the `ai-risk-engineer` handoff from Chapter 04 — this is exactly the artifact flow the chapter names ("red-team evidence you can cite in the pilot-to-rollout decision"). Name the request specifically; schedule before go/no-go.

**Checkpoint 2:**

- [ ] All six tickets have a queue, an owner, and a next step.
- [ ] Ticket #3 is in queue I; the row explicitly names same-day triage and parallel notification.
- [ ] Ticket #4's row names the Chapter 01 co-author / owner distinction and routes policy ratification to the head of AI governance.
- [ ] Ticket #6's row names the `ai-risk-engineer` handoff and the specific evidence requested.

---

## Step 3 — Pattern-scan the week (10 min)

Weekly triage is not just routing; it is also pattern detection. Answer these three questions below your table:

1. **Which tickets repeat a pattern you have seen before?** (For Week 9, the honest answer is "none, you've just started" — but write the sentence anyway, because the habit of pattern-scanning is what makes the catalog, curriculum, and policy actually improve.)
2. **Which tickets reveal a missing service in the catalog (Lab 02)?** Add a `<!-- catalog-update: ... -->` note.
3. **Which tickets reveal a gap in the decision-rights table (Lab 01)?** Add a `<!-- decision-rights-update: ... -->` note.

Example output of Step 3 after Ticket #3 (shadow-AI incident):

```markdown
### Pattern scan — Week 9

- Repeats: none this week; log Ticket #3 for pattern-check in Weeks 10–12.
- Catalog gaps:
  - <!-- catalog-update: HR had no clear front door for "is this allowed?" before they acted. Add "data-sensitivity self-check for AI tools" to the For-individuals segment as a `coming` service. -->
- Decision-rights gaps:
  - <!-- decision-rights-update: Table did not have a row for "approve use of AI on named-employee salary data"; this incident belongs on next quarter's revision. -->
```

**Checkpoint 3:**

- [ ] Your Step 3 output names at least one catalog gap and at least one decision-rights gap surfaced by this week's traffic.
- [ ] Each gap note is specific enough to action next week — not "we need more policy."

---

## Step 4 — Write the one-paragraph weekly summary (5 min)

Below the ticket log and pattern scan, write a 4–6 sentence summary that the head of AI governance (level 60) could read in under 60 seconds. Include:

- Total tickets by queue (e.g., "4 long-tail, 1 pilot-pipeline, 1 incident").
- The highest-stakes item of the week (usually the incident if there is one).
- Any handoff waiting on an adjacent role (e.g., "red-team evidence request outstanding with `ai-risk-engineer` ahead of Ticket #2 pilot decision").
- Next week's one must-do.

This paragraph is what feeds the Chapter 04 handoff up to the head of AI governance. It is also what you archive for the Article 4 evidence trail (Chapter 05) if any of the tickets touched training or literacy.

---

## Deliverable

- `triage-log-week-9.md` — the ticket log table (6 rows filled), the Step 3 pattern-scan, and the Step 4 weekly summary paragraph.

## Expected output shape

A single page. The table is the bulk; the pattern scan is a short section; the summary paragraph closes it. If this document exceeds two pages, you are over-specifying the tickets — the triage artifact is a running log, not an essay.

## Checkpoint — self-evaluation

- [ ] Every ticket has exactly one queue (L / P / I).
- [ ] At least one ticket routes to each queue (L, P, and I) across the six.
- [ ] Every ticket with an owner outside the CoE has a named handoff in the Chapter 04 vocabulary.
- [ ] The incident ticket (#3) has a same-day SLA and parallel notification to governance and security.
- [ ] The policy ticket (#4) does not quietly make the CoE the policy owner — the co-author / owner line is visible in your row.
- [ ] The pattern-scan produced at least one catalog update note and at least one decision-rights update note.
- [ ] The weekly summary paragraph could be pasted into an email to the head of AI governance without further editing.

## Common failure modes

- **Treating Ticket #4 as a win.** Drafting the policy *for* the BU is scope creep that looks like helpfulness. Co-author with governance, or route to governance; do not ship a policy with your name on it.
- **Opening a new-use-case ticket for Ticket #1.** It belongs in L; opening a P ticket for every employee question is how the CoE drowns (Chapter 03).
- **Letting Ticket #3 wait for the weekly cadence.** The incident fast lane is not a queue that waits a week. Chapter 03: "same-day triage, kill-switch authority on the CoE lead, parallel notification."
- **Running the triage alone.** The intake triage from Chapter 03 is "the CoE lead and the governance partner review new tickets." If governance is absent, your routing is a draft awaiting their read, not a final decision.

## What this prepares you for

The weekly triage is the single most repeated activity of the role in steady state. The quality of the triage is downstream of the artifacts you built in Lab 01 (decision rights) and Lab 02 (service catalog), and upstream of the executive scorecard (Chapter 06 week 12) and the handoffs in Chapter 04. Running it dry here, on synthetic traffic, surfaces the cheap-to-fix gaps before real tickets do.
