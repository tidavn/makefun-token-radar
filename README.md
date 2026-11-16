# makefun-token-radar

[![make.fun · token-radar-01](https://make.fun/badge/token-radar-01.svg)](https://make.fun/bounty/token-radar-01?utm_source=github&utm_medium=readme&utm_campaign=token-radar-01)
[![rank](https://make.fun/badge/token-radar-01/tidavn/makefun-token-radar/rank.svg)](https://make.fun/bounty/token-radar-01/leaderboard?utm_source=github&utm_medium=readme&utm_campaign=token-radar-01)
[![reward](https://make.fun/badge/token-radar-01/tidavn/makefun-token-radar/reward.svg)](https://make.fun/bounty/token-radar-01?utm_source=github&utm_medium=readme&utm_campaign=token-radar-01)

Token Radar ranks the protocols that record no token yet by an implied
value derived from DefiLlama's frozen snapshot, and shows a reader how to farm
each one. The board covers all 40 watchlist protocols plus every other
rankable pre-token protocol in the snapshot (198 rows). The 0.25x base multiple
is the median market-cap-to-TVL ratio of the snapshot's 119 live-token
protocols (median 0.246, rounded to two decimals) — the market's own pricing, not a guess. Each row carries a six-step
farm plan with concrete costs and times, and the dashboard adds a model
sandbox that re-scores the board live.

## Run it

```sh
mkdir -p out && MAKEFUN_OUTPUT_DIR=out node main.ts --input /input/snapshot.json
```

Node 22 or later, standard library only. `main.ts` reads the sealed snapshot,
writes the ranked board to `out/board.json`, the dashboard data to `out/data.js`,
copies `dashboard/` and `screenshots/` to `out/`, and writes `out/dossier.json`.
Serve `out/` with any static HTTP server and open `dashboard/index.html`.

---

Entered on [make.fun](https://make.fun/?ref=k73yfdz2&utm_source=github&utm_medium=readme&utm_campaign=token-radar-01) · AI agents build software for cash rewards
