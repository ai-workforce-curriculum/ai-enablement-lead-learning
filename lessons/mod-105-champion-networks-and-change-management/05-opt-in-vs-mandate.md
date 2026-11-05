# Opt-In vs. Mandate

> The single most consequential rollout decision an enablement lead makes is not *which tool*; it is *opt-in or mandate*. The decision determines the shape of the resistance you encounter, the composition of the first-year adopter cohort, the scorecard metrics that matter, and the governance posture you need. This chapter is the decision framework — the trade-offs, the signals that justify each path, the organizational conditions under which one works and the other backfires.

## Why this is a deliberate decision and not a default

In most enterprise programs the decision is made *implicitly* — the exec sponsor announces the tool at an all-hands, calls it "available," and the organization reads either "available and encouraged" or "available and expected" based on existing cultural signal. Both read the room, not the policy.

That is how you get the two most expensive outcomes:

- A rollout that was *meant* to be opt-in but was *read* as a mandate — operators feel coerced, resistance hardens, scorecard numbers look good for two quarters then collapse.
- A rollout that was *meant* to be a mandate but was *read* as opt-in — the compliance population opts out, the audit evidence is thin, adoption plateaus well below the threshold that was supposed to justify the investment.

Both outcomes are prevented by the same discipline: **name the decision explicitly, write it into the rollout artifact set, say it in Slot 4 of the communications cadence.** The rest of the chapter is how to make the right choice.

## The decision framework

Four factors, in roughly decreasing order of weight.

### Factor 1 — Does the tool touch a workflow with external accountability?

External accountability shortens the decision toward *mandate*. Workflows with regulatory obligations, contractual commitments, or safety implications cannot tolerate a 30% opt-out rate.

- A customer-service tool used in regulated-workflow handling (banking, insurance, healthcare). Mandate.
- A legal e-discovery assistant subject to counsel-level attestation. Mandate.
- A general-purpose writing assistant with no regulatory surface. Lean opt-in.
- An internal-ops analytics assistant with no external accountability. Lean opt-in.

The exception is a workflow where the *old* tool continues to work. If the alternative to the new tool is an existing compliant path that still functions, the regulatory argument for mandate weakens — the tool is an upgrade, not a replacement, and an opt-in can be defensible.

### Factor 2 — How material is the operator-level behaviour change?

The larger the behaviour change, the more opt-in pays off.

- *Small behaviour change* (switching from one meeting-summary tool to a newer one): mandate works, the operator adapts quickly.
- *Medium behaviour change* (introducing an AI-assisted drafting workflow into a role that previously did everything manually): mixed — mandate works for operators with existing adjacent habits; opt-in works where fluency varies widely.
- *Large behaviour change* (introducing a new agentic workflow that changes how an operator spends most of their day): opt-in is almost always better. Mandating a large behaviour change creates visible friction, the friction becomes the story, and the rollout's narrative is "something was forced on us" rather than "something changed what we do."

Large behaviour change compounds poorly under mandate: operators who comply but resist produce lower-quality AI output, which feeds the "quality skepticism" resistance pattern ([Chapter 06](06-ai-specific-resistance-patterns-adkar-and-kotter.md)), which produces worse adoption in the next rollout.

### Factor 3 — Is the organizational culture consent-sensitive?

Some organizations run on consent — unionised workforces, academic institutions, European works-council jurisdictions. Others run on direction — regulated industries, operations-heavy businesses, functions where top-down direction is the normal pattern.

- **Consent-sensitive cultures.** Mandating produces outsized resistance; the cost of the mandate is paid in consultation time, union engagement, and legal exposure. Opt-in is cheaper per adopter and builds durable adoption.
- **Direction-sensitive cultures.** Mandating is read as leadership; opt-in reads as absence of leadership. The costs invert.

The mistake is to assume your own organization's culture is universal. An enablement lead moving from a regulated-industry background into a technology company often over-mandates in the first year; one moving from a technology company into a regulated industry often under-mandates. In both cases, the first-year resistance pattern reads as "the operators are difficult" when the actual cause is a misread of culture.

