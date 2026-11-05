# EU AI Act Article 4 and the Literacy Floor

> Most of the training curriculum you will design (covered in [mod-104](../mod-104-training-programs-and-ai-literacy-curriculum/README.md)) is about *outcome* — getting people fluent enough to do real work with AI. One slice of it is also about *regulatory floor* — the minimum AI literacy a deployer must ensure under the EU AI Act. If any part of your organization touches the EU market, this chapter is load-bearing.

## What Article 4 says

Article 4 of Regulation (EU) 2024/1689 — the EU AI Act — is titled "AI literacy." The operative text (own words, read the regulation itself):

> Providers and deployers of AI systems shall take measures to ensure, to their best extent, a sufficient level of AI literacy of their staff and other persons dealing with the operation and use of AI systems on their behalf, taking into account their technical knowledge, experience, education and training and the context the AI systems are to be used in, and considering the persons or groups of persons on whom the AI systems are to be used.

A few things to notice carefully:

1. **"Providers and deployers."** A *deployer* is any natural or legal person using an AI system under its authority (except in a personal non-professional activity). Almost every organization using commercial AI tools — Copilot, ChatGPT Enterprise, Claude for Work, vendor copilots — is a deployer. Deployer obligations apply even if you did not build the system.
2. **"Staff and other persons … on their behalf."** This includes employees *and* contractors, consultants, and outsourced providers who operate AI systems on the organization's behalf. You scope the audience wider than you'd guess.
3. **"To their best extent."** Article 4 is an obligation of effort proportionate to context, not a hard numerical bar. The size of your organization, the sensitivity of the system, and the vulnerability of the people on whom the system is used all shape "sufficient."
4. **"Technical knowledge, experience, education and training and the context."** The literacy must be *appropriate* — leadership-level literacy and operator-level literacy are different things.

Article 4 has been in application since **2 February 2025**. Enforcement is in the hands of the EU member state market-surveillance authorities and (for prohibited practices and a few other categories) the European AI Office. Penalties for Article 4 breaches themselves are not the headline — the headline is that an organization unable to demonstrate Article 4 compliance has a credibility problem on every *other* AI Act obligation it faces.

<!-- needs-research: confirm member-state-level enforcement guidance published since 2025-02-02 and any EU AI Office literacy guidelines that have landed by 2026-11; update citations in resources.md. -->

## Why this is the enablement lead's problem

Governance owns the regulatory claim. Legal counsel owns the regulatory position. You own the *operational substance* that makes the claim defensible. Specifically:

- **The curriculum.** Someone has to actually teach literacy content. That is the training program from [mod-104](../mod-104-training-programs-and-ai-literacy-curriculum/README.md).
- **The audience segmentation.** "Sufficient" is role-dependent. The literacy content a senior developer needs is different from the literacy content a customer-service representative needs, which is different from what a board member needs. You segment.
- **The evidence.** Completion rosters, assessment results, refreshed-every-year records — all have to exist, be accurate, and survive an audit. You build them.
- **The scope decision.** Who is in scope and who is out? Contractors? US-based employees whose AI output reaches an EU customer? The right answer is often "err wider" — but *you* have to make the scoping call with legal and governance as counsel.

## What a defensible literacy program looks like

An Article 4-ready program has four properties. Each one maps onto a design decision you make deliberately.

### 1 — Audience-segmented content tied to roles

Three audience tiers are a reasonable starting shape. Your organization may need more.

