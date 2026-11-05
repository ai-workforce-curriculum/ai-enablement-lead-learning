# The Enablement Cost Model at Org Scope

> [mod-106 Chapter 05](../mod-106-outcome-measurement-and-executive-reporting/05-partnering-with-finance-on-cost-model-and-roi.md) sketched the four cost components that belong in the denominator of the scorecard ROI line. This chapter is where the cost model is built at depth: the full line-item taxonomy, how each line is sourced, the common undercounts, and the ledger discipline that keeps the denominator defensible across reorganizations, tool swaps, and staffing changes. If this chapter does the job, the ROI narrative in [Chapter 02](02-projecting-roi-with-confidence-bands.md) inherits a denominator that does not surprise anyone.

## Why most enablement cost models are smaller than reality

Three structural pressures push the cost model toward an undercount.

- **Only the invoiceable lines are visible.** Vendor seat invoices arrive on a schedule Finance already tracks. Embedded partner FTE time, training-production labor, champion operating effort, and downstream support cost do not arrive on an invoice; they have to be *constructed*. The enablement lead who copies the invoice set into the denominator is handing in a cost model that is only as complete as the AP system.
- **The CoE's own operating cost is self-obscured.** The enablement lead's own team is the hardest line to count because it feels like part of the overhead that pays for everything. It is not. The CoE is a cost center attributable to the AI enablement program; the fully-loaded cost of the enablement team belongs in the denominator on the same footing as the tool licenses.
- **Costs follow the rollouts in different ledgers.** Training-production labor sometimes sits inside L&D. Champion time sits inside BU operating budgets. Support-ticket volume lands in IT. Legal review time lands with the general counsel. The honest cost model reaches across ledgers; the ledger-internal cost model systematically under-reports.

The goal of the chapter is to give the role a cost taxonomy, sourcing map, and ledger discipline that produces a denominator the role can defend in a CFO review without a line being discovered mid-meeting.

## The cost taxonomy — six families, every line in one of them

Every cost line in the enablement cost model belongs to exactly one of six families. The families are chosen so the sourcing rules differ — same family, same source pattern — and so a reviewer can scan the model top-down without a line hiding in a category it does not belong to.

### Family 1 — Tool licenses

The direct cost of AI tools in production and in flight.

- **Enterprise seat subscriptions.** Per-seat per-month charges for coding/knowledge-work copilots, platform add-ons, industry-specific tools. Include the full contracted-seat count, not the active-seat count — unused seats are a cost whether or not value is being extracted; the gap between contracted and active is a separate scorecard signal, not a reason to shrink the denominator.
- **Usage-based charges.** API consumption, token-based billing on internal-build components, metered inference on bring-your-own-model deployments. Usage charges are variable; they belong in the denominator at the trailing-twelve-month trailing average or the current quarter's run-rate, with the choice stated.
- **Premium add-ons and tiers.** Annotations, retention, vendor-side admin features, enterprise-security tiers. These line items hide inside a "Microsoft Copilot" or "GitHub Copilot" invoice and can be two to four times the base-seat rate for advanced tiers. Itemize them.
- **True-ups and over-use charges.** Contracts commonly reconcile a true-up at renewal. The reconciled amount belongs to the quarter the usage occurred, not the quarter the invoice landed — a recognition rule your Finance partner will have an opinion on.
- **Pilot and POC costs.** Short-duration, out-of-envelope pilot licenses. Carry them in a separate line while the pilot is running; collapse them into the enterprise-seat line once the rollout is live. The pilot-vs-rollout line boundary is the trigger.

### Family 2 — Enablement-program direct spend

The operating budget of the CoE / enablement team itself.

- **Enablement-team headcount, fully-loaded.** Enablement lead, program managers, instructional designers, measurement analysts. Fully-loaded (salary + benefits + facilities + overhead allocation) at the organization's standard multiplier; see the fully-loaded FTE question in [mod-106 Chapter 05](../mod-106-outcome-measurement-and-executive-reporting/05-partnering-with-finance-on-cost-model-and-roi.md). This is the single largest non-vendor line on most cost models and the one the enablement lead is most often reluctant to count.
- **External services and consulting.** Change-management consultants, outside instructional designers, assessment vendors, benchmarking subscriptions, analyst-firm advisory retainers. Easy to count — they come as invoices.
- **Enablement tooling.** LMS seats, authoring tools, survey platforms, dashboard subscriptions used by the enablement function, workflow-interview transcription tools. These are *CoE infrastructure*, not AI-tool licenses; keep them separated.
- **Internal communication and content production.** Video production, intranet publishing, event hosting (town halls, roadshows), merchandising for the champion program. Often absorbed into communications departments; attribute the AI-enablement share.
- **Travel and events.** Rollout kickoffs, champion-network convenings, peer-exchange participation. Variable by cycle; reported at actual.

