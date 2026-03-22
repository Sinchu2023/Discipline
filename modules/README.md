# Module Map

This project is organized into domain-oriented modules so each area of behavior has a clear owner.

## Directory Responsibilities

- `/core`  
  Shared state management and foundational application state access.

- `/execution`  
  Execution-mode workflows, focus helpers, and quick presets.

- `/shadow-engine`  
  SHADOW benchmark adapters and advanced self-competition computations.

- `/trainer`  
  Recommendation generation and guidance logic.

- `/analytics`  
  Long-range metrics, KPI rollups, and insight synchronization.

- `/ui`  
  Mission Control-first shell navigation and progressive disclosure flows.

- `/services`  
  Cross-module orchestration and state synchronization services.

## Notes

Legacy runtime behavior still exists in `assets/js/app.js` to preserve timer behavior and existing mechanics while modularization continues.
