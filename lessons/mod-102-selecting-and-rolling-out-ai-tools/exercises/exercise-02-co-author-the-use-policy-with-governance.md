# Exercise 02 — Co-Author the Use Policy with Governance

**Estimated effort:** 3 hours
**Format:** 1-2 page policy draft, Markdown
**Grounding chapters:** [03 — The Rollout Artifact Set](../03-the-rollout-artifact-set.md), [06 — Partnering with Peers on Evidence and Build](../06-partnering-with-peers-on-evidence-and-build.md)

## Objective

Write the enablement-side first draft of the use policy for a specific AI tool rollout. The draft is the thing you hand to `head-of-ai-governance` (L60), legal, and security so they can redline it — not the final document you ask them to approve. The point of the exercise is to produce something a governance partner is *happy* to react to, not one that reads like it was written past them.

## Prerequisites

- Chapters 03 and 06 read.
- A specific tool and organization in mind. Carry forward the pairing from Exercise 01 if you can — the exercise is best when the organization is already live in your head. If not, choose one of:
  - rolling out a coding assistant (e.g. Copilot-class) at the 3,000-person US bank
  - rolling out a general-purpose chat assistant (e.g. ChatGPT Enterprise-class) at the 12,000-person global pharma
  - rolling out a general-purpose chat assistant at the 500-person SaaS company

## Problem statement

Launch is in six weeks. The rollout artifact set (Chapter 03) names the use policy as *item one* — it must exist before launch, not after. `head-of-ai-governance` has 45 minutes on the calendar with you next week and has asked for "something to react to." You are not the owner of this policy. You are the co-author who writes the draft that governance, legal, and security then redline into the signed version. The full co-authoring process is in [mod-103](../../mod-103-policy-co-authoring-with-governance/README.md); this exercise is the first draft that *invites* that process.

You are not a lawyer. Legal counsel owns the legal reading of this document. Your job is to write a draft that your legal partner responds to — not to render a legal opinion.

## Requirements

Deliver a 1-2 page policy draft with exactly these sections, in this order:

1. **Scope and in-scope users** — which tool, which environments, which populations of the organization are covered by this policy.
2. **Approved uses** — named, concrete. "Summarize meeting notes you took yourself" is useful; "productivity use cases" is not. At least five.
3. **Prohibited uses** — named, concrete. At least five. Specific enough that a reader knows whether their intended use is on the list.
4. **Data classes allowed and forbidden** — map to the organization's existing data classification scheme if it has one; name the scheme you are mapping to. If no scheme exists, say so and propose the minimum classes this policy needs.
5. **The "if in doubt" default** — one sentence. What does a user do when their use case is not clearly on either list.
6. **Escalation path to governance and security** — who, how, and expected response time. Name roles, not people.
7. **Review cadence** — when this policy is re-opened, by whom, and against what inputs.

Every section of the policy must be marked with a **co-author tag** naming:

- who drafts it (you, the AI Enablement Lead)
- who redlines it (`head-of-ai-governance` L60)
- who signs the legal reading (legal counsel)
- who signs the security reading (CISO or delegate)

Not every section needs all four signatures. Make the tag honest: if security has no stake in the review cadence section, do not pretend they do.

## Starter guidance

- Chapter 03 names the use policy as the first pre-rollout artifact. Chapter 06 names the signing surface. Read both before you start — they tell you what governance will be looking for when they open your draft.
- The hardest section is **approved uses**. Vague approvals are worse than no approvals — they get stretched by users and then yanked by governance when the stretch becomes visible. Write five uses so concrete that a line manager could read them aloud in a team meeting.
- **Prohibited uses** is easier to write and easier to get wrong. The failure mode is listing things that are obviously illegal ("do not use this tool to commit fraud") and skipping the ones that are actually contested at your organization ("do not paste customer PII into prompts"). Write the contested ones.
- The **"if in doubt" default** is the most important sentence in the document. It is what a user does when policy does not cover their case. If the default is "ask your manager," the policy has pushed the decision to someone with no more information than the user. If the default is "do not use the tool," the policy has pre-decided against adoption. Pick deliberately.
- Co-author tags are not decoration. They tell the redliner which parts of the document they own and which parts they are reviewing as a courtesy. If you tag every section the same way, you have not thought about ownership.
- Do not write the policy *for* your legal partner. Write the policy that gives your legal partner the specific hooks they need to add the legal reading. For example: name the data classes, and let legal attach the retention and disclosure obligations that attach to each class.
- Where a fact about the organization is load-bearing and you do not know it (e.g. the name of the data classification scheme, the SLA for governance tickets), mark `<!-- needs-research: ... -->` inline. Do not invent.

## Deliverables

- `use-policy-draft.md`: 1-2 pages, seven sections above, co-author tags on each section.
- A short appended note (no more than 4 sentences) naming the two sections you most expect `head-of-ai-governance` to rewrite, and why. This is the note you send with the draft when you share it ahead of the 45-minute meeting.

## Acceptance criteria

- The draft fits in 1-2 pages at normal body-text size. If it spills, you are writing a policy manual, not a rollout artifact — cut.
- All seven required sections are present, in the required order.
- Approved uses and prohibited uses each have at least five named, concrete entries. No "productivity," no "misuse."
- Each section carries a co-author tag, and the tags are not uniform across sections.
- Data classes reference a named classification scheme (real or proposed).
- The "if in doubt" default is one sentence.
- No section reads as a legal opinion. Legal hooks are present; legal conclusions are not.
- `<!-- needs-research: ... -->` is used wherever an organization-specific fact is missing. No invention.
- The appended note names two sections and gives a one-sentence reason for each.

## Stretch goals

- Write the 3-sentence email that goes with the draft when you send it to `head-of-ai-governance`. Frame what you are asking for (redlines, not approval), what you are *not* asking for (sign-off), and the decision you need by the end of the 45-minute meeting.
- Add a one-paragraph "what this policy does not cover" section at the bottom and name the adjacent artifacts (incident response runbook, training materials, measurement plan) that handle what it leaves out. Point at the mod-102 chapter that owns each one.
- Sketch the redline you expect legal to make on the **prohibited uses** section — three bullets, your best guess at the language they will tighten. Do not try to be right. Try to be specific enough that you can tell afterward whether you were.

## Why this exercise matters

The use policy is the first artifact every rollout is judged against. It is also the artifact most often written *after* launch, by the wrong person, under pressure, in response to an incident. Writing a draft now — as a co-author, not as the owner, with the signing surface in view — is the move that keeps the policy ahead of the rollout instead of behind it. In the real role, you will write a draft like this every time you introduce a tool. This is the exercise where you build the muscle.
