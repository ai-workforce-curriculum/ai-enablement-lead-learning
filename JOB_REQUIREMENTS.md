# Job Requirements — AI Enablement Lead

**Role level:** 45 (org-wide enablement scope — AI Workforce family)
**Catalog source:** [`.aicg/job-requirements.json`](.aicg/job-requirements.json)
**Research window:** 2026-08-07 → 2026-11-05 (90-day target, aligned to current cycle)
**Live postings sampled:** 26 (target minimum: 25 — met)
**Refreshed:** 2026-11-05

## Status

The requirements catalog is grounded in **26 in-window postings fetched and verified between 2026-08-07 and 2026-11-05**. Sources span LinkedIn, BuiltIn, Greenhouse, Lever, Ashby, Workday, Welcome to the Jungle, and employer career sites; staffing-agency duplicates and aggregator-only stubs are discarded. The literal title "AI Enablement Lead" is now the modal market title for the role; "Head of AI Enablement", "Director, AI Enablement", "AI Adoption Lead", "AI Transformation Lead", and "AI Center of Excellence Lead" are near-interchangeable and are included in the sample.

**Known gaps in this cycle's sample** (carried into the next cycle's `next_cycle_todo`):

- 12 of 26 postings do not render `date_posted` on their canonical page — counted with `date_observed = 2026-11-05` after live-verification.
- 3 retained postings (Dodge & Cox, Ridgeline, CSI) were observed as removed inside the window — language retained as representative because removal date falls inside the window.
- 2 postings (Disney, Common Securitization Solutions) rely on secondary-source coverage (Ladders / Artificial Lawyer) because the canonical fetch was blocked or unresolvable.
- EU/EEA representation thin (1 UK) and public-sector representation is 0 this cycle. The only in-window European posting (ECB AI Adoption Lead, Frankfurt) closed outside the window and was excluded.

## Sampling shape

| Dimension | Count |
|---|---|
| Tech / SaaS | 9 |
| Finance | 5 |
| Healthcare / Pharma | 4 |
| Consulting / Services | 2 |
| Media / Entertainment | 2 |
| Education | 2 |
| Enterprise other | 2 |
| US | 24 |
| UK | 1 |
| Multi-region remote | 1 |

## Ownership rule

Primary coverage is assigned to the lowest level on the ladder where the requirement is genuinely required. Higher-level roles link to that owner unless they need different depth, architectural scope, or leadership framing. **AI Enablement Lead (level 45, AI Workforce family) is the terminal rung of the AI Workforce ladder for org-wide enablement scope.** It owns org-wide AI tool rollout, policy co-authoring with governance, training programs + champion networks + change management, and outcome measurement across the organization. It defers:

