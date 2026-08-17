# LexxUp

A macOS dictionary app for **EPWING** electronic dictionaries. Point it at your
dictionary folder and search your whole shelf at once — one query, results from
every dictionary, merged and grouped, in a fast, familiar interface.

An English dictionary is **included**, so it works the moment you open it:
Webster's Revised Unabridged Dictionary (1913), in the public domain. Add your
own EPWING dictionaries whenever you like — and **DICT (dictd) dictionaries** as
well, which is the format the freely licensed collections from dict.org and
FreeDict ship in.

## What it does

- **An English dictionary is included** — Webster's Revised Unabridged Dictionary
  (1913), about 114,000 entries, public domain. Nothing to download or configure
  before the first search.
- **Reads EPWING and DICT (dictd)** dictionaries, in one shelf and one search.
  DICT bodies may be plain or dictzip-compressed. (Backward "ends with" matching
  is EPWING-only: a dictd index is sorted forwards and has nothing to answer it
  with.)
- **Cross-dictionary search** across every registered EPWING dictionary, run in
  parallel — one query returns hits from all of them, grouped per dictionary with
  a hit count for each.
- **Incremental (as-you-type) search** with Exact / Forward / Backward matching,
  plus **typo-tolerant** search and a **base-form fallback** that retries a
  no-hit query with the word's stem (running → run).
- **Optional full-text (in-body) search** over entry bodies, not just headwords
  (opt-in; a background index keeps it fast).
- **Romaji → kana input** — type `jisho` and search じしょ — plus clipboard
  search that looks up copied text, a recent-searches menu, and search-term
  highlighting in results.
- Scope a search with **category tabs** and your own **dictionary groups**;
  enable, disable, categorize, and reorder dictionaries in a Collections view.

- **Audio pronunciation** for dictionaries that embed recorded sound, **figures
  inline**, and **clickable cross-references** with Back / Forward and
  Previous / Next navigation. Right-click a selection to look it up.
- **History** grouped by day and **bookmarks** in folders; customizable font,
  size, spacing and colors, zoom, **vertical writing**, and dark mode.
- **English and Japanese interface**, following your in-app preference rather
  than the OS locale.

## Install

[On the Mac App Store](https://apps.apple.com/app/id6791462846?mt=12) — ¥3,000.
Requires macOS 14 (Sonoma) or later on Apple silicon.

## Privacy

LexxUp runs entirely on your Mac. No data is collected, transmitted, or shared,
and it makes no network requests — no analytics, no advertising, no tracking.
Your dictionaries are read-only; your history, bookmarks, and settings stay on
your Mac and can be wiped from **Settings → Privacy**.

[Full privacy policy](privacy-policy.md)

## Suite

**LexxUp** is part of a small family of macOS apps:

- [Skopeion](../skopeion/) — comic / image viewer (manga-tuned)
- [Pinakeion](../pinakeion/) — image-archive library manager
- [Arkheion](../arkheion/) — read-only archive inspector with Quick Look
- [Kineion](../kineion/) — video library manager (external-player based)

## Support

Bug reports and feature suggestions: shinichiyuhara1@gmail.com

## License

Proprietary. The binary is distributed via the Mac App Store. Third-party library
licenses are shown in the in-app **About → Licenses** tab.
