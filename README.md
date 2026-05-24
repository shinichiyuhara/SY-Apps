# SY Apps — macOS app suite

A small family of focused macOS apps for organising and reading your local media — images, archives, and video. Each app ships standalone on the Mac App Store under App Sandbox, works entirely offline, and shares conventions (signing, localisation, privacy stance) with its siblings.

| App | Description | App Store |
|---|---|---|
| [Skopeion](skopeion/) | Comic / image viewer (manga-tuned) | Coming soon |
| [Pinakeion](pinakeion/) | Image-archive library manager | Coming soon |
| [Arkheion](arkheion/) | Read-only archive inspector with Quick Look | Coming soon |
| [Kineion](kineion/) | Video library manager (external-player based) | Coming soon |

## Cross-app integration

Each app operates independently. The only cross-app interaction is OS-standard file open: Pinakeion delegates archive opening to your system default handler (which can be Skopeion if you set it as the default for the relevant archive types in Finder). No background data exchange, no shared containers.

## Common privacy stance

- Offline by default. No network entitlements; no analytics, crash reporters, or advertising.
- Local-only data. Everything lives in each app's sandbox container.
- One-click wipe in each app. Uninstalling via Finder also removes the sandbox container.
- Each app's full privacy policy lives in its directory ([Skopeion](skopeion/privacy-policy.md), [Pinakeion](pinakeion/privacy-policy.md), [Arkheion](arkheion/privacy-policy.md), [Kineion](kineion/privacy-policy.md)).

## Contact

shinichiyuhara1@gmail.com

## License

Proprietary. Distributed via the Mac App Store. Source not open.
