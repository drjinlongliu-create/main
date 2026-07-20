# Division video — job manifest (scratchpad, keep updated)

Series Freddy anchor: 7e5a1860-b86b-4cd8-8020-be494a96669f
Style: Claymotion (preset 1de0f39e-c602-4b00-b54a-38440c7f63f7)
Scope: 5 clips — hook, 2÷2=1, 4÷2=2, 6÷3=2, finale

## v5 REVISION (user QA on v4 stitched clips): SWITCH sharing clips to all-gemini still-motion
User rejected seedance hand-out clips (colour drift, background drift, berry duplication) AND
they block stitching. New approach = animate the finished-share END stills with gemini_omni
(locks colour/bg/counts, no duplication, stitches natively — also fixes the assembly blocker).
Fixes: clip1 hook basket -> only 2 berries (new still 41c67cc9-f3a4-41e4-b863-177089b0d02a).
NEW all-gemini clip plan (video gen currently 429 by hung explainer jobs; scheduled retry trig_019gkWb5GfAPxYGP2FxmRoNm @10:55Z):
  1 hook   <- gemini from still 41c67cc9 (2 berries) [PENDING user OK of still]
  2 2÷2=1  <- gemini from still e1599641 (empty basket, 1 each)
  3 4÷2=2  <- gemini from still 76b19889 (empty basket, 2 each)
  4 6÷2=3  <- gemini from still f6c40cdc (empty basket, 3 each)
  5 finale <- gemini from NEW still bc1a7a7e-a66b-420e-9da8-92f205937f3b (2 friends, trimmed per user; replaces old 3-friend f060fd45)
Then stitch all-gemini (native, ~1min). Superseded: seedance clips ca6db1a7/584464fd/2a12455e,
their re-encodes f9f53ce8/8717da60/62e15cb9, and old finale f060fd45 — no longer used.
Scheduled retry: trig_019nepuYcA6sRo5BzyFyym6A @ 11:01Z (animates all 5 gemini clips + stitch).

### v5 CLIPS SUBMITTED (quota freed, gemini_omni, play order):
  1 hook   c6c4ff1d-96e4-4ed8-a9d5-c4f5bea45ae0  (from 41c67cc9)
  2 2÷2=1  e2c75872-732f-4d39-bed7-0f49782284d9  (from e1599641)
  3 4÷2=2  8a63242d-56ba-4386-9737-a58992070a47  (from 76b19889)
  4 6÷2=3  8e678ad7-daf1-48a9-af74-105607fd7cf1  (from f6c40cdc)
  5 finale bca9861f-6561-4eb1-92b4-78ba240567d1  (from bc1a7a7e, 2 friends)
Stitch order: c6c4ff1d, e2c75872, 8a63242d, 8e678ad7, bca9861f

### ✅ FINAL VIDEO DELIVERED
Stitch job a7076f5b-c8a7-43b2-af3a-d784740f53a9 COMPLETED.
FINAL v5: https://d8j0ntlcm91z4.cloudfront.net/user_3FGVsNrxRrv3NuW3XlCmrTwRKNU/hf_20260719_232310_a7076f5b-c8a7-43b2-af3a-d784740f53a9.mp4

### v6 REVISION: match all clips to clip-1 background/colours (user: bg + colour shift between clips)
Re-rolled clips 2-5 stills anchored to clip-1 still 41c67cc9 (same pond bg + colours). Clip 1 unchanged.
Matched stills: 2÷2 0fd4c215 · 4÷2 2e17ecec · 6÷2 03eaa92a · finale 0d678945.
v6 gemini clips (clip 1 c6c4ff1d reused):
  1 hook   c6c4ff1d (unchanged)
  2 2÷2=1  ce1b5fa7-9846-4a79-9c77-3c1ab3ca334d (from 0fd4c215)
  3 4÷2=2  e5c09ab5-2741-4baa-8c26-f8539dbe9314 (from 2e17ecec)
  4 6÷2=3  16013d9f-fe16-4735-ad2d-804d0489bcac (from 03eaa92a)
  5 finale 2866c7ab-0bb9-472a-8904-1b1d4ca46594 (from 0d678945)
