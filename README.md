# Stylus

A next-generation YouTube client for Android. Built for speed, clean aesthetics, and a fluid spatial experience.

Status: Active Development • Designed for Android • Built with Flutter

## Table of Contents
- [Overview](#overview)
- [Design Language & Visual Engine](#design-language--visual-engine)
- [Core Experience](#core-experience)
- [Intelligent Feed Engine](#intelligent-feed-engine)
- [Seamless Updates](#seamless-updates)
- [Tech Stack & Architecture](#tech-stack--architecture)
- [Roadmap](#roadmap)
- [License & Rights](#license--rights)

## Overview

Stylus is an unofficial, reimagined YouTube client crafted to strip away the clutter and restore focus to the content you love. 

Instead of relying on heavily restricted public endpoints that yield generic results, Stylus uses a custom recommendation engine and official Google OAuth to build a feed that actually belongs to you. It delivers a futuristic user experience that blends real-time Liquid Glass UI, adaptive layouts, and fluid natural motion.

Whether you want a clean environment to watch your favorite creators, or a hyper-minimalist spatial interface, Stylus adapts effortlessly. 

## Design Language & Visual Engine

### Liquid Glass Aesthetic
Experience true translucent materials with hardware-accelerated glassmorphism. 
- **Real-Time Refraction:** The custom bottom dock utilizes the native power of `liquid_glass_easy` to bend and refract the content scrolling underneath it.
- **Adaptive Surfaces:** Elements dynamically blend with the dark theme and vibrant thumbnails to maintain perfect visual hierarchy.

### Fluid Motion & Typography
Every interaction is designed to feel natural and responsive.
- **Expansive Typography:** The app ditches the standard, cramped top bar in favor of expansive, collapsible SliverAppBars that prioritize readability.
- **Haptic Precision:** Thoughtful spacing, smooth scrolling, and edge-to-edge layouts create a premium browsing experience.

## Core Experience

### Custom Navigation Dock
The floating Liquid Glass dock acts as your central hub.
- **4-Pillar Navigation:** Access your Home (FYP), Subscriptions, Search, and Profile with fluid transitions.
- **Integrated Create Button:** A dedicated action button sits at the center of the dock, ready for creator tools.

### True Personal Subscriptions
Log in securely via Google OAuth. Stylus fetches your actual YouTube subscriptions and displays them in a beautiful, horizontal avatar rail. 
- **Subscriber Feed:** Watch the latest videos from the creators you actually follow, sorted chronologically for a true timeline experience.
- **In-App Playback:** Watch seamlessly using the embedded YouTube iFrame player, without leaving the app's aesthetic.

### Personalized Content Discovery
Youtube's official API restricts personalized recommendations. Stylus solves this by building its own local algorithm.

## Intelligent Feed Engine

Stylus calculates a dynamic "For You" score for videos by combining multiple data points:
- **Weighted Signals:** Channels you are subscribed to receive the highest priority.
- **Interaction History:** Videos from channels you have liked in the past get a boost.
- **Temporal Relevance:** Newer videos are scored higher to keep your feed fresh.
- **Smart Fallbacks:** If your history is sparse, Stylus intelligently blends in trending content without overwhelming your feed.

## Seamless Updates

Stylus features a built-in OTA (Over-The-Air) updater tied directly to GitHub Releases.
- **Auto-Check on Launch:** Every time you open the app, Stylus silently checks for a newer version.
- **Direct APK Download:** No need to visit the browser. The app downloads the new `.apk` directly and prompts the Android system installer to update instantly.

## Tech Stack & Architecture

Stylus is powered by a modern, robust Flutter stack:
- **Framework:** Flutter (Dart)
- **State Management:** Riverpod (Reactive & predictable state)
- **Authentication:** `google_sign_in` (OAuth 2.0 with YouTube readonly scopes)
- **API Integration:** `googleapis` (Official YouTube Data API v3)
- **Local Caching:** Hive (Lightning-fast local NoSQL database)
- **UI/UX:** `liquid_glass_easy`, `youtube_player_iframe`, `cached_network_image`

## Roadmap

- [x] Liquid Glass Dock implementation
- [x] Google OAuth Login & Session Persistence
- [x] Custom Local Recommendation Engine (FYP)
- [x] Subscriptions Feed & Channel Rail
- [x] In-App Video Player
- [x] GitHub OTA Updater
- [ ] Custom Video Player Overlay (Gestures for seeking/volume)
- [ ] Background Audio Playback (PiP)
- [ ] Playlist Management
- [ ] Shorts integration (if API permits)

## License & Rights

Stylus is an open-source project created and maintained by `hyper29tt-cpu`.

- This is an **unofficial** client. It is not affiliated with, endorsed by, or sponsored by YouTube or Google.
- Using the YouTube Data API is subject to the [YouTube API Services Terms of Service](https://developers.google.com/youtube/terms/api-services-terms-of-service).
- Stylus does not strip ads or bypass playback restrictions. It renders the official iFrame player exactly as YouTube serves it.
