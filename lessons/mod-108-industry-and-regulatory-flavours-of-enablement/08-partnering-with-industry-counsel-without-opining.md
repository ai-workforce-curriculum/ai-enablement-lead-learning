# Partnering with Industry Counsel — Without Rendering Legal Opinion

> Chapters 03 through 06 told the enablement lead what is in each industry's regulatory surface; Chapter 07 said who owns which obligation. This chapter is how the enablement lead *works* with the industry-specific legal and compliance partners day to day — asks questions well, surfaces risk cleanly, and produces the operational substance that lets counsel's judgment land — without crossing into legal opinion. The role's posture is simple: the enablement lead is an operator, not an advisor. The discipline is less simple.

## Why this posture is load-bearing

Three reasons the posture matters in regulated industries specifically.

- **Legal opinions are costly to clean up.** A line in an AUP, SOP, training module, or executive brief that reads as a legal conclusion is now on the record. If the conclusion is wrong, the organization has to retract it (expensive) or defend it (more expensive). The enablement lead who writes "under Rule 1.6 this is permitted" has issued an opinion; the enablement lead who writes "see Rule 1.6 — legal to confirm the specific posture" has not.
- **Professional-responsibility rules bind the people who can give opinions.** Attorneys, medical professionals, licensed financial professionals, and others operate under rules of professional responsibility that constrain them and that protect the client / patient / counterparty. Those protections do not run through non-licensed operators. When the enablement lead speaks as though they do, the protections silently do not attach. That is a harm the organization will find out about on the worst possible timing.
- **The counterpart counsel and compliance partners are the long-term relationship.** The enablement lead will co-author artifacts with these partners across every module of this track and across the role's full tenure. The partners' willingness to co-author depends on their confidence that the enablement lead will stay in scope. The role that drifts into opinion loses the counterpart's trust and gets slower service on every subsequent artifact.

## The three postures to know by name

Three distinct postures the enablement lead can occupy in a conversation with legal or compliance. Each has a legitimate use; mixing them is the common failure.

### Posture 1 — Operator surfacing a question

The default posture. The enablement lead brings a question, provides operational context, and asks for a decision. Does not propose the answer; may propose structure for making the answer easier to reach.

Example:

> "Our customer-success team has asked for permission to use [tool X] to draft responses to customer support tickets that include summaries of PHI. The tool has a BAA. We would like compliance to confirm whether the proposed use is permitted under the BAA's defined services and HIPAA's minimum necessary standard. I have attached the proposed workflow with the specific prompt and output patterns, and the three use cases the team is most frequently facing. We have paused the use pending response. The customer-success lead can defer this for 14 business days without impact; longer than that, we should discuss."

Three features of this posture: a clear question, operational context, a decision-ask, a timing signal. No proposed legal conclusion.

### Posture 2 — Co-author refining counsel's draft

The enablement lead takes counsel's or compliance's output and translates it into operator-facing language. Does not change the substance; does flag where the operator-facing language risks drifting.

Example:

> "Compliance's draft of the AUP's 'prohibited uses' section includes the line 'no use of AI output as the sole basis for a credit decision.' From an operator-facing perspective, operators have asked what 'sole basis' means operationally — if a credit analyst uses an AI-drafted memo in forming their view, is the AI 'the sole basis'? I don't have an answer for that; the operational substance I can add is a concrete example pattern that compliance can either confirm or redraft against. Attached is a proposed example under the current draft; please confirm or redline."

The enablement lead has not re-drafted the compliance language; has flagged the operator-facing ambiguity and offered an operational example for compliance to anchor to.

### Posture 3 — Carrier of a decision that has already been made

When counsel or compliance has decided something, the enablement lead carries the decision to operators without re-interpreting it. If an operator asks "does this apply to case X?" and the decision is ambiguous on case X, the enablement lead escalates — does not interpret.

Example:

> "Compliance has determined that AI-assisted adverse-action notices require the reason-code verification workflow. The workflow is available at [link]; the training module is [link]. If your team encounters a case where the applicability of the workflow is unclear, please escalate through [channel] rather than making the call locally."

The enablement lead has carried the decision, pointed to resources, and defined the escalation path. Has not extended the decision to a case counsel did not consider.

