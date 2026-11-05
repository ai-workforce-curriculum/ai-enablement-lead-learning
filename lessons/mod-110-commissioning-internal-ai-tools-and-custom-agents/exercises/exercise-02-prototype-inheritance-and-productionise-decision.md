# Exercise 02 — Prototype Inheritance and Productionise Decision

**Estimated effort:** 3 hours
**Format:** productionize-worthiness assessment + recommendation + no-go memo (if applicable), Markdown
**Grounding chapters:** [03 — Inheriting Prototypes and the Honest No-Go](../03-inheriting-prototypes-and-the-honest-no-go.md); [01 — The Commissioner Stance — Not the Builder](../01-the-commissioner-stance-not-the-builder.md). Prior reading: [mod-103 Chapter 05](../../mod-103-policy-co-authoring-with-governance/05-the-data-handling-sop.md); [mod-107 Chapter 03](../../mod-107-budget-roi-and-build-vs-buy-at-org-scope/03-the-build-vs-buy-matrix-at-enterprise-scope.md).

## Objective

Produce the productionize-worthiness assessment for a prototype that has arrived on your desk asking to graduate to production. The assessment runs the five dimensions from Chapter 03; the output is a specific recommendation — **productionise**, **rebuild from brief**, or **no-go** — with the artefact that corresponds to the recommendation attached. If the recommendation is no-go, the five-section honest-no-go memo is the deliverable. If the recommendation is productionise or rebuild, the cover note names the brief revisions Exercise 01's brief requires to accommodate the recommendation.

The exercise carries the organisation from Exercise 01 but introduces a specific prototype inheritance scenario that may or may not map to the commission you wrote. Half the exercise's teaching value is in recognising when a prototype does not fit a commission that is otherwise on the roadmap.

## Prerequisites

- Chapter 03 read.
- Chapter 01 re-read, specifically the three postures section.
- Exercise 01 complete (you have a signed brief or a ready-to-sign brief for your chosen organisation).
- [mod-103 Chapter 05](../../mod-103-policy-co-authoring-with-governance/05-the-data-handling-sop.md) read as the data-posture ground truth.
- [mod-107 Chapter 03](../../mod-107-budget-roi-and-build-vs-buy-at-org-scope/03-the-build-vs-buy-matrix-at-enterprise-scope.md) re-read as the Column 4 TCO envelope the prototype's cost shape is assessed against.

## Problem statement

A prototype has arrived on your desk in your chosen organisation. Pick the provenance scenario that creates the most interesting assessment against the organisation you chose in Exercise 01 — one of the three patterns from Chapter 03:

1. **Billable-consultant prototype (the ClearView pattern).** A consulting firm finished a three-month engagement and left behind a working prototype. The prototype is in daily use by a specific team the consulting firm advised. The firm's partner has offered to productionise it on a monthly retainer, or alternatively to transfer it to the organisation's engineering team. Specifics you make up (and flag as simulated): the prototype's stack (model provider, retrieval pattern, deployment surface), the data classes it touches, the current operating cost, and the documentation state.

2. **Business-user prototype (the shadow-IT pattern).** A business user (a product analyst, an operations lead, or a specialist who built on their own time) has produced a prototype in a low-code agent-builder on an individual-license tier. The prototype's user cohort is twelve people on the same team; the business user is a trained operator whose champion status is uncontested. The prototype is loved by the team and invisible to IT. The business user wants the enablement program to adopt it; IT identity wants to know how it gets on the organisation's SSO.

3. **Hackathon prototype (the executive-sponsorship pattern).** A hackathon team at the organisation's innovation day built a prototype that the CEO saw at the showcase. The CEO has emailed the head of engineering asking when it ships. The hackathon team has disbanded; the lead engineer on the team is on parental leave; no maintenance owner has volunteered. The prototype's provenance and stack are known but the team's follow-up has been thin.

Pick one of the three. Specify the prototype's operating details (stack, data classes, cost, documentation state, support footprint) in a simulated form — flag the specifics as simulated, do not invent organisational facts.

## Requirements

### Part A — The productionize-worthiness assessment

A Markdown document with five dimension sections, each with a score (**pass**, **concerns**, **fail**) and a one-sentence read. Per Chapter 03:

- **Dimension 1 — Problem fit.** Does the prototype solve a problem that passes the Chapter 01 one-paragraph test? Specifically: workflow-step problem, envelope checked, user cohort real at scale, outcome measurable on the mod-106 framework.
- **Dimension 2 — Data posture.** Does the data flow pass [mod-103 Chapter 05](../../mod-103-policy-co-authoring-with-governance/05-the-data-handling-sop.md)? Data classes known, SSO respected, retention windows acceptable, no exfiltration to unauthorised model providers.
- **Dimension 3 — Operational fit.** Support channel, champion network, kill-switch runbook, logging surface, documentation.
- **Dimension 4 — Cost shape.** Steady-state cost within the mod-107 Chapter 03 Column 4 TCO envelope, or triggers a return to the matrix.
- **Dimension 5 — Maintenance fit.** Named maintenance owner, skills match, dated commitment, scope, on-call expectation.

For each dimension, list the specific evidence you used (what you looked at or would need to look at to call it). The evidence is what makes the assessment auditable — a dimension scored without stated evidence is a judgment call hiding as an assessment.

### Part B — The recommendation

A one-page Markdown document naming one of three recommendations with the reasoning:

