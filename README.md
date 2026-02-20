# Field Tweaks

Helpers that improve field authoring hygiene without changing Backdrop core. It currently targets two requests:

1. Suggest machine names that include the target bundle machine name when creating a new field (backdrop/backdrop-issues#6172), as an opt-in UX aid.
2. Provide a per-field option to trim leading/trailing whitespace for text-based fields before they are saved (backdrop/backdrop-issues#6386), defaulting to off.

## Status

This is scaffold only. Hooks are stubbed in `field_tweaks.module`; no behavior ships yet.

## Planned admin surface

- Per-content-type toggles on a new secondary tab under `Manage fields` (e.g., `.../manage/post/fields/tweaks`), stored in `field_tweaks.settings`.
- Per-field setting on text field instances to enable trimming.

## Install

Place the module in `modules/custom`, enable it, then configure at the path above once implemented.

## Notes

- Keep features opt-in to avoid surprises with shared fields and existing content.
- Machine name suggestions must respect the 32-character limit and shared-field workflows.
- Trimming should run late in presave to catch programmatic writes as well as UI submissions.