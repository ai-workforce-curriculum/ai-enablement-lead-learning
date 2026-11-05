# The Quarterly Cross-Functional Operating Ritual

> The weekly operating loop ([Chapter 01](01-the-coe-at-steady-state.md)), the service catalog ([Chapter 02](02-the-service-catalog-as-the-coes-public-interface.md)), the three operational instruments ([Chapter 03](03-operational-instruments-decision-log-status-report-risk-register.md)), and the vendor portfolio ([Chapter 04](04-vendor-and-external-partner-management.md)) keep the CoE functional at steady state. Once a quarter the CoE has to be legible to the rest of the organisation — governance, the executive leadership team, business-unit leaders, and the functional partners who deliver into the enablement program but do not report into it. That legibility is a scheduled ritual, not a one-off deck. This chapter authors the ritual: who sits at each surface, what is decided there, what moves between surfaces, and how the quarter's work gets its cross-functional sign-off.

## Why "ritual" and not "meeting series"

A meeting series suggests an itinerary. A ritual suggests a repeating pattern whose shape is worth preserving even when the content changes quarter-to-quarter. The distinction matters because the cross-functional surface has four properties a meeting series does not reliably produce:

- **It is scheduled a year in advance, not a quarter.** The AI council, exec review, BU reviews, and functional-partnership renewals all appear on the enterprise calendar at the start of the fiscal year. Rescheduling is possible but costly; the ritual's standing makes the CoE's authority routine, not contested.
- **It carries a standing agenda before specific content.** The AI council's quarterly agenda has the same shape every quarter — operating-loop read, service-catalog review, risk-register escalations, policy stack re-read, vendor-portfolio review. Content varies; shape does not. The standing agenda is what lets substitute attendees read the artefacts without the lead re-explaining the structure.
- **It signs decisions, not conversations.** Every surface produces decision-log entries ([Chapter 03](03-operational-instruments-decision-log-status-report-risk-register.md)). A meeting that produces no decision-log entries is a meeting that did not run; a ritual whose surfaces reliably produce entries is a ritual that is operating.
- **It renews partnerships, not just reviews work.** The functional-partnerships surfaces specifically recommit on cadence. A quarter without a renewal is a quarter in which partnerships drift; the ritual prevents the drift by making recommitment a visible event.

R15 (cross-functional program management, 0.35) names the general practice; this chapter names the AI-CoE-specific application of the practice.

## The four surfaces of the quarterly ritual

The ritual has four distinct surfaces, each with a different composition, cadence, duration, and decision scope. They do not substitute for each other and they are not collapsed into one big meeting.

### Surface 1 — The AI Council (quarterly, 90 minutes)

The governance-and-enablement operating council. The seat the role was taught to hold in [mod-103 Chapter 02](../mod-103-policy-co-authoring-with-governance/02-the-governance-council-liaison-seat.md) is the enablement liaison seat on *this* council. Attendees:

- **Chair:** `head-of-ai-governance` (level 60).
- **Enablement seat:** the enablement lead (this role, level 45).
- **Architect seat:** `senior-ai-governance-architect` (level 50).
- **Risk-engineering seat:** `ai-risk-engineer` (level 25).
- **Program-governance analyst:** `ai-governance-analyst` (level 15).
- **Industry counsel where applicable:** legal, security, privacy representatives for regulated BUs ([mod-108](../mod-108-industry-and-regulatory-flavours-of-enablement/README.md)).
- **CAIO observer seat** when a chief-ai-officer is in place.

**Standing agenda:**

