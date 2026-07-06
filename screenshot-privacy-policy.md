# Privacy Policy — Auto-Name Screenshot

**Last updated: July 2026**

Auto-Name Screenshot ("the extension") captures full-page screenshots in your browser and uses an AI vision model to suggest a descriptive filename. This policy explains what data is involved and how it's used.

## What we collect

- **A random install identifier (clientId).** Generated locally on first run and stored in your browser's extension storage. It is a random UUID — it contains no name, email, or personal information.
- **A downscaled screenshot image** — only when you click Capture. Before any network request, the screenshot is resized so its longest side is at most 1568px and re-encoded as JPEG. This downscaled image is sent to our server to generate a filename suggestion.

## What we never collect

Your name, email, passwords, login sessions, payment card details, cookies, browsing history, or any page content beyond the single screenshot you explicitly captured. **Card data never touches our servers** — payments are handled entirely by Stripe on Stripe's own checkout page.

## How the AI title feature works

When you capture a page, the downscaled JPEG is sent to our Cloudflare Worker (`https://ai-screenshot-worker.snowball11.workers.dev`), which forwards it to an OpenRouter-hosted vision model that returns a 3–6 word filename suggestion. The image is **not stored** — a hash-based cache of the generated title is kept for up to 24 hours so that re-titling an identical screenshot is free, and then discarded.

## Free-tier usage tracking

To enforce the 5 AI-titles-per-month free limit, the Worker maintains a per-clientId monthly counter. This counter contains only a number and your random clientId — nothing else.

## Third-party services

- **Cloudflare** — hosts the Worker that proxies AI title requests.
- **OpenRouter** — provides the vision model that names screenshots.
- **Stripe** — processes subscription payments. Card data is collected on Stripe's own checkout page and is never transmitted to our server.

## Data retention

- **Screenshot images:** not stored. Discarded after the title is generated (24-hour response cache only).
- **Usage counters:** kept for the current month plus up to 35 days, then automatically deleted.
- **Subscription records:** kept for as long as your subscription is active, in order to maintain your Pro entitlement.

## Your rights

- Cancel your subscription anytime via Stripe.
- To request deletion of your data, contact us (below).
- Uninstalling the extension removes the local clientId from your browser.

## Children's privacy

Not directed at, or intended for, children under 13. We do not knowingly collect personal information from children.

## Changes to this policy

We may update this policy from time to time. Material changes will be reflected by the "Last updated" date above.

## Contact

File an issue at the extension's GitHub repository, or email: **[your-email@example.com]** _(replace this placeholder before submitting to the Chrome Web Store)_.
