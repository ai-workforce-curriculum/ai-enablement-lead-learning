# Exercise 01 — One-Page Acceptable-Use Policy Drill

**Estimated effort:** 2 hours
**Format:** 1–2 page policy draft, Markdown
**Grounding chapters:** [01 — The Co-Author Posture and the Redline Log](../01-the-co-author-posture-and-the-redline-log.md), [04 — The One-Page Acceptable-Use Policy](../04-the-one-page-acceptable-use-policy.md)

## Objective

Write the enablement-side first draft of the acceptable-use policy (AUP) for one specific AI tool at one specific organization. The draft is the document you hand to `head-of-ai-governance` (L60), counsel, security, and privacy so they can *redline* it — not the final policy you ask them to approve. The exercise's whole point is to produce a draft that is shaped to invite the co-authoring cycle, not to short-circuit it.

## Prerequisites

- Chapters 01 and 04 read.
- A chosen tool and organization in mind. Carry forward the pairing you used in mod-102 if you can; otherwise pick one of:
  - Rolling out a coding assistant (e.g., Copilot-class) at a 3,000-person US bank.
  - Rolling out a general-purpose chat assistant (e.g., ChatGPT Enterprise-class) at a 12,000-person global pharma.
  - Rolling out a general-purpose chat assistant at a 500-person SaaS company.
- Carry the same tool and organization forward through Exercises 02 and 03 to produce a coherent artifact set (AUP + data-handling SOP + intake questionnaire) worth keeping.

## Problem statement

Launch is in six weeks. The rollout artifact set ([mod-102 Chapter 03](../../mod-102-selecting-and-rolling-out-ai-tools/03-the-rollout-artifact-set.md)) names the AUP as item one — it must exist before launch, signed by the full co-author surface. `head-of-ai-governance` has a 45-minute walking-redline slot with you next week and has asked for "something to react to." Counsel, CISO, and the DPO are on cc.

You are not the owner of this policy; `head-of-ai-governance` is. You are the co-author who writes the draft that governance, legal, security, and privacy then redline into the signed version. The posture is [Chapter 01](../01-the-co-author-posture-and-the-redline-log.md); the shape is [Chapter 04](../04-the-one-page-acceptable-use-policy.md).

You are not a lawyer. Counsel owns the legal reading. Your job is to write a draft that *gives counsel legal hooks to attach obligations to* — not to render a legal opinion.

## Requirements

Deliver a 1–2 page AUP draft with exactly these seven sections, in this order:

1. **Scope and in-scope users** — which tool, which environments, which populations. Include contractors and consultants acting on behalf of the organization explicitly.
2. **Approved uses** — at least **five**, named, concrete. "Summarize meeting notes you took yourself" is usable; "productivity use cases" is not.
3. **Prohibited uses** — at least **five**, named, concrete. Include at least one entry on each of: sensitive data classes, external-facing output without review, high-risk decision categories (hiring, firing, credit, benefits, safety-of-life). Include the ones that are actually contested at your chosen organization.
4. **Data classes allowed and forbidden** — map to the organization's data classification scheme by name. If no scheme exists, say so and propose the minimum classes this policy needs.
5. **The "if-in-doubt" default** — **one sentence**. Pick "ask your manager" or "do not use the tool" (or your defensible variant). Append a 2-sentence justification immediately below it.
6. **Escalation path to governance and security** — named roles (not named people), channel, expected response time.
7. **Review cadence** — when the policy reopens, by whom, against what inputs.

Every section must carry a **co-author tag** naming: drafter (this role), redliner (`head-of-ai-governance` L60), legal signer (counsel), security signer (CISO or delegate), privacy signer (DPO or delegate). The tags must not be uniform across sections — demonstrate that you thought about who actually owns each section.

An **appended note** (no more than 4 sentences) at the bottom of the draft naming the two sections you most expect `head-of-ai-governance` to rewrite and why.

## Starter guidance

- Chapter 04 describes the seven sections in enough depth that your draft should not have to improvise the shape. Spend your two hours on the *content*, not the structure.
- The hardest section is **approved uses**. Vague approvals are worse than no approvals — they get stretched by users and then yanked by governance when the stretch becomes visible. Write five uses so concrete that a line manager could read them aloud at a team meeting and no operator would need to guess at the intent.
- **Prohibited uses** is easier to draft and easier to get wrong. The failure mode is listing the obvious ("do not use the tool to commit fraud") and omitting the contested ("do not paste customer PII into prompts"). Write the contested ones — they are the reason the policy exists.
- The **if-in-doubt default** is the most important sentence in the document. Do not hedge it into two sentences performing as one ("ask your manager or governance"). Pick one default deliberately and justify it in your 2-sentence justification.
- **Co-author tags are not decoration.** They tell the redliner which parts of the document they own and which parts they are reviewing as a courtesy. Uniform tags across all seven sections is a strong signal you have not thought about ownership at the section level.
- Do not write the policy *for* counsel. Write the policy that gives counsel the specific hooks they need to attach their obligations. Name the data classes; let counsel attach the retention and disclosure obligations that attach to each.
- Where a fact about the organization is load-bearing and you do not know it (the name of the data classification scheme, the SLA for governance tickets, the specific jurisdictions the tool's data crosses), mark `<!-- needs-research: ... -->` inline. Do not invent.

## Deliverables

- `use-policy-draft.md`: 1–2 pages, seven sections in the required order, co-author tags per section, appended 4-sentence note at the bottom.

## Acceptance criteria

- Fits in 1–2 pages at normal body-text size. If it spills onto page three, cut.
- All seven required sections present, in the required order.
- Approved uses and prohibited uses each have at least five named, concrete entries. No "productivity," no "misuse."
- At least one prohibited-use entry in each of the five required domains (sensitive data classes, external-facing output, high-risk decisions, etc.).
- Data classes reference a named classification scheme (real or clearly labeled as proposed).
- The if-in-doubt default is one sentence with a 2-sentence justification appended.
- Each section carries a co-author tag; tags are not uniform across sections.
- No section reads as a legal opinion. Legal hooks are present; legal conclusions are not.
- `<!-- needs-research: ... -->` is used wherever an organization-specific fact is missing. No invention.
- Appended note names two sections and gives a one-sentence reason for each.

## Stretch goals

- Write the 3-sentence email that accompanies the draft when you send it to `head-of-ai-governance`. Frame what you are asking for (redlines), what you are *not* asking for (sign-off), and the decision you need by the end of the 45-minute walking-redline slot.
- Sketch the redlines you expect **counsel** to make on prohibited uses — three bullets, your best guess at the language they will tighten or add. Do not try to be right. Try to be specific enough that after the slot you can tell whether you were.
- Propose a review-cycle calendar for the next 12 months: ratification date, first review window, trigger events (incidents, regulator guidance, major tool updates) that would open a mid-cycle review.

## Why this exercise matters

The AUP is the first artifact every rollout is judged against. It is also the artifact most often written *after* launch, by the wrong author, under pressure, in response to an incident. Writing a draft now — as a co-author, not as the owner, with the full signing surface in view — is the move that keeps policy ahead of the rollout instead of behind it. In the real role, you will write a draft like this every time you introduce a tool. This is the exercise where you build the muscle; Exercises 02 and 03 build the two artifacts that sit next to it.
