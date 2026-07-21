# Streamline

A private, self-hosted watchlist app for tracking TV shows across every streaming service — built to run entirely on your own phones with no accounts, no servers, and no data leaving your device.

Streamline is a single, self-contained HTML file. Host it anywhere static (GitHub Pages, a home server, a Raspberry Pi) and add it to your phone's home screen. It works offline, saves to each device locally, and syncs between family members with a tap.

---

## Features

- **Track progress** — mark shows as Watching, Queued, or Finished, with per-season episode tracking and a visual progress dial.
- **Multiple lists** — keep separate lists for different groups or moods (e.g. shared, kids, movie night). Each list tracks and syncs on its own.
- **Tags & filtering** — add free-form tags like `date night` or `with the kids`, then filter by them. Search matches titles, platforms, people, and tags.
- **Family sync** — share a list with a tappable link. Updates merge intelligently: newer progress wins, new shows are added, nothing is overwritten blindly. A list you don't have yet is created automatically when you receive it.
- **Backup & restore** — export everything (all lists, tags, progress, household) to a file you keep in cloud storage; restore on a new phone in seconds.
- **Private by design** — watchlists live only on each device. Data moves only when you deliberately send a sync link. Nothing is uploaded anywhere.
- **Installable** — add to the home screen for a full-screen, offline, app-like experience.

---

## Quick start

### Use it right away
Open `index.html` in a mobile browser. It works immediately and saves your data. (Tappable sync links and QR codes need hosting — see below.)

### Host it (recommended)
Any static host works. For a free option:

1. Put `index.html` in a repository and enable **GitHub Pages** (Settings → Pages → deploy from the `main` branch, root folder).
2. Open the resulting URL on each phone.
3. Tap **Share → Add to Home Screen**.

That's it — the app now opens full-screen, works offline, and sync is live.

> For a fully private option, host it on a home server or Raspberry Pi on your LAN, reachable over a VPN when away from home.

---

## How it works

| Area | Detail |
|------|--------|
| **Storage** | Each device keeps its own copy in local browser storage. No backend. |
| **Sync** | A list is packed into a link; the recipient's app decodes and merges it. Works over any connection — WiFi, cell data, or offline via AirDrop. |
| **Merge rule** | Per show, the most recently edited version wins. New shows are added. Lists are matched by ID, so shared lists stay in sync rather than duplicating. |
| **Updates** | Re-host a new `index.html` at the same URL. Because storage is tied to the URL, everyone's data stays intact. |

---

## Backups

Because data lives on each device, keep a backup:

- **Settings → Save backup file** exports all lists to a dated `.json` file. Keep it in iCloud or Drive.
- **Settings → Restore from a backup file** brings everything back on a new or wiped device.

Recommended: export a backup now and then, and always before switching phones or changing where the app is hosted.

---

## Privacy

- Watchlists are stored locally on each phone and are never uploaded.
- Hosting the app publicly exposes only the app's code, never anyone's lists.
- The only time list data leaves a device is when a person chooses to send a sync link.

---

## Tech

- Single self-contained HTML file — no build step, no dependencies to install.
- Vanilla JavaScript and CSS.
- Bundles [qrcode-generator](https://github.com/kazuhikoarase/qrcode-generator) (MIT) for invite QR codes; its license notice is retained inline.

---

## License

Released under the MIT License. See [LICENSE](LICENSE).
