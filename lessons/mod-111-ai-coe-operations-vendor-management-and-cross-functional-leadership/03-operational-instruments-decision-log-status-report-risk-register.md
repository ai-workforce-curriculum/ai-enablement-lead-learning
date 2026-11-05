# Operational Instruments — Decision Log, Status Report, Risk Register

> The operating loop from [Chapter 01](01-the-coe-at-steady-state.md) and the service catalog from [Chapter 02](02-the-service-catalog-as-the-coes-public-interface.md) run on three written instruments: a decision log, a weekly status report, and a risk register. Nothing else lets the three weekly questions (what is in flight, what is blocked, what is at risk) survive the attrition of a hundred small conversations across a quarter. This chapter authors the three instruments at operational depth — what each records, what each does not, and how they interlock so that no decision, no obstacle, and no risk lives only in the lead's head.

## Why three, not one

A single mega-log of everything the CoE touches would be unreadable. A single status update that tried to carry decisions, open work, and risks would land as either a wall of text or a sanitised summary. The three instruments are separated because they answer three different questions on three different time horizons:

- **The decision log** is the organisation's memory of *what was decided and why*. It is long-lived and additive. Entries age gracefully; no entry is deleted.
- **The status report** is the organisation's view of *what moved this week*. It is cyclic — every Friday a new one ships, and last week's is the delta the new one is measured against.
- **The risk register** is the CoE's agenda of *what has not yet happened but might*. It is live — items come on, items come off, items re-age. The register is the forward-looking instrument the other two are not.

The three instruments share one storage location — the governance evidence store named in [mod-110 Chapter 06](../mod-110-commissioning-internal-ai-tools-and-custom-agents/06-signing-surfaces-maintenance-and-handoff-calendar.md) — but they are maintained as three distinct artefacts with three distinct cadences. When they blur into one, the CoE loses its ability to answer the three weekly questions cleanly, and the operating loop starts to leak.

## The decision log

### What it is

The decision log is the permanent record of every decision the CoE makes that affects the organisation's AI enablement. Decisions range in scope — from "we are routing this intake request back to the requester with a specific input gap" at Monday triage, to "we are promoting Vendor X from pilot to adopt" at a pilot-to-rollout gate, to "we are deprecating the Outcome Measurement slot's ad-hoc read SLA to 15 business days." The log is additive — entries are added, never deleted — and every entry is stamped, authored, and cross-referenced.

### Required fields per entry

- **Decision ID.** A durable identifier the rest of the organisation can cite — `DEC-2026-Q4-087` is the shape.
- **Date of decision.**
- **Author.** The named human who made the call — the lead for most entries, the AI council chair for council decisions, the exec sponsor for budget decisions above the delegated ceiling.
- **Scope.** The service-catalog slot ([Chapter 02](02-the-service-catalog-as-the-coes-public-interface.md)) the decision affects, or "cross-slot" for CoE-level calls.
- **Decision.** One sentence. Not a paragraph.
- **Why.** Two to four sentences. The evidence and reasoning that led to the decision. "Because the executive sponsor said so" is a legitimate why *if the executive sponsor's name and the specific authorisation surface are recorded* — a council vote, a budget-approval memo, a signed exec one-on-one. Decisions without a legible why are the surface of future audit failures.
- **Dissent.** If the decision was contested, who dissented and on what grounds. The dissent field is not optional — a decision with no dissent field is a decision whose dissent was not surfaced, which is not the same as a decision that had no dissent.
- **Review date.** When the decision is due for a re-read. Not every decision has a review date, but decisions with a time-sensitive scope (pilot adopt, vendor renewal, slot deprecation) do. The absence of a review date is itself a decision.
- **Cross-references.** Linked IDs for the rollout artefact set, the risk-register item, the commissioning brief, or the vendor record this decision binds to.

### What the log does *not* record

- **Discussion threads.** The log records the decision and the why, not the slack thread that preceded it. Threads live in slack; decisions live in the log.
- **Hypotheticals.** "We thought about doing X but did Y" is a legitimate why-field sentence; it is not a decision in its own right. Decisions are things that were committed to.
- **Project tracking.** The log is not a project plan. The in-flight work's status is the status report (next section). The log is only touched when a decision has been made.

### How the log is used after the fact

The log's value is what it enables six months later. When a BU head asks "why did the CoE choose Vendor A over Vendor B for the triage rollout," the lead cites `DEC-2026-Q4-054` and walks the decision's why-field. When the exec scorecard reports a miss that the CoE has publicly committed to not retrofitting ([mod-106 Chapter 06](../mod-106-outcome-measurement-and-executive-reporting/06-the-misses-first-exec-scorecard.md)), the log is the artefact the lead cites to show which decision surface led to the miss and what review date is scheduled for it. When the quarterly ritual (Chapter 05) re-reads the service catalog, the log is read backwards to see which decisions produced the current catalog shape.

