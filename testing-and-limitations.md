# Testing, evidence catalog and limitations

Review date: 6 November 2026. Application baseline is unchanged from `326f0b8`; later development commits added documentation/export tooling. VERIFIED means a bounded observation/assertion, not universal correctness.

## Current and historical QA

| Check | Evidence / result | Boundary |
| --- | --- | --- |
| Current default parallel test attempt | FAILED: process memory exhaustion and worker-channel failure | Not counted as a completed pass |
| Current resource-limited test run | VERIFIED: `npm test -- --maxWorkers=1`, 454 passed / 31 files, exit 0 | Same suite, no tests/assertions removed; not whole-product certification |
| Current initial build attempt | FAILED: process memory exhaustion while run alongside tests | Not hidden by quoting an earlier successful build |
| Sequential build retry | Completion output was not retained after tool-session interruption | UNKNOWN result; no new success claimed and no indefinite retries |
| Earlier build of unchanged application | VERIFIED historical successful build; main chunk 458.70 kB, gzip 117.58 kB | Historical environment result, not current deploy or whole-page performance |
| Screenshots / tab navigation | VERIFIED historical local 1440 × 1000 guest capture; no runtime exception/desktop overflow | Three console error-level calls remain unresolved; no new deployed/session capture |
| Dependency audit | Earlier recorded full-tree 2 critical / 1 moderate; runtime-only zero | Latest audit attempt's completion output not retained; no new clean audit or reachability clearance claimed |

No dependency, memory setting, application configuration or quality threshold was changed to make these results pass. Build/reliability/security issues remain application work, not documentation achievements.

## Public evidence catalog

Exact confidential paths/assertion references remain in a separate private index. These IDs let a reviewer distinguish the basis of each claim without receiving private code.

| ID | Sanitized evidence | What it supports / does not support |
| --- | --- | --- |
| E01 | Owner brief, feedback and publication authorization | DOCUMENTED goals, contribution and self-reported duration; not market research |
| E02 | Existing requirements/design notes | DOCUMENTED vision and planned features, not completion |
| E03 | Application/workspace inspection | VERIFIED implementation structure, not whole-flow behavior |
| E04 | Readiness/service/crew unit assertions | VERIFIED supported guard cases; not every UI connection |
| E05 | Slot/backup/corruption assertions | VERIFIED supported local cases; not all reload/cloud behavior |
| E06 | Save-envelope/migration assertions | VERIFIED supported repair/refusal cases; not server authority |
| E07 | Financial/fuel/checkpoint assertions | VERIFIED selected formulas, equality and replay guards; not market validity or every live path |
| E08 | Initial scenario-render isolation assertion | VERIFIED non-mutation in that test only |
| E09 | Preset/custom-route implementation inspection | VERIFIED geometry-versus-estimate distinction; not navigation certification |
| E10 | Previously reviewed guest screenshots and capture record | VERIFIED bounded historical visual evidence, not production state |
| E11 | Git metadata | VERIFIED dated recorded milestones, not a month of daily work or all commit-message claims |
| E12 | Current test/build attempts and earlier recorded QA | Exact results above; failed/unavailable results remain visible |
| E13 | Cloud integration and historical setup inspection | VERIFIED contract disagreement; live RLS/schema UNKNOWN |
| E14 | Owner-provided demo address | DOCUMENTED public URL; availability/deployed commit/complete flow UNVERIFIED |
| E15 | Existing fixed-file exporter/manual workflow | VERIFIED file-copy mechanism, not an evidence-generating system |

## Screenshots and disclosure

The three images are unchanged copies of previously captured default guest-company UI, not imported customer records or generated mockups. Their sample balances/labels are game data, not evidence of a real operator's finances or employees. Captured viewport, original capture date and hashes are in [screenshot provenance](screenshots/evidence.json). Local URLs/debug endpoints/filesystem metadata are omitted from the new public manifest.

Map attribution is retained. The screenshots were visually inspected; no OCR/steganography or independent third-party rights audit is claimed. Provider/brand/font assets remain subject to their owners' terms. Existing publication is not proof of redistribution permission for every future use.

## Still unverified

Complete acquisition/preparation/dispatch/settlement/reload journeys; equal-input parity across every timed/instant/day/offline path; live database RLS/two-user/device behavior; market/legal/financial assumptions; mobile/keyboard/screen-reader behavior; Web Vitals; clean-clone setup; production headers/deployment; user satisfaction and commercial outcomes. Some tests in an 'e2e' directory run as unit/scenario tests and must not be described as real-browser end-to-end tests.

The public demo link is not a security endorsement. Do not submit sensitive business data or reuse personal passwords in a prototype. This package is a documentation handoff, not an application release or security certificate.
