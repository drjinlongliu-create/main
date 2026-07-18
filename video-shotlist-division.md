# 🎬 Video Shot List — "Sharing With Freddy" (Division Intro, ~50s)

Freddy the clay frog teaches **division as fair sharing** for a 5-year-old:
you have some berries, share them evenly onto lily-pad "plates," and everybody
gets the **same** amount. The mirror image of the 2× multiplication video
(which *built* equal groups) — here we *split* a total into equal groups.

Built with the locked-cast, still-first workflow (see `CLAUDE.md`).
Style: **Claymotion** (`1de0f39e-…`), matching the counting + multiplication
videos. Anchored to the series Freddy (`7e5a1860`) so he stays identical.

**Scope (user-approved):** short 5-clip cut (~50s), silent/ambient clips with
a Suno track overlaid.

| # | Time | Beat | What happens | Math |
|---|------|------|--------------|------|
| 1 | 0:00 | Hook | Freddy holds a basket of red berries beside empty lily-pad plates, waves hello | — |
| 2 | 0:10 | Share by 2 | 2 berries drop one-by-one onto 2 pads → 1 berry each | 2 ÷ 2 = 1 |
| 3 | 0:20 | Share by 2 | 4 berries share onto 2 pads → 2 berries each | 4 ÷ 2 = 2 |
| 4 | 0:30 | Share by 3 | 6 berries share onto 3 pads → 2 berries each | 6 ÷ 3 = 2 |
| 5 | 0:40 | Finale | Freddy and friends cheer over equal berry piles, "Sharing is fair!" | — |

## Educational design
- **One idea, repeated:** division = **equal shares**. Number of lily pads =
  how many groups; berries per pad = the answer.
- **Every equation is countable:** the pads and berries on screen always match
  the numerals, so a child can count the answer even if a digit renders loosely.
- **Totals stay ≤ 6 and groups small (2–3 pads),** keeping counts inside the
  model's reliable range; the per-still user QA gate backs it up.
- **Numerals on screen are content, not banned text** — the equation
  (e.g. "6 ÷ 3 = 2") is allowed; only other words/letters are negatived.

## Audio
None baked in; clips are silent/ambient on purpose. Overlay the Suno track
(`suno-prompt-division.md`) in any editor so audio sits cleanly on top.
