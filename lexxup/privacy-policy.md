# Privacy Policy — LexxUp

Last updated: 2026-07-18

LexxUp ("the app") does not collect, transmit, or share any personal
information. It runs entirely on your Mac and makes no network requests.

## What we don't do

- We do not collect any personal data.
- We do not use analytics, crash reporting services, or advertising SDKs.
- We do not establish network connections.
- We do not transmit or share your searches, files, or reading habits.

## What is stored locally

Stored only on your Mac (macOS UserDefaults, the app's local SQLite database, or
its Application Support / Caches directories):

- **Your dictionary folder** — read-only. You choose the folder; on the Mac App
  Store version a security-scoped bookmark is saved so the app can reopen it
  across launches. LexxUp reads the EPWING dictionaries in it to search and
  display entries, and never modifies, moves, or deletes your dictionaries.
- **History** — the entries you navigate to, grouped by day.
- **Bookmarks** — saved entries and the folders you organize them into.
- **Dictionary registry** — which dictionaries are enabled, their order, and the
  categories/groups you assign.
- **Recent searches** — your recent query terms.
- **Full-text search index** (optional; off by default) — an index over entry
  bodies, derived from your dictionaries, kept inside the local SQLite database
  and never sent anywhere.
- **Character-rendering resources** — GAIJI (external-character) maps and a
  cached image rendering of dictionary glyphs, kept in Application Support and
  Caches. These are derived rendering resources, not personal data.
- **Preferences** — interface language, display settings (font, size, spacing,
  colors, zoom, vertical writing), and behavior flags. Stored in macOS
  UserDefaults.
- **Activity log** — an in-memory diagnostic log shown in the app's log panel;
  it is not written to disk and is discarded when you quit. Dictionary file names
  and paths in it are redacted by default (Settings → Diagnostics).

App data lives under `~/Library/Application Support/Jisho/` and
`~/Library/Caches/`; preferences live in macOS UserDefaults. Nothing leaves your
Mac.

## Required-reason APIs

LexxUp declares only these Apple "required reason" APIs, used solely for the
app's own on-device function:

| API category | Reason code | Use in LexxUp |
|---|---|---|
| UserDefaults | CA92.1 | store your own settings |
| FileTimestamp | C617.1 | compare dictionary/index modification times to decide whether the full-text index needs rebuilding |
| DiskSpace | 85F4.1 | show the database / index size in Settings |

## How to delete the data

- Settings → Privacy → **Erase all app data** wipes your history, bookmarks,
  the dictionary registry, recent searches, and the full-text index in one step.
  Your dictionaries and cached rendering resources are preserved, as they are
  resources rather than personal data.

## Children

The app is suitable for ages 4+ and contains no advertising, no in-app
purchases, and no links to external services.

## Contact

Questions or concerns: shinichiyuhara1@gmail.com
