# Privacy Policy — X Broadcast Metrics

**Last updated:** 2026-10-26

X Broadcast Metrics ("the extension") is a Chrome browser extension that helps
you track the viewer and view counts X shows for broadcasts, and statistics about them. This
policy comprehensively describes every category of data the extension handles,
how it is used, where it is stored, and every party it is shared with.

## Summary

- All data is stored locally on your device using Chrome's `chrome.storage.local` API.
- The extension does not operate any backend server. The developer has no
  database, analytics service, or telemetry pipeline that receives your data.
- The extension contains no analytics, advertising, or tracking SDKs.
- The only third party that ever receives data from the extension is
  Telegram — and only if you explicitly enable and configure Telegram
  notifications with your own personal bot (see Section 4).

## 1. Data the extension collects

### a) Broadcast data read from X

When you visit a broadcast page on `https://x.com` (URLs matching
`/i/broadcasts/...`), the extension reads the public broadcast data that X
already returns to your browser through its own API. This is the same data
the X website itself displays to you. The extension does not modify, block,
or log any other network traffic, and does not access DMs, timelines, or
account credentials.

The following fields are extracted and stored locally:

- The broadcaster's public username and user ID
- The broadcast ID, broadcast URL path and public broadcast title
- The broadcast's viewer counts as X reports them (live viewers, or total views),
  sampled over time
- Timestamps of each sample
- Computed statistics (peak viewers or views gained, growth rate per
  interval, session duration, sample count)

### b) User-provided configuration

The extension stores settings you enter yourself:

- Theme, view mode, chart preferences
- Alert rules, alert thresholds, custom alert notes, sound selections,
  banner duration, cooldown values
- OPTIONAL: Telegram Bot Token and Telegram Chat ID (only if you enable
  Telegram notifications)

### c) Data the extension does NOT collect

The extension does not collect: personally identifiable information, email
addresses, passwords, X account credentials, browsing history outside of X
broadcast pages, IP addresses, device identifiers, geolocation, or any
analytics/telemetry.

## 2. How the data is used

- Broadcast data is used solely to render the on-page widget and dashboard,
  and to evaluate the alert rules you define.
- Configuration data is used to render the UI and control extension
  behavior according to your preferences.
- Telegram credentials (if provided) are used solely to send you
  notifications through your own Telegram bot when your alerts fire.

The extension does not use any collected data for advertising, profiling,
resale, or any purpose beyond delivering the features described in the
Chrome Web Store listing.

## 3. Where data is stored

All data listed in Section 1 is stored in `chrome.storage.local`, which is
Chrome's local-only storage area scoped to this extension on your device.
It is **not** synced to your Google account, **not** uploaded to any
developer-run server, and **not** accessible to other websites or extensions.

You can delete all stored data at any time from the extension's Settings
page ("Clear all data") or by removing the extension from Chrome.

## 4. Third parties that receive data

### Telegram (api.telegram.org) — OPTIONAL, user-configured

If — and only if — you enter a Telegram Bot Token and Chat ID in the
Settings page and enable Telegram notifications, the extension will send
HTTPS requests to Telegram's Bot API at `https://api.telegram.org` when one
of your alerts fires.

The content sent to Telegram consists of the alert message text, which may
include:

- The broadcaster's public username
- The broadcast URL
- The metric value that triggered the alert
- Any custom note you attached to the alert rule

These messages are delivered to your own personal Telegram bot and chat.
The developer has no access to them. Telegram's own handling of this data
is governed by Telegram's privacy policy at https://telegram.org/privacy.

This integration is disabled by default. You can disable it at any time by
clearing the token and chat ID in the Settings page.

No other third parties receive any data from this extension. The extension
contains no analytics SDKs, no advertising SDKs, no crash reporting, and no
remote code loading.

## 5. Permissions used

| Permission | Why it is needed |
|---|---|
| `host_permissions: https://x.com/*` and a content script on `https://x.com/*` | Run the viewer-tracking widget on X. The script loads with X's pages but stays inactive until you open a broadcast page |
| `host_permissions: https://api.telegram.org/*` | Deliver optional Telegram notifications to your own bot (only when enabled) |
| `scripting` | Add the small script that reads the viewer count to a broadcast page once it has loaded |
| `storage` | Save settings and viewer history locally on your device |
| `unlimitedStorage` | Let locally stored viewer history grow beyond Chrome's default 10 MB limit, which otherwise stops saving silently once reached |

## 6. Data export

You can export your locally stored data to CSV or JSON at any time using
the export buttons on the Settings page. Exported files are saved directly
to your downloads folder by Chrome and are never sent anywhere by the
extension. You can also import a previously exported JSON file; it is read
on your device and added to your local history, and is not sent anywhere.

## 7. Data retention and deletion

Data persists locally until you clear it via the Settings page, clear your
browser storage, or uninstall the extension. Under "Keep history for" in
Settings you can also have samples older than a chosen age deleted
automatically (off by default), and each broadcast keeps at most its newest
66,666 samples. No data is retained on any remote system by the developer.

## 8. Children's privacy

The extension is not directed at children under 13 and does not knowingly
collect data from them.

## 9. Changes to this policy

If this policy changes, the "Last updated" date at the top will be revised.
Material changes will be noted in the extension's update notes on the
Chrome Web Store.

## 10. Contact

For privacy questions about this extension, contact: **yahyasaqqa@hotmail.com**