The discipline of writing the log is *not optional for the lead*. The log is the CoE's memory. A CoE without a decision log operates with the lead's memory as backup, and the lead rotates every three to four years ([mod-112](../mod-112-career-positioning-and-the-next-step-on-the-ladder/README.md) is the full treatment of that rotation). When the lead rotates, the next lead inherits the log, not the memory.

### An example entry

```
DEC-2026-Q4-062
Date: 2026-11-14
Author: Enablement Lead (J. Lee)
Scope: Rollout and the Artefact Set — p-copilot-service-team
Decision: Delaying the service-team Copilot rollout go-live from 2026-11-20 to 2026-12-10.
Why: Pilot evaluation confirmed outcome movement on first-contact resolution (+6pp,
  CI [+3, +9]) but surfaced a policy gap (no data-handling SOP for the policy-grounded
  Q&A surface). Cannot sign the rollout artefact set with Section 4 open; mod-103 Ch 05
  path produces the SOP in ~12 business days with governance co-author bandwidth.
Dissent: BU head J. Fuentes dissented, preferring to proceed with a deferred-SOP note
  carried in the rollout memo. Position noted; call is held at CoE level because mod-102
  Ch 03 does not support a partially-signed artefact set.
Review date: 2026-12-03 (go/no-go check against the SOP delivery date).
Cross-references: ROLLOUT-2026-Q4-copilot-service; RISK-REG-2026-035;
  mod-103 Ch 05 SOP task #POL-SOP-2026-18.
```

The example is concrete deliberately. A decision-log entry that cannot be read like this — because it is hedged, because it omits the dissent, because it has no review date — is a weak entry. The log is strong only when the entries are.

## The weekly status report

### What it is

The status report is the one artefact the CoE produces every Friday afternoon. It answers the three weekly questions (what is in flight, what is blocked, what is at risk — [Chapter 01](01-the-coe-at-steady-state.md)) against the week's activity. The report is short deliberately — the length discipline is the forcing function that keeps the content focused on what actually moved.

### Required sections

- **Header.** Date, CoE lead, distribution list (exec sponsor, AI council chair, CAIO if present, BU leaders, functional partners).
- **In flight.** One line per active engagement in the service catalog — the slot, the ask, the owner, the current gate, the next milestone. 10–20 lines typically.
- **Blocked.** Items that cannot move without external action — the ask, the blocker, the surface the blocker lives on (exec, procurement, vendor, governance, BU), the specific action requested. Short — if blocked is longer than four lines, the operating loop is in trouble.
- **At risk.** Items on track but at risk of missing — the ask, the specific risk trajectory, the mitigation the CoE is executing against, the review date. Short — if at risk is longer than six lines, the scorecard discipline is drifting.
- **Decisions this week.** A list of decision IDs (and one-line titles) from the log, with a one-line why on the two or three most consequential.
- **Risk register delta.** New risks opened, risks closed, risks re-aged. Not the full register — just the delta.
- **Next week preview.** What the CoE expects to move next week. Not a commitment; a signal of focus.

### The misses-first discipline

[mod-106 Chapter 02](../mod-106-outcome-measurement-and-executive-reporting/02-authoring-the-executive-scorecard-weekly-monthly-quarterly.md) named the misses-first discipline for the exec scorecard. The weekly status report inherits the same discipline at the operating level: **at risk** and **blocked** come *before* **in flight** on the page. The CoE's week is credible when the hardest items are visible first, not buried under a wall of green-check "proceeding as planned" entries.

A status report that leads with wins is a status report whose reader has learned to stop reading after the first page. The misses-first discipline is specifically for keeping the reader at the hard parts.

### What the report is *not*

- **A deck.** The report is a Markdown page, not a slide bundle. Slides come once a quarter at the exec review (Chapter 05).
- **A project plan rollup.** Gantt charts live in the slot-level working artefacts. The status report is the lead's one-page read; a Gantt is the operations analyst's working surface.
- **A commitment.** The next-week preview signals focus; it is not a Friday-afternoon commitment the lead will be measured against on Monday. The commitment surface is the service-level agreement on each catalog slot, not the preview.

### Distribution and read discipline

