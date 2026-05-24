# Skopeion

A fast, distraction-free comic and image viewer for macOS — tuned for manga readers but at home with any image collection.

## What it does

- Reads ZIP / CBZ / RAR / CBR / 7z / TAR (gz / bz2 / xz) / Zstandard / PDF / EPUB and every common image format (JPEG, PNG, GIF, BMP, TIFF, WebP, AVIF, HEIC, JPEG 2000, RAW, and more).
- Right-to-left two-page spreads for manga, left-to-right for Western comics. First page shows alone as a cover.
- Smooth page turns: pages decoded ahead and behind in the background. Next volume's cover is pre-fetched so jumping between archives feels instant.
- Continuous reading across sibling archives. Stays out of your way under macOS App Sandbox.
- Bookmarks for archive pages **and** individual images in a folder; slideshow (1–60 s), webtoon vertical scroll, EXIF/IPTC metadata overlay, loupe (adjustable from the Show menu or `.` `,` `'` `;`), tile view, fullscreen (`f` or ⌃⌘F).
- 90° rotation in both directions; menu items show their shortcuts; toggle items use macOS-conventional checkmarks for current state.
- Open a folder of plain JPEG/PNG/etc. and navigate it just like an archive — ←/→ move between files, two-page spreads work, and the Inspector shows the same metadata.
- Error-log overlay (`l`) lists files in the current folder that were excluded from the image list (subfolders, unsupported formats, neighbouring archives) along with any per-page or per-archive load failures from the current session.
- Reading statistics with per-session detail (start, end, last page reached). On by default with a first-launch consent banner; one-click off in **Settings → Statistics**.
- Recovers garbled filenames in legacy Japanese / Korean / Chinese ZIPs (Shift_JIS / CP949 / GBK).
- Encrypted RAR support with password prompt + macOS Keychain cache.
- English / Japanese interface.

## Install

Coming to the Mac App Store — macOS 14 (Sonoma) or later, Apple Silicon required.

## Privacy

Skopeion works entirely offline. It does not transmit anything over the network and shares nothing with the developer or third parties.

Reading statistics are recorded by default — a first-launch consent banner lets you turn them off before any data is written. Stats stay on this Mac and are read only by Skopeion itself, powering the Top Archives list and per-session detail in **Settings → Statistics**.

Encrypted-archive passwords live in your macOS Keychain. Everything can be wiped from **Settings → Privacy → Delete All Data**.

[Full privacy policy](privacy-policy.md)

## Suite

**Skopeion** is part of a small family of macOS apps:

- [Pinakeion](../pinakeion/) — image-archive library manager
- [Arkheion](../arkheion/) — read-only archive inspector with Quick Look
- [Kineion](../kineion/) — video library manager (external-player based)

## Support

Bug reports and feature suggestions: shinichiyuhara1@gmail.com

## License

Proprietary. The binary is distributed via the Mac App Store under Apple's Standard EULA for licensed applications. Third-party library licenses (and the full Skopeion license text) are bundled in the in-app **Settings → About** tab.
