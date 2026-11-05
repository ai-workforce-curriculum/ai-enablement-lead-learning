# Exercise 04 — Opt-In vs. Mandate Decision Worked Example

**Estimated effort:** 2 hours
**Format:** one artifact of 2–3 pages (decision memo), Markdown or docx
**Grounding chapter:** [05 — Opt-In vs. Mandate](../05-opt-in-vs-mandate.md)

## Objective

Apply the four-factor decision framework to a specific rollout in a specific organization and produce the decision memo that the exec sponsor signs off on before any launch comms are drafted. The memo names the decision explicitly, walks the factor-by-factor reasoning, specifies the rollout shape, and declares the specific signals that would cause the decision to be revisited.

## Prerequisites

- Chapter 05 read.
- A specific rollout and a specific organization. Pick one of the following, or carry forward a rollout from Exercise 03 or from mod-102 Exercise 03:
  - **Case A.** A 3,000-person US bank; the rollout is an AI-assisted branch customer-service tool going to 400 branch service representatives across Tier 1 ticket categories.
  - **Case B.** A 12,000-person global pharma; the rollout is a general-purpose AI writing assistant across R&D, commercial, and corporate functions. European sites include unionised workforces; the works-council consultation is in progress but not complete.
  - **Case C.** A 500-person SaaS company; the rollout is an AI pair-programming assistant for the engineering organization (120 engineers); the sales organisation (80 operators) is separately asking for the same AI sales-ops assistant.
  - **Case D.** Your own real case.

## Problem statement

Your exec sponsor is about to sign off on the launch date. Before they sign, you are briefing them on *the decision shape* — opt-in, mandate, or hybrid three-tier — and the reasoning. The memo is the artifact of record for the decision. If you are wrong, this memo is where the governance partner, the audit team, or the post-incident review will read your reasoning.

## Requirements

Deliver one decision memo with the following sections.

### 1. Rollout framing (3–5 sentences)

What tool, what population, what the alternative-workflow continuity is (does an existing compliant workflow remain), what the GA target date is, what the pilot evidence base shows.

### 2. The four-factor walk (one subsection per factor)

Walk each factor from [Chapter 05](../05-opt-in-vs-mandate.md) in order. For each: name the signal, cite the evidence, declare the factor's directional pull (toward mandate / toward opt-in / weak / mixed), and note any uncertainty.

#### 2a. Factor 1 — External accountability

Regulatory, contractual, or safety implications. Cite the specific regulation or contractual clause if applicable. For regulated industries (banking, pharma, healthcare, insurance), be specific about jurisdiction — the EU AI Act Article 4 reading from [mod-101 Chapter 05](../../mod-101-role-and-the-org-wide-enablement-operating-model/05-eu-ai-act-article-4-and-the-literacy-floor.md) applies if the organization touches the EU; for US-anchored cases, name any federal-agency guidance (e.g., CFPB, FDA, OCC) that touches the workflow. <!-- needs-research: cite the specific CFPB / OCC / FDA guidance documents relevant to the chosen case as of 2026-11. -->

#### 2b. Factor 2 — Behaviour-change magnitude

Small / medium / large. Named with respect to the specific operator day. Reason about *where* in the operator's day the tool sits, what fraction of their work it changes, whether existing habits transfer.

#### 2c. Factor 3 — Consent-sensitivity of culture

Direction-sensitive / consent-sensitive / mixed. Name the specific cultural signals — unionised workforce, works-council jurisdiction, academic governance tradition, codetermination rights, operations-heavy direction-sensitive culture. For European sites, name the specific instrument (works-council consultation under Directive 2002/14/EC, or the applicable member-state statute).

#### 2d. Factor 4 — Defensibility of the literacy floor

Is the Article 4-shape literacy floor in place for the in-scope population as of GA? If not, how far behind is it, and what is the plan? [mod-104 Chapter 03](../../mod-104-training-programs-and-ai-literacy-curriculum/03-the-foundational-ai-literacy-curriculum.md) is the reference for what counts.

### 3. The decision and the explicit shape

One of the three shapes from [Chapter 05](../05-opt-in-vs-mandate.md):

- Shape A — Opt-in with high visibility.
- Shape B — Mandate with the floor visible.
- Three-tier hybrid — explicit Tier 1 Required / Tier 2 Expected / Tier 3 Available.

