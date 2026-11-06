# Business Requirements Document

Status: evidence-backed analytical draft, 6 November 2026. Requirement IDs were assigned during this review; they are not claimed as the project's original historical backlog. Objectives: [BO1–BO4](problem-and-context.md).

## Business requirements and functional scope

| Business ID | Requirement | Functional ID / behavior | Current status |
| --- | --- | --- | --- |
| BR1 | A player understands whether a bus can leave and how to prepare it | FR1: list permit, crew, fuel, condition and busy-state blockers | VERIFIED helper cases, E04; end-to-end usability UNVERIFIED |
| BR2 | One trip has explainable and nonduplicated financial consequences | FR2: preserve assumptions, account for fuel/tolls/receipts and reconcile result/cash | Selected helper assertions VERIFIED historically, E07; all live paths UNVERIFIED |
| BR3 | Continue a company without losing or mixing owned progress | FR3: isolate slots, recover supported corruption and refuse unsafe overwrite | Supported unit cases VERIFIED historically, E05/E06; all refresh cases UNVERIFIED |
| BR4 | Experimental scenarios do not alter the owned company | FR4: independent scenario inputs/results | Initial render isolation VERIFIED historically, E08; exhaustive interactions UNVERIFIED |
| BR5 | Geographic information communicates its actual precision | FR5: distinguish simulated position, preset geometry, approximate custom corridor and real navigation | Implementation distinction VERIFIED, E09; trustworthy labels/route creation still incomplete |
| BR6 | Remote access protects each user's data | FR6: agree on cloud contract, authorize ownership and handle device conflicts | PROPOSED acceptance target; live behavior UNKNOWN, E13 |
| BR7 | Public project evidence excludes private source/data and unsupported claims | FR7: separated evidence, sanitized artifacts, review and owner-approved publication | DOCUMENTED requirement E01; handoff checks recorded in publish review |

## Non-functional requirements

- NFR1 — PROPOSED security: no privileged secrets, private endpoints, customer exports or private evidence in public artifacts; validate ownership and untrusted data at actual boundaries.
- NFR2 — DOCUMENTED quality expectation: formula tests and reproducible checks; do not equate a test count with overall product correctness.
- NFR3 — PROPOSED usability: an understandable keyboard/mobile-capable core journey, actionable errors and honest terminology. Certification UNKNOWN.
- NFR4 — PROPOSED reliability: no duplicate financial posting on repeat/reload; no corruption-induced silent data loss; unsupported actions must fail visibly.
- NFR5 — PROPOSED performance: measure real interaction/loading behavior against recorded project budgets. No Web Vitals or field-performance achievement is claimed here.

## Business rules and exceptions

**VERIFIED helper inspection/tests, E04:** crew assigned to another bus must not become free staff for a second bus; live-trip crew changes and unsafe service/dispatch cases are guarded. These are simulation rules, not statutory staffing advice.

**VERIFIED helper assertions, E07:** consumed fuel expense differs from buying fuel inventory; checkpoint helpers reject/ignore unsupported or repeated financial applications as specified by their tests. This does not prove every store transition uses those guards.

**VERIFIED supported persistence assertions, E05/E06:** slot data is isolated; a valid same-slot backup can recover a corrupt primary; supported migration preserves owned assets; certain corrupt/future inputs are refused without destructive mutation.

**PROPOSED:** route permission, road geometry and legal operating permission remain separate concepts. A game permit is not a real licence. Real prices, legal fees, cash-flow forecasts and demand need independent validation.

## Outcomes and KPI plan

**VERIFIED limited outputs:** inspected implementation, local test/build records and sample screenshots. **UNKNOWN business outcomes:** user satisfaction, retention, operator efficiency, commercial revenue and investment return.

**PROPOSED measurements:** unassisted trip-completion rate, time to resolve blockers, unexplained cash deltas, repeat-credit incidents and reload failures. No baseline or improvement percentage has been measured. [RTM](requirements-traceability-matrix.md) tracks support and gaps rather than declaring all requirements complete.