1. **Operating-loop read.** The enablement lead walks the quarter's status reports, citing the decision log and risk register. Misses-first ([Chapter 03](03-operational-instruments-decision-log-status-report-risk-register.md)); eight-ten minutes.
2. **Service-catalog review.** The slot-by-slot read of the service catalog's quarterly throughput, SLA misses, deprecations proposed. 10 minutes.
3. **Risk-register escalations.** The lead presents the program-level risks the council has to decide on; the governance chair rules.
4. **Policy stack re-read.** Policy edits proposed, policy items in redline against field signal from [mod-105 Chapter 03](../mod-105-champion-networks-and-change-management/03-routing-field-signal-back-to-policy-tooling-and-training.md), new policy asks raised by the industry-flavour slice ([mod-108](../mod-108-industry-and-regulatory-flavours-of-enablement/README.md)). Decisions signed in the council's own log, cross-referenced from the CoE's decision register.
5. **Vendor-portfolio review.** The quarterly portfolio page from [Chapter 04](04-vendor-and-external-partner-management.md). Certification lapses, concentration risks, renewals. Decisions above the enablement lead's delegated ceiling are council-signed.
6. **Incident patterns.** Incidents from the quarter ([mod-109](../mod-109-ai-incident-response-and-enablement-side-rollback/README.md)), the fold-back status, open after-action items.
7. **Next quarter preview.** What the CoE expects to bring to the council next quarter. Signal of focus, not commitment.

**What this surface is for:** program-level governance of the enablement operating system. Items that the enablement lead cannot decide alone — policy edits, certification lapses with budget consequence, risk escalations crossing governance's own authority — are the AI council's work.

**What this surface is *not* for:** executive storytelling. The council is operational; the exec review (Surface 2) is where the executive storytelling happens.

### Surface 2 — The Executive Leadership Team Review (quarterly, 60 minutes)

The CAIO's review of the enablement program, with the CEO / COO / CFO or equivalent members of the executive leadership team in attendance.

**Attendees:**

- **Chair:** the CAIO (level 70). If no CAIO is in place, the enablement lead's executive sponsor chairs. The chair is not the enablement lead — this is the point of the surface; the lead presents to a chair who has more authority than the lead.
- **Executive leadership members** at the level the organisation convenes for strategic reviews.
- **Enablement lead** as presenter.
- **Governance observer:** `head-of-ai-governance`. Governance is not the presenter but is in the room so that the exec read of enablement is not detached from the governance read of risk.

**Standing agenda (60 minutes total, tight):**

1. **The quarter's outcome scorecard.** The exec-scorecard [mod-106 Chapter 02](../mod-106-outcome-measurement-and-executive-reporting/02-authoring-the-executive-scorecard-weekly-monthly-quarterly.md) quarterly deep-read. 15 minutes. Misses first.
2. **The programmatic highlights.** The two or three in-flight initiatives of the kind an exec reader cares about. 10 minutes.
3. **The budget read.** The quarter's spend vs. plan, the forward-looking cost curve, the ROI confidence bands from [mod-107 Chapter 02](../mod-107-budget-roi-and-build-vs-buy-at-org-scope/02-projecting-roi-with-confidence-bands.md). 10 minutes.
4. **The asks.** What the enablement program needs from the executive leadership this quarter — a decision on a vendor renewal above the delegated ceiling, a signal on a BU conflict, a sponsor commitment on a change-management mandate. 10 minutes.
5. **Discussion.** 15 minutes.

**What this surface is for:** executive alignment on the enablement program's trajectory, authorisation on asks that require executive sign-off, and the standing legibility of the program to the people funding it.

**What this surface is *not* for:** program operations. If the exec review's discussion keeps pulling into operational detail, the AI council's output is not adequately summarising the operating picture and the lead's deck has drifted into project-management minutiae.

### Surface 3 — The BU Leadership Reviews (quarterly, 30–45 minutes each)

