# Arkheion

A sandboxed, read-only archive inspector for macOS — browse and preview every common format without unzipping, or hand off to your favourite extractor.

## What it does

- Opens ZIP / TAR / GZIP / BZIP2 / XZ / LZMA / 7-Zip / Zstandard / RAR / CBR in a single window. **Read-only by design — never modifies archive contents.**
- Bundled Finder Quick Look preview extension: Space-key entry-list preview, four columns (Name / Size / Modified / Kind), folder collapse, striped rows.
- Inline previews without unzipping — text, source code, JSON (pretty), Markdown, RTF, HTML (CSP-locked), CSV/TSV table, images (pinch / wheel zoom), PDF, and an Apple Quick Look fallback for Office / iWork / audio / video / 3-D / PSD.
- Quick Preview window: select a file inside Arkheion, press Space for a larger preview with arrow-key navigation through the whole archive; Escape closes.
- EPUB metadata: title, chapter count, Dublin Core fields shown in the status bar.
- Smart character-set recovery for Japanese / Korean / Chinese archives from old Windows tools (UTF-8 / Shift_JIS / CP949 / GBK / Latin-1 in a configurable preference order).
- Encrypted RAR and ZIP prompt for a password and offer to remember it in the macOS Keychain; ZIP covers WinZip AES (128/192/256-bit) and traditional encryption. One default password can unlock anything that shares the same key. Encrypted 7-Zip is flagged as unsupported instead of silently dropping entries.
- Open with your favourite extractor — toolbar button + `File → Open with Default App` (⌘⇧O) + right-click hand the archive to Archive Utility / Keka / BetterZip / whichever app Launch Services has registered.
- Extraction with guardrails: path-traversal blocked, configurable destination (source folder / fallback / always ask), smart auto-subfolder wrap, macOS metadata filter, quarantine xattr propagation, optional trash-source-after-extract.
- Decompression-bomb defence: 4 GiB compressed / 8 GiB uncompressed cap surfaces malicious "tiny → huge" payloads as a clear size-limit message instead of stalling the app.
- Folder Expand / Collapse All across every subtree (⌥⌘E / ⇧⌥⌘E), in the main app and the Quick Look preview header alike.
- Persistent folder access across launches via security-scoped bookmarks; English / Japanese interface (runtime-switchable), light + dark icon.
- Built-in activity log panel (toolbar / View menu / ⇧⌘L): a resizable bottom dock mirroring what Arkheion is doing, with a severity filter, copy, and clear. File and folder names written into log lines are hashed by default, and everything is erasable from Settings.

## Install

Coming to the Mac App Store — requires macOS 14 (Sonoma) or later. Sibling apps in the suite (Skopeion, Pinakeion, Kineion) are also pre-release; the cross-links below point at their own GitHub mirrors, not live App Store records yet.

## Privacy

Arkheion works entirely offline. It ships without any network entitlement — no analytics, no crash reports, no telemetry, no advertising. Diagnostic logs are off by default; saved Keychain passwords stay local to your Mac and are never synced to iCloud. A single **Settings → Privacy → Erase All Personal Data** button wipes logs, Keychain passwords, bookmarks, and Recent Files.

[Full privacy policy](privacy-policy.md)

## Suite

**Arkheion** is part of a small family of macOS apps:

- [Skopeion](../skopeion/) — comic / image viewer (manga-tuned)
- [Pinakeion](../pinakeion/) — image-archive library manager
- [Kineion](../kineion/) — video library manager (external-player based)
- [LexxUp](../lexxup/) — EPWING dictionary reader (cross-dictionary search)

## Support

Bug reports and feature suggestions: shinichiyuhara1@gmail.com

## License

Proprietary. The binary is distributed via the Mac App Store. Third-party library licenses are bundled in the in-app About window.
