# Seascape

A long-exposure exposure calculator for a **Hasselblad 503CW** shooting seascapes on film.

It answers one question on a cold beach: *how long do I hold B open?*

**Open it here: https://marvpdroid.github.io/Photography/**

On an iPhone: open that link in Safari → Share → **Add to Home Screen**. It then runs
full-screen, works offline, and remembers your filters and calibration.

## What it does

- **Reciprocity, properly.** Metered 2½ minutes becomes a real 11¼ minutes on HP5+. The arithmetic
  everyone does in their head is the arithmetic that ruins the frame.
- **Solves either direction.** Pick the look you want and it tells you which ND to fit; or tell it
  what is on the lens and it tells you what you will get.
- **Tone placement for reflected metering.** Spot-meter white surf on a Canon 7D, take the reading
  at face value, and you are two stops under. It handles that.
- **Tide, sun and moon** for the spot and the day, so you know when low water lands in the golden
  hour and how much moonlight there will be after dark.
- **A bulb timer** that beeps and buzzes at three, two, one and close.

## Film stocks

| Film | Speed | Reciprocity |
|---|---|---|
| Ilford HP5 PLUS | 400 | Ilford's published T^1.31 |
| Ilford FP4 PLUS | 125 | Ilford's published T^1.31 |
| Kodak Gold | 200 | +1 stop at 1 s, +2 at 10 s, +3 at 100 s |
| Kodak Portra 400 | 400 | +⅓ stop at 1 s, +1 at 10 s, +2 at 100 s |

Portra holds reciprocity nearly as well as the Ilford films; Gold is the worst of the four past a
few seconds. The app says so, with the number, when you have Gold selected.

## Metering

Pick the meter you actually used:

- **Sekonic L-308S, incident** — no compensation. The dome reads the light falling on the scene,
  so the tone of what you point at is irrelevant. The one to trust.
- **Sekonic L-308S, reflected** or **Canon 7D, spot** — both render whatever they read as mid-grey,
  so they need placing. Sunlit foam is +2 stops, wet dark rock is −1⅔, and so on.

There is a calibration panel for the real measured strength of each ND filter (most "10-stops" are
not ten) and for an offset between the two meters. Set it once.

## Filters

Densities are shown next to the stop count, so the chips match what is written on the filter:
0.3 = 1 stop, 0.6 = 2, 0.9 = 3, 1.8 = 6 (Lee Little Stopper), 3.0 = 10 (Big Stopper),
4.5 = 15 (Super Stopper). It considers every combination of what you own, not just pairs.

## Accuracy

- Sun times are computed on the device and agree with published values to within a minute.
- Moon phase and rise/set use the standard low-precision lunar series — good to a few minutes.
- Tide comes from [Open-Meteo](https://open-meteo.com/)'s marine model, cached locally so it
  survives a beach with no signal. **Heights are relative to mean sea level, not chart datum** —
  use it for timing, not for depth. For navigation use the real tide tables.
- Moonlight exposure is an estimate. No handheld meter reads that low. Bracket two stops either side.

## Built with

One HTML file, no dependencies, no build step, no tracking, no network calls except the tide lookup.
