# EU AI Act Article 4 — Training Content at Depth

> [mod-101 Chapter 05](../mod-101-role-and-the-org-wide-enablement-operating-model/05-eu-ai-act-article-4-and-the-literacy-floor.md) read Article 4 as the regulatory floor of the enablement operating model — who the obligation falls on, what "sufficient" means, what a defensible program has to look like at the surface. This chapter goes a layer deeper: the concrete *training content* that lives inside the Article 4 obligation. Who is trained on *what*, by *when*, at *what depth*, with *what evidence*. The chapter stays with the obligation itself; the industry flavours on top of it start in Chapter 03.

## Why Article 4 is in the industry module

Article 4 is not an industry regulation. It is a horizontal obligation that attaches to any organization — in any industry — that touches the EU market as a deployer. It lives in this module for three reasons.

- **The EU-touching surface is a flavour of its own.** For every US-headquartered organization that acquires an EU subsidiary, opens a sales office in Dublin, hires contractors in Berlin, or processes data about EU residents, Article 4 is the first flavour that lands on top of the industry-neutral operating model. Treating the EU surface as its own flavour is cleaner than treating it as industry-generic — the Article 4 content is unlike what any US regulator asks for yet.
- **The content design is the move.** Chapter 05 of mod-101 stopped at the shape of a defensible program. The move the role has to make on the ground is drafting the actual content for each tier, in a language instructional designers can produce and an auditor can verify. That is this chapter.
- **It is the model for every other industry flavour.** The healthcare, finance, legal, and education chapters that follow each do the same move — translate a regulator's obligation into training content that someone can be taught and certified on. Article 4 is the cleanest instance, because the regulator's text is short and the obligation is explicit. Doing it well here makes the industry-flavour chapters faster.

## The three tiers, concretely

[mod-101 Chapter 05](../mod-101-role-and-the-org-wide-enablement-operating-model/05-eu-ai-act-article-4-and-the-literacy-floor.md) named three starting-shape audience tiers — leadership, operator, specialist. This chapter writes the actual content outline for each. For each tier the outline covers: the audience definition, what the content covers, duration envelope, assessment shape, and the written rationale for *why the content is sufficient for that audience and context* under Article 4's own language.

### Leadership tier

**Audience.** Executives (C-suite and reports to C-suite), board members (as applicable), and senior managers whose decisions set direction on AI investment, deployment, or policy. Sized at roughly 1% to 3% of total in-scope headcount in a typical enterprise.

**Content outline.**

- The technology. What generative AI is and is not at the altitude a decision-maker needs; the rough contour of what today's systems can and cannot reliably do; where current systems fail in ways that are not obvious from a demo.
- The organization's AI posture. The approved-tool envelope ([mod-102](../mod-102-selecting-and-rolling-out-ai-tools/README.md)), the policy stack ([mod-103](../mod-103-policy-co-authoring-with-governance/README.md)), the operating model ([mod-101](../mod-101-role-and-the-org-wide-enablement-operating-model/README.md)), the escalation path, the incident-response posture ([mod-109](../mod-109-ai-incident-response-and-enablement-side-rollback/README.md)).
- The organization's AI Act obligations at executive altitude. The deployer-side obligations (Article 4, Article 26, Article 27 where applicable), the high-risk designation process, the serious-incident reporting obligation (Article 73), and where the executive sits in the accountability chain.
- The scorecard. How the executive reads the enablement scorecard ([mod-106](../mod-106-outcome-measurement-and-executive-reporting/README.md)) and what questions it should prompt.
- The default behaviours. When to escalate, when to abstain, when the executive is the escalation point and what that looks like.

**Duration envelope.** 60 to 90 minutes, split across a live session and a short asynchronous pre-read. Annual refresh at 30 to 45 minutes.

**Assessment.** Short scenario-based attestation: the executive is given three realistic scenarios (a BU leader bypassing the approved-tool envelope; a vendor commercial pitch that contradicts the SOP; a regulator inquiry) and selects the correct next-action-and-escalation-target. Passing threshold stated in the program design; 80% is a reasonable starting point. The attestation record is the evidence line.

