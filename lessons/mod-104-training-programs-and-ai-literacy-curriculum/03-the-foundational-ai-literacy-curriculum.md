# The Foundational AI Literacy Curriculum

> There is a single curriculum that every in-scope person in the organization completes — regardless of role, regardless of tier. It is short. It is tool-agnostic. It is the thing an auditor reads first and the thing new hires complete on day one. Most of the design mistakes in enterprise literacy programs are in this foundational curriculum: too long, too vendor-specific, too divorced from the organization's policy, and too focused on "what is an LLM" at the expense of "what do I do and not do here."

## What "foundational" means — and what it does not

Foundational is not *beginner*. It is the shared baseline every tier of fluency rests on. A VP needs it. A warehouse operator needs it. The specialist tier builds on top of it without re-teaching it.

Foundational is *not* the full operator curriculum. The foundational layer covers what is common across operators; the role-based playbooks in [Chapter 04](04-role-based-playbooks-and-use-case-libraries.md) cover the function-specific depth that comes after. A three-hour foundational module plus a one-hour role playbook will beat a seven-hour generic course every time.

The foundational layer's job is to make the next thing — the role-based playbook — land cleanly. If a specialist can skip the foundational layer and lose nothing, your foundational layer is too shallow. If an operator finishes the foundational layer and still does not know what to do differently tomorrow, it is too abstract.

## The six-module skeleton

The foundational curriculum breaks into six modules. Each one maps to a question an operator will actually ask. Teach the modules in this order; the dependencies are real.

### Module 1 — What these tools are, in one honest page

- The shape of a modern generative AI tool (LLM, context window, prompt, response, tool calls, retrieval). The point is not depth; the point is a mental model that does not mislead.
- Three honest statements about limits: (a) output is a prediction, not a fact; (b) the tool does not know what it does not know; (c) the tool changes quietly between versions. Every operator needs these three statements in their head.
- One demonstration — not a "wow, look what AI can do" demo, a *grounded* demo of a real workflow the operator will do themselves next week.

Delivery: 20–25 minutes. Live or recorded. The thing to protect against: slides that present AI as more capable or less capable than it is. Both failures feed dysfunction.

### Module 2 — The approved-tool envelope

The organization's current list of approved tools, with the sanctioned use for each. Deliberately *not* the full catalog of every tool anyone might have heard of — the approved envelope, with the line between "approved for use in regulated workflows" and "approved for general use" visible.

This module ages the fastest. Design it as a *data section* (a table pulled from the service catalog, a link to the live list) rather than embedded slides, so the content stays current without re-authoring.

Delivery: 10–15 minutes. Mostly a reference. The acceptance criterion is that an operator leaves knowing which tool to open for which task — not that they can recite the list.

### Module 3 — The acceptable-use policy in operator voice

The one-page acceptable-use policy from [mod-103 Chapter 04](../mod-103-policy-co-authoring-with-governance/04-the-one-page-acceptable-use-policy.md), taught as behavior, not as text. Three or four scenarios ("you're about to paste a customer list into a chatbot — what do you do?") beat a recitation of the policy clauses.

Delivery: 20–30 minutes. This module is where the co-authoring work from mod-103 pays off: the policy is readable, and the operator leaves with it in their head instead of in a tab.

### Module 4 — The data-handling SOP, in scenarios

The data-handling SOP from [mod-103 Chapter 05](../mod-103-policy-co-authoring-with-governance/05-the-data-handling-sop.md). Four to six scenarios covering the data classes the organization has named (public, internal, confidential, restricted, regulated — whichever your taxonomy uses) and what the operator does with each when an AI tool is open.

This module is *the* module that fails Article 4 audits when it is thin. Do not shortcut it. Build the scenarios from real incident patterns if you have them (anonymized) and from the industry incident databases if you do not (AI Incident Database, OECD.AI Incidents Monitor — resources at the end of the module).

Delivery: 30–40 minutes. Scenario-based.

### Module 5 — Verification, not trust

The habit that separates a fluent operator from a brittle one. A short module on how to verify AI output against ground truth when it matters, when "it matters" applies, and what verification looks like per common output type (a draft, a summary, a classification, a citation, a line of code).

Three concrete techniques to teach in this module:

1. **The checked sentence.** If any AI-generated sentence names a fact, a number, a citation, or a person's attribution, that sentence is checked against the source before the output leaves the operator's hands. In regulated workflows, the check is logged.
2. **The compare-two-outputs technique.** For high-stakes outputs, ask the same question in two ways and compare. The divergences are where the operator's attention goes.
3. **The "would I sign this in my own name" test.** If the operator is going to put their name on an output — a client email, a memo, a report — they own the content as if they wrote it. The AI is a drafting assistant; the signature is on the operator.

Delivery: 20–30 minutes. This module is the one that correlates most strongly with reduced incident rate in post-program measurement; invest.

### Module 6 — Escalation signals and the "stop and call" list

Three to five signals per role that mean *stop and escalate*. For a service rep: a legal-sounding complaint, a mental-health signal, a refund over a threshold. For a legal reviewer: a novel contract clause, a question that requires a license to answer. For an engineer: a prompt that asks the model to help bypass a control.

