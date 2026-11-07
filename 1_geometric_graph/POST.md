# Complete geometric graphs on random points: a boundary-triangle constant

Draw all segments between n random points in a smooth convex region and look at the cells along the hull.

**What's in the attachments**

- Each hull edge borders exactly one bounded cell, a triangle (elementary, proved).
- The expected total area of those triangles scales like n^(−2/3) with constant c_B = Γ(8/3)/12 · I = 0.0916946380…, I an explicit double integral; the classical missing-hull-area constant is c_M = 0.7886206526…, so the triangles asymptotically occupy c_B/c_M = 0.11627… of the missing area.
- Corollary: the region of Tukey depth ≥ 2 misses, in expectation, 5/3 − c_B/c_M = 1.5503944924… times the area the hull misses. Exact identity B = S₁ − U behind it.
- The interior local limit (anisotropic Poisson line process, with moment convergence); classical in substance.

**Status.** Proved in the limit model (quadrature to 10 digits; independent Monte Carlo agrees to 0.2%); finite-n simulations at n = 512–8192 within 1%; finite-n transfer argument written but unrefereed. Parabolic scaling, c_M and Tukey-depth regions are classical; the constant itself was not found in the literature.

**Attached:** `proof_audit.pdf` (claim-by-claim status), `geometric_graph_boundary_proof_closure.pdf` (the theorem and the integral), `geometric_graph_boundary_report.pdf`, `geometric_graph_local_limit_report.pdf`.
