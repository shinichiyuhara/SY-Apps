# Privacy Policy — Demion

Last updated: 2026-07-19

Demion ("the app") does not collect, transmit, or share any personal
information.

## What we don't do

- We do not collect any personal data.
- We do not use analytics, crash reporting services, or advertising SDKs.
- We do not establish network connections. The app ships without any
  network entitlement, so it cannot make one.
- We do not transmit or share your files, filenames, or archive contents.

## What is stored locally

Stored only on your Mac (macOS UserDefaults, the Keychain, or the app's
sandbox container under
`~/Library/Containers/com.shinichiyuhara.Demion/Data/`):

- **Preferences**: chosen archive format and compression level, split
  size, extraction destination policy, subfolder behaviour, macOS
  metadata exclusion, size caps, concurrency, interface language, window
  and panel state. Stored in UserDefaults under the `Demion.*` keys.
- **Optional diagnostic log** (toggle from Settings → Diagnostics):
  written to
  `~/Library/Containers/com.shinichiyuhara.Demion/Data/Library/Application Support/com.shinichiyuhara.Demion/Logs/`,
  auto-rotated. File paths written into the log are replaced with
  XXHash64 digests, so the log records what happened without recording
  your folder or file names.
- **File access grants**: security-scoped bookmarks for folders you
  explicitly authorised in Settings → File Access, so the app can reach
  them again on the next launch. Nothing is accessed without your
  approval.
- **Default password (Keychain)**: only if you set one in Settings →
  Password. It is held in the macOS Keychain on this device and is never
  synced anywhere by the app. Passwords you type for a single archive are
  used for that job and not stored.

Demion keeps no library, catalogue, or index of the files you process. The
archives it creates and the files it extracts are written where you tell
it to, and the app forgets them afterwards apart from the most recent
output location used by the "Show in Finder" command.

## How to delete the data

- Settings → Privacy lists every stored item above with its size, and
  **Erase All** wipes preferences, the log directory, the stored
  password, and all file access grants in one step.
- Individual items can be cleared from the same list.
- Removing the app from /Applications and deleting
  `~/Library/Containers/com.shinichiyuhara.Demion/` removes everything
  else.

## Children

The app is suitable for ages 4+ and contains no advertising, no in-app
purchases, and no links to external services.

## Contact

Questions or concerns: shinichiyuhara1@gmail.com
