# Privacy Policy: Change Set Helper for Salesforce

_Last updated: 2026-11-20_

Change Set Helper for Salesforce ("the extension") is a browser extension that adds search, sorting, CSV export, multi-select, `package.xml` export and "recreate as outbound" tools to Salesforce change set pages.

**Short version: the extension does not collect, store, sell or transmit your data to the developer or to any third party. It runs entirely in your browser and talks only to the Salesforce org you are already signed in to.**

## What the extension accesses

| Data | Why | Where it goes |
|---|---|---|
| Salesforce session cookie (`sid`) for the Salesforce host of the current tab | To authenticate read-only Salesforce REST/Tooling API queries | Sent only to that same Salesforce host, as an `Authorization` header. Read in the background worker only; never exposed to web pages, never stored, never logged. |
| Change set pages you view (component names, types, parent objects) | To build the search index, sort columns, CSV and `package.xml` | Stays in your browser. |
| Component metadata returned by Salesforce (names, API names, last modified date and user) | To show "Last modified" columns and to resolve real API names for `package.xml` | Stays in your browser. Held in memory (cached per tab) and discarded when the tab closes. |
| One preference: Plugin view / Standard view | To remember your choice | Saved in the Salesforce page's `localStorage` on your device. |

The extension only runs on Salesforce change set pages (`/changemgmt/*` and `/p/mfpkg/*` on `*.salesforce.com`, `*.force.com` and `*.salesforce-setup.com`).

## What the extension does not do

- No analytics, telemetry, crash reporting, advertising or tracking.
- No developer-operated servers. The extension has no backend.
- No sale, rental or sharing of data. No use of data for creditworthiness, lending or unrelated purposes.
- No remote code. All code ships inside the extension package.
- No reading of browsing history or of pages outside the Salesforce domains above.

## Actions you start yourself

- **Copy CSV / Download CSV / Copy package.xml** put data on your clipboard or save a file on your device. Nothing is sent anywhere.
- **Deploy with Diffbridge** copies the `package.xml` to your clipboard and opens `https://diffbridge.com` in a new tab so you can paste it. Once you are on that site, its own privacy policy applies. The extension does not send the file to it.
- **Recreate as outbound** and **Remove selected** make changes in your own Salesforce org, only after you confirm. They use your existing Salesforce session through Salesforce's own pages.
- **Request a feature / Report a bug / Contact us** open a pre-filled GitHub issue (or email draft) in your browser. Nothing is sent unless you submit it. Bug reports include the extension version and your browser's user-agent string. Review them before posting. GitHub's privacy policy applies to anything you post there.
- The Diffbridge link in the popup includes `utm_source=change-set-helper`. This lets Diffbridge count visits from the extension. It contains no personal data.

## Children

The extension is a developer and administrator tool and is not directed at children.

## Changes

If this policy changes, the new version will be published at the same location with an updated date. Material changes will also be noted in the extension's release notes.

## Contact

Questions about this policy: email **support@diffbridge.com** or open an issue at https://github.com/kalusartem/change-set-helper-privacy/issues.

Publisher: Mokahub LLC

## Not affiliated with Salesforce

Salesforce is a trademark of Salesforce, Inc. This extension is an independent third-party tool and is not affiliated with, endorsed by or sponsored by Salesforce, Inc.
