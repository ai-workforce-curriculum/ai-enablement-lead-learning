# Inheriting Prototypes and the Honest No-Go

> A billable consultant finished a three-month engagement at the firm and left behind a working prototype — a document-triage agent for the deals team that the deal partners now rely on. The consultant's contract is over. The prototype is running on a free-tier API key charged to someone's personal credit card. Nobody at the organisation knows the prompt structure, the retrieval index was built against a point-in-time snapshot of the shared drive, and there is no eval harness. The deal partners want the enablement lead to "productionise it." This chapter is the discipline for that conversation.

## Where the prototype comes from

Chapter 02 wrote the brief for the net-new commission — the problem lands, the brief is authored, the build begins from zero. The second commissioning surface this role operates on arrives at the opposite end: the build has already happened, the artefact is sitting on someone's desktop, and the question is whether it should graduate to production. Three common provenance patterns:

- **Billable-consultant prototypes.** A consulting firm's engagement included an AI-prototype deliverable. ClearView Healthcare Partners' public job postings cite this pattern explicitly — a client-facing consulting firm whose senior-manager roles name "productionising prototype AI tools" as a stated responsibility of the client-side enablement counterpart. The pattern is common across professional-services verticals (consulting, law, healthcare-advisory, boutique financial services): a consultant builds the demo on the engagement, the demo works, the client wants to keep running it after the engagement ends.
- **Business-user prototypes.** A sufficiently motivated business user — a product analyst, an operations lead, a deal partner — builds a prototype in a low-code agent-builder or a vendor's agent-studio product. The prototype is in regular use by their immediate team. Scaling it beyond the team is the trigger that routes it to enablement.
- **Hackathon or internal-innovation-day prototypes.** The organisation ran a hackathon; something shipped; an executive sponsor now wants to see it in general availability inside a quarter.

The three patterns are different on origin, cost shape, and documentation posture; they are the same on arrival. The prototype exists. The organisation has emotional investment. The enablement lead is asked to make it a real tool.

## The commissioning question the prototype hides

The question the deal partners are asking the enablement lead is "productionise it." The question the enablement lead has to answer is harder: **is this a commission or is this a request to adopt a working tool, and if it is a commission, is it a build-from-prototype or a rebuild-from-brief?**

The prototype's existence biases every stakeholder in the room toward "productionise it as-is." Three reasons:

- **The prototype has already demonstrated value.** Someone built it; someone uses it; the counterfactual of "we don't do this" has already been priced into the deal partners' workflow.
- **The prototype's build cost has been paid.** The engineer-week cost is in the past. Starting over feels like throwing away work.
- **The prototype's maker has institutional standing.** The consultant's firm, the business user, the hackathon team — each has advocates who would prefer the prototype survive.

None of those reasons is a good reason to graduate a prototype that should not graduate. The commissioner's job is to run the prototype through a productionize-worthiness assessment, produce a specific recommendation (productionise / rebuild / no-go), and defend the recommendation against the three advocacy patterns above.

## The productionize-worthiness assessment — five dimensions

The assessment is a one-page scorecard the commissioner authors against the prototype before the commissioning brief is even started. Each dimension produces a score and a one-sentence read; the composite score plus the narrative drives the recommendation.

### Dimension 1 — Problem fit

**Does the prototype solve a problem that passes the Chapter 01 one-paragraph test?**

- The problem is named at the workflow step.
- The commercial envelope has been checked (or can be checked quickly) and no vendor tool satisfies the problem.
- There is a named user cohort the prototype is actually being used by, not just a theoretical population.
- The outcome is measurable on the mod-102/mod-106 framework.

Common fail mode: the prototype was built by a consultant to solve a problem the consultant found interesting, which does not precisely match any problem the organisation actually has at scale. The deal partners who champion it are a persona of one; the broader user cohort either does not exist or does not have the problem the prototype solves.

### Dimension 2 — Data posture

**Does the prototype's data flow pass [mod-103](../mod-103-policy-co-authoring-with-governance/README.md)?**