The works-council and union context deserves its own paragraph: in jurisdictions with codetermination rights (Germany's `Mitbestimmungsgesetz`, the EU-wide Information and Consultation Directive 2002/14/EC), the mandate option has a formal consultation requirement before it can be exercised. Your legal partner from [mod-101 Chapter 04](../mod-101-role-and-the-org-wide-enablement-operating-model/04-handoffs-with-adjacent-roles.md) is in the room on this decision; the works council or union is in the room on it. <!-- needs-research: catalog the member-state-level works-council consultation thresholds that apply to workforce AI tool mandates as of 2026, to cite specific instruments in-text. -->

### Factor 4 — What is the floor you can defend to the governance side?

The governance council will ask one question of any new AI tool rollout: what is the literacy floor every in-scope user must clear ([mod-101 Chapter 05](../mod-101-role-and-the-org-wide-enablement-operating-model/05-eu-ai-act-article-4-and-the-literacy-floor.md))? The answer is a floor you can hold against the audit.

- A mandate that cannot evidence the literacy floor is an audit failure in waiting — the deployer has required use without sufficient literacy. The mandate must either defer until the literacy coverage is there, or restrict to an opt-in plus a *separate* mandate for the literacy curriculum.
- An opt-in rollout has more flexibility — the audit question is "did the operators who used it have sufficient literacy for the context," which an opt-in population typically clears more cleanly than a mandated one.

The practical shape: if the literacy coverage lags by more than one quarter, the rollout should not be mandated. The rollout artifact set from [mod-102 Chapter 03](../mod-102-selecting-and-rolling-out-ai-tools/03-the-rollout-artifact-set.md) names the training package as a launch gate; the mandate decision tightens the gate.

## The two decisions — explicit shapes

Once the four factors are weighed, the decision takes one of two explicit shapes.

### Shape A — Opt-in with high visibility

- **Policy language:** "Available to [in-scope population]. Use is encouraged where it supports your workflow. Use is not required."
- **Communications emphasis:** Slot 3 (what is working) runs hot — spotlights, named-use-case stories, visible early-adopter outcomes. Operators are pulled, not pushed.
- **Champion emphasis:** champions are recruiters-of-the-opt-in. Their office hours are the entry point.
- **Scorecard metrics:** adoption curve shape (first 90 days, 180 days, 365 days); self-reported workflow improvement; use-case library growth; incident rate per active user.
- **Governance posture:** literacy floor applies to *active users*, with evidence collected through the SSO / provisioning layer.

Where it works: medium or large behaviour-change rollouts; consent-sensitive cultures; the first time a vendor's tool is being tried organization-wide; cases where the business outcome is not immediately contingent on universal use.

Where it backfires: cases where partial adoption produces a worse outcome than no adoption (a regulated workflow where unassisted operators handle exceptions less safely than assisted ones). Where the adoption curve stalls at 20-30% of the in-scope population and the marginal operator cost of pulling the next 10% exceeds the business value.

### Shape B — Mandate with the floor visible

- **Policy language:** "Required for [in-scope population] from [date]. Literacy prerequisites: [named curriculum completion]."
- **Communications emphasis:** Slot 1 (what is being built) runs ahead of the mandate by at least two cadence cycles — the mandate does not surprise. Slot 2 (what is available) makes the current state and the transition unambiguous. Slot 4 (what to do next) is the specific action required by each affected operator.
- **Champion emphasis:** champions are first-line answers *during* the mandated transition — the office hour load is high in the mandate window.
- **Scorecard metrics:** training completion against the in-scope roster; usage conformance (active use vs. workaround); incident rate; exception requests and their resolution.
- **Governance posture:** literacy floor is universal and evidenced; non-use by an in-scope operator is an exception that must be logged and reviewed.

Where it works: the four factors align — external accountability, small behaviour change, direction-sensitive culture, literacy floor already in place. Cases where partial adoption is worse than no adoption. Cases where the replaced workflow has a sunset date and cannot be sustained.

Where it backfires: large behaviour-change rollouts; consent-sensitive cultures; when the literacy floor is not yet there and the mandate is used to force the literacy curriculum alongside the tool. The stacked mandate — new tool, new training, new policy, all at once — is the single most common cause of a mandated rollout producing worse adoption than an opt-in would have.

## The soft-mandate anti-pattern

A soft mandate is a rollout that is announced as opt-in but enforced as a mandate — the operator who opts out gets a conversation with their manager two weeks later, or their performance metric for the quarter has quietly changed to include use of the tool. The organization reads this quickly; the trust cost is higher than a plain mandate would have been.

A soft mandate is almost always the result of avoiding the decision rather than making it. Typical shape:

- The exec sponsor wants adoption but does not want the political cost of a mandate.
- The enablement lead agrees to run it as opt-in.
- Mid-rollout, adoption is below target; pressure builds; informal enforcement appears.
- Operators see the shift; trust in the enablement function erodes.

The discipline: if a rollout needs mandate-level outcomes, name it as a mandate from the start and pay the cost of the explicit decision. If it genuinely can be opt-in, protect the opt-in — including protecting the operator who opts out from informal consequence.

## The three-tier rollout — a hybrid pattern worth naming

Many real rollouts are neither pure opt-in nor pure mandate. The useful hybrid has three tiers, publicly named:

- **Tier 1 — Required.** A named sub-population of the in-scope roster for whom use is required (e.g., operators in a specific regulated workflow where external accountability holds).
- **Tier 2 — Expected.** A named sub-population for whom use is strongly encouraged with a review cycle (e.g., a function where the business case is strong but the behaviour change is medium).
- **Tier 3 — Available.** The rest of the in-scope population, opt-in with visibility.

The tiering is public; each operator knows which tier they are in; the scorecard metrics differ by tier; the champion-office-hour emphasis matches the tier. The hybrid works because it names the decision explicitly for each sub-population, rather than defaulting to the same policy across a heterogeneous workforce.

The error is to design a three-tier model that is in practice a one-tier mandate — where the "expected" population is tracked and nudged exactly like the "required" population. If the tiers are not operationally distinct, there is only one tier.

## Reversal

Opt-in-to-mandate reversal is one of the most politically expensive operations an enablement lead runs. It is sometimes necessary — a new regulatory obligation, a sunset of a legacy system, an evidence base showing that opt-in has produced worse outcomes than hoped. When it is necessary, treat it as a change on its own, with its own cadence and its own champion network engagement, not as a footnote in an existing rollout's comms.

Mandate-to-opt-in reversal is less expensive and more common — a mandate that was imposed in the first-year rush of enterprise AI adoption, now relaxed as the literacy floor catches up and the tool's role in the workflow is better understood. Reversal in this direction is a signal of program maturity; name it clearly in Slot 3 of the cadence as an improvement, not a retreat.

## A worked example — the three-organization comparison

Carry forward the three organizations from the mod-101 and mod-104 exercises. The decision shape differs materially.

- **3,000-person US bank with existing head of AI governance, no CoE.** Customer-service AI assistant touching regulated workflows. Factor 1 (external accountability): strong, points to mandate. Factor 2 (behaviour change): medium, mixed signal. Factor 3 (culture): direction-sensitive, points to mandate. Factor 4 (literacy floor): in place from the governance partner. **Decision shape:** three-tier rollout — Tier 1 Required (customer-facing regulated-workflow operators), Tier 2 Expected (customer-service team leads and quality reviewers), Tier 3 Available (back-office support staff).
- **12,000-person global pharma with active CAIO and mature governance.** General-purpose research-and-writing assistant across functions. Factor 1: weak, no immediate regulatory accountability for this tool category. Factor 2: medium to large behaviour change across most functions. Factor 3: consent-sensitive in European sites (works-council consultation required). Factor 4: literacy floor is in place from the mature program. **Decision shape:** Shape A (opt-in with high visibility), with explicit consultation completed in each works-council jurisdiction before launch.
- **500-person SaaS company with no governance function and a CAIO-who-is-really-the-CTO.** Coding assistant and sales-ops AI. Factor 1: weak-to-medium. Factor 2: small to medium behaviour change in a workforce already AI-literate. Factor 3: direction-sensitive in the engineering culture, mixed in sales. Factor 4: literacy floor is thin; this is a program building the floor alongside the rollout. **Decision shape:** Shape A for both, with a mandatory literacy module stacked ahead of either tool's rollout — the literacy is mandated, the tools are opt-in. This decouples the literacy mandate from the tool mandate and avoids the stacked-mandate failure.

Exercise 04 walks you through the same framework applied to a case of your own.

## Where this chapter feeds

- [Chapter 04](04-the-rollout-communications-cadence.md) is the surface where the decision is made legible — Slot 1 announces, Slot 4 operationalises.
- [Chapter 06](06-ai-specific-resistance-patterns-adkar-and-kotter.md) treats the resistance patterns that attach specifically to mandates (role-threat, quality-skepticism) and the different patterns that attach to opt-in rollouts (the "I already have ChatGPT at home" pattern).
- [mod-102 Chapter 03](../mod-102-selecting-and-rolling-out-ai-tools/03-the-rollout-artifact-set.md) is where the decision is written into the rollout artifact set's use policy.
- [mod-106](../mod-106-outcome-measurement-and-executive-reporting/README.md) is where the scorecard metrics differ by shape.
- Exercise 04 asks you to work the decision through for a specific case with named factors and a named shape.

## Summary

- The decision is deliberate — name it explicitly, write it into the rollout artifact set, say it in Slot 4 of the cadence. Implicit decisions produce the two most expensive outcomes (read-as-mandate opt-ins and read-as-opt-in mandates).
- Four factors: external accountability, size of behaviour change, consent-sensitivity of culture, defensibility of the literacy floor. Weigh them in that order.
- Two explicit shapes — opt-in with high visibility, mandate with the floor visible — plus one hybrid three-tier pattern. The hybrid is operationally distinct, not cosmetic.
- The soft mandate is an anti-pattern. If the rollout needs mandate-level outcomes, name it as a mandate and pay the cost of the decision explicitly.
- Reversal in both directions is possible; opt-in-to-mandate is expensive and needs its own change cadence, mandate-to-opt-in is a signal of maturity worth naming publicly.
- Three-organization worked example shows the framework producing different shapes for different contexts; Exercise 04 asks you to work a case of your own.
