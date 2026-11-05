# Exercise 01 — Enablement-Side Incident Triage Drill

**Estimated effort:** 2 hours
**Format:** triage log + first-hour timeline + four one-page signal cards, Markdown
**Grounding chapters:** [01 — The Enablement Side of the Incident Path](../01-the-enablement-side-of-the-incident-path.md); [04 — The First Ten Minutes to the First Hour](../04-the-first-ten-minutes-to-the-first-hour.md). Prior reading: [mod-102 Chapter 03](../../mod-102-selecting-and-rolling-out-ai-tools/03-the-rollout-artifact-set.md); [mod-105 Chapter 08](../../mod-105-champion-networks-and-change-management/08-the-handoff-to-the-governance-incident-path.md).

## Objective

Produce the triage drill output for four incoming signals, one from each of the four signal sources named in Chapter 01. The drill proves you can recognise the source quickly, run the T+0 to T+30 timeline against the right first-move for each shape, page the correct named owner on the escalation ladder, and keep the enablement-side scope under incident pressure.

The output is a triage log, a first-hour timeline for one of the four signals carried to T+60, and four one-page "signal cards" summarising how you would run each signal from recognition to packet-ready.

## Prerequisites

- Chapters 01 and 04 read.
- [mod-102 Chapter 03](../../mod-102-selecting-and-rolling-out-ai-tools/03-the-rollout-artifact-set.md) read, specifically Artifact 5 (support & escalation path) and Artifact 7 (kill-switch & rollback plan).
- [mod-105 Chapter 08](../../mod-105-champion-networks-and-change-management/08-the-handoff-to-the-governance-incident-path.md) read.
- A chosen rollout — **you will carry this rollout across Exercises 01, 02, 03, and 04**. Choose deliberately. If you do not have one in mind, pick one of:
  - A 4,000-person professional-services firm rolling out a general-purpose coding assistant (GitHub Copilot or equivalent) to its software-engineering population with a bounded pilot in two teams, now expanding to full engineering GA.
  - An 8,000-person regional health system rolling out a clinical-documentation summarisation tool to physicians in three specialties with full business-associate-agreement (BAA) coverage, now expanding beyond the pilot.
  - A 12,000-person bank rolling out a knowledge-base-grounded customer-service assistant to contact-centre agents, co-authored with model risk management under SR 11-7.
  - A 2,500-person ed-tech vendor rolling out an internal AI-enablement platform for employees (customer success, product, L&D) whose outputs can touch customer-facing deliverables.

## Problem statement

You are the enablement lead on the rollout above. Four signals arrive on your surfaces inside a 10-day window; you treat each as the first-contact event and run the triage through to T+60 for the one your instructor (or you, if self-studying) picks as most representative. For the other three, produce a one-page signal card showing how you would triage without walking the full timeline. Produce the triage log that spans all four in parallel as a working artefact.

The four signals, one per source:

1. **Champion field report** — a champion in your rollout files a report tagged `incident-shaped`. Narrative: an operator used the tool to produce an output that reached an external party (patient, customer, client — pick one appropriate for your chosen rollout), and the output included something the operator believes should not have been shared. The operator has already told their manager. The champion has preserved the prompt and output.
2. **Usage anomaly** — the dashboard shows a 3x spike in sessions in a specific team over the last 72 hours, concentrated outside business hours, with prompt-length distribution shifted toward longer prompts than the pilot baseline.
3. **Outcome regression** — the executive scorecard shows a regression in a key outcome metric (first-contact resolution, documentation-quality score, code-review turnaround, pick one appropriate) in the function using the tool. The regression is roughly the magnitude of a single reporting-period shift; no single operator event has been flagged.
4. **External complaint** — an email arrives at the organisation's general inbox from an external party (customer, regulator liaison, counterparty) complaining about an AI-produced response they received. The email is routed to you because "you run the AI program." The sender has copied a specific office-holder (external counsel, state attorney general liaison, or an industry regulator contact — pick one).

## Requirements

### Part A — The triage log

A single Markdown document, append-only, timestamped, covering all four signals in parallel. Required entries per signal:

- **T+0 recognition entry.** Source classification; one-sentence summary of what the signal says.
- **T+2 preservation entry.** What you preserved and where.
- **T+5 brief-yourself entry.** The four-item enablement-side brief (what the signal says, source, provisional severity, named owner about to be paged).
- **T+7 paging entry.** Which named owner on the escalation ladder, by what channel, with the short paging message you sent.
- **T+10–T+15 thread-confirmation entry.** Governance-side owner on thread; three decisions requested; three answers (you can simulate the answers plausibly, but flag them as simulated).
- **T+15–T+20 kill-switch-or-not entry.** Decision taken, authorising role.
- **T+20–T+30 champion-brief entry.** What went to which champions, on what channel, in what words.