**Written rationale under Article 4.** "The leadership tier equips the executive with the technical knowledge of AI systems' capabilities and failure modes, the organizational knowledge of the policy stack and operating model, and the contextual judgment to recognize when the executive is the correct escalation point — appropriate to the executive's role as a decision-maker on AI deployment direction, not an operator of AI tools." This sentence is the one the regulator reads. Write the equivalent for every tier your organization defines.

### Operator tier

**Audience.** Employees and contractors using AI tools in the course of their work. The *default* tier — everyone in scope who is not in leadership or specialist tiers lands here. Typically the majority of in-scope headcount.

**Content outline.**

- The tools and the envelope. The approved-tool envelope ([mod-102 Chapter 02](../mod-102-selecting-and-rolling-out-ai-tools/README.md)), what to do when a useful tool is not in the envelope, the intake path for requesting one ([mod-103 Chapter 06](../mod-103-policy-co-authoring-with-governance/06-the-intake-questionnaire.md)).
- The acceptable-use policy. The seven sections of the AUP ([mod-103 Chapter 04](../mod-103-policy-co-authoring-with-governance/04-the-one-page-acceptable-use-policy.md)), with the five named approved uses and the five named prohibitions, read aloud with examples drawn from the operator's own role.
- The data-handling SOP. The data classes allowed and forbidden ([mod-103 Chapter 05](../mod-103-policy-co-authoring-with-governance/05-the-data-handling-sop.md)), the ten-minute accident path, the escalation line to security and privacy.
- Prompt and output discipline for the operator's role. The high-leverage patterns and the common pitfalls — drawn from the role's workflow interviews ([mod-104](../mod-104-training-programs-and-ai-literacy-curriculum/README.md)), not generic prompting content.
- The failure signals that mean *stop and escalate*. When the model is confident and wrong in a way that matters; when the output pattern suggests the data boundary has been crossed; when the output would be material if sent external.
- Transparency obligations where they attach (Article 50). If the operator's role produces content that interacts with people (customer-facing chat, external-facing written output, deepfake-adjacent content), the transparency content attaches here.

**Duration envelope.** 90 to 120 minutes, typically split across a general operator module (60 minutes) and a role-specific module (30 to 60 minutes). Annual refresh at 45 to 60 minutes; shorter targeted refreshes when the approved-tool envelope or AUP changes materially.

**Assessment.** Mixed: multiple-choice knowledge check on the policy stack (passing threshold 80%); scenario-based judgement on three to five realistic role situations; optional prompt-and-review exercise for roles that use generative AI in the open. The combination is what evidences "sufficient for the operator's context."

**Written rationale under Article 4.** "The operator tier equips the employee or contractor to operate approved AI tools inside the organization's acceptable-use and data-handling envelope, recognize the failure signals that require escalation, and meet the transparency obligations attached to the operator's role under Article 50 where applicable — appropriate to the operator's role as a user of AI systems in the course of their work."

### Specialist tier

**Audience.** People whose job is to build, configure, red-team, administer, or deeply review AI tools. Typically the engineering, risk-engineering, ML, and security-engineering populations; small share of headcount but the tier the auditor reads most carefully because their mistakes propagate.

**Content outline.**

- Everything in the operator tier, plus:
- The technical and operational depth of the AI Act obligations that bind the organization's build posture. High-risk obligations under Chapter III (risk management system, data governance, technical documentation, record-keeping, human oversight, accuracy / robustness / cybersecurity) at the altitude the specialist's role actually touches them.
- The organization's internal AI engineering standards — build standards, model-eval standards, deployment gates — handed off to the adjacent curricula. See `applied-ai-engineer-learning`, `ai-risk-engineer-learning`, and the AI Engineering family's own content for the engineering-depth material; the specialist tier in the enablement curriculum references it rather than reproducing it.
- The incident-response specialist content ([mod-109](../mod-109-ai-incident-response-and-enablement-side-rollback/README.md)) for roles that are on-call for AI incidents.

**Duration envelope.** Variable. The enablement lead sets a floor (60 minutes on the enablement-side content: policy, operating model, escalation, transparency); the role-specific technical content is set by the adjacent curriculum's owner.

