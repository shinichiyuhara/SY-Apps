# Privacy Policy — Arkheion

Last updated: 2026-07-09

Arkheion ("the app") is a read-only archive inspector for macOS. It does not transmit any data over the network and does not share anything with the developer or third parties. This policy explains exactly what data the app touches on your Mac, where it lives, and how to remove it.

## What we don't do

- We do not collect or send any personal data off your Mac.
- We do not use analytics, crash reporting services, or advertising SDKs.
- We do not ship with any network entitlement (`com.apple.security.network.client`); the app cannot reach the internet for telemetry, automatic updates, or anything else.
- We do not sign you in to any account, cloud, or server backend.
- We do not share anything with the developer or any third party.

## What is stored locally

Everything below lives only on your Mac, inside the app's sandbox container (`~/Library/Containers/com.shinichiyuhara.Arkheion/`), and only if you opted into the corresponding feature.

- **Diagnostic logs** *(off by default)* — `Data/Library/Application Support/com.shinichiyuhara.Arkheion/Logs/` inside the sandbox container (files `arkheion.log`, rotated `arkheion.1.log`). Enable in Settings → Privacy. Rotates at 5 MB × 2 files (10 MB cap). Records archive opens, format detection, read failures, extraction events, and settings changes. Archive contents are never logged; by default the file and folder names that would appear in event lines and error messages are hashed, and appear verbatim only if you turn off name redaction in Settings.
- **Recent archives** — security-scoped bookmarks for the most recent N archives you opened.
- **Preferences** — language, encoding preference order, extraction destination, default extractor app, and other Settings values. Stored at `Data/Library/Preferences/com.shinichiyuhara.Arkheion.plist`.
- **File access grants** — when you grant Arkheion persistent access to a folder (Home / Volumes / chosen folder), the security-scoped bookmark is saved in the sandbox container so the grant survives launches.
- **Saved passwords** — when you tick "Remember in Keychain" on the unlock prompt for an encrypted archive, or when you set a default password in Settings → Password, the password is stored in the **macOS Keychain** as a generic-password item under service `com.shinichiyuhara.Arkheion.passwords`. The account label is a SHA-256 digest of the archive's absolute path for per-archive entries, or the constant `__default__` for the default password. Stored with `kSecAttrAccessibleWhenUnlockedThisDeviceOnly`; never synced to iCloud, never available before login.
- **Quick Look preview temp files** — when you Space-preview a file inside an archive, its bytes are staged to `Data/tmp/Arkheion-QL/` inside the sandbox container so macOS Quick Look can render them. These are removed when the preview closes, swept on the next launch, and cleared by Erase All Personal Data.

Nothing in this list ever leaves your Mac.

## How to delete the data

Open **Settings → Privacy → Erase All Personal Data**. This removes every diagnostic log file, every saved Keychain password, every security-scoped bookmark, every Quick Look preview temp file, the Recent Archives list, and resets preferences to defaults in one action. The bundle itself stays installed; every byte the app wrote to your disk goes away.

## Extraction and "Open with"

When you extract entries, the files land in the destination you pick at that moment — either the original archive's folder, a fallback folder you configured under **Settings → Extraction**, or a folder selected via the system save panel. Arkheion only writes to paths you explicitly authorize. The Launch Services hand-off ("Open with Archive Utility / Keka / …") passes the archive URL to the OS; Arkheion itself does not read, copy, or transmit the file's contents during this hand-off.

## Quick Look extensions

The bundled Quick Look preview extension (`ArkheionPreview.appex`) runs inside macOS's extension host process. It receives only the archive URL Finder hands it, reads its contents to render the entry listing, and shares no preferences, Keychain entries, recent-archives history, or other state with the main Arkheion app.

## Children

Suitable for ages 4+. No advertising, no in-app purchases, no links to external services beyond the App Store itself.

## Contact

Questions or concerns: shinichiyuhara1@gmail.com
