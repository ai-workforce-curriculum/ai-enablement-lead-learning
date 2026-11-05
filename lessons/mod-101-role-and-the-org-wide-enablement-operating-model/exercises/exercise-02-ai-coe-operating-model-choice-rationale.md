# Exercise 02 — AI CoE Operating Model Choice & Rationale

**Estimated effort:** 2.5 hours
**Format:** 1-page decision memo + 1-page sketch of the CoE shape
**Grounding chapters:** [02 — The AI CoE Pattern Family](../02-the-ai-coe-pattern-family.md), [03 — Authoring the Enablement Operating Model](../03-authoring-the-enablement-operating-model.md)

## Objective

Pick one of the four AI CoE shapes — hub, hub-and-spoke, federated, or embedded — for a specific organization and defend the choice in a short decision memo your executive sponsor could sign.

The point is **defensible rationale**, not "the right answer." Each of the four shapes is right for some organization. Your job is to name the organizational facts your choice follows from.

## Prerequisites

- Chapters 02 and 03 read.
- A chosen organization (the same one you used in Exercise 01, or a new one — your call).
- A rough mental model of the organization's size, BU autonomy, regulatory posture, and AI maturity.

## Problem statement

Your executive sponsor has asked, "Which CoE shape will we run?" They want a decision memo they can take to the executive team. Going in without a choice is not an option; going in with the wrong rationale (bias, cargo-cult, "everyone else is doing hub-and-spoke") will not survive the room.

## Requirements

### Part A — The decision memo (one page)

Structure:

1. **Recommendation** — one sentence. "Recommend `<shape>` for `<organization>` because `<the single strongest reason>`."
2. **Organizational facts the choice follows from** — four to six specific facts about the organization, each tied to a rationale. Examples of the *shape* of a fact: "the organization operates under two different market regulators (FINRA in the US, FCA in the UK) across two business units"; not "we are heavily regulated."
3. **What this choice makes easy** — three bullets.
4. **What this choice makes hard** — three bullets. If you cannot write three, you have not thought hard enough.
5. **Alternatives considered and why rejected** — one line each for the three shapes you did *not* pick.
6. **The six-month revisit** — one line naming the condition under which you would re-open the choice.

### Part B — The sketch (one page)

A simple diagram (drawn, ASCII, mermaid, whatever your preferred medium) showing the shape in place at the organization. It should identify:

- The CoE (hub) and its headcount estimate.
- The spokes (if any), and where they sit — which BU, reporting to whom.
- The executive sponsor and the governance partner.
- The flow of a typical intake (one arrow, one label).

Keep it readable at a glance. If you need a legend longer than three lines, redraw.

## Starter guidance

- Three facts matter most: size, BU autonomy, regulatory posture. A fourth, AI maturity, often shifts the answer from one shape to the next most-adjacent shape.
- Watch for the biases named in Chapter 02: consulting-style bias toward hub (it slides well), BU-leader bias toward federated (it preserves autonomy). Your memo should pre-empt both.
- If your choice is hub-and-spoke, name the spoke roles explicitly. If you cannot staff them, the choice is wrong.
- If your choice is federated, name the central-coordination roles explicitly. Even a thin center has some headcount.
- If your choice is embedded, say what *makes* it embedded — which existing roles pick up the enablement responsibilities. If the answer is "everyone and no one," you don't have an operating model.

## Deliverables

- `coe-shape-decision-memo.md` — the one-page memo above.
- `coe-shape-sketch.*` — the one-page diagram (any format your reviewer can open).

## Acceptance criteria

- The memo fits on one page at body-text size.
- Every "organizational fact" is a *fact*, not an adjective. Facts can be checked.
- The "what this makes hard" bullets are not platitudes; they are specific to your shape and organization (e.g., for a hub-and-spoke choice at a global pharma: "spoke reporting lines are dotted into the CoE and solid into the BU — accountability for cross-BU coordination will degrade unless we fund a quarterly operating ritual").
- The sketch is understandable without the memo. The memo is understandable without the sketch.
- You have *not* copied this chapter's decision factors verbatim. You have applied them to your organization.

## Stretch goals

- Build a **second** version of the memo with a different shape than you recommended. Use it as the "alternative" section of your primary memo and note where the two memos actually disagree on fact (as opposed to disagreeing on weight).
- Add a two-paragraph section on **funding model** (central vs. BU vs. hybrid). This belongs in the full operating-model doc, but even a short note here surfaces whether the CoE is deliverable at the funding level the shape implies.
- Stress-test the sketch: write the one scenario — a new regulator, a new BU acquisition, a flagship rollout — under which your sketch has to redraw. If none of the three breaks it, you have probably over-abstracted.

## Why this exercise matters

Most AI CoE missteps in the market are not failures of execution; they are failures of shape. An organization that should have been federated runs a hub and starves the BUs of local capacity. An organization that should have been hub-and-spoke runs embedded and has no one to answer regulators. Writing the shape choice down, with the facts, is the thing that protects against the failure.
