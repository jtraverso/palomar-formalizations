# My own research: details

[← Back to the list](../README.md)

## Affine profile reduction for fractional triangle packings in split graphs

Palomar: [PALOMAR-2026-10-28-000028](https://palomar-registry.org/entry.html?id=PALOMAR-2026-10-28-000028&version=2) (version 2) · code: [jtraverso/erdos81-fractional-split-profiles @ f8690bc](https://github.com/jtraverso/erdos81-fractional-split-profiles/tree/f8690bcba57bddc5deefd8626f5b07e0d63e6086) · [archived copy](https://github.com/PalomarArchive/jtraverso--erdos81-fractional-split-profiles--2f8b880d7704/tree/palomar/PALOMAR-2026-10-28-000028-v2/f8690bcba57bddc5deefd8626f5b07e0d63e6086)

**What is proved.** A Lean 4 / Mathlib formalization of the main result of the author's preprint "Affine Profile Reduction for Fractional Triangle Packings in Split Graphs" (Erdős #81 series, Paper I): for every finite split graph G on n vertices, |E(G)| − 2ν₃*(G) ≤ n²/6 + n/2, where ν₃* is the fractional triangle packing number (the maximum total weight of a nonnegative weighting of the triangles with load at most one on every edge). It is stated both for the paper's finite split model (clique Fin p, independent vertices, neighbourhoods) and for every split graph in Mathlib's SimpleGraph, with the definitions of split graphs and fractional triangle packings of two registered entries; the weaker bound n²/6 + n of the first edition is also included. The proof reduces the fractional packing problem to neighbourhood profiles and a three-variable linear program, using finite LP duality. Version 2 states the finite LP duality used in the series as results of its own, over ℝ (Farkas' lemma in inequality form and covering/packing strong duality, from this proof) and over ℚ (Farkas' lemma by Fourier–Motzkin elimination and strong duality for the rational packing LP, from the author's Paper V).

**Sources.**