- **Productionise** — all five dimensions pass. The prototype inherits Exercise 01's brief as a productionisation brief (Chapter 03's productionise outcome). Name the specific brief revisions Section 1 and Section 7 require to reflect the inheritance.
- **Rebuild from brief** — problem fit passes, one or more structural dimensions fail. The prototype is an input to Section 1's baseline and to Section 3's performance baseline but not to the build itself. Name which dimensions failed structurally and why rebuild is the correct response.
- **No-go** — problem fit fails, or multiple structural dimensions fail in a way that cannot be rebuilt into the standing operating surface. Author the honest-no-go memo (Part C).

The recommendation is the commissioner's call, defended with the assessment evidence.

### Part C — The honest no-go memo (if the recommendation is no-go)

If Part B's recommendation is no-go, author the five-section memo from Chapter 03:

1. What the prototype did — credit the maker, name the problem it solves and the cohort it served.
2. What the productionize-worthiness assessment found — the five dimensions with the specific failures.
3. Why rebuild-from-brief is not the recommendation either — the dimensions where rebuild would still fail.
4. What happens to the prototype — the team's continued use, the policy routing if a violation exists, the specific non-interventions.
5. What the next commission in this problem space would look like — the direction a right commission would take.

If the recommendation is productionise or rebuild, replace Part C with a one-page cover note naming the brief revisions and the maintenance-owner conversation required to proceed.

## Starter guidance

- The dimensions are not independent. A prototype that fails Dimension 2 (data posture) often fails Dimension 3 (operational fit) for the same underlying reason — it was built outside the organisation's managed surface. Do not count the same failure twice in the composite read.
- The Chapter 01 one-paragraph test is a precondition for Dimension 1. If the problem fit question is "does the prototype solve a real problem," you are at the wrong altitude — the right question is "does the prototype solve a problem at the altitude a commissioning brief would name it at?" Many prototypes fail this question because the problem is a persona-of-one in the user cohort rather than an organisational pattern.
- The hardest recommendation to defend is **rebuild from brief**. It implicitly says the prototype's value is in demonstrating the problem is solvable, not in the specific solution. Write the rebuild recommendation explicitly as a credit to the prototype-maker and a redirect of their work into the pilot-cohort champion role from [mod-105 Chapter 03](../../mod-105-champion-networks-and-change-management/03-routing-field-signal-back-to-policy-tooling-and-training.md).
- The hardest no-go memo is written against stakeholder resistance. The memo's Section 1 is what keeps the memo from reading as dismissive — credit the maker specifically, in their own vocabulary, before the assessment lands.
- For the billable-consultant scenario, note that the consulting firm's retainer offer is a [mod-107 Chapter 04](../../mod-107-budget-roi-and-build-vs-buy-at-org-scope/04-partnering-with-procurement-finance-and-it.md) vendor contract, not a maintenance commitment inside the enablement program. The assessment sometimes concludes "this is not a commission at all — route to Procurement" rather than any of the three Chapter 03 outcomes. If that is your conclusion, write it as a fourth, meta-recommendation and justify.
- Where an organisational fact you need is unknown (specific policy document names, specific cost-model numbers, specific baseline readings), use `<!-- needs-research: ... -->` inline.

## Deliverables

- `productionize-worthiness-assessment.md` — the five-dimension assessment with evidence.
- `recommendation.md` — the one-page recommendation.
- `no-go-memo.md` **or** `revision-cover-note.md` — depending on the recommendation.
- A short cover note (3–5 sentences) summarising the dimension you found hardest to score and the Chapter 01 posture you most actively guarded against — this exercise most often tests apologist posture (defending an orphan prototype against evidence).

## Acceptance criteria

- The assessment has all five dimensions with a score and a stated evidence basis per dimension.
- The recommendation is one of three (productionise, rebuild from brief, no-go) and is defended against the assessment, not against stakeholder preference.
- If no-go: the memo has all five Chapter 03 sections, Section 1 credits the maker specifically, Section 5 names the direction a right commission would take.
- If productionise or rebuild: the cover note names the specific brief revisions and the maintenance-owner conversation required.
- The composite read does not double-count underlying failures across dimensions.
- `<!-- needs-research: ... -->` is used wherever an organisational fact is missing.

## Stretch goals

- Author a **second provenance scenario** from the list of three and run the assessment on it. Running the drill twice against the same organisation sharpens the signal from the specific provenance pattern to the repeatable assessment discipline.
- Draft the **stakeholder-communication plan** for the recommendation — who hears what, in what order, on what channel. For a no-go, this is the specific sequence (maker first, exec sponsor second, governance third, user cohort fourth) that keeps the decision from leaking as speculation.
- Add a **retrospective section** to the assessment memo — one page — naming the two or three organisational practices (vendor contracts, hackathon aftercare, shadow-IT discovery) whose change would reduce the rate at which orphan prototypes reach your desk. This is the close-the-loop input Chapter 03 leans into without writing.

## Why this exercise matters

The honest no-go is the recommendation this chapter exists to make possible. Running the assessment under stakeholder pressure — the consultant who wants the retainer, the business user who built the tool themselves, the exec sponsor who told the CEO it ships this quarter — is the specific discipline this exercise rehearses. The productionize-worthiness assessment is the audit surface the recommendation lives or dies on; running it under a three-hour budget is calibration for running it when the stakeholder meeting is on the calendar tomorrow and the prototype's advocates are ready to defend it.
