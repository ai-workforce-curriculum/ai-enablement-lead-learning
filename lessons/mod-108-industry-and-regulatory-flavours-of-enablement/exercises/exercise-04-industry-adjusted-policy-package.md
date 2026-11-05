# Exercise 04 — Industry-Adjusted Policy Package

**Estimated effort:** 4 hours
**Format:** AUP + SOP + intake-questionnaire delta, Markdown
**Grounding chapters:** the chosen industry chapter among [03](../03-healthcare-flavour-hipaa-and-phi.md) / [04](../04-finance-flavour-sr-11-7-and-finra.md) / [05](../05-legal-engineering-flavour.md) / [06](../06-education-flavour-ferpa-coppa-and-ed-tech.md); [07](../07-enablement-vs-governance-responsibility-split.md); [08](../08-partnering-with-industry-counsel-without-opining.md). Required prior reading: [mod-103 Chapters 04, 05, and 06](../../mod-103-policy-co-authoring-with-governance/README.md) for the industry-neutral baselines.

## Objective

Produce the industry-adjusted version of the mod-103 policy package for one in-scope industry of your choice. The package consists of three artifacts:

1. The **industry-adjusted acceptable-use policy (AUP)** — the seven sections from [mod-103 Chapter 04](../../mod-103-policy-co-authoring-with-governance/04-the-one-page-acceptable-use-policy.md), with industry-specific content.
2. The **industry-adjusted data-handling SOP** — the five sections from [mod-103 Chapter 05](../../mod-103-policy-co-authoring-with-governance/05-the-data-handling-sop.md), with industry-specific content.
3. The **industry-adjusted intake questionnaire delta** — the industry-specific fields that sit on top of the mod-103 Chapter 06 baseline schema.

The three artifacts are not stand-alone documents — they are *deltas and specializations* of the mod-103 baselines. The exercise is to show that you can preserve the shape of the industry-neutral artifact while flavouring the content for a specific regulator, specific data classes, and specific counterpart roles.

## Prerequisites

- The chosen industry chapter (03, 04, 05, or 06) read; Chapters 07 and 08 read.
- mod-103 Chapters 04, 05, and 06 read. If you did Exercises 01, 02, or 03 of mod-103, carry forward your artifacts to the extent they are reusable.
- A chosen organization in the chosen industry. Use the same organization you used in Exercises 02 and 03 of this module if possible.
- The real regulatory texts cited in the industry chapter at reaching distance. For healthcare: HIPAA Privacy / Security / Breach Notification Rules. For finance: SR 11-7, FINRA Rule 3110 and Regulatory Notice 24-09. For legal: ABA Model Rules, ABA Formal Opinion 512. For education: FERPA, COPPA Rule, your organization's two most significant state-law overlays.

## Problem statement

Launch is in eight weeks. Your organization is deploying its first enterprise AI tool in a regulated line of business — the specific tool is for you to choose (a coding assistant, a chat assistant, a document-review tool, an ed-tech-specific product, a legal-engineering-specific product). The industry-neutral AUP, SOP, and intake-questionnaire baselines exist and were co-authored last year; they do not survive contact with the regulated line of business. The head of AI governance and the industry-specific regulatory counterpart (privacy officer, MRM lead, general counsel, chief privacy officer, registrar) have asked for the industry-adjusted versions of the three documents in time for a walking-redline cycle three weeks from now. Legal counsel, CISO, and the industry-specific counterparts are on the signing surface.

You are the drafter, not the owner. Your job is to produce the three documents at the level where the industry-specific counterpart can either sign or redline — not re-draft from scratch. The posture is [mod-103 Chapter 01](../../mod-103-policy-co-authoring-with-governance/01-the-co-author-posture-and-the-redline-log.md) and [Chapter 08](../08-partnering-with-industry-counsel-without-opining.md).

## Requirements

### Part A — Industry-adjusted AUP (2 pages maximum)

Follow the seven-section structure from [mod-103 Chapter 04](../../mod-103-policy-co-authoring-with-governance/04-the-one-page-acceptable-use-policy.md). Each section flavoured for the industry:

1. **Scope and in-scope users** — named with the industry's regulatory roles if relevant (registered representatives, licensed attorneys, clinicians, licensed educators).
2. **Approved uses** — five named, concrete, and regulator-aware. At least one approved use reflects an industry-specific distinction (regulated-decision vs. non-regulated for finance; PHI-touching vs. non-PHI for healthcare; privileged vs. non-privileged for legal; student-data-touching vs. non for education).
3. **Prohibited uses** — five named, concrete, industry-specific. Must include at least one prohibition that would not exist in a generic AUP.
4. **Data classes allowed and forbidden** — named in the industry's regulatory vocabulary (PHI / ePHI / Part 2; NPI / MNPI / FINRA communications; privileged / work product / client confidences; education records / COPPA-covered / learning-analytics).
5. **If-in-doubt default** — one sentence, industry-specific justification.
6. **Escalation path** — named to include the industry-specific counterparts (privacy officer, MRM lead, general counsel, chief privacy officer, registrar).
7. **Review cadence** — including industry-specific triggers (new guidance from the regulator, enforcement actions at peer organizations, new state-law updates).

