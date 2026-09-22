# Sonetro

**A modern music player for Android, built for local libraries and self-hosted music.**

Sonetro is designed around a clean listening experience, flexible library management, responsive home screen widgets, and direct integration with your own music servers.

It supports local music as well as Plex, Jellyfin, and Subsonic-compatible servers.

---

## Features

### Your Music, Your Library

- Play music stored directly on your device
- Connect directly to Plex servers
- Connect directly to Jellyfin servers
- Support for Subsonic-compatible music servers
- Browse and manage multiple music libraries
- Remove songs from Sonetro without deleting the original files
- Permanently delete local files with explicit confirmation
- Improved library and playlist management

### Playback

- Reliable background playback
- Queue and Up Next support
- Improved playback recovery after interruptions
- Better reconnection after service restarts
- Crossfade support
- Favorites
- Live playback view
- Dynamic Up Next predictions

### Home Screen Widgets

Sonetro includes a fully responsive widget system designed to adapt to different Android launchers and widget sizes.

- 19 adaptive widget configurations
- Circular **Vinyl** widget
- Live playback progress
- Responsive typography
- Dynamic artwork
- Album art persistence
- Dynamic theming
- Automatic layout adaptation
- Progress rings and playback indicators
- Improved artwork loading and recovery

### Personalization

- Custom song and artist background images
- Dynamic artwork
- Multiple accent colors
- Black
- White
- Coral
- Indigo
- Responsive interface typography
- Improved contrast for light and dark accents
- Appearance customization

### Privacy

Sonetro does **not collect or sell your personal data**.

There are no analytics trackers used to profile your listening activity, and your music library remains under your control.

Connections to Plex, Jellyfin, Subsonic, and other self-hosted servers are made directly from your device.

---

## Supported Sources

| Source | Support |
| --- | --- |
| Local Android music | ✅ |
| Plex | ✅ |
| Jellyfin | ✅ |
| Subsonic-compatible servers | ✅ |

---

## Installation

Download the latest Sonetro release from the **Releases** section of this repository.

> When installing an APK manually, Android may ask you to allow installation from your browser or file manager.

### Updating

You can normally install a newer Sonetro APK over your existing installation without removing the previous version.

Your app data and settings should remain intact when updating normally.

---

## What's New

### Latest Release

- Added native **Plex and Jellyfin support** for easier server discovery, setup, and playback.
- Added **Remove from Library**, allowing songs to be hidden from Sonetro without deleting the original files.
- Improved library management with clearer confirmation for individual and bulk removals.
- Improved permanent file deletion with safer Android system handling.
- Added a new **heart shower animation** and refined favorite transitions.
- Added support for **custom song and artist background images**.
- Improved heading responsiveness across different screen sizes and accessibility font settings.
- Improved playback resume behavior and reconnection reliability.
- Improved **Up Next** predictions so they update according to the duration of the current track.
- Added **Black, White, Coral, and Indigo** accent colors.
- Improved interface contrast for neutral and dynamic accent colors.
- Renamed **Look** to **Appearance** in Settings.
- Improved library selection for self-hosted music servers.
- Improved local network compatibility for Plex, Jellyfin, Subsonic, and similar servers.
- Redesigned the home screen widget system with **19 adaptive layouts**.
- Added the circular **Vinyl** widget.
- Added smoother, high-frequency widget playback progress.
- Improved widget performance and memory usage.
- Improved widget artwork loading, retries, and duplicate request handling.
- Improved remote Subsonic artwork support.
- Added a **Windows Phone 7-inspired contextual dialog animation**.
- Improved dialog dimming across system bars and different screen sizes.
- Improved widget typography, progress rendering, artwork persistence, and dynamic theming.
- Improved widget and playback recovery after service restarts.
- Various performance, stability, playback, library, animation, and visual improvements.

---

## Self-Hosted Server Notes

For local Plex, Jellyfin, and Subsonic servers, Sonetro can communicate directly with servers on your local network.

Some local server configurations may use:

- Local IP addresses
- Custom ports
- HTTP instead of HTTPS
- User-installed certificates
- Self-hosted HTTPS certificates

Make sure your Android device can access the server from the same network.

---

## Permissions

Depending on the features you use, Sonetro may request access to:

- Music and audio files
- Network access
- Notifications / media playback controls
- Android's system file deletion confirmation

Sonetro only requests permissions required for the features you choose to use.

---

## Feedback

Found a bug or have an idea for Sonetro?

Open an issue in this repository and include as much relevant information as possible, such as:

- Sonetro version
- Android version
- Device model
- Music source being used
- Steps to reproduce the problem

Please avoid posting passwords, access tokens, server credentials, or other private information in public issues.

---

## Disclaimer

Sonetro is an independent application.

Plex, Jellyfin, Subsonic, Android, and other product names are trademarks of their respective owners. Sonetro is not affiliated with or endorsed by those projects unless explicitly stated.

---

## Sonetro

**Your library. Your servers. Your music.**
