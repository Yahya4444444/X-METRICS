# Privacy Policy — X Broadcast Metrics

**Last updated:** 2026-05-20

X Broadcast Metrics ("the extension") is a Chrome browser extension that helps you track live viewer counts and statistics on X broadcasts. This policy explains what data the extension handles and how.

## Summary

- The extension stores all data **locally on your device only**, using Chrome's built-in `storage.local` API.
- The extension **does not** transmit your data to any remote server.
- The extension **does not** collect personally identifiable information.
- The extension **does not** sell, share, or transfer data to third parties.
- The extension **does not** use analytics, advertising, or tracking SDKs.

## What the extension accesses

When you visit a broadcast page on `https://x.com` (URLs matching `/i/broadcasts/...` or `/i/spaces/...`), the extension reads the public broadcast data that X already returns to your browser through its own API. This is the same data the X website itself displays to you. The extension does not intercept, log, or access anything else.

The extension extracts the following fields from that response and stores them locally:

- The broadcaster's public username and user ID
- The broadcast ID and broadcast URL path
- Live viewer counts, sampled over time
- Timestamps of each sample
- Computed statistics (peak viewers, rate of change)

## Where data is stored

All data is stored in `chrome.storage.local`, which is Chrome's local-only storage area scoped to this extension on your device. It is **not** synced to your Google account, **not** uploaded anywhere, and **not** accessible to other websites or extensions.

You can delete all stored data at any time from the extension's Settings page ("Clear all data") or by removing the extension from Chrome.

## Permissions used

| Permission | Why it is needed |
|---|---|
| `host_permissions: https://x.com/*` | Run the viewer-tracking widget only on X broadcast pages |
| `scripting` | Inject the tracking script into broadcast pages |
| `webNavigation` | Detect when you open or navigate to a broadcast URL |
| `tabs` | Open the dashboard page in a new tab when you click the extension icon |
| `storage` | Save viewer history locally on your device |

## Data export

You can export your locally stored data to CSV or JSON at any time using the export buttons on the Settings page. Exported files are saved directly to your downloads folder and are never sent anywhere by the extension.

## Children's privacy

The extension is not directed at children under 13 and does not knowingly collect data from them.

## Changes to this policy

If this policy changes, the "Last updated" date at the top will be revised. Material changes will be noted in the extension's update notes on the Chrome Web Store.

## Contact

For privacy questions about this extension, contact: **yahyasaqqa@hotmail.com**
