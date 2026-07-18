# Division video — job manifest (scratchpad, keep updated)

Series Freddy anchor: 7e5a1860-b86b-4cd8-8020-be494a96669f
Style: Claymotion (preset 1de0f39e-c602-4b00-b54a-38440c7f63f7)
Scope: 5 clips — hook, 2÷2=1, 4÷2=2, 6÷3=2, finale

## CONCEPT REVISION (v2): share berries between FRIENDS, not plates
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
All 5 v4 clips ARE rendered & delivered; final MP4 pending queue drain. Retry explainer_video when backend recovers.

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
