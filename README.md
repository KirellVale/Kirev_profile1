# osu!standard — Personal Competitive Skin & Settings

A personal osu!lazer setup focused on **readability, timing accuracy, consistency, and low visual noise**. The skin uses a minimal **black-and-pink UI** outside gameplay and prioritizes competitive clarity during gameplay.

> **Personal-use project.** This repository is a customization workspace, not an official osu! project. Settings below are the agreed configuration targets from our optimization process, not a claim that every recommendation was applied or benchmarked on the PC.

## Setup

| Item | Configuration |
| --- | --- |
| Client | osu!lazer |
| Ruleset | **osu!standard only** |
| Play style | No Mod (NM) primarily, Hidden (HD) occasionally |
| Display resolution | 1920 × 1080 |
| Monitor | 180 Hz capable, **165 Hz selected** |
| Skin | Customized legacy skin (`doki_mix_3` was the working name) |
| Output audio device | TOPPING USB DAC |

## 1. Graphics and performance

| Setting | Recommended configuration |
| --- | --- |
| Screen mode | Fullscreen |
| Resolution | 1920 × 1080 |
| Display refresh rate | 165 Hz (current Windows/display setting) |
| Minimize on focus loss | Off |
| UI scale | 1.0× |
| Screen scaling | Disabled |
| Renderer | Automatic (keep unless troubleshooting) |
| Frame limiter | **4× refresh rate** — approximately **660 FPS** at 165 Hz |
| Threading mode | Multithreaded |
| Show FPS | On while checking stability; optional afterward |
| Hardware video acceleration | Off if videos are disabled/not used |
| Screenshot format | PNG (lossless) |
| Include menu cursor in screenshots | Off |

**FPS note:** 4× is the recommended starting point, **not a proven universal minimum-latency setting**. Compare frame-time stability against 8× or *Basically unlimited* only if needed. Avoid VSync when minimizing input latency is the priority.

## 2. Input

| Setting | Configuration / guidance |
| --- | --- |
| High-precision mouse | On **for mouse play**; check tablet-driver compatibility before applying |
| Mouse sensitivity | 1.2× was shown in settings; retain familiar sensitivity rather than changing it blindly |
| Confine mouse to window | During gameplay |
| Disable mouse-wheel volume adjustment | **On (recommended change)** |
| Disable mouse clicks during gameplay | On **if using keyboard keys for tapping** |
| Gameplay cursor size | **0.4×**, visually validated with the revised cursor; recheck if asset changes |
| Automatic cursor size by beatmap | Off |
| Show cursor with touch input | Off when not using touch |
| Disable Windows key during gameplay | **On (recommended change)** |
| Increase first-object visibility with visual mods | **On (recommended for Hidden)** |

**Tablet note:** Tablet area, pen pressure, and sensitivity must be calibrated in the relevant tablet/driver section. Mouse sensitivity does not substitute for tablet calibration.

## 3. Audio and timing

| Setting | Configuration / guidance |
| --- | --- |
| Output device | TOPPING USB DAC |
| Legacy audio mode | Was enabled in the captured settings; **test non-legacy audio**, retaining whichever is stable and synchronized |
| Master volume | 100% |
| Volume when unfocused | 1% |
| Effects / hitsounds volume | 30% current; **40% is an optional comparison**, not confirmed |
| Music volume | 30% |
| Global audio offset | **0 ms** unless an actual consistent offset is measured |
| Positional/stereo separation of hitsounds | Off |
| Always play first combo-break sound | Off |

Optimized hitsounds were prepared for hit normals, claps, finishes, whistles, slider ticks, and selected spinner events. Continuous slider sounds and unnecessary notifications were intentionally kept quiet. **`failsound.wav` and `applause.wav` were intentionally preserved.**

Do **not** adjust global offset or switch audio modes based on assumptions alone: test against actual timing and audio stability.

## 4. Gameplay — visuals and beatmap content

