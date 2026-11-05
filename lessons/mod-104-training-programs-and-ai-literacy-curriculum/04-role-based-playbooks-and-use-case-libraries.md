# Role-Based Playbooks and Use-Case Libraries

> The foundational curriculum makes every operator safe. The role-based playbooks make every operator *productive*. Without the playbooks, you have a literacy program that clears Article 4 and produces no business value. Without them, operators finish the foundational curriculum, open the approved tool, and have no idea what to type in. The playbooks are the thing that closes the gap from "knows the policy" to "does the job faster with AI."

## What a role-based playbook is

A role-based playbook is a short, maintained artifact per function (sales, service, operations, finance, HR, legal, engineering, leadership — plus any function your org runs at headcount scale: marketing, procurement, clinical, field operations, etc.) that contains:

1. **The named use cases** for the role, ranked by frequency and impact. Three to twelve per role.
2. **A prompt library** — the approved prompt templates for each use case, with placeholders, variables, and the data classes they accept.
3. **An agent / workflow library** — the approved internal agents or multi-step workflows for use cases where a single prompt is insufficient.
4. **Verification and escalation notes** specific to the function (not the generic version from the foundational curriculum; the version that names the regulated data, the counterparties, the audit pattern).
5. **Worked examples** — before-and-after artifacts showing a real operator's workflow with and without AI. Named example, not generic.
6. **Owner and refresh cadence** — who maintains the playbook, how often it is reviewed, when it was last changed.

Keep each playbook to 10–20 pages. More than that and it is a reference manual nobody reads. Less than that and it is a marketing brochure.

## Why one artifact per function

The alternative is a single org-wide prompt library. That alternative fails for three reasons.

- **Operators don't browse.** A sales rep looking for a prompt wants to open *their* playbook and find three to twelve relevant entries. They are not going to read 400 prompts across every function to find theirs.
- **Data handling differs by function.** A legal reviewer's acceptable data classes are not the same as a service rep's. Mixing them in one library creates ambiguity about what each operator can safely use.
- **Maintenance owners differ.** The legal playbook should be maintained by a senior legal reviewer with AI fluency (a specialist-tier contributor). The sales playbook should be maintained by a senior sales enablement partner. One org-wide library has no credible owner.

The playbook is the delivery unit. One per function. Named owner, named refresh cycle, named consumers.

## The eight starter playbooks

Not every organization needs all eight; most mid-size organizations need six or seven, and large organizations need more. The eight that recur:

### Sales

Use cases that recur: inbound-lead qualification notes, account-research synthesis (public-source only, with a clear rule against scraping), proposal-draft starters from a brief, discovery-call summary and next-step list, objection-response drafts.

Verification notes: every quoted figure about a prospect is checked against the primary source. AI-generated "discovery insights" are flagged as assumptions, not facts.

Escalation: anything that touches pricing terms outside a published playbook escalates to the deal desk. AI never quotes custom pricing.

### Service / customer support

Use cases that recur: on-brand reply drafts to tier-1 tickets, 14-day case-history summaries for handoff, ticket classification, de-escalation language suggestions, knowledge-base draft entries from resolved tickets.

Verification notes: every policy citation in a customer reply is checked against the live policy, not the AI's recollection of it. Every refund / credit figure named in a draft is checked against the system of record.

Escalation: legal-sounding complaints, mental-health signals, requests for information the AI generates but the agent cannot personally verify. The escalation list is published and dated.

### Operations

Use cases that recur: incident-report drafts from a raw log, SOP revision from a changed input, meeting minutes with action-item extraction, shift-handoff summaries, root-cause narrative drafts.

Verification notes: AI-generated causal claims in incident reports are flagged "preliminary" until a human reviews. Timestamps are checked against the system of record.

Escalation: anything that touches a regulated workflow (safety-critical process, labelled-batch processing, etc.) has a hard review gate before the AI draft leaves the operator.

### Finance

Use cases that recur: variance-commentary drafts from a close pack, expense-policy classification, vendor-document summarization, memo drafts for internal finance decisions, policy-language explanation for operator audiences.

Verification notes: every number in a draft is traced to the pack it came from. AI does not generate numbers; it narrates them. "The margin fell 3.2 ppt" is *checked* against the pack; "the margin fell 3.2 ppt because of X" is *the operator's* causal claim, drafted by AI, owned by the operator.

Escalation: anything that would be sent to an auditor, a tax authority, or a regulator. No AI-generated artifact crosses that line without a named human sign-off step.

