# DJ Spinfox Music Productions

Coordination hub for DJ Spinfox music creation, publication, and publicity across Suno AI, Dropbox, TuneCore, and social media.

## What this repo is

This is the central source of truth for the DJ Spinfox release workflow. It does **not** store audio files or artwork directly — those stay in Dropbox and on the hosting platforms. Instead, this repo tracks:

- Release metadata (title, type, status, ISRC/UPC, platform links)
- Links to source assets (Suno AI, Dropbox DJ mixes, local masters)
- TuneCore publication status and checklist
- Social-media marketing copy and schedule
- Automation scripts for repeatable tasks

## What lives outside this repo

| Content                    | Location                                                                            | Why                                |
| -------------------------- | ----------------------------------------------------------------------------------- | ---------------------------------- |
| Suno AI source tracks      | [suno.ai](https://suno.ai) / Suno account                                           | Hosted platform                    |
| AI lyric generation app    | [`GiGwebs/suno-lyrics-generator`](https://github.com/GiGwebs/suno-lyrics-generator) | Separate codebase                  |
| DJ mixes / edits           | `Dropbox/MUSIC BANK/Music Production/` and `Dropbox/Projects/DJ SPINFOX/DJ Mixes/`  | Large audio files, keep in Dropbox |
| Final masters for TuneCore | `Dropbox/.../SUNO AI creations/` or local Mac folder                                | Distribution-ready files           |

## Important constraint

**TuneCore does not expose a public API for uploads.** Full end-to-end upload automation is not currently possible. The repo therefore automates _preparation, metadata, and marketing_, with human/assisted submission into TuneCore.

## Repo structure

```
.
├── AI_HANDOVER.md          # Current project state and next action
├── CONTEXT.md              # Domain model and terminology
├── README.md               # This file
├── .gitignore              # Keep audio, secrets, and caches out of Git
├── releases/               # One file per track or release
│   └── YYYY-MM-title.yaml
├── scripts/                # Automation helpers
├── docs/                   # Process documentation
├── socials/                # Post copy, templates, schedules
└── assets/                 # Links/manifests to external assets only
```

## Quick start

1. Add a new release under `releases/` using the template in `docs/release-template.yaml`.
2. Run validation: `python3 scripts/validate_releases.py` (when available).
3. Generate social copy from a release record: `python3 scripts/generate_socials.py releases/YYYY-MM-title.yaml` (when available).

## Related projects

- [`suno-lyrics-generator`](https://github.com/GiGwebs/suno-lyrics-generator) — AI lyric generation for Suno tracks
