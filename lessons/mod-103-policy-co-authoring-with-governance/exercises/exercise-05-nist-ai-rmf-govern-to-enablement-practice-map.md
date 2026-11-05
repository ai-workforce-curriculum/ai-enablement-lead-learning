# Exercise 05 — NIST AI RMF GOVERN → Enablement Practice Map

**Estimated effort:** 2–3 hours
**Format:** mapping table (2 pages) + 1-page memo, Markdown
**Grounding chapters:** [03 — NIST AI RMF GOVERN and ISO/IEC 42001 for the Enablement Seat](../03-nist-ai-rmf-govern-and-iso-iec-42001-for-the-enablement-seat.md), [07 — What You Route Out](../07-what-you-route-out-counsel-soc-architect.md)

## Objective

Produce the one-artifact answer to the governance-partner question "which pieces of your enablement operating model evidence which parts of our standards?" The deliverable is a **mapping table** of the enablement-side artifacts to the NIST AI RMF GOVERN categories and ISO/IEC 42001 clauses they feed, paired with a **1-page memo** that flags two places where the enablement artifacts do not yet map cleanly and proposes what would need to change — in enablement practice, not in the standard.

This is the mapping artifact `head-of-ai-governance` (L60) and `senior-ai-governance-architect` (L50) will ask you for inside the first three months of any real role. Do the exercise in a standalone slot — unlike Exercises 01–04, this one does not require a carried-forward tool or organization.

## Prerequisites

- Chapter 03 read.
- Chapter 07 read (so the "no standard rewrites, no control-library redesigns" guardrail is fresh).
- Skim access to the module READMEs for mod-101, mod-102, mod-104, mod-105, mod-106, mod-109 — the mapping references artifacts from across the track.

## Problem statement

The organization is scheduled for an ISO/IEC 42001 pre-certification readiness review in six weeks and for a cross-mapping exercise with the US-side NIST AI RMF implementation in eight. `head-of-ai-governance` and `senior-ai-governance-architect` have asked each cross-functional lead to produce a one-page view of "which of your artifacts evidence which parts of the standards we are certifying against."

Your job is to produce that view for the enablement-side artifacts. The architect owns the control-library mapping; you own the operating-model view of which practice produces which evidence.

The constraint from Chapter 07: you do **not** propose standard rewrites. You do **not** propose control-library redesigns. You surface enablement-practice changes that would close the gaps you have surfaced.

## Requirements

### Deliverable A — the mapping table

A table with at least **eight rows** and these columns:

| Artifact | Primary NIST AI RMF GOVERN category | Primary ISO/IEC 42001 clause(s) | Evidence this role produces | Owner on the standards side |
|----------|-------------------------------------|-------------------------------|-----------------------------|-----------------------------|

Rows must cover (at a minimum) these eight artifacts:

- Acceptable-use policy (mod-103 Chapter 04).
- Data-handling SOP (mod-103 Chapter 05).
- Intake questionnaire (mod-103 Chapter 06).
- Training rosters (mod-104).
- Champion network (mod-105).
- Executive scorecard (mod-106).
- Kill-switch and rollback plan (mod-102 artifact 7 / operated by mod-109).
- Redline log (mod-103 Chapter 01).

Add additional rows if you want (90-day entry plan from mod-101, pilot charter from mod-102, incident after-action from mod-109, etc.) — eight is the minimum, not a cap.

Column rules:

- **NIST AI RMF GOVERN category**: name the function (GOVERN) and the category family at orientation level (roles & responsibilities, policies/processes/procedures, workforce competence, third-party risk, information integrity, DEI). Use `<!-- needs-research: confirm exact GOVERN sub-category ID -->` if you want to quote a specific sub-category ID (GOVERN 1.1, GOVERN 5.2, etc.) and are not certain of the number. Do not invent sub-category IDs.
- **ISO/IEC 42001 clause(s)**: name the clause family with confidence (Clause 5 Leadership, Clause 6 Planning, Clause 7 Support — 7.2 Competence, 7.3 Awareness, 7.5 Documented information, etc.). Mark `needs-research` on Annex A control IDs you quote.
- **Evidence this role produces**: a concrete artifact — "ratified AUP + redline log," "annual training completion roster per role tier," "monthly council pre-read packet" — not a generic noun like "policy documentation."
- **Owner on the standards side**: name the specific role — `senior-ai-governance-architect` (L50), `head-of-ai-governance` (L60), or this role. Where the architect is accountable for the control design and this role is accountable for the evidence operation, say both and distinguish.

### Deliverable B — the gaps memo

A 1-page memo, addressed to `head-of-ai-governance` (L60) and `senior-ai-governance-architect` (L50) as intended readers, naming **two places** where the current enablement artifacts do not yet map cleanly to a standard category or clause, with a 2-sentence proposed change in enablement practice for each gap.

