# Exercise 04 — Procurement and Finance Partnership Contract

**Estimated effort:** 2 hours
**Format:** written operating contract (Markdown)
**Grounding chapters:** [04 — Partnering with Procurement, Finance, and IT](../04-partnering-with-procurement-finance-and-it.md), [mod-106 Chapter 05](../../mod-106-outcome-measurement-and-executive-reporting/05-partnering-with-finance-on-cost-model-and-roi.md)

## Objective

Draft the standing three-way operating contract across Procurement, Finance, and IT that [Chapter 04](../04-partnering-with-procurement-finance-and-it.md) describes. The contract specifies — in a form the three partners can co-sign — the interfaces, the cadence, the artifacts, the ownership split, and the explicit out-of-scope lines. The output is the operating document that keeps the three-way partnership running without becoming either a bottleneck or a shadow governance program.

## Prerequisites

- [Chapter 04](../04-partnering-with-procurement-finance-and-it.md) read; the six contract-term surfaces, the four Procurement interfaces, the three cost-recovery models, the IT licensing and SSO/SCIM structure, and the out-of-scope lines close enough to cite without the chapter open.
- [mod-106 Chapter 05](../../mod-106-outcome-measurement-and-executive-reporting/05-partnering-with-finance-on-cost-model-and-roi.md) read; the running Finance partnership is extended, not replaced.
- Optional — the chosen organization from Exercises 01-03. The contract can be organization-specific (naming real partners and real cadences) or role-generic (template form); choose at the start and state which.

## Problem statement

Your organization has grown the AI enablement program to the point where ad-hoc partnership with Procurement, Finance, and IT is no longer serviceable. In the last quarter, a vendor contract renewed with the standard 12% uplift because Procurement did not have a 90-day lead; a build-vs-buy case stalled for six weeks because Finance was pulled in only after Procurement had committed to a negotiation posture; a rollout slipped by a quarter because IT discovered the SSO integration surface two weeks before planned launch. The executive sponsor has asked you to produce a standing operating contract with Procurement, Finance, and IT that prevents these from recurring.

You have two hours (this exercise) to draft the contract before taking it into the first joint working session with the three partners.

## Requirements

### Part A — the contract document

A single Markdown document, roughly 1,000-1,500 words, structured as follows.

**Section 1 — Purpose and scope.** Three to five sentences on why the contract exists and what it covers. Name the four surfaces explicitly: new vendor contracts, running vendor management, annual budget cycle, and in-flight rollout integration.

**Section 2 — Ownership split.** Three tables, one per partner, each listing what the partner owns, what enablement owns, and what is co-owned. Use the splits from [Chapter 04](../04-partnering-with-procurement-finance-and-it.md) as the baseline; adapt to the organization's specifics where needed.

- Procurement: contract text, redline cycle, counter-party relationship, signature, paper trail. Enablement: use case, cohort, data posture, integration surface, acceptable-use language. Co-owned: negotiation brief, redline priorities on use-case-touching clauses, renewal case, vendor review rhythm.
- Finance: time-to-currency conversion, fully-loaded FTE multiplier, vendor-invoice recognition, uncertainty-reporting band, sign-off on the ROI line. Enablement: outcome measurement, attribution logic, denominator scope, ROI narrative. Co-owned: attribution fraction, confidence band, sensitivity analysis.
- IT: SSO/SCIM/identity-store architecture, licensing provisioning, admin-surface integration standards, operational load. Enablement: cohort shape, policy requirements, use-case technical requirements. Co-owned: IT-readiness check, seat-lifecycle discipline, admin-surface review cadence.

**Section 3 — The running cadence.** A compressed table of weekly / monthly / quarterly / semi-annual / annual surfaces per partner, with the artifact produced at each:

```
                        | Weekly | Monthly | Quarterly | Semi-annual | Annual
------------------------+--------+---------+-----------+-------------+--------
Procurement             | ad-hoc |         |     ✓     |             |   ✓   
Finance                 |        |    ✓    |     ✓     |      ✓      |   ✓   
IT                      |        |    ✓    |     ✓     |             |   ✓   
```

For each filled cell, name the interface and the artifact (e.g., "Procurement quarterly: vendor-portfolio review; artifact: vendor-health one-pager").

**Section 4 — The four Procurement interfaces.** Detailed description of:

1. Pre-negotiation briefing (trigger, attendees, duration, enablement input, Procurement input, output artifact).
2. Redline review as called (trigger conditions — which clauses escalate to enablement, response-time SLA, output).
3. Standing quarterly vendor review (attendees, agenda, artifact).
4. Renewal-plus-90 review (trigger, attendees, agenda, artifact).

**Section 5 — The five Finance interfaces.** Extending [mod-106 Chapter 05](../../mod-106-outcome-measurement-and-executive-reporting/05-partnering-with-finance-on-cost-model-and-roi.md):

1. Annual budget cycle (duration, joint artifacts, decision points).
2. Standing quarterly ROI review (unchanged from mod-106 Chapter 05).
3. Monthly invoice reconciliation (extended to six-family taxonomy).
4. Ad-hoc for contracts and build-vs-buy (trigger, review shape).
5. Semi-annual FTE-attribution working group.

**Section 6 — The three IT interfaces.**

