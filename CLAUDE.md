# CLAUDE.md

This repo produces kids' educational video content (nursery rhymes, counting
songs, and a Freddy multiplication series) with Higgsfield for visuals and
Suno (external) for sung audio. Follow the workflow below — it was refined
across the counting video (v1–v4) and the 2× times-table video, and each rule
exists because skipping it caused a real defect.

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
Re-rolling a still is cheap; re-rolling a clip is 30 credits. Show a reference
+ 1–2 pilot stills first and WAIT for approval before generating the full set.

- **Intentional duplicates (multiplication):** the "no duplicates" rule is
  per-scene, not absolute. For the 2× table each pad holds a deliberate PAIR
  of identical Freddys — so the still says "EXACTLY N pads × 2 = 2N frogs, N
  groups of two" and the negative bans only counts *beyond* the intended
  (e.g. "an eighth pad", "eleventh frog"), never "duplicated frog".
- **Equations on screen are content, not banned text:** math scenes state the
  numerals ("2 × 7 = 14") and keep them in the negative only as
  "no words/letters other than the equation numerals".
- **Exact counts get unreliable ≥ ~12** even still-first; big grids
  (2×8/2×9/2×10 = 16/18/20) are where the model drops a pad/pair. Expect the
  user to catch these per-clip; the fix is: re-roll that ONE still to the exact
  count → re-animate → re-stitch (assembly is free).
- **Reuse the locked character across videos:** anchor a new video's reference
  to the series Freddy (`7e5a1860`) so he matches earlier videos.
- **Scope control:** honor "stop at still N" / "animate only 1..N" — animate
  just that subset and end the video there.

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
  still-first pipeline, not prompt insistence — and even then ≥ ~12 needs
  per-clip user QA and targeted re-rolls.
- Numerals in scenes are fine, but ban letters/words in NEGATIVE prompts
  (except deliberate thumbnail text or equation numerals, which the user must
  eyeball).
- **False NSFW flag on dense identical grids:** a tidy grid of many identical
  figures (e.g. 18 clay Freddys) can return `status: "nsfw"` — a false
  positive. Re-submit the same still with softened wording ("a wholesome,
  cute, child-friendly Claymotion cartoon", "friendly little groups") and it
  passes.
- **Assembly is free and the MCP server flaps:** `explainer_video` costs no
  credits, so retry it through disconnects ("Tool permission stream closed" /
  "No such tool") — the clips are already rendered; just wait for a stable
  window and fire the same call. Save the clip-id manifest so a mid-run
  disconnect loses nothing, and commit an OUTPUT doc even while the final
  stitch is still pending.
- **Per-clip fix loop:** to correct one block, regenerate just that still to
  the exact count (user approves) → animate it image-to-video → re-run
  `explainer_video` with that clip swapped into the same ordered list.

## Repo layout
- `lyrics.md` / `README.md` / `guide.md` — the song, concept, teacher guide
- `suno-prompt.md` — Suno music kit (full-length + 3-min video-matched cut)
- `video-shotlist.md` — 18-block shot list (10s per block)
- `OUTPUT.md` — counting-video manifest (v4 final video + all job ids)
- `OUTPUT-multiplication.md` — 2× times-table video manifest (2×1–2×10 + ids)
- `promo.md` — thumbnail, hashtags (`#CountWithFreddy`), captions, posting tips
