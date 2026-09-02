---
name: wp-update-radar
description: Use when deciding whether to update one or more public wordpress.org plugins and current public support-forum evidence would help.
---

# WP Update Radar

Use `wp_update_radar_check` for one plugin and exact release. Use
`wp_update_radar_check_many` for a site's list of public wordpress.org plugins
(up to 25).

Treat the result as bounded public-community evidence, never as a guarantee.

- `known-bad` and `wait` are reasons to pause and investigate.
- `update-now` means the observed forum volume is not unusual for that plugin;
  it does not prove the user's site is safe.
- `too-new` and `insufficient-data` mean the tool does not know enough yet.
- A plugin outside the tracked index must remain unknown, not assumed safe.

Do not use this tool as a CVE or malware check. Do not ask for WordPress
credentials, site backups, customer data, database exports, or private plugin
code: the tool does not need them and cannot use them.
