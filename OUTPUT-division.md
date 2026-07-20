# ➗ Generated Media — "Sharing With Freddy" (Division Intro)

Claymotion division intro for a 5-year-old: **division = sharing berries fairly
between friends**. Freddy shares berries so each friend gets an equal share.
~50s, 5 clips, silent/ambient (overlay the Suno track).

Built with the locked-cast, still-first workflow (see `CLAUDE.md`).
Style: **Claymotion**. Anchored to the series Freddy (`7e5a1860`).
Cast: Freddy (green frog) shares with the **blue snail** + **teal dragonfly**.

## 🎬 FINAL assembled video (~50s, 1280×720)

**▶️ https://d8j0ntlcm91z4.cloudfront.net/user_3FGVsNrxRrv3NuW3XlCmrTwRKNU/hf_20260720_134345_319bef58-96e9-4edd-aed7-2af48d622427.mp4**

5 clips × 10s, in play order. Assembly job `319bef58-96e9-4edd-aed7-2af48d622427`.
(v7 — clips 2/3/4 now animate the HAND-OUT: Freddy starts with the berries in his
basket and gives them out to the two friends. Animated with gemini from start
frames anchored to clip 1, so the pond background + colours stay consistent.)

## 🎞️ The 5 clips (play order)

Base: `https://d8j0ntlcm91z4.cloudfront.net/user_3FGVsNrxRrv3NuW3XlCmrTwRKNU/`

| # | Beat | Math | Clip file | Job id | From start still |
|---|------|------|-----------|--------|-----------|
| 1 | Hook — Freddy + 2 friends, basket w/ 2 berries | — | `hf_20260719_222654_c6c4ff1d-96e4-4ed8-a9d5-c4f5bea45ae0.mp4` | c6c4ff1d | 41c67cc9 |
| 2 | Freddy hands out 2 berries, 1 each | 2 ÷ 2 = 1 | `hf_20260720_103709_e6494276-4072-48e5-902d-6616f9e27e24.mp4` | e6494276 | 6b3ca861 |
| 3 | Freddy hands out 4 berries, 2 each | 4 ÷ 2 = 2 | `hf_20260720_..._56cc5e41-c91d-4a4b-a447-d3cf43010a63.mp4` | 56cc5e41 | 4ebb119d |
| 4 | Freddy hands out 6 berries, 3 each | 6 ÷ 2 = 3 | `hf_20260720_103716_d5b7d0e7-8752-4ea6-b0ad-e96c87029bb7.mp4` | d5b7d0e7 | 2802bef1 |
| 5 | Finale — 2 friends cheer w/ equal shares | — | `hf_20260719_232844_2866c7ab-0bb9-472a-8904-1b1d4ca46594.mp4` | 2866c7ab | 0d678945 |

**How the clips were made (v7, final):** every clip is `gemini_omni` single-frame
animation from an approved still (locks Freddy's colour + the background, stitches
natively). Clips 2/3/4 animate from a START frame (basket holding the berries,
friends empty-handed, anchored to clip 1) so Freddy hands the berries out during
the clip. Earlier still-motion versions (end-state only) are `ce1b5fa7 / e5c09ab5
/ 16013d9f`; the seedance start→end hand-out was abandoned (colour/background
drift, berry duplication, and couldn't stitch without a re-encode).

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
