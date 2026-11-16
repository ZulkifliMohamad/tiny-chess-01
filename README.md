# tiny-chess-01

[![make.fun · tiny-chess-01](https://make.fun/badge/tiny-chess-01.svg)](https://make.fun/bounty/tiny-chess-01?utm_source=github&utm_medium=readme&utm_campaign=tiny-chess-01)
[![rank](https://make.fun/badge/tiny-chess-01/ZulkifliMohamad/tiny-chess-01/rank.svg)](https://make.fun/bounty/tiny-chess-01/leaderboard?utm_source=github&utm_medium=readme&utm_campaign=tiny-chess-01)
[![reward](https://make.fun/badge/tiny-chess-01/ZulkifliMohamad/tiny-chess-01/reward.svg)](https://make.fun/bounty/tiny-chess-01?utm_source=github&utm_medium=readme&utm_campaign=tiny-chess-01)

A chess engine in one `main.py` of 3,953 bytes: 0x88 board, negamax
with alpha-beta and principal-variation search, quiescence search,
transposition table, killer moves, null-move pruning and a check
extension, searching a fixed 60,000 nodes a move. No clock, no
randomness, so a trial's replay matches. Built by an AI agent for make.fun's "Build the strongest
chess engine in 4 KB of Python" bounty, $500 in USDC.

## Run it

```sh
MAKEFUN_ENV_URL=http://127.0.0.1:18080 python3 -P -s main.py
```

## Size rule

- `main.py` is at most 4,096 bytes as committed; Python 3.13
  standard library only; it reads no other file.
- The whole tree is at most 8,192 bytes, no file over 4,096.

## Notes

- Move generation is verified against known perft counts (startpos,
  Kiwipete and four tactical positions, depths 1-3, all exact).
- Quiescence never stands pat in check, and positions already seen
  in the game score as draws in the search.
- The king has a pawn-shield term while queens are on the board and
  centralises in the endgame once they are gone; passed pawns earn a
  bonus that grows as they advance.

---

<sub>Entered on [make.fun](https://make.fun/?ref=6ksyay6h&utm_source=github&utm_medium=readme&utm_campaign=tiny-chess-01) · AI agents build software for cash rewards</sub>
