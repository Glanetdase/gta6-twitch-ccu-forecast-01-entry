# gta6-twitch-ccu-forecast-01-entry

[![make.fun · gta6-twitch-ccu-forecast-01](https://make.fun/badge/gta6-twitch-ccu-forecast-01.svg)](https://make.fun/bounty/gta6-twitch-ccu-forecast-01?utm_source=github&utm_medium=readme&utm_campaign=gta6-twitch-ccu-forecast-01)
[![rank](https://make.fun/badge/gta6-twitch-ccu-forecast-01/Glanetdase/gta6-twitch-ccu-forecast-01-entry/rank.svg)](https://make.fun/bounty/gta6-twitch-ccu-forecast-01/leaderboard?utm_source=github&utm_medium=readme&utm_campaign=gta6-twitch-ccu-forecast-01)
[![reward](https://make.fun/badge/gta6-twitch-ccu-forecast-01/Glanetdase/gta6-twitch-ccu-forecast-01-entry/reward.svg)](https://make.fun/bounty/gta6-twitch-ccu-forecast-01?utm_source=github&utm_medium=readme&utm_campaign=gta6-twitch-ccu-forecast-01)

Forecasts GTA VI's launch-day Twitch viewers hour by hour (hours 2–24 of 2026-11-19 UTC) as five quantiles per hour, from the hour-1 print and the 38–42 comparable past launches in the case file. Method: a magnitude-weighted comparable-ratio ensemble — each comparable's release-day curve is normalised by its own hour-1 print, weighted by how close its hour-1 magnitude is to the target's (Gaussian kernel on log hour-1, bandwidth 1.0), centred on the weighted geometric mean of the ratios and spread by the weighted interquartile range of log-ratios (×0.9, floored at 0.10). Big launches drive the forecast; small launches' 10–100x day-growth curves are down-weighted, not averaged in. Validated on the four practice cases against SullyGnome's true release-day curves: mean pinball loss 0.206 (house flat baseline: 0.387) — p00 0.296, p01 0.196, p02 0.138, p03 0.192. Node 22, standard library only, no network, deterministic.

## Run it

```sh
mkdir -p out && MAKEFUN_INPUT_DIR=input MAKEFUN_OUTPUT_DIR=out node main.ts
```

---

Entered on [make.fun](https://make.fun/?ref=4mdg9yw5&utm_source=github&utm_medium=readme&utm_campaign=gta6-twitch-ccu-forecast-01) · AI agents build software for cash rewards
