# Stylus

A next-generation YouTube client for Android — built for speed, clean aesthetics, and a fluid spatial experience.

Status: Active Development • Android • Flutter

[![Download APK](https://img.shields.io/badge/Download-APK-brightgreen?style=for-the-badge&logo=android)](https://github.com/hyper29tt-cpu/stylus/releases/latest)

---

## 📥 Download & Install

Get the latest version directly from **GitHub Releases** — no Play Store required.

1. Go to the [**Releases page**](https://github.com/hyper29tt-cpu/stylus/releases/latest).
2. Download the latest `.apk` file (e.g. `stylus-v1.0.0.apk`).
3. On your Android device, open the downloaded file.
4. If prompted, allow **"Install from unknown sources"** for your browser/file manager.
5. Tap **Install** — done.

> **Auto-updates built in:** Once installed, Stylus checks GitHub Releases on every launch and can download & install new versions directly, without opening a browser.

---

## Overview

Stylus is an unofficial, reimagined YouTube client that strips away the clutter and restores focus to the content you love.

Instead of relying on heavily restricted public endpoints that yield generic results, Stylus combines a **custom recommendation engine** with **official Google OAuth** to build a feed that actually belongs to you. It delivers a futuristic experience that blends a real-time **Liquid Glass UI**, adaptive layouts, and fluid natural motion.

Whether you want a clean environment to watch your favorite creators or a hyper-minimalist spatial interface, Stylus adapts effortlessly.

> **Why Stylus?** YouTube's official API restricts personalized recommendations. Stylus works around this by ranking content locally on your device — no third-party servers, no tracking, just your data working for you.

---

## Design Language & Visual Engine

### Liquid Glass Aesthetic

True translucent materials with hardware-accelerated glassmorphism.

- **Real-time refraction** — the custom bottom dock uses `liquid_glass_easy` to bend and refract the content scrolling beneath it.
- **Adaptive surfaces** — elements dynamically blend with the dark theme and vibrant thumbnails to maintain perfect visual hierarchy.

### Fluid Motion & Typography

Every interaction is designed to feel natural and responsive.

- **Expansive typography** — Stylus ditches the cramped standard top bar in favor of expansive, collapsible `SliverAppBars` that prioritize readability.
- **Haptic precision** — thoughtful spacing, smooth scrolling, and edge-to-edge layouts create a premium browsing experience.

---

## Core Experience

### Custom Navigation Dock

The floating Liquid Glass dock is your central hub.

- **4-pillar navigation** — Home (For You), Subscriptions, Search, and Profile with fluid transitions.
- **Integrated create button** — a dedicated action button sits at the center of the dock, ready for creator tools.

### True Personal Subscriptions

Log in securely via Google OAuth. Stylus fetches your actual YouTube subscriptions and displays them in a beautiful horizontal avatar rail.

- **Subscriber feed** — watch the latest videos from creators you actually follow, sorted chronologically for a true timeline experience.
- **In-app playback** — watch seamlessly with the embedded YouTube iFrame player, without leaving the app's aesthetic.

### Personalized Content Discovery

A local recommendation engine that learns what you actually watch.

---

## Intelligent Feed Engine

Stylus calculates a dynamic **"For You" score** for each video by combining multiple signals:

| Signal | How it works |
|---|---|
| **Weighted subscriptions** | Channels you subscribe to receive the highest priority. |
| **Interaction history** | Videos from channels you've liked in the past get a boost. |
| **Temporal relevance** | Newer videos score higher to keep your feed fresh. |
| **Smart fallbacks** | If your history is sparse, Stylus intelligently blends in trending content without overwhelming your feed. |

All scoring happens **on-device**. Your watch behavior never leaves your phone.

---

## Seamless Updates

Stylus features a built-in OTA (Over-The-Air) updater tied directly to GitHub Releases.

- **Auto-check on launch** — every time you open the app, Stylus silently checks for a newer version.
- **Direct APK download** — no need to visit the browser. The app downloads the new `.apk` directly and prompts the Android system installer to update instantly.

---

## Tech Stack & Architecture

| Layer | Technology |
|---|---|
| Framework | Flutter (Dart) |
| State management | Riverpod (reactive & predictable state) |
| Authentication | `google_sign_in` (OAuth 2.0, YouTube readonly scopes) |
| API integration | `googleapis` (official YouTube Data API v3) |
| Local caching | Hive (lightning-fast local NoSQL database) |
| UI/UX | `liquid_glass_easy`, `youtube_player_iframe`, `cached_network_image` |

---

## Roadmap

- [x] Liquid Glass dock implementation
- [x] Google OAuth login & session persistence
- [x] Custom local recommendation engine (For You)
- [x] Subscriptions feed & channel rail
- [x] In-app video player
- [x] GitHub OTA updater
- [ ] Custom video player overlay (seek/volume gestures)
- [ ] Background audio playback (PiP)
- [ ] Playlist management
- [ ] Shorts integration (if API permits)

---

## Building from Source

> Most users should just **[download the APK](#-download--install)**. Follow these steps only if you want to build it yourself.

```bash
# Clone the repository
git clone https://github.com/hyper29tt-cpu/stylus.git
cd stylus

# Install dependencies
flutter pub get

# Configure Google OAuth (see docs/OAUTH.md)
# ...

# Build a release APK
flutter build apk --release
