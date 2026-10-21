# ECARLATE

**A local-first video workspace for people who actually watch, study, and review video.**

No accounts. No telemetry. No cloud. Everything stays on your machine.

![version](https://img.shields.io/badge/version-1.0.0-7c5cff)
![platform](https://img.shields.io/badge/platform-Windows-3d8bff)
![license](https://img.shields.io/badge/license-MIT-22c55e)
![made with](https://img.shields.io/badge/made%20with-Tauri%20%2B%20Rust-f59e0b)

---

## Why ECARLATE?

Most video players are built for *watching*. ECARLATE is built for **working with video**:

- You're learning from a lecture and want to **take timestamped notes**.
- You're reviewing footage and need to **step frame by frame**.
- You're studying a film and want to **search dialogue**, **track chapters**, **mark scenes**.
- You have a folder of 200 videos and want to **find that one line** you remember.

ECARLATE brings all of that into one keyboard-first desktop app — with a library, a queue, subtitles, transcripts, and a mini-player.

---

## Features

### Library
- Import files or whole folders (recursive scan)
- Grid of cards with real thumbnails, duration, resolution, size
- Favorites, collections, filters (recent / in-progress / unwatched / completed)
- Global search — **including dialogue search across transcripts**
- Drag-and-drop from Explorer
- Context menu: play, play next, add to queue, reveal, remove

### Player
- Keyboard-first controls (customizable in Settings)
- Timeline with **hover thumbnails**, chapter markers, scene markers
- Subtitle support (SRT / VTT / ASS / SSA) with offset, size, color, position, background
- Auto-find external subtitles next to the video file
- Speed control, jump step, PiP, fullscreen
- Chapters (from container metadata), scene detection (ffmpeg), user markers

### Transcripts
- **Local speech-to-text** using Whisper (no cloud, no API keys)
- 4 model sizes: Tiny / Base / Small / Medium
- 60+ languages supported
- Segments clickable to seek, auto-highlight during playback
- Full-text search across all transcripts (FTS5)

### Study & Review
- **Study view**: video + notes panel, timestamped notes saved per video
- **Review view**: video + markers panel, frame-by-frame stepping (`,` / `.`)

### Queue
- Persistent queue (survives restarts)
- Shuffle, repeat (off / all / one), drag-to-reorder
- "Play all" from any filtered view

### Mini player
- Compact always-on-top window
- Full playback controls, draggable
- Global shortcuts: `F9` toggle mini, `F10` toggle always-on-top

### Extras
- 5 accent colors, light/dark/system theme
- Adjustable UI scale (80% – 130%)
- Custom shortcuts (rebindable)
- Storage stats, cache management
- Native system media controls (SMTC on Windows)

---

## Screenshots

> *(Screenshots)*

---

## Installation

### Windows

Download the latest installer from the [Releases page](https://github.com/lancelotech-app/ecarlate/releases):

- `ECARLATE_1.0.0_x64-setup.exe` — NSIS installer (per-machine)
- `ECARLATE_1.0.0_x64_en-US.msi` — MSI installer

Run the installer, launch ECARLATE, and you're set.

### Bundled dependencies

ECARLATE ships with `ffmpeg.exe` and `ffprobe.exe` bundled — no separate install required.

Whisper models are **not** bundled (they range from 75 MB to 1.5 GB). Download them from **Settings → Storage → Whisper models** when you need transcription.

---

## Building from source

### Requirements

- [Rust](https://rustup.rs/) 1.90+
- [Node.js](https://nodejs.org/) 20+
- [Tauri CLI](https://tauri.app/v1/guides/getting-started/prerequisites)
- Windows: Visual Studio Build Tools + WebView2
