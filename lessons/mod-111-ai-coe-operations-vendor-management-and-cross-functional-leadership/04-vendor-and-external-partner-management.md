# Vendor and External-Partner Management

> R17 — vendor and external-partner management — sits at 0.23 in the role evidence (6/26 postings, below-threshold but monitored). The low frequency is not low importance; the sample simply reflects that most enablement leads inherit a vendor portfolio rather than build one from zero. By the time the CoE is at steady state, the portfolio is real — a primary tooling vendor, several point-tool vendors, a training-production agency, a change-management consultancy on retainer, a handful of external AI experts and contractors who show up in briefs — and it needs its own operating surface. This chapter authors that surface: screening, training, certification, and the quarterly review that keeps the external portfolio honest.

## Why the role manages vendors as a first-class surface

The temptation, at level 45, is to treat vendors as a procurement problem. Procurement owns contracts, so vendors belong to Procurement. [mod-107](../mod-107-budget-roi-and-build-vs-buy-at-org-scope/README.md) has already named the boundary: this role **partners with procurement on contracts (DPA, SOC 2, model-provenance, data-residency terms)** but does not execute the contracts themselves. The partnership works when the enablement lead brings three things that Procurement cannot:

- **The enablement bar.** A vendor whose contract is clean and whose SOC 2 is current can still deliver training sessions that contradict the org's AI policy, run a pilot that undermines the mod-106 measurement framework, or embed a consultant into a BU whose brief-shaped authority ([mod-110 Chapter 01](../mod-110-commissioning-internal-ai-tools-and-custom-agents/01-the-commissioner-stance-not-the-builder.md)) collapses on contact with the CoE. The bar is enablement-specific and Procurement is not positioned to set it.
- **The portfolio view.** A vendor is in a portfolio of vendors, not a point relationship. Overlapping copilot licences, redundant consultancy retainers, parallel agency engagements — these are visible from the CoE's catalog view, not from the contract view. [mod-107 Chapter 06](../mod-107-budget-roi-and-build-vs-buy-at-org-scope/06-the-vendor-vetting-rubric.md) named the rubric at commission time; this chapter names the operating cadence that keeps the portfolio coherent after commission.
- **The field evidence.** The same field signal that drives the champion community (Chapter 06) and the policy walking-redline ([mod-103](../mod-103-policy-co-authoring-with-governance/README.md)) also reports on vendor delivery. A champion whose tier-two cohort is being trained badly, a policy question a consultant is answering wrong, a SOW that is being delivered three weeks late — the enablement lead is the surface closest to these signals, not Procurement.

The practical consequence: the CoE runs a **vendor portfolio instrument** that is parallel to the service catalog from [Chapter 02](02-the-service-catalog-as-the-coes-public-interface.md) and the operational instruments from [Chapter 03](03-operational-instruments-decision-log-status-report-risk-register.md). The portfolio instrument is what the rest of this chapter walks.

## The four vendor archetypes the enablement portfolio carries

Vendors show up in four distinct archetypes. Each has a different interface with the service catalog, a different certification shape, and a different renewal cadence. Collapsing them into "vendors" loses the operating resolution.

### Archetype 1 — The primary tooling vendor

The licensed productivity-copilot stack the organisation has adopted — the general-purpose copilot plus the domain tools the three-stage selection from [mod-102 Chapter 01](../mod-102-selecting-and-rolling-out-ai-tools/01-the-three-stage-selection-decision.md) has signed. This archetype is low-count (typically 3–8 vendors at steady state in a 5,000-person organisation) and high-contract-value. Example shapes in the current market: Microsoft 365 Copilot or Google Gemini for Workspace or Zoom AI Companion at the productivity surface; Cursor, GitHub Copilot, Claude Code, or Windsurf at the engineering surface. These names change; the archetype does not.

**Interface with the catalog.** The primary tooling vendor sits behind the Tool Selection, Pilot, and Rollout slots. The vendor's product is what the slots are delivering against.

**Certification shape.** The tooling vendor is certified by Procurement, Security, Privacy, and the AI council (Chapter 05) jointly at adoption time. The enablement lead's certification contribution is: the rollout artefact set is deliverable, the training package is authorable against the vendor's product surface, the measurement framework from [mod-106](../mod-106-outcome-measurement-and-executive-reporting/README.md) can be instrumented against the vendor's telemetry.

**Renewal cadence.** Annual to tri-annual depending on the contract. The enablement lead's input to the renewal is the outcome evidence from the scorecard and the field evidence from the champion community.

### Archetype 2 — The training-production agency