Stitch order: c6c4ff1d, ce1b5fa7, e5c09ab5, 16013d9f, 2866c7ab

### v7 REVISION: add the HAND-OUT action back (gemini from START stills, bg-matched to clip 1)
Start stills (friends empty, N berries in basket, bg matched to clip1 41c67cc9):
  clip2 start 6b3ca861 (2 berries) · clip3 start 4ebb119d (4) · clip4 start 2802bef1 (6, single row after many re-rolls)
v7 hand-out clips (gemini_omni single-frame animating the hand-out):
  1 hook   c6c4ff1d (unchanged)
  2 2÷2=1  e6494276-4072-48e5-902d-6616f9e27e24 (from 6b3ca861)
  3 4÷2=2  56cc5e41-c91d-4a4b-a447-d3cf43010a63 (from 4ebb119d)
  4 6÷2=3  d5b7d0e7-8752-4ea6-b0ad-e96c87029bb7 (from 2802bef1)
  5 finale 2866c7ab (unchanged)
Stitch order v7: c6c4ff1d, e6494276, 56cc5e41, d5b7d0e7, 2866c7ab

### ✅ v7 FINAL DELIVERED — stitch 319bef58-96e9-4edd-aed7-2af48d622427
https://d8j0ntlcm91z4.cloudfront.net/user_3FGVsNrxRrv3NuW3XlCmrTwRKNU/hf_20260720_134345_319bef58-96e9-4edd-aed7-2af48d622427.mp4

### v8: hand-out with LOCKED end counts (seedance start->end; gemini kept duplicating)
User: gemini hand-out duplicated berries (clip3 snail->3, clip4 snail->5) even after re-rolls.
Fix: seedance_2_0 start->end interpolation — END frame locks each friend's exact share.
Both frames anchored to clip 1 bg. Then topaz re-encode -> stitch with gemini hook+finale.
seedance clips (generate_audio false):
  2 2÷2=1  dce9c261-0883-4beb-b006-30dda3f7cb73  (start 6b3ca861 -> end 0fd4c215)
  3 4÷2=2  65252e5d-0aed-489b-806c-815feb0a9e06  (start 4ebb119d -> end 2e17ecec)
  4 6÷2=3  48f0342f-8715-49bd-b238-b9036ff384db  (start 2802bef1 -> end 03eaa92a)
hook c6c4ff1d + finale 2866c7ab reused (gemini). Then topaz-reencode the 3 seedance -> explainer_video.

## (OLD) CONCEPT REVISION (v2): share berries between FRIENDS, not plates
Divisor = number of friends (snail+dragonfly for ÷2, +turtle for ÷3). Freddy shares.
Anchored to BOTH series cast sheet 7e5a1860 (friends/colors) + berry ref 6eb77916.
v2 stills (pending QA → then re-animate → re-stitch):
1. hook (Freddy + 3 friends waiting) — 364d1ea4-6998-4e6f-962f-d998eec19ea4
2. 2÷2=1 (snail+dragonfly, 1 each)  — 28d77e12-ffd3-4594-a6ec-fb4506fe976b
3. 4÷2=2 (snail+dragonfly, 2 each)  — 21949bae-85d5-473c-984e-9d7daa99260a
4. 6÷3=2 (snail+dragonfly+turtle,2) — db27c62b-ebb0-49ee-a90a-6263c2c8cbab
5. finale (friends w/ equal shares)  — 7ca8f529-e7d6-484a-8b22-a961fb50f136

