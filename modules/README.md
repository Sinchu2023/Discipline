# Modules

- `core/`: app bootstrap, state, event bus, shared utilities.
- `ui/`: rendering layer and DOM updates.
- `logic/`: business rules (shadow, trainer, flow protocol, analytics).
- `services/`: persistence, import/export, sync integrations.

Current implementation is centralized in `assets/js/app.js` after extraction from inline script.
Next step is incremental class-by-class relocation into these module folders.