One review per business unit of material enablement-program footprint. In a 12,000-person organisation this might be 6–10 BUs; in a 3,000-person organisation, 3–5. Each review is one-to-one between the enablement lead and the BU head (plus the BU's embedded enablement partner if the pattern family [mod-101 Chapter 02](../mod-101-role-and-the-org-wide-enablement-operating-model/02-the-ai-coe-pattern-family.md) carries one).

**Standing agenda (30–45 minutes):**

1. **The BU's slice of the scorecard.** The outcome / workflow / usage reads specific to this BU's rollouts. 10 minutes.
2. **The BU's champion network health.** The adoption curve, the retention, the resistance signal from [mod-105 Chapter 07](../mod-105-champion-networks-and-change-management/07-measuring-change-management-health.md). 10 minutes.
3. **The BU's tooling and pilot status.** In-flight selections, pilots, rollouts, commissions specific to the BU. 10 minutes.
4. **The BU's asks.** What the BU wants the enablement program to prioritise next quarter. 5–10 minutes.
5. **The lead's asks.** What the enablement program needs from the BU — exec-sponsor attention on a specific rollout, champion recruitment, access to a function for a baseline read. 5 minutes.

**What this surface is for:** keeping the enablement program in cadence with each BU's reality, picking up BU-specific field signal that the standing instruments miss, and honouring the federated or hub-and-spoke pattern's scope-contract commitment to each BU's autonomy.

**What this surface is *not* for:** renegotiating the service catalog on a BU-by-BU basis. Catalog revisions happen at the AI council; the BU review surfaces the ask that the council processes, it does not substitute for the council.

### Surface 4 — The Functional-Partnership Renewal Reviews (quarterly, 30 minutes each)

The quarterly recommitment with each of the functional partners whose service into the enablement program is contracted but not reporting. Seven standard partnerships:

- **HR.** Role-based playbook adoption across the HR function, delivery partnership for leadership training ([mod-104 Chapter 08](../mod-104-training-programs-and-ai-literacy-curriculum/08-partnering-with-hr-ld-and-internal-comms.md)), recognition-and-recognition surfaces for the champion community ([Chapter 06](06-the-org-wide-champions-community-of-practice.md)).
- **L&D.** The AI-literacy curriculum's delivery partnership, the learning-platform integration, the fluency-assessment instrumentation.
- **IT.** The approved-tool envelope's operational surface — provisioning, SSO / IAM, access and offboarding ([mod-102 Chapter 03](../mod-102-selecting-and-rolling-out-ai-tools/03-the-rollout-artifact-set.md) artefact 3).
- **Legal.** The policy stack's legal-review partnership ([mod-103](../mod-103-policy-co-authoring-with-governance/README.md) is the depth); industry-flavour counsel on regulated rollouts ([mod-108 Chapter 08](../mod-108-industry-and-regulatory-flavours-of-enablement/08-partnering-with-industry-counsel-without-opining.md)).
- **Security.** The vendor-screening security review, the incident-path handoff contracts ([mod-109 Chapter 05](../mod-109-ai-incident-response-and-enablement-side-rollback/05-handoff-contracts-ai-risk-engineer-head-of-governance-secops.md)).
- **Privacy.** The data-handling SOP ([mod-103 Chapter 05](../mod-103-policy-co-authoring-with-governance/05-the-data-handling-sop.md)) and the industry-flavour privacy reads ([mod-108 Chapter 03](../mod-108-industry-and-regulatory-flavours-of-enablement/03-healthcare-flavour-hipaa-and-phi.md), [Chapter 06](../mod-108-industry-and-regulatory-flavours-of-enablement/06-education-flavour-ferpa-coppa-and-ed-tech.md)).
- **Procurement and Finance.** The vendor portfolio ([Chapter 04](04-vendor-and-external-partner-management.md)), the enablement cost model ([mod-107 Chapter 01](../mod-107-budget-roi-and-build-vs-buy-at-org-scope/01-the-enablement-cost-model-at-org-scope.md)), the budget re-read.

**Standing agenda for each partnership review:**

1. **The last quarter's partnership contract.** Was each named commitment met? Misses first.
2. **The current quarter's partnership contract.** What is the enablement program committing to on this partner's surface; what is the partner committing to on the enablement program's surface.
3. **Signal and feedback.** What each side has picked up about the other that needs naming.
4. **Signature.** The partnership contract for the quarter is co-signed and filed in the governance evidence store.

**What this surface is for:** keeping the partnerships live. A partnership that goes two quarters without a renewal review is a partnership that is operating on memory of a prior commitment.

**What this surface is *not* for:** executing partnership work. Work happens in the weekly loop; the renewal review is the standing surface where the contract itself is maintained.

## Sequence and interlock across the ritual

The four surfaces run in a specific sequence inside the quarter. The sequence is what makes the ritual legible, not just repeated.

### Weeks 1–3 of the quarter — Operating work

The first three weeks are the weekly loop running at full volume. No ritual surfaces fire. The CoE is executing against the catalog, closing the prior quarter's open items, and populating the risk register with new items.

### Week 4 — The AI council (Surface 1)

The council meets at the beginning of the quarter's operating depth, not the end. The reason is forward-looking: council decisions on policy edits, vendor certifications, and risk escalations need to land before the rest of the quarter can be planned against them. A council meeting in Week 12 of the quarter is a council meeting that is ratifying history; a council meeting in Week 4 is a council meeting that is setting the quarter.

### Week 5 — The BU leadership reviews (Surface 3)

The BU reviews happen *after* the council's policy and catalog signals have landed. The lead walks each BU head with a current read of the operating picture; BU-specific asks that surface here are logged and routed. Reviews are stacked across one or two weeks — not one per week spread across a quarter.

### Week 6 — The executive leadership team review (Surface 2)

The exec review follows the council and the BU reviews. The exec review's content is the quarterly scorecard read, and the scorecard is credible only after the council's governance read has signed and the BU reviews have surfaced the BU-specific asks. An exec review that fires before the council is an exec review that is briefing the CAIO on an incomplete operating picture.

### Weeks 7–11 of the quarter — Operating work, renewals interleaved

The weekly loop continues. The functional-partnership renewals (Surface 4) run one per week across the five weeks, with the operations analyst scheduling. Each renewal is a 30-minute commitment that the lead holds personally with the partner lead; neither side delegates.

### Week 12 of the quarter — Close-out

The lead closes the quarter against the decision log, the risk register, and the status-report archive. The quarterly deep-read for one service-catalog slot ([Chapter 01](01-the-coe-at-steady-state.md)) is written. The budget actuals are reconciled with Finance. The outputs of the quarter — the council's own decisions, the exec review's signed asks, the BU reviews' outputs, the signed partnership contracts — are filed in the governance evidence store.

### Week 13 — The new quarter begins

The lead walks the new quarter's planned catalog against the prior quarter's outcomes; the operations analyst resets the risk register's aging clock; Monday triage opens with the new quarter's first batch of intake. The ritual restarts.

## What moves across surfaces

Information flows through the ritual in a specific pattern:

- **Field signal** originates at the champion-community level ([Chapter 06](06-the-org-wide-champions-community-of-practice.md)) and the BU reviews (Surface 3). It becomes part of the operating loop's weekly instruments, then feeds into the council (Surface 1) at the next quarter.
- **Policy edits** originate at the council (Surface 1) and flow down to the policy stack and the training content. Field signal from Surface 3 is the input that the council's policy agenda operates on.
- **Vendor-portfolio decisions** originate at the quarterly portfolio review ([Chapter 04](04-vendor-and-external-partner-management.md)), surface at the council (for certifications and lapses) and at the exec review (for renewal asks above the delegated ceiling). Procurement and Finance enter via Surface 4.
- **Budget asks** originate at the enablement cost model's operating reality, surface at the exec review (Surface 2), and are reconciled quarterly with the Finance partnership review.
- **Partnership contracts** originate at Surface 4 and feed the assumptions each of the other surfaces runs on. A partnership that is not renewed on Surface 4 is a partnership whose commitments cannot be cited at Surfaces 1–3 the next quarter.

The movement is the ritual's functional property. A surface that stops feeding the surfaces downstream from it has broken the ritual. The lead's job in Week 12 is to confirm the movement happened; if it did not, the close-out memo flags it for the next quarter's plan.

## Three ritual failure modes

### Failure mode 1 — The council becomes a status meeting

Symptom: the AI council spends its 90 minutes being briefed on the operating loop. No decisions are made; no escalations are ruled on; the council's own decision log is empty.

Diagnosis: the enablement lead is bringing the council an operating-loop read without an ask. The standing agenda's first item (operating-loop read) has absorbed the rest of the meeting.

Correction: compress the operating-loop read to 8–10 minutes as the agenda specifies. The remaining 80 minutes are items 2–7 of the agenda, each with a specific ask — a policy edit to sign, an escalation to rule on, a vendor certification to lapse, a catalog slot to deprecate. A council meeting that cannot produce 4–8 decision-log entries is a council meeting whose structure is being misused.

### Failure mode 2 — The exec review becomes the executive's daily

Symptom: the CAIO or executive sponsor keeps asking for additional reads between the quarterly exec reviews. The quarterly surface is not sufficient; the lead is drafting bespoke briefings every few weeks.

Diagnosis: the quarterly surface's content is too high-level for the executive to track, *or* the weekly status report is not reaching the executive, *or* the executive is treating the lead as a reactive briefer rather than a standing one.

Correction: tier the exec distribution. The weekly status report should be on the executive's standing read; the monthly scorecard rollup should be a standing dashboard; the quarterly review is the decision surface. If bespoke briefings are still being requested after tiering, the ask is about the executive's own operating style rather than about the ritual, and the lead has a one-on-one with the executive about the tiers.

### Failure mode 3 — The partnership contracts stop being signed

Symptom: the functional-partnership renewals are happening on calendar but the contract artefact is not being updated. Last quarter's contract is still the live document.

Diagnosis: the renewal review has become a catch-up meeting rather than a commitment surface. Both sides show up, exchange updates, and leave.

Correction: the operations analyst prepares a draft contract redline ahead of each renewal review; the review is a 30-minute signature session, not a drafting session. If the redline cannot be prepared ahead, the preceding quarter's partnership was underspecified and the renewal becomes a scope re-read rather than a signature. Either outcome ends with a signed quarter-specific contract.

## The relationship to the chapters ahead

- [Chapter 06](06-the-org-wide-champions-community-of-practice.md) names the community of practice that sits above the per-team champion networks. The community's surface is the field-signal engine that feeds the BU reviews and the council.
- [Chapter 07](07-the-credentials-portfolio-as-shared-vocabulary.md) names the credentials portfolio that makes the ritual's cross-functional surfaces legible — AIGP shared between the council and governance, Prosci / ATD shared between the BU reviews and HR / L&D, ISO/IEC 42001 shared between the council and architect / risk seats.

## Summary

- **The quarterly ritual is a standing pattern, not a meeting series.** It is scheduled a year in advance, carries a standing agenda per surface, produces decision-log entries, and renews partnership contracts on cadence.
- **Four surfaces, each with distinct composition and decision scope:** the AI council for program-level governance, the exec review for executive alignment and asks, the BU leadership reviews for BU-specific signal and commitment, and the functional-partnership renewals for contracted partners.
- **The surfaces fire in sequence across the quarter.** Council in Week 4, BU reviews in Week 5, exec review in Week 6, partnership renewals across Weeks 7–11, close-out in Week 12. The sequence is what makes the ritual legible.
- **Information flows across surfaces in a specific pattern.** Field signal up, policy edits down, vendor decisions out to Procurement and Finance, budget asks to the exec review, partnership contracts underpinning all of it.
- **Three failure modes to watch:** the council becoming a status meeting, the exec review degrading into bespoke briefings, and partnership contracts going unsigned. Each has a specific correction in the agenda, the distribution tiering, or the renewal preparation discipline.
