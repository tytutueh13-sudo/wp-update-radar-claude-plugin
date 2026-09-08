---
name: wp-update-radar
description: Use when deciding whether to update one or more public wordpress.org plugins and current public support-forum evidence would help.
---

# WP Update Radar

Use `wp_update_radar_check` for one plugin and exact release. Use
`wp_update_radar_check_many` for a site's list of public wordpress.org plugins
(up to 25).

Treat the result as bounded public-community evidence, never as a guarantee.
Prefer `state`, `signal`, `reasonCodes`, `coverage`, `freshness`, and `unknowns`
over the legacy `verdict` field.

- `HOLD` and `WAIT` are reasons to pause and investigate.
- `GUARDED_ROLLOUT` means no elevated public signal was observed; stage, back
  up, and retain a rollback path.
- `NOT_ENOUGH_EVIDENCE` means the tool does not know enough to support a
  reading.
- A plugin outside the tracked index must remain unknown, not assumed safe.

Do not use this tool as a CVE or malware check. Do not ask for WordPress
credentials, site backups, customer data, database exports, or private plugin
code: the tool does not need them and cannot use them.