1. Pre-rollout integration review (trigger, attendees, artifact — the IT-readiness check).
2. Standing monthly licensing reconciliation (artifact, composition with Finance's monthly cycle).
3. Quarterly admin review (artifact, composition with [mod-103](../../mod-103-policy-co-authoring-with-governance/README.md)'s governance cycle).

**Section 7 — Out-of-scope.** Explicit statement of what the enablement lead does *not* do:

1. Contract execution (redlines, negotiation, signature).
2. Final budget authority.
3. IT operational decisions (SSO architecture, DLP policy configuration, admin-surface integration standards).

The out-of-scope section is three sentences but is load-bearing; carrying it explicitly is what keeps the partnerships functional.

**Section 8 — Escalation and dispute resolution.** Where the three-way partnership disagrees, how disagreement is resolved. Typically: the executive sponsor or their delegate is the escalation point; the sponsor's decision is logged and the contract is amended if the decision implies a standing change.

**Section 9 — Amendment protocol.** How the contract is updated. Typically: annual refresh at the budget cycle; mid-year amendments require the sponsor's sign-off; the amendment log is kept with the contract.

### Part B — the cost-recovery model statement

A short section (3-5 sentences) stating which of the three cost-recovery models from [Chapter 04](../04-partnering-with-procurement-finance-and-it.md) the organization uses (central funding, chargeback by usage, shared-services allocation), with rationale. If the recovery model is not yet settled, state which model is proposed and what the Finance partner's position is. This is often the most politically sensitive part of the contract; writing it explicitly forces the conversation.

### Part C — the open-items log

A short list of two or three items that cannot be resolved in the contract draft and will be surfaced for resolution in the first joint working session. Candidates:

- The fully-loaded FTE multiplier (if the organization's number is not yet confirmed).
- The materiality threshold for the cost model.
- The specific SLA on Procurement redline response time.
- The specific sign-off chain for attestations.
- The cost-recovery model (if open).

Each item is one sentence stating the issue and one sentence stating the proposed resolution path.

## Starter guidance

- The contract is co-authored, not unilaterally drafted. The exercise produces the enablement lead's first draft; the three partners will revise it in the joint working session. Write it in a form that invites revision — not in a form that locks in enablement's preferred positions.
- The ownership split is the single most-contested section. Partners will push to expand their columns or narrow enablement's. The draft should state the baseline split from [Chapter 04](../04-partnering-with-procurement-finance-and-it.md) clearly; the working session is where the baseline is adapted to the organization.
- The out-of-scope section (Section 7) is what makes the contract usable. A contract that promises everything commits enablement to work it cannot deliver. Partners *want* to see the out-of-scope lines; the explicit boundaries are what makes the role a credible counterparty.
- The cadence table (Section 3) is a meeting calendar. Do not populate cells with surfaces the role will not actually run; empty cells are honest. A weekly Procurement check-in cell that is never filled is a broken contract within one quarter.
- The amendment protocol (Section 9) prevents the contract from calcifying. Annual refresh is the standard; mid-year amendments should be rare but possible. Without the protocol, the contract either becomes stale or becomes impossible to update.
- If the organization has an existing partnership document with any of the three partners, reference it rather than replace it. The enablement partnership contract composes with existing supplier-management and procurement documents, not over them.
- Keep the language operating-contract, not legal-contract. This is a working document between partners; it is not a legal agreement. Clear, specific, short.

## Deliverables

- `three-way-partnership-contract.md` containing Parts A, B, and C.

## Acceptance criteria

- Section 1 names the four surfaces the contract covers.
- Section 2 contains three ownership tables (one per partner), each with the three columns (partner owns, enablement owns, co-owned).
- Section 3 cadence table is populated with specific interfaces and artifacts (not placeholders).
- Section 4 describes all four Procurement interfaces with trigger, attendees, duration, enablement input, Procurement input, and artifact for each.
- Section 5 describes all five Finance interfaces, extending (not replacing) [mod-106 Chapter 05](../../mod-106-outcome-measurement-and-executive-reporting/05-partnering-with-finance-on-cost-model-and-roi.md).
- Section 6 describes all three IT interfaces with triggers and artifacts.
- Section 7 states explicitly the three out-of-scope lines; no softening language ("usually," "mostly").
- Section 8 names an escalation point and a logging protocol.
- Section 9 states an amendment protocol with refresh cadence.
- Part B states the cost-recovery model with rationale.
- Part C lists two or three open items with proposed resolution paths.
- The document reads as a working contract; a partner receiving it could reasonably mark it up and return revisions within one working session.

## Stretch goals

- Produce the one-page executive-sponsor briefing on the contract. The sponsor will not co-sign the contract directly, but the sponsor's awareness of the contract's existence and shape is what makes escalations work. The briefing is the BLUF of the contract plus the two or three items most likely to require sponsor arbitration in the first year.
- Draft the first joint working session agenda. 90 minutes, three partners plus enablement, going section by section through the contract. The agenda produces the working session's output artifact: the signed contract.
- Extend the contract to a fourth partner — the Security/Privacy partner from [mod-103](../../mod-103-policy-co-authoring-with-governance/README.md). Security is adjacent to all three partners in this contract (contract DPA review is Procurement-plus-Security; data-residency compliance is Finance-plus-Security; DLP integration is IT-plus-Security). Add a Section 6b for Security's interfaces and update the cadence table.

## Why this exercise matters

The three-way partnership is often inherited rather than designed. Enablement leads who do not write the partnership contract explicitly find themselves re-negotiating the ownership split in the middle of a vendor renewal, a budget review, or a rollout launch — at the worst possible moments. The contract itself is small; the operating benefit of having one is large. This exercise is the first draft of the artifact that converts the role from ad-hoc coordinator to running counterparty.