### Family 3 — Training production and delivery

Separated from enablement-program direct spend because the production of training is a cost pattern distinct from the ongoing CoE operation, and because large-scale training production is often outsourced or shared with L&D.

- **Curriculum development labor.** Instructional-designer hours for AI-literacy curriculum, role-specific modules, tool-specific onboarding, refresh cycles. Count internal labor at fully-loaded cost; count outside instructional-designer firms at invoice.
- **Subject-matter-expert time.** Internal experts seconded to training production — legal partners reviewing policy modules, security reviewing data-handling modules, BU leaders recording role-specific content. 10% of a senior director's time on SME duties for a quarter is a cost; it does not show up on any invoice; count it anyway.
- **Delivery labor.** Live-session facilitation, cohort-based program leadership, office-hours staffing, learning-pod co-leads. Half the cost of a well-run program; also commonly the most-undercounted line.
- **Learning-platform and content licensing.** Third-party AI-literacy courseware, platform licensing for the LMS component dedicated to AI content, certification fees. These sit between Family 2 (CoE infrastructure) and Family 3 (training production); place consistently and document the rule.
- **Assessment and credentialing.** Proctored assessments, certification exam fees, badge infrastructure. Small lines individually; cumulatively meaningful at enterprise scale.

### Family 4 — Embedded enablement partner FTE

Partners embedded in business units who spend a fraction of their time on enablement work. The hardest family to count because the labor is partial, distributed, and resides in operating headcount the CoE does not control.

- **BU-embedded enablement partners.** Dedicated or fractional partners in each BU who run the local rollouts, coordinate with the CoE, and own the BU-level operating details.
- **Champion-network operator time.** Named champions carrying 10%–20% of a role's time on champion duties. At enterprise scale with a hundred champions, this is the largest line in Family 4 by a wide margin — see [Chapter 05](05-reconciling-the-tool-stack-across-bus.md) and [mod-105](../mod-105-champion-networks-and-change-management/README.md) for the champion operating model.
- **Shadow enablement time.** The engineering lead who runs informal office hours for their team, the operations manager who writes BU-specific tip sheets, the HR business partner who coaches managers through change. Real work, real time, rarely attributed to the enablement program. Count it where it is material; acknowledge the estimation error in the methodology appendix.
- **Governance and policy-partner time.** Legal, security, privacy, and compliance partners who review enablement artifacts (policy, training content, DPAs). Fractional, substantial in aggregate.

The accounting convention here is a bright-line rule, co-authored with Finance and HR/Workforce Planning: a role allocates to the enablement program at a stated percentage of their time, at the organization's fully-loaded cost multiplier, with the allocation ratified in an annual working group (see the FTE-attribution working group in [mod-106 Chapter 05](../mod-106-outcome-measurement-and-executive-reporting/05-partnering-with-finance-on-cost-model-and-roi.md)). Without the convention, the family is unreported; with the convention, it is defensible.

### Family 5 — Champion-network operating cost

Separated from Family 4 so the champion-network cost is readable on its own. The champion program has budget lines that do not reduce to FTE time.

- **Champion recognition and rewards.** Any formal recognition budget (titles, badges, spot bonuses, swag, annual recognition events, mentorship allocations). Typically small per-champion but material in aggregate.
- **Champion training and development.** Onboarding the champions themselves, continuing-development for champion skills (facilitation, change management, communication craft), external training allocations if the organization sponsors them.
- **Community infrastructure.** Collaboration spaces, intranet surfaces, newsletter publishing, event hosting (champion summits, quarterly gatherings), travel to convenings.
- **Champion-coordinator team (if dedicated).** Some organizations staff a dedicated champion-program manager and operations function; carry its fully-loaded headcount here rather than inside Family 2.

### Family 6 — Downstream support, risk, and operating cost

The costs the enablement program *generates downstream* but does not directly spend. The hardest family to quantify; the easiest for a skeptical reviewer to call out as missing.

- **Help-desk and IT support.** Tickets generated by AI-tool support: account provisioning, licensing questions, integration issues, "it stopped working." Measurable through the ticketing system's AI-tag; attribute at the ticket-time cost rate.
- **Security review and monitoring.** Ongoing security operations load generated by AI tools: DLP monitoring, data-exfil review, incident triage on AI-related alerts.
- **Legal and compliance review.** Ongoing contract review, DPA updates, policy iteration load generated by the AI program. See [Chapter 04](04-partnering-with-procurement-finance-and-it.md) on the partnership model.
- **Incident-response cost.** When an AI-related incident occurs, the incident-response labor and remediation cost (see [mod-109](../mod-109-ai-incident-response-and-enablement-side-rollback/README.md)) belongs in the denominator for the period it occurred.
- **Change-management load on managers.** The team-manager time absorbed by rollout coordination, team-level measurement, 1:1 coaching through adoption. See [mod-105](../mod-105-champion-networks-and-change-management/README.md) for the shape.
- **Opportunity cost of the time operators spend learning and adopting the tools.** Measured at operator fully-loaded time × hours per adoption cycle. Finance will ask about this; have a number or have a stated reason the number is excluded.

