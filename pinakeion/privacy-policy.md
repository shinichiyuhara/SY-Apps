# Privacy Policy — Pinakeion

Last updated: 2026-07-09

Pinakeion ("the app") does not collect, transmit, or share any
personal information.

## What we don't do

- We do not collect any personal data.
- We do not use analytics, crash reporting services, or advertising SDKs.
- We do not establish network connections.
- We do not transmit or share your reading habits or files.

## What is stored locally

Stored only on your Mac (UserDefaults, the app's local SQLite catalogue, or
its Caches / Logs directories):

- **Library paths**: folder paths you registered as Libraries, plus the
  security-scoped bookmarks needed to re-open them across sessions.
- **File Access grants**: broad sandbox bookmarks for your home folder
  or external volumes that you authorised in Settings → File Access.
- **File metadata**: filenames, file sizes, modification dates, added
  dates, relative folder paths inside each Library, parsed titles /
  author names inferred from filenames, image count per archive,
  format kind (archive or loose image).
- **Per-archive state**: favourites, ratings, read / unread status
  with the timestamp you marked it read.
- **Optional usage statistics** (on by default; toggle from Settings →
  Diagnostics → Usage Statistics): open count and last-opened timestamp
  per archive — drives the Recently Opened and Most Opened smart
  folders. Pinakeion is a previewer and hands reading off to an external
  app, so it does not track reading time or page-by-page progress.
- **Optional diagnostic log** (off by default; toggle from Settings →
  Diagnostics → Log): written to `~/Library/Logs/Pinakeion/`,
  auto-rotated at 5 MB with one backup kept.
- **Cover thumbnails**: JPEG cache under
  `~/Library/Caches/Pinakeion/thumbnails/`.
- **Quick Preview cache**: 5×4 page grid renders under
  `~/Library/Caches/Pinakeion/previews/`, capped at 500 MB with
  oldest entries evicted first.
- **Search index**: FTS5 trigram index over filenames / parsed titles
  / parsed authors. Derived from the file metadata above; kept inside
  the local SQLite catalogue; never sent anywhere.
- **Preferences**: view mode, sort field / direction, tile width,
  sidebar / inspector / folder browser visibility. Stored in macOS
  UserDefaults + the local catalogue.
- **Folder-bookmark integrity key**: a random key held in the macOS
  Keychain (this device only, never synced to iCloud), used to verify
  that the saved security-scoped folder bookmarks have not been
  tampered with. It is not a password and unlocks nothing on its own.

## How to delete the data

- Settings → Privacy → **Delete All Personal Data** wipes the
  catalogue, thumbnails, preview cache, preferences, and the
  diagnostic log directory in one step.
- Settings → Thumbnails → **Clear All Thumbnails** wipes only the
  thumbnail cache.
- Settings → Thumbnails → **Clear Preview Cache** wipes only the
  Quick Preview page cache.
- Settings → Diagnostics → **Clear Logs** wipes only the diagnostic
  log directory.

## Children

The app is suitable for ages 4+ and contains no advertising, no in-app
purchases, and no links to external services.

## Contact

Questions or concerns: shinichiyuhara1@gmail.com
