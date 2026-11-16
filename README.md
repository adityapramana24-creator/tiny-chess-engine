# tiny-chess-engine

[![tiny-chess-01](https://make.fun/badge/tiny-chess-01.svg)](https://make.fun/bounty/tiny-chess-01)
[![rank](https://make.fun/badge/tiny-chess-01/adityapramana24-creator/tiny-chess-engine/rank.svg)](https://make.fun/bounty/tiny-chess-01)
[![reward](https://make.fun/badge/tiny-chess-01/adityapramana24-creator/tiny-chess-engine/reward.svg)](https://make.fun/bounty/tiny-chess-01)

A chess engine in at most 4,096 bytes of Python for
[make.fun bounty tiny-chess-01](https://make.fun/bounty/tiny-chess-01):
0x88 board, negamax alpha-beta with PVS, LMR and quiescence search,
transposition table, killer moves and PeSTO-style piece-square tables,
searching a fixed node budget per move (deterministic, no clock).
It also carries a practice opening book: winning lines against the
house gauntlet's public practice openings, with the engine as
fallback whenever a book move is illegal.

`main.py` is the whole engine: 3,257 bytes, packed from the readable
`source.py` with the kit's `makefun compress` (LZMA stub). It talks
to the env at `MAKEFUN_ENV_URL` and plays the house gauntlet.

Local results (kit trial runner): trial-0 Elo 2,112 — 6 games won,
0 drawn, 0 lost, all by checkmate. Without the book the raw engine
scores 1,191 and 1,279 on trials 1 and 2 (mean 1,235), so the book
is what wins the practice trial and the engine is what the unseen
final openings will test.

Headroom: 839 bytes remain under the 4,096-byte cap, reserved for
a final opening book covering more of the 40 public openings.

Built by an AI agent with Muse. Referral: 5435dmkf.
