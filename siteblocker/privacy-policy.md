# Privacy Policy — SiteBlocker

Last updated: 2026-08-20

SiteBlocker is a Chrome extension (Manifest V3) that blocks distracting websites. To do its job it
stores some data — your block list, settings, and (optionally) per-site time. **By default it all
stays on your device.** We run no servers of our own, and SiteBlocker never sells your data or uses
it for advertising. One optional feature you can turn on — cross-device settings sync — uses your
**browser's own sync** to copy your block list and settings to your other devices; it is described
under "What is stored" below and is **off by default**.

## What we don't do

- No accounts, no sign-in.
- No servers, no analytics, no telemetry, no advertising.
- No collection or transmission of your browsing history, page contents, or URLs to us or any third party.
- No reading of page content. Blocking, the block screen, and element hiding are applied without
  inspecting what a page contains.

## What is stored

By default, all settings and state live only in the browser's local extension storage
(`chrome.storage.local`) on your device:

- Your block list, blocking mode (block-list / allow-list), schedules, focus-timer settings,
  element-hiding settings, and block-screen settings.
- Optional time tracking: foreground time per **host** (daily totals only) for sites you visit — no
  full URLs, page contents, or browsing history. It can be turned off, in which case nothing is
  recorded. This data is kept **on your device until you delete it** (so year-over-year totals are
  possible); clear it any time from Stats → reset or Settings → Privacy & data.
- If you enable password protection, the password is stored **hashed with PBKDF2** — never in plaintext.

### Optional cross-device settings sync (off by default)

If — and only if — you turn on **"Sync settings across devices"**, SiteBlocker places your **block
list and settings** (including the PBKDF2-**hashed** password, if set) into the browser's synced
extension storage (`chrome.storage.sync`). Your browser (Chrome, Brave, etc.) then copies them to
your other devices signed in to the **same browser account**, through **that browser vendor's sync
service** — governed by the browser's own privacy policy, not ours. We still receive nothing and run
no servers. This built-in sync covers **settings and the block list only**; to share your
**time-tracking totals** across your devices, use the Nudge integration below. This is off by
default; when off, nothing is synced.

### Optional native-messaging integration (off by default)

If — and only if — you explicitly enable "Send website time to Nudge", the extension passes **host
names and daily totals only** (day + host + seconds — no full URLs, paths, visit times, or page
content) to a companion app (Nudge) running **on the same computer**, via the operating system's
native-messaging channel. The hand-off itself is local — not a network request, and nothing is sent
to us or to any server we run.

Nudge is your own app. If you use **Nudge's multi-device sync**, Nudge may then copy these day/host
totals to **your other devices** so your website-time log is complete across the machines you use.
That sync is performed by Nudge through a storage location **you** choose (for example a folder you
already sync), under Nudge's own privacy policy — again, with no server of ours involved. This whole
integration is off by default; when off, nothing is passed or shared.

## How to delete the data

- Remove individual entries in the extension's Settings, or use Stats → reset to clear recorded time.
- **Settings → Privacy & data** offers "Reset settings to defaults" (keeps your block list and tracked
  time) and "Remove all data" (erases block list, settings, tracked time, and password — irreversible).
- Turn off "Track time on all sites" to stop and keep no time data.
- Turn off "Sync settings across devices" to stop syncing; "Remove all data" also clears the synced
  copy from your browser's storage.
- Removing (uninstalling) the extension deletes all of its local storage.

## Permissions

`declarativeNetRequest` (blocking), `storage` (save settings), `tabs` (read the active tab's host to
show block/unblock state; URLs are not stored or sent), `alarms` (schedules and the focus timer),
`idle` (pause local time tracking while you are away), `contextMenus` (right-click "block this site"),
`notifications` (focus/break phase alerts), `nativeMessaging` (optional Nudge integration above), and
host permissions (so blocking, the block screen, and element hiding can apply to sites you choose).

## Children

SiteBlocker is a general-purpose productivity tool and is not directed to children. We do not sell
anyone's personal information or send it to any server of ours.

## Third-party content

Bundled backgrounds are Public Domain / CC0; ambient audio is CC BY 4.0 (Scott Buckley, Chris
Zabriskie) plus one CC BY-SA 4.0 rain recording (Robert EA Harvey); quotes are public-domain works
with our own short renderings. Attributions are listed in the project README and credits files.

## Contact

Bug reports and questions: shinichiyuhara1@gmail.com
