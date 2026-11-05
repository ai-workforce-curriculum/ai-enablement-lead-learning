# The AI Governance Council Liaison Seat

> You are not the chair. You are the seat that keeps the chair from making policy decisions on bad information. The council without you is a forum of signals that lag the operating model by a quarter; the council with you is a forum whose decisions move the operating model inside a week.

## What the council is, and what it isn't

The AI governance council is the cross-functional forum where governance, legal, security, privacy, risk, and (in mature organizations) finance decide tool approvals, policy changes, risk-classification outcomes, and incident posture. It is chaired by `head-of-ai-governance` (L60) in most organizations and by a `chief-ai-officer` (L70) in a few. In smaller organizations it is the only governance-level forum at all; in larger ones it is the summit of a tiered governance program with working groups beneath it.

What it is not: a monthly status review. The failure mode of young councils is drifting into a pure reporting forum — program dashboards, usage telemetry, vendor-contract updates. When that happens, the decisions that *should* be made at council (approve this tool, classify this use case, reopen this policy) migrate down into bilateral conversations that never produce an audit-visible artifact. The enablement seat exists partly to preempt that drift.

## Why this role has a seat

The council without ground truth from operators and ground truth from rollout telemetry makes policy decisions on bad information. Two things are missing without you:

- **Field evidence on how tools are actually used.** The intake questionnaire captures intent. The council classifies tools at approval. Six weeks after approval, the tool is being used for a task cohort that was not in the intake — a champion has quietly repurposed it. If nobody surfaces that, the risk classification is stale and the council is governing an imaginary tool.
- **Operator-voice reading of proposed policy changes.** Governance proposes a new acceptable-use clause. On paper it is sound. In practice it forbids a workflow that fifty teams depend on and that nobody present at the council knows about. You carry the operator reading into the room so the clause is right before it ships, not after.

Co-ownership of this seat with `head-of-ai-governance` is the model. They chair. You brief. The council is not *your* forum, but the enablement seat is non-optional.

## The three jobs at council

Everything you do at council maps to one of three jobs. Keep the three separable in your own head and the seat stays coherent through pressure.

### Job 1 — Feed the intake workflow

You bring the list of tools and requests currently in flight through the operating model's intake path (treated in depth in [Chapter 06](06-the-intake-questionnaire.md)), with a status tag per item:

- `pre-intake` — a BU has raised a request; the questionnaire has not been started.
- `intake-in-progress` — the enablement runner is collecting inputs; the questionnaire is partially complete.
- `schema-complete` — the questionnaire is complete; awaiting architect / risk review.
- `awaiting-council-decision` — the item is ready for a council vote.
- `council-approved` / `council-declined` / `council-deferred` — resolved, with the next-step owner named.

This is the forcing function that keeps tools moving instead of dying in queue. Without it, intake becomes a graveyard — tools enter, nothing resolves, requesters get frustrated and buy shadow licenses. The council does not need to approve every item every meeting, but every item needs a visible status.

### Job 2 — Provide risk-classification input

You do not classify. `senior-ai-governance-architect` (L50) designed the risk schema; `head-of-ai-governance` ratifies classifications; `ai-risk-engineer` (L25) supplies engineered-risk evidence. Your input is *field-level facts the schema is applied to*:

- The cohort that is actually using the tool — size, role mix, geography.
- The task mix observed via workflow interviews and champion reports — what the tool is being used for, not only what it was intended for.
- The data classes observed in operator practice — pasted in, generated out.

Classification drift is the thing you watch for. A tool approved for one cohort and task mix is now being used by a different cohort for a different task mix. Flag it. The council decides whether the classification should move; the architect redesigns the schema if the pattern recurs. You do not argue the classification. You provide the input.

### Job 3 — Surface field signal from champions

This is the job most newly-seated enablement leads skip. Treating the council seat as a one-way push (you brief, they decide) is the shape of someone who has not yet realized the seat is an *interface*. Field signal flows upward through this seat too:

- Policy clauses champions report are repeatedly misunderstood (the training package has drifted, or the clause is worded past operators).
- Use cases forming in the field that the current policy does not address — not yet an incident, not yet a request, but a *pattern*.
- Early-warning incidents that have not yet tripped the formal escalation path but are worth the council knowing about before they do.

Package this as a running section on the pre-read (see below). One or two items per council. Each with the evidence (how many champions reported it, over what window) and the recommended council action — which may be "no action, just awareness."

## The pre-read

The council's time is scarce. The enablement seat's value scales with how tight the written brief is going into the meeting. Write a pre-read and send it 48 hours ahead. The discipline is:

- One page.
- Three sections — one for each job.
- Each item has a named ask: *decision*, *discussion*, or *informational*. If everything is informational, you are not using the seat.
- Status tags on intake items; evidence bullets on classification-drift items; recommended-action on field-signal items.

Exercise 04 drills this pre-read. Do it; the muscle matters.

## The report-back to champions

The second half of the two-way interface is the report-back. Within two or three business days of each council, brief the champion network on what changed:

- Which policies were ratified or opened.
- Which tools were approved, declined, or deferred.
- Which classifications moved.
- What signal from the field the council acted on (closing the loop from Job 3).

This is how the next cycle's field signal gets higher fidelity. When champions see their reports land on the council agenda and produce decisions, the quality of what they report rises. When they do not, the champion network degrades into a social club.

## What you do not do at council

Three drifts are easy to make and every one of them damages the seat:

- **Argue a legal reading.** Counsel reads law. You do not. If you disagree with a legal position, your move is to ask counsel a specific question — not to counter-argue.
- **Redesign the control library.** That is `senior-ai-governance-architect` (L50). You can bring evidence that a control is not being evidenced in practice; you do not propose a replacement control. [Chapter 07](07-what-you-route-out-counsel-soc-architect.md) has the discipline.
- **Vote on program direction.** The quarterly program plan, the regulator engagement calendar, the board narrative — those are `head-of-ai-governance` decisions. You consume them; you do not shape them at council.

## A shape for the relationship with `head-of-ai-governance`

Co-ownership of this seat is a weekly or biweekly bilateral. The bilateral is where the two of you decide what makes it onto the council pre-read, what the house position is on contested items, and who is briefing whom on what. Without that bilateral, you and the head of governance arrive at council in different stances and the council spends time negotiating between its own partners instead of deciding. The bilateral is cheap and makes the council work; skipping it is false economy.

## Summary

- The AI governance council is a decision-making forum, not a status review. Co-chaired in practice between `head-of-ai-governance` (L60) and this role as the operating-model liaison.
- The three jobs at council are: feed the intake workflow (status-tagged pipeline), provide risk-classification input (field-level facts, not classifications), and surface field signal from champions (packaged as a running pre-read section).
- The pre-read is one page, three sections, named-ask per item, sent 48 hours ahead.
- The report-back to champions closes the loop and is what makes the next cycle's field signal useful.
- What you do not do at council: argue legal readings, redesign the control library, vote on program direction. See [Chapter 07](07-what-you-route-out-counsel-soc-architect.md).
- The weekly or biweekly bilateral with `head-of-ai-governance` is the cheap discipline that keeps co-ownership of the seat coherent through contested items.
