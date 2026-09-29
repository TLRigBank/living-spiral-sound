# Living Spiral Sound

Sound and music library for developing tracks and albums inside Living Spiral Systems.

This repo is the **chart, catalog, and production desk**.
Raw audio lives beside it (Git LFS, GitHub Releases, or local/Drive), not as unbounded blobs on `main`.

**Repo:** https://github.com/TLRigBank/living-spiral-sound

## What lives here

| Layer | Path | Job |
|---|---|---|
| Catalog | `CATALOG.md` | Index of sessions, tracks, albums |
| Sessions | `sessions/` | Source takes, measurements, cells |
| Albums | `albums/` | Track cards, arrangement maps, release notes |
| Library | `library/` | Pointers for sources, loops, stems, masters |
| Instruments | `instruments/` | Tuning and scale notes per instrument |
| Docs | `docs/` | Recording spec, workflow, album pipeline |
| Templates | `templates/` | Copy these to start a session, track, or album |

## First working set (2026-09-28)

Source session: [`sessions/2026-09-28-hadpan1/`](sessions/2026-09-28-hadpan1/SESSION.md)

EP 01 — *Wave Count*

1. [Still Point](albums/ep-01-wave-count/tracks/still-point.md) — 46 BPM half-time, healing / long-form
2. [Wave Count](albums/ep-01-wave-count/tracks/wave-count.md) — 93 BPM album cut
3. [Desert Canon](albums/ep-01-wave-count/tracks/desert-canon.md) — 45–60s loopable social cut

Core language of the take: **D–A–E hover** on a D Kurd handpan. Pulse **92–94 BPM** (half-time 46). Tuning on this file ~A4 442–444 Hz, slightly sharp of 440 — mix *to the pan*.

## How to add work

1. Copy `templates/session.md` into `sessions/YYYY-MM-DD-slug/`.
2. Measure the take (tempo, tuning, cells, form).
3. Open or extend an album folder from `templates/album.md`.
4. One card per track from `templates/track.md`.
5. Point `library/` READMEs at the actual audio (Release tag, LFS path, or Drive).
6. Update `CATALOG.md` in the same commit.

Full steps: [`docs/WORKFLOW.md`](docs/WORKFLOW.md)

## Audio rule

Do **not** commit large masters to `main` as normal git objects.

- Preview loops under ~5 MB may use Git LFS (see `.gitattributes`).
- Session masters and stems go in a dated GitHub Release or local `audio/` (gitignored) plus a catalog pointer.
- Always keep the text chart in git even if the audio lives elsewhere.

## Sister systems

- `TLRigBank/living-spiral-systems` — Spine / Shell / cycles
- Eden Weaver / RAF — regenerative framing for the work, not decoration on the mix

## License

- Text, charts, and production notes: MIT (see `LICENSE`)
- Sound recordings: all rights reserved until a track card sets a release license
