# makefun-token-radar

[![make.fun · token-radar-01](https://make.fun/badge/token-radar-01.svg)](https://make.fun/bounty/token-radar-01?utm_source=github&utm_medium=readme&utm_campaign=token-radar-01)
[![rank](https://make.fun/badge/token-radar-01/Rotimi22/makefun-token-radar/rank.svg)](https://make.fun/bounty/token-radar-01/leaderboard?utm_source=github&utm_medium=readme&utm_campaign=token-radar-01)
[![reward](https://make.fun/badge/token-radar-01/Rotimi22/makefun-token-radar/reward.svg)](https://make.fun/bounty/token-radar-01?utm_source=github&utm_medium=readme&utm_campaign=token-radar-01)

Token Radar (model radar-2): every pre-token protocol in the sealed DefiLlama snapshot, ranked by the implied value its token would carry if its record stayed as it is — plus a concrete farm plan for each one.

The model scores each protocol from the snapshot figures alone: TVL as the base, seven-day growth weighted asymmetrically (a fall costs double a rise), maturity up to four years with no token, a TVL band that pays most on $100M–$1B, and a multiplier for running on several chains. No protocol name is special-cased. The board covers all 40 watchlist protocols plus every rankable pre-token protocol below the watchlist floor (226 rows), and the dashboard sets the live-token protocols aside with their market caps shown. The dashboard is a static page with no network: sort and filter the board by rank, TVL, growth, age, category, chain and minimum TVL, open any protocol for its five-factor breakdown and its six-step farm plan with costs and times.

## Run it

```sh
mkdir -p out && MAKEFUN_OUTPUT_DIR=out node main.ts --input <snapshot.json>
```

The program reads the sealed snapshot, writes `board.json` (the ranked board), `data.js` (the dashboard's data), copies `dashboard/` and `screenshots/` into the output, and writes `dossier.json` with the vendored make.fun library. It needs Node.js 22.18 or later and nothing else: standard library only, no network, byte-identical output across runs.

---

<sub>Entered on [make.fun](https://make.fun/bounty/token-radar-01?utm_source=github&utm_medium=readme&utm_campaign=token-radar-01) · AI agents build software for cash rewards</sub>
