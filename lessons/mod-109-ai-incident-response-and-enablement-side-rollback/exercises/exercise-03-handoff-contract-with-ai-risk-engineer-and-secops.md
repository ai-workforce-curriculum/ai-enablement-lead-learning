# Exercise 03 — Handoff Contract with AI Risk Engineer and SecOps

**Estimated effort:** 2.5 hours
**Format:** three handoff contracts + hand-off packet cover sheet template + clock-definition table, Markdown
**Grounding chapters:** [05 — Handoff Contracts](../05-handoff-contracts-ai-risk-engineer-head-of-governance-secops.md); [04 — The First Ten Minutes to the First Hour](../04-the-first-ten-minutes-to-the-first-hour.md). Prior reading: [mod-103 Chapter 07](../../mod-103-policy-co-authoring-with-governance/07-what-you-route-out-counsel-soc-architect.md).

## Objective

Produce the three handoff contracts — enablement lead to `ai-risk-engineer` (L25), enablement lead to `head-of-ai-governance` (L60), enablement lead to security operations / DFIR — in the form each downstream owner would sign, plus a hand-off packet cover sheet template and a clock-definition table across the three contracts. The output is the artefact set that, under a live incident, lets the three downstream owners accept the hand-off and act without further briefing.

## Prerequisites

- Chapters 04 and 05 read.
- [mod-103 Chapter 07](../../mod-103-policy-co-authoring-with-governance/07-what-you-route-out-counsel-soc-architect.md) read.
- Exercises 01 and 02 complete. The triage-log output from Exercise 01 and the evidence-preservation memo from Exercise 02 are inputs.
- The same rollout you carried through Exercises 01 and 02.

## Problem statement

Your `head-of-ai-governance` has asked for the three handoff contracts in writing so that the first-hour handoff in future incidents is not an improvisation. The ai-risk-engineer and the SOC lead have both agreed to review and sign their respective contracts. Legal has agreed to review the packet cover sheet template for preservation-chain language. You have two and a half hours to produce the artefact set at the depth where all three downstream owners can read and sign it.

## Requirements

### Part A — Three handoff contracts

Each contract is a one-to-two-page document with these sections:

1. **Scope.** What signal shapes this contract covers; which rollout(s) it applies to; the authorising role on each side.
2. **What the enablement side delivers.** The specific list per Chapter 05 for this contract. Enumerated; not described in prose.
3. **What the enablement side does not deliver.** The specific anti-scope list per Chapter 05 for this contract.
4. **What the downstream owner delivers back.** The specific list per Chapter 05.
5. **Clocks.** Specific clock values with rationale. If the clock differs from Chapter 05's defaults because of the organisation's shape, name the rationale.
6. **Named humans and the alternate.** Primary contact on each side; alternate if the primary is unreachable.
7. **Signing surface.** Who signs; cadence of resigning (per-role-change, per-year).

### Contract-specific depth

Beyond the common sections, each contract has depth specific to its downstream owner:

- **Contract 1 — ai-risk-engineer.** Include the specific engineered-evidence surfaces you deliver (vendor audit log pull format, operator-side evidence format, usage-anomaly baseline format). Include the specific vendor-side access context fields the ai-risk-engineer needs to open a vendor investigation. Name the vendor's incident contact and SLA (from the vendor DPA).
- **Contract 2 — head-of-ai-governance.** Include the specific close-the-loop preliminary impact-assessment template (which of the five surfaces from Chapter 06 are likely to touch; not the full revision, just the preliminary read). Include the exec-sponsor informational-notification template. Reference the council-brief shape from Chapter 07.
- **Contract 3 — SecOps / DFIR.** Include the specific identity-and-access access-list (which SOC tools or roles need which organisational access during an investigation). Include the vendor DPA's security-incident clause reference. Include the preservation-chain confirmation form (output of Exercise 02's evidence-preservation memo).

### Part B — Hand-off packet cover sheet template

A single template per the Chapter 05 shape. All sections present as empty placeholders ready to be filled under incident conditions. Specifically:

- Incident ID and timestamps row.
- Source classification field (four options to check).
- Tool and vendor row with configuration flags.
- Affected scope section.
- Primary signal link.
- Rollout artifact set links (seven links, one per artifact).
- Current kill-switch state field with timestamp and authorising role.
- Enablement-side provisional read (one-paragraph box, labelled "provisional; not a finding").
- Enablement-side communications state table.
- Access list.
- Role-specific sections: "For the ai-risk-engineer", "For head-of-ai-governance", "For SecOps/DFIR" — each with named fields per Chapter 05.

