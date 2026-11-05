# Exercise 02 — Industry Posting to Enablement Obligation Map

**Estimated effort:** 2.5 hours
**Format:** posting-reading memo + obligation-map table, Markdown
**Grounding chapters:** [01 — The Industry-Flavour Problem](../01-the-industry-flavour-problem.md); [03 — Healthcare](../03-healthcare-flavour-hipaa-and-phi.md); [04 — Finance](../04-finance-flavour-sr-11-7-and-finra.md); [05 — Legal Engineering](../05-legal-engineering-flavour.md); [06 — Education](../06-education-flavour-ferpa-coppa-and-ed-tech.md).

## Objective

Read a real industry-flavoured posting and map its language to the industry's regulatory surface and the enablement-side obligations that attach. Produce a two-part artifact:

1. A **posting-reading memo** that names what the posting says explicitly, what it implies about the regulatory surface, and what it leaves unsaid that the role still must own.
2. An **obligation map** listing the enablement-side obligations the role carries on day one, grounded in the industry chapter.

The exercise builds the reading skill — most industry postings do not spell out the regulatory surface, they imply it through company name, location, business line, and a few load-bearing phrases. The enablement lead who cannot read those signals walks into the first week unprepared.

## Prerequisites

- Chapter 01 read; the industry chapter(s) for the chosen posting read.
- Access to one real posting. Pick one of:
  - `p-018` Navitus Health Solutions — Lead AI Governance & Enablement (healthcare, PBM, PHI exposure).
  - `p-008` WelbeHealth — AI Adoption & Enablement Lead (healthcare, PACE-model care provider).
  - `p-014` Wells Fargo — AI Enablement Lending Lead (finance, national bank, lending flavour).
  - `p-012` Dodge & Cox — AI Enablement Manager (finance, SEC-registered investment adviser).
  - `p-022` Common Securitization Solutions — Director, Transformation & AI Enablement (finance, GSE-adjacent).
  - `p-021` The Walt Disney Company — Director, AI Enablement & Legal Engineering (legal engineering).
  - `p-017` McGraw Hill — Director, Engineering — AI Enablement (education, publisher).
  - `p-013` Ridgeline — AI Enablement Lead (investment-management platform with ed-flavoured content).
  - `p-009` Ed-tech client via Experis — AI Enablement Lead (education, ed-tech vendor).
- You will need to find the posting (or the retained snapshot) to work from. If you cannot find it, use the company's public-facing description of the role or the industry to approximate; mark gaps with `<!-- needs-research: ... -->`.

## Problem statement

You have interviewed for the role, the final round is the week after next, and you have decided to walk in with a prepared reading. You will not use the prepared reading as a monologue — you will carry it in your head. The written version is the drill. Produce a memo your future self can read in five minutes before the final-round interview, and that could stand on its own as the first week's orientation document if you took the role.

## Requirements

### Part A — Posting-reading memo (one page, no more)

Three sections.

1. **What the posting says explicitly.** The regulators, standards, data classes, obligations, and counterpart roles the posting names by name. Quote short phrases where the quote is load-bearing.
2. **What the posting implies.** The regulatory surface that follows from the organization's business line, location, and customer base, even though the posting does not name it. Draw on the relevant industry chapter. This is the section that matters most; the posting almost never lists everything.
3. **What the posting leaves unsaid.** The obligations you expect to attach that the posting does not reference, where you will want to verify in interview or in the first week. Includes known regulatory-surface items and known operational-model items (e.g., does the organization have a governance council? what is the CoE's maturity? does an MRM or privacy-officer function exist?).

### Part B — Obligation map (table, one page)

A table with one row per enablement-side obligation. Columns:

- **Obligation.** What the enablement lead owns operationally in this role.
- **Regulatory anchor.** The specific rule, standard, or practice that grounds the obligation (HIPAA Security Rule 164.308; SR 11-7 Section III; FINRA Rule 3110; FERPA 34 CFR Part 99; ABA Model Rule 1.6; EU AI Act Article 4; etc.).
- **Owning counterpart.** The role on the signing surface the enablement lead co-authors with.
- **First-week move.** The concrete thing the enablement lead would do in week one to engage this obligation (meet the role, read the current artifact, pull the current training roster, etc.).
- **Drift risk.** The specific drift from the industry chapter that this obligation most often triggers. One sentence.

At minimum, 10 rows. More is better if the industry supports them; the map is not padded, but it is comprehensive within the industry's surface.

## Starter guidance

- The posting is the source for *signals*, not the full picture. The industry chapter is the source for the full picture. The memo's job is to connect them.
- The "what the posting leaves unsaid" section is where most readers under-deliver. Force yourself to list five items — the memo should look like it was written by someone who has read the industry chapter, not just the posting.
- Where the posting uses a specific company-level term ("model risk governance," "privacy by design," "clinical informatics partnership"), carry the term forward in the map. Companies often read their own language back and warm faster to candidates who speak it.
- The first-week moves in the map should be specific — not "meet legal," but "meet the privacy officer and request the current HIPAA training roster and the BAA inventory."
- Drift risk is the one-sentence summary of the specific drift the industry chapter warns about. Keep it specific; "absorb HIPAA training program" is specific, "take on too much" is not.
- Where the posting is silent on facts you need (e.g., the maturity of the MRM function, the existence of a governance council, the size of the current training program), mark `<!-- needs-research: ... -->` in the memo. Do not invent context.

## Deliverables

- `posting-reading-memo.md` — one page, three sections.
- `obligation-map.md` — one-page table with at least 10 rows.
- A short reflection (3-5 sentences) on the two biggest surprises from the posting read versus your prior expectation of the role.

## Acceptance criteria

- The memo cites specific phrases from the posting in the "what the posting says" section (not just paraphrase).
- The "what the posting implies" section references the industry chapter explicitly and names at least three additional regulatory items not in the posting.
- The "what the posting leaves unsaid" section has at least five items.
- The obligation map has at least 10 rows and every row has all five columns filled.
- Every row's regulatory anchor is a specific rule / standard / practice — not a generic "privacy law."
- Every row's first-week move is a concrete action, not an abstraction.
- Every row's drift risk is a one-sentence specific drift from the industry chapter.
- `<!-- needs-research: ... -->` is used where organizational-context facts are not knowable from the posting.

## Stretch goals

- Choose **two** postings from different industry families and write a side-by-side obligation-map comparison. Call out the three obligations that look similar but are grounded in different regulators (for example, both finance and healthcare have "do not allow X data into non-approved tools"; the grounding is different).
- Write a three-question version of the interview questions you would ask the hiring manager after reading the posting. Each question should be calibrated — specific enough that a vague answer surfaces a red flag, not so specific that the hiring manager cannot answer.
- Identify the **one thing you would not do** in the first week based on your reading — the drift the industry chapter warned about that the posting looks structured to pull you into. Name it directly.

## Why this exercise matters

An enablement lead taking a role in a regulated industry without this reading starts the first week consuming context the organization has already paid someone to document. Running the reading as a drill before the first day — or for a more senior reader, running it before the final-round interview — gives the role two to four weeks of head start. Across a two-year tenure, that head start compounds into the difference between a role that lands early wins and a role that is still ramping when the first exam cycle arrives.
