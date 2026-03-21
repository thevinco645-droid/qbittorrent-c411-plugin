# C411 qBittorrent Search Plugin

Unofficial qBittorrent search plugin for `c411.org`.

Maintainer: `OptimusKoala`

## What it does

- Searches `c411.org` through its native Torznab API
- Downloads `.torrent` files through the API without exposing your API key in qBittorrent search results
- Supports qBittorrent Python search plugins (`nova3`)

## Files

- `c411.py`: the plugin
- `c411.json.example`: example configuration

## Install

1. Install `c411.py` from qBittorrent Search > Search plugins > Install a new one.
2. Put `c411.json` next to `c411.py` in the qBittorrent `nova3/engines` directory.
3. Restart qBittorrent if needed.

## Configuration

Create `c411.json` next to `c411.py`:

```json
{
  "site_url": "https://c411.org",
  "api_url": "https://c411.org/api",
  "api_key": "YOUR_API_KEY_HERE",
  "page_size": 100,
  "max_pages": 2,
  "debug": false,
  "debug_file": "c411.log"
}
```

## Notes

- This plugin is for a private tracker and requires a valid `c411.org` API key.
- For qBittorrent versions with built-in Torznab support, `c411.org` can also be configured directly as a Torznab indexer.
- If you enable debug, `c411.log` is created next to the plugin.

## Publishing checklist

Before publishing this plugin publicly:

1. Verify `c411.py` does not contain any personal key or URL.
2. Update the repository URL references if needed.
3. Host `c411.py` at a stable raw URL on GitHub.
4. Add the plugin to the qBittorrent unofficial plugins wiki.