## The sentence patterns that stay in scope

The posture is easier to run with a set of sentence patterns the enablement lead can reach for.

**Starting sentences that stay in scope:**

- "Operationally, we see the following pattern — what is counsel's position?"
- "From an enablement-content perspective, the training module would need to say X, Y, or Z — which is correct?"
- "I can draft a first version of the operator-facing language against compliance's position; could compliance provide the position?"
- "The intake questionnaire can route this type of case to [team]; would you like it to?"
- "I am not qualified to answer this; let me route to [role]."

**Starting sentences that have drifted:**

- "Under [rule], the correct approach is…"
- "Legally, this is permitted / prohibited because…"
- "Our counsel's position on this is X." (unless you have confirmed this with counsel for this specific question in this specific context)
- "The precedent on this is Y." (precedent-citing is a legal act)
- "The regulatory requirement is Z." (interpreting the regulatory requirement is a legal act; summarizing a confirmed requirement is fine)

**Middle sentences that stay in scope:**

- "The operator population size is [N], and the use frequency is roughly [X per week]; this tells me the operational impact of your decision but not the decision itself."
- "I can structure the training content so that the answer is reflected in operator behavior; the answer is counsel's."
- "If counsel's decision changes, I can update the SOP within [window]; here is the content-update trigger matrix."

**Closing sentences that stay in scope:**

- "I will carry the decision into the AUP / SOP / training once I have it; please let me know the decision timing."
- "The escalation path for ambiguous cases is now [channel]; I will coach operators to use it."
- "If this decision changes the approved-tool envelope, I will coordinate with [procurement / IT / governance].

## The four questions that signal drift

Four questions the enablement lead should hear themselves asking as a signal they are drifting. Each has a redirect.

- **"What is the legal interpretation of…?"** The enablement lead asks this of counsel, not answers it. If an operator asks the enablement lead this, the redirect is "that is a question I will bring to legal; here is the escalation."
- **"Is this permitted under…?"** Same pattern. If the enablement lead is forming an opinion, the opinion lives with counsel, not with the enablement lead.
- **"Does this regulation apply to our use case?"** The applicability question is a legal question. The enablement lead's role is to surface the use case clearly so counsel can answer.
- **"What should we do about this new regulation / guidance / enforcement action?"** The enablement lead can note that something has happened and ask for direction; the direction itself is counsel's.

## The pre-read discipline for industry conversations

When the enablement lead is going into a conversation with a specific industry counterpart (privacy officer, MRM lead, general counsel, chief privacy officer at an ed-tech vendor, academic-integrity office), the pre-read discipline keeps the conversation productive and inside the role.

- **One-page pre-read.** Three sections. (1) The operational situation — what the user population is, what the tool is, what the data flow looks like, what the proposed change is. (2) The specific questions that need a decision — framed as decisions, not conclusions. (3) The timing signal — when the decision is needed, what the cost of a delay is, what the cost of a wrong-fast decision would be.
- **Attached operational context.** Workflow diagrams, prompt examples, output patterns, intake-question responses, training-content drafts. Enough material for counsel to make the decision without an additional round of information requests.
- **A proposed structure for the answer.** Not a proposed answer. A structure — "the decision could be made at the AUP level / the per-tool level / the per-use-case level; our preference is level X for operational reasons Y, but we defer to counsel on which level is actually load-bearing from a regulatory perspective."
- **The non-asks made explicit.** "We are not asking counsel to review the specific wording of the training module; the module will be re-reviewed if the decision changes." This narrows the ask and avoids the common drift where every meeting with counsel becomes an open-ended review.

## The ongoing-relationship moves

Four moves across the full relationship with industry counsel, not just inside one conversation.

- **Regular cadence.** Standing meetings with the privacy officer, the compliance officer, the general counsel's office — short, agenda-driven, not open. The enablement lead's calendar discipline here protects both roles.
- **The quarterly artifact review.** Once a quarter, walk the AUP, SOP, intake questionnaire, and scorecard surfaces with each counterpart. Catch drift before it accumulates.
- **The incident-adjacent retrospective.** After any incident that touches the counterpart's regulatory surface, a short retrospective to update the operational substance and the training. The retrospective is not a legal review; it is an operational one.
- **The capacity-signal.** When the counterpart's team is a bottleneck (MRM at a bank, privacy officer at a healthcare organization, chief privacy officer at an ed-tech vendor), the enablement lead surfaces the bottleneck to leadership. The move is not to backfill the counterpart; the move is to make the bottleneck visible so leadership can fund capacity.

