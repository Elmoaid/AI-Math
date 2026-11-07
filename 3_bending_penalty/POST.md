# Turn-penalty inside 2-opt (Euclidean TSP heuristic): measured properly, it helps a little

Question: does a geometric "bending" penalty added during 2-opt and removed at the end help the heuristic? An early run on 12 instances suggested it "halves 2-opt's excess"; reimplemented and measured against LKH-3 optima, it doesn't.

Objective during search: L(tour) + λ·Σ |eᵢ||eᵢ₊₁|·sin(turnᵢ). First-improvement 2-opt from random starts, then plain 2-opt polish. Mean excess over the optimum, best of the same 3 starts (SE in parentheses):

| n (instances) | plain 2-opt | λ=1 | λ=4 | 2-opt + Or-opt |
|---|---|---|---|---|
| 35 (400) | 2.82% (0.12) | 2.46% (0.10) | 2.27% (0.10) | 0.52% (0.05) |
| 70 (200) | 5.77% (0.16) | 5.58% (0.15) | 5.05% (0.16) | 1.78% (0.10) |
| 140 (200) | 8.49% (0.13) | 8.03% (0.12) | 7.32% (0.12) | 3.44% (0.08) |

Costs 2–3× the time of plain 2-opt; plain 2-opt with equal-time restarts beats it; Or-opt beats it by 2–4×; no growth with n. Known family: landscape smoothing (Gu–Huang 1994), guided local search, the noising method; turn costs as in the angular-metric TSP; tour-geometry smoothing as in the elastic net.