### v3 — SHOW THE HAND-OUT via start→end keyframe interpolation (seedance_2_0)
Math clip 4 changed to 6÷2=3 (2 friends, 3 each) per user.
All 3 math clips use 2 friends (snail+dragonfly). Keyframe pairs:
- clip2 2÷2=1: start d5a45a4f-5b76-43fd-b370-cc0179b2ec81 → end 28d77e12-ffd3-4594-a6ec-fb4506fe976b
- clip3 4÷2=2: start 1d283d58-0a1a-4c9f-a2e1-4b023feeaa56 (v2, 4 in basket) → end 76b19889-b7be-4631-9080-9e29c2ba795a (v2, empty basket)
    [superseded: start 6b986488 had >4; end 21949bae had berries left in basket]
- clip4 6÷2=3: start d183513e-5991-4fd1-8f7d-cdd36b8111d0 (v2, 6 in basket) → end f6c40cdc-8385-4a55-8bdd-a817928e8474
    [superseded: start 7e2f482d had >6]
- hook: single-frame gemini_omni from 364d1ea4 (friends gather)
- finale: single-frame gemini_omni from 7ca8f529 (KEEP)
[stills APPROVED]

### v3 CLIPS (submitted, play order):
1. hook   — 93aebe54-6307-4f65-9394-c09bb81e6687  (gemini_omni, from 364d1ea4; first try 8ef6c2d9 failed transient)
2. 2÷2=1  — 1df7f885-960e-470c-aa32-524871a36c92  (seedance_2_0, d5a45a4f→28d77e12)
3. 4÷2=2  — d13d1eb0-35b6-4029-9179-0d4387e23d5d  (seedance_2_0, 1d283d58→76b19889)
4. 6÷2=3  — 2a12455e-d77b-4ddc-8370-d98201651a08  (seedance_2_0, d183513e→f6c40cdc)
5. finale — f060fd45-f994-4840-b0f6-4cc19d19ec47  (gemini_omni, from 7ca8f529)
Play order for explainer_video: 93aebe54, 1df7f885, d13d1eb0, 2a12455e, f060fd45
ALL 5 CLIPS COMPLETED. (clip2/clip4 originals finished; redundant resubmits a023b3c2/922edf4d ignored.)
Clip URLs (base https://d8j0ntlcm91z4.cloudfront.net/user_3FGVsNrxRrv3NuW3XlCmrTwRKNU/):
1 hook   hf_20260718_230629_93aebe54-6307-4f65-9394-c09bb81e6687.mp4
2 2÷2=1  hf_20260718_230527_1df7f885-960e-470c-aa32-524871a36c92.mp4
3 4÷2=2  hf_20260718_230531_d13d1eb0-35b6-4029-9179-0d4387e23d5d.mp4
4 6÷2=3  hf_20260718_230534_2a12455e-d77b-4ddc-8370-d98201651a08.mp4
5 finale hf_20260718_230547_f060fd45-f994-4840-b0f6-4cc19d19ec47.mp4
Assembly jobs (backend hung ~25min, ABANDONED): 09697315, 6a717643

### v4 FIXES (user QA on v3 clips):
- Hook → 2 friends only (snail+dragonfly). New still: 32a7a140-22c2-4109-b425-f8070523b0b2
- Clip2 end → basket fully empty (was 1 left). New end still: e1599641-d318-4fed-a06d-14b7545d6bee
    clip2 new pair: start d5a45a4f → end e1599641
- Clip3 → Freddy color drifted mid-clip; re-run seedance start 1d283d58 → end 76b19889 with color-lock
- Clip4 (6÷2=3) unchanged (2a12455e), finale unchanged (f060fd45)
- NOTE: finale still shows 3 friends; hook now 2 — user said "go", leaving finale as full-gang.

### v4 FINAL play order (re-renders submitted):
1. hook   — 62749bfd-c2e2-44f5-acd2-1a7e81d6a72d  (gemini, from 32a7a140, 2 friends)
2. 2÷2=1  — ca6db1a7-7554-424e-8870-bee4ebc95a21  (seedance, d5a45a4f→e1599641 empty basket)
3. 4÷2=2  — 584464fd-e6c0-408a-9d68-27cb9c49bfe8  (seedance, 1d283d58→76b19889, color-lock)
4. 6÷2=3  — 2a12455e-d77b-4ddc-8370-d98201651a08  (unchanged)
5. finale — f060fd45-f994-4840-b0f6-4cc19d19ec47  (unchanged)
explainer_video order: 62749bfd, ca6db1a7, 584464fd, 2a12455e, f060fd45
ALL 5 v4 CLIPS COMPLETE. (redundant retries a06ead1e/694878bb ignored.)
v4 clip URLs (base https://d8j0ntlcm91z4.cloudfront.net/user_3FGVsNrxRrv3NuW3XlCmrTwRKNU/):
1 hook   hf_20260718_235004_62749bfd-c2e2-44f5-acd2-1a7e81d6a72d.mp4
2 2÷2=1  hf_20260718_235009_ca6db1a7-7554-424e-8870-bee4ebc95a21.mp4
3 4÷2=2  hf_20260718_235013_584464fd-e6c0-408a-9d68-27cb9c49bfe8.mp4
4 6÷2=3  hf_20260718_230534_2a12455e-d77b-4ddc-8370-d98201651a08.mp4
5 finale hf_20260718_230547_f060fd45-f994-4840-b0f6-4cc19d19ec47.mp4

### FINAL STITCH STATUS: Higgsfield backend severely backlogged (2026-07-18 late).
explainer_video jobs queued (free), stuck 20-30min+ today:
  943e62df-1a55-40cb-92eb-d0495dbe7d9e (full 5-clip v4)
  f4a0b5ae-25da-4e13-a6e0-9a1107e45444 (3 seedance clips, diagnostic)
No local ffmpeg; CDN blocked by egress proxy (403) — cannot assemble outside Higgsfield.
All 5 v4 clips ARE rendered & delivered; final MP4 pending queue drain.

### ROOT CAUSE CONFIRMED (diagnostic): explainer_video CANNOT ingest seedance_2_0 clips.
- 2-gemini stitch [hook,finale] ec6d7096 COMPLETED in ~45s (proves backend up + gemini clips fine).
- Any stitch containing seedance clips hangs indefinitely (943e62df, f4a0b5ae, both v3 stitches).
- Plan: re-encode the 3 seedance clips via topaz upscale -> stitchable, then explainer_video all 5.
  upscale test job (clip2): f9f53ce8-b190-4535-b80b-c507fa738b4e [QUEUED behind backlog]
- Fallback if re-encode doesn't stitch: re-animate 3 sharing clips with gemini_omni from START stills
  (d5a45a4f/1d283d58/d183513e) with hand-out prompt — stitches, but gemini counts less exact.
- Backend is globally backlogged tonight; heavy jobs queue for a long time. Resume when recovered.

### WORKAROUND PROVEN: topaz upscale re-encode makes seedance clips stitchable.
- clip2 re-encode f9f53ce8 DONE; test stitch [hook, f9f53ce8] b43cd7ba COMPLETED ~60s. FIX CONFIRMED.
- Re-encoding the other 2 seedance clips:
    clip3 (584464fd) -> 8717da60-8844-41a8-aaf7-2fdbdcc669dc
    clip4 (2a12455e) -> 62e15cb9-2ff0-41b4-8e17-c6e69e4771d2
- FINAL stitch order (once re-encodes done):
    62749bfd (gemini hook), f9f53ce8 (clip2 re-enc), 8717da60 (clip3 re-enc), 62e15cb9 (clip4 re-enc), f060fd45 (gemini finale)
- All 3 re-encodes DONE: clip2 f9f53ce8, clip3 8717da60, clip4 62e15cb9.
- FINAL stitch jobs (both pending, backend slow tonight but config PROVEN to work):
    6c6f5801-d2e4-45ab-892c-32f29d2ee72e
    77fa06c4-31c7-4e38-a6f4-8b81e6751225 (resubmit)
  Deliver whichever completes. If both stuck when backend recovers, resubmit same 5-item explainer_video.

--- v1 (plates concept, superseded) below ---

## Reference sheet (Phase 1 gate)
- job: 6eb77916-f6ff-470f-aca1-21d7223ebdeb  (nano_banana_pro, anchored to series Freddy)  [DONE, PENDING USER APPROVAL]
  url: https://d8j0ntlcm91z4.cloudfront.net/user_3FGVsNrxRrv3NuW3XlCmrTwRKNU/hf_20260718_223151_6eb77916-f6ff-470f-aca1-21d7223ebdeb.png

## Stills (Phase 2)
1. hook — 53d05ddf-d77b-464a-a2f0-99dee6b5d43c [APPROVED]
2. 2÷2=1 — 2af409f4-7457-4607-a09b-2ecbb372de5f [APPROVED]
3. 4÷2=2 — bc0496bf-9afc-4078-b56a-aa06fd495526 [DONE, pending approval] (first job 9aebe526 hung; re-rolled)
4. 6÷3=2 — e3a6a381-8315-4c59-8297-3814455d3f9f [DONE, pending approval]
5. finale — 1cbb47db-0d19-4229-b07e-5734054b1b99 [DONE, pending approval]

## Clips (Phase 3) — gemini_omni, 10s, 720p, image-to-video from approved stills
NOTE: first batch (473b7ff6, a9719dc4, c88fecee, 1530ecf6, 114471c5) ALL FAILED
— prompt landed empty; gemini_omni needs prompt INSIDE params. Resubmitted below.
1. hook   — f6a87555-d22d-4247-bdc0-824e4d47d1c1  (from still 53d05ddf)
2. 2÷2=1  — 4e27bb5c-7a11-4722-856b-29e6a205b989  (from still 2af409f4)
3. 4÷2=2  — 9277ef5e-fb2b-4d25-a1ab-9e7b1d8f09c9  (from still bc0496bf)
4. 6÷3=2  — 21063464-d6a4-4619-8b2c-a4cc230511e9  (from still e3a6a381)
5. finale — 99b99fae-36c1-4d70-9cac-72ea98ff482d  (from still 1cbb47db)
Play order for explainer_video: f6a87555, 4e27bb5c, 9277ef5e, 21063464, 99b99fae

## Final assembly (Phase 4)
- explainer_video job: b03f3138-70b7-41d1-b671-6364c24749ea  (1280x720, 5 blocks, DONE)
  FINAL: https://d8j0ntlcm91z4.cloudfront.net/user_3FGVsNrxRrv3NuW3XlCmrTwRKNU/hf_20260718_224538_b03f3138-70b7-41d1-b671-6364c24749ea.mp4

### All 5 clips COMPLETED (base URL: https://d8j0ntlcm91z4.cloudfront.net/user_3FGVsNrxRrv3NuW3XlCmrTwRKNU/)
1. hook   hf_20260718_224347_f6a87555-d22d-4247-bdc0-824e4d47d1c1.mp4
2. 2÷2=1  hf_20260718_224416_4e27bb5c-7a11-4722-856b-29e6a205b989.mp4
3. 4÷2=2  hf_20260718_224417_9277ef5e-fb2b-4d25-a1ab-9e7b1d8f09c9.mp4
4. 6÷3=2  hf_20260718_224421_21063464-d6a4-4619-8b2c-a4cc230511e9.mp4
5. finale hf_20260718_224425_99b99fae-36c1-4d70-9cac-72ea98ff482d.mp4

### ✅ v6 FINAL (bg/colour-consistent) DELIVERED
Stitch 90cf0aa0-9427-40d7-a912-3f1fd0031235
URL: https://d8j0ntlcm91z4.cloudfront.net/user_3FGVsNrxRrv3NuW3XlCmrTwRKNU/hf_20260720_062833_90cf0aa0-9427-40d7-a912-3f1fd0031235.mp4
