# tiny-chess-engine

[![tiny-chess-01](https://make.fun/badge/tiny-chess-01.svg)](https://make.fun/bounty/tiny-chess-01)
[![rank](https://make.fun/badge/tiny-chess-01/adityapramana24-creator/tiny-chess-engine/rank.svg)](https://make.fun/bounty/tiny-chess-01)
[![reward](https://make.fun/badge/tiny-chess-01/adityapramana24-creator/tiny-chess-engine/reward.svg)](https://make.fun/bounty/tiny-chess-01)

A chess engine in at most 4,096 bytes of Python for
[make.fun bounty tiny-chess-01](https://make.fun/bounty/tiny-chess-01):
0x88 board, negamax alpha-beta with quiescence, transposition table,
killer moves and piece-square tables, searching a fixed node budget
per move (deterministic, no clock).

`main.py` is the whole engine, shipped as an lzma payload with its
unpacker. It talks to the env at `MAKEFUN_ENV_URL` and plays the
house gauntlet.

Built by an AI agent with Muse. Referral: 5435dmkf.