| Setting | Recommended configuration |
| --- | --- |
| Score display mode | Standardised |
| Hit lighting | Off |
| Star fountains | Off |
| Background dim | **90%** |
| Background blur | **0%** |
| Brighten during breaks | **Off (recommended change)** |
| Turn playfield red when health is low | Off |
| Beatmap skins | Off |
| Beatmap combo colours | Off — use skin colours |
| Beatmap hitsounds | Off — use skin samples |
| Storyboards / videos | Off |
| Combo-colour normalisation | **0%** |

### osu!standard-specific visuals

| Setting | Configuration / guidance |
| --- | --- |
| Snaking in sliders | On |
| Snaking out of sliders | On was validated; optionally compare Off for less motion |
| Hit animations | On, as validated; reduce only if they prove distracting |
| Cursor trail | Off in client effects (custom assets remain separately controlled) |
| Cursor ripples | Off |
| Playfield border style | Corners |

## 5. HUD

| Setting | Recommended configuration |
| --- | --- |
| HUD visibility | Always |
| Replay settings overlay | Off |
| Always show key overlay | Off |
| Always show gameplay leaderboard | Off |
| Require holding a key to pause | Optional safety preference |
| Always show menu button | Off |
| Show health bar when failing is impossible | Off |

The HUD layout was simplified by removing the extra live **rank display** from `MainHUDComponents.json`, keeping essential gameplay information.

## 6. User interface

### General and main menu

| Setting | Configuration |
| --- | --- |
| Rotate cursor when dragging | Off |
| Menu cursor size | 0.5× |
| Menu parallax | Off |
| Hold-to-confirm delay | 0 ms |
| Menu tips | Off |
| Interface voices | Off |
| osu! theme music | Off |
| Intro animation | Circles (cosmetic; optional) |
| Menu background source | Skin |
| Seasonal backgrounds | **Off recommended** (captured value was Sometimes) |

### Song Select

| Setting | Configuration |
| --- | --- |
| Show converted beatmaps | Off |
| Random selection algorithm | Never repeat |
| Mod-select shortcut style | Sequential |
| Auto-focus mod search field | Off shown; personal preference |
| Song Select background blur | Off |

The minimal `SongSelect.json` visual accent was adjusted to avoid overlapping song titles; the native osu!lazer interface remains largely controlled by the client.

## 7. Debug and maintenance

| Setting | Guidance |
| --- | --- |
| Garbage collector (GC) mode | **Default** |
| Clear all caches | Only for troubleshooting, not regular optimization |
| Renderer and audio troubleshooting | Change one option at a time and compare gameplay stability |

## Skin implementation notes

- **Colour order:** green, red, yellow, blue; optional fifth purple. Prioritize distinctness over aesthetics.
- **UI style:** black and pink, minimal and readable.
- **Gameplay style:** low clutter; clean hitcircles, cursor, slider-follow ring, follow points, and spinner indicators.
- **Image naming:** double-resolution assets must have `@2x` **before `.png`**, e.g. `cursor@2x.png` and `followpoint-3@2x.png`.
- **`skin.ini` `Version: 2.2`:** the **legacy skinning format version**, not the custom project's release version. Do not increment it to version the project.
- **Skin metadata:** `skin.ini` holds `Name` and `Author`; osu!lazer also stores skin metadata in `skininfo.json`.
- **Distribution:** the intended use is personal. Do not assume original/remixed third-party assets are licensed for redistribution.

## Validation checklist

- [x] Personal visual check of the revised cursor and gameplay appearance in osu!lazer
- [x] Resolution and `@2x` naming review reported complete
- [ ] Confirm recommended toggles that were not shown again after changes
- [ ] Compare 4× FPS limit with alternatives only if frame pacing is unstable
- [ ] Compare legacy/non-legacy audio on the TOPPING USB DAC if changing audio mode
- [ ] Retest No Mod and Hidden after any future skin or input change

### References

- [osu! Skinning FAQ — high-resolution assets](https://osu.ppy.sh/wiki/en/Skinning/FAQ)
- [osu!lazer source code](https://github.com/ppy/osu)
