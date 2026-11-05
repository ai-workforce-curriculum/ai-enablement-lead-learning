# Exercise 02 — Vendor Vetting and Certification Rubric

**Estimated effort:** 3 hours
**Format:** vendor portfolio instrument + archetype-specific certification rubric + one worked certification record, Markdown
**Grounding chapter:** [04 — Vendor and External-Partner Management](../04-vendor-and-external-partner-management.md). Prior reading: [mod-107 Chapter 06](../../mod-107-budget-roi-and-build-vs-buy-at-org-scope/06-the-vendor-vetting-rubric.md); [mod-107 Chapter 04](../../mod-107-budget-roi-and-build-vs-buy-at-org-scope/04-partnering-with-procurement-finance-and-it.md).

## Objective

Populate the vendor portfolio instrument with the chosen organisation's current set of AI-adjacent vendors, author the archetype-specific certification rubric at full depth, and produce one certification record at operating depth. The output is a bundle the quarterly portfolio review ([Chapter 04](../04-vendor-and-external-partner-management.md)) could run against on the day it is submitted.

You carry the same organisation across Exercises 01, 02, 03, and 04. Build on Exercise 01's catalog — the vendors you populate here plug into the catalog slots you specified there.

## Prerequisites

- [Chapter 04](../04-vendor-and-external-partner-management.md) read.
- [mod-107 Chapter 06](../../mod-107-budget-roi-and-build-vs-buy-at-org-scope/06-the-vendor-vetting-rubric.md) read as the upstream vendor-vetting rubric this exercise extends to operating cadence.
- [mod-107 Chapter 04](../../mod-107-budget-roi-and-build-vs-buy-at-org-scope/04-partnering-with-procurement-finance-and-it.md) read as the procurement / finance partnership context.
- Your Exercise 01 service catalog in hand — the catalog slots are what the vendor portfolio plugs into.

## Problem statement

Your CoE has been running for three cycles. The portfolio accreted — a primary tooling vendor contract was signed, a training-production agency was brought on for the role-based playbooks, a change-management consultancy was engaged for the first regulated-BU rollout, and three external AI experts have been consulted over the year. Procurement has been managing contracts; the enablement bar on the vendors has been informal. The quarterly portfolio review is in four weeks and the CoE has to walk into it with a real portfolio instrument, real archetype-specific rubrics, and real certification records.

Write the portfolio as if the CoE's operations analyst will own the weekly read and the quarterly review will convene in a month. The lead's name and the operations analyst's name belong on every record they sign; the vendors' named counterparts have to be real roles your organisation can staff.

## Requirements

### Part A — The vendor portfolio instrument

A single Markdown document that populates the portfolio with 6–10 vendors across all four archetypes. Required for each vendor:

- **Vendor ID.** Durable identifier.
- **Vendor name.** If you are inventing a vendor for the exercise (allowed for the consultancy and the external experts), prefix with `[fictional]` so the reader knows.
- **Archetype.** One of the four from [Chapter 04](../04-vendor-and-external-partner-management.md).
- **Current engagement.** SOW, retainer, or licence with start and end dates (invent plausible dates), scope in one sentence.
- **Catalog slot(s).** Which of your Exercise 01 catalog slots the vendor plugs into.
- **Certification status.** Current / under review / lapsed, with date of last review.
- **Delivery history.** One line summarising any prior misses or notable wins.
- **Risk-register items.** One line referencing any open items (for the exercise, you can invent 1–2 plausible items per two vendors).
- **Named counterpart.** The specific role at the vendor the CoE talks to — a name is not required for the exercise; the role title is.
- **Contract hygiene.** DPA signed, SOC 2 current, model-provenance terms clear, data-residency terms satisfied, AI-specific clauses negotiated — yes / no / in progress for each.

Open the portfolio document with a one-paragraph preface naming:

- The portfolio concentration posture (how much reliance on any one vendor is tolerable, by archetype).
- The portfolio's total cost against the enablement cost model from [mod-107 Chapter 01](../../mod-107-budget-roi-and-build-vs-buy-at-org-scope/01-the-enablement-cost-model-at-org-scope.md).
- The quarterly review cadence.

### Part B — The archetype-specific certification rubric

A Markdown document with four rubrics — one per archetype — each at operating depth. For each archetype:

- **The named criteria** (four for each archetype from [Chapter 04](../04-vendor-and-external-partner-management.md)).
- **For each criterion:** the specific evidence the CoE requires (a cited deliverable, a session attendance record, a dissent entry, a field-report fold-back memo, a conflict declaration). "The vendor must demonstrate X" is not enough; name the artefact the certification record will cite.
- **The certification period** — annual, per-engagement, or something else; with rationale.
- **The lapse conditions** — what specific failures trigger a move from current to under-review, and from under-review to lapsed.
- **The remediation path** — the specific steps a lapsed vendor takes to recover certification.