The module teaches the signals and gives the operator the exact names of who to escalate to. Not a role ("your manager") — the current roster of named humans (via a link to the current roster, not embedded, because names rotate).

Delivery: 15–20 minutes.

## Total budget for the foundational curriculum

Add it up: 20 + 15 + 25 + 35 + 25 + 18 = ~130 minutes of content. In practice, after introductions, assessments, and the inevitable overrun, budget a **three-hour foundational offering** for operators. For leadership, trim the role-irrelevant modules and target 60–90 minutes.

Three hours is not a long training commitment for a professional capability that lasts a career. It is also short enough that managers will approve the calendar hold. If your foundational curriculum is longer than three hours, you are over-building; if it is shorter than 90 minutes, you are under-building for Article 4.

## Format choices

Each module has a format that fits it. Not every module is a lecture.

- **Live cohort (synchronous).** Best for Modules 3, 4, 5. The behavioral payload is highest; the discussion matters.
- **Self-paced (asynchronous).** Best for Modules 1 and 2. The content is transfer-of-information; discussion adds little.
- **Scenario workshop.** Best for Module 4 run at depth with a function-heavy cohort (e.g., a legal team or a service team) where the data-handling scenarios are specific to the function.
- **Reference card (not a module).** Module 6's escalation list, Module 2's envelope list. These are living references, not courses.

The dominant pattern at scale: **a hybrid cohort** — self-paced Modules 1 and 2 as prework, a 90–120 minute live session covering Modules 3–5, a reference-card handoff for Module 6, and an assessment at the end.

## Assessment at the foundational layer

The foundational curriculum ends with an assessment. Two layers only; the behavioral layer waits for the role-based playbook.

1. **Knowledge check** — a short, scenario-based quiz. 10–15 items. Pass bar 80%. Retake allowed. Items drawn from the real policy and the real data-handling SOP, not generic AI trivia. [Chapter 07](07-measuring-fluency-growth.md) treats item design.
2. **Open-book artifact** — a short artifact the operator produces at the end: typically a *one-paragraph summary of the acceptable-use policy in the operator's own words*. This is the most reliable test of whether Module 3 landed. Graded against a two-line rubric by the operator's manager or by the LMS auto-grader in the simple case.

The assessment is the thing an auditor reads. Design it to be *defensibly* linked to the content. A 10-item quiz that could pass without taking the course is evidence of nothing.

## Refresh cadence

Annually at minimum. Also:

- Whenever the approved-tool envelope changes (Module 2 refreshes).
- Whenever the acceptable-use policy or data-handling SOP changes (Modules 3 and 4 refresh, and the assessment regenerates from the new policy text).
- Whenever an incident surfaces a Module-6-style escalation signal that was not on the list.

Keep a short changelog at the top of each module file. "2026-09-14: added data class 'regulated-health' to Module 4 scenario set after the service-team incident." The changelog is itself the audit artifact.

## The "shadow AI" fork

Many of the operators you need in the foundational curriculum are already using AI tools outside the approved envelope. The curriculum has to acknowledge this directly or operators will tune out of the data-handling module as if it does not apply to their real workflow.

The right move: in Module 2, name shadow AI explicitly. Something like "if you are using a tool not on this list for work, that is a signal we need to hear — not something we are going to punish. There's an amnesty path: [link to the intake]." This is a policy choice co-authored with HR and governance; see [mod-103](../mod-103-policy-co-authoring-with-governance/README.md) for the posture. Without this fork, operators who are the biggest users of AI opt out of the program mentally.

## Common failures at the foundational layer

- **"What is an LLM" takes the whole program.** Module 1 is 20 minutes. If it has grown to 45, you are teaching architecture to people who need to teach themselves to verify an output.
- **The policy is paraphrased rather than taught.** Modules 3 and 4 need to be the operator-voice version of the *actual* policy, not a paraphrase that drifts. If a user cannot reconcile the training with the signed policy, the training loses.
- **The assessment is trivia.** 10 questions on who founded OpenAI is not evidence of literacy. Scenario-based items grounded in the organization's policy are.
- **The curriculum is static.** Last year's curriculum with "2026" in the header is not a refreshed curriculum.

## Where this chapter feeds

- [Chapter 04](04-role-based-playbooks-and-use-case-libraries.md) picks up each role after they have completed the foundational curriculum.
- [Chapter 05](05-the-delivery-mix.md) treats the full menu of delivery vehicles; this chapter named the ones that fit each foundational module.
- [Chapter 07](07-measuring-fluency-growth.md) builds out the assessment design this chapter leans on.
- Exercise 02 asks you to produce a detailed foundational curriculum outline.

## Summary

- Six modules: tool shape, approved-tool envelope, acceptable-use in operator voice, data-handling in scenarios, verification habits, escalation signals.
- Budget three hours of content for operators; trim to 60–90 minutes for leadership.
- Hybrid cohort is the dominant format: async prework + live session + reference handoff + assessment.
- Assessment is a scenario-based knowledge check plus an artifact (an operator-voice policy summary). Both grounded in the organization's actual policy.
- Refresh on policy, envelope, and incident triggers — not only on a calendar.
- Name shadow AI directly in Module 2 so your biggest users do not mentally opt out.
