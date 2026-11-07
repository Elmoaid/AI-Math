# A two-sided inradius bound for convex polygons (short note)

Nearest published results (Zeng–Dong, arXiv:2306.15208; Chouikha, arXiv:math/0103210; Zhang 1997) cover polygons circumscribed about or inscribed in a circle; this version is for any convex polygon with inradius r. Likely folklore.

For a convex n-gon with area A, perimeter P and inradius r:

    r·P/2  ≤  A  ≤  r·P − n·tan(π/n)·r².

Lower equality: tangential polygons. Upper equality: regular n-gons and, for even n only, regular n-gons stretched parallel to a pair of opposite sides (every rectangle). Equivalent form of the upper bound: P² − 4·n·tan(π/n)·A ≥ (P − 2·n·tan(π/n)·r)², the polygonal analogue of Bonnesen's L² − 4πA ≥ (L − 2πr)².

**Proof.** Lower: A = ½ Σ sᵢhᵢ with every hᵢ ≥ r. Upper: for the inner parallel bodies K₋ₜ, A = ∫₀ʳ P(K₋ₜ) dt and −dP/dt = 2 Σ tan(αᵢ/2) ≥ 2·m·tan(π/m) ≥ 2·n·tan(π/n) (Jensen, then m ≤ n sides), so P(K₋ₜ) ≤ P − 2·n·tan(π/n)·t; integrate. Equality needs no side lost before t = r, equal exterior angles, and K₋ᵣ a point or (n even) a segment.