## When the enablement lead is themselves a licensed professional

Some enablement leads hold the license of the industry they serve — attorney, nurse, physician, registered representative, FINRA Series holder, certified accountant. The posture is especially important in this case because the organization is paying the role for enablement work, not for the professional-responsibility exercise of their license.

Two disciplines:

- **Separate the hats explicitly.** When the licensed-professional enablement lead is about to render a view that would be a professional opinion in their license, they stop and say "I'll take this question off the enablement surface; speaking as a licensed [profession] I would…" The explicit separation documents which hat was worn. In practice, the right move is often to route the question to the counterpart with the license-and-accountability pairing for the organization's purposes.
- **Do not blur the hat in writing.** The enablement lead's written artifacts (AUPs, SOPs, training content, intake routing) do not carry professional opinion even if the drafter holds the license. Written artifacts are the enablement lead's; opinions are the licensed professional's — and the organization typically expects the licensed role, not the enablement role, to be the source.

This is subtle enough that it is worth discussing with the general counsel when the enablement lead is hired into a legal-engineering role or when a dual-hatted person takes on the enablement responsibility.

## A short case walk — healthcare example

To ground the posture:

**Situation.** A clinical informatics team has started using a coding assistant to generate patient-portal replies. The tool has a BAA. The quality is good; the volume is growing. The privacy officer gets wind of the use pattern and flags it for review.

**Wrong move.** The enablement lead writes a memo stating that under HIPAA's minimum necessary standard, the use is permitted because the tool has a BAA and the operators are only providing minimum necessary PHI in each prompt.

**Right move.** The enablement lead writes a one-page situation memo that includes: the use pattern with example prompts and outputs, the tool's BAA terms as attached, the operator population and volume, the proposed guardrails for the operator-facing content (specific prompt patterns, specific prohibited content), and the question for the privacy officer — "does this use meet HIPAA's minimum necessary and the BAA's defined services? If yes, the training module and SOP update can land in two weeks; if conditional, under what conditions; if no, we will pause the use within 24 hours." The privacy officer makes the call. The enablement lead executes against the call.

The difference between the two moves is not the operational substance — the enablement lead did the same work. The difference is who holds the regulatory determination.

## A short case walk — finance example

**Situation.** A credit analyst team has asked to use a generative tool to draft portions of credit memos. The memos are used in loan approval. The tool is in the approved-tool envelope; the use has not been through MRM.

**Wrong move.** The enablement lead declares the use permitted because "the output is still reviewed by the analyst and underwriter" and updates the AUP's approved uses to include it.

**Right move.** The enablement lead routes the use to MRM as a candidate model, documents the operational workflow, pauses the use pending MRM determination, and surfaces the MRM-queue latency to the CRO if the determination is slow. The AUP's approved uses do not change until MRM has determined classification.

Same operational substance; different ownership of the determination.

## Summary

- The enablement lead is an operator, not an advisor. Operator-side artifacts and training are the enablement lead's; opinions and regulatory determinations belong to counsel and compliance.
- Three postures by name: operator surfacing a question, co-author refining counsel's draft, carrier of a decision already made. Mixing them is the common failure.
- Sentence patterns that stay in scope (starting, middle, closing) and sentence patterns that have drifted into legal opinion.
- Four questions that signal drift: legal interpretation, permission, applicability, response-to-new-regulation. Each has a redirect.
- Pre-read discipline for industry conversations: one-page pre-read, attached operational context, proposed structure (not answer), explicit non-asks.
- Ongoing-relationship moves: regular cadence, quarterly artifact review, incident retrospectives, capacity signal — not capacity backfill.
- When the enablement lead holds the license of the industry, separate the hats explicitly in speech and keep written artifacts on the enablement side.
- Two short case walks (healthcare, finance) illustrate the same operational substance under different ownership of the determination.
