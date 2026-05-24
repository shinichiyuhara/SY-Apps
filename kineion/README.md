# Kineion

A macOS library manager for video collections — manage, tag, and preview without playing.

## What it does

- Registers one or more folders as Libraries; recognises 44 video extensions (mp4 / m4v / mov / mkv / webm / avi / wmv / flv / mpg / ts / 3gp / vob / mxf / dv / hevc / av1 and more).
- AVFoundation-driven metadata extraction (duration, resolution, codec) cached in a sandboxed SQLite database; library scans run incrementally so the grid populates while indexing is still in flight.
- Tags, 5-star ratings, favorites, and free-form notes per video.
- Thumbnail pipeline (QuickLook → AVFoundation with dark-frame detection → optional in-process FFmpegKit when linked) plus a 5×4 contact sheet in three quality tiers; press Space for an enlarged preview.
- Background prefetch — after a Library scan finishes, thumbnails generate automatically so subsequent browsing is instant.
- Hands playback off to your favourite external player: IINA, VLC, mpv, QuickTime Player, Movist / Movist Pro, and others are auto-detected and one-click selectable from **Settings → Playback**.
- Full menu-bar Cmd shortcuts (Cmd+I inspector, Cmd+B favorite, Cmd+U watched, Cmd+R reveal, Cmd+1..5 stars, Cmd+F search, etc.) plus 27 user-assignable single-key shortcuts in **Settings → Keybindings**. Cmd-scrollwheel tile zoom, arrow-key grid navigation, type-to-jump on the grid and list.
- English / Japanese interface, bundled M PLUS 1p typeface.

## Install

Coming to the Mac App Store — macOS 14 (Sonoma) or later, Apple Silicon required.

## Privacy

Kineion works entirely offline. It does not collect, transmit, or share any data. Library folders are referenced via security-scoped bookmarks (Kineion never modifies the underlying video files); metadata, tags, ratings, and the thumbnail cache live only inside Kineion's sandbox container. No telemetry, no analytics, no crash reporters.

[Full privacy policy](privacy-policy.md)

## Suite

**Kineion** is part of a small family of macOS apps:

- [Skopeion](../skopeion/) — comic / image viewer (manga-tuned)
- [Pinakeion](../pinakeion/) — image-archive library manager
- [Arkheion](../arkheion/) — read-only archive inspector with Quick Look

## Support

Bug reports and feature suggestions: shinichiyuhara1@gmail.com

## License

Proprietary. The binary is distributed via the Mac App Store. Third-party library licenses (M PLUS 1p, EB Garamond, GRDB.swift, and — when linked — FFmpeg / libdav1d) are listed in **Settings → About**.
