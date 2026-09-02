# WP Update Radar

## Install in Cursor

This repository is a Cursor Plugin as well as a Claude plugin. In Cursor,
install it from the Marketplace once it is approved, or add the remote MCP
endpoint below to a local `mcp.json` while the public beta is under review:

```json
{
  "mcpServers": {
    "wp-update-radar": {
      "url": "https://updates.utilityhouse.xyz/mcp/cursor"
    }
  }
}
```

WP Update Radar adds two free, remote MCP tools for one narrow question:
whether public wordpress.org support-forum activity for an exact plugin release
looks unusual for that plugin.

It is free during beta. It needs no account, key, payment method, WordPress
credential, or site access.

## What it does

- Checks one public wordpress.org plugin release.
- Checks up to 25 public wordpress.org plugin releases in one call.
- Returns the supporting forum threads and a bounded verdict.
- Returns `insufficient-data` or an error instead of guessing when coverage is
  not sufficient.

## What it does not do

- It does not update, back up, roll back, scan, or log in to a site.
- It is not a security advisory, CVE lookup, malware scan, or compatibility
  guarantee.
- It does not cover premium plugins, private plugins, themes, custom code, or
  host-specific behaviour.

## Data boundary

Only a public plugin slug and exact version are sent to the free endpoint.
The service retains aggregate daily outcome counts only; it does not retain
the request body, site address, plugin inventory, caller identity, or payment
data.
