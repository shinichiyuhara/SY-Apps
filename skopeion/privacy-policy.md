# Privacy Policy — Skopeion

Last updated: 2026-07-30

Skopeion ("the app") does not transmit any data over the network and does not share anything with the developer or third parties. Reading-history data is recorded locally on this Mac only, and is read only by Skopeion itself — see *Reading statistics* below for details and how to disable it.

## What we don't do

- We do not collect or send any personal data off your Mac.
- We do not use analytics, crash reporting services, or advertising SDKs.
- We do not establish network connections of any kind. Menu items that open a web page hand the URL to your browser; Skopeion itself never opens a connection. See *Children* below for the full list of those links.
- We do not share anything with the developer or any third party.

## What is stored locally

Everything below lives only on your Mac, inside the app's sandbox container (`~/Library/Containers/com.shinichiyuhara.Skopeion/`):

- **Preferences** — reading direction, two-page mode, language, loupe size, preload counts, slideshow interval, and the like.
- **Per-archive resume index** — the last page you viewed in each archive, so you can pick up where you left off.
- **Bookmarks** — pages you marked with `b`, including a security-scoped reference to the source file so it survives Sandbox restarts.
- **Recent files** — up to 15 most recently opened files, also security-scoped.
- **Folder access grants** — when you grant a folder via Open Folder (`Cmd+Shift+O`), a security-scoped bookmark for that folder is saved so sibling-archive navigation keeps working between launches.
- **Reading statistics** *(on by default since v1.2, with a first-launch consent prompt)* — total opens, viewing seconds per archive, and per-session detail (start time, end time, last page reached, total pages). Recorded locally only. Skopeion shows them back to you as a Top Archives list and per-session detail in Settings → Statistics; they never leave this Mac. Disable any time in Settings → Diagnostics → "Record reading statistics", and erase via Settings → Privacy → "Delete All Data…". The first-launch banner lets you turn this off before any data is written. Stats stay on this Mac and are read only by Skopeion itself — Skopeion does not share them with any other app.
- **First-image cache** — a small PNG of each pre-fetched neighboring archive's cover, capped at 500 MB, stored under `~/Library/Caches/`. Lets the next-volume transition feel instant.
- **Optional error log** *(off by default)* — `~/Library/Logs/Skopeion/skopeion.log`, rotated past 5 MB.
- **Encrypted-archive passwords** — when you unlock an encrypted RAR, the password is stored in the **macOS Keychain** (not in plain text) so subsequent files don't have to be retyped.

Storage backends used internally: SQLite (for bookmarks, statistics, and per-archive page progress, via the GRDB.swift library), plus standard `UserDefaults` for small settings.

## How to delete the data

- **Delete All Data…** under Settings → Privacy wipes preferences, the SQLite database, the disk cache, folder bookmarks, keychain passwords, recent files, statistics, and logs in one go.
- Granular controls in the same tab:
  - Settings → Privacy → "Clear caches" removes only the first-image / decoded-page cache.
  - Settings → File Access lets you revoke individual folder grants without touching other data.
  - Settings → Diagnostics → "Delete Logs Now" removes the on-disk log file.
- Uninstalling the app via Finder also removes the sandbox container.

## Children

Suitable for ages 4+. No advertising and no in-app purchases. Skopeion does open a few links in your browser when you ask it to: the Mac App Store pages for our other apps, the sample-file download page on the project's public repository (Help → Download Sample Files), and the upstream pages of the bundled open-source licences listed in Settings → About. The app itself makes no network connections; following one of those links is always something you choose to do.

## Contact

Questions or concerns: shinichiyuhara1@gmail.com