- **Down** to [`ai-augmented-team-manager`](https://github.com/ai-workforce-curriculum/ai-augmented-team-manager-learning) (level 40) for team-scope AI adoption and team-level ROI; to [`ai-augmented-product-manager`](https://github.com/ai-workforce-curriculum/ai-augmented-product-manager-learning) (level 30) for AI-feature product ROI; to [`ai-augmented-analyst`](https://github.com/ai-workforce-curriculum/ai-augmented-analyst-learning) (level 20) and [`ai-assisted-software-engineer`](https://github.com/ai-engineering-curriculum/ai-assisted-software-engineer-learning) (level 20) for IC-level AI-assisted mechanics.
- **Sideways** to the AI Governance family — [`ai-governance-analyst`](https://github.com/ai-governance-curriculum/ai-governance-analyst-learning) (level 15, operational legwork), [`ai-risk-engineer`](https://github.com/ai-governance-curriculum/ai-risk-engineer-learning) (level 25, engineered risk and red-team), [`senior-ai-governance-architect`](https://github.com/ai-governance-curriculum/senior-ai-governance-architect-learning) (level 50, control-library architecture), [`head-of-ai-governance`](https://github.com/ai-governance-curriculum/head-of-ai-governance-learning) (level 60, program leadership).
- **Sideways** to the AI Engineering family — [`applied-ai-engineer`](https://github.com/ai-engineering-curriculum/applied-ai-engineer-learning), [`agentic-ai-engineer`](https://github.com/ai-engineering-curriculum/agentic-ai-engineer-learning), [`agentic-systems-architect`](https://github.com/ai-engineering-curriculum/agentic-systems-architect-learning) — for the build of internal agents and platforms this role commissions.
- **Out of scope** to legal counsel (no legal opinion), to procurement / finance (contract execution, billing), and to IT identity teams (SSO / IAM implementation).

## Requirements summary

Threshold: a requirement that appears in **≥ 30% of in-window postings** gets dedicated curriculum coverage. Below-threshold requirements are monitored and surface as exercises or link-outs rather than full modules.

### Above threshold — dedicated coverage

| ID | Theme | Frequency | n/26 | Primary module |
|---|---|---|---|---|
| R7 | Training program design | 0.85 | 22 | [mod-104](.aicg/curriculum-plan.json) training-programs-and-ai-literacy-curriculum |
| R4 | Outcome / workflow / usage measurement | 0.77 | 20 | [mod-102](.aicg/curriculum-plan.json) selecting-and-rolling-out-ai-tools + [mod-106](.aicg/curriculum-plan.json) outcome-measurement-and-executive-reporting |
| R9 | Change management & stakeholder comms | 0.69 | 18 | [mod-105](.aicg/curriculum-plan.json) champion-networks-and-change-management |
| R3 | Rollout artifact set (policy, access, training, support, champions, kill switch) | 0.65 | 17 | [mod-102](.aicg/curriculum-plan.json) selecting-and-rolling-out-ai-tools |
| R6 | Executive reporting & exec-ready communications | 0.58 | 15 | [mod-106](.aicg/curriculum-plan.json) outcome-measurement-and-executive-reporting |
| R8 | Champion networks (design, recruit, run, measure, iterate) | 0.54 | 14 | [mod-105](.aicg/curriculum-plan.json) champion-networks-and-change-management |
| R13 | AI governance partnership (co-author / consumer) | 0.54 | 14 | [mod-103](.aicg/curriculum-plan.json) policy-co-authoring-with-governance (co-owned with [`head-of-ai-governance`](https://github.com/ai-governance-curriculum/head-of-ai-governance-learning)) |
| R1 | Tool selection / vendor evaluation | 0.42 | 11 | [mod-102](.aicg/curriculum-plan.json) selecting-and-rolling-out-ai-tools |
| R5 | Policy co-authoring with legal / security / governance | 0.42 | 11 | [mod-103](.aicg/curriculum-plan.json) policy-co-authoring-with-governance |
| R12 | Role-based playbooks / use-case libraries | 0.38 | 10 | [mod-104](.aicg/curriculum-plan.json) training-programs-and-ai-literacy-curriculum |
| R16 | Internal AI tool build / agent commissioning | 0.38 | 10 | [mod-110](.aicg/curriculum-plan.json) commissioning-internal-ai-tools-and-custom-agents (owner: [`applied-ai-engineer`](https://github.com/ai-engineering-curriculum/applied-ai-engineer-learning); this role commissions) |
| R11 | Prompt-engineering coaching for non-engineers | 0.35 | 9 | [mod-104](.aicg/curriculum-plan.json) training-programs-and-ai-literacy-curriculum (coaching framing only) |
| R14 | Budget / ROI / business case | 0.35 | 9 | [mod-107](.aicg/curriculum-plan.json) budget-roi-and-build-vs-buy-at-org-scope |
| R15 | Cross-functional program management | 0.35 | 9 | prerequisite — see [`PREREQUISITES.md`](PREREQUISITES.md) |
| R10 | AI literacy curriculum for employees | 0.31 | 8 | [mod-104](.aicg/curriculum-plan.json) training-programs-and-ai-literacy-curriculum |
| R2 | Pilot design & rollout execution | 0.31 | 8 | [mod-102](.aicg/curriculum-plan.json) selecting-and-rolling-out-ai-tools |

### Below threshold — monitored

| ID | Theme | Frequency | n/26 | Status |
|---|---|---|---|---|
| R19 | Industry-specific compliance (HIPAA / FINRA / legal / EU AI Act in-industry) | 0.27 | 7 | Covered at the flavour-overlay level in [mod-108](.aicg/curriculum-plan.json); deep industry-specific regulatory work defers to [`head-of-ai-governance`](https://github.com/ai-governance-curriculum/head-of-ai-governance-learning) (level 60) |
| R17 | Vendor / external-partner management | 0.23 | 6 | Covered at a lightweight vendor-vetting rubric level in [mod-107](.aicg/curriculum-plan.json) and [mod-111](.aicg/curriculum-plan.json); one cycle from clearing the 0.30 bar |
| R18 | Data privacy & DLP for AI tools | 0.23 | 6 | Enablement-side artifact carried by R5 (policy co-authoring) in [mod-103](.aicg/curriculum-plan.json); deep privacy engineering defers to [`ai-privacy-engineer`](https://github.com/ai-governance-curriculum/ai-privacy-engineer-learning) |
| R20 | Agent-platform / agentic architecture build | 0.19 | 5 | Architectural scope defers to [`agentic-systems-architect`](https://github.com/ai-engineering-curriculum/agentic-systems-architect-learning) (peer, AI Engineering family); commissioning side carried by [mod-110](.aicg/curriculum-plan.json) |
| R21 | M&A / enterprise-scale transformation framing | 0.12 | 3 | Defers upward to [`chief-ai-officer`](https://github.com/ai-governance-curriculum/chief-ai-officer-learning) (level 70) |

### Prerequisites — not re-taught here

| ID | Theme | Owner | Rationale |
|---|---|---|---|
| R15 | Cross-functional program management | general program-management background | Status reporting, risk registers, decision logs, portfolio coordination — assumed at the L45 entry bar |
| R22 | Dashboard mechanics (chart construction, pipeline building) | [`ai-augmented-analyst`](https://github.com/ai-workforce-curriculum/ai-augmented-analyst-learning) (level 20) | This role *commissions* and *reads* dashboards; building them is IC work done by the analyst track |
| R23 | People-management fundamentals | general management background | 1:1s, feedback, hiring, performance, budget at the baseline level — assumed |

## Sampled postings

| ID | Employer | Title | Date observed | Location | Seniority |
|---|---|---|---|---|---|
| p-001 | Harvard University (HUIT) | AI Enablement Lead | 2026-11-05 (posted 2026-10-15) | Cambridge, MA (on-site) | Lead |
| p-002 | Restaurant365 | Senior AI Enablement Manager | 2026-11-05 | Austin TX / Akron OH / Irvine CA (hybrid) | Senior |
| p-003 | iHerb | Head of AI Enablement | 2026-11-05 | Remote, US | Head |
| p-004 | BuildOps | Head of AI Center of Excellence | 2026-11-05 | Los Angeles / San Francisco, CA (hybrid) | Head |
| p-005 | Zoom | AI Transformation Lead | 2026-11-05 | Remote, US | Senior / Executive |
| p-006 | Liminal | Applied AI Enablement Lead | 2026-11-05 | Remote | Lead |
| p-007 | Walker & Dunlop | Program Manager, AI Enablement | 2026-11-05 (posted 2026-10-19) | Remote, US | Manager / Senior |
| p-008 | WelbeHealth | AI Adoption & Enablement Lead | 2026-11-05 (posted 2026-09-05) | US | Lead |
| p-009 | Experis USA (ed-tech client) | AI Enablement Lead | 2026-11-05 (posted 2026-10-29) | Raleigh, NC | Mid-senior |
| p-010 | Voice Systems Engineering | Head of AI Enablement & Transformation | 2026-11-05 (posted 2026-10-27) | Remote, US | Executive |
| p-011 | Axios | AI Enablement Lead | 2026-11-05 | Remote, US | Lead |
| p-012 | Dodge & Cox | AI Enablement Manager | 2026-11-05 (removed 2026-08-12) | San Francisco, CA | Senior |
| p-013 | Ridgeline | AI Enablement Lead | 2026-11-05 (removed 2026-10-23) | New York, NY | Senior |
| p-014 | Wells Fargo | AI Enablement Lending Lead | 2026-11-05 (posted 2026-10-26) | New York, NY | Senior Lead |
| p-015 | Crunchyroll | Director, AI Enablement | 2026-11-05 (posted 2026-10-08) | Los Angeles, CA | Director |
| p-016 | Greystar | Senior Director, AI Enablement | 2026-11-05 | Remote, US | Senior Director |
| p-017 | McGraw Hill | Director, Engineering — AI Enablement | 2026-11-05 (posted 2026-11-03) | Remote, US | Director |
| p-018 | Navitus Health Solutions | Lead AI Governance & Enablement | 2026-11-05 (posted 2026-08-14) | Remote, US | Senior Lead |
| p-019 | ClearView Healthcare Partners | AI Enablement Manager | 2026-11-05 (posted 2026-08-15) | San Francisco / Boston / NY | Manager |
| p-020 | CVS Health | Lead Director AI Platform Enablement Automation | 2026-11-05 (posted 2026-10-30) | Northbrook, IL | Director |
| p-021 | The Walt Disney Company | Director, AI Enablement & Legal Engineering | 2026-11-05 (posted 2026-09-24) | Burbank, CA / New York, NY | Director |
| p-022 | Common Securitization Solutions | Director, Transformation & AI Enablement | 2026-11-05 | Remote, US | Director |
| p-023 | Illumina | Supply Chain AI Enablement Lead | 2026-11-05 (posted 2026-11-03) | San Diego, CA | Lead |
| p-024 | Global Advertising Agency (via Edge Tech, London) | Head of AI Enablement | 2026-11-05 | London, UK (hybrid) | Head |
| p-025 | CSI (Computer Services, Inc.) | AI Adoption Manager | 2026-11-05 (removed 2026-08-17) | Remote, US | Manager |
| p-026 | IMA Financial Group | AI Enablement Lead | 2026-11-05 | Denver, CO (remote) | Lead |

Full URLs, posting-level `evidence` quotes, and the full requirement-to-posting map live in [`.aicg/job-requirements.json`](.aicg/job-requirements.json).

## Salary ranges

<!-- needs-research: live posting sample did not capture compensation bands (most Greenhouse / Lever / Workday / Ashby detail pages did not render a published salary range, and secondary-source captures for Disney and Common Securitization Solutions omitted the band). Backfill compensation data on the next cycle via employer career sites and state-mandated pay-transparency postings (CA, CO, NY, WA, IL) where present. -->

## Next cycle

- Widen to EU/EEA postings (ECB, national AI offices, Deutsche Bahn-class enterprises).
- Pick up public-sector and NGO / foundation postings.
- Watch R17 (vendor management 0.23), R18 (data privacy / DLP 0.23), R19 (industry-specific compliance 0.27), R20 (agent-platform build 0.19) — any of these crossing 0.30 justifies dedicated coverage.
- Backfill compensation bands.
