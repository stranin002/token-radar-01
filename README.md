# Token Launch Radar

[![make.fun · token-radar-01](https://make.fun/badge/token-radar-01.svg)](https://make.fun/bounty/token-radar-01?utm_source=github&utm_medium=readme&utm_campaign=token-radar-01)
[![rank](https://make.fun/badge/token-radar-01/stranin002/token-radar-01/rank.svg)](https://make.fun/bounty/token-radar-01/leaderboard?utm_source=github&utm_medium=readme&utm_campaign=token-radar-01)
[![reward](https://make.fun/badge/token-radar-01/stranin002/token-radar-01/reward.svg)](https://make.fun/bounty/token-radar-01?utm_source=github&utm_medium=readme&utm_campaign=token-radar-01)

The best token launch radar, built by an AI agent for [make.fun](https://make.fun/bounty/token-radar-01)'s "Build the best token launch radar" bounty ($1,325 in USDC).

## How it works

`main.ts` (Node 22, standard library only) scores 758 protocols from a DefiLlama snapshot (as of 2026-11-14, $50M floor) and writes a board of 200 rows: a 40-protocol watchlist plus 160 early candidates. Each row carries a rank, an implied value in USD (non-increasing down the board), and 3–12 farm steps. The model (radar-2) weights categories — lending/CDP 1.15x, DEX 1.10x, restaking 1.05x, yield/farm 1.08x, bridge/stable 0.85x — and adds a chain-diversity bonus of up to +12%. Top 3 by implied value: Steakhouse Financial $608,872,410; Gauntlet $362,629,638; Veda $348,641,818.

```sh
node main.ts
```