- The data classes the prototype reads, writes, retains, and emits are known and nameable.
- The data flow respects the data-handling SOP in [mod-103 Chapter 05](../mod-103-policy-co-authoring-with-governance/05-the-data-handling-sop.md).
- Retention windows are known and acceptable under the organisation's policy stack.
- No data exfiltrates to a model provider whose contract does not cover the data class.
- The prototype uses the organisation's SSO, not a personal account or an unmanaged API key.

Common fail mode: the prototype runs on an API key the consultant obtained on their personal account, reads from a point-in-time snapshot of the shared drive that is no longer refreshed, and sends prompts to a model-provider surface the organisation has no DPA with. This is not a prototype that fails policy at the margins; this is a prototype whose entire operating posture has to be rebuilt before anything else is discussed.

### Dimension 3 — Operational fit

**Does the prototype slot into the standing operating surfaces the enablement program runs?**

- Support channel exists or can be created without displacing other rollouts.
- Champion network can be briefed inside the cadence from [mod-105 Chapter 04](../mod-105-champion-networks-and-change-management/04-the-rollout-communications-cadence.md).
- Kill-switch runbook can be authored against the prototype's deployment surface — the authorising role, revocation sequence, and user-visible state from [mod-109 Chapter 02](../mod-109-ai-incident-response-and-enablement-side-rollback/02-the-kill-switch-as-an-operating-artifact.md).
- The prototype has (or can have) a logging surface the incident path can read.
- Documentation exists at the level the mod-102 rollout artefact set demands.

Common fail mode: the prototype runs on infrastructure the IT identity team does not administrate, has no observability, and cannot be killed cleanly. A tool that cannot be killed cleanly cannot be rolled out — [mod-102 Chapter 03](../mod-102-selecting-and-rolling-out-ai-tools/03-the-rollout-artifact-set.md) is unambiguous on this.

### Dimension 4 — Cost shape

**Is the prototype's steady-state cost defensible on the mod-107 cost model?**

- Inference cost at projected rollout volume is known.
- Infrastructure cost (compute, storage, retrieval, observability) is known.
- Maintenance cost is estimable from the prototype's complexity.
- The total cost sits within the Column 4 TCO envelope from the [mod-107 Chapter 03](../mod-107-budget-roi-and-build-vs-buy-at-org-scope/03-the-build-vs-buy-matrix-at-enterprise-scope.md) matrix, or triggers a return to the matrix if it does not.

Common fail mode: the prototype's cost at pilot volume was trivial (a few dollars a week of API calls on a hobbyist tier) and is approximately linear in volume. Scaled to the real user cohort, the cost is three times the comparable commercial tool. The prototype was never Column 4; it was Column 2 or 3 in disguise, and nobody looked.

### Dimension 5 — Maintenance fit

**Is there a maintenance owner who will accept the handoff under [Chapter 02](02-the-commissioning-brief-as-the-load-bearing-artifact.md) Section 7's commitment shape?**

- A named team or engineer has committed to carrying the tool.
- The maintenance owner's team has the skills to maintain the prototype's stack. If the prototype is built on a framework or model-provider surface the organisation's engineering team does not use, maintenance will decay.
- The commitment is dated, scoped (bug fixes, prompt iteration, eval-harness updates, model-version bumps in scope; feature expansion out), and co-signed by the owner's manager.
- The on-call expectation is explicit.

Common fail mode: the consultant's firm offers to maintain the prototype on a monthly retainer. This is not a maintenance commitment inside the enablement program; it is a vendor relationship that belongs back in [mod-107 Chapter 04](../mod-107-budget-roi-and-build-vs-buy-at-org-scope/04-partnering-with-procurement-finance-and-it.md). If the recommendation is to keep the consulting-firm relationship, the prototype is not a commission — it is a vendor contract, and the assessment that follows is the vendor-vetting rubric from [mod-107 Chapter 06](../mod-107-budget-roi-and-build-vs-buy-at-org-scope/06-the-vendor-vetting-rubric.md), not this chapter's productionize-worthiness assessment.

## The recommendation — three outcomes

