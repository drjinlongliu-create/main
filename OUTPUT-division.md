# ➗ Generated Media — "Sharing With Freddy" (Division Intro)

Claymotion division intro for a 5-year-old: **division = sharing berries fairly
between friends**. Freddy shares berries so each friend gets an equal share.
~50s, 5 clips, silent/ambient (overlay the Suno track).

Built with the locked-cast, still-first workflow (see `CLAUDE.md`).
Style: **Claymotion**. Anchored to the series Freddy (`7e5a1860`).
Cast: Freddy (green frog) shares with the **blue snail** + **teal dragonfly**.

## 🎬 FINAL video — status

**v8 (locked-count hand-out) is the latest.** All 5 v8 clips below are rendered
and final (verified `completed`). The one remaining step is the single stitched
MP4: the *free* `explainer_video` assembly is stuck in a prolonged Higgsfield
backend jam — two queued jobs (`288b78e9…`, `110e2ac6…`) have sat `in_progress`
for hours. Two ways to get the finished cut **now**:

- **Drop the 5 v8 clip links (table below) straight into your editor** with the
  Suno track — that's the same final assembly you'd do for the audio anyway, so
  there's no need to wait on Higgsfield.
- Or use the **v7 stitched cut** as a ready-made fallback (identical structure;
  the only v8 improvement is clips 3 & 4 now frame-lock the counts):
  ▶️ https://d8j0ntlcm91z4.cloudfront.net/user_3FGVsNrxRrv3NuW3XlCmrTwRKNU/hf_20260720_134345_319bef58-96e9-4edd-aed7-2af48d622427.mp4

Once the backend frees up, re-running the stitch (command at the bottom) yields
the v8 MP4.

## 🎞️ The 5 clips (play order)

Base: `https://d8j0ntlcm91z4.cloudfront.net/user_3FGVsNrxRrv3NuW3XlCmrTwRKNU/`

| # | Beat | Math | Clip file | Job id | From start still |
|---|------|------|-----------|--------|-----------|
| 1 | Hook — Freddy + 2 friends, basket w/ 2 berries | — | `hf_20260719_222654_c6c4ff1d-96e4-4ed8-a9d5-c4f5bea45ae0.mp4` | c6c4ff1d | 41c67cc9 |
| 2 | Freddy hands out 2 berries, 1 each | 2 ÷ 2 = 1 | `hf_20260720_103709_e6494276-4072-48e5-902d-6616f9e27e24.mp4` | e6494276 | 6b3ca861 |
| 3 | Freddy hands out 4 berries, 2 each | 4 ÷ 2 = 2 | `hf_20260720_135636_2554a62f-1866-46ca-80b1-68a118005cb6.mp4` | 2554a62f | 4ebb119d→2e17ecec |
| 4 | Freddy hands out 6 berries, 3 each | 6 ÷ 2 = 3 | `hf_20260720_135638_fc6fddbb-124a-46fb-a448-6cad9bf2a192.mp4` | fc6fddbb | 2802bef1→03eaa92a |
| 5 | Finale — 2 friends cheer w/ equal shares | — | `hf_20260719_232844_2866c7ab-0bb9-472a-8904-1b1d4ca46594.mp4` | 2866c7ab | 0d678945 |

**How the clips were made (v8, final):** hook (`c6c4ff1d`) + finale (`2866c7ab`)
are `gemini_omni` single-frame animation from approved stills (locks Freddy's
colour + pond background). Clip 2 (`e6494276`) is also gemini — its count was
never flagged. Clips 3 & 4 use `seedance_2_0` start→end interpolation so the END
frame **frame-locks each friend's exact share** — this fixed the berry
duplication gemini produced when handing out (snail got handed 3, then 5). The
two seedance clips are then topaz re-encoded (`2554a62f` / `fc6fddbb`) so
`explainer_video` can ingest them (raw seedance clips hang the stitch). Earlier
all-gemini end-state versions are `ce1b5fa7 / e5c09ab5 / 16013d9f`.

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
**v8 stitch order:** `explainer_video(width:1280, height:720, items:[c6c4ff1d,
e6494276, 2554a62f, fc6fddbb, 2866c7ab])` (hook, 2÷2 gemini, 4÷2 re-enc, 6÷2
re-enc, finale). Extend (8÷2=4, 9÷3=3, 10÷2=5): make a finished-share
still (empty basket, each friend's equal pile + equation), animate with
`gemini_omni`, add its clip id to the ordered list.