**Assessment.** Deferred to the adjacent curriculum where possible — if the AI engineer has completed the applied-ai-engineer-learning track's own evaluated content on model evaluation, do not re-assess them on the same material. The enablement lead's evidence line for the specialist tier is the completion record of the enablement-side content plus the pointer to the adjacent curriculum's evidence.

**Written rationale under Article 4.** "The specialist tier equips the role that builds, configures, administers, or red-teams AI systems with the deeper technical and risk material appropriate to the specialist's context — deferred to the adjacent AI Engineering curricula where the engineering-depth content lives, with the enablement-side content providing the policy, operating-model, escalation, and transparency layer."

## The content-update trigger matrix

Article 4 obliges the content to be *current*. The audit question is: *when the tools, policies, or risk posture change, how long before the content catches up?* An answer of "it floats" is a failed answer. The trigger matrix is the written rule.

```
Trigger                                              | Content reviewed             | Review window
-----------------------------------------------------+------------------------------+---------------
Approved-tool envelope change (add, remove, swap)    | Operator + specialist        | 30 days
AUP or SOP revision                                  | All tiers (sections changed) | 30 days
EU AI Office or member-state authority guidance      | All tiers                    | 60 days
Serious incident retrospective finding               | All tiers (affected material)| 30 days
Member-state enforcement action (any deployer)       | All tiers                    | 90 days
Vendor model or capability change (material)         | Operator + specialist        | 60 days
Annual methodology review                            | All tiers                    | Annual
```

Three disciplines make the matrix survive contact:

- **Each trigger has a named owner.** The approved-tool envelope owner surfaces envelope changes to the curriculum team on commit, not on discovery. The AUP owner routes a revision through the curriculum-update process on redline-finalization. The incident-response lead surfaces retrospective findings on close. Without named owners, the triggers do not fire.
- **The review window is a deadline, not an aspiration.** If the review window is 30 days and the review takes 90 days, the content is out of compliance for 60 days. The window is a scorecard signal; publish it in the scorecard ([mod-106](../mod-106-outcome-measurement-and-executive-reporting/README.md)).
- **The matrix itself is versioned.** Add rows when new trigger types emerge (a new regulator's guidance, a new vendor relationship, an acquired BU's regulator). Review the matrix annually alongside the methodology.

## The scope decision

Article 4 obliges deployers to ensure literacy for *staff and other persons dealing with the operation and use of AI systems on their behalf*. The scope decision has four honest questions and one default.

