# Kineion

A macOS library manager for video collections — manage, tag, preview, play, and repair.

## What it does

- Registers one or more folders as Libraries; recognises **44 video extensions** (mp4 / m4v / mov / mkv / webm / avi / wmv / flv / mpg / ts / 3gp / vob / mxf / dv / hevc / av1 / h266 and more).
- AVFoundation-driven metadata extraction (duration, resolution, codec) cached in a sandboxed SQLite database; library scans run incrementally (size/mtime diff) so the grid populates while indexing is still in flight.
- Tags, 5-star ratings, favorites, watched flag, and free-form notes per video. Smart folders for All Videos, Favorites, Watched, Recently Added, Recently Opened, per-rating buckets, and **Corrupted / Unplayable** (files no decoder could open).
- Thumbnail pipeline (QuickLook → AVFoundation with dark-frame detection over 9 timestamp candidates → in-process FFmpegKit for mkv / VP9 / AV1 / Opus / VVC) plus a contact sheet in three tiers: 3×3 inline (1024 px), 5×4 enlarged preview (2048 px), 5×4 export (4096 px) — press **v** or **Space** for the enlarged preview.
- Contact sheet **export to JPEG, WebP, or AVIF** with per-format quality sliders (**Settings → Thumbnails**).
- Background prefetch — after a Library scan finishes, thumbnails generate automatically so subsequent browsing is instant.
- **Portable per-library cache** — choose where each Library's thumbnail / contact-sheet cache lives: the central OS-managed cache (best for internal drives) or a hidden `.Kineion/` folder at the Library root, keyed by the file's library-relative path so an external drive carries its cache to another Mac and reuses it instead of regenerating. Switchable any time from the sidebar (**Cache Location**); a leftover `.Kineion/` from a folder that is no longer a Library is detected on scan and offered for cleanup.
- **iCloud Drive / Dropbox / Google Drive / OneDrive / Box placeholder handling** — files not downloaded locally are detected up front (no AVFoundation hangs), badged in the grid, and the inspector offers a one-click iCloud download or "Reveal in Finder" route for File Provider sources.
- **Library-offline detection** — if a folder's security-scoped bookmark goes stale (drive ejected, folder moved), the sidebar shows a red badge and a "Re-authorize Library…" context-menu item resolves it without losing tags / ratings / notes.
- **Built-in playback** in a dedicated window (AVKit) for AVFoundation-decodable formats (mp4 / mov / H.264 / HEVC …). For everything else — and whenever you configure a preferred player — it hands off to your external player of choice: IINA, VLC, mpv, QuickTime Player, Movist, Movist Pro, Elmedia Player, and Mac Blu-ray Player are auto-detected and one-click selectable from **Settings → Playback**.
- **Repair** corrupt / unplayable videos: an in-process remux (no re-encode) rebuilds a broken container — a damaged `moov`, index, or interleaving — into a `name.fixed.ext` copy next to the original, which is left untouched. Powered by the bundled FFmpeg; the library re-scans automatically so the repaired file appears.
- **Move to Trash** sends a video's source file to the Finder Trash (recoverable) and drops its row, distinct from **Remove from Library** which keeps the file and only forgets the catalogue entry.
- Full menu-bar Cmd shortcuts (Cmd+I inspector, Cmd+B favorite, Cmd+U watched, Cmd+R reveal, Cmd+1..5 stars, Cmd+F search, etc.) plus **27 user-assignable single-key shortcuts** in **Settings → Keybindings**. Cmd-scrollwheel tile zoom (120–360 pt), arrow-key grid navigation, type-to-jump on grid and list.
- English / Japanese interface, rendered in the macOS system font for correct display across every language macOS supports.

## Install

Coming to the Mac App Store — macOS 14 (Sonoma) or later, Apple Silicon (M1 / M2 / M3 / M4).

## Privacy

Kineion works entirely offline. It does not collect, transmit, or share any data. Library folders are referenced via security-scoped bookmarks; metadata, tags, ratings, and thumbnail caches live only on your Mac. Kineion only ever touches your video files when you explicitly ask it to — **Repair** writes a new `name.fixed.ext` copy (leaving the original in place) and **Move to Trash** sends a file to the Finder Trash. It never modifies a source file in place, and nothing is deleted without confirmation. No telemetry, no analytics, no crash reporters.

[Full privacy policy](privacy-policy.md)

## Suite

**Kineion** is part of a small family of macOS apps:

- [Skopeion](../skopeion/) — comic / image viewer (manga-tuned)
- [Pinakeion](../pinakeion/) — image-archive library manager
- [Arkheion](../arkheion/) — read-only archive inspector with Quick Look
- [LexxUp](../lexxup/) — EPWING dictionary reader (cross-dictionary search)

## Support

Bug reports and feature suggestions: shinichiyuhara1@gmail.com

## License

Proprietary. The binary is distributed via the Mac App Store. Third-party library licenses (EB Garamond, GRDB.swift, and — when linked — FFmpeg / libdav1d) are listed in **Settings → About**.
