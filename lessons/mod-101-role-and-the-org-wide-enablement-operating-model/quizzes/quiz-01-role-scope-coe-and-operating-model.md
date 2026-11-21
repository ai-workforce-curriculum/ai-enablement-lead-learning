# Quiz 01 — Role, Scope, CoE Pattern Family, and the Operating Model

**Format:** multiple choice · **Questions:** 11 · **Estimated effort:** 20–25 minutes
**Grounding:** [Chapter 01](../01-the-level-45-role-and-its-scope-contract.md), [Chapter 02](../02-the-ai-coe-pattern-family.md), [Chapter 03](../03-authoring-the-enablement-operating-model.md), [Chapter 04](../04-handoffs-with-adjacent-roles.md), [Chapter 05](../05-eu-ai-act-article-4-and-the-literacy-floor.md), [Chapter 06](../06-credentials-and-the-90-day-entry-plan.md)

## How to take this quiz

Pick the single best answer for each question. Each question tests whether you can *apply* a chapter idea — paraphrasing the chapter is not enough. Answer key with short explanations is at the bottom; resist the urge to read it until you have your own answers written down.

---

### Q1. The hiring manager for a new AI Enablement Lead role describes the job as "run AI adoption for the customer-service org — 220 people across four teams." The scope contract from Chapter 01 says you should:

- **A.** Accept; four teams is roughly the right unit of work for a level-45 role.
- **B.** Refuse outright; a level-45 AI Enablement Lead never works at BU scale.
- **C.** Flag it as "team-manager plus" scope — a single-BU program with a bigger title — and negotiate in the contract whether the role is organization-scope or stays single-BU.
- **D.** Accept, and privately plan to redefine the role to organization scope in the first 90 days.

### Q2. You are at an AI governance council meeting. The head of AI governance is out, and legal counsel is pushing to re-open the acceptable-use policy. Based on the scope contract (Chapter 01) and Chapter 04's handoff map, your correct posture is:

- **A.** Decide on the policy change; you are the enablement lead and this is your meeting now.
- **B.** Capture legal counsel's concerns, mark the item for the head of AI governance's return, and offer to draft a redline for their ratification — the policy is co-authored, not owned by you.
- **C.** Defer the meeting; nothing can proceed until the head of AI governance is present.
- **D.** Agree to legal's changes verbally so the meeting ends; you can renegotiate with governance later.

### Q3. A European holding company owns five substantially autonomous business units (a bank regulated by the ECB/local prudential authority, a general insurer, a life insurer, a wealth-management arm, and a retail-brokerage arm). Each BU has its own CIO, its own product organization, and its own regulator. AI maturity is uneven but moderate. The CEO wants a single AI strategy narrative. Based on Chapter 02, the defensible CoE shape is:

- **A.** Hub — it gives the CEO the single narrative.
- **B.** Hub-and-spoke — one hub sets standards, five spokes execute inside the BUs.
- **C.** Federated — BUs own AI; a thin central layer handles vendor contracts, cross-BU reuse, and policy alignment with legal / security / privacy.
- **D.** Embedded — each BU is already mature enough; no central structure is needed.

### Q4. Chapter 02 describes a classic hub-and-spoke failure mode where the hub overspecifies and the spokes become ticket-takers. The most direct operating-model fix, per Chapter 03, is to:

- **A.** Collapse the shape to pure hub and remove the spokes.
- **B.** Rewrite the decision-rights table so more decisions sit with the spokes and BUs, moving the CoE from "D" to "C" on routine operational calls.
- **C.** Add a central bureaucracy to track spoke activity.
- **D.** Promote every spoke by one level so they have more authority.

### Q5. Chapter 03 says intake has three queues — the long-tail employee intake, the new-use-case pilot pipeline, and the incident fast lane. For the long-tail employee intake, the chapter's design goal is that:

- **A.** Every request becomes a tracked intake ticket so nothing is missed.
- **B.** 80%+ of long-tail traffic resolves at self-serve / office hours / training / champion routing and never becomes an intake ticket.
- **C.** All traffic routes to the champion network first and only reaches the CoE on escalation.
- **D.** The CoE responds to every request within one business hour.

### Q6. On the decision-rights table in Chapter 03, the row for "pull kill switch on a rollout" assigns **Decide** to:

- **A.** The BU leader whose team is using the tool.
- **B.** The head of AI governance.
- **C.** The CoE (the AI Enablement Lead).
- **D.** The security team, since kill switches usually touch access.

### Q7. An executive sponsor proposes: "Let's pure-chargeback the CoE — every BU pays for every service it uses. That way we prove ROI and the CoE defends its own headcount." Based on Chapter 03's funding-model analysis, your most grounded response is:

- **A.** Agree; the demand-side signal is strictly better than central funding.
- **B.** Push back: pure charge-back usually costs more in overhead than it buys in demand signal for the first two years, and the services most important to the organization (policy, training, incident response) are the hardest to bill for — a hybrid model is the common mature-program answer.
- **C.** Agree in principle but propose to charge-back only the training curriculum, because that is the easiest to invoice.
- **D.** Refuse any funding change; central funding is the only defensible model.

### Q8. Chapter 04 names four load-bearing handoffs. "Field signal — use cases that worked, use cases that didn't, the tools their team tried off-envelope" is listed as something that crosses the handoff with:

- **A.** `ai-governance-analyst` (level 15).
- **B.** `ai-risk-engineer` (level 25, peer).
- **C.** `head-of-ai-governance` (level 60).
- **D.** `ai-augmented-team-manager` (level 40) — they hand it up to you.

### Q9. A US-headquartered manufacturer has 400 engineers in Germany using GitHub Copilot and a legal team using a vendor contract-review copilot on contracts that touch EU customers. Under Chapter 05's reading of EU AI Act Article 4, the correct scope conclusion is:

- **A.** Article 4 does not apply because the company is US-headquartered.
- **B.** Article 4 applies because the organization is a deployer of AI systems with EU-touching activity, and the obligation extends to employees *and* to contractors / third-party operators acting on the organization's behalf — scope the audience wider than you'd initially guess.
- **C.** Article 4 applies only to the 400 Germany-based engineers; US employees are out of scope regardless of what they touch.
- **D.** Article 4 is a provider-only obligation and does not apply to deployers.

### Q10. Chapter 05 tests an Article-4 literacy program by asking: "If an auditor from a reasonably sophisticated member-state market-surveillance authority walked in tomorrow, could we defend this as proportionate?" Which of the following would most undermine a positive answer for a 50,000-person bank?

- **A.** A multi-tier curriculum with role-based rationales, annual refresh cadence, and a dated completion roster retrievable by someone other than the AI Enablement Lead.
- **B.** A single 20-minute "what is AI" e-learning module delivered once in 2024, no refresh since, no segmentation, no non-completer policy.
- **C.** A written proportionality rationale that references the tier audience's technical knowledge, experience, education, and context of use.
- **D.** An evidence catalog that names where the content library, completion records, and refresh log live, who maintains them, and who can retrieve them.

### Q11. Chapter 06 lays out the 90-day entry plan in three 30-day phases. Which of the following week-9 activities is **best-aligned** with the chapter's sequencing?

- **A.** Launch the flagship enterprise-copilot rollout across the organization.
- **B.** Sign the scope contract for the first time.
- **C.** Open the intake path to a pilot cohort (one BU, two teams) and run the first weekly triage, expecting messes to iterate on.
- **D.** Hire the Training & Curriculum Lead, the Change & Champion Network Lead, and all embedded enablement partners at once.

---

## Answer key

**Q1 — C.** Chapter 01 names "team manager plus" scope — a single team's or single-BU AI program with a bigger title — as the specific trap to catch in the contract. The level-45 role runs the system that makes any team's adoption possible; it does not run one BU's adoption. (Chapter 01 — *The adjacent roles the contract is written against → `ai-augmented-team-manager`*.)

**Q2 — B.** The scope contract and the Chapter 04 handoff draw the line at co-author vs. owner. You draft and feed evidence; the head of AI governance ratifies. Deciding in their absence blurs the line that regulators and legal partners rely on. (Chapter 01 — *`head-of-ai-governance`* section; Chapter 04 — *Handoff 4*.)

**Q3 — C.** Substantially autonomous BUs under a holding-company structure with distinct regulators is the canonical "federated" fit: BUs own AI work, a thin central layer handles vendor contracts, cross-BU reuse, and policy alignment. Chapter 02 names holding-company structures and multi-brand groups where each business line has its own regulator as the federated shape's home ground. (Chapter 02 — *Shape 3 — Federated*.)

**Q4 — B.** The hub-overspecifies failure is ultimately a decision-rights problem. Chapter 03's remedy framing — "every non-trivial decision becomes a meeting with eight people" when the table isn't written — points to rewriting the table so routine operational decisions sit with the BUs / spokes, not escalating to the CoE. (Chapter 02 — *Shape 2 — Hub-and-spoke*; Chapter 03 — *Decision rights*.)

**Q5 — B.** Chapter 03 states the design goal explicitly: "80%+ of the long-tail traffic resolves at the first four outcomes [self-serve, office hours, training, champion routing] and never becomes an intake ticket. If every request becomes a ticket, you will drown." (Chapter 03 — *Intake path → The employee intake*.)

**Q6 — C.** Chapter 03's starter decision-rights table assigns **D** on "Pull kill switch on a rollout" to the CoE, with BU / Governance / Security on **I**. The scope contract (Chapter 01) also lists kill-switch authority among the unilateral decisions. (Chapter 03 — decision-rights table; Chapter 01 — *The decisions this role makes unilaterally*.)

**Q7 — B.** Chapter 03 names the pure-chargeback trap directly: overhead typically exceeds the demand-signal benefit for the first two years, and the most important services (policy, training, incident response) are the hardest to bill for. Hybrid — central for shared infrastructure, BU-funded for spokes and commissioned builds — is named as the common mature-program structure. (Chapter 03 — *Funding model*.)

**Q8 — D.** The team manager's "what they hand you" list in Chapter 04 leads with field signal — use cases that worked, use cases that didn't, the off-envelope tools their team tried — then champion nominations, team-level metrics, and early warning on incidents. (Chapter 04 — *Handoff 1*.)

**Q9 — B.** Chapter 05 is explicit that a *deployer* is any natural or legal person using an AI system under its authority, and that the obligation runs to staff *and* to "other persons … on their behalf" — contractors, consultants, outsourced providers. The chapter instructs scoping the audience wider than a first reading suggests. (Chapter 05 — *What Article 4 says*.)

**Q10 — B.** A single stale generic module at a 50,000-person bank violates every property Chapter 05 names as making a program defensible: tiered content, proportionate to role / context, current to the toolset, with completion + non-completer records retrievable by an auditor. A / C / D each describe properties that *strengthen* the proportionality defence. (Chapter 05 — *What a defensible literacy program looks like* and *The "best extent" trap*.)

**Q11 — C.** Chapter 06's week 9 reads: "Open the intake path to a pilot cohort (one BU, two teams). Run the first weekly triage. Expect messes in the intake form, the questionnaire, the hand-off to governance — note them and iterate." A is explicitly listed as a 90-day trap; B belongs in week 5; D violates the "hire one role at a time, after you have load to justify it" guidance. (Chapter 06 — *Days 61–90* and *Common first-90-days traps*.)