An external agency that authors or delivers training content on retainer — the role-based playbooks from [mod-104 Chapter 04](../mod-104-training-programs-and-ai-literacy-curriculum/04-role-based-playbooks-and-use-case-libraries.md), the specialist-tier bootcamps from [mod-104 Chapter 05](../mod-104-training-programs-and-ai-literacy-curriculum/05-the-delivery-mix.md), or the foundational curriculum for a specific function. The enablement program's bandwidth is finite; a training-production agency is often the surge capacity that lets the CoE's small team ship a big curriculum.

**Interface with the catalog.** The agency sits behind the Training and Enablement slot. Their deliverables are inside the artefact bundle the slot returns.

**Certification shape.** The agency is certified by the enablement lead against four criteria:

1. **Policy fluency.** The agency has read the organisation's acceptable-use policy, data-handling SOP, and escalation path. They are not teaching "what the vendor's product does"; they are teaching what the *organisation* has decided is in-policy use.
2. **Outcome framing.** Deliverables cite the mod-106 outcome / workflow / usage framework. Training that is measured on satisfaction only, without an outcome handoff, fails certification.
3. **Internal co-authorship.** The agency produces content *with* the CoE and *with* HR / L&D, not in isolation. A certification entry names the specific internal co-authors on each deliverable.
4. **Field-signal openness.** The agency receives field reports from the champion community during delivery and folds the signal into revisions. An agency that ships a curriculum once and does not revise on field signal fails certification on renewal.

**Renewal cadence.** Typically annual, with a quarterly delivery review inside the year.

### Archetype 3 — The change-management or implementation consultancy

Consultants who embed inside a BU to accelerate an enablement initiative — a specific BU's rollout, a specific industry-flavour adjustment ([mod-108](../mod-108-industry-and-regulatory-flavours-of-enablement/README.md)), or a specific capability gap the CoE's internal shape cannot cover. These are typically engagement-shaped (a named SOW, a named start and end date, named deliverables) rather than retained.

**Interface with the catalog.** Consultants plug into the Rollout slot and the Incident Support slot. In more mature CoEs, they also plug into Tool Selection when the three-stage decision is in a high-regulation industry and the consultancy carries specific regulatory experience.

**Certification shape.** The consultancy is certified against the enablement-lead-shape work they are delivering into. Specifically:

1. **Brief-shaped authority discipline.** If the consultancy is operating adjacent to the AI Engineering family on a commissioned build, the consultancy honours the Chapter 01 of [mod-110](../mod-110-commissioning-internal-ai-tools-and-custom-agents/01-the-commissioner-stance-not-the-builder.md) posture — they do not write architecture into briefs; they do not inherit the apologist posture when outcomes miss.
2. **Rollout-artefact-set fluency.** The consultancy delivers against the seven-piece artefact set from [mod-102 Chapter 03](../mod-102-selecting-and-rolling-out-ai-tools/03-the-rollout-artifact-set.md); their deliverable fits *into* the organisation's artefact bundle, not alongside it as a separate consulting deck.
3. **Hand-off completeness.** The consultancy's engagement includes a hand-off plan for the CoE's operating team. "We built it, we ran it, we leave" without a hand-off is a certification failure.
4. **Dissent recording.** When the consultancy disagrees with a CoE decision, the dissent is recorded in the decision log ([Chapter 03](03-operational-instruments-decision-log-status-report-risk-register.md)) as a named entry, not carried as resentment into the engagement.

**Renewal cadence.** Per-engagement at SOW close. Multi-year retainers are allowed but should be re-certified annually.

### Archetype 4 — The external AI expert on call

An individual contractor, a university affiliate, or a boutique expert the CoE calls when a specific deep question needs expertise the internal team does not carry — a question of agent-system architecture pattern beyond Chapter 04 of [mod-110](../mod-110-commissioning-internal-ai-tools-and-custom-agents/04-handing-architectural-depth-to-the-agentic-systems-architect.md), a question of empirical productivity methodology beyond the literature read in [mod-106 Chapter 04](../mod-106-outcome-measurement-and-executive-reporting/04-reading-the-empirical-ai-productivity-literature-for-method-not-numbers.md), a question of industry-regulator interpretation beyond [mod-108](../mod-108-industry-and-regulatory-flavours-of-enablement/README.md)'s read.

**Interface with the catalog.** External experts plug into the Outcome Measurement and Tool Selection slots as a specialist consult surface, not as a delivery surface. They do not produce the artefact bundle; they inform the CoE's authorship of it.

**Certification shape.** Light-weight. The expert is vetted on:

1. **Named prior work.** The expert is cited for a specific body of work — a paper, a public talk, a prior engagement — that is relevant to the specific question being asked. "Generalist AI expert" is not a certification shape.
2. **Advisory posture.** The expert's output is an advisory memo cited in the CoE's decision log, not a deliverable the CoE is bound to execute.
3. **Conflict declaration.** The expert declares any current or prior relationships with the primary tooling vendors or the training-production agencies in the portfolio.

**Renewal cadence.** None — engagements are per-question. A recurring expert is either reclassified as a consultancy or formalised as a part-time hire.

## The vendor portfolio instrument

The portfolio is tracked as a single living artefact, maintained alongside the three instruments from [Chapter 03](03-operational-instruments-decision-log-status-report-risk-register.md). Required fields per vendor:

- **Vendor ID.** Durable; reused across contracts and engagements.
- **Archetype.** One of the four above.
- **Current engagement.** Named SOW, retainer, or licence with start and end dates and scope.
- **Catalog slot(s).** Which slot(s) from [Chapter 02](02-the-service-catalog-as-the-coes-public-interface.md) the vendor plugs into.
- **Certification status.** Current / under review / lapsed, with date of last review.
- **Delivery history.** Material misses or notable wins from prior cycles, cross-referenced to the decision log and the status report.
- **Risk-register items.** Open items on the risk register ([Chapter 03](03-operational-instruments-decision-log-status-report-risk-register.md)) that reference this vendor.
- **Named counterpart.** The specific human at the vendor the enablement lead or operations analyst talks to. Not "support@vendor.com"; a name.
- **Contract hygiene.** DPA signed, SOC 2 current, model-provenance terms clear, data-residency terms satisfied, AI-specific clauses (training-data usage, model-output ownership, right-to-audit) negotiated. These belong to Procurement but are mirrored in the portfolio view so the lead can read the hygiene without a procurement query.

The portfolio is read:

- **Weekly** at Thursday writing — the vendors with open risk-register items get checked; the vendors with impending renewals get flagged.
- **Monthly** at the service-catalog monthly deep dive ([Chapter 01](01-the-coe-at-steady-state.md)) — the slot's vendor-dependency map is read.
- **Quarterly** at the full portfolio review (below).
- **Annually** at the budget re-read ([mod-107](../mod-107-budget-roi-and-build-vs-buy-at-org-scope/README.md)) — the portfolio's cost line items are reconciled with the enablement cost model.

## Screening — who becomes a vendor in the first place

Screening answers *should this vendor enter the portfolio*. The screening gate is upstream of the three-stage selection from [mod-102 Chapter 01](../mod-102-selecting-and-rolling-out-ai-tools/01-the-three-stage-selection-decision.md) for tooling vendors and upstream of the engagement SOW for service vendors. Six screening questions:

1. **Does the vendor's product or service map to a named service-catalog slot?** A vendor whose offering does not map to a slot is a vendor the CoE cannot operate against.
2. **Is there an existing vendor in the portfolio already covering this slot?** If yes, the screening becomes a "replace or add" conversation, not a "sign" conversation. Portfolio concentration (one vendor per slot or one plus a backup) is the default; parallel overlapping vendors is the exception that needs justification.
3. **Does the vendor's AI posture align with the organisation's policy stack?** Specifically: the vendor's training-data position (opt-out available), the vendor's model-output ownership position (customer-owned), the vendor's data-residency position (matches the organisation's regulated surface), the vendor's security posture (SOC 2 Type II current, or an equivalent).
4. **Does the vendor's delivery model fit the operating loop?** A vendor whose delivery model requires a dedicated internal product manager, a weekly steering committee, or a bespoke environment the CoE cannot staff is a vendor the CoE cannot support without a budget-shape conversation.
5. **Does the vendor commit to the enablement bar?** The four-criteria certification (archetype-specific) is the enablement-side commitment. A vendor who cannot commit to the four is a vendor the CoE cannot bring into the portfolio.
6. **What is the exit cost?** How difficult is it to leave the vendor — data-migration cost, re-training cost, licence commitment cost? A high exit cost is not a disqualifier, but it is a disclosed cost the portfolio carries forever.

The screening is not done by the enablement lead alone. Procurement, Security, Privacy, and (for training vendors) HR / L&D are all co-signatories. A vendor who passes screening is cleared for the three-stage selection (tooling) or the SOW authorship (service) — not yet signed.

## Training — making the vendor usable inside the operating loop

Once a vendor is signed, the lead's job is to make the vendor *usable* — specifically, to bring the vendor's working team to a point where they can operate inside the organisation's AI policy stack, training surface, measurement framework, and incident path. This is "training the vendor" and it is a first-class activity, not a soft-skill nicety.

