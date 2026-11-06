# Testing, evidence and publication limits

Date: 6 November 2026, Asia/Dhaka. Application baseline: `326f0b835171aa29b221651cf4f735293096065a` on main. Environment: Windows, Node 24.13.0; installed Vite 6.4.5, Vitest 3.2.7; screenshot browser Chrome 156.0.8078.80. No recovery-branch test results are borrowed.

## Checks executed for this package

| Check | Recorded result | What it does not establish |
| --- | --- | --- |
| `npm test` | **454 passed, 31 files**, exit 0 | All UI flows, real-world model accuracy or production readiness |
| `npm run build` | Exit 0, no build warnings | Deployment, clean installation or all runtime behavior |
| Main JS build artifact | 458.70 kB; gzip 117.58 kB | Whole-page download size, LCP or INP |
| `node scripts/capture-portfolio.mjs` | Three real screenshots; tab navigation and no desktop horizontal overflow; runtime exceptions `[]` | Dispatch/settlement, refresh, slot switching, mobile, a11y or full network verification |
| Screenshot-session console | 0 warning calls, **3 error-level calls** | Cause not classified; do not describe the console as clean |
| `npm audit` | 2 critical, 1 moderate, 0 high findings | Reachability/remediation not established in this task |
| `npm audit --omit=dev` | Zero reported findings | Absence of unknown vulnerabilities or application-level security flaws |

Full-tree dependency findings remain open; no forced upgrade or audit suppression was performed. Review and remediate them before treating this as a production release. No full design-gate result is asserted for this baseline during this task; constraints remain in force.

## Automated coverage inspected

Tests include calculator formulas, fuel/checkpoint helpers, purchases, readiness/crew boundaries, persistence/migration/backup cases, route geometry, scheduling, banking and selected scenario/stress suites. Some tests under `tests/e2e/` run with Vitest; their directory name does not make them real-browser end-to-end tests.

The existing `scripts/verify-fleet-browser.mjs` is a separate broader browser workflow. It was not rerun for this documentation package. There is no newly verified complete acquisition-to-settlement/reload demonstration of main in this task.

## Screenshot provenance and reproduction

Start the local app with `npm run dev` on port 3000. The capture script expects a **dedicated, non-personal Chrome instance** exposing DevTools at `http://127.0.0.1:9223`; do not attach it to your daily authenticated browser. It creates a disposable browser context, loads a fresh guest company, switches to English labels, pauses via real input events, opens three tabs and disposes that context. It never imports personal saves or reads authentication material.

```sh
node scripts/capture-portfolio.mjs
```

Outputs under [screenshots/](screenshots/):

- [Operations](screenshots/operations.png): paused default company and map; attribution retained.
- [Fleet](screenshots/fleet.png): readiness/dispatch interface; no claim that a trip was dispatched in this capture.
- [Business Lab](screenshots/business-lab.png): scenario inputs and displayed projections; not validated investment figures.
- [Evidence manifest](screenshots/evidence.json): source commit, timestamp, viewport, browser, runtime counts, image hashes and limits.

All three images were visually inspected. They are ordinary viewport screenshots at 1440 × 1000, not full-page captures, generated mockups or retouched UI. The script requires network access for tiles/external assets; it asserts at least one tile loaded, not completeness of every network response. Regeneration replaces these named generated evidence files; preserve the originals if you need historical comparisons. Its manifest will identify whichever commit you run it against.

## Not checked / unresolved

- Owner-reported confusing/broken gameplay and browser-specific refresh problems; screenshot smoke does not close them.
- Complete Career/Lab/timed/instant/day/offline financial equivalence and duplicate-payment resilience across every path.
- Current road legality, bus restrictions, regulatory fees, market prices, demand or feasibility predictions.
- Live cloud tables, RLS, two-user access isolation, device conflicts or production auth behavior.
- Mobile/tablet responsive audit, keyboard/screen-reader use, contrast, Lighthouse/Web Vitals and long-session performance.
- Clean-clone installation, deployed demo, external usability study, paying customers or commercial operation.
- Comprehensive secret/history/PII audit and third-party asset redistribution permission. A bounded publication scan is not a security certification.

Before any production release, verify secrets/config exclusions, licensing and the unresolved security/quality gates. Publishing this documentation does not constitute deployment or production/security approval.
