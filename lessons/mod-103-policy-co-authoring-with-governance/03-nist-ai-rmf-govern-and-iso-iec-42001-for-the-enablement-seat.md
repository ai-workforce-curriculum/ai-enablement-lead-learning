# NIST AI RMF GOVERN and ISO/IEC 42001 for the Enablement Seat

> Reading is speaking fluently. Reading is not architecting. This chapter is the vocabulary an enablement lead needs to co-author policy with governance partners who live in these documents — and the line, drawn clearly, where the architect's work begins.

## Why read these two at all

Your governance partners — `head-of-ai-governance` (L60), `senior-ai-governance-architect` (L50), `ai-governance-analyst` (L15), counsel, CISO, DPO — speak the vocabulary of two documents more than any others: the **NIST AI Risk Management Framework 1.0** (and its companion Generative AI Profile, NIST AI 600-1) and **ISO/IEC 42001:2023** (the AI management-system standard). If you cannot speak either, the co-authoring conversation runs at the wrong altitude — partners end up explaining concepts instead of negotiating clauses, and the walking-redline cadence from [Chapter 01](01-the-co-author-posture-and-the-redline-log.md) stalls.

Reading does **not** mean architecting. The control-library design on top of these standards is `senior-ai-governance-architect` work; the program leadership is `head-of-ai-governance` work. The enablement seat reads to be fluent — so the right things get said in the right vocabulary in the right rooms, and so the artifacts this module produces can be mapped cleanly to the standard categories the partners track their evidence against.

## NIST AI Risk Management Framework 1.0

### The four functions

The RMF is organized into four functions:

- **GOVERN** — the policies, processes, procedures, and practices across the organization for AI risk management. Roles and responsibilities. Accountability structures. Workforce competence. Policies for third-party AI. Transparency and documentation.
- **MAP** — contextual understanding of the AI system. The categorization of AI systems, intended use, impacts, risks to individuals and groups.
- **MEASURE** — the quantitative and qualitative assessment of mapped risks. Test, evaluation, verification, and validation (TEVV).
- **MANAGE** — the risk-response activities that follow from measurement. Prioritization, mitigation, documentation, communication.

The RMF deliberately presents these as *functions* that interlock continuously, not sequential phases.

### Why GOVERN is the function enablement leads camp in

GOVERN is where policy, workforce, and organizational practice live. Every artifact this module produces — acceptable-use policy, data-handling SOP, intake questionnaire, redline log, training rosters — maps to a GOVERN category. The other three functions touch enablement-side work but are owned elsewhere:

- MAP touches you through the intake questionnaire (which is the organization's primary mapping artifact for new tools), but the schema of MAP evidence is architect-owned.
- MEASURE is `ai-risk-engineer` (L25) and (for outcome measurement at rollout scope) your own [mod-106](../mod-106-outcome-measurement-and-executive-reporting/README.md) work, but the TEVV discipline itself is not enablement-led.
- MANAGE is governance program leadership — `head-of-ai-governance` — supported by the enablement side's rollout and incident-response work ([mod-109](../mod-109-ai-incident-response-and-enablement-side-rollback/README.md)).

Camping in GOVERN is the right altitude for this role.

### GOVERN categories at an orientation level

The GOVERN function is organized into categories covering (at the level an enablement lead should speak to without claiming architect depth):

- Roles, responsibilities, and lines of accountability for AI risk management.
- Organizational policies, processes, and procedures for AI risk, including risk tolerances and mitigation prioritization.
- Workforce competence — training, qualifications, and ongoing literacy for people who design, develop, deploy, operate, or use AI systems.
- Third-party AI risks — including vendors, external providers, and supply chain considerations.
- Processes for information integrity, accountability, and transparency.
- Diversity, equity, inclusion, and accessibility considerations in the AI lifecycle.

<!-- needs-research: confirm exact GOVERN category numbering and sub-category IDs (GOVERN 1.1 through GOVERN 6.N) against the published AI RMF 1.0 text; include the sub-categories most relevant to acceptable-use policy, training, and third-party risk when citing. -->

Note that the workforce-competence category is where this role's training-rosters artifact and the [mod-101 Chapter 05](../mod-101-role-and-the-org-wide-enablement-operating-model/05-eu-ai-act-article-4-and-the-literacy-floor.md) EU AI Act Article 4 literacy work directly connect. If an auditor asks the organization to evidence GOVERN workforce-competence outcomes, the artifacts the enablement side produces are much of the answer.

### The Generative AI Profile — NIST AI 600-1

When the tool in question is generative — which is most tools this role handles in practice — the Generative AI Profile is the companion you read. It is not a separate framework; it is a layer that specifies how the RMF functions apply when the system is generative. It names GenAI-specific risks (confabulation, harmful bias amplification at generation, information security exposures, environmental impact, among others) and recommends how GOVERN / MAP / MEASURE / MANAGE adapt.

Your co-authors will quote the Profile when they draft the GenAI-specific clauses of policies. Being able to recognize the Profile's framing is enough; you do not need to author against it.

## ISO/IEC 42001:2023

### What the standard is

ISO/IEC 42001:2023 is the international management-system standard for artificial intelligence. Published in 2023. Organizations can be certified against it by an accredited certification body — in the same way they can be certified against ISO/IEC 27001 for information security management or ISO 9001 for quality management. The clause structure deliberately parallels 27001 and 9001, which is good news if your organization is already certified in either: the auditors, the internal management-system cadence, and the clause-numbering convention will be familiar.

### The clauses this role touches

The standard runs through ten main clauses. The ones that intersect the enablement seat are:

- **Clause 4 — Context of the organization.** Who the organization is, what AI systems it uses, which stakeholders it has. You contribute the operator-facing context — cohorts, task mix, business units touched.
- **Clause 5 — Leadership.** Top-management responsibility. Policy (including the overall AI policy from which the acceptable-use policy descends). Roles, responsibilities, authorities. This is the clause the acceptable-use policy ([Chapter 04](04-the-one-page-acceptable-use-policy.md)) maps most directly into — the AUP is one of the leadership-policy outputs.
- **Clause 6 — Planning.** Actions to address risks and opportunities. AI objectives. The risk-classification scheme that the intake questionnaire feeds into ([Chapter 06](06-the-intake-questionnaire.md)) is the operating-model input to this clause.
- **Clause 7 — Support.** Resources (7.1), competence (7.2), awareness (7.3), communication (7.4), documented information (7.5). **7.2 and 7.3 are the enablement lead's primary audit evidence surfaces.** Training rosters evidence 7.2. Communications sent through the champion network evidence 7.3. Both are things an auditor will ask for and expect to see.
- **Clauses 8, 9, 10 — Operation, Performance evaluation, Improvement.** Program-level and architect-level in most organizations; know them by name so you can route questions correctly in a council conversation, but do not try to author against them.

### Annex A

ISO/IEC 42001 has an Annex A of AI-specific controls that mirrors the structure of ISO/IEC 27001's Annex A. The architect designs the organization's **Statement of Applicability** against Annex A — which controls apply, which are excluded with justification, which are implemented and how. Your job is to *operate the pieces that touch training, competence, and awareness* — and to feed the evidence the architect needs to demonstrate those controls are implemented.

<!-- needs-research: name the specific Annex A control areas (e.g., AI policies, internal organization, resources, impact assessments, lifecycle) and confirm the control-numbering convention before citing exact controls in co-authoring. -->

### What you bring to a 42001 audit conversation

When the organization sits a 42001 surveillance or certification audit, the enablement seat's evidence surface is roughly:

- Training records — who completed what, when, to what score, against which role tier.
- Awareness-communication evidence — the policy announcements sent, the champion-network briefings run after each council, the operator-facing policy summaries in current circulation.
- Policy drafts, redline logs, and ratification records for every policy this module covers.
- Use-case and intake records — the questionnaire corpus.

Package these as the enablement-side evidence pack six weeks before the audit window opens. Do not assemble it the day before.

## Where this reading stops

The explicit guardrail of this chapter: you read these standards to speak the vocabulary. You do not read them to:

- Design the control library against Annex A — that is `senior-ai-governance-architect`.
- Rewrite the risk-classification taxonomy — architect again.
- Set the organization's AI risk tolerance — `head-of-ai-governance` with CAIO-level ratification.
- Lead the certification engagement — governance program.

The moment you find yourself drafting a Statement of Applicability or redesigning a GOVERN sub-category mapping, you have drifted into another ladder. [Chapter 07](07-what-you-route-out-counsel-soc-architect.md) has the handoff mechanics.

## A practical closing move — the mapping exercise

Exercise 05 of this module is the mapping exercise: walk each artifact this track's role owns (AUP, data-handling SOP, intake questionnaire, training rosters, champion network, executive scorecard, kill-switch plan, redline log) across the GOVERN categories and the 42001 clauses they evidence, and name the standards-side owner for each. Do the exercise. The map is a one-page artifact your governance partners will ask you for inside the first three months of any real role.

## Summary

- Two documents carry most of the governance-side vocabulary: NIST AI RMF 1.0 (with the GenAI Profile, AI 600-1) and ISO/IEC 42001:2023. Read both at orientation depth.
- Of the four RMF functions, GOVERN is where enablement camps — it covers policy, workforce competence, and organizational practice. MAP / MEASURE / MANAGE are touched but not led by this role.
- Of the ten 42001 clauses, 5 (Leadership), 6 (Planning), and 7 (Support — especially 7.2 Competence and 7.3 Awareness) are the enablement lead's primary surfaces. Annex A is the architect's territory.
- Audit evidence this role brings: training records, awareness-communication records, policy drafts and redline logs, intake questionnaire corpus.
- Reading is fluency; reading is not architecture. Statement of Applicability, control-library design, and taxonomy ownership are routed out. [Chapter 07](07-what-you-route-out-counsel-soc-architect.md) covers how.
- The mapping exercise (Exercise 05) produces the one-page artifact your governance partners will ask for inside the first three months.
