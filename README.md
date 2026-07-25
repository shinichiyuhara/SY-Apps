# SY Apps — macOS app suite

A small family of focused macOS apps for organising and reading your local media — images, archives, video, and dictionaries. Each app ships standalone on the Mac App Store under App Sandbox, works entirely offline, and shares conventions (signing, localisation, privacy stance) with its siblings.

| App | Description | App Store |
|---|---|---|
| [Skopeion](skopeion/) | Comic / image viewer (manga-tuned) | [Mac App Store](https://apps.apple.com/app/id6771427796?mt=12) |
| [Pinakeion](pinakeion/) | Image-archive library manager | [Mac App Store](https://apps.apple.com/app/id6772719033?mt=12) |
| [Arkheion](arkheion/) | Read-only archive inspector with Quick Look | [Mac App Store](https://apps.apple.com/app/id6772701489?mt=12) |
| [Kineion](kineion/) | Video library manager (external-player based) | Coming soon |
| [LexxUp](lexxup/) | EPWING dictionary reader (cross-dictionary search) | Coming soon |
| [Demion](demion/) | File archiver (compress and extract) | Coming soon |

## Cross-app integration

Each app operates independently. The only cross-app interaction is OS-standard file open: Pinakeion delegates archive opening to your system default handler (which can be Skopeion if you set it as the default for the relevant archive types in Finder). No background data exchange, no shared containers.

## Common privacy stance

- Offline by default. No network entitlements; no analytics, crash reporters, or advertising.
- Local-only data. Everything lives in each app's sandbox container.
- One-click wipe in each app. Uninstalling via Finder also removes the sandbox container.
- Each app's full privacy policy lives in its directory ([Skopeion](skopeion/privacy-policy.md), [Pinakeion](pinakeion/privacy-policy.md), [Arkheion](arkheion/privacy-policy.md), [Kineion](kineion/privacy-policy.md), [LexxUp](lexxup/privacy-policy.md),
  [Demion](demion/privacy-policy.md)).

## Contact

shinichiyuhara1@gmail.com

## License

Proprietary. Distributed via the Mac App Store. Source not open.
