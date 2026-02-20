# Field Tweaks

Helpers that improve field authoring hygiene without changing Backdrop core. It delivers two opt-in features:

1. Suggest machine names that include the target bundle machine name when creating a new field (backdrop/backdrop-issues#6172), as an opt-in UX aid with optional custom prefix override.
2. Provide trimming of leading/trailing whitespace for text-based fields before they are saved (backdrop/backdrop-issues#6386), with bundle-level modes: off, trim all, or enable per-field toggles.

## Admin surface

- Per-content-type toggles on a secondary tab under `Manage fields` (e.g., `.../manage/post/fields/tweaks`), including custom machine-name prefix and trim mode selection, stored in `field_tweaks.settings`.
- When trim mode is set to per-field, a checkbox appears on text field instance settings (Edit tab) to enable trimming for that field.

## Install

Place the module in `modules/custom`, enable it, then configure per content type under `Manage fields > Settings`.

## Notes

- Keep features opt-in to avoid surprises with shared fields and existing content.
- Machine name suggestions must respect the 32-character limit and shared-field workflows.
- Trimming should run late in presave to catch programmatic writes as well as UI submissions.
