# CLAUDE.md

This repo produces kids' educational video content (nursery rhymes, counting
songs) with Higgsfield for visuals and Suno (external) for sung audio.
Follow the workflow below — it was refined over four versions of the Freddy
the Frog video, and each rule exists because skipping it caused a real defect.

## Video content creation workflow

### Phase 0 — Feasibility before generating anything
1. Check `balance` and get real costs with `get_cost: true`
   (video ≈ 30 credits per 10s clip; stills are cheap). Budget the whole run
   before starting — never begin a batch that can't finish.
2. Confirm tool capabilities honestly: Higgsfield `seed_audio` is
   **speech-only** (it cannot sing); there is no Suno connector — for sung
   tracks, deliver a copy-paste Suno kit (style prompt + `[Verse]`-tagged
   lyrics, ≤4 min per generation, see `suno-prompt.md`).
3. The user picks the visual style from the `get_youtube_explainer_presets`
   gallery — never choose for them.

### Phase 1 — Locked character sheet (the consistency anchor)
Generate ONE character reference sheet (`nano_banana_pro`) with every
character named, in canonical order, with fixed colors. **User approves it
before anything else is built.** For this series the locked cast is:
1 green frog Freddy · 2 blue snail · 3 teal dragonfly · 4 green turtle ·
5 yellow duck · 6 orange fish · 7 red bird · 8 brown beaver ·
9 yellow firefly · 10 white bunny.

### Phase 2 — Verified stills (the QA gate)
One still per scene, anchored to the sheet (`medias: [{value: <sheet job id>,
role: "image"}]`), prompt stating "EXACTLY N characters" with every character
named, plus explicit negatives (no duplicates, no extra animals).
**The user spot-checks every still before animation** — Claude cannot view
frames (the CDN is blocked by the egress proxy), so the user is the only QA.
Re-rolling a still is cheap; re-rolling a clip is 30 credits.

### Phase 3 — Animate from stills (never from text)
Animate each approved still image-to-video: `gemini_omni`, `duration: 10`,
`resolution: "720p"`, the still as the image reference. Prompt pattern:
"ANIMATE THE ATTACHED IMAGE… preserve exactly… do not add, remove, duplicate,
or split any character" + gentle scene motion + ambient-only audio (no voice —
clips stay silent/ambient so the Suno track overlays cleanly).
**Never generate scene clips from text alone** — that was the root cause of
duplicated characters, wrong animals, and color drift in v1–v3.

### Phase 4 — Assemble and record
Stitch with `explainer_video` (1280×720), poll `job_display`. Then update
`OUTPUT.md` with the final URL + every clip job id, and commit/push at every
milestone — the session container is ephemeral.

## Operational pitfalls (all hit in practice)
- **Rate limit:** ~6 concurrent `gemini_omni` jobs → submit in batches of 3–4,
  wait for the queue to drain (429 = resubmit later, jobs are not queued).
- **Preset hijack:** `generate_video` sometimes returns a
  `preset_recommendation` notice instead of running — retry with
  `declined_preset_id` (pass it preemptively on kid-content prompts).
- **Aspect:** `gemini_omni` outputs 16:9 (1280×720) even from 9:16 presets;
  16:9 is fine for YouTube kids content; use `reframe` for Shorts.
- **Save job-id manifests immediately** (scratchpad + repo) — the MCP server
  disconnects mid-session and in-flight tool calls are lost.
- **AI counts are unreliable at 6+:** exact head-counts only survive via the
  still-first pipeline, not prompt insistence.
- Numerals in scenes are fine, but ban letters/words in NEGATIVE prompts
  (except deliberate thumbnail text, which the user must eyeball).

## Repo layout
- `lyrics.md` / `README.md` / `guide.md` — the song, concept, teacher guide
- `suno-prompt.md` — Suno music kit (full-length + 3-min video-matched cut)
- `video-shotlist.md` — 18-block shot list (10s per block)
- `OUTPUT.md` — generated-media manifest (v4 final video + all job ids)
- `promo.md` — thumbnail, hashtags (`#CountWithFreddy`), captions, posting tips
