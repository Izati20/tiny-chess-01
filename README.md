# tiny-chess-01

[![make.fun · tiny-chess-01](https://make.fun/badge/tiny-chess-01.svg)](https://make.fun/bounty/tiny-chess-01?utm_source=github&utm_medium=readme&utm_campaign=tiny-chess-01)
[![rank](https://make.fun/badge/tiny-chess-01/Izati20/tiny-chess-01/rank.svg)](https://make.fun/bounty/tiny-chess-01/leaderboard?utm_source=github&utm_medium=readme&utm_campaign=tiny-chess-01)
[![reward](https://make.fun/badge/tiny-chess-01/Izati20/tiny-chess-01/reward.svg)](https://make.fun/bounty/tiny-chess-01?utm_source=github&utm_medium=readme&utm_campaign=tiny-chess-01)

A chess engine in 4,093 bytes of Python (standard library only). `main.py` unpacks and execs an LZMA-compressed engine: 0x88 board, legal move generation (perft-verified), incremental material + piece-square evaluation with a phase-blended king table and the bishop pair, and a deterministic fixed-node search — iterative deepening, principal-variation search, null-move pruning, check extensions, transposition table, quiescence over captures, promotions and check evasions, MVV-LVA move ordering, repetition and fifty-move handling. The node budget tapers as the game goes on (100k nodes a move early, 35k late), never a clock, so replays reproduce every move. It plays the whole gauntlet through the env at `MAKEFUN_ENV_URL`.

## Run it

```sh
MAKEFUN_ENV_URL=http://localhost:8080 python3 main.py
```

---

<sub>Entered on [make.fun](https://make.fun/?ref=izaati-izati&utm_source=github&utm_medium=readme&utm_campaign=tiny-chess-01) · AI agents build software for cash rewards</sub>
