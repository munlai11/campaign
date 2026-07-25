# Spelling Corrector — Privacy Policy

**Last updated:** 2026-07-25

## The short version

Spelling Corrector does **not** collect, store, transmit, sell, or share any of
your personal data. Your text never leaves your device. **There is no server.**

---

## What data we collect

**None.**

Spelling Corrector does not collect any personal data, usage data, browsing
history, communications, account information, or any other information about
you or from your device.

## What data we transmit

**None.**

The extension makes **zero outbound network requests**. There is no analytics
SDK, no advertising SDK, no crash reporter, no telemetry, and no remote server.
The only `fetch()` calls in the source code are to
`chrome.runtime.getURL(...)`, which loads files that are **already bundled
inside the extension package** (specifically, the English dictionary used to
check spelling). These requests never leave your browser — they read from the
extension's own installed files on your device.

## What is stored on your device

The following items are saved locally on your device using
`chrome.storage.local`. They are **never synced, never transmitted, and never
leave your browser**:

| Item | Purpose |
| --- | --- |
| Whether the extension is **enabled or disabled** | Master on/off toggle |
| Your **theme preference** (light / dark / system) | UI appearance only |
| Your **personal dictionary** — words you have explicitly added | Words you mark as "not misspelled" so they are never flagged again |

You can clear all of this at any time by removing the extension, or by using
your browser's "Clear data" feature for the extension.

## How text is processed (and why this is **not** data collection)

When you type into a text field on any website, the extension reads that text
**in memory, on your device** for one purpose only: to identify misspelled
words and draw a wavy red underline beneath them. When you click a suggested
correction, the extension rewrites the text directly into the field on the
page.

This text is:

- **Not stored** — not written to disk, not saved to any database, not logged.
- **Not transmitted** — never sent to any server, anywhere.
- **Discarded immediately** — gone the moment the page is closed or the field
  cleared.

Reading text in memory to draw an underline is **not** data collection under
Google's Chrome Web Store policy or under privacy regulations such as GDPR or
CCPA, because no data persists and no data leaves your device.

## Permissions, in plain English

| Permission | Why it's needed |
| --- | --- |
| `host_permissions (<all_urls>)` | Required so the extension can read the text you type into text fields on any website, draw underlines beneath misspelled words, and apply corrections when you click a suggestion. All processing happens locally — no text is transmitted. The extension cannot function on a site-by-site permission basis because users type into text fields on essentially every website. |
| `storage` | Used to persist your settings and personal dictionary (see above). Stored via `chrome.storage.local` — stays on your device, never synced or transmitted. |
| `activeTab` | Allows the popup (when you click the toolbar icon) to show a live count of misspelled words on the tab you're viewing. No data is transmitted. |

## Third parties

Spelling Corrector does **not** use any third-party services. There are no
analytics providers, advertisers, crash reporters, authentication providers,
CDNs, or tracking SDKs involved.

The dictionary used for spell checking (Hunspell format, US English) is a
static data file bundled inside the extension. It is not a "service" and does
not communicate with any server.

## Remote code

Spelling Corrector does **not** execute or load any remote JavaScript. All
code is bundled inside the extension package. There is no `eval`, no dynamic
`import()` from external domains, and no remote `<script>` loading.

## Authentication

Spelling Corrector does **not** require an account, sign-in, API key, or any
form of authentication. There is no login system.

## Children's privacy

Spelling Corrector is not directed at children under 13 (or the applicable age
in your jurisdiction) and collects no data from anyone — children or adults.

## Data retention

Because no data is collected, there is no data to retain. The only items
stored on your device (settings and personal dictionary) persist until you
choose to remove the extension or clear the data yourself.

## International users

Spelling Corrector can be used from any location. Because no data is collected
or transmitted, your location is irrelevant to privacy — there is no
cross-border data transfer because there is no data transfer.

## Your rights (GDPR / CCPA and similar)

Because Spelling Corrector does not collect any personal data, the rights
granted under GDPR, CCPA, and similar regulations (access, deletion,
portability, etc.) are automatically satisfied — **there is no data about you
to access, delete, or port.** Your settings and personal dictionary are under
your sole control on your own device.

## Changes to this policy

If this privacy policy ever changes, this page will be updated and the "Last
updated" date at the top will be advanced. We will never quietly weaken these
commitments — any change that introduces data collection will be disclosed
clearly and in advance.

If a future version of the extension were ever to introduce any form of data
collection (it currently does not), it would require explicit user opt-in
consent before any data is transmitted, and the updated policy would describe
exactly what is collected, why, and where it goes.

## Open source

Spelling Corrector's source code is available for independent audit. If you
are a security researcher or simply curious, you can read every line of code
and verify the claims in this policy yourself.

## Contact

To report a privacy concern, request more information, or ask a question about
this policy, please open an issue on the extension's public source repository
(GitHub), or contact the developer at the email listed on the Chrome Web
Store listing.

---

**Summary, once more:** No data collected. No data transmitted. No server.
Your text never leaves your device. That's not a promise — it's verifiable
from the source code.