Each section carries a co-author tag naming: drafter (the enablement lead), redliner (`head-of-ai-governance`), legal signer (counsel of the relevant specialty), industry-specific signer (the industry counterpart). Tags should not be uniform across sections.

### Part B — Industry-adjusted SOP (3 pages maximum)

Follow the five-section structure from [mod-103 Chapter 05](../../mod-103-policy-co-authoring-with-governance/05-the-data-handling-sop.md). Industry-specific content throughout, including:

- The data-class-handling table named in industry vocabulary.
- The ten-minute accident path mapped to the industry's regulatory clock (HIPAA 60-day breach notification; FINRA 4511 recordkeeping-breach; privilege-exposure matter-management notification; FERPA parent-notification). The operator-level first step still fires at the ten-minute mark; the hand-off is industry-specific.
- The industry-specific launch gate — the counterpart who must sign before the tool can be used on the relevant data class.
- Any industry-specific constraints that do not exist in the generic SOP (minimum necessary for healthcare, MNPI handling for finance, matter-level classification for legal, customer-contract alignment for ed-tech, school-official-exception assertion for institutions).

### Part C — Intake-questionnaire delta (1-2 pages)

A delta against the mod-103 Chapter 06 baseline schema. Not a complete questionnaire — the additional fields and the routing rules the industry requires.

Required fields:

- At least five industry-specific fields grounded in the industry chapter (PHI / BAA / CDS / Part 2 for healthcare; model-classification / regulated-decision / regulated-communication / MNPI / PCI for finance; privilege / work-product / court-filing / outside-counsel-sharing / client-disclosure for legal; student-data / COPPA / customer-contract / tier / product-or-internal for education).
- Each field has a hard-stop rule stated — what values force routing to a specific counterpart or block progress.
- A short memo (half page) to `senior-ai-governance-architect` explaining the schema-refinement implications of these additions.

## Starter guidance

- Begin with the mod-103 industry-neutral versions (yours from mod-103 if you have them, or the chapter structures if not). Do not re-invent the shape; the shape is stable across industries.
- The hardest section in the AUP is approved uses. Vague approvals do more harm in a regulated industry than in a generic organization because the regulator reads them literally. Write approvals so concrete that a line manager can read them aloud and the industry counterpart could not dispute what they permit.
- The hardest section in the SOP is the ten-minute accident path. The operator-level step is simple ("stop using the tool, call the escalation line, preserve the evidence"); the hand-off to the regulatory clock is where the industry flavouring matters.
- The intake-questionnaire delta is most useful when the hard-stop rules are explicit — if answer X on field Y forces routing to counterpart Z, write that rule in the field itself.
- Do not render legal opinion. Where a regulatory question is load-bearing (does this use fall under the privilege envelope? is this a model under SR 11-7? is the use consistent with the BAA's defined services?), route it to the counterpart. The AUP or SOP can reference the determination process without making the determination.
- Where an organizational fact is load-bearing and you do not know it (the specific BAA inventory, the current SR 11-7 risk-tier bands, the specific state-law coverage, the organization's privilege theory), mark `<!-- needs-research: ... -->` inline.

## Deliverables

- `industry-adjusted-aup.md` — maximum 2 pages.
- `industry-adjusted-sop.md` — maximum 3 pages.
- `intake-questionnaire-delta.md` — maximum 1.5 pages plus a half-page memo to the architect.
- A short cover note (3-5 sentences) summarizing the two deltas you most expect the industry counterpart to redline and why.

## Acceptance criteria

- All three artifacts stay inside their page limits. If they spill, cut.
- AUP has all seven required sections in order; each section carries a non-uniform co-author tag.
- At least one approved use and one prohibited use in the AUP are industry-specific — would not appear in a generic AUP.
- Data classes in the AUP are named in the industry's regulatory vocabulary, not generic classes.
- SOP's ten-minute accident path maps to the industry's regulatory clock with specific timing.
- Intake delta has at least five industry-specific fields, each with a hard-stop rule stated.
- The architect memo is a half page and names at least two schema-refinement implications of the new fields.
- No section renders a legal opinion. Regulatory determinations are routed, not made.
- `<!-- needs-research: ... -->` is used wherever an organizational fact is missing.

## Stretch goals

- Write a **coupled change-log entry** showing which lines of the industry-neutral baseline were changed, which were added, and which were kept unchanged. This is the artifact the architect uses to assess whether the schema can be generalized or must branch.
- Produce a **cross-industry compare**: for one of your prohibited uses, show the equivalent prohibition in a different industry's flavour. Same operational substance, different regulatory anchor.
- Draft the **three-sentence email** to the industry counterpart that accompanies the delivery of the three artifacts. Frame what you are asking for (redlines on Parts A and B), what is a hard ask versus soft ask, and the decision deadline.

## Why this exercise matters

The industry-adjusted artifact package is the deliverable the role is most often judged on in the first six months of a regulated-industry role. The industry-neutral baseline is table stakes; the industry-adjusted version is the artifact that demonstrates the enablement lead can read the regulator, name the data classes correctly, and co-author with the industry counterpart without drifting into legal opinion. The exercise also produces the policy half of the pair the Exercise 05 industry-adjusted curriculum will teach against.