The shape is declared explicitly, with the policy language for the acceptable-use policy and the Slot 4 language for the communications cadence. Include:

- The exact single sentence that will appear in the AUP.
- The exact single sentence that will appear in Slot 4 of the first cadence send.
- For three-tier: the roster of each tier (by function or named sub-population).

### 4. The reversal triggers

Three to five specific signals that would cause the decision to be revisited. Each signal is measurable or observable. Examples:

- Adoption curve stalling below X% active use by month 3 (reversal to a different shape).
- Resistance survey anxiety scores rising above Y in two consecutive quarters.
- A regulatory change that strengthens or weakens the external-accountability factor.
- Business outcomes falling below the floor that justified the shape.

Reversal triggers are the discipline that prevents a decision from being treated as final when the context changes.

### 5. The audit-posture paragraph

A short paragraph (3–5 sentences) explaining how the decision defends against the audit question in this organization's primary jurisdiction. For EU-touching organizations, name Article 4. For US banking, name the relevant federal guidance. For regulated-industry cases generally, name the regulator and the question the memo answers for them.

### 6. The soft-mandate self-check

A single short paragraph confirming you are not inadvertently authoring a soft mandate. The check: if the shape is opt-in, what specifically protects the operator who opts out from informal performance consequence? If the shape is mandate, is there an exception path that is operationally real, not symbolic?

## Starter guidance

- The hardest factor is usually 2 (behaviour-change magnitude). Pilots give evidence; general-purpose tools often sit at "medium" for operators whose existing habits transfer easily and at "large" for operators whose workflows are being significantly reshaped. The same tool can have different magnitudes for different sub-populations, which is one of the strongest arguments for the three-tier hybrid.
- Case B (pharma, European sites) is the case most likely to require the three-tier hybrid *and* to require explicit consultation before launch. Do not model it as a pure opt-in; the works-council engagement is itself a formal process.
- Case C (SaaS, engineering + sales) often reaches two different decisions for the two populations — opt-in for engineering (consumer-AI-fluent workforce, large behaviour change), opt-in with a separate mandated literacy prerequisite for sales. Documenting that explicitly is better than one blanket decision.
- Be honest about uncertainty. A factor you genuinely don't know is a factor you name as needing more pilot evidence before launch; a factor you claim with confidence that is actually weak will haunt the post-incident review.
- Reversal triggers are what separate this memo from a one-time rationalisation. Writing them well is the exercise.

## Deliverables

- `opt-in-vs-mandate-memo.md`: the six sections above.
- A short **context note** (3–5 sentences) at the bottom declaring the assumptions you made for the chosen case to keep the memo concrete — organization size, the regulatory shape you inferred, the pilot evidence you assumed, any named champion or function leader you referenced.

## Acceptance criteria

- All four factors walked in order with specific evidence or cited uncertainty.
- The decision shape is one of the three explicit shapes, declared cleanly.
- The AUP sentence and the Slot 4 sentence are actual written text, not descriptions.
- At least three reversal triggers, each measurable or observable.
- The audit-posture paragraph names a specific regulation or guidance document.
- The soft-mandate self-check is not elided.

## Stretch goals

- Author the **counter-case** — the memo as it would be written if you had chosen the *opposite* shape. Read it against your actual memo and note where the counter-case is actually stronger than expected. This is the practice move that catches the decision you are rationalising rather than reasoning to.
- Run the memo past a peer who does not know the organization. Ask them to find the weakest factor in your walk. If the weakest factor in their reading is not the one you flagged as uncertain, your self-awareness of the decision's weak points is off.
- Author the **communications-to-operators** addendum — the version of the decision an operator in the function reads. One paragraph, no jargon, no hedging. This is the surface the operator meets; it needs to be readable.

## Why this exercise matters

The opt-in / mandate decision is the single most consequential one in each rollout and the one most frequently made implicitly. Writing a real memo for a real rollout — with factors walked, reversal triggers named, soft-mandate check completed — is the practice that produces the muscle to make the decision explicitly in the actual role. The memo is also the artifact your governance partner, your audit team, and (if an incident occurs) your post-incident reviewer will read; writing it well is what protects the program's credibility over time.
