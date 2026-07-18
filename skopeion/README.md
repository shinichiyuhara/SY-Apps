# Skopeion

A fast, distraction-free comic and image viewer for macOS — tuned for manga readers but at home with any image collection.

## What it does

- Reads ZIP / CBZ / RAR / CBR / 7z / TAR (gz / bz2 / xz) / Zstandard / PDF / EPUB and every common image format (JPEG, PNG, GIF, BMP, TIFF, WebP, AVIF, HEIC, JPEG 2000, RAW, and more).
- PDF table of contents: PDFs with a built-in outline show a Table of Contents sidebar — click an entry to jump to that page, with the current section highlighted. Toggle with `o` or the View menu.
- EPUBs read in their intended order, following the book's own spine instead of guessing from filenames — so pages stay in the right sequence even when files are named irregularly.
- Right-to-left two-page spreads for manga, left-to-right for Western comics. First page shows alone as a cover.
- Smooth page turns: pages decoded ahead and behind in the background. Next volume's cover is pre-fetched so jumping between archives feels instant.
- Continuous reading across sibling archives — Up / Down step to the previous / next archive at a page edge, Cmd+←/→ any time. Stays out of your way under macOS App Sandbox.
- Nested archives (zip-in-zip) are flattened; heavy formats buried inside (7z, bz2) wait behind an Expand button instead of unpacking behind your back, and macOS housekeeping files (`._*`, `__MACOSX/`, `.DS_Store`) are ignored so they never show up as phantom pages.
- Bookmarks for archive pages **and** individual images in a folder; slideshow (1–60 s), webtoon vertical scroll, EXIF/IPTC metadata overlay, loupe (adjustable from the Show menu or `.` `,` `'` `;`), tile view, fullscreen (`f` or ⌃⌘F).
- 90° rotation in both directions; menu items show their shortcuts; toggle items use macOS-conventional checkmarks for current state.
- Open a folder of plain JPEG/PNG/etc. and navigate it just like an archive — ←/→ move between files, two-page spreads work, and the Inspector shows the same metadata.
- Error-log overlay (`l`) lists files in the current folder that were excluded from the image list (subfolders, unsupported formats, neighbouring archives) along with any per-page or per-archive load failures from the current session.
- Reading statistics with per-session detail (start, end, last page reached). On by default with a first-launch consent banner; one-click off in **Settings → Diagnostics**.
- Recovers garbled filenames in legacy Japanese / Korean / Chinese ZIPs (Shift_JIS / CP949 / GBK) — now including very large multi-gigabyte archives.
- Encrypted RAR support with password prompt + macOS Keychain cache.
- English / Japanese interface.

## Install

Coming to the Mac App Store — requires macOS 14 (Sonoma) or later.

## Privacy

Skopeion works entirely offline. It does not transmit anything over the network and shares nothing with the developer or third parties.

Reading statistics are recorded by default — a first-launch consent banner lets you turn them off before any data is written. Stats stay on this Mac and are read only by Skopeion itself; turn them off any time in **Settings → Diagnostics**.

Encrypted-archive passwords live in your macOS Keychain, and the bookmarks that remember your granted folders are encrypted at rest. Filenames are scrubbed from diagnostic logs. Everything can be wiped from **Settings → Privacy → Delete All Data**.

[Full privacy policy](privacy-policy.md)

## Suite

**Skopeion** is part of a small family of macOS apps:

- [Pinakeion](../pinakeion/) — image-archive library manager
- [Arkheion](../arkheion/) — read-only archive inspector with Quick Look
- [Kineion](../kineion/) — video library manager (external-player based)
- [LexxUp](../lexxup/) — EPWING dictionary reader (cross-dictionary search)

## Support

Bug reports and feature suggestions: shinichiyuhara1@gmail.com

## License

Proprietary. The binary is distributed via the Mac App Store. Third-party library licenses are bundled in the in-app **Settings → About** tab.
