# Requirements Traceability Matrix

Traceability is not a completeness certificate. Technical descriptions are sanitized; exact confidential source/assertion references are held in the private evidence index. VERIFIED unit scope and UNVERIFIED complete flows must not be conflated. Current execution status is in [Testing](../testing-and-limitations.md).

| Objective → business requirement | Product feature / technical boundary | Evidence and test support | Classification / remaining acceptance |
| --- | --- | --- | --- |
| BO1 → BR1 / FR1 | Fleet preparation; readiness/service/crew guards | E03/E04: fully staffed idle bus; all blocker codes; malformed inputs; independent crew; active-trip changes; service limits | VERIFIED helper support from recorded tests; complete preparation UI and AC1 OPEN |
| BO2 → BR2 / FR2 | Trip economics, fuel inventory and checkpoint helpers | E07: equal-input costs, P&L versus trip cash, fuel snapshot, duplicate/unknown checkpoint assertions | VERIFIED helper support; whole timed/instant/day/offline parity and AC2 OPEN |
| BO3 → BR3 / FR3 | Versioned local state and isolated slot backups | E05/E06: slot isolation, corruption recovery/refusal, migration and numeric repair | VERIFIED supported cases; browser refresh/offline behavior and AC3 OPEN |
| BO2 → BR4 / FR4 | Business Lab scenario state | E08: initial render preserves Career-owned vehicle/route inputs | VERIFIED initial isolation assertion; sliders, scenario methodology and AC4 OPEN |
| BO3 → BR5 / FR5 | Terminal corridor builder and map sampler | E09: preset geometry versus heuristic custom path; E10: displayed sample map | VERIFIED implementation distinction; genuine custom road routing/honest labels and AC5 OPEN |
| BO3 → BR6 / FR6 | Optional account/cloud boundary | E13: inspected contract disagreement; no live two-user/RLS result | UNVERIFIED; AC6 OPEN |
| BO4 → BR7 / FR7 | Public draft versus private evidence and publication gate | E01: owner rules; publish-review records allowed content/scans | DOCUMENTED requirement; bounded artifact checks VERIFIED only after recorded execution; AC7 reviewed at handoff |

## Non-functional traceability

| Requirement | Existing evidence | Gap |
| --- | --- | --- |
| NFR1 security/privacy | Bounded publication scan and separated evidence | No comprehensive app penetration test, RLS isolation or licensing clearance |
| NFR2 calculation verification | E07 plus local QA summary | Tests validate assumptions/implementation, not current Bangladesh market/legal accuracy |
| NFR3 accessibility/usability | E10 historical desktop screenshots | No new mobile/keyboard/screen-reader certification |
| NFR4 persistence/idempotency | E05/E06/E07 selected cases | No complete browser reload and repeat-settlement proof across every path |
| NFR5 performance | Build output exists | No measured production Web Vitals or representative-device performance result |

Evidence tags are not hyperlinks to private code. A reviewer can inspect the public test summary without receiving confidential implementation. Missing evidence remains a gap; linking a source file to a requirement would not, by itself, make the requirement pass.
