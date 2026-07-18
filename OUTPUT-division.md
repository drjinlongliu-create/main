# ➗ Generated Media — "Sharing With Freddy" (Division Intro)

Claymotion division intro for a 5-year-old: Freddy the clay frog shares a
basket of berries **equally** onto lily-pad "plates" to teach **division as
fair sharing** (~50s, 5 clips). The mirror of the 2× multiplication video —
here a total is *split* into equal groups instead of *built* up.

Built with the locked-cast, still-first workflow (see `CLAUDE.md`).
Style: **Claymotion** (`1de0f39e-…`). Anchored to the series Freddy
(`7e5a1860`) so he matches the counting + multiplication videos.

- **Division reference sheet:** `6eb77916-f6ff-470f-aca1-21d7223ebdeb`
  (Freddy + lily-pad plate + berries, anchored to the series Freddy).
- Clips are **silent / ambient** — overlay the Suno track
  (`suno-prompt-division.md`) for a sung version.

## 🎬 Final assembled video (~50s, 1280×720)

**▶️ https://d8j0ntlcm91z4.cloudfront.net/user_3FGVsNrxRrv3NuW3XlCmrTwRKNU/hf_20260718_224538_b03f3138-70b7-41d1-b671-6364c24749ea.mp4**

5 clips × 10s, in play order. Also in your Higgsfield Generations.
Assembly job: `b03f3138-70b7-41d1-b671-6364c24749ea`.

## 🎞️ The 5 clips (play order)

Base: `https://d8j0ntlcm91z4.cloudfront.net/user_3FGVsNrxRrv3NuW3XlCmrTwRKNU/`

| # | Beat | Clip file | Job id | From still |
|---|------|-----------|--------|-----------|
| 1 | Hook (basket + 2 empty pads) | `hf_20260718_224347_f6a87555-d22d-4247-bdc0-824e4d47d1c1.mp4` | f6a87555 | 53d05ddf |
| 2 | 2 ÷ 2 = 1 | `hf_20260718_224416_4e27bb5c-7a11-4722-856b-29e6a205b989.mp4` | 4e27bb5c | 2af409f4 |
| 3 | 4 ÷ 2 = 2 | `hf_20260718_224417_9277ef5e-fb2b-4d25-a1ab-9e7b1d8f09c9.mp4` | 9277ef5e | bc0496bf |
| 4 | 6 ÷ 3 = 2 | `hf_20260718_224421_21063464-d6a4-4619-8b2c-a4cc230511e9.mp4` | 21063464 | e3a6a381 |
| 5 | Finale (friends cheer, equal piles) | `hf_20260718_224425_99b99fae-36c1-4d70-9cac-72ea98ff482d.mp4` | 99b99fae | 1cbb47db |

## Stills (verified, used as animation frames)
Reference sheet `6eb77916`, then 5 stills:
`53d05ddf, 2af409f4, bc0496bf, e3a6a381, 1cbb47db`.
(Still `bc0496bf` for 4÷2 was a re-roll after the first job `9aebe526` hung.)

## Notes / lessons this run added
- **`gemini_omni` needs the prompt INSIDE `params`** (like `nano_banana_pro`).
  The first clip batch submitted with only a top-level prompt rendered with an
  empty prompt and all 5 **failed instantly** — resubmit with `params.prompt`.
- Assembly (`explainer_video`) is free and completed on the first try.

## To re-stitch / extend
`explainer_video(width:1280, height:720, items:[f6a87555, 4e27bb5c, 9277ef5e,
21063464, 99b99fae])`. To extend (8÷2=4, 9÷3=3, 10÷2=5): re-roll a still to the
exact count → animate image-to-video → add its clip id to the ordered list.
