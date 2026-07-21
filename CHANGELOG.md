# Changelog

All notable changes to Streamline are documented here.

The format is based on [Keep a Changelog](https://keepachangelog.com/),
and this project uses [Semantic Versioning](https://semver.org/).

## [1.1.0] — 2026-07-21

### Added
- Backup reminders — a gentle prompt to back up when you open or return to the app after making changes, capped to once per day so it never nags. A red dot on the Settings gear shows whenever you have un-backed-up changes.

### Changed
- Made the backup indicator dot red and larger with a subtle pulse so it's easier to notice (respects reduced-motion settings).
- Made the tag field's example text generic, so nothing personal ships with the app when shared outside the household.

## [1.0.0] — 2026-07-21

First complete release for the family.

### Added
- Multiple lists — keep separate watchlists (e.g. shared, kids, movie night); each tracks and syncs independently. A list you receive but don't have yet is created automatically.
- Backup & restore — export all lists, tags, progress, and household to a `.json` file; restore on a new or wiped device.
- Tags & filtering — free-form tags per show, tappable filter chips, and search across titles, platforms, people, and tags.
- Household setup — name the people sharing the app; each entry is stamped with who added it.
- Family sync — share a list via a tappable link; updates merge (newer progress wins, new shows added). QR invite to install the app on another phone.
- Show editing — edit a show's title, platform, status, and tags, or remove it.
- Installable app — home-screen icon, full-screen standalone mode, works offline.

### Changed
- Accent color changed from orange to a soft sage green; progress and completion markers moved to a soft dusty blue for contrast.

## [0.5.0] — 2026-07-21

### Changed
- Renamed the app to **Streamline** with a new play-and-streamlines icon.
- One-time automatic migration preserves data saved under the earlier name.

## [0.4.0] — 2026-07-21

### Added
- Backup and restore via exported files.

## [0.3.0] — 2026-07-21

### Added
- Custom tags and tag-based filtering.
- Search bar that appears once a list grows past a handful of shows.

## [0.2.0] — 2026-07-21

### Added
- Standalone single-file app: runs without a server, saves to each device.
- First-run household setup and per-person attribution.
- Link-based sync and QR invite.
- Home-screen install support.

## [0.1.0] — 2026-07-21

### Added
- Initial watchlist tracker: Watching, Queue, and Finished sections with per-season episode tracking and a progress dial.
- Share-code sync between devices.

---

## How to update this file

When you publish a new version of `index.html`:

1. Add a new section at the top under a new version number and today's date.
2. Group changes under **Added**, **Changed**, **Fixed**, or **Removed**.
3. Bump the version: patch (`1.0.1`) for small fixes, minor (`1.1.0`) for new features, major (`2.0.0`) for big or breaking changes.
