<p align="center">
  <img src="assets/app-icon.png" width="104" height="104" alt="Sonetro app icon">
</p>

<h1 align="center">Sonetro — Offline Music Player</h1>

<p align="center">
  <strong>A polished, local-first music player for Android, built with Kotlin and Jetpack Compose.</strong>
</p>

<p align="center">
  <img src="https://img.shields.io/badge/Android-7.0%2B-3DDC84?logo=android&logoColor=white" alt="Android 7.0 or newer">
  <img src="https://img.shields.io/badge/Kotlin-2.2-7F52FF?logo=kotlin&logoColor=white" alt="Kotlin 2.2">
  <img src="https://img.shields.io/badge/UI-Jetpack%20Compose-4285F4" alt="Jetpack Compose interface">
  <img src="https://img.shields.io/badge/Playback-Media3-0D9488" alt="Media3 playback">
</p>

## Overview

Sonetro brings music stored on your device, optional personal music servers, and internet radio into one player. Its panoramic Home connects Live playback, Collection, History, and New, with responsive controls and artwork-led browsing.

Playback continues in the background through a media session service. Library discovery, playback state, offline downloads, widgets, and settings are handled on the device; no Sonetro account is required.

<p align="center">
  <a href="https://github.com/Moajjem/Sonetro-Releases/releases/latest"><strong>Download the latest release</strong></a>
  &nbsp;·&nbsp;
  <a href="https://github.com/Moajjem/Sonetro-Releases/releases/tag/v1.1.960">See what’s new</a>
  &nbsp;·&nbsp;
  <a href="https://github.com/Moajjem/Sonetro-Releases/issues">Get help</a>
</p>

---

## Meet your music

<p align="center">
  <img src="assets/live-preview-1.1.960.png" width="240" alt="Sonetro Live player with artist background and playback controls">
</p>

<p align="center"><strong>Live</strong> · <strong>Collection</strong> · <strong>History</strong> · <strong>New</strong></p>

Swipe through a panoramic Home, revisit songs in History, discover recent additions in New, and open any song in Live. The interface adapts to different phone sizes while keeping playback close at hand.

## At a glance

