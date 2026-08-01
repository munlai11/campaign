# Focus Tab — Privacy Policy

_Last updated: August 1, 2026_

Focus Tab is a new-tab-page browser extension. It replaces your new tab with a
clock, greeting, daily focus, to-do list, weather, quote, and quick links. This
policy explains, in plain language, what data the extension uses and where it
goes.

> **The short version:** Focus Tab has no servers, no accounts, and no
> analytics. The only thing you can type in (your name, focus, to-dos, links,
> settings) is stored in your own browser. The only external requests the
> extension makes are for **local weather** — and only if you opt in — sending
> nothing more than approximate coordinates.

---

## 1. What we collect

Focus Tab **does not collect, sell, rent, or share personal data**, and it does
not operate any backend service, database, or logging of its own.

### Data you enter
When you use the extension, the following information may be **stored in your
browser** via `chrome.storage.sync` (the browser's own synced-storage feature):

- An optional **display name** (used only to personalize the greeting).
- A **daily focus** and a **to-do list** (free text you choose to type).
- **Quick links** (bookmarks you add: a title and URL).
- **Settings** (clock format, temperature unit, background dimming,
  show-seconds).

This data lives in your browser profile. If you are signed into Chrome or Brave
sync, the browser replicates it across your signed-in devices through
**Google's or Brave's own sync infrastructure** — Focus Tab never transmits it
to any server it controls. If you are not signed into sync, it stays on the
device. Uninstalling the extension removes it from that device.

### Geolocation (optional, opt-in)
To show **local weather**, Focus Tab may request your device's location via the
browser's standard geolocation prompt. Location is requested with **city-level
accuracy** (`enableHighAccuracy: false`) and is **cached for the browser
session** so it isn't re-requested on every tab. If you deny the prompt or keep
weather closed, no location is ever obtained.

---

## 2. Where data goes (external services)

After you opt into weather, Focus Tab makes **only two** outbound network
requests. Both are unauthenticated `GET` requests and send **nothing but
latitude and longitude** — no cookies, no user identifier, no API key, no other
data from your browser.

| Service | Purpose | What is sent | What is returned |
|---|---|---|---|
| **Open-Meteo** (`api.open-meteo.com`) | Current temperature and weather condition | Latitude, longitude | A temperature value and a weather code |
| **BigDataCloud** (`api.bigdatacloud.net`) | Convert coordinates into a city name to display | Latitude, longitude | A city/locality name string |

Both are free, key-less, public APIs. They are contacted only when the weather
widget fetches or refreshes data (at most once every 30 minutes).

### What Focus Tab does NOT do
- **No analytics or telemetry** of any kind (no Google Analytics, no Sentry,
  no Amplitude, no Mixpanel, etc.).
- **No advertising** and no ad SDKs.
- **No accounts, login, or authentication.**
- **No reading of your browsing history, other tabs, or any page content.** The
  extension only runs on its own new-tab page; it has no content scripts and no
  background worker that observes other sites.
- **No remote code.** Fonts, icons, background photos, and quotes are all
  bundled inside the extension. Quick-link tiles render as colored letter
  tiles, so adding a bookmark does **not** contact any third party.
- **No sale, transfer, or use of data for purposes unrelated to the extension's
  functionality.**

---

## 3. Permissions and why each is needed

| Permission | Why it's required |
|---|---|
| `storage` | To save your name, focus, to-dos, quick links, and settings so they persist between tabs and sync across your devices. |
| `geolocation` | To get approximate coordinates for local weather. Requested only when weather is used; denied gracefully if you decline. |
| Host permission: `api.open-meteo.com` | To fetch the current weather for your location. |
| Host permission: `api.bigdatacloud.net` | To turn your coordinates into a city name for display. |

All four are directly necessary for the features they support, and nothing
more.

---

## 4. Data security

- The only data that leaves your device are coordinates sent over **HTTPS** to
  the two weather services above.
- Your stored content (name, focus, to-dos, links, settings) is held by the
  browser's own storage and protected by the browser's standard storage
  controls. It is never transmitted by Focus Tab.

---

## 5. Children's privacy

Focus Tab is a general-purpose productivity tool and is not directed at
children under 13 (or the applicable age in your country). It does not
knowingly collect any personal information from children. The optional
geolocation feature uses only coarse, city-level accuracy when the user
explicitly enables it.

---

## 6. Your choices

- **Weather:** You can decline the location prompt, or simply not open the
  weather widget. No location is then obtained.
- **Quick links:** You don't have to add any. Tiles render locally without
  contacting any site.
- **Data removal:** Uninstall the extension to delete its data from that
  device. Synced copies are governed by your browser account's sync settings.
- **Browser sync:** You can disable Chrome/Brave sync to keep all stored data
  local to one device.

---

## 7. Changes to this policy

If the extension's data practices change, this policy will be updated and the
"Last updated" date above revised.

## 8. Contact

This is an independent project, unaffiliated with Momentum or any other product.
For privacy questions, please open an issue on the project's source repository
or contact the developer through the Chrome Web Store listing.