The status report ships Friday afternoon to a fixed distribution list. Monday's intake triage is the lead's read of the status report back — the three questions walked against the previous Friday's answers. If the lead cannot defend Friday's at-risk list on Monday, something in the operating loop has drifted; the Thursday writing block is probably the first place to look (Chapter 01's second failure mode).

The report is not a request for help. If the lead needs help on a blocker, that help is asked for *by name and on a specific surface* — not by implication in a status item. Exec sponsors who read status reports looking for implicit asks become exec sponsors who stop reading status reports. The asks are in the blocked section with the specific surface and specific action named.

## The risk register

### What it is

The risk register is the forward-looking instrument. It records items that *have not yet happened* but could, with enough likelihood and enough impact to warrant naming and tracking. At steady state the register is maintained by the operations analyst and reviewed weekly by the lead (the Thursday block — [Chapter 01](01-the-coe-at-steady-state.md)). It is co-owned with the AI council (Chapter 05) and with `head-of-ai-governance` at the program risk layer named in [mod-109](../mod-109-ai-incident-response-and-enablement-side-rollback/README.md).

### Required fields per entry

- **Risk ID.** `RISK-REG-2026-035` is the shape.
- **Title.** One sentence.
- **Date opened.**
- **Current age.** Days or weeks the risk has been open. The age field is where ossification (Chapter 01's third failure mode) shows up.
- **Likelihood.** Low / medium / high. The CoE does not try to calibrate quantitatively at this altitude; the categorical read is defended with evidence in the next field.
- **Impact.** Scorecard, policy, operational, vendor-portfolio, reputational, or multi-axis. Impact is named at the surface the risk would materialise on, not as a generic rating.
- **Current signal.** What specific evidence is the current likelihood/impact read standing on? "Vendor X has not confirmed their SOC 2 renewal and the renewal gate is in 40 days" is a current signal; "we have concerns about Vendor X" is not.
- **Mitigation.** The specific action under way to reduce likelihood or impact, with an owner and a review date.
- **Escalation.** If the risk crosses a defined threshold, where does it route? Governance at program level, procurement at vendor level, the exec sponsor at scorecard level, the incident path at operational level ([mod-109 Chapter 01](../mod-109-ai-incident-response-and-enablement-side-rollback/01-the-enablement-side-of-the-incident-path.md)).
- **Closure condition.** What specific outcome closes the risk? "Vendor X SOC 2 renewed, filed, and dated" is a closure condition; "we are more comfortable now" is not.

### The register's weekly cadence

Every Thursday:

- **Re-read the register.** The lead and the operations analyst walk the register start to finish. Every open item either has a current signal (something moved) or does not (nothing moved).
- **Close what can close.** Any item whose closure condition has been met is closed, with a one-line closure note in the entry and a cross-reference from the next status report.
- **Age what has not moved.** Every open item's age field is incremented. Items that have crossed their escalation threshold are escalated, with a decision-log entry recording the escalation.
- **Open what is new.** The week's evidence is checked for new risks. The service catalog's monthly deep-dive data, the status report's at-risk list, the vendor portfolio's quarterly reads (Chapter 04), the champion community's field reports (Chapter 06) are the sources.

The Thursday cadence is what keeps the register from becoming wallpaper. The register's health is its churn — the ratio of items that have moved (opened, closed, escalated, mitigation-advanced) against items that have not. A register with no churn is a register that is not operating.

### The two-category structure

The register sorts risks into two categories, not more:

1. **Enablement-operating risks.** Risks to the CoE's capacity to run the operating loop — staffing shape underwater, intake queue exceeding Monday triage, service-catalog slot demand spike, vendor delivery slipping. The lead owns.
2. **Program-level risks.** Risks to the enablement program's standing posture — policy gap, compliance miss, scorecard miss trajectory, incident precursor (a field report whose pattern matches a previous incident). Co-owned with `head-of-ai-governance` and routed to the AI council (Chapter 05).

Two categories is a deliberate restraint. More than two categories produces a register whose structure takes up more thought than its content. Two categories forces the lead to choose — and choosing is the point.

### What the register is *not*

- **An incident log.** Incidents are the subject of [mod-109](../mod-109-ai-incident-response-and-enablement-side-rollback/README.md); they live on the incident path, not the risk register. The register's forward-looking function is to catch precursors *before* they become incidents.
- **A scorecard.** The exec scorecard ([mod-106](../mod-106-outcome-measurement-and-executive-reporting/README.md)) reports outcomes; the register anticipates them. The register's at-risk items that pop into the scorecard as misses are the close-loop surface, but the two artefacts are not the same.
- **A wish list.** "We wish we had more training production capacity" is not a risk. "If Vendor X does not confirm their SOC 2 renewal in 40 days we will miss the Q1 rollout" is a risk.

## How the three instruments interlock

A single week's full operating record walks across all three instruments:

- Monday triage produces 8–15 decision-log entries (new routings, returns to requester, slot-match confirmations, queue entries). A few are consequential enough to be cited in Friday's report; the rest are reference records.
- Tuesday–Wednesday delivery produces slot-level work that shows up in Friday's **in flight** section — one line per active engagement, cross-referenced to the slot's artefact set in the evidence store.
- Thursday writing is where the status report is drafted, the risk register is re-read, and the decision log is checked for follow-up on prior-week decisions. Two or three decisions get re-opened for review; four or five risks are updated; two risks close; one new risk opens.
- Friday afternoon the status report ships. The next week's Monday triage opens with the previous Friday's at-risk list — the loop is closed.

The interlock is what makes the operating loop legible in writing. A CoE with only a status report has no memory of why things were decided; a CoE with only a decision log has no sense of what moved this week; a CoE with only a risk register knows what might go wrong but not what has decided or what is currently happening. The three together are the written surface of the operating loop.

## Tooling — what to run the instruments on

The instruments can run on any writing surface that supports plain text, link anchors, and durable storage. The specific tooling is less important than three characteristics:

- **The storage is durable.** The instruments live past the lead's tenure, past a vendor migration, past a reorg. The same governance evidence store named in [mod-110 Chapter 06](../mod-110-commissioning-internal-ai-tools-and-custom-agents/06-signing-surfaces-maintenance-and-handoff-calendar.md) is the right default — the policy stack, the rollout artefact sets, the commissioning briefs, and the operating instruments all live there.
- **The entries are cross-linkable.** A decision ID in the log is cited by a risk register entry, by a status report line, by a rollout artefact set, by a policy edit. Cross-linking is what lets the instruments operate as one record, not three parallel streams.
- **The instruments are versioned.** A decision log entry can be amended if the facts change, but the amendment is dated and the original remains legible. A status report is immutable once shipped — the next week's report is the delta, not an edit. The risk register's weekly snapshot is preserved; the current register is live but prior snapshots are kept for the quarterly ritual's re-read.

Common tooling choices at CoE scale: Confluence or SharePoint for the durable write surface, with cross-references into the ITSM system for intake and into the governance evidence store for the full artefact bundles. Specific vendor choices are out of scope for this chapter; the characteristic list above is the discipline.

## The two drifts to watch for

### Drift 1 — The log becomes a project tracker

The temptation is to use the decision log as a to-do list — every in-flight item gets a log entry. The log stops being a record of decisions and becomes a wall of project status. The symptom is the log exceeding ten entries per week on average — more than the CoE could plausibly be making decisions at.

Correction: Enforce the decision-only discipline. An entry without a committed decision is a status-report item, not a log entry. Monday triage's routing calls *are* decisions (route, return, queue); Tuesday–Wednesday's slot delivery is not.

### Drift 2 — The register tracks only what has already happened

The register slowly fills with items that are more properly incidents. A rollout that has already missed its scorecard target is an incident surface, not a risk — the risk was "may miss" and it has now materialised. A policy that has already been contravened is an incident surface, not a risk.

Correction: On the Thursday re-read, ask one question of each open item: *has this already happened?* If yes, route to the appropriate surface (incident path, scorecard miss, decision log) and close the risk. The register is forward-looking only.

## The relationship to the chapters ahead

- [Chapter 04](04-vendor-and-external-partner-management.md) uses the decision log for vendor certification decisions, the risk register for vendor-portfolio concentration and delivery risks, and the status report for vendor engagement progress.
- [Chapter 05](05-the-quarterly-cross-functional-operating-ritual.md) uses the weekly status report as the input stream for the monthly rollup and the quarterly review packet; the AI council reads the register and ratifies escalations.
- [Chapter 06](06-the-org-wide-champions-community-of-practice.md) uses the status report's field-report-sourced items as the input for cross-team lesson posts; the register's precursors often originate as champion-community signal.

## Summary

- **The three instruments answer three different questions on three different horizons.** The decision log is the organisation's memory, the status report is the week's movement, the risk register is the forward agenda.
- **The decision log is additive and dissent-including.** Every decision is dated, authored, and cross-referenced; dissent is a required field; review dates are attached where the decision is time-sensitive.
- **The weekly status report walks the three operating-loop questions misses-first.** At-risk and blocked precede in-flight; the next-week preview is a signal of focus, not a commitment.
- **The risk register is forward-looking and churn-measured.** The Thursday cadence closes what can close, ages what has not moved, escalates what has crossed its threshold, and opens what is new. A register with no churn is a register that is not operating.
- **The three instruments interlock.** Decisions cross-reference risks; risks cite status; status cites decisions. The interlock is what makes the operating loop legible in writing and survivable past the lead's tenure.
- **Two drifts to watch:** the log turning into a project tracker, and the register filling with items that have already materialised. Each drift has a specific correction in the Thursday block.
