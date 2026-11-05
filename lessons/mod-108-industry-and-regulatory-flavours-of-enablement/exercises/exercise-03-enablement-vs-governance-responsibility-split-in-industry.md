# Exercise 03 — Enablement vs. Governance Responsibility Split in Industry

**Estimated effort:** 2 hours
**Format:** RACI-style responsibility table + two drift memos, Markdown
**Grounding chapters:** [07 — Enablement vs. Governance Responsibility Split](../07-enablement-vs-governance-responsibility-split.md); [08 — Partnering with Industry Counsel Without Opining](../08-partnering-with-industry-counsel-without-opining.md); references [mod-101 Chapter 04](../../mod-101-role-and-the-org-wide-enablement-operating-model/04-handoffs-with-adjacent-roles.md) and [mod-103 Chapter 07](../../mod-103-policy-co-authoring-with-governance/07-what-you-route-out-counsel-soc-architect.md).

## Objective

Write the industry-specific version of the enablement-vs-governance responsibility split for one chosen industry at one specific organization. Produce:

1. A **responsibility table** covering twelve named obligations the role meets in that industry, showing who is Responsible, Accountable, Consulted, and Informed on each (RACI), with the full named-role surface for the organization.
2. A **drift memo (enablement absorbs governance)** — one scenario, 1 page, naming a specific obligation the enablement lead is most likely to absorb in this industry, the mechanism by which the absorption happens, and the intervention that prevents it.
3. A **drift memo (governance absorbs enablement)** — one scenario, 1 page, naming a specific obligation the governance lead is most likely to retain past the handoff window, the mechanism, and the intervention.

The exercise builds the discipline that keeps the boundary stable across a full tenure.

## Prerequisites

- Chapters 07 and 08 read; the industry chapter(s) for your chosen industry read.
- A chosen organization. For continuity with the rest of the module, use the same organization you used in Exercise 02; if you did not do Exercise 02, pick one of the organizations in Exercise 01's scope-definition shape.

## Problem statement

Your head of AI governance has asked for a clear writeup of the responsibility split in your industry, as part of the operating-model documentation for the AI governance program. The writeup is intended to prevent two years of accumulating drift — the pattern of this organization's previous attempt, which "worked fine" for the first 90 days and had to be re-done after a serious incident revealed who actually owned what. You have two hours. Produce the three artifacts above at the level a new enablement lead, a new governance analyst, and the CRO can all read.

## Requirements

### Part A — Responsibility table (RACI)

Twelve rows, one per obligation. Pick obligations that are *industry-specific* — generic obligations (meeting a weekly 1:1) are not the point. Examples per industry:

- **Healthcare.** HIPAA workforce training program, breach-notification process, BAA signing with AI vendors, FDA SaMD determination, PHI data-handling SOP, approved-tool envelope for PHI-touching tools, BAA-status review in intake, clinical-informatics partnership on AI in workflow, 42 CFR Part 2 handling, FERPA-adjacent concerns on pediatric care, ONC-certification considerations, HHS OCR engagement cadence.
- **Finance.** SR 11-7 model risk management program, model inventory, model validation, FINRA 3110 supervision, SEC 206(4)-7 compliance, CFPB adverse-action reason-code workflow, fair-lending compliance program, AML program, exam readiness, MNPI handling, adviser marketing review, regulator-engagement cadence.
- **Legal engineering.** Privilege theory, court-standing-order compliance, Rule 1.1 / 1.6 / 3.3 posture, matter-level AI-use classification, outside-counsel AI interoperability, CLE program for attorneys on AI, citation-verification workflow, enterprise AUP legal-side signing, state-bar opinion engagement, client-disclosure process, incident response for privilege-exposure events, risk committee reporting.
- **Education.** FERPA compliance program, customer-contract alignment for ed-tech vendor workforce AI use, COPPA compliance, state student-privacy coverage map, academic-integrity policy on AI-generated student work, special-education compliance, teacher professional-development on AI, product-vs-workforce privacy boundary (vendor), student-use policy (institution), parent-communication posture, FTC engagement cadence (vendor), state-AG engagement cadence.

Columns:

- Obligation (named specifically; e.g., "SR 11-7 model classification determination for a candidate AI tool," not "model risk").
- Responsible — the role that does the work.
- Accountable — the role that answers to leadership / the regulator.
- Consulted — roles whose input is required before the decision.
- Informed — roles that are kept updated but do not gate.
- The specific test from Chapter 07 that establishes the split — signing-surface, regulator-communication, professional-responsibility, or three-lines-of-defense.

