# Lab 02 — Draft the CoE Service Catalog v0.1

**Duration:** 60 minutes
**Format:** guided hands-on — structured entry build across five audience segments
**Grounding chapters:** [03 — Authoring the Enablement Operating Model](../03-authoring-the-enablement-operating-model.md), [02 — The AI CoE Pattern Family](../02-the-ai-coe-pattern-family.md)

## Objective

Produce a **service catalog v0.1** — the external-facing menu of what the CoE offers — covering the five audience segments Chapter 03 names (individuals, teams, BUs, functions, executive office). The catalog must be short, specific, versioned, and sized to what a first-quarter CoE can realistically deliver.

This lab is not Exercise 02 (CoE shape memo) or Exercise 03 (handoff map). It operates on a different plane — the public menu the organization reads. Most of the organization never reads the operating model; they read the catalog.

## Prerequisites

- Chapter 03 read, specifically *The service catalog* section.
- A chosen CoE shape (from Exercise 02 if you did it; otherwise pick one deliberately before starting — the shape changes what you can plausibly publish).
- A chosen organization context (same one you used in Exercise 01 / 02 or a new one).
- Blank markdown file.

## Why this lab matters

Service catalogs collapse under their own weight when every well-intentioned idea goes in and nothing comes out. Chapter 03 names three specific anti-patterns: a catalog that only grows, a catalog longer than the first 90 days can ship, and a catalog that lists services the CoE cannot deliver without hiring that hasn't been approved. This lab forces the catalog through those filters on the first draft.

## Setup

Create `service-catalog-v0-1.md` with this skeleton:

```markdown
# <organization> AI CoE — Service Catalog

**Version:** v0.1 (draft)
**Owner:** AI Enablement Lead
**CoE shape:** <hub / hub-and-spoke / federated / embedded>
**Catalog horizon:** services deliverable in the first 180 days of CoE operation.

## For individuals

<entries>

## For teams

<entries>

## For BUs

<entries>

## For functions (legal, security, privacy, finance, HR)

<entries>

## For the executive office

<entries>

## Change log

- v0.1 (today) — initial draft. Next review: day 90.
```

Each entry (across every segment) uses this shape — copy it as a template:

```markdown
- **<Service name>** — one-line description.
  - *Who it's for:* <audience>.
  - *Access path:* <how someone requests it; a URL, an email, an office-hour slot>.
  - *SLA / cadence:* <same-day / weekly / monthly / on-request>.
  - *Owner inside CoE:* <role>.
  - *Status:* `active` / `pilot` / `coming <quarter>` / `sunset <date>`.
```

If you cannot populate all six fields for a service, the service is not ready for v0.1 — cut it or mark it `coming` with a date.

---

## Step 1 — "For individuals" segment (12 min)

Chapter 03's example entries: approved-tool list and access, Level 1 literacy curriculum (self-paced), role-based playbooks (by function), office hours, prompt-coaching clinic.

Draft **three to five** entries for this segment. Prioritize what the long-tail intake path (Chapter 03) actually needs — if 80%+ of employee traffic should resolve at self-serve, office hours, training, or champion routing, the catalog has to make each of those a visible, reachable service.

**Minimum coverage check:**

- [ ] At least one entry for the long-tail intake front door (self-serve resources behind one link).
- [ ] At least one entry that maps to "office hours" in the intake path.
- [ ] At least one entry that maps to "training" in the intake path.
- [ ] At least one entry that maps to "champion routing" in the intake path.

If you cannot staff all four in the first quarter — which is realistic for most starting CoEs — mark the missing ones `coming <quarter>` with a specific date, not an aspirational "soon." Chapter 03: "The catalog is a promise. Keep it small until you can deliver what's on it."

---

## Step 2 — "For teams" segment (8 min)

Chapter 03's example entries: team-adoption kit, team-manager playbook, use-case workshop, champion nomination path.

Draft **two to four** entries. Note the handoff from Chapter 04: the team-manager relationship is what you hand them (playbooks, training, champion slot, scorecard template) and what they hand you (field signal, nominations, metrics). The catalog is where you publish the left side of that exchange.

**Coverage check:**

- [ ] One entry explicitly supports the `ai-augmented-team-manager` (level 40) handoff.
- [ ] The champion nomination path names the SLA — how fast does a nomination get a yes/no?

---

## Step 3 — "For BUs" segment (8 min)

Chapter 03's example entries: embedded enablement partner (if hub-and-spoke), BU-level rollout planning, BU-level scorecard template, executive-briefing template.

Draft **two to four** entries. Here is where the CoE shape from Step 0 shapes the catalog:

- **Hub shape:** no embedded partner; publish rollout-planning as a CoE service with a central cadence.
- **Hub-and-spoke:** publish the embedded partner as a named service; name the BU-to-spoke mapping or say where it lives.
- **Federated:** publish only the thin-center services — vendor contracts, cross-BU reuse, policy alignment — and route BU-specific services to the BU's own program.
- **Embedded:** this segment may be near-empty; the catalog is thin by design.

**Coverage check:**

- [ ] The entries match the CoE shape named in the header. If "embedded enablement partner" is listed on a federated-shape catalog, something is wrong — fix one or the other.

---

## Step 4 — "For functions" segment (8 min)

Chapter 03's example entries: co-authored policy artifacts, intake-questionnaire support, policy-change notification cadence.

Draft **two to three** entries. These are the services that feed the handoffs to governance analyst (level 15), risk engineer (level 25, peer), and head of AI governance (level 60) from Chapter 04. Keep the entries in the catalog *narrow* — this segment is for partners, not for the whole org.

**Coverage check:**

- [ ] At least one entry names policy co-authoring with a cadence (e.g., "quarterly policy-draft review on <date>").
- [ ] At least one entry names a notification mechanism the governance analyst (level 15) can consume without you being in the loop.

---

## Step 5 — "For the executive office" segment (8 min)

Chapter 03's example entries: monthly executive scorecard, quarterly board-ready review, budget & ROI narrative, incident briefings.

Draft **two to four** entries. These are the public artifacts behind the scope contract's "decisions this role escalates" list (Chapter 01).

**Coverage check:**

- [ ] The scorecard entry names its cadence (monthly in Chapter 06's 90-day plan).
- [ ] At least one entry maps to an escalation path from the scope contract — regulator-notification criteria, multi-million-dollar vendor commits, board narrative, AI-misuse terminations.

---

## Step 6 — Cut and version (8 min)

Read the catalog back. Apply three cuts before you call it v0.1:

1. **Deliverability cut.** For every entry marked `active`, ask: "can the staffing shape I actually have deliver this in the first 90 days?" If no, downgrade to `pilot` or `coming <quarter>`. The staffing-shape target from Chapter 03 for first quarter is typically *you, one training person, one operations analyst*. Treat anything beyond that as a stretch commitment unless you have hired against it.
2. **Length cut.** If the catalog is longer than two pages at body-text size, cut services until it fits. Chapter 03 is explicit: "Keep it short and specific."
3. **Sunset reservation.** Mark one entry — pick the most speculative — with a placeholder `sunset: review <date 6 months out>`. The habit of writing sunsets at creation time is what keeps the catalog from only growing.

Write a one-sentence note at the bottom of the file: "This catalog promises what the CoE will deliver in the next 180 days. Services marked `coming` are commitments conditional on named hires or decisions; services marked `pilot` run with a known small cohort before general release."

---

## Deliverable

- `service-catalog-v0-1.md` — five segments, each with the right number of entries (3–5 / 2–4 / 2–4 / 2–3 / 2–4), every entry carrying all six fields, change-log footer present.

## Expected output shape

Roughly 1.5–2 pages of markdown. 12–18 total entries across the five segments. One sunset placeholder visible. No entry missing any of the six template fields. The CoE shape named in the header matches what the "For BUs" segment publishes.

## Checkpoint — self-evaluation

- [ ] Every entry has all six fields populated (or is cut).
- [ ] The intake path's four self-resolve outcomes (self-serve / office hours / training / champion routing) each map to at least one `active` or `pilot` entry.
- [ ] At least one entry carries a visible `sunset` date — the catalog is not an append-only log.
- [ ] A new hire into the CoE could read the catalog and, in ten minutes, know what the CoE delivers and what it does not.
- [ ] A skeptical executive sponsor could read the catalog and point at which entries the current staffing shape cannot deliver — and those entries are already marked `coming`, not `active`.

## Common failure modes

- **"Executive briefing on demand" as a service.** Not a service — an open-ended time commitment. Convert to "monthly executive scorecard + quarterly review" with named dates.
- **Everything marked `active`.** The CoE has not shipped anything yet. Honest statuses are `pilot` and `coming`; use `active` only for services you can deliver today.
- **Services that overlap with governance.** If "policy ownership" or "regulator engagement" shows up in the catalog, you have collapsed the Chapter 01 co-author / owner distinction. Reword.
- **No sunset dates anywhere.** Every catalog grows. Pre-committing a sunset at creation time is the only reliable prevention.

## What this prepares you for

Service catalog v0.1 is the first public artifact of the CoE after the scope contract and operating-model doc. It is the thing champions will send to their peers when asked "what does the CoE do?" The catalog you draft here is the baseline you will revise at day 90 after the first cohort has run through it (per Chapter 06's 90-day plan), and it is the backbone of the operating model you run in [mod-111](../../mod-111-ai-coe-operations-vendor-management-and-cross-functional-leadership/README.md).
