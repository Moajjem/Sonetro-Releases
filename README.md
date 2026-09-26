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

### Latest Release — 1.1.927

- Redesigned Home with smoother panoramic scrolling and more responsive movement.
- Added wider History and New screens with tiles in multiple sizes.
- Added a featured History tile that shows whether a song is playing or paused.
- Song taps in History, New, and library lists start playback and open Live with a smooth transition.
- Improved Home layouts for different screen sizes and display settings.
- Aligned headings, tiles, and navigation arrows throughout Home.
- Refined text size and spacing in History and New.
- Simplified song indicators: cloud music shows a cloud icon, while local music has no icon.

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
