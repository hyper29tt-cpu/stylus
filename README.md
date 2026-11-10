# Stylus

An YouTube client for Android — built to make YouTube beautiful.

Status: Active Development • Android • Flutter

[![Download APK](https://img.shields.io/badge/Download-APK-brightgreen?style=for-the-badge&logo=android)](https://github.com/hyper29tt-cpu/stylus/releases/latest)

---

## 📥 Download & Install

Get the latest version directly from **GitHub Releases** — no Play Store required.

1. Go to the [**Releases page**](https://github.com/hyper29tt-cpu/stylus/releases/latest).
2. Download the latest `.apk` file.
3. Open the downloaded file on your Android device.
4. If prompted, allow **"Install from unknown sources"**.
5. Tap **Install** — done.

> **Auto-updates built in:** Stylus checks GitHub Releases on every launch and can download & install new versions directly, without opening a browser.

---

## Overview

Stylus is an unofficial YouTube client built to **make YouTube beautiful**.

It strips away the clutter and restores focus to the content you love — with a real-time **Liquid Glass UI**, adaptive layouts, and fluid natural motion. It also builds a personalized **For You** feed locally on your device, using your actual subscriptions and watch history.

> **Why Stylus?** YouTube's official API restricts personalized recommendations. Stylus works around this by ranking content locally — no third-party servers, no tracking, just your data working for you.

---

## Highlights

- **Liquid Glass UI** — true translucent materials, real-time refraction, adaptive surfaces.
- **Personal For You feed** — a local recommendation engine built from your subscriptions and history.
- **True subscriptions** — log in via Google OAuth and see your actual YouTube subscriptions in a clean timeline.
- **In-app playback** — watch without leaving the app's aesthetic.
- **OTA updates** — the app updates itself directly from GitHub Releases.

---

## Tech Stack

| Layer | Technology |
|---|---|
| Framework | Flutter (Dart) |
| State management | Riverpod |
| Authentication | `google_sign_in` (OAuth 2.0) |
| API integration | `googleapis` (YouTube Data API v3) |
| Local caching | Hive |
| UI/UX | `liquid_glass_easy`, `youtube_player_iframe`, `cached_network_image` |

---

## Roadmap

- [x] Liquid Glass UI
- [x] Google OAuth login & session persistence
- [x] Local For You recommendation engine
- [x] Subscriptions feed
- [x] In-app video player
- [x] GitHub OTA updater
- [ ] Custom video player overlay (seek/volume gestures)
- [ ] Background audio playback (PiP)
- [ ] Playlist management
- [ ] Shorts integration (if API permits)

---

## Building from Source

> Most users should just **[download the APK](#-download--install)**.

```bash
git clone https://github.com/hyper29tt-cpu/stylus.git
cd stylus
flutter pub get
flutter build apk --release
