# Brainy Baby — Channel Brand Assets

Brand identity for the **Brainy Baby** nursery-rhyme YouTube channel.

- **Style:** Soft & pastel — baby blue, mint green, soft peach, lavender; rounded shapes, cozy nursery aesthetic.
- **Mascot:** "Brainy" the baby owl — round eyeglasses, fluffy baby-blue body, perched on an open storybook.
- **Tagline:** *Nursery Rhymes & Songs for Little Learners*
- **Generation model:** `nano_banana_pro` (Higgsfield). Banner + thumbnail are anchored to Logo A so the owl stays identical across assets.

> Note: CDN links are Higgsfield outputs. Download and re-host / upload to YouTube directly — treat these URLs as the source of truth for re-generation, not permanent hosting.

## Logo (1:1 — profile picture / channel icon)

Two options were generated; **Option A is the locked brand anchor**.

- **Logo A (locked anchor)** — job `7b1e48d5-7975-49a5-8c44-33544f41f205`
  https://d8j0ntlcm91z4.cloudfront.net/user_3FGVsNrxRrv3NuW3XlCmrTwRKNU/hf_20260712_042221_7b1e48d5-7975-49a5-8c44-33544f41f205.png
- **Logo B (alternate)** — job `05449a38-48b9-4990-a555-303212e04da1`
  https://d8j0ntlcm91z4.cloudfront.net/user_3FGVsNrxRrv3NuW3XlCmrTwRKNU/hf_20260712_042221_05449a38-48b9-4990-a555-303212e04da1.png

YouTube channel icon: recommended 800×800 (min 98×98). The 1024×1024 logo meets this.

## Banner (16:9 — channel cover art)

- **Banner** — job `c2a3a351-05d4-4667-80b5-0af012d42395`, 1376×768, anchored to Logo A
  https://d8j0ntlcm91z4.cloudfront.net/user_3FGVsNrxRrv3NuW3XlCmrTwRKNU/hf_20260718_215352_c2a3a351-05d4-4667-80b5-0af012d42395.png

- **Banner — 4K upscaled (upload this one)** — job `1e5b8bb3-db16-4e6e-9d8b-7f97142b93a5`, 4096×2294
  https://d8j0ntlcm91z4.cloudfront.net/user_3FGVsNrxRrv3NuW3XlCmrTwRKNU/hf_20260718_220814_1e5b8bb3-db16-4e6e-9d8b-7f97142b93a5.png

YouTube banner: recommended upload **2048×1152 minimum** (safe area 1235×338 for text/logo, visible on all devices). The 4K-upscaled banner (4096×2294) exceeds this and YouTube's 2560×1440 recommendation — use it for upload. Title + owl are kept in the central safe area.

## Thumbnail template (16:9 — reusable per-episode)

- **Thumbnail template** — job `e8dab8d6-14f6-45af-8ebf-eeb38b316752`, 1376×768, anchored to Logo A
  https://d8j0ntlcm91z4.cloudfront.net/user_3FGVsNrxRrv3NuW3XlCmrTwRKNU/hf_20260718_215358_e8dab8d6-14f6-45af-8ebf-eeb38b316752.png

Layout: owl waving on the right, large open title panel on the left (sample text "TWINKLE TWINKLE"), logo badge top-left. Swap the title text per episode; 1376×768 exceeds YouTube's 1280×720 thumbnail spec.

## Launch kit extras

### Transparent-background logo (for video watermark / overlays)
- **Logo A cutout (transparent PNG)** — job `8aadb195-2071-4824-8a32-bb06047bb195`
  https://d8j0ntlcm91z4.cloudfront.net/user_3FGVsNrxRrv3NuW3XlCmrTwRKNU/hf_20260718_221136_8aadb195-2071-4824-8a32-bb06047bb195.png

### Ready-to-upload episode thumbnails (16:9, anchored to Logo A)
- **ABC Song** — job `54f2eb75-4abe-410f-8a4a-37d8747b09c2`, 1376×768
  https://d8j0ntlcm91z4.cloudfront.net/user_3FGVsNrxRrv3NuW3XlCmrTwRKNU/hf_20260718_221143_54f2eb75-4abe-410f-8a4a-37d8747b09c2.png
- **Wheels on the Bus** — job `cab7cc05-1dd7-4d70-89be-17a53eef7e4b`, 1376×768
  https://d8j0ntlcm91z4.cloudfront.net/user_3FGVsNrxRrv3NuW3XlCmrTwRKNU/hf_20260718_221147_cab7cc05-1dd7-4d70-89be-17a53eef7e4b.png

### Video watermark (transparent PNG, simplified owl icon — reads at small size)
Purpose-built as a YouTube video watermark / branding overlay (recommended 150×150,
transparent). Simplified single owl-head icon (no text) so it stays legible in a video corner.
- **Watermark Option 1** — job `3f520e40-7eab-4dad-b057-92fd0fb91636` (transparent PNG)
  https://d8j0ntlcm91z4.cloudfront.net/user_3FGVsNrxRrv3NuW3XlCmrTwRKNU/hf_20260718_222947_3f520e40-7eab-4dad-b057-92fd0fb91636.png
- **Watermark Option 2** — job `93a49835-2857-4826-b08f-8e0ce8af392e` (transparent PNG)
  https://d8j0ntlcm91z4.cloudfront.net/user_3FGVsNrxRrv3NuW3XlCmrTwRKNU/hf_20260718_222948_93a49835-2857-4826-b08f-8e0ce8af392e.png

> Two watermark styles exist: this **simplified owl icon** (best for the small YouTube
> corner watermark) and the earlier **full-logo cutout** `8aadb195` (badge + text, better
> for larger end-screen / overlay use where text is readable).

To add in YouTube: Studio → Customize channel → Branding → Video watermark → upload.

See **`LAUNCH.md`** for the full channel setup checklist.

## To-do / optional next steps
- [x] Pick final logo (A vs B) — **A locked**, approved by user.
- [x] Upscale banner for YouTube upload — done, 4096×2294 (job `1e5b8bb3`).
- [x] Transparent-background logo cutout — done (job `8aadb195`).
- [x] Example thumbnails with real episode titles — ABC Song + Wheels on the Bus.
- [ ] Optional: animated channel trailer (Higgsfield `gemini_omni` from a still).
