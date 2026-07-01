# GCampaign Privacy Policy

Last updated: July 1, 2026

GCampaign ("the extension") is a mail-merge tool that sends personalized
email campaigns through your own Gmail account. This policy describes what
information is accessed and how it is handled.

## What we collect
GCampaign does NOT operate any server of its own and does NOT collect, sell,
share, or analyze your data. All data the extension processes is stored
locally in your browser via chrome.storage.local and is transmitted only to
Google's official APIs to perform the actions you request.

Specifically, the extension may access:
- Your Google account email address and display name (via OpenID Connect),
  used to identify you and pre-fill sender information.
- OAuth access and refresh tokens, stored locally so the extension can call
  Gmail and Google Sheets on your behalf.
- Recipient email addresses and any merge data you import from a Google
  Sheet, used only to address and personalize the campaign you are sending.
- The email subject and body you author, used only to send your campaign.

## How data is used
- To authenticate you with Google (OAuth 2.0).
- To read recipient lists from Google Sheets that you select.
- To send emails through your own Gmail account using the Gmail API.
- To pace sends and respect daily sending limits.

Data is never used for advertising, analytics, profiling, or any purpose
unrelated to sending your campaigns.

## Data storage and retention
All data is kept locally in your browser. It is not uploaded to any server
controlled by the developer. Uninstalling the extension removes the locally
stored data. You can also revoke the extension's Google access at any time
from your Google Account -> Security -> Third-party access, or by signing out
within the extension.

## Third-party services
The extension communicates solely with Google services (Gmail API, Google
Sheets API, Google Drive metadata API, Google OAuth). Your use of those
services is governed by Google's Privacy Policy
(https://policies.google.com/privacy).

## Children's privacy
The extension is not directed to children under 13 and does not knowingly
collect their information.

## Contact
For privacy questions, contact: justpick22@gmail.com
