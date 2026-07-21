# Pinakeion

A macOS library manager for collections of image archives. Register one or more folders as Libraries, browse the whole catalogue through a fast sortable grid, double-click any archive to open it in your default reader.

## What it does

- Indexes ZIP / CBZ / RAR / CBR / 7z / TAR (gz / bz2 / xz / Zstandard) / PDF / EPUB plus every common image format (JPEG, PNG, GIF, BMP, TIFF, WebP, AVIF, HEIC, JPEG 2000, RAW, and more).
- Multi-Library catalogue across internal SSD, external HDD, or NAS — nested sub-folders tracked as a navigable tree; scans run incrementally so the grid populates while indexing is still in flight.
- Three-pane macOS-native layout (sidebar / folder tree / grid or list), each pane independently collapsible (⌘⌃S sidebar, ⌘⌃D folder browser, ⌘I inspector), plus a resizable inspector with cover preview, parsed metadata, and an interactive 5-star rating picker.
- Sidebar smart folders — Favorites, ★1–★★★★★, Read, Recently Added, Recently Opened, Most Opened, Broken — all covering-index backed and Library-scopable. The Broken folder gathers any archive Pinakeion couldn't read (corrupt container) so damaged files are easy to find and clear out.
- A tile with no cover explains itself instead of sitting blank — BROKEN, PASSWORD PROTECTED, FILE MISSING, OFFLINE, NOT DOWNLOADED or NO IMAGES, shown in the cover space and repeated in the list's status column. Red is kept for genuine damage: a missing file, an unmounted Library or an undownloaded iCloud placeholder read as recoverable, because reconnecting the drive or downloading the file brings them back.
- FTS5 trigram full-text search; substring matches on filename / parsed title / parsed author resolve in single-digit milliseconds even at 100 k+ archives, with native Japanese support.
- Cover extraction cached as a JPEG thumbnail; priority-aware queue keeps visible tiles fast and caps RAR at one concurrent decode so it never starves the rest. Tile labels keep the file extension (`.rar`, `.zip`, `.cbz`, …) so you can see the format at a glance.
- Live external-volume tracking: unplug a drive that hosts one of your Libraries and Pinakeion instantly flags it in the sidebar, drops its archives from smart folders, and stops queueing thumbnails it can't reach — replug and prefetch picks up where it left off. No manual rescan, no relaunch.
- Built-in Quick Preview (Space / ⌘Y) renders the first 5×4 pages of ZIP / CBZ / EPUB / PDF so you can scan the artwork without launching an external reader; pages are disk-cached for instant re-open.
- Full menu-bar coverage with macOS-canonical shortcuts (⌘O open, ⌘Y quick preview, ⌘B favorite, ⌘U read, ⌘1–⌘5 rating, ⌘F find, ⌘R rescan current library, ⌘⌃D folder browser). Right-click context menus carry the same hints inline.
- Double-click opens the archive with the system default handler (whichever reader you've associated with the file type in Finder).
- **Remove from Library** (⌥⌘⌫) forgets an archive's catalogue entry while leaving the file untouched on disk; delete the file itself in Finder whenever you want.
- Library → Re-scan (and the toolbar Refresh button) purge orphan rows + their derived thumbnail / preview cache files, so a Finder-side delete is reflected end-to-end.
- Scanning skips cache, temp, and system folders, and never descends into your Apple Music, Photos, or other OS media libraries — so it stays fast, keeps the catalogue clean, and never triggers a media-access permission prompt.
- Settings → File Access grants broad sandbox access to your home folder or an external volume in one step, separate from the Library catalogue.
- English / Japanese interface; menu titles follow the in-app Language preference, not the OS locale.

## Install

[Available on the Mac App Store](https://apps.apple.com/app/id6772719033?mt=12) — requires macOS 14 (Sonoma) or later.

## Privacy

Pinakeion works entirely offline. No data is collected, transmitted, or shared. Library paths, metadata, thumbnails, favorites, ratings, and usage statistics (on by default, toggleable) live only on your Mac. Everything can be wiped from **Settings → Privacy**.

[Full privacy policy](privacy-policy.md)

## Suite

**Pinakeion** is part of a small family of macOS apps:

- [Skopeion](../skopeion/) — comic / image viewer (manga-tuned)
- [Arkheion](../arkheion/) — read-only archive inspector with Quick Look
- [Kineion](../kineion/) — video library manager (external-player based)
- [LexxUp](../lexxup/) — EPWING dictionary reader (cross-dictionary search)

## Support

Bug reports and feature suggestions: shinichiyuhara1@gmail.com

## License

Proprietary. The binary is distributed via the Mac App Store. Third-party library licenses are bundled in the in-app **Settings → Licenses** tab.