- **Leadership tier.** For executives and senior managers whose AI decisions set direction. Content: what the technology is and isn't, what the organization's AI posture is, what the organization's obligations are, how to read the executive scorecard, what the escalation path looks like.
- **Operator tier.** For employees using AI tools in the course of their work. Content: the tools in your approved envelope, the acceptable-use policy, the data-handling SOP, the prompt-coaching basics for their role, the signals that mean "stop and escalate."
- **Specialist tier.** For people whose job is to build, configure, red-team, or administer AI tools. Content: deeper technical and risk material. Often overlaps with [`ai-risk-engineer`](https://github.com/ai-governance-curriculum/ai-risk-engineer-learning) and the AI Engineering family's content and defers out appropriately.

Each tier gets a defensible rationale for *why the content is sufficient for that audience and context*. That rationale is the thing an auditor reads.

### 2 — A completion and freshness record

Every person in scope has, for each tier they belong to, a dated record: *took the training on YYYY-MM-DD, passed assessment at NN%*. A record that is older than your organization's refresh cadence (annual is typical; you choose) is a failed record. The refresh cadence is itself a policy decision — write it down.

### 3 — Material that is proportionate and current

"Proportionate" is the regulatory word for *not laughable*. A 20-minute e-learning module on "what is AI" does not clear Article 4 for an operator using generative AI in healthcare triage. Material must be updated as the organization's tools and risk posture change — material frozen in 2024 for a tool bought in 2026 is not current.

### 4 — Evidence that an auditor can read without your help

An auditor will ask: *Show me the content. Show me who completed it. Show me what you did about people who didn't. Show me how you updated it when the toolset changed.* All four should be retrievable in an afternoon by someone who is not you. If any of the four requires you to explain, it is not evidence yet.

## The "best extent" trap

Article 4 does not define a threshold; this is a feature, not a bug — it adapts to context. But "best extent" is *not* license to under-do. In practice, if your organization uses AI at scale and you cannot demonstrate a serious literacy program, you have under-done it. A lightweight program at a 50-person law firm is reasonable. The same program at a 50,000-person bank is not.

The test to apply internally: *if an auditor from a reasonably sophisticated member-state market-surveillance authority walked in tomorrow, could we defend this as proportionate?* If the honest answer is "probably not," you need more.

## Where Article 4 ends and the rest of the AI Act begins

Article 4 is a *floor*. Several other AI Act obligations stack on top and are **not** the enablement lead's primary responsibility:

- Prohibited practices (Article 5) — do not deploy them. Legal and governance own the ban list.
- High-risk system obligations (Chapter III) — risk management, data governance, technical documentation, record-keeping, human oversight, accuracy / robustness / cybersecurity. `senior-ai-governance-architect` and `head-of-ai-governance` own the control library and program.
- GPAI model obligations (Chapter V) — model providers, not deployers.
- Transparency obligations (Article 50) — some deployer responsibilities (e.g., informing people they are interacting with an AI system in certain contexts). You co-author the operator training that makes this real on the ground.
- Serious incident reporting (Article 73) — for high-risk systems. [mod-109](../mod-109-ai-incident-response-and-enablement-side-rollback/README.md) covers how you support without authoring.

Know the difference. On Article 4, you lead. On the rest, you support.

## For organizations that do not touch the EU market

If none of your organization, employees, contractors, customers, data subjects, or output recipients touches the EU, Article 4 does not directly apply. Read it anyway. Two reasons:

- It is the first serious, enforceable AI-literacy obligation in a major jurisdiction. Other regulators are watching. Jurisdiction creep is likely (UK, Canada, several US states, Brazil, Japan have signaled interest in related obligations; details vary and move quickly). <!-- needs-research: refresh the non-EU jurisdictional landscape in the next content cycle. -->
- The *structure* of a defensible literacy program (tiered, role-based, evidenced, current) is good design even where it is not legally required. The Article 4 shape doubles as the floor-and-skeleton of [mod-104](../mod-104-training-programs-and-ai-literacy-curriculum/README.md)'s curriculum.

## Summary

- EU AI Act Article 4 obliges deployers (almost every organization using AI tools) to ensure sufficient AI literacy among staff and persons acting on their behalf.
- "Sufficient" is proportionate to role, context, and the people on whom the system is used.
- The enablement lead owns the operational substance — audience segmentation, curriculum, evidence, refresh cadence — that makes the claim defensible.
- Treat Article 4 as the floor of your training program, not the ceiling. Everything else in [mod-104](../mod-104-training-programs-and-ai-literacy-curriculum/README.md) builds on top.
- Even outside the EU, use the Article 4 shape as the skeleton — it will travel to the next jurisdiction's obligations with minor rework.
