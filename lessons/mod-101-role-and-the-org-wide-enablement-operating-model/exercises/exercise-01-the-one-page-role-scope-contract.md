# Exercise 01 — The One-Page Role Scope Contract

**Estimated effort:** 2 hours
**Format:** one page of written artifact, Markdown or docx
**Grounding chapters:** [01 — The Level-45 Role and Its Scope Contract](../01-the-level-45-role-and-its-scope-contract.md)

## Objective

Write the one-page scope contract you would sign on day 30 of a new AI Enablement Lead role at a specific, realistic organization. The contract must be:

- *Short* — one page, not a job description.
- *Specific* — about this organization, not a template.
- *Defensible* — every line of "does not own" points to the role that does.

## Prerequisites

- Chapter 01 read.
- A clear picture — real or realistic — of one organization you will write the contract for. If you do not have a real one in front of you, pick one of:
  - a 3,000-person US bank with an existing head of AI governance and no CoE yet
  - a 12,000-person global pharma with an active CAIO and a mature governance program
  - a 500-person SaaS company with no governance function and a CAIO who is really the CTO wearing a second hat

## Problem statement

You have just accepted the AI Enablement Lead role at the chosen organization. Your boss's boss has asked for "the one-pager that describes what you'll own and what you won't" before signing off on your hiring approval. You have the weekend.

## Requirements

Deliver a single page with the five sections named in Chapter 01:

1. **What this role owns** — bulleted, specific to the organization.
2. **What this role does not own** — bulleted, with each line naming the role or function that *does* own it.
3. **RACI on five decisions** — a tiny table (one row per decision) across you, the BU, governance, security, and executive sponsor. Choose the five decisions that matter most for your organization.
4. **Decisions this role makes unilaterally** — three to five.
5. **Decisions this role escalates** — three to five, naming who they escalate to.

## Starter guidance

- The "does not own" section is the hardest. Fight the instinct to leave it vague. "This role does not own policy ownership (→ `head-of-ai-governance`)" is useful; "this role does not own policy" is not.
- Your five RACI decisions should be the ones you expect to be fought over in month one. For a bank, "approve a tool for pilot use on customer data" probably makes the cut. For a SaaS company, it probably doesn't.
- The unilateral decisions and the escalations should not overlap. If a decision is in both lists, you have not actually made the call.
- Resist the urge to describe *how* the role will do things. The contract is about *what*, not *how*; the operating model (Exercise 02 of [mod-102](../../mod-102-selecting-and-rolling-out-ai-tools/README.md), and later chapters) handles *how*.

## Deliverables

- `role-scope-contract.md` (or `.docx`): one page, five sections above.
- A short appended note (no more than 3 sentences) naming which one of the three bullet-pointed decisions you expect to be most contested in the signing conversation, and why.

## Acceptance criteria

- The contract is one page at normal body-text size. If it spills onto two, you are describing a job, not a contract — cut.
- Every line of "does not own" names the role or function that owns it.
- The RACI table is five rows (give or take one) with a single decider per row.
- The organization-specific detail is visible. A reader who knows your chosen organization should be able to tell you wrote this *for them*.
- Appendix: the "most contested decision" note is three sentences or fewer.

## Stretch goals

- Write a 100-word *opening paragraph* for the contract — the first thing your boss's boss reads. Frame the role in one sentence, the organization in one sentence, and the first 90-day outcome in one sentence.
- Pick one line from "does not own" and sketch — three bullets — what the handoff to the owning role looks like in practice. (You will build this out more fully in Exercise 03.)
- Compare your contract to the plain reading of a real posted AI Enablement Lead JD (the organization's or anyone's). Note the three biggest divergences and whether your contract or the JD is right in each case.

## Why this exercise matters

The scope contract is the first artifact of the role. It is the thing you will point at when the fifth person this quarter tries to hand you work that is not yours. Writing it as an exercise, under no pressure, gives you a template you can adapt when you are three weeks into a real role and the pressure is on.
