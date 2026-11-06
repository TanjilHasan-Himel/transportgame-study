# Acceptance criteria and present disposition

These are PROPOSED product acceptance criteria. A helper test does not close the complete criterion.

| ID | Criterion / requirement | Present disposition |
| --- | --- | --- |
| AC1 | FR1: a fresh guest resolves every readiness blocker through visible actions and dispatches once | OPEN; helper guards supported, complete UI task not newly verified |
| AC2 | FR2: timed/instant/day/offline paths under equal assumptions reconcile operating result and actual cash, including repeat/reload | OPEN; helper equality/checkpoint assertions do not certify all orchestration paths |
| AC3 | FR3: reload retains owned assets and active-trip state; supported corrupt saves recover/refuse without silent overwrite | PARTIAL unit support; browser/offline behavior OPEN |
| AC4 | FR4: all scenario input interactions remain isolated and results disclose uncertainty | PARTIAL initial-render support; complete interaction/methodology OPEN |
| AC5 | FR5: selected route and marker share a documented path, with truthful precision/GPS labels | OPEN; preset map sample is not real-time/bus-safe routing proof |
| AC6 | FR6: two users cannot access each other's cloud saves and device conflicts are safely resolved | UNKNOWN; no live database test |
| AC7 | FR7: exact sanitized public tree excludes private artifacts; evidence/status and image review recorded; owner authorizes publication | Artifact-level result in [publish review](../publish-review.md); does not imply app security |

**PROPOSED review method:** repeat the core journey from fresh and saved sample companies, compare calculations manually, test insufficient cash/crew/fuel/permit cases, interrupt/repeat completion and reload, then repeat on mobile/keyboard. Preserve failures and sample inputs. No fabricated user acceptance sign-off is attached.