Treat the rubric as the operational surface — not the aspirational description of what a certified vendor looks like. A rubric that cannot be run by the operations analyst is a rubric that is decorative.

### Part C — One worked certification record

Pick one vendor from your portfolio. Produce the full one-page certification record as specified in [Chapter 04](../04-vendor-and-external-partner-management.md):

- **Vendor, archetype, scope of certification.**
- **The named criteria that apply to this archetype.**
- **The evidence satisfying each criterion** — cited specifically. For the exercise, invent plausible evidence (a specific session date, a specific decision-log entry ID, a specific field-report fold-back memo) but make the citation shape realistic.
- **The certification period** and **the renewal date.**
- **Signed by** the enablement lead (your name or a placeholder) and the vendor's named counterpart (role title at least).

The record must stand on its own — a certification record whose evidence citations the reader cannot verify (because the citations are generic placeholders) is a record that fails its own operational test. Specific evidence, even if invented for the exercise, makes the record testable.

## Starter guidance

- Pick the four archetypes deliberately. The primary tooling vendor is usually the easiest (an obvious commercial product). The training-production agency is sometimes a dotted-line relationship with internal L&D — if the chosen organisation prefers in-house to agency delivery, name the shape and still write the rubric. The consultancy is usually engagement-shaped; pick a plausible engagement that matches the chosen organisation's recent history. The external AI experts are often a short list of academic affiliates, boutique practitioners, or regulatory-specialist consultants — invent two.
- The hardest rubric to write is usually the consultancy's. The brief-shaped authority discipline is the specific criterion that often has no prior evidence surface in the organisation's existing vendor practice. If your chosen organisation has a strong consulting history, the rubric will bite there specifically.
- For the ed-tech vendor option (2,500 people, FERPA / COPPA regime), the external AI expert archetype often includes industry regulatory specialists. The conflict declaration criterion is the one to watch — expert networks in regulated industries often carry concurrent vendor relationships.
- For the bank option (12,000 people, SR 11-7 regime), the model-provenance contract clause is the specific line that regulators will cite in an audit. The rubric's evidence requirement should make this specific, not generic.
- Where an organisational fact you need is unknown, use `<!-- needs-research: ... -->` inline. Do not invent SOC 2 attestations or model-provenance clauses — reference them as needs-research if you do not have them.

## Deliverables

- `vendor-portfolio.md` — the portfolio instrument with 6–10 vendors and the one-paragraph preface.
- `certification-rubric.md` — the archetype-specific rubric with criteria, evidence, lapse conditions, and remediation paths.
- `worked-certification-record.md` — the one full certification record for the chosen vendor.
- A short cover note (3–5 sentences) summarising the archetype you found hardest to write a rubric for and the one certification record you most wanted to push to under-review status.

## Acceptance criteria

- The portfolio has 6–10 vendors across all four archetypes; no archetype is empty.
- Each portfolio record is complete across all specified fields; missing contract-hygiene items are tagged `<!-- needs-research: ... -->` rather than left blank.
- The certification rubric covers all four archetypes with named criteria, specific evidence, lapse conditions, and remediation paths.
- The worked certification record cites evidence specifically (a dated session, a specific decision-log entry, a specific memo). Generic placeholders are not acceptance-worthy.
- Each certification record names the enablement lead signatory and the vendor counterpart role; "signed by TBD" is not a signed record.
- The portfolio's cost rollup is consistent with the cost model line items from your Exercise 01 catalog's preface.
- `<!-- needs-research: ... -->` is used wherever an organisational fact is missing.

## Stretch goals

- **Author a lapse case.** Pick one vendor from the portfolio and walk the three-state discipline through a specific triggering event — the SOC 2 renewal gap, the consultancy's unlogged dissent, the agency's missed field-signal fold-back. Three pages: the triggering event, the move from current to under-review, the remediation plan with named dates, the lapse call if remediation fails, and the exit path.
- **Produce the quarterly portfolio review's output page** — the one-page artefact that would feed the Chapter 05 exec review (Surface 2) and the AI council (Surface 1). Draft against the portfolio you authored; cite specific risks, specific renewals, and specific concentration asks.
- **Produce a one-page "vendor-training content outline"** for the primary tooling vendor. The four content areas from [Chapter 04](../04-vendor-and-external-partner-management.md) with the organisation-specific policy citations, the organisation's rollout artefact set references, the measurement framework specific to the organisation, and the incident path specific to the organisation.

## Why this exercise matters

Vendors are inherited. By the time the CoE is operating at steady state, the portfolio is real — a contract was signed, an agency was engaged, a consultant was embedded — and the enablement bar has to be made operational, not aspirational. The portfolio instrument, the archetype-specific rubric, and the worked certification record are what move the enablement bar from "the lead holds it in their head" to "the operations analyst can enforce it in practice." Producing all three under a three-hour budget is calibration for producing them against a live portfolio whose vendors have been operating informally for a year and whose first certification review is going to surface uncomfortable gaps.
