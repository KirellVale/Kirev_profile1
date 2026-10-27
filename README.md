# osu!lazer — Competitive Setup (osu!standard)

Quick reference for a **1920×1080 / 165 Hz** setup, mainly **NM** with occasional **Hidden**. Priorities: readability, consistent timing, and minimal distractions.

## Graphics

| Setting | Value |
| --- | --- |
| Display | Fullscreen · 1920×1080 · 165 Hz |
| Renderer / threading | Automatic / Multithreaded |
| Frame limiter | **8× refresh rate** (~1000 FPS at 165 Hz) |
| UI scale / screen scaling | 1× / Disabled |

**Check:** 4× is a starting point. Compare 8× or *Basically unlimited* if frame times or responsiveness improve; avoid VSync for lowest-latency play.

## Input

| Setting | Value |
| --- | --- |
| High-precision mouse | On for mouse; test with tablet drivers |
| Mouse sensitivity | Keep familiar setting (1.2×) |
| Confine cursor | During gameplay |
| Disable mouse clicks / wheel volume | On when tapping with keyboard / On |
| Cursor size / auto-size | **0.4×** with current asset / Off |
| Disable Windows key in-game | On |
| First object visibility with visual mods | On (Hidden) |

**Check:** Tablet area and pen sensitivity must be set in your tablet software or tablet settings, not via mouse sensitivity.

## Gameplay & HUD

| Setting | Value |
| --- | --- |
| Background dim / blur | **90% / 0%** |
| Hit lighting / star fountains | Off / Off |
| Brighten during breaks / low-health red tint | Off / Off |
| Beatmap skins / colours | Off / Off |
| Beatmap hitsounds | Off for consistent skin audio¹ |
| Storyboards / videos | Off |
| Combo colour normalisation | 0% |
| HUD | Always visible; leaderboard and extra key overlay Off |
| Cursor ripples / built-in trail effects | Off / Off |
| Slider snaking | In: On; Out: preference |

¹ Beatmap hitsounds are mapper-authored. Turn them back on if you want the intended audio design.

## Audio

| Setting | Value |
| --- | --- |
| Output | Selected USB DAC / headphones |
| Master / music / effects | **100% / 30% / 30%**, adjust to comfort |
| Positional hitsound separation | Off |
| Audio offset | **0 ms** unless measured otherwise |
| Legacy audio | Keep whichever mode is stable and synchronized |

## Skin & important notes

- Combo colours: **green → red → yellow → blue**.
- Use `@2x` for double-resolution assets: `cursor@2x.png`, `followpoint-3@2x.png`, etc.
- After changing cursor, sliders, hitcircles, or input, test dense patterns in **NM and Hidden**.
- Change one performance or audio setting at a time; don't chase theoretical latency gains at the expense of stability.

*Personal baseline, not a universal performance preset.*