The five-dimension read produces one of three recommendations. The recommendation is the commissioner's call; the signatures in [Chapter 06](06-signing-surfaces-maintenance-and-handoff-calendar.md) validate it.

### Productionise

**All five dimensions pass; the prototype inherits the brief and the maintenance owner.**

The commissioner authors the Chapter 02 commissioning brief as a *productionisation* brief — the same eight sections, with Section 1 referencing the prototype's demonstrated value and Section 7 naming the maintenance owner who is inheriting the stack. The build budget (Section 5) covers the productionisation delta — documentation authoring, eval-harness construction, integration with IT identity and observability, policy-stack binding — not a greenfield build. The `applied-ai-engineer` receiving the brief inherits the prototype; the brief names the specific documentation and runbook outputs that must exist before acceptance.

Productionise is the rarer outcome than the stakeholder room expects. Most prototypes that reach the enablement lead's desk fail at least one of the five dimensions.

### Rebuild from brief

**Problem fit passes; one or more of dimensions 2–5 fail in a way that is structural rather than incremental.**

The prototype exists as evidence that the problem is real and that a solution shape works; it does not exist as the shape the production tool will take. The commissioner authors a Chapter 02 brief from scratch, treating the prototype as an input to Section 1 and as a reference for Section 3's baseline (the prototype's demonstrated performance becomes the baseline the production tool has to exceed). The `applied-ai-engineer` or `agentic-ai-engineer` building against the brief does not inherit the prototype's stack; they build the production tool on the standing stack the engineering family has committed to maintain.

The rebuild recommendation is often the right call when a prototype passes problem fit and operational fit but fails on cost shape (the prototype's architecture is expensive at scale) or on maintenance fit (the prototype's stack is foreign to the engineering team).

### No-go

**Problem fit fails, or multiple structural dimensions fail in a way that cannot be rebuilt into the standing operating surface.**

The prototype should not graduate. The commissioner writes the no-go memo (below) and delivers it to the stakeholders. The prototype may continue to run as an unofficial tool inside a small cohort — the commissioner cannot and should not forcibly retire a tool the team built for themselves — but it does not enter the enablement program, does not inherit the rollout artefact set, does not appear on the mod-106 scorecard, and does not receive engineering maintenance capacity.

No-go is the recommendation this chapter exists to make possible. Without it, the organisation accumulates a drawer of orphan prototypes dressed as commissioned tools, each with a maintenance tax the engineering family did not budget for, each underperforming on a scorecard it should never have entered.

## The honest no-go memo

A no-go recommendation is not an email ("we've decided not to productionise this"). It is a one-page memo written for the prototype's advocates, the exec sponsor, and `head-of-ai-governance`. The memo has five sections:

1. **What the prototype did.** One paragraph. Credit the maker. Name the problem it solves and the cohort it served. Not a backhanded compliment — a specific, real description of the value the prototype has produced.
2. **What the productionize-worthiness assessment found.** Each of the five dimensions with the one-sentence read. The specific dimension failures that drive the recommendation named explicitly.
3. **Why rebuild-from-brief is not the recommendation either.** The dimensions where rebuild would still fail — often problem fit (the organisation does not have this problem at scale) or cost shape (the problem does not justify the Column 4 TCO envelope). If rebuild were viable, the memo would recommend rebuild, not no-go.
4. **What happens to the prototype.** The team that built it continues to use it if they wish; the enablement program does not maintain it, does not report on it, does not block its use. If the prototype's data posture is a policy violation, the memo routes the violation separately to [mod-103](../mod-103-policy-co-authoring-with-governance/README.md) and [mod-109](../mod-109-ai-incident-response-and-enablement-side-rollback/README.md) rather than wrapping the policy call inside the productionisation decision.
5. **What the next commission in this problem space would look like.** One paragraph. If the problem is real but the prototype is wrong, the memo names the direction the right commission would take — a different Column choice in the mod-107 matrix, a different cohort scope, a different success criterion. This is the exit ramp that keeps the no-go from reading as a dead end to the business sponsor.