| | |
| --- | --- |
| Platform | Android 7.0 or newer |
| Current release | [1.1.960](https://github.com/Moajjem/Sonetro-Releases/releases/tag/v1.1.960) |
| Distribution | Signed APK in the [Releases](https://github.com/Moajjem/Sonetro-Releases/releases) section |
| Account | No Sonetro account required |

## Features

### Listen

- Play device music and tracks from a connected personal server.
- Continue listening in the background with notification, lock screen, headset, and compatible car controls.
- Use the Live player, mini-player, queue, seeking, shuffle, repeat, and playback controls.
- Resume the current track and queue after an interruption or app restart.
- View embedded or online lyrics, follow timestamped lines, and import, replace, or remove custom lyrics from the lyrics heading.
- Adjust playback with equalizer presets and other audio settings.

### Explore your library

- Browse music, artists, albums, playlists, downloads, and Radio+; manage included and excluded device folders in Settings.
- Search across available library content and move from a song list directly into Live playback.
- Use the panoramic Home view to move between Live, Collection, History, and New.
- See recent and newly added tracks in mixed-size artwork tiles. The featured History tile shows the current playing or paused state.
- Organize playlists and manage local files through Android's confirmation flows.

### Discover radio

- Stream internet radio inside the same Live player used for music.
- Browse genres, recently played stations, stations from your country, geographical locations, globally popular stations, and saved stations.
- Search globally by station name, country, region, genre, language, or available tags. Optional country, genre, language, location, and popularity filters refine the results.
- Star stations from their rows, contextual menus, or the Live drawer. Saved stations and deduplicated recents persist across app restarts.
- Use station artwork and available song/artist broadcast information; scan moves to another station.
- Local Radio requests approximate location access to identify your country. Location browsing also works independently through country selection, with finer levels when metadata is available.

### Make it yours

- Choose appearance and accent colors, and use artwork in the app background.
- Set one custom artist background for all songs by that artist, or remove it directly from the context menu.
- Add adaptable home screen widgets with artwork, transport controls, and playback progress.
- Browse Settings with a category sidebar on wide screens, or the familiar swipeable layout on regular phones.
- Use layouts that respond to screen size, display density, and text settings.

## What’s new in 1.1.960

- Added **Radio+**, with Genre, Recents, Local Radio, Location, Most Popular, and Saved browsing.
- Added global station search with partial matching, optional filters, incremental loading, and persistent station favorites and recents.
- Radio plays in the shared Live player with station artwork, available broadcast metadata, and a scan action. “Add to…” is disabled while radio is the active playback source.
- Back from Live returns to the originating music or radio list, preserving the browsing context and radio search results.
- Improved reusable page-turn animation resources and queue reuse for song selection and shuffle all, plus the Live next/previous cover slide.
- Refined artist background selection, Radio helper-text spacing, contextual actions, and widget previews.

Read the [full release notes](release-notes/1.1.960.md).

## Install or update

1. Open the [latest release](https://github.com/Moajjem/Sonetro-Releases/releases/latest) on your Android device.
2. Download the `Sonetro-<version>-release.apk` asset.
3. Open the downloaded file and follow Android's installation prompts. Your browser or file manager may need permission to install apps.

To update, install the newer signed APK over the existing app. Keep the installed app in place if you want to retain its data and settings. Android accepts an in-place update only when the APK has the same application ID, a compatible signing certificate, and a suitable version code.

**Release 1.1.960 verification:** SHA-256 of `Sonetro-1.1.960-release.apk`:

```text
a58760f1a8b464d4d0e45e6a07408816f84a71f6fab747fc03c6aa1e7ed926ee
```

## How Sonetro is built

Sonetro is a Kotlin app with a Jetpack Compose interface. Its major parts work together as follows:

```text
Device music ── Android media library ──┐
                                         ├── Unified library ── Browse and search
Personal server ── Provider adapters ───┘          │
                           │                        └── Playback queue
                           └── Sync and downloads             │
                                    │                 Media session service
                              Offline storage                 │
                                                    App, system controls, widgets
```

| Layer | Responsibility |
| --- | --- |
| Interface and navigation | Compose screens, the Home panorama, responsive layout rules, and transitions between lists and Live. |
| Library state | A lifecycle-aware view model combines device tracks, server catalog entries, playlists, favorites, history, and the active queue into observable UI state. |
| Device library | Android's media library supplies local tracks and metadata; Sonetro refreshes when the device library changes. |
| Server integration | Provider adapters connect to configured personal servers and present their catalogs alongside device music. |
| Radio discovery | Radio Browser queries, station identities, saved stations, recent listening, and browsing/search state feed the shared player. |
| Playback | A Media3 media library service owns the player and session so playback and system controls continue outside the app screen. |
| Offline music | Background workers synchronize catalog data and manage downloads. A local SQLite store tracks server catalog and offline state. |
| Widgets | Android widgets read playback state and provide artwork, progress, and transport actions. |
| Preferences | On-device settings retain appearance, playback choices, and library configuration. |

This is an architectural overview of the app, not a claim that this releases repository contains its source code. The releases repository hosts installable builds and user-facing release information.

## Music sources and connectivity

Device music is available after granting Android's audio access permission. Personal server access is optional and requires a server you can reach from your device. Server authentication, library selection, and offline downloads are managed in the app's settings.

A network connection is needed for internet radio discovery and streaming through Radio Browser, server discovery, streaming, synchronization, online lyrics from LRCLIB, and artist-portrait lookup through MusicBrainz and TheAudioDB. Tracks downloaded for offline listening remain available when the server is unreachable. Availability can depend on the file, server configuration, connection, and Android device.

## Privacy and permissions

Sonetro has no app account requirement, advertising SDK, or analytics SDK. Library data, preferences, playlists, radio favorites, and listening history are kept on the device. Radio search sends queries to Radio Browser, station playback connects to the broadcaster, and directory-backed plays may report a station click to Radio Browser. Local Radio uses Android location/geocoding services when you grant location access. When you configure a personal server, the app connects to that server for the features you choose to use. Online lyrics and artwork lookups send relevant track or artist metadata to their providers; device lyrics imports are stored locally.

Android may ask for access to audio files, notifications, and approximate location for Local Radio. Background playback uses a foreground media service. Deleting or changing local files may trigger an Android system confirmation. Grant only the permissions needed for the features you use.

## Help and feedback

For a problem or feature request, [open an issue](https://github.com/Moajjem/Sonetro-Releases/issues). Include the Sonetro version, Android version, device model, music source, and steps to reproduce the behavior. Do not post passwords, access tokens, or other private details.

Sonetro is an independent application. This repository distributes its release builds; use and redistribution remain subject to the rights granted by the publisher.