## The sourcing map — where each line comes from

Each family has a different authoritative source. The sourcing map is the second artifact (after the taxonomy) that the Finance partnership from [Chapter 04](04-partnering-with-procurement-finance-and-it.md) ratifies.

```
Family                           | Authoritative source                           | Reconciliation cadence
---------------------------------+------------------------------------------------+------------------------
Tool licenses                    | Vendor invoices + procurement ledger           | Monthly
Enablement-program direct spend  | CoE cost center GL                             | Monthly
Training production              | L&D cost center + SME time attestation         | Quarterly
Embedded FTE                     | HR/Workforce Planning + BU-time attestation    | Semi-annually
Champion operating cost          | Champion-program ledger (Family 2 if sub-line) | Quarterly
Downstream support               | IT ticketing + security + legal timesheets     | Quarterly
```

Three sourcing disciplines keep the map defensible.

- **Cross-ledger reconciliation.** Costs cross organizational-unit boundaries. The AI-tag on IT tickets, the AI-project code on legal timesheets, the enablement-program allocation on HR records — these are the hooks that let the model aggregate across ledgers. Setting up the hooks is one-time work; running them is cheap.
- **Attestation for partial time.** Lines that cannot be read from a system (SME time, shadow enablement, BU-time allocation to champion duties) run on an attestation rhythm — a short structured form the time-contributor signs off on each quarter. Attestation is slower than a system read; it is also the floor a Finance auditor will accept.
- **Dollar-threshold materiality.** Not every $300 line is worth the collection cost. Set a materiality threshold with Finance (typical: items under 0.5% of the total denominator can be collapsed into an "other / small lines" bucket). The threshold is published in the methodology appendix.

## A worked example — a cost model, sketched

A sketch of a mid-sized organization's annual enablement cost model, line structure only. Numbers are illustrative; the shape is what to study.

```
Family 1 — Tool licenses
  Enterprise copilot seats (2,400 × $360/yr)              864,000
  Platform-add-on seats (M365 Copilot, 1,100 × $360/yr)   396,000
  Specialty tool licenses (legal, support)                220,000
  Usage-based inference (API, internal RAG)               180,000
  Premium tiers and admin add-ons                          95,000
  Pilot and POC licenses                                   48,000
                                                       ----------
                                            Family 1   1,803,000

Family 2 — Enablement-program direct spend
  CoE team, fully-loaded (9 FTE)                        2,340,000
  External services and consulting                        320,000
  Enablement tooling (LMS, authoring, surveys)             95,000
  Content production                                       75,000
  Travel and events                                        60,000
                                                       ----------
                                            Family 2   2,890,000

Family 3 — Training production and delivery
  Curriculum development (internal)                       380,000
  SME time (attested)                                     210,000
  Delivery labor (facilitators, office hours)             420,000
  Learning-platform and content licensing                  85,000
  Assessment and credentialing                             35,000
                                                       ----------
                                            Family 3   1,130,000

Family 4 — Embedded enablement partner FTE
  BU-embedded partners (6 × 40%)                          960,000
  Champion time (100 × ~12% of fully-loaded)            1,560,000
  Shadow enablement (attested)                            210,000
  Governance partner time (legal, security, privacy)      280,000
                                                       ----------
                                            Family 4   3,010,000

Family 5 — Champion-network operating cost
  Recognition and rewards                                  45,000
  Champion training and development                        85,000
  Community infrastructure and events                      70,000
  Champion-coordinator role (fractional)                  180,000
                                                       ----------
                                            Family 5     380,000

Family 6 — Downstream support, risk, operating
  IT support load (AI-tagged tickets)                     220,000
  Security review and monitoring                          180,000
  Legal / compliance review                               140,000
  Incident-response cost (FY trailing)                     60,000
  Manager change-management load (attested)               310,000
  Operator learning time (adoption cycles)                420,000
                                                       ----------
                                            Family 6   1,330,000

                                                       ==========
Total annual denominator                              10,543,000
```

Three observations about the sketch.

