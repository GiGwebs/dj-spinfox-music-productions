# Domain context — DJ Spinfox Music Productions

## Core entities

### Track

A single piece of music created by DJ Spinfox.

- `title` — track title
- `type` — `suno-ai` | `dj-mix` | `edit` | `mashup`
- `status` — `idea` | `in-production` | `ready-for-release` | `submitted` | `published` | `archived`
- `source_url` — link to Suno AI track, Dropbox file path, or local path
- `master_file` — path to distribution-ready master (WAV/MP3/FLAC)
- `cover_art` — path to cover image
- `lyrics` — lyrics text or link to lyric file
- `genre` / `mood` / `bpm` / `key`
- `created_at` / `released_at`

### Release

A publication event on TuneCore (and optionally other platforms).

- `release_title` — may differ from track title for compilations
- `upc` / `isrc`
- `release_date`
- `tunecore_status` — `not-started` | `draft` | `submitted` | `approved` | `live`
- `tracks` — list of Track references
- `territories` / `distribution_channels`

### Asset

A file or link used by a Track or Release.

- `type` — `audio-master` | `cover-art` | `lyrics` | `promo-video` | `stems`
- `location` — Dropbox path, Suno URL, local path
- `checksum` / `size` — for verification (optional)

### Platform

A destination where music is hosted or distributed.

- `tunecore` — digital distribution
- `suno` — AI track hosting / creation
- `dropbox` — file storage for masters and mixes
- `socials` — Instagram, TikTok, YouTube, etc.

### Campaign

A marketing push for a Release.

- `platforms` — which social channels
- `posts` — copy and media references
- `schedule`
- `status`

## Key terminology

- **Suno AI track** — AI-assisted song generated on Suno AI.
- **DJ mix** — mixed set or standalone DJ mix, typically stored in `Dropbox/Projects/DJ SPINFOX/DJ Mixes/`.
- **Edit** — short intro/outro/chop edit of an existing song (e.g., files under `SPINFOX EDITS`).
- **Master** — final distribution-ready audio file.
- **UPC** — Universal Product Code for a release.
- **ISRC** — International Standard Recording Code for a track.
