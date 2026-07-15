# ProductGuesser Privacy Policy

**Last updated: 2026-07-14**

ProductGuesser is built privacy-first. The extension never sees, stores, or
transmits your API keys, and it collects no personal data about you.

## What we collect

**Nothing about you personally.** We do not use analytics, tracking pixels, or
advertising SDKs. We do not collect your email, name, or browsing history.

The only identifier we generate is a **random client id** (a UUID) stored
locally in your browser. It is used solely to enforce the free monthly usage
cap. It is not correlated with your identity and is never sold or shared.

## What is sent to our server

When you click "Analyze this page," the extension sends to our Cloudflare
Worker:

1. **A JPEG screenshot of the current tab's visible viewport.**
2. **Extracted text** from the page (title, meta description, headings, hero
   copy, and navigation link labels).
3. The page's URL (sent as part of the extracted text for context).
4. Your random client id (for usage accounting only).

Our Worker forwards the screenshot and text to **OpenRouter**, which routes
the analysis to a vision model (e.g. Google Gemini) and generates the
simulated product screenshots via an image model (e.g. Google Gemini Flash
Image). OpenRouter receives the page content described above and processes it
under their own terms. Nothing is stored on our servers after the response is
returned.

## What we do not send

- No browsing history, cookies, or credentials.
- No data from pages you do not explicitly analyze.
- Nothing happens until you click the button — there is no background tracking.

## Data retention

- The screenshot and text are processed ephemerally to produce the analysis
  and are not stored on our servers.
- The only thing we persist is a **monthly usage count** keyed by your random
  client id, with a ~6-week TTL, after which it is automatically deleted.

## Third-party services

- **Cloudflare** — hosts the Worker that proxies requests.
- **OpenRouter** — routes both analysis requests (to a vision model) and image
  generation requests (to an image model). See
  [OpenRouter's privacy policy](https://openrouter.ai/legal/privacy-policy).

Their privacy policies govern any data they receive.

## Your choices

- You can clear your client id and usage count at any time by removing the
  extension's stored data (chrome://extensions → ProductGuesser → Details →
  Site settings / clear data) or by uninstalling the extension.
- You can point the extension at your own self-hosted Worker via the Settings
  sheet.

## Contact

Questions about this policy? Email **[your-email@example.com]** (replace with
your contact address before hosting this page) or open an issue on the project
repository.