### Vendor-training content

Four required areas per archetype:

- **The approved-tool envelope and policy stack.** The acceptable-use policy ([mod-103 Chapter 04](../mod-103-policy-co-authoring-with-governance/04-the-one-page-acceptable-use-policy.md)), the data-handling SOP ([mod-103 Chapter 05](../mod-103-policy-co-authoring-with-governance/05-the-data-handling-sop.md)), and the intake questionnaire. A vendor who does not know the policy stack will accidentally contravene it, and the contravention will be the enablement lead's problem to clean up.
- **The rollout artefact set.** The seven-piece artefact set from [mod-102 Chapter 03](../mod-102-selecting-and-rolling-out-ai-tools/03-the-rollout-artifact-set.md). Vendors who are producing content or running delivery need to understand which slots in the artefact set they are producing against.
- **The measurement framework.** The outcome / workflow / usage stack from [mod-102 Chapter 04](../mod-102-selecting-and-rolling-out-ai-tools/04-measuring-whether-the-rollout-changed-anything.md) and the exec-scorecard discipline from [mod-106](../mod-106-outcome-measurement-and-executive-reporting/README.md). Vendors who are delivering anything the scorecard reports on need to know what metrics mean, how baselines are set, and how a confidence band is read.
- **The incident path and the kill-switch.** The enablement-side incident path from [mod-109](../mod-109-ai-incident-response-and-enablement-side-rollback/README.md), named escalation contacts, kill-switch mechanics. Vendors who are operating in production need to know how to recognise, escalate, and *not interfere with* an incident.

### Delivery shape

Vendor training is typically a one-day session at engagement kickoff plus a half-day refresh per renewal. The CoE's operations analyst owns scheduling; the enablement lead delivers the policy and incident sections personally for the certification record. For primary tooling vendors who deliver at scale, a quarterly refresh is standard practice.

The training's evidence is a signed attestation per vendor — specific humans at the vendor confirm they received the training and will operate within it. The attestation lives in the governance evidence store alongside the vendor's contract.

## Certification — the bar vendors have to meet to deliver

Certification is the enablement-side signal that a vendor is cleared to deliver into the catalog. The archetype-specific criteria named above are the certification bar. The certification artefact is short — a one-page certification record per vendor per cycle — that names:

- **Vendor, archetype, scope of certification.**
- **The named criteria that apply to this archetype.**
- **The evidence satisfying each criterion** — a cited deliverable, a session attendance record, a dissent entry in the decision log, a field-report fold-back memo.
- **The certification period.** Typically one year for ongoing engagements, per-engagement for consultancies.
- **The renewal date.** Visible on the portfolio instrument.
- **Signed by** the enablement lead and the vendor's named counterpart.

Certification is renewable, revocable, and loseable. The three states:

- **Current.** All criteria satisfied with cited evidence; renewal date not yet reached.
- **Under review.** One or more criteria lacking evidence; the vendor is operating on a conditional basis with a specific remediation deadline. Status flagged on the portfolio and on the status report.
- **Lapsed.** Remediation deadline missed, or evidence of a criteria breach surfaced. The vendor cannot deliver into the catalog until recertified. Certification lapse is a decision-log entry with a named why.

The three-state discipline is what gives certification meaning. A certification that cannot be lapsed is a stamp, not a bar. A vendor who moves to lapsed status is a vendor the catalog's affected slots have to re-plan for — the Monday triage next week will reflect the loss.

## The quarterly portfolio review

Once a quarter the enablement lead and the operations analyst — joined by named counterparts from Procurement, Security, and (for training vendors) HR / L&D — walk the entire vendor portfolio in a two-hour session. The review is sequenced:

1. **Walk the portfolio by archetype.** Every active vendor in each of the four archetypes is reviewed against delivery history, certification status, risk-register items, and renewal cadence.
2. **Reconcile with the budget.** The portfolio's cost rollup is checked against the enablement cost model's vendor line ([mod-107 Chapter 01](../mod-107-budget-roi-and-build-vs-buy-at-org-scope/01-the-enablement-cost-model-at-org-scope.md)). Overspend flagged; underspend investigated.
3. **Surface concentration risks.** Any slot with only one vendor and no backup, any BU with a single consultancy dependency, any archetype whose cost is above 40% of the portfolio total.
4. **Decide renewals.** Vendors whose renewal is in the next quarter are given an explicit renew / renegotiate / replace call, logged in the decision register.
5. **Decide lapses and remediations.** Under-review vendors are given either a path back to current or a lapse decision; lapsed vendors are given a path to re-certification or exit.
6. **Author one vendor-portfolio page** for the quarterly ritual's exec review packet (Chapter 05).