### HR

Use cases that recur: job-description drafting, interview-note synthesis, feedback-letter drafts, policy-FAQ generation, onboarding-document personalization.

Verification notes: every statement about an individual employee is checked against the record. AI-drafted feedback is explicitly labelled as a draft for the manager's revision.

Escalation: anything touching protected-category assessments, disciplinary actions, or legal proceedings. The data-handling SOP for HR is stricter than most functions; the playbook names it.

### Legal

Use cases that recur: contract-clause extraction, precedent-search starter, redline-first-pass against a standard, matter-summary for intake, plain-English explanation of a clause for an operator audience.

Verification notes: every clause cited by the AI is verified against the actual contract text. AI-generated case law is treated as a hypothesis, not a citation, until a human verifies the case exists and says what the AI said it says.

Escalation: anything that creates a legal opinion. The legal playbook is clear: AI drafts *descriptive* legal text, humans draft *opinions*. This maps directly to [mod-103 Chapter 07](../mod-103-policy-co-authoring-with-governance/07-what-you-route-out-counsel-soc-architect.md) on what the enablement side routes to counsel.

### Engineering

Use cases that recur: pair-programming, test generation, code review, documentation generation, repository-scoped Q&A.

**This is the deferral case.** The engineering playbook for IC engineers mostly points to the [`ai-assisted-software-engineer`](https://github.com/ai-engineering-curriculum/ai-assisted-software-engineer-learning) curriculum (level 20) for the in-depth patterns. Your playbook names the approved tools, the data-handling rules for code and secrets, and the two or three org-specific patterns (e.g., "when generating tests for the billing service, use these fixtures"). Depth lives in the level-20 track; you do not re-author it.

Likewise the IC-analyst playbook defers to [`ai-augmented-analyst`](https://github.com/ai-workforce-curriculum/ai-augmented-analyst-learning) (level 20) for the data-exploration and chart-generation patterns.

### Leadership

Use cases that recur: executive-summary drafting from a longer artifact, meeting-prep brief generation, decision-memo first drafts, scorecard narrative drafting from numbers.

Verification notes: AI does not surface strategic claims a leader has not vetted. Everything that would be quoted in a board meeting is read aloud by the leader before the meeting; the AI is a drafting assistant, not a strategist.

Escalation: anything the AI drafts about people in the organization requires a named human review before it is shared.

## The prompt library — what makes it usable

The prompt library inside each playbook is where operators go when they are mid-task. Design it for the moment of use, not the moment of reading.

Each library entry has:

- **Name.** Short, task-shaped. "Draft a tier-1 service reply," not "Email generation."
- **When to use it.** One or two sentences. The common failure is a prompt for a case the operator does not have.
- **The prompt template.** Verbatim text, with named placeholders in `[[BRACKETS]]`. The variables are named by *content*, not by variable name: `[[CUSTOMER_TICKET_TEXT]]`, not `[[INPUT_A]]`.
- **Data classes accepted.** Which data classes from the SOP are safe to put in `[[CUSTOMER_TICKET_TEXT]]`. "Public, internal. Not confidential or restricted." The field is non-optional.
- **Example filled-in input and output.** One real, anonymized example. This is often the thing the operator reads most.
- **Known failure modes.** Two or three sentences on where this prompt breaks and how to notice.

Keep the prompt library in a *format operators can actually open at the point of use* — a wiki page, a shared doc, a sidebar in the approved tool if integrated. A beautifully designed PDF nobody opens is a worse library than a working wiki page.

The prompt library is **not** a prompt-engineering textbook. If an operator needs to invent a new prompt mid-task, they go to office hours ([Chapter 05](05-the-delivery-mix.md)) or to prompt coaching ([Chapter 06](06-prompt-coaching-for-non-engineers.md)) — they do not improvise inside the prompt library and then share the improvisation.

## The agent / workflow library

Some use cases need more than a single prompt — a multi-step workflow, a retrieval-augmented pattern, an internal agent commissioned from [mod-110](../mod-110-commissioning-internal-ai-tools-and-custom-agents/README.md). The agent library is where those live. Each entry has:

- **Agent name and owner.** The named internal owner of the agent configuration (not the vendor).
- **What it does, in operator voice.** One paragraph.
- **How to open it.** Link or instructions.
- **Inputs and outputs.** What the agent takes; what it produces.
- **Approved data classes.** Same taxonomy as the prompt library.
- **Known limits.** Where this agent fails, and what to do when it does.
- **Escalation path when the agent misbehaves.** The incident fast lane from [mod-109](../mod-109-ai-incident-response-and-enablement-side-rollback/README.md).

Not every playbook has an agent library on day one. Start with the prompt library. Add the agent library as internal agents are commissioned.

## The playbook authoring process

You do not write the playbooks alone. The process is three-partied:

1. **The function's senior IC or manager** nominates and prioritizes the use cases. They know the role; you do not. If you write the playbook without this seat, the use-case list will be aspirational, not actual.
2. **A specialist-tier contributor (often a champion from [mod-105](../mod-105-champion-networks-and-change-management/README.md))** authors the prompt library entries and the worked examples. They are the operator-voice author.
3. **You (the enablement lead) and the governance co-author** vet the data-handling and escalation notes, map them against the SOP, and sign the published version.

The playbook is signed by all three parties. Signed-and-dated is the audit evidence; a draft in a shared drive is not.

Budget per playbook: 4–8 weeks of elapsed time from kickoff to a signed v1, with an owner continuing to maintain it quarterly after. Not every function gets a playbook in year one. [Chapter 05](05-the-delivery-mix.md) treats the sequencing.

## The use-case library — the cross-function view

Underneath the per-function playbooks sits a single organizational artifact: the **use-case library**. Each entry is a durable record of a use case that has been piloted, decisioned, and either rolled out or shelved.

The use-case library is maintained as part of the operating model from [mod-101 Chapter 03](../mod-101-role-and-the-org-wide-enablement-operating-model/03-authoring-the-enablement-operating-model.md), and the rollout pipeline from [mod-102](../mod-102-selecting-and-rolling-out-ai-tools/README.md) is where new entries come from. For the training program, the use-case library plays two roles:

- It is the *source* of the role-based playbook's use-case list — you don't invent use cases in the playbook; you draw them from the library.
- It is the *display case* for use-case spotlights ([Chapter 05](05-the-delivery-mix.md)) — the delivery vehicle that shares successes across functions.

If your organization does not have a use-case library yet, build it. One row per use case. Columns for: name, function, sponsor, approved data classes, approved tools, pilot date, decision date, rollout status, link to the playbook entry, link to the lessons-learned note. An unmaintained use-case library is a sign that rollouts are not being closed out properly.

## Common playbook failures

- **The playbook is a wish list.** Someone drafts 40 use cases, three are actually used, and the artifact loses credibility. Rank by frequency; start with the top three; expand once used.
- **The playbook is vendor-branded.** If a playbook is written around the current approved tool and the tool is replaced, the playbook is scrap. Write the use cases first, the vendor-specific instructions in a replaceable section.
- **The playbook has no owner.** An unowned playbook is a dead playbook within 90 days. Name the owner on the title page and in the service catalog.
- **The playbook duplicates the operator curriculum.** The playbook assumes the foundational curriculum; it does not re-teach data handling from scratch. Point to the SOP; do not repeat it.
- **The playbook does not name the escalation humans.** "Escalate to legal" is insufficient. "Escalate to the Senior Counsel on duty — current roster at [link]" is sufficient.

## Where this chapter feeds

- [Chapter 05](05-the-delivery-mix.md) is where use-case spotlights, bootcamps, and challenges draw from the playbooks and the use-case library.
- [Chapter 06](06-prompt-coaching-for-non-engineers.md) runs the coaching that improves prompt-library entries over time.
- [Chapter 07](07-measuring-fluency-growth.md) uses the playbook's named use cases as the task-level proficiency targets.
- Exercise 03 asks you to author one complete role-based playbook for one function.

## Summary

- One playbook per function. Starter set: sales, service, operations, finance, HR, legal, engineering, leadership.
- Each playbook has six pieces: named use cases, prompt library, agent / workflow library, verification and escalation notes, worked examples, owner and refresh cadence.
- Engineering and IC-analyst playbooks *defer* depth to the level-20 tracks (`ai-assisted-software-engineer`, `ai-augmented-analyst`). The playbook names tools, data rules, and org-specific patterns; the depth lives in the engineering curricula.
- Three-partied authoring: function senior IC + specialist-tier contributor + enablement lead with governance co-author. Signed-and-dated is the audit evidence.
- Underneath the per-function playbooks sits the cross-function use-case library — the source of truth for what the org has piloted, decisioned, and shipped.
- The playbook is a usable artifact, not a reference manual. 10–20 pages. Short entries. Updated quarterly. Owned by someone named.
