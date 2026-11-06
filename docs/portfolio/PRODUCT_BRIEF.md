# Product brief: scoped PRD and product-management plan

Status: current-main documentation, not a commitment that all requirements are complete. Source baseline `326f0b8`; reviewed 6 November 2026. Approximately one month of development, with daily work ongoing according to the owner. No invented delivery date or time log.

## Problem and intended users

The product explores bus-company management in a Bangladesh setting while allowing separate what-if operating scenarios. Intended users are management-simulation players, learners exploring transport economics and reviewers evaluating the engineering prototype. Actual user adoption and willingness to pay have not been measured.

## Product hypothesis

A player can understand the consequences of preparing, dispatching and expanding a fleet if vehicle readiness, route assumptions, journey status and financial results stay connected. The Business Lab can support learning if inputs, assumptions and uncertainty are visible. Neither hypothesis has been validated by a formal user study.

## Minimum useful journey

Select a bus → choose a permitted corridor → resolve fuel/crew/condition blockers → confirm dispatch → follow simulated progress → inspect trip result and cash movement → reload the same company.

For Business Lab: select vehicle/route → adjust fare, occupancy and costs → inspect results and assumptions without mutating Career state. Results are educational scenarios, not financial recommendations.

## Current scope versus requirements

| Capability | Current evidence | Required before treating it as reliable |
| --- | --- | --- |
| Operations/Fleet/Lab workspaces | Implemented; captured and navigated in current desktop browser smoke | Task-based usability review and mobile/keyboard checks |
| Fleet readiness and preparation | Source and unit tests for guards/service/crew; interfaces visible | Full purchase/prepare/dispatch scenario against this exact version |
| Journey and financial settlement | Timed/instant/day paths and calculation tests exist | Equal-input parity, idempotent settlement, insufficient-cash and reload checks across all live paths |
| Route creation | Preset geometry; custom terminal corridor builder exists | Road-network-backed custom geometry and stable trip snapshots; no success on routing failure |
| Local saves | Version-5 envelope, migration and corruption/backup tests | UI refresh/slot rehearsal, offline-popup accounting review and browser-specific failure reproduction |
| Account/cloud | Supabase client exists | Schema agreement, two-user RLS tests, save conflicts and graceful network failure |
| Feasibility analysis | Adjustable scenario outputs and isolation test | Explicit assumptions and independently verified inputs; full cash-flow methodology if advertised |
| Multi-division economy/progression | Design ambition and partial code/interfaces | Separate specification and end-to-end proof; not an available complete game |

## Acceptance criteria for the next playable slice

These are open requirements, not reported test results:

1. A fresh guest can prepare and dispatch one bus without hidden blockers or unrelated popups; every blocker has a visible corrective action.
2. The route line and marker share a documented path; the interface distinguishes simulated position from GPS and approximate corridors from road routing.
3. Fuel, tolls, wages and receipts reconcile to one trip record and the company cash delta. Timed and instant completion agree under equal assumptions; repeat completion cannot credit twice.
4. A refresh retains the company and active trip without duplicate settlement, unexplained charges or an unavoidable report. Never require clearing storage to continue.
5. The same journey can be completed on a 360px viewport and with keyboard navigation; errors explain what failed and how to recover.

## Priorities and roadmap

| Priority | Work | Exit evidence |
| --- | --- | --- |
| Now: portfolio baseline | README, actual screenshots, scoped product/engineering/test reports | Working links, identified source commit, honest limitations and no private data |
| P0: core loop | Preparation, dispatch, settlement and reload reliability | Repeatable end-to-end browser scenario plus formula assertions |
| P0: financial/data trust | Shared transitions and clear cash versus profit labels | Equal-input parity, duplicate-credit guards, documented data assumptions |
| P1: route trust | Approved-terminal route creation and path persistence | Saved real road path used by map and active journey; provider failure has no charge |
| P1: security and usability | Dependency triage, cloud contract/RLS, responsive/a11y gates | Recorded passing checks or explicit unresolved blockers; no silent waivers |
| Later | Onboarding, progression, multi-division and advanced fleet systems | Separate small specifications after the core loop passes |

Dependencies matter: account/device sync must not be advertised before local persistence and schema/security behavior are proven. Avoid new catalogs or dashboards merely to grow the feature count.

## PM approach and success measures

Work in small slices: define the user outcome, add the relevant test, implement, check in the browser and record evidence. Stop after two unsuccessful repair attempts for a given issue and report the blocker instead of starting a broad loop.

Future measures should include unassisted trip completion rate, time to resolve readiness blockers, cash-reconciliation discrepancies and reload failures. No baseline, conversion rate, retention metric or improvement percentage has been measured, so none is presented as an achievement.

Scope changes belong in a decision log. Owner feedback is discovery evidence, not a request to implement every proposed feature simultaneously. Existing PRD (source-only reference) and game design (source-only reference) retain the long-term vision; this brief narrows the next verifiable work without deleting it.
