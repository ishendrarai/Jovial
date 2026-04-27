# 🎵 Jovial — The Music Streaming Platform That Feels Alive Together

> Listen alone. Vibe together. Sync everywhere.  
> The music player that connects hearts, rooms, and devices in perfect harmony.

![Node](https://img.shields.io/badge/Node.js-18+-green)
![React](https://img.shields.io/badge/React-18+-blue)
![MongoDB](https://img.shields.io/badge/MongoDB-7-brightgreen)
![Socket.io](https://img.shields.io/badge/Socket.io-4+-black)
![WebRTC](https://img.shields.io/badge/WebRTC-Enabled-orange)
![Redis](https://img.shields.io/badge/Redis-7-red)
![License](https://img.shields.io/badge/License-MIT-yellow)
![Status](https://img.shields.io/badge/Status-Production--Ready-success)

---

## 📌 Table of Contents

- [✨ Overview](#-overview)
- [🚀 Why Jovial?](#-why-jovial)
- [🌐 Live Demo](#-live-demo)
- [📸 Screenshots](#-screenshots)
- [🔥 Core Features](#-core-features)
- [⭐ Unique Features — Deep Dive](#-unique-features--deep-dive)
- [🛠 Tech Stack](#-tech-stack)
- [🏗 Architecture](#-architecture)
- [🔐 Authentication](#-authentication)
- [🗄 Database Schema](#-database-schema)
- [🔌 API Documentation](#-api-documentation)
- [📡 WebSocket & Real-Time Events](#-websocket--real-time-events)
- [🔊 Device Sync (StereoLink) — Technical Design](#-device-sync-stereolink--technical-design)
- [🔐 Security](#-security)
- [⚡ Performance](#-performance)
- [🧪 Testing](#-testing)
- [📋 Prerequisites](#-prerequisites)
- [⚙ Installation & Setup](#-installation--setup)
- [🌍 Environment Variables](#-environment-variables)
- [📁 Project Structure](#-project-structure)
- [🚀 Deployment](#-deployment)
- [🔧 Troubleshooting](#-troubleshooting)
- [❓ FAQ](#-faq)
- [📊 Design Decisions](#-design-decisions)
- [🛣 Roadmap](#-roadmap)
- [🤝 Contributing](#-contributing)
- [👥 Contributors](#-contributors)
- [📄 License](#-license)
- [📬 Contact](#-contact)

---

## ✨ Overview

**Jovial** is a full-stack music streaming platform built on the MERN stack that reimagines how people experience music — together. Beyond being a beautifully crafted personal player with a reel-style swipe interface, Jovial introduces two breakthrough features that no mainstream streaming platform has ever shipped properly:

| Feature | Status | Capability |
|---|---|---|
| 🟢 Reel-Style Player | Full Integration | Swipe to change tracks, full controls, lyrics overlay |
| 🟢 Together Mode (Couple) | Full Integration | 2 people, 1 queue, real-time sync, shared controls |
| 🟢 Listening Room | Full Integration | Group sessions, room creator controls, invite links |
| 🟢 StereoLink (Device Sync) | Full Integration | 2 phones sync as stereo speakers over local network |
| 🟢 Real-Time Chat in Rooms | Full Integration | In-session chat, emoji reactions, song requests |
| 🟢 Personalised Discovery | Full Integration | Mood-based recommendations, listen history, smart queues |

Jovial is built for people who believe music is best when it's **shared** — whether that's two people falling asleep to the same playlist, a group of friends hosting a virtual DJ room, or two phones placed side by side turning any room into a speaker system.

---

## 🚀 Why Jovial?

### The Problem

Music listeners today face a fragmented, isolating experience:

- ❌ **Streaming is solitary** — Spotify's Group Session is clunky, limited, and requires Premium
- ❌ **No real device sync** — Bluetooth pairs to one device only; AirPlay is Apple-only
- ❌ **Couple listening is an afterthought** — No platform treats 2-person listening as a first-class feature
- ❌ **Boring player UIs** — Traditional list-style players lack the tactile, scroll-through-music joy
- ❌ **Group rooms need a DJ** — One person controls the queue and everyone else just follows

### The Solution

Jovial acts as a **social music layer** on top of a world-class streaming player:

- ✅ **Reel-style music discovery** — Swipe through tracks like scrolling a feed, feel the vibe before committing
- ✅ **Together Mode** — Two people listen with perfect millisecond-level sync, both can control playback
- ✅ **Listening Rooms** — Create a room, invite anyone, the creator holds the remote, everyone enjoys
- ✅ **StereoLink** — Two phones on the same Wi-Fi become left and right speakers of a virtual stereo system
- ✅ **Built for mobile-first** — Every gesture, every animation, every feature designed around mobile

> It's not just a music app. It's a **shared listening experience**.

---

## 🌐 Live Demo

🔗 **https://jovial-app.vercel.app**

### Test Credentials

```
Email:    demo@jovial.music
Password: demo1234
```

> **Note:** Demo account comes with pre-populated playlists, a seeded Together Mode room, and a mock StereoLink demo session.

---

## 📸 Screenshots

### 🎵 Reel-Style Player
![Player](./screenshots/reel-player.png)
*Swipe up/down to change tracks — full controls, album art blur background, lyrics overlay*

### 💑 Together Mode
![Together](./screenshots/together-mode.png)
*Two listeners, one queue — see your partner's avatar, share controls in real time*

### 🏠 Listening Room
![Room](./screenshots/listening-room.png)
*Room creator holds the remote — guests listen, react, and request songs*

### 🔊 StereoLink Device Sync
![StereoLink](./screenshots/stereolink.png)
*Two phones detected on the same network — assign left/right channel, hit play*

---

## 🔥 Core Features

### 🎵 Reel-Style Music Player
- **Swipe to change tracks** — Swipe up for next, down for previous, just like reels/shorts
- **Full playback controls** — Play/pause, seek bar, shuffle, repeat (one/all/off), volume
- **Visualiser** — Live audio waveform visualiser synced to the current track
- **Lyrics overlay** — Time-synced rolling lyrics powered by Musixmatch API
- **Sleep timer** — Auto-stop playback after a set duration
- **Queue management** — Drag-to-reorder queue, add next, add to end, clear queue
- **Crossfade** — Smooth 1–12 second crossfade between tracks
- **Background playback** — Continues playing when screen locks or browser tabs switch
- **Offline cache** — Last 10 played tracks cached for offline replay

### 🔍 Music Discovery
- **Smart search** — Search by track, artist, album, genre, mood, or BPM
- **Mood-based queues** — Auto-generate queues from mood tags: Chill, Hype, Sad, Focus, Party
- **Trending section** — Real-time trending by region and genre
- **Artist radio** — Infinite auto-queue seeded from any artist or track
- **Recently played** — Full history with timestamps and session context
- **Liked songs** — Personal library with smart sorting options

### 👤 User Profiles & Social
- **Public profile** — Show off listening stats, favourite artists, playlists
- **Follow system** — Follow friends, see what they're listening to (with privacy controls)
- **Activity feed** — Recent plays, new playlists, Together Mode sessions from followed users
- **Listening stats** — Weekly/monthly wrapped-style stats: top artists, genres, total minutes
- **Shareable links** — Share any track, album, playlist, or room with a deep link

### 📚 Library & Playlists
- **Unlimited playlists** — Create, edit, reorder, add covers, set privacy
- **Collaborative playlists** — Invite friends to co-edit a playlist
- **Smart playlists** — Auto-update playlists based on rules (e.g., "liked songs from 2023 with BPM > 120")
- **Import from Spotify** — One-click playlist migration from Spotify using public API
- **Download for offline** — Cache full playlists locally (mobile)
- **Folders** — Organise playlists into folders

---

## ⭐ Unique Features — Deep Dive

### 💑 Feature 1: Together Mode & Listening Rooms

This is the heart of Jovial. Music is inherently social — Jovial makes that real.

#### 🔹 Together Mode (2-Person Listening)

Together Mode is a private, intimate 2-person listening session where both users are perfectly synced to the same song at the same millisecond.

**How it works:**

```
User A                       Server (Socket.io)              User B
  │                                  │                          │
  │── Create Together Session ──────►│                          │
  │◄─ session_id + join_link ────────│                          │
  │                                  │◄── Join via link ────────│
  │                                  │── Sync state to both ───►│
  │                                  │                          │
  │── Play/Pause/Seek ──────────────►│── Broadcast to B ───────►│
  │◄─ Confirm + timestamp ───────────│◄─ B also controls ───────│
  │                                  │── Broadcast to A ────────│
```

**Key capabilities:**
- 🔁 **Bidirectional control** — Both users can play, pause, seek, skip, and change volume. Changes are reflected on both screens instantly
- 🕐 **Millisecond-level sync** — Server-authoritative timestamp with client-side NTP-style clock offset correction ensures sub-100ms sync
- 🎵 **Shared queue** — Either user can add tracks, reorder the queue, or skip
- 🟢 **Presence indicators** — See a live avatar bubble showing your partner's online status
- 💬 **Reaction bar** — Send emoji reactions that float over the album art in real time
- 🎙 **Sync chat** — Lightweight text chat anchored to the current track ("this part 🔥")
- 🔔 **Push notifications** — Get notified when your partner starts a session and invites you
- 🔒 **Private by default** — Sessions are invite-only via a one-time link or direct user invite

#### 🔹 Listening Rooms (Group Sessions)

Listening Rooms extend Together Mode to support 2 to 50 listeners simultaneously, with clear role-based control.

**Room Roles:**

| Role | Permissions |
|---|---|
| 👑 **Room Creator / DJ** | Full control: play, pause, seek, skip, add/remove tracks, kick users, change room settings |
| 🎤 **Co-DJ** (optional) | Creator can grant Co-DJ status to specific listeners — they get full playback control |
| 👂 **Listener** | Hear everything in sync, send reactions, send song requests, participate in chat |

**Room Features:**
- 🔗 **Shareable room link** — Invite anyone with a URL, no account required to join as a guest
- 🎧 **Live listener count** — See who's in the room and their avatars in a scrollable panel
- 📨 **Song Request system** — Listeners submit requests; DJ sees a request queue and can accept/reject
- 🗳 **Vote to skip** — If majority votes to skip, the DJ gets a notification (optional mode: auto-skip)
- 💬 **Live room chat** — Full chat panel with emoji support, song mentions, and timestamps
- 🔊 **Room audio quality setting** — DJ can set the stream quality (128 / 256 / 320 kbps)
- 📖 **Room history** — Full log of songs played in the session
- 🔒 **Room privacy modes** — Public (discoverable), Unlisted (link-only), Private (invite-only)
- ⏰ **Scheduled rooms** — Schedule a room in advance; followers get a reminder notification
- 🎨 **Room themes** — Customisable room background — gradient, image, or album-art-reactive blur

**Room Sync Architecture:**

```
┌──────────────────────────────────────────────────────────────┐
│                     LISTENING ROOM                           │
│                                                              │
│  ┌──────────────┐   Socket.io Room Namespace                 │
│  │  Room Creator│◄──── room:{roomId} ────────────────────┐  │
│  │  (DJ)        │                                         │  │
│  └──────┬───────┘   Server-Authoritative                  │  │
│         │           Playback State                        │  │
│  ┌──────▼──────────────────────────────────────────────┐  │  │
│  │              ROOM STATE (Redis)                     │  │  │
│  │  currentTrack | position_ms | is_playing | queue    │  │  │
│  │  listeners[] | chat[] | requests[] | settings       │  │  │
│  └──────┬──────────────────────────────────────────────┘  │  │
│         │ Broadcast on every state change                  │  │
│  ┌──────▼──────────────────────────────────────────────┐  │  │
│  │   Listener 1   Listener 2   ...   Listener N        │  │  │
│  │   (Receiver)   (Receiver)         (Receiver)        │──┘  │
│  └─────────────────────────────────────────────────────┘     │
└──────────────────────────────────────────────────────────────┘
```

---

### 🔊 Feature 2: StereoLink — Dual Device Sync Speaker

StereoLink is Jovial's most technically innovative feature. It turns **two smartphones into a stereo speaker pair** — one device plays the left audio channel, the other plays the right channel, both perfectly time-synced over a local Wi-Fi network.

**The Vision:**

Place your phone and your friend's/partner's phone side by side. Both play Jovial. Tap "StereoLink". In seconds, your room transforms into a stereo sound system — music feels spatially wide, immersive, and powerful.

#### How StereoLink Works — Step by Step

```
Step 1: Discovery
    Device A broadcasts a StereoLink beacon over local network (mDNS / UDP broadcast)
    Device B detects the beacon → "Jovial device found nearby: [Device A]"
    User taps "Connect"

Step 2: Pairing & Role Assignment
    Device A becomes the MASTER (left channel, controls playback)
    Device B becomes the SLAVE  (right channel, follows master)
    Both agree on a shared session token via WebSocket handshake

Step 3: Clock Synchronisation
    Master and Slave perform NTP-style clock sync:
      - Master sends T1 (send timestamp)
      - Slave records T2 (receive timestamp), sends T3 (reply timestamp)
      - Master records T4 (reply receive timestamp)
      - Offset = ((T2 - T1) + (T3 - T4)) / 2
    Round-trip latency and clock offset are measured and compensated
    Sync accuracy target: < 20ms

Step 4: Playback Synchronisation
    Master plays ONLY the left audio channel (L channel extracted via Web Audio API)
    Slave plays ONLY the right audio channel (R channel extracted via Web Audio API)
    Master sends periodic "heartbeat" ticks with current track position_ms
    Slave adjusts playback rate by ±0.1% to correct drift without audible glitching

Step 5: Drift Correction (ongoing)
    Every 5 seconds, master broadcasts authoritative position_ms
    Slave compares with local position:
      - Drift < 20ms  → no correction
      - Drift 20–200ms → micro-adjust playback rate
      - Drift > 200ms  → hard seek to correct position (brief mute applied)
```

#### StereoLink Technical Stack

| Component | Technology | Purpose |
|---|---|---|
| Device Discovery | mDNS (Multicast DNS) + UDP broadcast | Find other Jovial devices on LAN |
| Signalling | Socket.io (WebSocket) | Session handshake + control messages |
| Audio Splitting | Web Audio API (ChannelSplitterNode) | Extract L/R channels independently |
| Clock Sync | NTP-inspired algorithm | Sub-20ms offset correction |
| Drift Correction | AudioContext.playbackRate | Smooth micro-adjustments to fix drift |
| Fallback | Web Audio API buffer offset | Hard seek with mute if drift > 200ms |

#### StereoLink Modes

| Mode | Description | Use Case |
|---|---|---|
| 🔊 **True Stereo** | Device A = Left channel, Device B = Right channel | Side-by-side speakers |
| 🔁 **Mirror Mode** | Both devices play full stereo, perfectly synced | Different rooms / louder playback |
| 🔀 **Swap Channels** | Swap which device is L and which is R | Reposition speakers at any time |
| 🔔 **Solo Mode** | Temporarily restore full stereo to one device | If partner steps away |

---

## 🛠 Tech Stack

### Frontend
| Technology | Purpose |
|---|---|
| ⚛ **React 18** | UI component framework |
| ⚡ **Vite** | Lightning-fast dev server and bundler |
| 🎨 **Tailwind CSS** | Utility-first styling |
| 🎞 **Framer Motion** | Swipe animations, player transitions, card physics |
| 🔄 **React Query (TanStack)** | Server state, caching, background refetch |
| 🗃 **Zustand** | Lightweight global state (player state, room state) |
| 🔌 **Socket.io-client** | Real-time WebSocket client |
| 🔊 **Web Audio API** | Channel splitting for StereoLink, visualiser, crossfade |
| 🧭 **React Router v6** | Client-side routing |
| 📝 **React Hook Form + Zod** | Form handling and validation |
| 🧩 **Howler.js** | Cross-browser audio playback engine |

### Backend
| Technology | Purpose |
|---|---|
| 🟢 **Node.js 18** | JavaScript runtime |
| 🚀 **Express.js** | REST API framework |
| 🔧 **TypeScript** | End-to-end type safety |
| 🔌 **Socket.io 4** | Real-time bidirectional WebSocket server |
| 🎫 **jsonwebtoken** | JWT authentication |
| 🔐 **bcrypt** | Password hashing |
| 🎯 **Zod** | Request validation |
| 📧 **Nodemailer** | Email service (invites, OTP) |
| 🌐 **node-mdns / bonjour** | mDNS service for StereoLink device discovery |

### Database & Cache
| Technology | Purpose |
|---|---|
| 🍃 **MongoDB 7** | Primary database — users, tracks, playlists, rooms |
| ⚡ **Redis 7** | Room state, Socket.io adapter, rate limiting, session tokens |
| ☁ **Cloudinary** | Audio file storage and streaming (CDN-backed) |
| 🔍 **MongoDB Atlas Search** | Full-text search across tracks, artists, albums |

### Real-Time & Sync
| Technology | Purpose |
|---|---|
| 🔌 **Socket.io** | Together Mode sync, Room broadcasts, chat, reactions |
| 📡 **WebRTC (Data Channels)** | P2P StereoLink sync on local network (low latency) |
| ⏱ **NTP-style clock sync** | Sub-20ms clock offset correction for StereoLink |
| 🔊 **Web Audio API** | Audio channel splitting, visualiser, playback rate control |

### External APIs
| Service | Purpose |
|---|---|
| 🎵 **Spotify Web API** | Playlist import, track metadata enrichment |
| 📝 **Musixmatch API** | Time-synced lyrics |
| 🎧 **Last.fm API** | Artist bios, similar artists, tags |
| 🔔 **Firebase Cloud Messaging** | Push notifications (Together Mode invites, room alerts) |

### DevOps & Tooling
| Technology | Purpose |
|---|---|
| 🐳 **Docker + Docker Compose** | Containerisation |
| 🔄 **GitHub Actions** | CI/CD pipeline |
| 📊 **Prometheus + Grafana** | Metrics and monitoring |
| 🌐 **Nginx** | Reverse proxy, SSL termination |
| ☁ **AWS EC2 + S3** | Server hosting and static asset CDN |
| 🔒 **Let's Encrypt** | SSL/TLS certificates |

---

## 🏗 Architecture

**Architecture Type:** Modular Monolith (Core API) + Socket.io Real-Time Layer + CDN Audio Streaming

### 🔷 High-Level Architecture

```
┌──────────────────────────────────────────────────────────────────────┐
│                          CLIENT LAYER                                │
│        React 18 + Vite  |  Tailwind CSS  |  Framer Motion           │
│        Howler.js (audio) | Web Audio API | Socket.io-client          │
└──────────────────────────────┬───────────────────────────────────────┘
                               │  HTTPS / WSS (WebSocket)
┌──────────────────────────────▼───────────────────────────────────────┐
│                         NGINX (Reverse Proxy)                        │
│              Rate Limiting | SSL Termination | Load Balance          │
└─────────────────┬────────────────────────────┬───────────────────────┘
                  │ REST                        │ WebSocket (Socket.io)
┌─────────────────▼────────────┐  ┌────────────▼───────────────────────┐
│   Express.js (REST API)      │  │     Socket.io Server               │
│   Auth | Tracks | Playlists  │  │     Together Mode | Rooms          │
│   Users | Library | Search   │  │     StereoLink | Chat | Reactions  │
└─────────────┬────────────────┘  └────────────┬───────────────────────┘
              │                                │
┌─────────────▼────────────────────────────────▼───────────────────────┐
│                       DATA LAYER                                     │
│   MongoDB (persistent)  |  Redis (room state, cache)                 │
│   Cloudinary CDN (audio streaming)                                   │
└──────────────────────────────────────────────────────────────────────┘
                                   │ External APIs
┌──────────────────────────────────▼───────────────────────────────────┐
│  Spotify API  |  Musixmatch API  |  Last.fm  |  Firebase FCM         │
└──────────────────────────────────────────────────────────────────────┘
```

### 🔹 Backend Module Breakdown

```
Express App
    │
    ├── Middleware
    │       ├── JWT Auth Guard
    │       ├── Zod Request Validator
    │       ├── Rate Limiter (Redis)
    │       └── Request Logger
    │
    ├── REST Routes
    │       ├── /api/auth        → AuthController → AuthService
    │       ├── /api/tracks      → TrackController → TrackService → MongoDB + Cloudinary
    │       ├── /api/playlists   → PlaylistController → PlaylistService → MongoDB
    │       ├── /api/rooms       → RoomController → RoomService → Redis + MongoDB
    │       ├── /api/search      → SearchController → MongoDB Atlas Search
    │       └── /api/users       → UserController → UserService → MongoDB
    │
    └── Socket.io Namespaces
            ├── /together        → Together Mode real-time sync
            ├── /room            → Listening Room broadcast + chat
            └── /stereolink      → StereoLink device pairing + clock sync
```

### 📐 Full Request Flow — Together Mode Playback Event

```
1.  User A presses PAUSE on the player
2.  React dispatch → Zustand playerStore.pause()
3.  Socket.io emits: together:pause { sessionId, position_ms, timestamp }
4.  Server receives on /together namespace
5.  Auth middleware validates session membership
6.  RoomService updates Redis: session:{id}:state → { is_playing: false, position_ms }
7.  Server broadcasts to room: together:state_update { is_playing, position_ms, actor: "User A" }
8.  User B's client receives event
9.  Howler.js pause() called with seek(position_ms) to guarantee sync
10. User B's UI updates: pause button active, seek bar frozen at position_ms
11. User B sees "User A paused" toast notification
```

### 📐 StereoLink Sync Request Flow

```
1.  Master plays track at position_ms T
2.  Every 5s: Master emits stereolink:heartbeat { position_ms, clock_ms }
3.  Slave receives heartbeat
4.  Slave calculates drift = (local_position_ms + network_offset) - received_position_ms
5.  If |drift| < 20ms    → No action
6.  If 20ms < drift < 200ms → AudioContext.playbackRate adjusted ±0.1%
7.  If drift > 200ms     → Hard seek + 200ms mute to avoid jarring pop
8.  Slave sends stereolink:ack { slave_position_ms, drift_ms }
9.  Master logs sync health; if repeated large drift → notify user to move devices closer
```

---

## 🔐 Authentication

### Supported Methods

1. **Email / Password** — Traditional auth with bcrypt
2. **Google OAuth 2.0** — Sign in with Google
3. **GitHub OAuth** — Sign in with GitHub
4. **Guest Access** — Join rooms without an account (limited to listener role)

### JWT Token Structure

```json
{
  "userId":    "64a3f2e1c8b97a001f2d5c3e",
  "email":     "user@jovial.music",
  "username":  "soundwave_vibes",
  "role":      "user",
  "iat":       1720000000,
  "exp":       1720604800
}
```

### Token Expiration
- **Access Token:** 7 days
- **Refresh Token:** 30 days (stored in HttpOnly cookie)
- **Room Invite Token:** 24 hours (single-use)
- **StereoLink Session Token:** 4 hours (scoped to device pair)

### Security Features
- Password hashing with bcrypt (12 salt rounds)
- Refresh token rotation on every use
- Token blacklisting on logout via Redis set
- Rate limiting on auth endpoints — 10 requests/minute
- Account lockout after 5 failed attempts (15-minute cooldown)
- Together Mode sessions require mutual consent (both users must accept)

---

## 🗄 Database Schema

### Entity Relationship Overview

```
USERS           ||--o{ PLAYLISTS        : "creates"
USERS           ||--o{ LIKED_SONGS      : "likes"
USERS           ||--o{ LISTENING_ROOMS  : "hosts"
USERS           }o--o{ ROOMS_MEMBERS    : "joins"
TRACKS          }o--o{ PLAYLISTS        : "belongs_to"
LISTENING_ROOMS ||--o{ ROOM_MESSAGES    : "has"
LISTENING_ROOMS ||--o{ SONG_REQUESTS    : "receives"
TOGETHER_SESSIONS||--o{ SESSION_EVENTS  : "logs"
```

### 👤 Collection: users

```javascript
{
  _id:           ObjectId,
  username:      String,           // unique
  email:         String,           // unique
  password_hash: String,
  display_name:  String,
  avatar_url:    String,
  bio:           String,
  preferences: {
    theme:       String,           // "dark" | "light" | "auto"
    audio_quality: String,         // "128" | "256" | "320"
    crossfade_seconds: Number,     // 0–12
    notifications: {
      together_invites: Boolean,
      room_start:       Boolean,
      new_follower:     Boolean,
    }
  },
  stats: {
    total_minutes_listened: Number,
    top_genres:  [String],
    top_artists: [ObjectId],       // ref: artists
  },
  followers:     [ObjectId],       // ref: users
  following:     [ObjectId],       // ref: users
  is_verified:   Boolean,
  last_active:   Date,
  created_at:    Date,
}
```

### 🎵 Collection: tracks

```javascript
{
  _id:           ObjectId,
  title:         String,
  artist:        { _id: ObjectId, name: String },
  album:         { _id: ObjectId, name: String, cover_url: String },
  duration_ms:   Number,
  audio_url:     String,           // Cloudinary CDN URL
  waveform_data: [Number],         // pre-computed amplitude array for visualiser
  genres:        [String],
  mood_tags:     [String],         // "chill", "hype", "sad", "focus"
  bpm:           Number,
  key:           String,
  lyrics_id:     String,           // Musixmatch track ID
  play_count:    Number,
  like_count:    Number,
  release_date:  Date,
  is_explicit:   Boolean,
  created_at:    Date,
}
```

### 📚 Collection: playlists

```javascript
{
  _id:           ObjectId,
  owner_id:      ObjectId,         // ref: users
  name:          String,
  description:   String,
  cover_url:     String,
  tracks:        [{ track_id: ObjectId, added_by: ObjectId, added_at: Date }],
  collaborators: [ObjectId],       // ref: users (can edit)
  privacy:       String,           // "public" | "unlisted" | "private"
  is_smart:      Boolean,
  smart_rules:   Object,           // { genre: "jazz", min_bpm: 100, year: 2022 }
  follower_count: Number,
  created_at:    Date,
  updated_at:    Date,
}
```

### 🏠 Collection: listening_rooms

```javascript
{
  _id:           ObjectId,
  room_code:     String,           // unique 6-char code (e.g. "JOV-7X2")
  name:          String,
  creator_id:    ObjectId,         // ref: users
  co_djs:        [ObjectId],       // ref: users
  privacy:       String,           // "public" | "unlisted" | "private"
  max_listeners: Number,           // default: 50
  current_track: {
    track_id:    ObjectId,
    position_ms: Number,
    is_playing:  Boolean,
    updated_at:  Date,
  },
  queue:         [{ track_id: ObjectId, added_by: ObjectId }],
  settings: {
    allow_requests:   Boolean,
    vote_to_skip:     Boolean,
    audio_quality:    String,
    chat_enabled:     Boolean,
  },
  listener_count: Number,
  play_history:  [{ track_id: ObjectId, played_at: Date }],
  is_active:     Boolean,
  scheduled_for: Date,
  created_at:    Date,
}
```

### 💑 Collection: together_sessions

```javascript
{
  _id:            ObjectId,
  session_token:  String,          // unique short-lived token for joining
  user_a:         ObjectId,        // ref: users (initiator)
  user_b:         ObjectId,        // ref: users (invitee)
  current_track: {
    track_id:     ObjectId,
    position_ms:  Number,
    is_playing:   Boolean,
    updated_at:   Date,
  },
  queue:          [ObjectId],      // ref: tracks
  chat_messages:  [{ user_id: ObjectId, text: String, sent_at: Date }],
  reactions:      [{ user_id: ObjectId, emoji: String, sent_at: Date }],
  is_active:      Boolean,
  started_at:     Date,
  ended_at:       Date,
}
```

### 🔊 Collection: stereolink_sessions

```javascript
{
  _id:              ObjectId,
  session_token:    String,
  master_device: {
    user_id:        ObjectId,
    device_name:    String,
    channel:        String,        // "left"
    ip_address:     String,
    clock_offset_ms: Number,
  },
  slave_device: {
    user_id:        ObjectId,
    device_name:    String,
    channel:        String,        // "right"
    ip_address:     String,
    clock_offset_ms: Number,
  },
  mode:             String,        // "stereo" | "mirror" | "swapped"
  sync_health: {
    avg_drift_ms:   Number,
    last_hard_seek: Date,
    heartbeat_count: Number,
  },
  is_active:        Boolean,
  started_at:       Date,
}
```

---

## 🔌 API Documentation

### Base URL

```
Development:  http://localhost:5000/api
Production:   https://api.jovial.music/api
```

### 🔐 Authentication Endpoints

#### Register
```http
POST /api/auth/register
Content-Type: application/json

{
  "username":   "soundwave_vibes",
  "email":      "user@example.com",
  "password":   "SecurePass123!"
}
```

**Response — 201 Created**
```json
{
  "success": true,
  "data": {
    "token":   "eyJhbGciOiJIUzI1NiIsInR5cCI6IkpXVCJ9...",
    "user": {
      "id":        "64a3f2e1c8b97a001f2d5c3e",
      "username":  "soundwave_vibes",
      "email":     "user@example.com"
    }
  }
}
```

#### Login
```http
POST /api/auth/login
Content-Type: application/json

{
  "email":    "user@example.com",
  "password": "SecurePass123!"
}
```

---

### 🎵 Track Endpoints

#### Get Track by ID
```http
GET /api/tracks/:id
Authorization: Bearer <token>
```

**Response — 200 OK**
```json
{
  "success": true,
  "data": {
    "id":           "64b1a2f3c8b97a001f2d5c5f",
    "title":        "Starboy",
    "artist":       { "id": "...", "name": "The Weeknd" },
    "album":        { "id": "...", "name": "Starboy", "cover_url": "https://..." },
    "duration_ms":  230000,
    "audio_url":    "https://res.cloudinary.com/jovial/...",
    "mood_tags":    ["hype", "confident"],
    "bpm":          186,
    "genres":       ["R&B", "pop"],
    "lyrics_id":    "12345678"
  }
}
```

#### Stream Track
```http
GET /api/tracks/:id/stream
Authorization: Bearer <token>
Range: bytes=0-
```
> Returns audio bytes with `Content-Type: audio/mpeg` and HTTP 206 Partial Content for range-based streaming

#### Search Tracks
```http
GET /api/tracks/search?q=starboy&genre=rnb&mood=hype&bpm_min=150&limit=20&page=1
Authorization: Bearer <token>
```

---

### 🏠 Room Endpoints

#### Create Listening Room
```http
POST /api/rooms
Authorization: Bearer <token>
Content-Type: application/json

{
  "name":            "Friday Night Vibes",
  "privacy":         "public",
  "max_listeners":   30,
  "allow_requests":  true,
  "vote_to_skip":    false
}
```

**Response — 201 Created**
```json
{
  "success": true,
  "data": {
    "room_id":   "64c2d3e4f5a6b7001g3h4i5j",
    "room_code": "JOV-7X2",
    "join_url":  "https://jovial.music/room/JOV-7X2"
  }
}
```

#### Get Room State
```http
GET /api/rooms/:roomCode
Authorization: Bearer <token>
```

#### Submit Song Request
```http
POST /api/rooms/:roomCode/requests
Authorization: Bearer <token>
Content-Type: application/json

{
  "track_id": "64b1a2f3c8b97a001f2d5c5f",
  "message":  "Please play this next! 🙏"
}
```

---

### 💑 Together Mode Endpoints

#### Create Together Session
```http
POST /api/together/create
Authorization: Bearer <token>
```

**Response — 201 Created**
```json
{
  "success": true,
  "data": {
    "session_id":    "64d4e5f6a7b8c001h4i5j6k",
    "session_token": "abc123xyz",
    "join_url":      "https://jovial.music/together/abc123xyz",
    "expires_at":    "2024-07-20T22:00:00Z"
  }
}
```

#### Invite User to Session
```http
POST /api/together/:sessionId/invite
Authorization: Bearer <token>
Content-Type: application/json

{
  "invite_username": "luna_beats"
}
```

---

### 🔊 StereoLink Endpoints

#### Initiate StereoLink Session
```http
POST /api/stereolink/initiate
Authorization: Bearer <token>
Content-Type: application/json

{
  "device_name": "My iPhone 14",
  "role":        "master",
  "channel":     "left"
}
```

**Response — 201 Created**
```json
{
  "success": true,
  "data": {
    "session_token": "stl_7xp2qr9abc",
    "qr_code_url":   "https://api.jovial.music/stereolink/qr/stl_7xp2qr9abc",
    "expires_in":    14400
  }
}
```

#### Join StereoLink Session (Slave Device)
```http
POST /api/stereolink/join
Authorization: Bearer <token>
Content-Type: application/json

{
  "session_token": "stl_7xp2qr9abc",
  "device_name":   "Partner's Samsung S24",
  "channel":       "right"
}
```

---

## 📡 WebSocket & Real-Time Events

### Namespaces

| Namespace | Purpose |
|---|---|
| `/together` | Together Mode (2-person) sync |
| `/room` | Listening Room broadcast, chat, requests |
| `/stereolink` | StereoLink device pairing + heartbeat |

### Together Mode Events

```
Client → Server:
  together:join           { session_token }
  together:play           { session_id, position_ms, timestamp }
  together:pause          { session_id, position_ms }
  together:seek           { session_id, position_ms }
  together:next_track     { session_id }
  together:prev_track     { session_id }
  together:add_to_queue   { session_id, track_id }
  together:reaction       { session_id, emoji }
  together:chat           { session_id, text }

Server → Client:
  together:state_update   { current_track, position_ms, is_playing, actor }
  together:queue_update   { queue }
  together:reaction       { user_id, emoji, timestamp }
  together:chat_message   { user_id, text, timestamp }
  together:partner_joined { user_id, username, avatar_url }
  together:partner_left   { user_id }
  together:session_ended  { reason }
```

### Listening Room Events

```
Client → Server:
  room:join               { room_code, guest_name? }
  room:send_message       { room_code, text }
  room:send_reaction      { room_code, emoji }
  room:song_request       { room_code, track_id, message }
  room:vote_skip          { room_code }

  [DJ/Creator only]
  room:play               { room_code, position_ms }
  room:pause              { room_code, position_ms }
  room:seek               { room_code, position_ms }
  room:next_track         { room_code }
  room:add_to_queue       { room_code, track_id }
  room:accept_request     { room_code, request_id }
  room:reject_request     { room_code, request_id }
  room:grant_codj         { room_code, user_id }
  room:kick_user          { room_code, user_id }

Server → Client:
  room:state_update       { current_track, position_ms, is_playing, dj_id }
  room:listener_joined    { user_id, username, avatar_url, listener_count }
  room:listener_left      { user_id, listener_count }
  room:chat_message       { user_id, username, text, timestamp }
  room:reaction           { user_id, emoji, timestamp }
  room:new_request        { request_id, track, message, requester }
  room:request_accepted   { request_id, track }
  room:request_rejected   { request_id }
  room:vote_skip_update   { votes_count, votes_needed }
  room:kicked             { }
  room:room_closed        { reason }
```

### StereoLink Events

```
Client → Server:
  stereolink:join         { session_token, device_name, channel }
  stereolink:clock_ping   { T1: timestamp_ms }
  stereolink:ack          { position_ms, drift_ms }
  stereolink:mode_change  { mode }       // "stereo" | "mirror" | "swapped"
  stereolink:disconnect   { }

Server → Client:
  stereolink:paired       { master_device, slave_device, mode }
  stereolink:clock_pong   { T1, T2, T3 }
  stereolink:heartbeat    { position_ms, clock_ms, track_id }
  stereolink:sync_warning { avg_drift_ms, recommendation }
  stereolink:disconnected { device_name }
```

---

## 🔊 Device Sync (StereoLink) — Technical Design

### Clock Synchronisation Algorithm

StereoLink uses a 4-message NTP-inspired exchange to compute clock offset between master and slave:

```
Master                     Slave
  │                           │
  │── T1: ping ──────────────►│  (T1 = master send time)
  │                           │  (T2 = slave receive time)
  │◄─ T3: pong ───────────────│  (T3 = slave reply time)
  │  (T4 = master receive)    │
  │                           │
  Offset = ((T2 - T1) + (T3 - T4)) / 2
  Latency = ((T4 - T1) - (T3 - T2)) / 2
```

This exchange repeats 5 times on connect; median offset is used to filter outliers.

### Audio Channel Splitting via Web Audio API

```javascript
// Master device — plays LEFT channel only
const audioCtx     = new AudioContext();
const source       = audioCtx.createMediaElementSource(audioElement);
const splitter     = audioCtx.createChannelSplitter(2);
const merger       = audioCtx.createChannelMerger(2);

source.connect(splitter);
splitter.connect(merger, 0, 0);  // left  → left
splitter.connect(merger, 0, 1);  // left  → right (mono-ify left)
merger.connect(audioCtx.destination);

// Slave device — plays RIGHT channel only
splitter.connect(merger, 1, 0);  // right → left
splitter.connect(merger, 1, 1);  // right → right (mono-ify right)
merger.connect(audioCtx.destination);
```

### Drift Correction Strategy

```
Every 5 seconds:
  Master → Slave: { position_ms: 93450, clock_ms: 1720000093450 }

Slave calculates:
  expected_position = received_position_ms + (local_clock_ms - received_clock_ms + clock_offset)
  actual_position   = audioElement.currentTime * 1000
  drift             = actual_position - expected_position

Correction:
  |drift| < 20ms   → no action (within acceptable range)
  20–200ms         → audioElement.playbackRate = 1.0 + (drift > 0 ? -0.001 : +0.001)
  > 200ms          → audioElement.currentTime = expected_position / 1000
                     (brief 200ms mute applied to mask seek pop)
```

---

## 🔐 Security

### Input Validation
- All API inputs validated with Zod schemas on every route
- File uploads restricted to audio MIME types; size capped at 50MB

### Rate Limiting (Redis-backed)
| Endpoint Group | Limit |
|---|---|
| Auth (login/register) | 10 requests / minute |
| Track streaming | 500 requests / hour |
| Room creation | 5 rooms / day |
| Search | 60 requests / minute |
| StereoLink initiate | 10 sessions / hour |

### Together Mode & Room Security
- Session tokens are single-use UUIDs, expire in 24 hours
- Room invite links are rotatable by the creator at any time
- Socket.io events from non-members are silently dropped
- Room creator can kick users, which revokes their socket session immediately

### Audio Streaming Security
- Cloudinary signed URLs for audio (expire in 1 hour, scoped to user)
- HLS chunked streaming to prevent direct file download
- Referrer validation on CDN to block hotlinking

---

## ⚡ Performance

### Audio Streaming Optimisations
- **HLS (HTTP Live Streaming)** — Tracks segmented into 10-second chunks; client buffers 3 chunks ahead
- **Adaptive bitrate** — Automatically drops from 320 → 256 → 128 kbps on poor network
- **Waveform pre-computation** — Waveform amplitude arrays stored in DB at upload time; never computed on-the-fly
- **Cloudinary CDN** — Audio served from nearest edge node; average latency < 80ms globally

### Real-Time Optimisations
- **Redis as Socket.io adapter** — Enables multi-instance horizontal scaling for rooms
- **Room state in Redis** — Sub-1ms state reads for heartbeat/sync events
- **Event debouncing** — Seek bar drag events debounced at 100ms before emitting
- **Binary heartbeats** — StereoLink heartbeats use compact binary frames (not JSON) for minimal latency

### Caching Strategy
| Data | Cache | TTL |
|---|---|---|
| Track metadata | Redis | 24 hours |
| Search results | Redis | 5 minutes |
| User profile | Redis | 1 hour |
| Trending tracks | Redis | 10 minutes |
| Room state | Redis | Active session only |
| Lyrics | Redis | 7 days |

---

## 🧪 Testing

### Test Coverage

| Layer | Framework | Coverage Target |
|---|---|---|
| Unit (Services) | Jest | ≥ 80% |
| Integration (API) | Supertest + Jest | ≥ 75% |
| Real-time (Socket.io) | socket.io-client mock | ≥ 70% |
| E2E (Full flows) | Playwright | Critical paths |

### Key Test Scenarios

- ✅ Together Mode: both users pause/play/seek in sync
- ✅ Room: creator kick removes user socket within 200ms
- ✅ StereoLink: clock offset < 5ms after 5-round NTP exchange
- ✅ StereoLink: drift correction fires within 100ms of drift detection
- ✅ Auth: token blacklist prevents reuse after logout
- ✅ Streaming: range requests return correct byte ranges

### Run Tests

```bash
# Unit tests
npm run test

# Integration tests
npm run test:integration

# E2E tests
npm run test:e2e

# Coverage report
npm run test:coverage
```

---

## 📋 Prerequisites

- **Node.js** ≥ 18.0.0
- **npm** ≥ 9.0.0
- **MongoDB** ≥ 7.0 (local) or MongoDB Atlas cluster
- **Redis** ≥ 7.0
- **Cloudinary** account (free tier works for development)
- **Musixmatch API key** (for lyrics)
- **Spotify Developer App** (optional, for playlist import)

---

## ⚙ Installation & Setup

### 1. Clone the Repository

```bash
git clone https://github.com/yourorg/jovial.git
cd jovial
```

### 2. Install Dependencies

```bash
# Backend
cd server
npm install

# Frontend
cd ../client
npm install
```

### 3. Configure Environment Variables

```bash
# Copy example env files
cp server/.env.example server/.env
cp client/.env.example client/.env
```

Fill in values as described in the [Environment Variables](#-environment-variables) section.

### 4. Seed the Database (Optional)

```bash
cd server
npm run seed
```

This populates MongoDB with 100 sample tracks, 10 artists, 5 playlists, and 3 demo users.

### 5. Start Development Servers

```bash
# Option A: All at once (requires concurrently)
npm run dev         # from root

# Option B: Separately
cd server && npm run dev    # → http://localhost:5000
cd client && npm run dev    # → http://localhost:3000
```

### 6. Start Redis

```bash
# macOS (Homebrew)
brew services start redis

# Ubuntu
sudo systemctl start redis

# Docker
docker run -d -p 6379:6379 redis:7-alpine
```

---

## 🌍 Environment Variables

### Server (`server/.env`)

```env
# Server
NODE_ENV=development
PORT=5000
CLIENT_URL=http://localhost:3000

# MongoDB
MONGODB_URI=mongodb://localhost:27017/jovial

# Redis
REDIS_URL=redis://localhost:6379

# JWT
JWT_SECRET=your_super_secret_jwt_key
JWT_REFRESH_SECRET=your_refresh_secret_key
JWT_EXPIRES_IN=7d
JWT_REFRESH_EXPIRES_IN=30d

# Cloudinary (Audio Storage & CDN)
CLOUDINARY_CLOUD_NAME=your_cloud_name
CLOUDINARY_API_KEY=your_api_key
CLOUDINARY_API_SECRET=your_api_secret

# OAuth
GOOGLE_CLIENT_ID=your_google_client_id
GOOGLE_CLIENT_SECRET=your_google_client_secret
GITHUB_CLIENT_ID=your_github_client_id
GITHUB_CLIENT_SECRET=your_github_client_secret

# External APIs
MUSIXMATCH_API_KEY=your_musixmatch_key
SPOTIFY_CLIENT_ID=your_spotify_client_id
SPOTIFY_CLIENT_SECRET=your_spotify_client_secret
LASTFM_API_KEY=your_lastfm_api_key

# Firebase (Push Notifications)
FIREBASE_PROJECT_ID=your_firebase_project_id
FIREBASE_PRIVATE_KEY=your_firebase_private_key
FIREBASE_CLIENT_EMAIL=your_firebase_client_email

# Email (Nodemailer)
SMTP_HOST=smtp.gmail.com
SMTP_PORT=587
SMTP_USER=your_email@gmail.com
SMTP_PASS=your_app_password
```

### Client (`client/.env`)

```env
VITE_API_URL=http://localhost:5000/api
VITE_SOCKET_URL=http://localhost:5000
VITE_FIREBASE_API_KEY=your_firebase_api_key
VITE_FIREBASE_APP_ID=your_firebase_app_id
```

---

## 📁 Project Structure

```
jovial/
├── client/                         # React frontend
│   ├── public/
│   ├── src/
│   │   ├── assets/                 # Fonts, icons, images
│   │   ├── components/
│   │   │   ├── player/             # Reel-style player, controls, visualiser
│   │   │   ├── together/           # Together Mode UI, partner avatar, reactions
│   │   │   ├── room/               # Room view, listener list, chat, requests
│   │   │   ├── stereolink/         # StereoLink pairing screen, sync status
│   │   │   ├── library/            # Playlists, liked songs, history
│   │   │   ├── discovery/          # Mood queues, trending, search
│   │   │   └── ui/                 # Shared design system components
│   │   ├── hooks/
│   │   │   ├── usePlayer.ts        # Howler.js + Web Audio API integration
│   │   │   ├── useTogetherSync.ts  # Socket.io Together Mode events
│   │   │   ├── useRoomSync.ts      # Socket.io Room events
│   │   │   └── useStereoLink.ts    # StereoLink pairing + drift correction
│   │   ├── store/
│   │   │   ├── playerStore.ts      # Zustand: playback state
│   │   │   ├── roomStore.ts        # Zustand: room state
│   │   │   └── authStore.ts        # Zustand: user session
│   │   ├── services/               # Axios API client functions
│   │   ├── pages/                  # Route-level page components
│   │   ├── lib/
│   │   │   ├── audioUtils.ts       # Web Audio API helpers, channel splitting
│   │   │   ├── clockSync.ts        # NTP-style offset computation
│   │   │   └── driftCorrector.ts   # Playback rate and seek correction logic
│   │   └── App.tsx
│   ├── package.json
│   └── vite.config.ts
│
├── server/                         # Node.js + Express backend
│   ├── src/
│   │   ├── config/                 # DB, Redis, Cloudinary config
│   │   ├── controllers/            # Route handler functions
│   │   ├── services/               # Business logic
│   │   ├── models/                 # Mongoose schemas
│   │   ├── routes/                 # Express route definitions
│   │   ├── sockets/
│   │   │   ├── together.socket.ts  # Together Mode namespace
│   │   │   ├── room.socket.ts      # Listening Room namespace
│   │   │   └── stereolink.socket.ts# StereoLink namespace
│   │   ├── middleware/             # Auth, rate limiter, validator
│   │   ├── utils/                  # JWT helpers, email templates, etc.
│   │   └── app.ts                  # Express + Socket.io bootstrap
│   ├── tests/
│   ├── package.json
│   └── tsconfig.json
│
├── docker-compose.yml
├── .github/
│   └── workflows/
│       ├── ci.yml
│       └── deploy.yml
└── README.md
```

---

## 🚀 Deployment

### Docker (Recommended)

```bash
# Build and start all services
docker-compose up --build -d
```

```yaml
# docker-compose.yml
version: '3.9'

services:
  server:
    build: ./server
    ports: ["5000:5000"]
    env_file: ./server/.env
    depends_on: [mongodb, redis]

  client:
    build: ./client
    ports: ["3000:3000"]
    env_file: ./client/.env

  mongodb:
    image: mongo:7
    ports: ["27017:27017"]
    volumes:
      - mongo_data:/data/db

  redis:
    image: redis:7-alpine
    ports: ["6379:6379"]
    volumes:
      - redis_data:/data

volumes:
  mongo_data:
  redis_data:
```

### Manual Production Build

```bash
# Build client
cd client && npm run build          # outputs to client/dist/

# Build server
cd server && npm run build          # compiles TypeScript to server/dist/

# Start server
cd server && node dist/app.js
```

### Production Checklist
- [ ] Set `NODE_ENV=production`
- [ ] Configure Nginx reverse proxy with SSL (Let's Encrypt)
- [ ] Use MongoDB Atlas with IP allowlist
- [ ] Use Redis with password auth and TLS
- [ ] Set `Socket.io` cors origin to your client domain only
- [ ] Enable Cloudinary signed uploads in production
- [ ] Configure Firebase FCM credentials

---

## 🔧 Troubleshooting

### StereoLink won't connect
- Ensure **both devices are on the same Wi-Fi network** — StereoLink does not work over mobile data
- Check that your router allows **UDP broadcast** (some mesh routers block this — try disabling AP isolation)
- If QR pairing fails, try entering the 6-digit code manually

### Together Mode desync
- If drift exceeds 200ms repeatedly, try **Resync Now** button (bottom of Together Mode screen)
- Desync usually occurs on weak mobile data — a stable Wi-Fi connection is strongly recommended

### Audio not playing
- Confirm Cloudinary keys are correct and the audio file was successfully uploaded
- Check browser console for CORS errors — ensure `CLIENT_URL` in `.env` matches your client origin exactly
- Verify Redis is running: `redis-cli ping` should return `PONG`

### Rooms not showing real-time updates
- Socket.io requires sticky sessions if running multiple server instances — ensure the Redis adapter is configured
- Check that `VITE_SOCKET_URL` in client `.env` points to the correct backend URL

---

## ❓ FAQ

**Q: Can I use Jovial with more than 2 devices in StereoLink?**  
A: Currently StereoLink supports a single pair (master + slave). Multi-speaker support (3+ devices) is planned for Phase 3 of the roadmap.

**Q: Does Together Mode work over mobile data (not just Wi-Fi)?**  
A: Yes! Together Mode works over the internet via WebSocket — both users just need a stable connection. StereoLink, however, requires the same local network.

**Q: How accurate is the audio sync in StereoLink?**  
A: After NTP clock synchronisation, typical drift is under 5ms. The drift correction system maintains < 20ms during normal playback. Occasional hard seeks may occur on very congested networks.

**Q: Can room guests control playback?**  
A: Only the Room Creator and Co-DJs can control playback. Guests can send song requests, vote to skip (if enabled), and participate in chat.

**Q: Is audio stored on Jovial's servers?**  
A: Audio files are stored on Cloudinary CDN. Serve your own licensed audio — Jovial does not provide a music catalog.

**Q: Can I self-host Jovial?**  
A: Yes! The entire stack runs with Docker Compose. See the [Deployment](#-deployment) section.

---

## 📊 Design Decisions

### Why Socket.io over raw WebSockets?

- Built-in room/namespace management maps directly to Together Sessions and Listening Rooms
- Auto-reconnect and fallback to HTTP long-poll handles mobile network drops gracefully
- Redis adapter enables horizontal scaling across multiple server instances with zero code changes

### Why MongoDB over PostgreSQL?

- Track metadata, playlist tracks, and room queues have deeply nested, variable-length structures that map naturally to documents
- Atlas Search provides full-text search without needing a separate Elasticsearch instance
- Schema flexibility allows fast iteration on track metadata fields during development

### Why Howler.js for audio playback?

- Consistent API across all browsers and formats (MP3, OGG, AAC, HLS)
- Built-in Web Audio API integration for visualiser, crossfade, and channel manipulation
- Sprite support for low-latency sound effects (button clicks, notification sounds)

### Why Redis for room state instead of MongoDB?

- Room state (current position, is_playing, queue) changes potentially hundreds of times per minute during active sessions
- Redis sub-millisecond writes and reads are essential for sync accuracy
- Pub/Sub lets the Socket.io Redis adapter broadcast room events to all server instances instantly

### Why NTP-style sync over WebRTC for StereoLink?

- WebRTC was evaluated but adds connection complexity (ICE, STUN, NAT traversal) that is unnecessary on a local network
- NTP over WebSocket achieves < 5ms offset accuracy — more than sufficient for audio sync on LAN
- WebRTC Data Channels are used as a fallback for sub-LAN scenarios in the roadmap

---

## 🛣 Roadmap

### Phase 1 — Core Release ✅ *(Completed)*
- [x] Reel-style player with full controls
- [x] Audio streaming (Cloudinary HLS)
- [x] Time-synced lyrics (Musixmatch)
- [x] Search, playlists, liked songs, library
- [x] JWT + OAuth (Google, GitHub) authentication

### Phase 2 — Social & Together ✅ *(Completed)*
- [x] Together Mode (2-person sync)
- [x] Listening Rooms (group sessions, DJ control)
- [x] Room chat, reactions, song requests
- [x] Follow system, activity feed
- [x] Listening stats (wrapped-style)

### Phase 3 — StereoLink & Mobile 🚧 *(In Progress)*
- [x] StereoLink dual-device stereo pairing
- [x] NTP clock sync + drift correction
- [ ] StereoLink 3+ device multi-speaker support
- [ ] Native mobile apps (React Native — iOS & Android)
- [ ] Background audio playback with lock-screen controls (mobile)
- [ ] StereoLink Bluetooth fallback (for offline/hotspot scenarios)

### Phase 4 — Discovery & Intelligence 📅 *(Planned)*
- [ ] AI-powered mood detection from listening history
- [ ] BPM-aware smart queues (workout, focus, wind-down)
- [ ] Discover Weekly — personalised weekly playlist
- [ ] Collaborative smart playlists between friends
- [ ] Spotify playlist import + bi-directional sync

### Phase 5 — Creator & Platform 📅 *(Future)*
- [ ] Artist upload portal — independent artists can upload tracks directly
- [ ] Tip/support artists from within the app
- [ ] Public developer API (public room player embeds)
- [ ] StereoLink SDK for third-party apps
- [ ] Desktop app (Electron)

---

## 🤝 Contributing

We welcome contributions from developers, audio engineers, and music lovers!

### How to Contribute

1. **Fork the repository**
   ```bash
   git clone https://github.com/yourorg/jovial.git
   cd jovial
   ```

2. **Create a feature branch**
   ```bash
   git checkout -b feature/your-feature-name
   ```

3. **Make your changes**
   - Write clean, readable code
   - Follow existing code style (ESLint + Prettier configured)
   - Add tests for new features
   - Update documentation as needed

4. **Commit with a conventional message**
   ```bash
   git add .
   git commit -m "feat: add vote-to-skip threshold setting for rooms"
   ```
   **Commit types:** `feat`, `fix`, `docs`, `style`, `refactor`, `test`, `chore`

5. **Push and open a Pull Request**
   ```bash
   git push origin feature/your-feature-name
   ```

### Contribution Guidelines

- **TypeScript everywhere** — No plain `.js` files in `server/src` or `client/src`
- **React:** Functional components with hooks only; no class components
- **Zustand:** Keep store slices small and focused on one domain
- **Socket.io:** Every event emitted from client must have a matching server handler and vice versa
- **Tests:** New Socket.io events require corresponding integration tests with mock client
- **Audio code:** Test StereoLink changes against known drift scenarios in `tests/stereolink/`

### Good First Issues

Look for issues labelled:
- `good first issue`
- `help wanted`
- `sync-bug`
- `ui-polish`
- `documentation`

---

## 👥 Contributors

Thanks to everyone who has helped build Jovial! 🙏

<table>
  <tr>
    <td align="center">
      <img src="https://via.placeholder.com/100" width="100px;" alt=""/><br />
      <sub><b>Your Name</b></sub><br />
      <small>Creator & Maintainer</small>
    </td>
  </tr>
</table>

Want to see your name here? [Contribute to Jovial!](#-contributing)

---

## 📄 License

This project is licensed under the **MIT License** — see the [LICENSE](LICENSE) file for full details.

```
MIT License

Copyright (c) 2024 Jovial Team

Permission is hereby granted, free of charge, to any person obtaining a copy
of this software and associated documentation files (the "Software"), to deal
in the Software without restriction, including without limitation the rights
to use, copy, modify, merge, publish, distribute, sublicense, and/or sell
copies of the Software, and to permit persons to whom the Software is
provided to do so, subject to the following conditions:

The above copyright notice and this permission notice shall be included in all
copies or substantial portions of the Software.

THE SOFTWARE IS PROVIDED "AS IS", WITHOUT WARRANTY OF ANY KIND, EXPRESS OR
IMPLIED, INCLUDING BUT NOT LIMITED TO THE WARRANTIES OF MERCHANTABILITY,
FITNESS FOR A PARTICULAR PURPOSE AND NONINFRINGEMENT.
```

---

## 📬 Contact

### Get in Touch

- **Email:** [hello@jovial.music](mailto:hello@jovial.music)
- **GitHub:** [@yourorg](https://github.com/yourorg)
- **Twitter:** [@jovialmusic](https://twitter.com/jovialmusic)
- **LinkedIn:** [Jovial](https://linkedin.com/company/jovial)
- **Discord:** [Join our server](https://discord.gg/jovial)

### Project Links

- **Live Demo:** https://jovial-app.vercel.app
- **Repository:** https://github.com/yourorg/jovial
- **Issue Tracker:** https://github.com/yourorg/jovial/issues
- **Roadmap:** https://github.com/yourorg/jovial/projects

---

## 🌟 Star History

[![Star History Chart](https://api.star-history.com/svg?repos=yourorg/jovial&type=Date)](https://star-history.com/#yourorg/jovial&Date)

---

## 🎯 Final Words

**Jovial** was built out of the belief that music is one of the most powerful ways humans connect with each other — and that streaming platforms have left that connection on the table for too long.

Whether you're:
- 💑 A couple who wants to fall asleep to the same song from separate cities
- 👨‍👩‍👧‍👦 A group of friends hosting a virtual music night where everyone actually gets a say
- 🔊 Someone who wants their two phones to fill the room with real stereo sound
- 🎧 A solo listener who just loves the feel of swiping through music like a feed

**Jovial is built for you.**

> *"Music gives a soul to the universe, wings to the mind, flight to the imagination, and life to everything."*  
> — Plato

---

<div align="center">

### Music is better together. 🎵❤️

**Give us a ⭐ if Jovial made your listening experience more alive!**

[Report Bug](https://github.com/yourorg/jovial/issues) · [Request Feature](https://github.com/yourorg/jovial/issues) · [Join Discord](https://discord.gg/jovial)

</div>

---

<div align="center">
  <sub>Made with ❤️ and 🎵 by the Jovial Team</sub>
</div>