# Publishing `c411` to qBittorrent community resources

## Recommended target

For `c411`, the safest path is:

1. Publish the plugin in your own GitHub repository
2. Add it to the qBittorrent wiki page `Unofficial-search-plugins`

This is a better fit for a private tracker plugin that needs user-specific configuration.

## Why this route

- The qBittorrent wiki explicitly invites community-maintained plugins on the unofficial page.
- The unofficial private-sites section already lists plugins that require user credentials or local edits.
- `c411.org` already exposes a Torznab API, so a community-maintained plugin or a direct Torznab setup is a natural fit.

## Suggested repository contents

- `c411.py`
- `c411.json.example`
- `README.md`

## Wiki PR target

Repository:

- `https://github.com/qbittorrent/search-plugins.wiki.git`

File:

- `Unofficial-search-plugins.mediawiki`

Section:

- `Plugins for Private Sites`

Ready-to-edit row:

- See `wiki-entry.mediawiki`

## Optional core repo PR

If you still want to try an official code PR against `qbittorrent/search-plugins`, you would typically need:

1. `nova3/engines/c411.py`
2. an entry in `nova3/engines/versions.txt`

But because this plugin targets a private tracker and requires user-side configuration, wiki publication is the path I would recommend first.
