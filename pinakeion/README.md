# Pinakeion

A macOS library manager for collections of image archives. Register one or more folders as Libraries, browse the whole catalogue through a fast sortable grid, double-click any archive to open it in your default reader.

## What it does

- Indexes ZIP / CBZ / RAR / CBR / 7z / TAR (gz / bz2 / xz / Zstandard) / LHA / LZH / PDF / EPUB plus every common image format (JPEG, PNG, GIF, BMP, TIFF, WebP, AVIF, HEIC, JPEG 2000, RAW, and more).
- Multi-Library catalogue across internal SSD, external HDD, or NAS — nested sub-folders tracked as a navigable tree; scans run incrementally so the grid populates while indexing is still in flight.
- Three-pane macOS-native layout (sidebar / folder tree / grid or list), each pane independently collapsible (⌘⌃S sidebar, ⌘⌃D folder browser, ⌘I inspector), plus a resizable inspector with cover preview, parsed metadata, and an interactive 5-star rating picker.
- Sidebar smart folders — Favorites, ★1–★★★★★, Read, Recently Added, Recently Opened, Most Opened — all covering-index backed and Library-scopable.
- FTS5 trigram full-text search; substring matches on filename / parsed title / parsed author resolve in single-digit milliseconds even at 100 k+ archives, with native Japanese support.
- Cover extraction cached as a JPEG thumbnail; priority-aware queue keeps visible tiles fast and caps RAR at one concurrent decode so it never starves the rest.
- Built-in Quick Preview (Space / ⌘Y) renders the first 5×4 pages of ZIP / CBZ / EPUB / PDF so you can scan the artwork without launching an external reader; pages are disk-cached for instant re-open.
- Full menu-bar coverage with macOS-canonical shortcuts (⌘O open, ⌘Y quick preview, ⌘B favorite, ⌘U read, ⌘1–⌘5 rating, ⌘F find, ⌘R rescan current library, ⌘⌃D folder browser). Right-click context menus carry the same hints inline.
- Double-click opens the archive with the system default handler (whichever reader you've associated with the file type in Finder).
- File → Re-scan (and the toolbar Refresh button) purge orphan rows + their derived thumbnail / preview cache files, so a Finder-side delete is reflected end-to-end.
- Settings → File Access grants broad sandbox access to your home folder or an external volume in one step, separate from the Library catalogue.
- English / Japanese interface; menu titles follow the in-app Language preference, not the OS locale.

## Install

Coming to the Mac App Store — macOS 14 (Sonoma) or later, Apple Silicon required.

## Privacy

Pinakeion works entirely offline. No data is collected, transmitted, or shared. Library paths, metadata, thumbnails, favorites, ratings, and (if you enable them) usage statistics live only on your Mac. Everything can be wiped from **Settings → Privacy**.

[Full privacy policy](privacy-policy.md)

## Suite

**Pinakeion** is part of a small family of macOS apps:

- [Skopeion](../skopeion/) — comic / image viewer (manga-tuned)
- [Arkheion](../arkheion/) — read-only archive inspector with Quick Look
- [Kineion](../kineion/) — video library manager (external-player based)

## Support

Bug reports and feature suggestions: shinichiyuhara1@gmail.com

## License

Proprietary. The binary is distributed via the Mac App Store. Third-party library licenses are bundled in the in-app **Settings → About → License & Attributions** section.