The review output is a decision-log entry per vendor action, a risk-register delta, and the quarterly page. The review is not a renegotiation forum — contract renegotiations are triggered by the review and executed by Procurement.

## Three vendor-management failure modes

### Failure mode 1 — The locked-in primary vendor

The primary tooling vendor was signed three years ago on a tri-annual contract. The org's enablement has matured; the field evidence is telling the CoE the product is not keeping up with the organisation's needs. The contract still has eight months to run. The lead, feeling that a re-selection decision in-contract is a procurement embarrassment, defers the conversation to renewal.

**Correction.** The three-stage selection from [mod-102 Chapter 01](../mod-102-selecting-and-rolling-out-ai-tools/01-the-three-stage-selection-decision.md) is re-run *inside* the contract term, not at renewal. The output is a decision-log entry: "re-selection concluded with [renew / renegotiate / replace at renewal] recommendation; evidence below." Renewal then runs against the recommendation, not against inertia. Procurement is not embarrassed by a well-cited mid-contract re-selection; Procurement is embarrassed by a surprise non-renewal decision at the last moment.

### Failure mode 2 — The consulting engagement that absorbs the CoE

The consultancy was brought in to accelerate a specific BU rollout. Six months in, the consultancy is attending Monday triage, writing sections of the Thursday status report, co-chairing the AI council. The CoE's internal team has quietly handed over institutional authority.

**Correction.** The certification criteria's hand-off completeness and brief-shaped authority discipline are the enforcement surface. At every engagement checkpoint — typically monthly for a consultancy engagement — the lead asks explicitly: *what is the hand-off path from this consultancy back to the internal team on each deliverable, and what is the date it closes?* An engagement without a visible hand-off path is an engagement that has over-absorbed the CoE.

### Failure mode 3 — The expert network without conflict declarations

The external AI experts on call are consultants who also carry working relationships with the tooling vendors in the primary portfolio. An expert consulted on a Tool Selection decision is simultaneously on retainer with the vendor being compared against. The conflict is not disclosed; the recommendation is not neutral.

**Correction.** The archetype-4 certification's conflict-declaration criterion is non-negotiable. Every expert engagement opens with a written declaration of current and recent vendor relationships; a declared conflict does not disqualify but does require disclosure in the decision log entry that cites the expert. An expert who declines to make the declaration is an expert who cannot be used.

## The relationship to the chapters ahead

- [Chapter 05](05-the-quarterly-cross-functional-operating-ritual.md) is where the quarterly portfolio review's output is read into the exec review and the AI council. Vendor-portfolio decisions above the delegated budget ceiling are council decisions.
- [Chapter 06](06-the-org-wide-champions-community-of-practice.md) is where field signal on vendor delivery surfaces; the community is one of the certification evidence sources (field-signal openness criterion).
- [Chapter 07](07-the-credentials-portfolio-as-shared-vocabulary.md) names the shared vocabulary that lets the enablement lead and the vendor counterparts speak the same frames — AIGP for governance, Prosci for change-management, ISO/IEC 42001 for standards.

## Summary

- **The lead manages vendors as a first-class surface in partnership with Procurement.** The partnership works when the lead brings the enablement bar, the portfolio view, and the field evidence that procurement is not positioned to supply.
- **Four vendor archetypes carry distinct interfaces, certification shapes, and renewal cadences:** the primary tooling vendor, the training-production agency, the change-management or implementation consultancy, and the external AI expert on call.
- **The vendor portfolio instrument sits alongside the operational instruments from [Chapter 03](03-operational-instruments-decision-log-status-report-risk-register.md).** It is read weekly, monthly, quarterly, and annually against the operating loop and the budget.
- **Screening is a six-question pre-gate, done jointly with Procurement, Security, Privacy, and HR / L&D.** A vendor who does not map to a catalog slot is a vendor the CoE cannot operate.
- **Training the vendor is a first-class activity.** Policy stack, rollout artefact set, measurement framework, incident path — the four content areas every vendor working inside the CoE's delivery surface needs.
- **Certification is a three-state discipline.** Current, under review, lapsed. A certification that cannot be lapsed is a stamp, not a bar.
- **The quarterly portfolio review** is the standing surface where vendor decisions are made. Renewals, remediations, and lapses are logged in the decision register; concentration risks surface on the risk register; an output page feeds the exec review.
- **Three failure modes to watch:** the locked-in primary vendor whose re-selection never happens, the consultancy that absorbs the CoE, and the expert network whose conflicts are not declared. Each has a specific correction inside the certification discipline.
