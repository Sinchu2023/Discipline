# Architecture Overview and Refactor Direction

This document describes the current architecture, the rationale behind recent structure changes, and the recommended next migration steps.

## 1) Problem Statement (Before Refactor)

Previously, the application logic and presentation concerns were highly concentrated:

- HTML included structure, inline styles, and script-heavy logic.
- Runtime behavior, state handling, analytics, and orchestration lived in tightly coupled sections.
- Class names suggested separation of concerns, but file boundaries were not enforcing those boundaries.
- Direct DOM coupling made testing, onboarding, and isolated debugging more difficult.

## 2) Current Baseline Architecture

The project now has a clearer separation between shell, styling, and behavior:

- `index.html` → application shell and mount points
- `assets/css/app.css` → centralized styling
- `assets/js/app.js` → current runtime logic and managers

This gives the app a stable baseline while preserving behavior.

## 3) Architectural Principles

The ongoing direction follows these principles:

1. **Behavior preservation first**: avoid regressions while extracting modules.
2. **Explicit ownership**: each module owns a bounded responsibility.
3. **Local-first reliability**: keep storage contracts stable through migration.
4. **Incremental extraction**: split by domain, not by arbitrary file size.
5. **Testability**: reduce hidden coupling to make logic unit-test friendly.

## 4) Proposed Module Topology

Target folder responsibilities:

- `core/` → state model and shared state lifecycle
- `ui/` → shell management and progressive disclosure views
- `execution/` → execution mode helpers and focus workflows
- `shadow-engine/` → benchmark logic and comparison adapters
- `trainer/` → recommendation logic and behavior nudges
- `analytics/` → KPI aggregation and historical insights
- `services/` → synchronization and integration services

## 5) Integration Strategy

- Keep a single top-level controller for app startup and wiring.
- Use state-centric interfaces between modules (instead of implicit DOM reach-ins).
- Preserve existing storage key contracts during migration.
- Introduce explicit manager APIs before moving logic into separate files.

## 6) Migration Phases

### Phase 1 (Completed Baseline)
- Externalized CSS and JS from HTML shell.
- Established clearer top-level directories by responsibility.

### Phase 2 (In Progress / Recommended)
- Extract state bootstrap and app-wide state transitions to `core/state-manager.js`.
- Move UI shell orchestration to `ui/shell-manager.js`.
- Centralize synchronization behavior in `services/state-sync.js`.

### Phase 3 (Recommended Next)
- Split major domains from `assets/js/app.js` into dedicated modules.
- Introduce a lightweight event bus/pub-sub layer for cross-domain events.
- Add domain-focused tests (analytics, shadow benchmark, anti-sandbag rules).

## 7) Expected Outcomes

- Lower regression risk through smaller, purpose-specific modules
- Faster onboarding for contributors
- Improved maintainability and debuggability
- Better readiness for CI checks, linting, and future API integration