- **Family 1 is less than a fifth of the total.** Organizations that report only the tool-license line are under-reporting by five-fold or more. The denominator discipline is in the other five families.
- **Family 4 is the largest line.** At enterprise scale with a champion network, embedded-partner time is usually the top line. The absence of this family is the single most common gap in published enablement cost models.
- **Family 6 is the hardest line to produce and the easiest to attack.** The mid-sized organization in the sketch could not claim $10.5M as its denominator if Family 6 was zero; a reviewer would ask about it and find nothing. Build Family 6 with Finance from the start.

## Common undercounts and how they are caught

Five recurring undercounts, each with the specific question the reviewer asks and the specific line the reviewer wants to see.

- **"Where is the champion time?"** The most common challenge. Count champion time at fully-loaded cost in Family 4; reinforce with the champion-program ledger in Family 5.
- **"Where is the operator learning time?"** A rollout that consumes 90 minutes of operator time for onboarding across 2,400 operators is 3,600 hours of fully-loaded labor. Finance will model this at the standard fully-loaded rate.
- **"Where is the help-desk cost?"** Family 6 line; sourced from AI-tagged tickets. If the ticketing system does not AI-tag, say so in the methodology note and quote a sampled estimate until the tag lands.
- **"Why is Family 2 so small?"** When the CoE line reports only the enablement lead's salary, the reviewer asks where the rest of the team is. Fully-loaded CoE headcount is the right line; confirm the multiplier with Finance ([mod-106 Chapter 05](../mod-106-outcome-measurement-and-executive-reporting/05-partnering-with-finance-on-cost-model-and-roi.md)).
- **"Where is the pre-existing cost separated from the AI-incremental cost?"** Microsoft 365 and Google Workspace seats existed before the AI add-ons; only the incremental AI license belongs in the AI denominator. Separate the AI-incremental cost from the pre-existing baseline explicitly in the methodology note. This is the same discipline the vendor-marketing argument fails ([mod-106 Chapter 05](../mod-106-outcome-measurement-and-executive-reporting/05-partnering-with-finance-on-cost-model-and-roi.md)).

## Keeping the cost model current

Three cadence commitments keep the model from decaying between the quarterly reviews.

- **Monthly invoice reconciliation with Finance.** Family 1 and part of Family 2 reconcile monthly (see interface 2 in [mod-106 Chapter 05](../mod-106-outcome-measurement-and-executive-reporting/05-partnering-with-finance-on-cost-model-and-roi.md)). The remainder reconciles on the family's own cadence per the sourcing map.
- **Quarterly attestation cycle.** SME time, shadow enablement, manager change-management load, and any attested lines run quarterly, with the attestation form signed off by the time-contributor's manager, not the time-contributor alone. This reduces self-report inflation.
- **Annual methodology refresh.** The family taxonomy, the materiality threshold, the fully-loaded multiplier, the allocation conventions — reviewed once a year with Finance and HR/Workforce Planning. Mid-year changes are permitted but logged; the audit trail is the methodology-footnote section of the annual review.

## What this chapter feeds

- [Chapter 02](02-projecting-roi-with-confidence-bands.md) uses the denominator produced here in the ROI equation; the attribution discipline there is only credible against a complete denominator.
- [Chapter 03](03-the-build-vs-buy-matrix-at-enterprise-scope.md) uses the cost model structure in a build-vs-buy run — total cost of ownership is the same taxonomy applied to a candidate build.
- [Chapter 04](04-partnering-with-procurement-finance-and-it.md) is where the sourcing map becomes a running Finance / Procurement / IT partnership.
- [Chapter 05](05-reconciling-the-tool-stack-across-bus.md) uses Family 1 and Family 4 to find overlapping-spend consolidation opportunities.
- [Chapter 06](06-the-vendor-vetting-rubric.md) uses the Family 1 and Family 6 lines to price vendor-specific risks into the cost model.

## Summary

- Every enablement cost line belongs to exactly one of six families: tool licenses, enablement-program direct spend, training production, embedded FTE, champion-network operating cost, downstream support/risk/operating.
- The sourcing map assigns each family an authoritative source and a reconciliation cadence; cross-ledger reconciliation hooks and an attestation rhythm make the map tractable.
- Family 4 (embedded FTE) is usually the largest line and the most commonly omitted; Family 6 (downstream) is the hardest to construct and the easiest for a reviewer to attack as missing.
- The standard fully-loaded multiplier is Finance's, not enablement's; use it rather than inventing one.
- Five named undercounts to catch in your own cost model before a reviewer catches them: champion time, operator learning time, help-desk cost, under-counted CoE headcount, un-separated AI-incremental cost.
- Running cadences — monthly invoice reconciliation, quarterly attestation, annual methodology refresh — keep the denominator current between the scorecard cadences from [mod-106 Chapter 02](../mod-106-outcome-measurement-and-executive-reporting/02-authoring-the-executive-scorecard-weekly-monthly-quarterly.md).
