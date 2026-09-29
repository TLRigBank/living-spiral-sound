# Workflow

Council desk for turning a take into catalogued tracks.

## 1. Ingest a session

1. Name it `sessions/YYYY-MM-DD-slug/`.
2. Fill `SESSION.md` from `templates/session.md`.
3. Store the source filename, duration, mono/stereo, bit depth if known.
4. Do **not** require the audio to live in git. Add a pointer: local path, Drive, or Release tag.

## 2. Measure

Capture at least:

- Pulse (BPM cluster + half-time)
- Tuning vs A440 and vs any claimed 432 target
- Notes actually played vs notes available on the instrument
- 2–3 motif cells
- Form as waves / breaths / drops, with clock times
- Recording faults (clip, mono, room slap)

## 3. Decide products

One take can feed more than one track. Default split when the form already has waves:

- long / still version (half-time)
- album version (measured pulse)
- short canon / social version (one cell, hard stop)

## 4. Write track cards

One file per track. Arrangement map, source loops, what *not* to add.

## 5. Place audio

| Kind | Where |
|---|---|
| Phone/field source | `library/sources/` pointer |
| Working loops | `library/loops/` pointer or LFS |
| Stems | `library/stems/` |
| Mix / master | `library/masters/` + album `releases/` note |

## 6. Close the catalog

Update `CATALOG.md` in the same commit. If nothing is ready to ship, status stays `development`.
