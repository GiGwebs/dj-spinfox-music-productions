# AI Handover — DJ Spinfox Music Productions

## Objective

Create a Git-based coordination hub that manages DJ Spinfox's music releases from creation (Suno AI, DJ mixes) through publication (TuneCore) to publicity (social media).

## Scope and approvals

- **In scope:** Release metadata tracking, asset linking, publication checklists, social-marketing generation, and automation scripts.
- **Out of scope (for now):** Storing audio/artwork in Git, direct TuneCore upload API (does not exist), and live social-media posting.
- **Asset boundary:** Audio and images remain in Dropbox / on hosting platforms. This repo holds links and metadata only.

## Accepted decisions

- Repo name: `dj-spinfox-music-productions`
- Platform: GitHub public repo under `GiGwebs`
- Local clone: `/Users/gigwebs/Library/CloudStorage/Dropbox/Projects/dj-spinfox-music-productions`
- Dropbox asset sources:
  - Suno AI creations: `Dropbox/MUSIC BANK/Music Production/DJ SPINFOX Music - Creation, Publication & Publicity/SUNO AI creations/`
  - DJ mixes: `Dropbox/Projects/DJ SPINFOX/DJ Mixes/`
- Related code: `GiGwebs/suno-lyrics-generator`

## Current state

- GitHub repo created and cloned.
- Initial skeleton files added: `README.md`, `CONTEXT.md`, `AI_HANDOVER.md`, `.gitignore`.
- Empty directories created: `releases/`, `scripts/`, `docs/`, `socials/`, `assets/`.

## Blockers / constraints

- TuneCore has no public API for distribution uploads. Human/assisted submission remains required.
- Suno AI API exists but requires a separate subscription and key; integration to be decided.

## Next steps

1. Add a sample release record in `releases/`.
2. Add a release template and validation script under `docs/` and `scripts/`.
3. Decide first social platforms and marketing format.
4. Link this repo to the existing `suno-lyrics-generator` workflow.

## Source pointers

- GitHub: https://github.com/GiGwebs/dj-spinfox-music-productions
- Suno lyric generator: https://github.com/GiGwebs/suno-lyrics-generator
- Suno AI assets: `Dropbox/MUSIC BANK/Music Production/DJ SPINFOX Music - Creation, Publication & Publicity/SUNO AI creations/`
- DJ mixes: `Dropbox/Projects/DJ SPINFOX/DJ Mixes/`
