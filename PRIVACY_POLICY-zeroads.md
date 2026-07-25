# ZeroAds Privacy Policy

**Last updated:** July 25, 2026

This Privacy Policy describes how ZeroAds ("we", "us", or "the extension") handles information when you use the ZeroAds browser extension (the "Service"). ZeroAds is an ad blocker for Chrome, Brave, Edge, Arc, and other Chromium-based browsers.

By installing and using ZeroAds, you agree to the practices described in this policy.

---

## The short version

ZeroAds does **not** collect, sell, share, or transmit your personal data. There are no accounts, no servers storing your data, no analytics, and no tracking. Your browsing stays on your device. The only network request ZeroAds makes is to download the open EasyList filter list (the same one most ad blockers use) so it can keep your blocking rules up to date.

---

## 1. Data we collect

**We do not collect any personal data.**

ZeroAds has no backend server that receives your data, no account system, and no analytics or telemetry of any kind. We do not collect:

- Your name, email, address, or any other personally identifiable information
- Your passwords or authentication credentials
- Payment or financial information
- Your personal communications
- Your location
- Your browsing history or the URLs you visit
- Your activity on websites (clicks, scrolls, form submissions)
- Your activity within the extension

---

## 2. Data processed on your device

To function, ZeroAds reads certain information **temporarily** on your device to apply blocking and display the popup. This information is **never stored permanently and never transmitted anywhere**:

| Data | Why it's read | Stored? | Transmitted? |
|---|---|---|---|
| The hostname of the page in your active tab | To check whether the site is on your allowlist and to display the per-tab block count | No — read ephemerally when the popup opens | No |
| Network requests made by the pages you visit | To match them against blocking rules and block ad/tracker requests | No | No |

---

## 3. Data stored on your device

ZeroAds stores the following **locally** in your browser using Chrome's `chrome.storage` API. This data never leaves your device, never syncs to any ZeroAds-controlled server, and is fully under your control (see [Your controls](#8-your-controls) below).

| Stored data | Purpose | Synced across devices? |
|---|---|---|
| Your settings (e.g. master on/off, badge preference) | Remembers your preferences between sessions | Via Chrome's built-in sync (see note below) |
| Your site allowlist | Remembers where you've paused blocking | Via Chrome's built-in sync |
| Your custom filter rules | Stores rules you've added | Via Chrome's built-in sync |
| The cached EasyList cosmetic-filter map | Avoids re-downloading filter data on every page load | No (local only) |
| Block counts (per-tab and total) | Powers the popup and badge counter | No (local only) |

**About Chrome sync:** Some of the above is stored in `chrome.storage.sync`, which Chrome itself may sync to your Google account so your preferences follow you across signed-in devices. This is a feature of your Google account and Chrome, not ZeroAds — ZeroAds does not operate this sync and has no access to it. If you'd prefer these items not sync, you can disable Chrome sync in your browser settings.

---

## 4. Network requests ZeroAds makes

ZeroAds makes exactly **one** kind of outbound network request, and it does not include any personal data:

- **Filter-list updates.** Approximately once per day, ZeroAds fetches the latest version of the [EasyList](https://easylist.to/) filter list from `https://easylist.to/easylist.txt`. This keeps your ad blocking up to date as new ads appear. The request includes only a generic `User-Agent` string identifying the extension (e.g. `ZeroAds/1.0`) — **no cookies, no user ID, no browsing data, no information that could identify you**.

That's it. ZeroAds does not connect to any other server, API, or endpoint.

---

## 5. Third-party services

ZeroAds relies on the following third-party resources:

- **[EasyList](https://easylist.to/)** — the open-source filter list (GPL-3.0-or-later) that provides the blocking rules. EasyList is downloaded directly from `easylist.to` and processed entirely on your device. EasyList has its own practices; see [easylist.to](https://easylist.to/) for details. ZeroAds is not affiliated with EasyList or its maintainers.
- **Open-source libraries** — ZeroAds is built on open-source software (React, Vite, shadcn/ui, Radix UI, Tailwind CSS, Lucide icons). These run locally within the extension and do not transmit your data.

ZeroAds does **not** use any advertising, analytics, error-reporting, or tracking SDKs.

---

## 6. How ad blocking works (and what we don't see)

ZeroAds applies blocking rules using Chrome's built-in `declarativeNetRequest` engine. The browser — not ZeroAds — evaluates each network request against the rules and blocks matching ones. ZeroAds does not see the contents of the pages you visit, the requests your browser makes, or anything you type. Blocking is declarative: rules are handed to the browser, and the browser does the matching in private.

For cosmetic (element-hiding) filtering, ZeroAds injects a stylesheet into pages that hides common ad elements. This stylesheet is generated from EasyList and contains no personal data.

---

## 7. Children's privacy

ZeroAds is intended for a general audience and does not knowingly collect any data from anyone — including children under 13 (or the equivalent age in your jurisdiction). Because ZeroAds collects no personal data, no parental consent is required. If you believe a child has provided us with personal data (which should not be possible), please contact us so we can investigate.

---

## 8. Your controls

Because all data ZeroAds uses is stored locally on your device, you have full control over it:

- **View or change your settings** — Open the ZeroAds popup or Options page at any time.
- **Clear your allowlist and custom filters** — Use the Options page to remove individual entries, or uninstall the extension to remove everything at once.
- **Clear all ZeroAds data** — Removing the extension from your browser automatically deletes all locally-stored settings, allowlists, custom filters, and counts. Nothing is left behind.
- **Chrome's site-data controls** — You can also clear extension storage via Chrome's "Clear browsing data" → "Cookies and other site data."

---

## 9. Data security

ZeroAds stores data only in your browser's local storage, which is sandboxed and isolated from other extensions and websites by Chrome's security model. ZeroAds does not transmit your data to any server, so there is no server-side breach surface. No data security incidents are possible against data that is never transmitted.

---

## 10. Changes to this policy

If we change this Privacy Policy, we will update the "Last updated" date at the top of this page and, for material changes, notify users through the extension or the Chrome Web Store listing. We encourage you to review this policy periodically.

Because ZeroAds does not collect personal data, changes to this policy will generally relate to the technical description of how the extension works, not to how your data is handled.

---

## 11. Your rights

Because ZeroAds does not collect or process personal data, most data-protection rights (such as access, correction, deletion, or portability of personal data) are automatically satisfied — there is no personal data about you for us to provide, correct, delete, or export. You retain full control over all locally-stored data, as described in [Your controls](#8-your-controls).

If you are located in the European Economic Area, the United Kingdom, or California, you have rights under the GDPR, UK GDPR, and CCPA respectively. As ZeroAds does not process personal data, it does not act as a "controller" or "processor" of such data.

---

## 12. Open source

ZeroAds is open-source software. Anyone may inspect, audit, and verify the claims in this policy by reading the source code at:

👉 **https://github.com/zeroads/zeroads**

*(Replace with your real repository URL before publishing.)*

---

## 13. Contact

If you have questions, concerns, or feedback about this Privacy Policy or ZeroAds, please contact:

- **Email:** `privacy@example.com` *(replace with your real contact email before publishing)*
- **Issues:** https://github.com/zeroads/zeroads/issues

We aim to respond to all legitimate inquiries within a reasonable timeframe.

---

*This document is provided for informational purposes and does not constitute legal advice. If you have specific legal or compliance requirements, consult a qualified professional.*
