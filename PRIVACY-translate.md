# Privacy Policy — Translate Page

**Effective date:** 2026-07-25

This policy explains what the **Translate Page** browser extension ("the extension") does with your information. It is short on purpose: the extension is built to collect as little as possible, and we want you to be able to verify that for yourself.

> Replace the bracketed placeholders below (`[CONTACT EMAIL]`, `[DEVELOPER NAME]`, `[POLICY URL]`) with your real details before publishing this page.

---

## The short version

- The extension **does not require an account** and **does not ask for your name, email, or any personal information**.
- The extension **does not include analytics, telemetry, advertising, or tracking** of any kind.
- The only data the extension stores is the **history of your recent translations, the entries you've saved to your phrasebook, and your preference settings** — all on your own device, in the browser's local storage.
- The only information the extension **sends anywhere** is the **specific text you explicitly select or type for translation**, sent over HTTPS to the Google Translate service to produce the translated result.

---

## 1. What we collect

Nothing about you. The extension does not request, store, or transmit:

- your name, email, phone number, or any contact details
- your IP address (we have no server to log it)
- your browsing history or the URLs you visit
- your search queries
- cookies or authentication tokens
- device identifiers

There is **no analytics SDK** and **no advertising SDK** bundled in the extension. We do not measure how you use the extension.

## 2. What is stored on your device

The following data is stored locally in your browser using `chrome.storage.local`. It never leaves your device unless you explicitly copy it elsewhere.

| Data | Purpose | Default limit |
|---|---|---|
| **Translation history** | Lets you recall and reuse recent translations from the popup's History tab. | Last 500 entries |
| **Phrasebook** | Stores translations you have explicitly starred so you can keep them indefinitely. | Up to 2,000 entries |
| **Preferences** | Remembers your chosen source and target languages, theme (light / dark / system), and whether to auto-translate on selection. | A few small values |

Each translation entry consists of: the source text you translated, the translated text, the source and target language codes, the language detected by the translator (when auto-detect was used), and a timestamp.

You can review and delete this data at any time:

- Open the extension's **Options** page → **Clear history** and **Clear phrasebook**.
- **Uninstalling** the extension removes all of the above immediately and permanently.

## 3. What is sent externally

When you select text on a web page, type text into the popup, trigger a full-page translation, or save a translation to your phrasebook, the **specific text you have selected or typed** is sent over an encrypted HTTPS connection to **Google Translate's public translation service** (`https://translate.googleapis.com`) for the sole purpose of producing a translation.

What is **not** sent:

- the rest of the page's content (only your selection is sent)
- the page's URL
- your cookies, credentials, or login state
- your IP address (beyond what is necessary for the HTTPS connection itself)
- any identifier that ties the request to you

We do not operate any server of our own. We do not log, store, or have access to the text you translate.

**Text-to-speech** (the 🔊 button) is handled entirely by your browser's built-in speech engine; no audio or text is transmitted.

## 4. Third-party services

| Service | What it receives | Purpose | Policy |
|---|---|---|---|
| Google Translate (`translate.googleapis.com`) | The specific text you select or type, plus the chosen source and target languages. | Produces the translation. | [Google Privacy & Terms](https://policies.google.com/privacy) |
| Browser speech synthesis | The translated text, locally inside your browser. | Reads translations aloud. | Handled by your browser; nothing is transmitted. |

Beyond the translation service above, the extension does not communicate with any third party.

## 5. Data retention

- **Translation history and phrasebook** are retained on your device until you clear them (Options page) or uninstall the extension.
- **Text sent to Google Translate** is governed by Google's own retention policy (linked above). The extension itself does not retain it beyond displaying it on your screen.

## 6. Children's privacy

The extension is a general-purpose translation tool and is **not directed at children under 13** (or the applicable age in your jurisdiction). We do not knowingly collect any personal information from anyone, including children.

## 7. Your rights

Because we don't collect personal data, most data-protection rights (access, correction, deletion, portability) are exercised directly by you through your browser:

- **Right of access / portability:** Your history and phrasebook are visible in the extension's popup and can be copied manually.
- **Right to deletion:** Use the "Clear history" and "Clear phrasebook" buttons on the Options page, or uninstall the extension.
- **Right to object:** Uninstall the extension at any time.

## 8. Open source

The extension's source code is open and auditable. If you would like to verify any claim in this policy, the code is the source of truth. [Link to your source repository — replace or remove this line.]

## 9. Changes to this policy

If the extension's data practices change in a future version, we will update this page and revise the "Effective date" above. We will not retroactively change how already-stored data is handled without your action.

## 10. Contact

If you have questions about this policy or the extension's data practices, contact:

- **Email:** [CONTACT EMAIL]
- **Developer:** [DEVELOPER NAME]
- **Source code:** [REPOSITORY URL]

---

*This document is provided in plain language. It is not legal advice and does not constitute a contract. Where this summary and the extension's actual behaviour differ, the extension's actual behaviour (which you can verify from the source code) is authoritative.*
