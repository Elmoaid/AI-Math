# AI-Math

Hobby project; the math was done by AI and re-checked by a second AI. Status stated on each item; no priority claims.

## 1. Complete geometric graphs on random points: a boundary-triangle constant

Take n random points in a smooth convex region, draw every segment between pairs, and look at the cells along the convex hull.

- Each hull edge borders exactly one bounded cell, and it is a triangle (elementary, proved).
- The expected total area of those triangles scales like n^(−2/3) with constant c_B = Γ(8/3)/12 · I = 0.0916946380…, where I is an explicit double integral. The classical missing-hull-area constant is c_M = 0.7886206526…, so the triangles take c_B/c_M = 0.11627… of the area the hull misses.
- Corollary: the Tukey depth ≥ 2 region misses, in expectation, 5/3 − c_B/c_M = 1.5503944924… times the area the hull misses (exact identity B = S₁ − U behind it).

Status: proved in the limit model (quadrature to 10 digits; independent Monte Carlo agrees to 0.2%); finite-n simulations at n = 512–8192 within 1%; finite-n transfer argument written but unrefereed. Parabolic scaling, c_M and Tukey-depth regions are classical; the constant itself was not found in the literature.

Attached: `proof_audit.pdf` (claim-by-claim status), `geometric_graph_boundary_proof_closure.pdf` (theorem and integral), plus two supporting reports.

## 2. A two-sided inradius bound for convex polygons

For a convex n-gon with area A, perimeter P and inradius r:

    r·P/2  ≤  A  ≤  r·P − n·tan(π/n)·r².

Lower equality: tangential polygons. Upper equality: regular n-gons and, for even n only, regular n-gons stretched parallel to a pair of opposite sides (every rectangle). Equivalent form: P² − 4·n·tan(π/n)·A ≥ (P − 2·n·tan(π/n)·r)², the polygonal analogue of Bonnesen's inequality.

Proof sketch: A = ½ Σ sᵢhᵢ with hᵢ ≥ r gives the lower bound. For the upper bound, with inner parallel bodies K₋ₜ, A = ∫₀ʳ P(K₋ₜ) dt and −dP/dt = 2 Σ tan(αᵢ/2) ≥ 2·n·tan(π/n) (Jensen, then at most n sides); integrate. Equality needs no side lost before t = r, equal exterior angles, and K₋ᵣ a point or (n even) a segment.

Status: nearest published results (Zeng–Dong, arXiv:2306.15208; Chouikha, arXiv:math/0103210) cover polygons circumscribed about or inscribed in a circle; this version is for any convex polygon. Likely folklore.

## 3. A heuristic tweak that didn't really work, measured properly

Adding a bending penalty λ·Σ |eᵢ||eᵢ₊₁|·sin(turnᵢ) to the tour length during 2-opt on random Euclidean instances, then removing it, was reported early on to "halve 2-opt's excess". Reimplemented and measured against LKH-3 optima on 400/200/200 instances at n = 35/70/140: it cuts plain 2-opt's excess by 3–19%, costs 2–3× the time, loses to equal-time restarts, and Or-opt beats it by 2–4×. Known family: landscape smoothing, guided local search, angular-metric turn costs.

