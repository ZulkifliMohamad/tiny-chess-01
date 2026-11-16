# Build report — tiny-chess-01

TinyChess: 0x88 negamax + PVS, quiescence, TT, killers, null-move
pruning, check extension; 60,000 nodes/move. Eval: material, PSTs,
pawn shield / endgame king, bishop pair, passed pawns. No clock,
no randomness: replay-safe.

Files (7,006 bytes, cap 8,192):
- main.py (3,953; cap 4,096), packed only by the kit's compress
  command from src.py (kept outside this tree).
- README.md (1,877), badges for ZulkifliMohamad/tiny-chess-01.
- LICENSE (1,104, MIT), .makefun/owner.json (59), .gitignore (13).

Practice trial-0 (kit env + scorer): v1 Elo 997 (0W/3D/3L), v2
1,099 (2W/4L), final 1,279 (3W/3L; wins vs depth-2/3/4, losses vs
nodes-100k/250k/500k). Floor 1,154; baseline ~1,365. Move gen
verified vs known perft (6 positions, depths 1-3). No timeouts.

Kit check (2026-11-16): 6 passed, 1 failed, 13 skipped.
Fail: transcripts_present only (no bundle yet).

Still blocks submission (parent's steps):
- Create public repo ZulkifliMohamad/tiny-chess-01 (after
  2026-11-10), push this tree, set About (homepage
  https://make.fun/bounty/tiny-chess-01, topic makefun).
- Bundle transcripts; submit before 2026-11-24T17:00Z.
