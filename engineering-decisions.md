# Decision records and reconstructed rationale

Reviewed 6 November 2026. These are retrospective analytical records, not invented original ADRs. Observed choices are VERIFIED by inspection; reasons/alternatives below are INFERRED unless explicitly described as owner-documented. None claims a comparative benchmark or a historically rejected technology without evidence.

## D1 — Browser-first guest company

**Observed, E03/E05/E06:** company state can be stored locally with version/slot handling. **Reconstructed rationale:** local guest operation reduces initial dependence on accounts/connectivity. **Trade-off:** editable browser storage is not server-authoritative multiplayer data; corruption and device recovery need explicit handling. A server-first design is an analytical alternative, not a proven rejected proposal.

## D2 — Separate scenario workspace

**Observed, E08:** initial scenario render preserves the Career vehicle/route input data in its test. **Reconstructed rationale:** experimentation should not change owned-company balances/assets. **Trade-off:** duplicated assumptions/paths can drift. **PROPOSED follow-up:** equal-input integration tests across all financial transitions, not just helper equality.

## D3 — Geographic display and custom corridors

**Observed, E09:** preset road geometry and approximate custom corridors coexist. **Reconstructed rationale:** bundled routes allow a geographic demo without requesting every path at runtime. **Trade-off:** street tiles can look authoritative while the selected path remains approximate. **PROPOSED:** distinguish permit, planned road, active trip and live position; never smooth a line merely to imply navigation correctness.

## D4 — Evidence-first public documentation

**DOCUMENTED current owner decision, E01:** source/configuration must remain private while product/engineering reasoning is shareable. **Observed, E15:** the previous export script copies an allowlist; it does not generate a case study. **Current handoff:** create separate private evidence and sanitized public reports, review exact artifacts, then publish with explicit owner approval. Blind every-push publication is not enabled or recommended here.

**Trade-off:** human review adds a deliberate checkpoint and prevents claims of zero-touch documentation. Draft generation, publication copying, test execution and screenshot capture are different capabilities. No complete reusable autonomous generator is claimed.
