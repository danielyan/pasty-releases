# Pasty releases

Update feed and signed archives for **Pasty**, a menu-bar macOS app: a small,
terminal-looking text box that opens on a hotkey, and copies what you typed to
the clipboard.

This repository holds only distribution artifacts — the application source lives
elsewhere and is private. Everything here is published automatically by Pasty's
release workflow; nothing is edited by hand.

## What's here

| Path | What it is |
|---|---|
| `appcast.xml` | The [Sparkle](https://sparkle-project.org) update feed the app polls |
| `Pasty-*.zip` | Notarized, stapled application archives |
| `Pasty-*.html` | Release notes for the matching archive |
| `old_updates/` | Archives retired from the feed by `generate_appcast` (not published) |

Served over GitHub Pages at <https://danielyan.github.io/pasty-releases/>.

## Installing

<!-- download:begin — rewritten by the release workflow -->
**[Download Pasty 0.1.0](https://danielyan.github.io/pasty-releases/Pasty-0.1.0.zip)** — macOS 14 or later.
<!-- download:end -->

Download the newest `Pasty-*.zip`, unzip it, and move `Pasty.app` to
`/Applications`. The app updates itself after that — Pasty checks this feed on
a schedule, and on demand from **Check for Updates…** in its menu.

Builds are signed with a Developer ID certificate and notarized by Apple, and
each update is additionally signed with an EdDSA key that the app verifies
before installing anything.
