# ➗ Generated Media — "Sharing With Freddy" (Division Intro)

Claymotion division intro for a 5-year-old: **division = sharing berries fairly
between friends**. Freddy starts with a basket of berries and hands them out so
each friend gets an equal share. ~50s, 5 clips.

Built with the locked-cast, still-first workflow (see `CLAUDE.md`).
Style: **Claymotion**. Anchored to the series Freddy (`7e5a1860`) so he matches
the counting + multiplication videos.

- **Division reference sheet:** `6eb77916-f6ff-470f-aca1-21d7223ebdeb`
  (Freddy + berries, anchored to the series Freddy).
- Cast used: Freddy (green frog) shares among the **blue snail** + **teal
  dragonfly** (÷2 clips); the finale adds the **green turtle**.
- Clips are **silent / ambient** — overlay the Suno track
  (`suno-prompt-division.md`) for a sung version.

Base URL: `https://d8j0ntlcm91z4.cloudfront.net/user_3FGVsNrxRrv3NuW3XlCmrTwRKNU/`

## 🎞️ Final clips (play order) — the sharing story

| # | Beat | Math | Clip file | Job id |
|---|------|------|-----------|--------|
| 1 | Hook — Freddy + 2 friends, full basket | — | `hf_20260718_235004_62749bfd-c2e2-44f5-acd2-1a7e81d6a72d.mp4` | 62749bfd |
| 2 | Share between 2 friends → 1 each | 2 ÷ 2 = 1 | `hf_20260718_235009_ca6db1a7-7554-424e-8870-bee4ebc95a21.mp4` | ca6db1a7 |
| 3 | Share between 2 friends → 2 each | 4 ÷ 2 = 2 | `hf_20260718_235013_584464fd-e6c0-408a-9d68-27cb9c49bfe8.mp4` | 584464fd |
| 4 | Share between 2 friends → 3 each | 6 ÷ 2 = 3 | `hf_20260718_230534_2a12455e-d77b-4ddc-8370-d98201651a08.mp4` | 2a12455e |
| 5 | Finale — friends cheer w/ equal shares | — | `hf_20260718_230547_f060fd45-f994-4840-b0f6-4cc19d19ec47.mp4` | f060fd45 |

**How the clips were made**
- Hook + finale: `gemini_omni` single-frame animation from approved stills.
- The 3 sharing clips: `seedance_2_0` **start→end interpolation** — the START
  still shows the basket holding exactly N berries with friends empty-handed;
  the END still shows the basket empty with each friend's equal share. Seedance
  animates the hand-out in between, so both counts stay locked to approved stills.

## 🧩 Stitch-ready (re-encoded) versions of the sharing clips
`explainer_video` can't ingest raw seedance clips (codec/container mismatch —
a stitch containing one hangs; an all-gemini stitch completes in ~45s). Fix:
re-encode the 3 seedance clips through a topaz pass, which makes them stitchable.

| Sharing clip | Raw (seedance) | Re-encoded (stitch-ready) |
|---|---|---|
| 2 ÷ 2 = 1 | ca6db1a7 | `f9f53ce8-b190-4535-b80b-c507fa738b4e` |
| 4 ÷ 2 = 2 | 584464fd | `8717da60-8844-41a8-aaf7-2fdbdcc669dc` |
| 6 ÷ 2 = 3 | 2a12455e | `62e15cb9-2ff0-41b4-8e17-c6e69e4771d2` |

**Final assembly command (once Higgsfield backend is healthy):**
```
explainer_video(width:1280, height:720, items:[
  62749bfd (hook),
  f9f53ce8 (2÷2 re-enc),
  8717da60 (4÷2 re-enc),
  62e15cb9 (6÷2 re-enc),
  f060fd45 (finale)
])
```
Verified working: a 2-clip test [hook + f9f53ce8] stitched in ~60s.

## ⚠️ Final stitch status
As of the last session the final 5-clip stitch was **blocked by a prolonged
Higgsfield backend outage** — assembly jobs hung for hours and new submissions
returned HTTP 429 (job quota saturated by the hung jobs). All 5 clips are
rendered and the re-encodes are done; only the free `explainer_video` join
remains. **Re-run the assembly command above when the backend recovers.**

## Locked reference stills (verified)
Reference sheet `6eb77916`. Sharing-clip keyframes:
- 2÷2: start `d5a45a4f`, end `28d77e12` (v2) → empty-basket end `e1599641` (v4)
- 4÷2: start `1d283d58`, end `76b19889`
- 6÷2: start `d183513e`, end `f6c40cdc`
- Hook still `32a7a140` (2 friends); finale still `7ca8f529` (3 friends).
