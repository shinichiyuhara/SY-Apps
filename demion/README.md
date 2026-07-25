# Demion

A native macOS archiver. Drop files or folders anywhere in the window — or on
the Dock icon — and Demion decides from the content: archives are extracted,
everything else is compressed, and a mixed drop asks.

## What it does

- **Content-based routing.** Both the extension and the magic bytes are
  checked, so a mislabelled file is still handled correctly. There is no drop
  target to aim at: format and level live in the always-visible compress
  toolbar, so an ordinary drop starts immediately. Ten or more items ask for
  confirmation first.
- **Ledger window (default).** One row per item — name, action, size, status —
  with a colour stripe marking compress or extract, a compress toolbar (format
  menu, level slider, inline Details for split size and behaviour toggles), and
  a bottom summary bar showing item count, compress/extract breakdown, total
  size, and output location. The earlier single-panel layout stays available as
  **View → Classic Window**.
- **Creates**: ZIP (store / deflate / auto — already-compressed data is stored,
  the rest deflated — with ZIP64), TAR, TAR.GZ, TAR.ZST, TAR.BZ2, TAR.XZ,
  single-file GZIP and Zstandard, and Apple Archive (`.aar`, LZFSE).
  Single-file gzip/zstd keep the original name (`1.webp` → `1.webp.gz`).
- **Extracts**: ZIP, TAR, GZIP, BZIP2, XZ, LZMA, 7z, Zstandard, RAR / CBR,
  Apple Archive, and Windows self-extracting archives. A self-extracting `.exe`
  is **never run** — Demion locates and verifies the 7z or ZIP payload appended
  to the executable and reads only that.
- **Smart subfolder extraction.** A single-item archive unpacks directly rather
  than into a redundant same-named folder; only multi-item archives get a
  wrapper. Configurable (never / multi-item only / always).
- **Cancellable queue** with per-job progress; cancelling deletes the partial
  output instead of leaving debris. Concurrency configurable 1–8.
- **Log panel** at the bottom of the window (⇧⌘L). Paths in the log are
  replaced with XXHash64 digests, so logs can be shared without exposing folder
  names.
- **Passwords.** ZIP archives can be password-protected, and protected ZIPs
  (plus encrypted RAR) can be opened. **WinZip AES-256** is the default —
  readable by 7-Zip / Keka / WinZip, but not by Windows Explorer. Legacy
  **ZipCrypto** stays selectable for very old extractors; it is breakable in
  practice and the app says so next to the password field. An empty password
  means no encryption, never a weak one.
- **English / Japanese** interface, chosen in Settings rather than inherited
  from the OS locale.

## Safety

- Fully offline: no network entitlement, no connections, no telemetry.
- Runs in the App Sandbox and touches only what you hand it.
- Entry paths that would escape the destination are refused (zip-slip); symbolic
  links are not followed out of the destination.
- Decompression-bomb size caps, with an explicit prompt offering to lift the
  cap, open Settings, or cancel — never a silent failure.
- macOS metadata (`._*`, `__MACOSX/`, `.DS_Store`) excluded from new archives by
  default.
- Filenames normalised to NFC, keeping Japanese and other non-ASCII names stable
  across systems.

## Not yet available

- **7z creation** — not supported, and not planned. 7z *extraction* works
  today, but **encrypted 7z cannot be opened**. Creating 7z would mean vendoring
  roughly 46,000 lines of C, and the permissively-licensed option cannot encrypt
  7z at all — so the cost would not even buy feature parity. Use ZIP with
  AES-256 when you need a password. (Password-protected **ZIP** works both ways,
  and encrypted **RAR** can be opened.)
- **RAR creation** is not possible for any third-party app: no open-source RAR
  encoder exists and the UnRAR license forbids building one. RAR is
  extract-only.

## Install

Requires macOS 14 (Sonoma) or later. [[APP_STORE_URL]]

## Privacy

Demion works entirely offline. Nothing is collected, transmitted, or shared.
Preferences, the optional diagnostic log, and the folder access grants you
approve stay on your Mac and can be erased from **Settings → Privacy**.

[Full privacy policy](privacy-policy.md)

## Suite

**Demion** is part of a small family of macOS apps:

- [Arkheion](../arkheion/) — read-only archive inspector with Quick Look
- [Pinakeion](../pinakeion/) — image-archive library manager
- [Skopeion](../skopeion/) — comic / image viewer (manga-tuned)

## Support

Bug reports and feature suggestions: shinichiyuhara1@gmail.com

## License

Proprietary. The binary is distributed via the Mac App Store. Third-party
library licenses (ZIPFoundation, SWCompression, BitByteData, zstd, bzip2,
minizip-ng, Unrar.swift) are bundled in the in-app **Settings → About /
Licenses** tab.