The memo is signed by the commissioner. The `ai-engineering-manager` and `head-of-ai-governance` read for program-level posture and co-sign if the recommendation is to be defensible at governance-council altitude. A no-go that collapses into a renegotiation under stakeholder pressure is the Chapter 01 apologist posture arriving one step earlier than Chapter 05 can catch it.

## Three patterns the prototype inheritance surfaces specifically

Three patterns show up repeatedly in the inheritance assessment and deserve explicit naming:

### Pattern 1 — The consultant's prototype as a lead-generation asset

The consulting firm built the prototype partly to demonstrate capability that would support the next engagement. The prototype is designed to showcase the firm's methodology, not to graduate into a production tool the client's engineering team can maintain. The firm's preferred productionisation path — a retainer with them — is the natural next step for the firm, not necessarily for the client.

**Commissioner read:** Dimension 5 (maintenance fit) often fails; the prototype's stack was chosen for the firm's convenience. Dimension 2 (data posture) often fails; the prototype was built against a snapshot of data the firm had access to during the engagement and does not integrate with the live data surface.

**Move:** The recommendation is usually rebuild-from-brief, with the consulting firm invited into the pilot-cohort partnership on the client-side implementation. If the firm's response is to decline unless they also own the build, the brief goes back to a greenfield `applied-ai-engineer` engagement — which is the posture the brief was always supposed to carry.

### Pattern 2 — The business-user prototype as a shadow IT tool

The business user built the prototype inside a low-code agent-builder on an individual-license tier. The team uses it daily. It is unobservable from IT identity's side and has no logging surface the SOC or the ai-risk-engineer can read. The team does not want to lose the tool; IT does not want to adopt the tool in its current form.

**Commissioner read:** Dimensions 2 and 3 usually fail. Problem fit (Dimension 1) often passes, which is why the team adopted the tool in the first place.

**Move:** The recommendation is usually rebuild-from-brief, with the business user invited to serve as the champion for the production version (Dimension 1 pass + organic enthusiasm + concrete workflow knowledge is exactly the champion profile from [mod-105 Chapter 03](../mod-105-champion-networks-and-change-management/03-routing-field-signal-back-to-policy-tooling-and-training.md)). The rebuilt tool uses the standing engineering stack; the business user's prototype can continue to run in the interim but does not enter the enablement program until the rebuild is accepted.

### Pattern 3 — The hackathon prototype as an executive-sponsorship artefact

The CEO saw the demo at the hackathon showcase. The CEO wants it shipped. The hackathon team disbanded a week after the event. No engineering function has carried maintenance in the intervening weeks.

**Commissioner read:** Dimension 5 (maintenance fit) always fails at the start. Dimensions 1 and 3 are often nameable to pass with investment. Dimensions 2 and 4 depend on what the hackathon team built on.

**Move:** The recommendation is usually rebuild-from-brief *if* the problem fit holds; otherwise no-go. The executive sponsorship becomes a benefit (the maintenance owner can be found more easily because the exec sponsor can cut through engineering-roadmap competition) rather than a bypass (the commissioner still runs the Chapter 02 brief, not an expedited back-channel build).

## Summary

- Prototypes arrive from billable consultants, business users, and hackathons; they bias every stakeholder toward "productionise as-is." The commissioner runs the productionize-worthiness assessment instead.
- Five dimensions: problem fit, data posture, operational fit, cost shape, maintenance fit. Each produces a one-sentence read; the composite drives the recommendation.
- Three recommendations: **productionise** (all five dimensions pass; the prototype inherits the brief), **rebuild from brief** (problem fit passes, one or more structural dimensions fail), **no-go** (the prototype should not graduate).
- The honest no-go memo has five sections: what the prototype did, what the assessment found, why rebuild is not viable either, what happens to the prototype, what the next commission in this space would look like.
- Three prototype-inheritance patterns show up repeatedly: the consultant's lead-generation asset, the business-user's shadow-IT tool, the hackathon's executive-sponsorship artefact. Each has a predictable dimension-failure shape and a predictable move.
- No-go is a load-bearing recommendation. Without it, the enablement program accumulates orphan prototypes that drag the scorecard and the engineering family's maintenance capacity.