Entries are observations, not findings. Entries use plain language. Entries are not revised after they land in the log.

### Part B — The first-hour timeline (one signal carried to T+60)

For the signal you pick as most illustrative (choose the one that most stresses the four signal sources' first-move distinctions for your rollout), extend the triage log through T+60:

- **T+30–T+45 packet assembly.** Describe the packet you assembled; name each artefact that goes in; name the person on the enablement side you listed as access-list contact.
- **T+45 exec informational entry.** The exact short message you sent to the exec sponsor; four sentences, not more.
- **T+60 hand-off entry.** Confirmation that the downstream owner has accepted the packet, or escalation to the ladder's alternate.

### Part C — Four one-page signal cards

For each of the four signals, a one-page card with these sections:

- **Source and shape.** Which of the four sources; the shape features that identified it quickly.
- **First-move distinctive to this source.** The move that distinguishes this source's triage from the other three (per Chapter 01's source table).
- **Who gets paged first; who is paged in parallel.** From the escalation ladder.
- **The top risk of posture collapse for this source.** Which of the three postures (investigator, mute, spokesperson) is most likely to fail on *this* source, and the specific prevention.
- **The 60-minute goal.** What the packet looks like for this specific signal shape; what the downstream owner needs to accept it.

Cards are tight — one page per card. Reserve detail for the primary carried signal.

## Starter guidance

- The hardest part of the drill is the **source classification** at T+0. Spend the first fifteen minutes just naming the four signals in your own words against the Chapter 01 source table; the rest of the drill is faster once source is firm.
- The simulated governance-side answers at T+10–T+15 should be reasonable, not optimistic. The governance side will not always pull the tool; a hold with investigation is a common call.
- The external-complaint signal is the one where posture-3 (spokesperson) failure is most likely. Write the paging message and the preservation entry as if the external sender might later subpoena your records.
- The usage-anomaly signal is the one most likely to resolve as *not* an incident. Your triage log should hold the distinction between "I am investigating on the change-management surface" and "I am escalating to incident territory" explicitly for this signal.
- The outcome-regression signal has the longest decision horizon. Your triage will probably fork — part of your output will be the escalation-worthy slice; part will be the parallel business-outcome investigation on the mod-106 scorecard surface. Do not collapse the two.
- Where an organisational fact you need is unknown (specific role titles for your escalation ladder; the exact dashboard metric names; the exec sponsor's title), use `<!-- needs-research: ... -->` inline. Do not invent.

## Deliverables

- `triage-log.md` — the append-only timestamped log for all four signals through T+30.
- `first-hour-timeline.md` — the carried signal extended through T+60.
- `signal-card-01-champion-field-report.md`
- `signal-card-02-usage-anomaly.md`
- `signal-card-03-outcome-regression.md`
- `signal-card-04-external-complaint.md`
- A short cover note (3-5 sentences) summarising which signal was hardest to triage cleanly and why, and the one posture failure you most actively prevented in your drill.

## Acceptance criteria

- The triage log has every required entry for all four signals; entries are timestamped, append-only, and written as observations not findings.
- Source classification is explicit at T+0 for each signal; the first-move distinctive to each source is visible in the T+2 to T+30 entries.
- The carried first-hour timeline extends to T+60 with a packet-assembly entry that lists every artefact in the packet.
- The exec informational entry is four sentences or fewer, informational not substantive.
- Each signal card has all five required sections and fits on one page.
- The named escalation ladder owners are role names (`head-of-ai-governance`, `ai-risk-engineer`, SOC liaison, privacy officer, general counsel), not person names.
- Posture-collapse risks named per signal card are specific, not generic.
- `<!-- needs-research: ... -->` is used wherever an organisational fact is missing.

## Stretch goals

- Add a **false-positive branch** to the usage-anomaly card showing the specific move you would make if investigation on the change-management surface revealed no incident: how the surfaces (dashboard baseline, champion brief) reset without the governance-council thread firing.
- Add a **parallel-regulator scenario** to the external-complaint card showing the specific move you would make if the complaint arrived from two regulators in parallel (for example, a healthcare-system incident that touched both HHS OCR and a state attorney general): how the paging in parallel runs, which named owners carry which thread.
- Draft a **"what I would want on the runbook before the next incident"** memo — one page — naming the specific gaps the drill exposed in your current rollout artefact set. This is the pre-input to Exercise 02 and Exercise 04.

## Why this exercise matters

The incident drill is the discipline that makes the first hour procedural instead of heroic. The role has three jobs on the clock (convene, operate the kill-switch, communicate internally); the drill is where the three jobs are rehearsed against the four source shapes, so that the recognition of source is fast and the first-move does not have to be improvised. The triage log and timeline outputs are the artifacts an auditor or a post-incident review will read — producing them cleanly under a two-hour budget is calibration for producing them cleanly under incident pressure, when the time budget is not two hours but ten minutes.
