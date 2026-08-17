# Privacy Policy — SiteBlocker

Last updated: 2026-08-16

SiteBlocker is a Chrome extension (Manifest V3) that blocks distracting websites. It does not
collect, transmit, or sell any personal data. Everything happens locally in your browser.

## What we don't do

- No accounts, no sign-in.
- No servers, no analytics, no telemetry, no advertising.
- No collection or transmission of your browsing history, page contents, or URLs to us or any third party.
- No reading of page content. Blocking, the block screen, and element hiding are applied without
  inspecting what a page contains.

## What is stored locally

All settings and state live only in the browser's local extension storage (`chrome.storage.local`)
on your device:

- Your block list, blocking mode (block-list / allow-list), schedules, focus-timer settings,
  element-hiding settings, and block-screen settings.
- Optional time tracking: foreground time per **host** (daily totals only) for sites you visit — no
  full URLs, page contents, or browsing history. It can be turned off, in which case nothing is
  recorded. Data is kept about 90 days.
- If you enable password protection, the password is stored **hashed with PBKDF2** — never in plaintext.

### Optional native-messaging integration (off by default)

If — and only if — you explicitly enable "Send website time to Nudge", the extension passes **host
names and daily seconds only** to a companion app (Nudge) running **on the same computer**, via the
operating system's native-messaging channel. This is not a network request and nothing leaves your
machine. It is off by default; when off, nothing is passed.

## How to delete the data

- Remove individual entries in the extension's Settings, or use Stats → reset to clear recorded time.
- Turn off "Track time on all sites" to stop and keep no time data.
- Removing (uninstalling) the extension deletes all of its local storage.

## Permissions

`declarativeNetRequest` (blocking), `storage` (save settings), `tabs` (read the active tab's host to
show block/unblock state; URLs are not stored or sent), `alarms` (schedules and the focus timer),
`idle` (pause local time tracking while you are away), `contextMenus` (right-click "block this site"),
`notifications` (focus/break phase alerts), `nativeMessaging` (optional Nudge integration above), and
host permissions (so blocking, the block screen, and element hiding can apply to sites you choose).

## Children

SiteBlocker is a general-purpose productivity tool and is not directed to children. It collects no
personal information from anyone.

## Third-party content

Bundled backgrounds are Public Domain / CC0; ambient audio is CC BY 4.0 (Scott Buckley, Chris
Zabriskie) plus one CC BY-SA 4.0 rain recording (Robert EA Harvey); quotes are public-domain works
with our own short renderings. Attributions are listed in the project README and credits files.

## Contact

Bug reports and questions: shinichiyuhara1@gmail.com