* Juan Pablo Traverso Gianini, *Affine Profile Reduction for Fractional Triangle Packings in Split Graphs*, Erdős #81 series, Paper I, preprint v1.4 (19 October 2026), Theorem 1.1 and its finite consequence; deposited in the series collection on Zenodo (series concept DOI 10.5281/zenodo.21273143) and in github.com/jtraverso/erdos-81-chordal-clique-partitions. [doi:10.5281/zenodo.23478825](https://doi.org/10.5281/zenodo.23478825) · [free full text](https://doi.org/10.5281/zenodo.23478825) (Zenodo)
* Juan Pablo Traverso Gianini, *Colorability and Realizability (Erdős #81 series, Paper V)*, Erdős #81 series, Paper V, preprint 1.0, in the 32-PDF series collection on Zenodo; Lean sources in github.com/jtraverso/erdos-81-chordal-clique-partitions. [doi:10.5281/zenodo.23479507](https://doi.org/10.5281/zenodo.23479507) · [free full text](https://doi.org/10.5281/zenodo.23479507) (Zenodo)

<details><summary>Background references</summary>

* Julius Farkas, *Theorie der einfachen Ungleichungen*, Journal für die reine und angewandte Mathematik 124 (1902), 1–27. [doi:10.1515/crll.1902.124.1](https://doi.org/10.1515/crll.1902.124.1)

</details>

## Complete-split extremizers for the fractional triangle-cover deficit on chordal graphs

Palomar: [PALOMAR-2026-10-29-000004](https://palomar-registry.org/entry.html?id=PALOMAR-2026-10-29-000004&version=1) (version 1) · code: [jtraverso/erdos81-complete-split-extremizers @ 7961c3a](https://github.com/jtraverso/erdos81-complete-split-extremizers/tree/7961c3aba6062b03de3df28f42d339c1aec145d8) · [archived copy](https://github.com/PalomarArchive/jtraverso--erdos81-complete-split-extremizers--398c83aea952/tree/palomar/PALOMAR-2026-10-29-000004-v1/7961c3aba6062b03de3df28f42d339c1aec145d8)

**What is proved.** A Lean 4 / Mathlib formalization of the main result of the author's preprint "Complete-Split Extremizers for a Fractional Triangle-Cover Functional on Chordal Graphs" (Erdős #81 series, Paper II). For a finite simple graph G let τ₃*(G) be its fractional triangle cover number (the least total weight of a nonnegative weighting of vertex pairs giving every triangle weight at least one on its edges) and Φ_τ(G) = |E(G)| − 2τ₃*(G). For every n ≥ 1, every chordal graph on n vertices satisfies Φ_τ(G) ≤ ⌊(2n + 1)²/24⌋, and equality is attained by a complete-split graph K_p ∨ K̄_q with p + q = n (Theorem 1.2). Chordality and fractional triangle covers use the definitions of two registered entries.

**Sources.**

* Juan Pablo Traverso Gianini, *Complete-Split Extremizers for a Fractional Triangle-Cover Functional on Chordal Graphs*, Erdős #81 series, Paper II, preprint v1.3 (19 October 2026), Theorem 1.2; deposited in the series collection on Zenodo (series concept DOI 10.5281/zenodo.21273143) and in github.com/jtraverso/erdos-81-chordal-clique-partitions. [doi:10.5281/zenodo.23478825](https://doi.org/10.5281/zenodo.23478825) · [free full text](https://doi.org/10.5281/zenodo.23478825) (Zenodo)

## Linear-error clique partitions of split graphs

Palomar: [PALOMAR-2026-10-29-000006](https://palomar-registry.org/entry.html?id=PALOMAR-2026-10-29-000006&version=1) (version 1) · code: [jtraverso/erdos81-split-clique-partitions @ a98dfa4](https://github.com/jtraverso/erdos81-split-clique-partitions/tree/a98dfa413428b3c532174575a39f89eb32b268b8) · [archived copy](https://github.com/PalomarArchive/jtraverso--erdos81-split-clique-partitions--91b4db9f18d8/tree/palomar/PALOMAR-2026-10-29-000006-v1/a98dfa413428b3c532174575a39f89eb32b268b8)

**What is proved.** A Lean 4 / Mathlib formalization of the main results of the author's preprint "Linear-Error Clique Partitions of Split Graphs via Structured Triangle Packing" (Erdős #81 series, Paper III): there is an absolute constant C such that every finite split graph G on n vertices satisfies |E(G)| − 2ν₃(G) ≤ n²/6 + C·n, where ν₃(G) is the maximum number of pairwise edge-disjoint triangles (Theorem 1.1); consequently G has a clique partition (a family of cliques covering every edge exactly once) with at most n²/6 + C·n cliques (Corollary 1.2). The quadratic coefficient 1/6 is the sharp one for split graphs. The constant C is existential and not explicit. Two ingredients of the proof, the asymptotic gap between fractional and integral triangle packings and exact triangle decompositions of dense triangle-divisible graphs, are taken from two registered formalizations (see related_formalizations).

**Sources.**

* Juan Pablo Traverso Gianini, *Linear-Error Clique Partitions of Split Graphs via Structured Triangle Packing*, Erdős #81 series, Paper III, preprint v1.6 (19 October 2026), Theorem 1.1 and Corollary 1.2; deposited in the series collection on Zenodo (series concept DOI 10.5281/zenodo.21273143) and in github.com/jtraverso/erdos-81-chordal-clique-partitions. [doi:10.5281/zenodo.23478825](https://doi.org/10.5281/zenodo.23478825) · [free full text](https://doi.org/10.5281/zenodo.23478825) (Zenodo)

## Clique partitions of chordal graphs: quantitative stability and sharp eventual bounds

Palomar: [PALOMAR-2026-11-01-000021](https://palomar-registry.org/entry.html?id=PALOMAR-2026-11-01-000021&version=2) (version 2) · code: [jtraverso/erdos81-chordal-quantitative-stability @ 39104cf](https://github.com/jtraverso/erdos81-chordal-quantitative-stability/tree/39104cffdbc26ee96eeb9091d9f75bfecf6d540e) · [archived copy](https://github.com/PalomarArchive/jtraverso--erdos81-chordal-quantitative-stability--77dfe98a72ff/tree/palomar/PALOMAR-2026-11-01-000021-v2/39104cffdbc26ee96eeb9091d9f75bfecf6d540e)

**What is proved.** A Lean 4 / Mathlib formalization of the chordal results of the author's preprint "Clique partitions with rooted simplicial defect: quantitative stability and sharp eventual bounds" (Erdős #81 series, Paper IV). With M(n) = ⌊n(n+1)/6⌋: there is b such that every chordal graph on n vertices has a clique partition into pieces of order at most four with at most M(n) + b pieces (Theorem A); for n large every chordal graph on n vertices has one with at most M(n) pieces, and some chordal graph on n vertices has one with exactly M(n) pieces that is optimal among all clique partitions (Theorem B, the bound asked in Erdős Problem #81 and its sharpness); 1/6 is the least quadratic coefficient (§6.3); the uniform mixed rounding of fractional triangle/K₄ packings (Theorem 3.1); integral stability with explicit constants and edit distance at most 16δ to a complete-split graph, for 0 ≤ δ ≤ γn² with γ = 10⁻¹⁶/4 (Theorem 6.1); same-root control of near-optimal partitions: one clique root satisfies all the conclusions of Theorem 6.1 and, for it, every partition with at most M(n) + τ pieces has at most τ + 48δ noncanonical pieces (Corollary 6.1a); the root-defect identity (6.7b); and the eventual classification of the extremal chordal graphs as complete-split graphs with a core of optimal size (Corollary 6.2). Version 2 adds the fixed-defect results for graphs of rooted simplicial defect at most s: the sharp eventual bound Q_s(n) = M(n + s) − C(s + 1, 2), attained by a partition optimal among all clique partitions (Theorem C); same-root stability with A_s = 2·10⁴¹·(s + 1)⁸ for 0 ≤ δ ≤ γn², edit distance at most A_s δ, at most τ + (1 + 7A_s)δ noncanonical pieces carrying at most 10τ + 10(1 + 7A_s)δ edges (Theorem C′); comparison with an optimal-size template at distance at most A_s δ + n√((1 + 4A_s)δ) and the equality case cp = c₄ = Q_s(n) (Corollary 6.3); the necessity of the square-root term (Proposition 6.3a); the bounds F₄(G) ≤ M(n − s) + ns (minus C(s + 1, 2) when 4s ≤ n) and their integral form up to εn² (Proposition 6.4); the sublinear-defect bound n²/6 + o(n²) and root stability (Theorem 6.5); the bound Q_s(n) for all s ≤ S once n ≥ T(P(S)), an explicit tower (Corollary 6.6); and the annex inequality: a chordal K_{d+2}-free graph has fractional triangle packing number at most ν₃ + (10 + d/2)n (G.1). 21 statements. The thresholds N and γ in Theorems B, C, C′ and Corollary 6.3 are existential; b, N, A_s and the tower are not claimed optimal.

**Sources.**

* Juan Pablo Traverso Gianini, *Clique partitions with rooted simplicial defect: quantitative stability and sharp eventual bounds*, Erdős #81 series, Paper IV, preprint v1.24.1: Theorems A, B, C, C′, 3.1, 6.1 and 6.5, Corollaries 6.1a, 6.2, 6.3 and 6.6, Propositions 6.3a and 6.4, identity (6.7b), the optimality of the quadratic coefficient (§6.3) and inequality (G.1) of the bounded-clique-gap annex. In the series collection on Zenodo (series concept DOI 10.5281/zenodo.21273143) and in github.com/jtraverso/erdos-81-chordal-clique-partitions (preprints/PAPER_IV). [doi:10.5281/zenodo.23479507](https://doi.org/10.5281/zenodo.23479507) · [free full text](https://doi.org/10.5281/zenodo.23479507) (Zenodo)

<details><summary>Background references</summary>

* Obinna Okechukwu, *Clique partitions and bounded simplicial defect*, arXiv:2609.20871v1 (15 September 2026), Theorem 1.1 and Corollary 1.2. [free full text](https://arxiv.org/pdf/2609.20871) (arXiv)
* Anonymous (repository credits: Morluto, N0zoM1z0), *Clique partitions of chordal graphs with linear error*, Preprint of 8 September 2026, manuscript/main.pdf at commit cbde8a0a0563372b23b1b39a44180d2c0fb02f44.
* Paul Erdős, Edward T. Ordman, Yechezkel Zalcstein, *Clique partitions of chordal graphs*, Combinatorics, Probability and Computing 2 (1993) 409–415. [doi:10.1017/S0963548300000808](https://doi.org/10.1017/S0963548300000808)

</details>

## Colorability and realizability defects in resource-dominated packing relaxations

Palomar: [PALOMAR-2026-11-01-000020](https://palomar-registry.org/entry.html?id=PALOMAR-2026-11-01-000020&version=1) (version 1) · code: [jtraverso/erdos81-colorability-realizability-defects @ 0c2f7df](https://github.com/jtraverso/erdos81-colorability-realizability-defects/tree/0c2f7dff52e5c578f39191c4905dd12248e7bb9a) · [archived copy](https://github.com/PalomarArchive/jtraverso--erdos81-colorability-realizability-defects--59ae4ccb591d/tree/palomar/PALOMAR-2026-11-01-000020-v1/0c2f7dff52e5c578f39191c4905dd12248e7bb9a)

**What is proved.** A Lean 4 / Mathlib formalization of the main results of the author's preprint "Colorability and Realizability Defects in Resource-Dominated Packing Relaxations" (Erdős #81 series, Paper V). For a conflict system (finite objects with a symmetric irreflexive conflict relation) and a multiset X of objects, the loss between fractional and integral packings is bounded by the colourability defect D_q of the conflict graph H[X] of the copies (Lemma 3.1, Corollary 3.2, Theorems 3.3, 3.4, 3.4w), and, more generally, by the cost of a realizability certificate whose classes are realized in a fixed target system (Theorems 4.2 and 4.4). Applications: host completion through list edge colouring of bipartite multigraphs (Theorem 5.2: Galvin and Borodin–Kostochka–Woodall; Corollary 5.3; Example 5.5, a quadratic separation on K_{r,r}), the vertex-copy inequalities ν₃*(G_{v→u}) + ν₃*(G_{u→v}) ≤ 2ν₃*(G), ν₃(G_{v→u}) + ν₃(G_{u→v}) ≤ 2ν₃(G) + oct(H[T₂]) and ≤ 3ν₃(G) for triangle packings (Theorems 6.1, 6.2, Corollary 6.2a) and mixed triangle/K₄ copy inequalities (Theorem 7.3). Eighteen statements in all.

**Sources.**

* Juan Pablo Traverso Gianini, *Colorability and Realizability Defects in Resource-Dominated Packing Relaxations*, Erdős #81 series, Paper V, preprint 1.0 (18 October 2026): Lemma 3.1, Corollary 3.2, Theorems 3.3, 3.4, 3.4w, 4.2, 4.4, 5.2, Corollary 5.3, Example 5.5, Theorems 6.1, 6.2, Corollary 6.2a and Theorem 7.3. In the series collection on Zenodo (series concept DOI 10.5281/zenodo.21273143) and in github.com/jtraverso/erdos-81-chordal-clique-partitions (preprints/PAPER_V/01_manuscript/PAPER_V_preprint_v1.0_en.pdf). [doi:10.5281/zenodo.23479507](https://doi.org/10.5281/zenodo.23479507) · [free full text](https://doi.org/10.5281/zenodo.23479507) (Zenodo)

<details><summary>Background references</summary>

* Fred Galvin, *The list chromatic index of a bipartite multigraph*, J. Combin. Theory Ser. B 63 (1995) 153–158. [doi:10.1006/jctb.1995.1011](https://doi.org/10.1006/jctb.1995.1011) · [free full text](https://doi.org/10.1006/jctb.1995.1011)
* O. V. Borodin, A. V. Kostochka, D. R. Woodall, *List edge and list total colourings of multigraphs*, J. Combin. Theory Ser. B 71 (1997) 184–204. [doi:10.1006/jctb.1997.1780](https://doi.org/10.1006/jctb.1997.1780) · [free full text](https://doi.org/10.1006/jctb.1997.1780)

</details>

## Optimal clique partitions under local perturbations

Palomar: [PALOMAR-2026-11-01-000006](https://palomar-registry.org/entry.html?id=PALOMAR-2026-11-01-000006&version=1) (version 1) · code: [jtraverso/erdos81-optimal-clique-partitions @ 719e39b](https://github.com/jtraverso/erdos81-optimal-clique-partitions/tree/719e39baf9d0e356a13f6bfe36b60b4ad5e910d6) · [archived copy](https://github.com/PalomarArchive/jtraverso--erdos81-optimal-clique-partitions--2ba058ab4ee3/tree/palomar/PALOMAR-2026-11-01-000006-v1/719e39baf9d0e356a13f6bfe36b60b4ad5e910d6)

**What is proved.** A Lean 4 / Mathlib formalization of the main results of the author's preprint "Optimal Clique Partitions under Local Perturbations" (Erdős #81 series, Paper VI). For a graph G on n vertices with a core P of size p = ⌊(n+1)/3⌋, h = Δ(G △ (K_P ∨ I_O)) and u, s, m the numbers of core, crossing and exterior edges: if p ≥ 18h + 1 then cp(G) = cp_{≤4}(G) = s − u − 2m = M(n) + C − A − 2m with M(n) = ⌊n(n+1)/6⌋ (Theorem A), and cp_{≤3}(G) − cp(G) = m (Theorem B); if p ≥ 63h, every assignment of the orders 4 or 5 to the exterior edges is realized by an optimal partition (Theorem C); for p ≥ 16 each assignment has at least p^{⌊p²/64⌋} optimal partitions and 2^m p^{⌊p²/64⌋} ≤ N(G) ≤ (n+1)^{5e(G)} (Theorem E). Also: the formula for other core sizes in an explicit window (Proposition 2.1), the intrinsic maximum over all cores (§8.1), the exact optimum with one exceptional vertex, cp = cp_{≤4} = cp*_= = s − u − 2m + D(a,b), ν₃ = ν₃* = u + min(a,b) and the restriction gap (Theorem D), and the complete-join variant cp(G) = M(n) − 2m (Theorem A.1). Twelve statements in all. The constants 18, 63, 16 and 24 are those of the paper; their optimality is not claimed.

**Sources.**

* Juan Pablo Traverso Gianini, *Optimal Clique Partitions under Local Perturbations*, Erdős #81 series, Paper VI, preprint 1.0: Theorems A, B, C, D, E and A.1, Proposition 2.1 and the intrinsic formula of §8.1. In the series collection on Zenodo (series concept DOI 10.5281/zenodo.21273143) and in github.com/jtraverso/erdos-81-chordal-clique-partitions (preprints/PAPER_VI/01_manuscript/PAPER_VI_preprint_v1.0_en.pdf). [doi:10.5281/zenodo.23479507](https://doi.org/10.5281/zenodo.23479507) · [free full text](https://doi.org/10.5281/zenodo.23479507) (Zenodo)

<details><summary>Background references</summary>

* Paul Erdős, Ralph J. Faudree, Edward T. Ordman, *Clique partitions and clique coverings*, Discrete Mathematics 72 (1988) 93–101. [doi:10.1016/0012-365X(88)90197-5](https://doi.org/10.1016/0012-365X(88)90197-5) · [free full text](https://doi.org/10.1016/0012-365x(88)90197-5)

</details>

## Two application notes of the Erdős #81 series: realizability transfer and exact chordal stability

Palomar: [PALOMAR-2026-11-01-000022](https://palomar-registry.org/entry.html?id=PALOMAR-2026-11-01-000022&version=1) (version 1) · code: [jtraverso/erdos81-series-notes @ 01be11e](https://github.com/jtraverso/erdos81-series-notes/tree/01be11e33fc4f416d5ef5df4d71aec936bc48023) · [archived copy](https://github.com/PalomarArchive/jtraverso--erdos81-series-notes--4dbca61df10f/tree/palomar/PALOMAR-2026-11-01-000022-v1/01be11e33fc4f416d5ef5df4d71aec936bc48023)

**What is proved.** A Lean 4 / Mathlib formalization of the two research notes of the author's Erdős #81 series, in one package. Note I, "From realizability certificates to the Erdős 81 bound": a realizability certificate of Paper V for an auxiliary conflict system whose target is the physical system of copies of K₃ and K₄ in G (conflict when they share an edge, gain C(|K|,2) − 1), with q ≥ 1 classes and budget q·e(G) + cost ≤ q·T + w(X), gives a clique partition of G into pieces of order at most four with at most T pieces (note_I_partition_of_certificate; no chordality); a physical packing with e(G) − g(P) ≤ T does the same (note_I_partition_of_paid_packing); with a certified fractional optimum w, the far branch (e(G) − w < n²/6 − ηn², every η > 0, large n, no chordality) and the near branch (chordal, n ≥ 4·10¹², η = 10⁻¹⁶) give partitions with at most M(n) = ⌊n(n+1)/6⌋ pieces (note_I_far_certificate, note_I_near_certificate); assembled through the transfer, every large chordal graph has such a partition (note_I_erdos81_eventual) and every chordal graph one with at most M(n) + b pieces for an absolute b (note_I_erdos81_all_orders). Note II, "Exact stability for nearly extremal chordal clique partitions": for n large, every chordal graph on n vertices with cp(G) ≤ M(n) and 2000 (M(n) − cp(G)) ≤ n has the root P = {v : n < 2 deg v}, which is a clique, with cp(G) = B(n,|P|) − A − 2m = cp_{≤4}(G), M − cp = (M − B) + A + 2m, edit distance to K_P ∨ I_O equal to A + m and at most M − cp, and (6|P| − 2n − 1)² ≤ 24(M − cp) + 25 (note_II_eventual_root_stability). Seven statements; the thresholds N and the constant b are existential.

**Sources.**

* Juan Pablo Traverso Gianini, *From realizability certificates to the Erdős 81 bound*, Erdős #81 series, research note I, version 1.0 (18 October 2026); formal companion v0.4 (the six public interfaces of §3). In github.com/jtraverso/erdos-81-chordal-clique-partitions (series_notes/NOTE_I_ERDOS81_TRANSFER). [doi:10.5281/zenodo.23458871](https://doi.org/10.5281/zenodo.23458871) · [free full text](https://doi.org/10.5281/zenodo.23458871) (Zenodo)
* Juan Pablo Traverso Gianini, *Exact stability for nearly extremal chordal clique partitions*, Erdős #81 series, research note II, version 1.0 (18 October 2026); formal companion v0.3 (public endpoint eventual_root_stability). In github.com/jtraverso/erdos-81-chordal-clique-partitions (series_notes/NOTE_II_CHORDAL_STABILITY). [doi:10.5281/zenodo.23458871](https://doi.org/10.5281/zenodo.23458871) · [free full text](https://doi.org/10.5281/zenodo.23458871) (Zenodo)

## The Nash–Williams triangle-decomposition theorem

Palomar: [PALOMAR-2026-10-21-000009](https://palomar-registry.org/entry.html?id=PALOMAR-2026-10-21-000009&version=1) (version 1) · code: [jtraverso/nash-williams-lean @ 2603197](https://github.com/jtraverso/nash-williams-lean/tree/2603197abdbf0a600ec663f6f046f70fbd209d4a) · [archived copy](https://github.com/PalomarArchive/jtraverso--nash-williams-lean--252fc7828395/tree/palomar/PALOMAR-2026-10-21-000009-v1/2603197abdbf0a600ec663f6f046f70fbd209d4a)

**What is proved.** A Lean 4 / Mathlib formalization of the Nash–Williams theorem for large graphs proved by Delcourt and Postle: there is N such that every finite simple graph on n ≥ N vertices that is triangle-divisible (3 divides the number of edges and every degree is even) and has minimum degree at least 3n/4 has a triangle decomposition; together with Delcourt–Postle's fractional threshold (every graph with 3n ≤ 4δ has a fractional triangle decomposition) and their fractional stability theorem (with an additional order threshold). The proof follows their extremal/non-extremal case division but does not assume their Theorem 13.16, whose proof is assigned to an unpublished manuscript: the extremal residuals are decomposed with typed absorption results developed in the same project, and the non-extremal case with a protected covering-round argument. The development has 1,070 modules.

**Sources.**

* Juan Pablo Traverso Gianini, *Triangle decompositions I: Formalizing the Nash–Williams theorem in Lean*, Preprint 1.0 (2026). [doi:10.5281/zenodo.23428173](https://doi.org/10.5281/zenodo.23428173) · [free full text](https://doi.org/10.5281/zenodo.23428173) (Zenodo)
* Juan Pablo Traverso Gianini, *Triangle decompositions II: Robust absorption for typed triangles*, Preprint 1.0 (2026). [doi:10.5281/zenodo.23502224](https://doi.org/10.5281/zenodo.23502224) · [free full text](https://doi.org/10.5281/zenodo.23502224) (Zenodo)
* Michelle Delcourt, Luke Postle, *A Proof of Nash-Williams' Conjecture*, arXiv:2606.11178 (2026), Theorems 1.4, 1.6 and 1.8. [doi:10.48550/arXiv.2606.11178](https://doi.org/10.48550/arXiv.2606.11178) · [free full text](https://arxiv.org/pdf/2606.11178) (arXiv)

<details><summary>Background references</summary>

* C. St. J. A. Nash-Williams, *An unsolved problem concerning decomposition of graphs into triangles*, Combinatorial Theory and its Applications III, North-Holland (1970), 1179–1183.

</details>

## Robust absorption for typed triangles (Triangle decompositions II)

Palomar: [PALOMAR-2026-10-23-000013](https://palomar-registry.org/entry.html?id=PALOMAR-2026-10-23-000013&version=1) (version 1) · code: [jtraverso/typed-triangle-absorption @ 673c6d4](https://github.com/jtraverso/typed-triangle-absorption/tree/673c6d4118b5679783bafa7606fd2c611161a254) · [archived copy](https://github.com/PalomarArchive/jtraverso--typed-triangle-absorption--055c1b37404f/tree/palomar/PALOMAR-2026-10-23-000013-v1/673c6d4118b5679783bafa7606fd2c611161a254)

**What is proved.** Typed triangle decomposition results from Paper II: a typical-host theorem under three-step links for four-label families; its nearly complete and balanced deductions with explicit type-weight hypotheses; a semidense two-label mixed-triangle theorem; a computer-assisted typical-host theorem for every admissible four-label family; and a terminal absorber obtained from a bounded signed certificate and explicit physical hinge supply. Divisibility includes global edge counts and local degree profiles. The typical-host hypotheses are retained; the result is not asserted for arbitrary divisible hosts. The repository contains the substantive proof development, including the finite family census and conserved-family constructions, with a small independent Mathlib-only Challenge.

**Sources.**

* Juan Pablo Traverso Gianini, *Triangle decompositions II: Robust absorption for typed triangles*, Preprint 1.0, 20 October 2026; Theorems A–D, balanced consequence of B and Lemma SC. [doi:10.5281/zenodo.23502224](https://doi.org/10.5281/zenodo.23502224) · [free full text](https://doi.org/10.5281/zenodo.23502224) (Zenodo)

<details><summary>Background references</summary>

* Peter Keevash, *The existence of designs II*, arXiv:1802.05900, Theorem 3.1. [doi:10.48550/arXiv.1802.05900](https://doi.org/10.48550/arXiv.1802.05900) · [free full text](https://arxiv.org/pdf/1802.05900) (arXiv)
* Michelle Delcourt, Luke Postle, *Refined Absorption: A New Proof of the Existence Conjecture*, arXiv:2402.17855. [doi:10.48550/arXiv.2402.17855](https://doi.org/10.48550/arXiv.2402.17855) · [free full text](https://arxiv.org/pdf/2402.17855) (arXiv)
* Michelle Delcourt, Luke Postle, *A Proof of Nash-Williams' Conjecture*, arXiv:2606.11178, partitioned residual applications. [doi:10.48550/arXiv.2606.11178](https://doi.org/10.48550/arXiv.2606.11178) · [free full text](https://arxiv.org/pdf/2606.11178) (arXiv)
* Ben Barber, Daniela Kühn, Allan Lo, Deryk Osthus, Amelia Taylor, *Clique decompositions of multipartite graphs and completion of Latin squares*, Journal of Combinatorial Theory, Series A 151 (2017). [doi:10.1016/j.jcta.2017.04.005](https://doi.org/10.1016/j.jcta.2017.04.005) · [free full text](https://www.sciencedirect.com/science/article/pii/S0097316517300432/pdf)

</details>

## Triangle decompositions III: physical typed absorption and prescribed statistics

Palomar: [PALOMAR-2026-11-03-000012](https://palomar-registry.org/entry.html?id=PALOMAR-2026-11-03-000012&version=1) (version 1) · code: [jtraverso/physical-typed-absorption @ 9d36e80](https://github.com/jtraverso/physical-typed-absorption/tree/9d36e80d75d81d9eabbfacd370dc4394b54e3d52) · [archived copy](https://github.com/PalomarArchive/jtraverso--physical-typed-absorption--5ba06d9516d5/tree/palomar/PALOMAR-2026-11-03-000012-v1/9d36e80d75d81d9eabbfacd370dc4394b54e3d52)

**What is proved.** The Lean source supplement of Paper III of the Nash-Williams series (preprint 1.0), packaged with a Mathlib-only Challenge. Theorem T: for fixed labels I, allowed label multisets F and constants alpha > 0, C >= 1, h >= 6, every labelled graph of order at least n0 that has an exact diffuse fractional triangle seed of constant C (H1), whose edge indicator lies in the integer lattice spanned by its allowed triangles (H2), with at least alpha n common neighbours labelled k for every pair of distinct vertices and every label k completing an allowed type (H3), and at least alpha n^(i-4) physical hinges of some order 6 <= i <= h for every pair of allowed triangles on a common edge (H4), has an allowed triangle decomposition. Theorem T+: for every eta > 0 and q the decomposition can moreover be chosen so that every family of at most n^q triangle tests bounded by 1, and the Pasch count, are within eta n^2 of their values under the seed. Applications: Latin squares following a bounded stochastic profile with prescribed statistics and Pasch count (Theorem 8.1), the uniform and signed rank-one profiles with their intercalate counts (Corollaries 8.2 and 8.3), two Latin squares each of which separately approximates, up to eps m^2, the same prescribed statistics and the same eight coarse-block targets (their own values need not coincide), with intercalate counts near different targets (Theorem 8.4, m divisible by four), and the balanced complete five-partite graph with parts of size 3|A| and rainbow triangles (Corollary 8.5). Seven statements. All thresholds are existential; the explicit tower bound of Section 7 is not compared.

**Sources.**

* Juan Pablo Traverso Gianini, *Triangle decompositions III: Physical typed absorption and prescribed statistics*, Preprint 1.0, 1 November 2026; Theorems T, T+, 8.1, 8.4 and Corollaries 8.2, 8.3, 8.5. [doi:10.5281/zenodo.23867836](https://doi.org/10.5281/zenodo.23867836) · [free full text](https://doi.org/10.5281/zenodo.23867836) (Zenodo)

<details><summary>Background references</summary>

* Michelle Delcourt, Luke Postle, *A Proof of Nash-Williams' Conjecture*, arXiv:2606.11178v1, Section 13.2: Definition 13.14 and Theorem 13.16. [doi:10.48550/arXiv.2606.11178](https://doi.org/10.48550/arXiv.2606.11178) · [free full text](https://arxiv.org/pdf/2606.11178) (arXiv)
* Juan Pablo Traverso Gianini, *Triangle decompositions II: Robust absorption for typed triangles*, Preprint 1.0, 20 October 2026. [doi:10.5281/zenodo.23502224](https://doi.org/10.5281/zenodo.23502224) · [free full text](https://doi.org/10.5281/zenodo.23502224) (Zenodo)
* Stefan Ehard, Stefan Glock, Felix Joos, *Pseudorandom hypergraph matchings*, Combinatorics, Probability and Computing 29 (2020), Theorem 1.2. [doi:10.1017/S0963548320000280](https://doi.org/10.1017/S0963548320000280) · [free full text](https://www.cambridge.org/core/services/aop-cambridge-core/content/view/AE0DE17C95900E7DD3F221E2C17FE203/S0963548320000280a.pdf/div-class-title-pseudorandom-hypergraph-matchings-div.pdf)

</details>

## Formalizing Delcourt–Postle’s refined absorption in Lean

Palomar: [PALOMAR-2026-10-29-000005](https://palomar-registry.org/entry.html?id=PALOMAR-2026-10-29-000005&version=1) (version 1) · code: [jtraverso/refined-absorption-lean @ 5bfe5c7](https://github.com/jtraverso/refined-absorption-lean/tree/5bfe5c7346a7b245581152dccebe363e22f072b6) · [archived copy](https://github.com/PalomarArchive/jtraverso--refined-absorption-lean--6accc6d51192/tree/palomar/PALOMAR-2026-10-29-000005-v1/5bfe5c7346a7b245581152dccebe363e22f072b6)

**What is proved.** One assembled Lean formalization of principal refined absorption results and their consequences. The selected results include refined omni-absorbers and refiners, labelled reserve matchings, dense compatible decompositions, an additive compatible-absorber interface retaining independence of the entire old ambient vertex set, and existence of simple designs for every fixed q > r ≥ 2 and index λ ≥ 1 at all sufficiently large admissible orders. The literal global embedding conclusion of the survey is refuted separately from a proved piecewise replacement. The research-note endpoints give completion avoiding an arbitrary forbidden partial Steiner system, sparse prescribed and finite embedded exact intersections, an initial polynomial intersection interval, and polynomial excess in partial parallel classes and Nash–Williams schedule rounds. Both external inputs are supplied by pinned proved theorems. The single comparison selects eighteen declarations from the existing aggregate proof root.

**Sources.**

* Juan Pablo Traverso Gianini, *Formalizing Delcourt–Postle’s refined absorption in Lean*, Research note, version 1.0.1 (2026); editorial update, unchanged proof sources. [doi:10.5281/zenodo.23715622](https://doi.org/10.5281/zenodo.23715622) · [free full text](https://doi.org/10.5281/zenodo.23715622) (Zenodo)
* Michelle Delcourt, Luke Postle, *Refined Absorption: A New Proof of the Existence Conjecture*, arXiv:2402.17855v1 (2024). [doi:10.48550/arXiv.2402.17855](https://doi.org/10.48550/arXiv.2402.17855) · [free full text](https://arxiv.org/pdf/2402.17855) (arXiv)
* Luke Postle, *Refined Absorption: A New Proof of the Existence Conjecture and Its Applications to Extremal and Probabilistic Design Theory*, ICM 2026, Volume 6, pp. 212–231; statement baseline arXiv:2510.19978v1. [doi:10.1137/25M1805977](https://doi.org/10.1137/25M1805977) · [free full text](https://arxiv.org/pdf/2510.19978) (arXiv)
* Stefan Ehard, Stefan Glock, Felix Joos, *Pseudorandom hypergraph matchings*. [doi:10.1017/S0963548320000280](https://doi.org/10.1017/S0963548320000280) · [free full text](https://www.cambridge.org/core/services/aop-cambridge-core/content/view/AE0DE17C95900E7DD3F221E2C17FE203/S0963548320000280a.pdf/div-class-title-pseudorandom-hypergraph-matchings-div.pdf)
* Michelle Delcourt, Luke Postle, *A Proof of Nash-Williams' Conjecture*. [doi:10.48550/arXiv.2606.11178](https://doi.org/10.48550/arXiv.2606.11178) · [free full text](https://arxiv.org/pdf/2606.11178)

<details><summary>Background references</summary>

* Nicholas Pippenger, Joel Spencer, *Asymptotic behavior of the chromatic index for hypergraphs*. [doi:10.1016/0097-3165(89)90074-5](https://doi.org/10.1016/0097-3165(89)90074-5) · [free full text](https://doi.org/10.1016/0097-3165(89)90074-5)
* Juan Pablo Traverso Gianini, *Triangle decompositions I: Formalizing the Nash–Williams theorem in Lean*. [doi:10.5281/zenodo.23428173](https://doi.org/10.5281/zenodo.23428173) · [free full text](https://doi.org/10.5281/zenodo.23428173) (Zenodo)
* Juan Pablo Traverso Gianini, *Triangle decompositions II: Robust absorption for typed triangles*. [doi:10.5281/zenodo.23502224](https://doi.org/10.5281/zenodo.23502224) · [free full text](https://doi.org/10.5281/zenodo.23502224) (Zenodo)
* C. C. Lindner, A. Rosa, *Steiner triple systems having a prescribed number of triples in common*. [doi:10.4153/CJM-1975-122-4](https://doi.org/10.4153/CJM-1975-122-4) · [free full text](https://www.cambridge.org/core/services/aop-cambridge-core/content/view/5B533F54045455CC7CE648B8E0B664F4/S0008414X00016473a.pdf/div-class-title-steiner-triple-systems-having-a-prescribed-number-of-triples-in-common-div.pdf)
* C. C. Lindner, A. Rosa, *Steiner triple systems having a prescribed number of triples in common (corrigendum)*, Canadian Journal of Mathematics 30 (1978), p. 896. [doi:10.4153/CJM-1978-077-9](https://doi.org/10.4153/CJM-1978-077-9) · [free full text](https://www.cambridge.org/core/services/aop-cambridge-core/content/view/00B5A6BBCBA1BCAA72FAE07054AE5E15/S0008414X00028030a.pdf/div-class-title-steiner-triple-systems-having-a-prescribed-number-of-triples-in-common-corrigendum-div.pdf)
* Michelle Delcourt, Cicely (Cece) Henderson, Thomas Lesgourgues, Luke Postle, *Erdős meets Nash-Williams*, arXiv:2507.23624v1, Appendix B. [doi:10.48550/arXiv.2507.23624](https://doi.org/10.48550/arXiv.2507.23624) · [free full text](https://arxiv.org/pdf/2507.23624) (arXiv)

</details>

## The Colbourn–Dinitz–Rosa conjecture and the exact block-type spectrum

Palomar: [PALOMAR-2026-11-07-000002](https://palomar-registry.org/entry.html?id=PALOMAR-2026-11-07-000002&version=1) (version 1) · code: [jtraverso/cdr-palomar-kernel @ 5d1e6fe](https://github.com/jtraverso/cdr-palomar-kernel/tree/5d1e6fe301e5fc01c92f6145aa34fddfe9c2bd10) · [archived copy](https://github.com/PalomarArchive/jtraverso--cdr-palomar-kernel--853fb49173b4/tree/palomar/PALOMAR-2026-11-07-000002-v1/5d1e6fe301e5fc01c92f6145aa34fddfe9c2bd10)

**What is proved.** A Lean 4 formalization of two results on strictly 3-bicolored Steiner triple systems. For every positive triple of class sizes a,b,c, existence is equivalent to n=a+b+c being 1 or 3 modulo 6, the identity a²+b²+c²-ab-ac-bc=n, and the exclusion of two classes of size 2. For every sufficiently large admissible profile, the number of AAC blocks is characterized exactly by two explicit arithmetic tests. The first result settles the class-size conjecture posed by Colbourn, Dinitz and Rosa in 1999; the second applies the typed absorption theorems of Triangle decompositions III. Both statements are compared in one shared development.

**Sources.**

* Juan Pablo Traverso Gianini, *The CDR class-size characterization and exact block-type spectrum*.
* Juan Pablo Traverso Gianini, *A proof of the Colbourn–Dinitz–Rosa conjecture*, https://doi.org/10.5281/zenodo.23987256. [doi:10.5281/zenodo.23987256](https://doi.org/10.5281/zenodo.23987256) · [free full text](https://doi.org/10.5281/zenodo.23987256) (Zenodo)
* Juan Pablo Traverso Gianini, *The exact block-type spectrum in the Colbourn–Dinitz–Rosa problem*, https://doi.org/10.5281/zenodo.23987251. [doi:10.5281/zenodo.23987251](https://doi.org/10.5281/zenodo.23987251) · [free full text](https://doi.org/10.5281/zenodo.23987251) (Zenodo)
* Juan Pablo Traverso Gianini, *Triangle decompositions III: Physical typed absorption and prescribed statistics*. [doi:10.5281/zenodo.23867836](https://doi.org/10.5281/zenodo.23867836) · [free full text](https://doi.org/10.5281/zenodo.23867836) (Zenodo)
* Charles J. Colbourn, Jeffrey H. Dinitz, Alexander Rosa, *Bicoloring Steiner triple systems*. [doi:10.37236/1457](https://doi.org/10.37236/1457) · [free full text](https://www.combinatorics.org/ojs/index.php/eljc/article/download/v6i1r25/pdf)

[← Back to the list](../README.md)