For each gap:

- 2 sentences describing the gap — what the standard requires or expects, which enablement artifact would normally evidence it, why the current artifact falls short.
- 2 sentences proposing a change in **enablement practice** — a new record kept, a revised cadence, a new section in an existing artifact, a role-based reporting split. **Not** a proposed standard rewrite. **Not** a proposed control-library redesign.

Close with one sentence that explicitly frames the memo as "operating-model recommendations for governance consideration" — not as decisions.

## Starter guidance

- Chapter 03 names the functions (GOVERN / MAP / MEASURE / MANAGE) and the 42001 clauses that touch enablement (Clauses 5, 6, 7 — especially 7.2 and 7.3) with confidence. Use those confidently; use `needs-research` for the exact sub-category or sub-clause IDs.
- Think from the auditor's seat. An auditor walks in and asks "show me how your organization evidences GOVERN workforce-competence." The evidence this role produces column should answer that question in one artifact, not three.
- The ** DEI / information-integrity** rows are often where the gaps live — the acceptable-use policy and the data-handling SOP cover most of the policy categories cleanly, but DEI and transparency often have no natural home in the current enablement artifact set. Those are good gap candidates.
- The "owner on the standards side" column is the discipline test. If every row lists this role as the owner, you have drifted into architecture. The architect owns the control design; you own the evidence operation. Both names belong on most rows, with the distinction made clear.
- The **gaps memo is the exercise's judgment test.** The failure mode is proposing standard rewrites ("GOVERN should add a sub-category for X") or control-library redesigns ("the control mapping should move Y to Z"). Those are not your proposals to make. Rewrite until each gap's proposed change is unambiguously a change to enablement practice.
- Where you do not know the exact 42001 clause number or the exact GOVERN sub-category ID, mark `<!-- needs-research: ... -->`. Do not invent numbers.
- Do not propose EU AI Act article-level changes in this exercise. The AI Act is the regulatory floor, not a management standard the enablement seat maps against directly — though it does show up in stretch goals.

## Deliverables

- `standards-mapping-table.md`: table with at least eight rows and the five required columns.
- `standards-mapping-gaps-memo.md`: 1-page memo naming two gaps with enablement-practice proposals.

## Acceptance criteria

- Both artifacts present.
- Table has at least eight rows, covers the eight required artifacts, and uses the five required columns.
- Every row names the NIST GOVERN category family (not just "GOVERN").
- Every row names an ISO/IEC 42001 clause family with confidence; sub-clause IDs and Annex A control IDs quoted are either verified or marked `needs-research`.
- "Evidence" column names a concrete artifact per row.
- "Owner" column is specific to a role; where the architect designs and this role operates, both are named with the distinction clear.
- No row lists this role as the sole owner of a control design.
- Memo fits on one page.
- Memo surfaces exactly two gaps with the required 2 + 2 sentence structure.
- Both gap proposals are changes in **enablement practice** — new records, revised cadences, new artifact sections, reporting splits. No standard rewrites. No control-library redesigns.
- Memo closes with one sentence explicitly framing the recommendations as "for governance consideration."
- `<!-- needs-research: ... -->` used wherever specific sub-category or sub-clause IDs are quoted without verification.

## Stretch goals

- Add a third standard column referencing **EU AI Act** articles relevant to each artifact — Article 4 (AI literacy) for training rosters, Article 50 (transparency) for AUP and operator communication, Article 73 (serious incident reporting) for kill-switch and incident after-action, Chapter III (high-risk system obligations) where applicable. Mark `needs-research` on article numbers beyond those four.
- Sketch which rows would also map to **IAPP AIGP body-of-knowledge** domains. A short mapping table of artifact → AIGP domain, with `needs-research` on exact domain names if you do not have the current BoK in front of you.
- Write the **briefing script** (3 bullets) you would use to walk `head-of-ai-governance` through the table in a 15-minute bilateral — what you lead with, what you flag, what you do not try to cover.
- Add a **refresh cadence** column to the table: how often the evidence artifact gets reproduced (annual, per-cycle, per-council, on-trigger).

## Why this exercise matters

Governance partners need to see the enablement operating model in standards vocabulary before they will trust the operating model to feed audit evidence. This mapping artifact is the one-pager they ask for — and the one that lets them stop re-explaining the standards in each conversation. The discipline of the memo — enablement-practice changes only, no standard rewrites, no control-library redesigns — is the same discipline from [Chapter 07](../07-what-you-route-out-counsel-soc-architect.md): observations and operating-model changes, not architecture. The map scales from this exercise into the real role unchanged; what you build here is the one-pager you will update every 6–12 months.
