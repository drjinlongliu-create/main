# ➗ Generated Media — "Sharing With Freddy" (Division Intro)

Claymotion division intro for a 5-year-old: **division = sharing berries fairly
between friends**. Freddy shares berries so each friend gets an equal share.
~50s, 5 clips, silent/ambient (overlay the Suno track).

Built with the locked-cast, still-first workflow (see `CLAUDE.md`).
Style: **Claymotion**. Anchored to the series Freddy (`7e5a1860`).
Cast: Freddy (green frog) shares with the **blue snail** + **teal dragonfly**.

## 🎬 FINAL assembled video (~50s, 1280×720)

**▶️ https://d8j0ntlcm91z4.cloudfront.net/user_3FGVsNrxRrv3NuW3XlCmrTwRKNU/hf_20260720_062833_90cf0aa0-9427-40d7-a912-3f1fd0031235.mp4**

5 clips × 10s, in play order. Assembly job `90cf0aa0-9427-40d7-a912-3f1fd0031235`.
(v6 — clips 2–5 re-animated from background-matched stills anchored to clip 1, so
the pond background and character colours stay consistent across all clips.)

## 🎞️ The 5 clips (play order)

Base: `https://d8j0ntlcm91z4.cloudfront.net/user_3FGVsNrxRrv3NuW3XlCmrTwRKNU/`

| # | Beat | Math | Clip file | Job id | From still |
|---|------|------|-----------|--------|-----------|
| 1 | Hook — Freddy + 2 friends, basket w/ 2 berries | — | `hf_20260719_222654_c6c4ff1d-96e4-4ed8-a9d5-c4f5bea45ae0.mp4` | c6c4ff1d | 41c67cc9 |
| 2 | Share between 2 friends → 1 each | 2 ÷ 2 = 1 | `hf_20260719_232833_ce1b5fa7-9846-4a79-9c77-3c1ab3ca334d.mp4` | ce1b5fa7 | 0fd4c215 |
| 3 | Share between 2 friends → 2 each | 4 ÷ 2 = 2 | `hf_20260719_232837_e5c09ab5-2741-4baa-8c26-f8539dbe9314.mp4` | e5c09ab5 | 2e17ecec |
| 4 | Share between 2 friends → 3 each | 6 ÷ 2 = 3 | `hf_20260719_232840_16013d9f-fe16-4735-ad2d-804d0489bcac.mp4` | 16013d9f | 03eaa92a |
| 5 | Finale — 2 friends cheer w/ equal shares | — | `hf_20260719_232844_2866c7ab-0bb9-472a-8904-1b1d4ca46594.mp4` | 2866c7ab | 0d678945 |

(Clips 2–5 stills 0fd4c215 / 2e17ecec / 03eaa92a / 0d678945 were re-generated
anchored to clip-1 still 41c67cc9 to keep the background + colours identical.)

**How the clips were made (v5, final):** every clip is `gemini_omni` single-frame
still-motion from an approved still. This locks Freddy's colour, the background,
and exact berry counts (no drift, no duplication) and stitches natively — the
approach we landed on after the seedance hand-out clips kept drifting AND
couldn't be stitched without a re-encode.

## Locked reference stills (verified)
Reference sheet `6eb77916`. Clip stills:
- Hook `41c67cc9` (Freddy + basket w/ exactly 2 berries + snail + dragonfly)
- 2÷2 `e1599641` (empty basket, each friend 1 berry, eq "2 ÷ 2 = 1")
- 4÷2 `76b19889` (each friend 2 berries, eq "4 ÷ 2 = 2")
- 6÷2 `f6c40cdc` (each friend 3 berries, eq "6 ÷ 2 = 3")
- Finale `bc1a7a7e` (Freddy cheering + snail + dragonfly, each 3 berries, confetti)

## Audio
Clips are silent/ambient by design. Overlay the Suno track from
`suno-prompt-division.md` in any editor for the sung version.

## Notes / lessons this build added
- `explainer_video` **cannot ingest raw seedance_2_0 clips** (a stitch
  containing one hangs; all-gemini stitches in seconds). If you must stitch
  seedance output, re-encode it first (topaz upscale pass).
- `gemini_omni` needs the prompt INSIDE `params` (empty prompt → the job fails).
- A prolonged Higgsfield backend outage hung early stitch jobs and saturated the
  video-job quota (HTTP 429); the final all-gemini render/stitch went through
  once the quota freed.

## To re-stitch / extend
`explainer_video(width:1280, height:720, items:[c6c4ff1d, e2c75872, 8a63242d,
8e678ad7, bca9861f])`. Extend (8÷2=4, 9÷3=3, 10÷2=5): make a finished-share
still (empty basket, each friend's equal pile + equation), animate with
`gemini_omni`, add its clip id to the ordered list.
