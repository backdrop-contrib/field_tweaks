Field Tweaks
============

Field Tweaks adds opt-in conveniences for field creation and text hygiene:
bundle-prefixed machine-name suggestions (with custom prefix support) and
leading/trailing whitespace trimming for text fields (global or per-field).

Requirements
------------

This module has no additional dependencies beyond Backdrop core.

Installation
------------

- Place this module in `modules/contrib` and enable it.
- For each content type, open `Manage fields > Settings` to:
  - Enable bundle-prefixed machine-name suggestions and set an optional prefix.
  - Choose a trim mode: off, trim all text fields, or per-field control.
- If using per-field trim mode, edit individual text fields (Edit tab) and
 check “Trim leading/trailing whitespace on save.”
- Clear caches if new UI elements do not appear.

Issues
------

Report bugs and feature requests in this project’s issue queue.

Current Maintainers
-------------------

- [alanmels](https://github.com/alanmels)

Credits
-------

- Sponsored by [AltaGrade](https://www.altagrade.com)

License
-------

This project is GPL v2 software. See the LICENSE.txt file in this directory for
the complete text.
