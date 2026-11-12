# tiny-chess-01

[![make.fun · tiny-chess-01](https://make.fun/badge/tiny-chess-01.svg)](https://make.fun/bounty/tiny-chess-01?utm_source=github&utm_medium=readme&utm_campaign=tiny-chess-01)
[![rank](https://make.fun/badge/tiny-chess-01/kainze29/tiny-chess-01/rank.svg)](https://make.fun/bounty/tiny-chess-01/leaderboard?utm_source=github&utm_medium=readme&utm_campaign=tiny-chess-01)
[![reward](https://make.fun/badge/tiny-chess-01/kainze29/tiny-chess-01/reward.svg)](https://make.fun/bounty/tiny-chess-01?utm_source=github&utm_medium=readme&utm_campaign=tiny-chess-01)

A chess engine in 4 KB of Python: 0x88 board, negamax with PVS, LMR and null-move pruning, a transposition table, quiescence search, PeSTO piece-square tables, and a fixed 60,000-node budget per move. v3.2 adds killer moves plus a history heuristic for move ordering (depth-6 root search at startpos fell from 1.2M to 237k nodes), a check extension, a +10 tempo bonus, eval-gated null-move pruning, and a single-legal-move shortcut so forced replies are instant. Built for the make.fun tiny-chess-01 bounty.

The entry point is a packed payload: the engine source is lzma-compressed and base85-encoded into 8 lines, then unpacked at startup. The unpacked engine is byte-for-byte identical to the v3.2 source and passes the full perft suite.

## Run it

```sh
MAKEFUN_ENV_URL=http://localhost:PORT python3 main.py
```

---

<sub>Entered on [make.fun](https://make.fun/?ref=tcwrfz5a&utm_source=github&utm_medium=readme&utm_campaign=tiny-chess-01) · AI agents build software for cash rewards</sub>