- **Are contractors and consultants in scope?** Usually yes, where the contractor uses an organization-owned AI tool (or the organization's own data in an AI tool) in the course of the work. Contract language should align; coordinate with procurement and legal.
- **Are outsourced operators in scope?** Yes, where a third-party operator (a BPO, a managed-service provider) operates an AI system on the organization's behalf. The literacy obligation flows through contract to the operator; the enablement lead ensures the contract has the hook and that evidence flows back.
- **Are US-only employees whose output can reach EU data subjects in scope?** This is the hard question. The honest answer most organizations arrive at: scope wider than the strict territorial reading suggests. If a US-based customer-service representative's AI-assisted response can reach an EU customer, the reasonable scope includes that representative. The alternative is to split the workforce in a way that is operationally expensive and defensively weak.
- **Are new hires in scope from day one?** Yes. The literacy obligation attaches to the role, not to tenure. New-hire onboarding includes the relevant tier's content before the new hire operates an AI tool in production.

**The default when in doubt — scope wider.** "Best extent" is read against the organization's actual AI surface, not the smallest scope the literal text permits. A narrow-scope posture backed by a theory read of territoriality is a posture a reasonably sophisticated market-surveillance authority will push back on. A wider-scope posture backed by the theory that the obligation attaches to the AI surface is one that is cheaper to defend and cheaper to explain to counterparts.

Document the scope decision as a dated artifact with the names of the counterparts (legal, HR, workforce planning) who ratified it. Scope-definition evidence is one of the four classes of audit evidence the regulator will look for first.

## The "by when" question

Article 4 has been in application since **2 February 2025**. For organizations that touched the EU market on that date, the obligation is live. For organizations that start touching the EU market later (via acquisition, geographic expansion, contractor hiring), the obligation lands on that organization at the moment of first deployer activity.

Three practical "by when" postures:

- **At-launch posture.** Every in-scope person has completed the relevant tier before they operate an AI tool against EU-touching activity. New hires complete onboarding before production use. The at-launch posture is the only defensible shape of the obligation.
- **Backfill-after-the-fact posture.** Operators are using AI tools; the training is scheduled for "next quarter." This is the posture most organizations have been in since 2 February 2025 and that has been dragging; it is not defensible against an active inquiry. If this is your posture, publish the completion date to the scorecard and work the dial.
- **"We'll do it when EU revenue justifies it" posture.** Not a posture. Article 4 attaches on the AI surface meeting the EU market; the revenue threshold is not in the regulation. Treat this posture as a failed answer.

## Evidence the regulator reads

Audit-read-this evidence has four classes, all of which must exist and be retrievable without the enablement lead in the room.

- **The content library.** The actual modules, assessments, scripts, slides, facilitator notes, performance-support materials. Versioned; each version dated; the retention period for retired versions stated in policy.
- **The completion roster.** Every in-scope person has, for each tier they belong to, a dated completion record and an assessment result. Non-completers' handling (reminder, manager escalation, access suspension if the SOP permits it) is recorded.
- **The content-update log.** Each trigger that fired, the content that was reviewed, the change that landed (or did not, with reason). The audit question is *how* the content stays current; the log answers it.
- **The scope-definition record.** The dated artifact naming the in-scope populations and the ratification signature line (legal, HR, workforce planning, the enablement lead). Revisit annually; log any mid-year revision.

Every evidence item has a named retriever who is not the enablement lead. If the only person who can produce the completion roster is the enablement lead, the evidence is not yet audit-ready; it is still inside the enablement lead's head.

## The three distortions to resist

Three recurring distortions push the content either too thin or too thick. The skilled enablement lead keeps the content proportional in both directions.

- **The 20-minute marketing e-learning.** A short video, a quiz, a certificate. Satisfies no part of Article 4 for most operators and no part at all for specialists or leaders. If the organization's current content is in this shape, the first move is not to improve the content — it is to re-scope the program against the three tiers.
- **The 10-hour engineering course for every employee.** The equal-and-opposite distortion: a thorough, deep, technical curriculum delivered to populations that do not need it. Expensive, unpopular, and creates its own failure mode (operators who disengage and complete the assessment with a browser tab open). Proportionality means *less* content, not *more*, for the operator who is a line-of-business individual contributor. Save the depth for the specialist.
- **The treat-literacy-as-communications distortion.** The content reads as internal marketing for the AI program — exciting, visionary, forward-looking. Zero literacy content. Fails Article 4 and misleads the workforce. Internal communications ([mod-105](../mod-105-champion-networks-and-change-management/README.md)) is a separate channel; the literacy curriculum is not it.

## How this chapter connects to the industry chapters

Article 4 is the horizontal obligation. The industry chapters that follow add the vertical content:

- A healthcare operator tier adds HIPAA data-class content (Chapter 03).
- A bank operator tier adds SR 11-7 awareness and FINRA supervision content for regulated roles (Chapter 04).
- A legal-engineering operator tier adds work-product and privilege content (Chapter 05).
- An education-sector operator tier adds FERPA / COPPA content for roles that touch student data (Chapter 06).

Each industry's exercises 05 build the industry-adjusted curriculum on top of the Article 4 shape. If the Article 4 shape is wrong, the industry overlays do not save the program.

## Summary

- Article 4 is in this module because it is the first flavour that lands on top of the industry-neutral operating model for EU-touching organizations and because its content-design move is the model for every other industry flavour.
- Each of three audience tiers gets a concrete content outline, duration envelope, assessment shape, and a written proportionality rationale in the regulator's own language.
- The content-update trigger matrix is the written rule for how the content stays current; each trigger has a named owner and a hard review-window deadline.
- Scope defaults wider — the organization scopes the obligation against its AI surface, not the smallest territorial read.
- Evidence sits in four classes (content library, completion roster, content-update log, scope-definition record); each has a retriever who is not the enablement lead.
- Three distortions to resist: marketing e-learning, blanket engineering course, literacy-as-communications.
- The industry chapters in the rest of the module stack vertical content on this horizontal skeleton. Get the skeleton right first.