Use named roles, not person names. Named roles include the enablement lead; `head-of-ai-governance`; `senior-ai-governance-architect`; the industry-specific counterparts named in the industry chapter (privacy officer, MRM lead, general counsel, chief privacy officer, registrar, etc.); the CRO; CCO; CISO; Procurement lead.

### Part B — Drift memo (enablement absorbs governance)

One page.

1. **The obligation that gets absorbed.** Pick one specific obligation from the responsibility table. The best choices are the obligations where the governance-side counterpart is new, under-staffed, or recently formed.
2. **The mechanism of absorption.** How does the absorption happen? Specific sequence — "the privacy officer is new and overwhelmed; the enablement lead has training infrastructure; HR asks for HIPAA training support; the enablement lead agrees; the HIPAA training program begins drifting under the enablement lead's team; the privacy officer loses visibility; a routine audit surfaces evidence gaps."
3. **The intervention.** The specific move that prevents or reverses the absorption. Not "communicate better"; a specific escalation path, a specific scorecard signal, a specific agreement that gets signed.

### Part C — Drift memo (governance absorbs enablement)

One page.

1. **The obligation that gets retained past the handoff window.** Pick one specific obligation.
2. **The mechanism of retention.** Often: a risk-averse governance function that "holds for the first 90 days until enablement is up to speed" and does not hand off on schedule.
3. **The intervention.** The specific move — a calendar-based handoff cadence, a scorecard signal on handoff status, a leadership-level commitment to the enablement role's scope.

## Starter guidance

- The twelve obligations should be concrete. "Model risk management" is too broad; "SR 11-7 model classification determination for candidate tools" is right. "Privacy program" is too broad; "the BAA-status field in the intake questionnaire and its routing to procurement and privacy" is right.
- Responsibility and Accountability are different. Responsible = does the work. Accountable = ultimately answers for it, including answering to the regulator. On regulated obligations, the Accountable role is usually *not* the enablement lead.
- The signing-surface test from Chapter 07 is the single easiest discriminator. When you are not sure, ask "who signs the artifact at the end of this process?"
- The drift memos should be realistic for the organization you chose — not drawn from a different industry's example. The mechanism is the specific social and organizational sequence by which the absorption happens in *this* context.
- The intervention in each drift memo must be *specific*. "Have a conversation with governance" is not an intervention; "surface the MRM-queue latency as a scorecard signal escalated monthly to the CRO" is.
- Where organizational facts are load-bearing and you don't know them (which roles report to whom, how the governance council is structured, whether a formal three-lines structure exists), mark `<!-- needs-research: ... -->`. Do not invent.

## Deliverables

- `industry-responsibility-table.md` — the twelve-row RACI table.
- `drift-memo-enablement-absorbs-governance.md`
- `drift-memo-governance-absorbs-enablement.md`
- A short cover note (3-5 sentences) summarizing the row in the table you are most likely to drift on personally and why.

## Acceptance criteria

- The table has at least twelve rows, each a specific industry-grounded obligation.
- Each row has all five columns (R, A, C, I, test) filled.
- Each R, A, C, I is a named role (not a person name).
- At least nine of the twelve rows show the Accountable role is *not* the enablement lead — the exercise is a boundary-check and should surface this ratio.
- Each drift memo names a specific obligation, a specific mechanism, and a specific intervention.
- Neither drift memo relies on "communicate better" or similar abstractions as the intervention.
- `<!-- needs-research: ... -->` used where organizational structure is uncertain.

## Stretch goals

- Add a thirteenth row that is *the obligation your organization has most recently had a drift incident on* — real or hypothetical based on peer-organization incidents. The row's intervention names what would have prevented the incident.
- Write the **three-sentence version** of the responsibility split that you would say to an operator who asks "wait, is this a governance thing or an enablement thing?" The three-sentence version has to work for someone who does not know what RACI stands for.
- Write a **90-day-boundary-audit** checklist — five questions you could ask yourself at the 90-day mark to detect whether a drift is already happening. Each question has to be answerable by looking at a specific artifact or calendar.

## Why this exercise matters

Regulated-industry enablement roles that drift into governance work are the most common failure mode in the sample — and the hardest to recover from, because the drift happens slowly and is invisible until an incident surfaces the accumulated exposure. Writing the responsibility split in advance, in RACI form, with the drift memos as adversarial self-review, is the discipline that keeps the two-year tenure in scope. It is also the artifact leadership can read when the pressure to absorb lands; a signed responsibility table is the thing that lets the enablement lead say "I will route this per our table" without re-litigating the boundary every time.