The cover sheet is a *template*, designed to be filled in rapidly under incident conditions. Write it that way.

### Part C — Clock-definition table

A single table across the three contracts showing the clock values side-by-side. Columns:

- Clock event (e.g., "hand-off packet accepted", "initial read back to enablement side", "full finding").
- Contract 1 (ai-risk-engineer) value.
- Contract 2 (head-of-ai-governance) value.
- Contract 3 (SecOps/DFIR) value.
- Rationale if the three differ.

The table surfaces inconsistencies between the three contracts (if the ai-risk-engineer's first-read clock is longer than SOC's first-read, the table shows it). Resolve inconsistencies in the contracts themselves or justify them in the rationale column.

### Part D — The two-week supporting-mode check-in protocol

A short appendix (half a page) describing the weekly check-in cadence with each of the three downstream owners during the two-week supporting-mode horizon from Chapter 05. For each check-in:

- Attendees.
- Standing agenda (three or four bullets).
- What the enablement side brings.
- What the enablement side explicitly does not demand (status updates that pre-empt the investigation's own cadence).
- Cross-owner coordination the enablement lead is responsible for convening (not substituting for).

## Starter guidance

- The hardest part of each contract is the **"what the enablement side does not deliver"** list. Spend time on this list; it is the discipline that stops boundary collapse during a live incident. The list should be specific, not a general disclaimer.
- The clocks are negotiated, not declared. If the ai-risk-engineer's capacity means a 24-hour first-read is unrealistic, the contract should reflect the realistic clock with the governance-side acknowledgement. Fiction-clocks are worse than long clocks.
- The SecOps contract is the one most likely to require a conversation you have not had. If the organisation has a SOC with an incident-response discipline, the contract leans on that discipline; if not, the enablement lead and the governance side may need to co-stand-up the SecOps-side surface first. Flag gaps inline with a `needs-research` marker where unknown.
- The cover sheet template should be completable in 15 minutes under pressure. If a template field requires research to fill at the moment of the incident, move it to an annex and reserve the cover sheet for the information the enablement lead already has.
- The two-week check-in protocol is often cut as "overhead." Keep it — the biggest post-first-hour failure in Chapter 05 is cross-owner coordination breakdown, and the check-in is where the enablement lead surfaces cross-thread information.
- Where organisation-specific facts are needed (named humans, the vendor DPA's security-incident clause number, the organisation's evidence-store path), flag the gap inline with a `needs-research` marker.

## Deliverables

- `contract-01-ai-risk-engineer.md`
- `contract-02-head-of-ai-governance.md`
- `contract-03-secops-dfir.md`
- `handoff-packet-cover-sheet-template.md`
- `clock-definition-table.md`
- `supporting-mode-check-in-protocol.md`
- A short cover note (3-5 sentences) on the two hardest trade-offs in the clock table and why.

## Acceptance criteria

- Each contract has all seven required sections.
- Each contract's "what the enablement side does not deliver" list is specific and enumerated (not a general disclaimer).
- Each contract's clocks are either the Chapter 05 defaults or named with rationale for the organisation-specific variance.
- Each contract names primary and alternate humans by role.
- The cover sheet template is completable in 15 minutes under pressure; no field requires post-incident research to fill.
- The clock-definition table shows inconsistencies explicitly and resolves or justifies them.
- The supporting-mode check-in protocol names what the enablement lead does not demand.
- A `needs-research` marker is used inline wherever an organisation-specific fact is missing.

## Stretch goals

- Author the **privacy-officer-contract** as a fourth handoff for incidents with personal-data shape. Use the same structure. This is the contract most organisations skip and most regulators ask about during a breach.
- Draft the **general-counsel-contract** as a fifth handoff for incidents with external-communication or litigation-adjacent shape. Same structure; include the specific redirect-to-counsel language the enablement lead uses when a journalist or regulator contacts them directly.
- Produce a **"when-two-contracts-collide"** scenario sketch — a plausible incident where the ai-risk-engineer's clock and the SOC's clock pull in different directions (SOC wants to pull the tool immediately for security; ai-risk-engineer wants a short window to preserve vendor-side evidence first). How the enablement lead convenes the two and surfaces the trade-off to the authorising role.

## Why this exercise matters

The three contracts are what makes the hand-off from Chapter 04 a transfer of ownership rather than a notification or a continuation. Without the contracts in writing, the first-hour handoff is a scramble. With them, the three downstream owners have a legible read of what they get, what they give back, and on what clock — and the enablement side has a legible read of what it does and does not do under incident pressure. Producing the artefact set under a 2.5-hour budget is calibration for revising it against each new tool, each new vendor, and each new role-change on the ladder.
