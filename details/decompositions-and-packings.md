# Decompositions and packings: details

[← Back to the list](../README.md)

## Dross's theorem on fractional triangle decompositions

Palomar: [PALOMAR-2026-10-15-000008](https://palomar-registry.org/entry.html?id=PALOMAR-2026-10-15-000008&version=1) (version 1) · code: [jtraverso/dross-fractional-triangle-decomposition @ 7720b7b](https://github.com/jtraverso/dross-fractional-triangle-decomposition/tree/7720b7b591e606d5a56f1d935d8be650dcbf6c6f) · [archived copy](https://github.com/PalomarArchive/jtraverso--dross-fractional-triangle-decomposition--f57504b1525c/tree/palomar/PALOMAR-2026-10-15-000008-v1/7720b7b591e606d5a56f1d935d8be650dcbf6c6f)

**What is proved.** A Lean 4 / Mathlib formalization of Dross's theorem: every finite graph on n vertices with minimum degree at least 9n/10 has a fractional triangle decomposition, i.e. nonnegative real weights on its triangles such that every edge lies in triangles of total weight exactly one. The threshold 9/10 is the exact one of the paper. The proof follows the max-flow/min-cut approach: the existence of the weights is reduced to a flow problem, a finite max-flow/min-cut theorem (included) is applied, and every cut is bounded below by counting triangles and K4s, with a peeling reduction for heavy triangles.

**Sources.**

* François Dross, *Fractional Triangle Decompositions in Graphs with Large Minimum Degree*, SIAM Journal on Discrete Mathematics 30 (2016), no. 1, 36–42. [doi:10.1137/15M1014310](https://doi.org/10.1137/15M1014310) · [free full text](https://hal-lirmm.ccsd.cnrs.fr/lirmm-01336680v1/document)

## Near-regular hypergraph matchings and the asymptotic triangle-packing gap

Palomar: [PALOMAR-2026-10-15-000011](https://palomar-registry.org/entry.html?id=PALOMAR-2026-10-15-000011&version=2) (version 2) · code: [jtraverso/asymptotic-triangle-packing @ 760e503](https://github.com/jtraverso/asymptotic-triangle-packing/tree/760e503972aad8ca9da7904ce72e5cce405f5991) · [archived copy](https://github.com/PalomarArchive/jtraverso--asymptotic-triangle-packing--a2c3300bc8ff/tree/palomar/PALOMAR-2026-10-15-000011-v2/760e503972aad8ca9da7904ce72e5cce405f5991)

**What is proved.** A Lean 4 / Mathlib formalization of four results. (1) A finite nibble theorem: r-uniform hypergraphs whose degrees are at most (1+μ)d everywhere and at least (1−μ)d outside an exceptional set of at most η|V| vertices, with codegrees at most μd, have matchings with at least (1−β)|V|/r edges. (2) The fractional–integral triangle-packing gap is o(n²) uniformly over finite graphs: every large graph has an edge-disjoint triangle family P such that every fractional triangle packing has weight at most |P| + εn² (the triangle case of Haxell–Rödl). (3) The cover form: a fractional triangle cover of weight at most |P| + εn² exists. (4) Version 2, the transfer form used in decomposition theory: every large graph on n vertices that has a fractional triangle decomposition has an edge-disjoint triangle family covering all but at most ηn² edges; it follows from (2), since a fractional decomposition is a fractional packing of weight e(G)/3 and a packing P covers exactly 3|P| edges. The proof of (1)–(3) combines a nibble with second-moment and Freedman-type concentration, a low-degree core reduction, Mathlib's Szemerédi regularity lemma with a cluster linear program rounded by explicit designs, and LP duality.

**Sources.**

* P. E. Haxell, V. Rödl, *Integer and fractional packings in dense graphs*, Combinatorica 21 (2001), no. 1, 13–38. [doi:10.1007/s004930170003](https://doi.org/10.1007/s004930170003)

<details><summary>Background references</summary>

* Raphael Yuster, *Integer and fractional packing of families of graphs*, Random Structures & Algorithms 26 (2005), no. 1–2, 110–118. [doi:10.1002/rsa.20048](https://doi.org/10.1002/rsa.20048) · [free full text](https://arxiv.org/pdf/math/0305350)
* P. Frankl, V. Rödl, *Near perfect coverings in graphs and hypergraphs*, European Journal of Combinatorics 6 (1985), no. 4, 317–326. [doi:10.1016/S0195-6698(85)80045-7](https://doi.org/10.1016/S0195-6698(85)80045-7) · [free full text](https://doi.org/10.1016/s0195-6698(85)80045-7)
* Nicholas Pippenger, Joel Spencer, *Asymptotic behavior of the chromatic index for hypergraphs*, Journal of Combinatorial Theory, Series A 51 (1989), no. 1, 24–42. [doi:10.1016/0097-3165(89)90074-5](https://doi.org/10.1016/0097-3165(89)90074-5) · [free full text](https://doi.org/10.1016/0097-3165(89)90074-5)
* Juan Pablo Traverso Gianini, *Linear-Error Clique Partitions of Split Graphs via Structured Triangle Packing (Paper III of the preprint series)*, GitHub repository jtraverso/erdos-81-chordal-clique-partitions, preprints/PAPER_III.
* Ben Barber, Daniela Kühn, Allan Lo, Deryk Osthus, Amelia Taylor, *Clique decompositions of multipartite graphs and completion of Latin squares*, Journal of Combinatorial Theory, Series A 151 (2017), 146–201; arXiv:1603.01043. [doi:10.1016/j.jcta.2017.04.005](https://doi.org/10.1016/j.jcta.2017.04.005) · [free full text](https://arxiv.org/pdf/1603.01043) (arXiv)

</details>

## The Nash-Williams–Tutte tree packing theorem and Nash-Williams' arboricity theorem

Palomar: [PALOMAR-2026-10-17-000008](https://palomar-registry.org/entry.html?id=PALOMAR-2026-10-17-000008&version=1) (version 1) · code: [jtraverso/nash-williams-trees @ 101e488](https://github.com/jtraverso/nash-williams-trees/tree/101e48847a929dd8102521f57723e2137989ce2e) · [archived copy](https://github.com/PalomarArchive/jtraverso--nash-williams-trees--9280327cd578/tree/palomar/PALOMAR-2026-10-17-000008-v1/101e48847a929dd8102521f57723e2137989ce2e)

**What is proved.** A Lean 4 / Mathlib formalization of three classical results on edge-disjoint trees and forests in finite simple graphs, none of which is in Mathlib. (1) The Nash-Williams–Tutte tree packing theorem: a graph has k edge-disjoint spanning trees if and only if every partition of its vertices into m parts has at least k(m − 1) edges between different parts. (2) Nash-Williams' arboricity theorem: the edges can be covered by k forests if and only if every nonempty vertex set S spans at most k(|S| − 1) edges. (3) The corollary that every 2k-edge-connected graph has k edge-disjoint spanning trees. Mathlib has no matroid union theorem and no graphic matroid; the proofs are direct edge-exchange arguments.

**Sources.**

* C. St. J. A. Nash-Williams, *Edge-Disjoint Spanning Trees of Finite Graphs*, Journal of the London Mathematical Society s1-36 (1961), 445–450. [doi:10.1112/jlms/s1-36.1.445](https://doi.org/10.1112/jlms/s1-36.1.445)
* W. T. Tutte, *On the Problem of Decomposing a Graph into n Connected Factors*, Journal of the London Mathematical Society s1-36 (1961), 221–230. [doi:10.1112/jlms/s1-36.1.221](https://doi.org/10.1112/jlms/s1-36.1.221)
* C. St. J. A. Nash-Williams, *Decomposition of Finite Graphs Into Forests*, Journal of the London Mathematical Society s1-39 (1964), 12. [doi:10.1112/jlms/s1-39.1.12](https://doi.org/10.1112/jlms/s1-39.1.12)

<details><summary>Background references</summary>

* B. Chen, M. Matsumoto, J. Wang, Z. Zhang, J. Zhang, *A short proof of Nash-Williams' theorem for the arboricity of a graph*, Graphs and Combinatorics 10 (1994), 27–28. [doi:10.1007/BF01202467](https://doi.org/10.1007/BF01202467)
* Reinhard Diestel, *Graph Theory*, Graduate Texts in Mathematics 173, 5th edition, Springer (2017), Section 2.4 (Theorem 2.4.1 and its proof). [doi:10.1007/978-3-662-53622-3](https://doi.org/10.1007/978-3-662-53622-3)

</details>

## Fractional triangle decompositions of dense tripartite graphs

Palomar: [PALOMAR-2026-10-30-000008](https://palomar-registry.org/entry.html?id=PALOMAR-2026-10-30-000008&version=1) (version 1) · code: [jtraverso/fractional-triangle-decompositions-tripartite @ d233113](https://github.com/jtraverso/fractional-triangle-decompositions-tripartite/tree/d2331132eac8b9c9c1891ba14162745d567ebfdb) · [archived copy](https://github.com/PalomarArchive/jtraverso--fractional-triangle-decompositions-tripartite--1b438fcdd323/tree/palomar/PALOMAR-2026-10-30-000008-v1/d2331132eac8b9c9c1891ba14162745d567ebfdb)

**What is proved.** A Lean 4 / Mathlib formalization of the main results of Allsop, Bowtell, Lesgourgues and Petrova, "Improved bounds on completion of partial Latin squares" (arXiv:2609.37877, 2026): there is η > 0 (here η = 1/20000) such that every K₃-divisible spanning subgraph of K_{n,n,n} with minimum partite degree at least (0.769 − η)n has a fractional triangle decomposition (Theorem 1.3). Also formalized: the Farkas characterization (Lemma 2.1); the reduction to triangle-covered, balanced, untied and nonzero edge weightings (Proposition 3.1, Corollary 3.5), with Lemma 3.4 proved through an integral maximum flow; the non-uniform proportional discharging (Definition 4.1) and its two estimates (Propositions 4.2 and 4.3); and the numerical inequality g_d ≥ 1 for the article's piecewise-linear f (Proposition 4.4). The two-variable inequalities of Proposition 4.4, which the article settles by numerical minimisation, are proved exactly by Bernstein certificates checked in Lean. Not formalized: the article's Corollary 1.4 (completion of partial Latin squares), which also needs the fractional-to-exact transfer of Barber, Kühn, Lo, Osthus and Taylor for tripartite graphs.

**Sources.**

* Jack Allsop, Candida Bowtell, Thomas Lesgourgues, Kalina Petrova, *Improved bounds on completion of partial Latin squares*, arXiv:2609.37877v1 (30 September 2026), Theorem 1.3, Lemma 2.1, Proposition 3.1, Corollary 3.5, Definition 4.1, Propositions 4.2, 4.3 and 4.4, and Appendix A. [free full text](https://arxiv.org/pdf/2609.37877) (arXiv)

## Fractional clique decompositions of dense partite graphs

Palomar: [PALOMAR-2026-11-03-000019](https://palomar-registry.org/entry.html?id=PALOMAR-2026-11-03-000019&version=1) (version 1) · code: [jtraverso/montgomery-fractional-clique-decompositions @ c638d93](https://github.com/jtraverso/montgomery-fractional-clique-decompositions/tree/c638d93a5dd3fc3758c1c09c44672e2c3d6e3ba9) · [archived copy](https://github.com/PalomarArchive/jtraverso--montgomery-fractional-clique-decompositions--db620b60fa20/tree/palomar/PALOMAR-2026-11-03-000019-v1/c638d93a5dd3fc3758c1c09c44672e2c3d6e3ba9)

**What is proved.** A Lean 4 / Mathlib formalization of the main theorem of R. Montgomery, "Fractional clique decompositions of dense partite graphs" (arXiv:1603.01039; Combin. Probab. Comput. 26 (2017)): for r ≥ 3, every balanced K_r-divisible r-partite graph with parts of size n in which every vertex has at least (1 − 1/(10⁶r³))n neighbours in every other part has a fractional K_r-decomposition (Theorem 1.1); and its non-partite consequence: every graph on n vertices with minimum degree at least (1 − 1/(10⁶r³))n has a fractional K_r-decomposition. The whole proof is formalized: clique counts (Proposition 3.2, Lemma 3.3), the two gadgets (Lemmas 4.2, 4.3), the splitting lemma (Lemma 4.4), the moving lemmas (Lemmas 5.2, 5.3, 5.6) and the final averaging. Not formalized: Theorem 1.2 (integral decompositions), which also needs the fractional-to-exact transfer of Barber, Kühn, Lo, Osthus and Taylor.

**Sources.**

* Richard Montgomery, *Fractional clique decompositions of dense partite graphs*, arXiv:1603.01039v1 (3 March 2016), Theorem 1.1, the non-partite consequence in the introduction, Proposition 3.2, Lemmas 3.3, 4.2, 4.3, 4.4, 5.2, 5.3 and 5.6. [free full text](https://arxiv.org/pdf/1603.01039) (arXiv)

## Triangle decompositions of dense tripartite graphs and completion of partial Latin squares

Palomar: [PALOMAR-2026-11-01-000005](https://palomar-registry.org/entry.html?id=PALOMAR-2026-11-01-000005&version=3) (version 3) · code: [jtraverso/triangle-decompositions-tripartite @ fd5c713](https://github.com/jtraverso/triangle-decompositions-tripartite/tree/fd5c713e00cc03454878cdfc3acd8a7c9b0c19de) · [archived copy](https://github.com/PalomarArchive/jtraverso--triangle-decompositions-tripartite--9560d1b43409/tree/palomar/PALOMAR-2026-11-01-000005-v3/fd5c713e00cc03454878cdfc3acd8a7c9b0c19de)

**What is proved.** A Lean 4 / Mathlib formalization of Corollary 1.6 for r = 3 of Barber, Kühn, Lo, Osthus and Taylor, "Clique decompositions of multipartite graphs and completion of Latin squares" (J. Combin. Theory Ser. A 151 (2017), arXiv:1603.01043): fractional triangle decompositions above a threshold give triangle decompositions above the same threshold. Precisely: if δ ≥ 3/4 and, for every ε > 0, every K₃-divisible tripartite graph with three parts of size n ≥ n₀(ε) and minimum partite degree at least (δ + ε)n has a fractional triangle decomposition, then for every ε > 0 there is n₀ such that every K₃-divisible tripartite graph with parts of size n ≥ n₀ and minimum partite degree at least (δ + ε)n has a triangle decomposition (BKLOT2017.corollary_1_6). The hypothesis δ ≥ 3/4 is an extra assumption of the Lean statement: the article does not need it because the fractional threshold is known to be at least 3/4, which is not formalized here. Combined with the fractional bound of Allsop, Bowtell, Lesgourgues and Petrova (pinned entry PALOMAR-2026-10-30-000008), this gives the unconditional statement with threshold 0.769 − 1/20000 (BKLOT2017.corollary_1_6_ablp). The proof follows the iterative absorption of the article (absorbers, vortex of partitions with random reserves, cover-down, balancing graph, assembly) but replaces the regularity-based Section 8 by a route through the fractional threshold and the Haxell–Rödl transfer. Version 2 adds Theorem 1.4 and Corollary 3.2 for r = 3, the completion of partial Latin squares: for every ε > 0 and all large n, every partial Latin square of order n in which every row, every column and every symbol is used at most (1 − δ − ε)n times extends to a Latin square, above the fractional threshold δ ≥ 3/4 (BKLOT2017.theorem_1_4, from Cor16 δ by BKLOT2017.corollary_3_2) and unconditionally with 1 − δ = 0.231 + 1/20000 (BKLOT2017.theorem_1_4_ablp).

**Sources.**

* Ben Barber, Daniela Kühn, Allan Lo, Deryk Osthus, Amelia Taylor, *Clique decompositions of multipartite graphs and completion of Latin squares*, J. Combin. Theory Ser. A 151 (2017) 146–201; arXiv:1603.01043v2. Corollary 1.6 for r = 3, proved through Theorem 1.1 and Sections 5–11 (Lemmas 6.6, 7.2, 8.1, 9.1, 10.1, 11.1, 11.2, Corollaries 7.5 and 9.4) specialised to triangles. [doi:10.1016/j.jcta.2017.04.005](https://doi.org/10.1016/j.jcta.2017.04.005) · [free full text](https://arxiv.org/pdf/1603.01043) (arXiv)

<details><summary>Background references</summary>

* Jack Allsop, Candida Bowtell, Thomas Lesgourgues, Kalina Petrova, *Improved bounds on completion of partial Latin squares*, arXiv:2609.37877v1 (30 September 2026), Theorem 1.3. [free full text](https://arxiv.org/pdf/2609.37877) (arXiv)

</details>

## Triangle decompositions of typical graphs of fixed density (Keevash, Counting designs, Theorem 2.1, weaker form)

Palomar: [PALOMAR-2026-11-06-000011](https://palomar-registry.org/entry.html?id=PALOMAR-2026-11-06-000011&version=1) (version 1) · code: [jtraverso/keevash-typical-triangle-decompositions @ 6eb072d](https://github.com/jtraverso/keevash-typical-triangle-decompositions/tree/6eb072d132ff300374286b314a4ae7ef6512a8b4) · [archived copy](https://github.com/PalomarArchive/jtraverso--keevash-typical-triangle-decompositions--6ac21d20076b/tree/palomar/PALOMAR-2026-11-06-000011-v1/6eb072d132ff300374286b314a4ae7ef6512a8b4)

**What is proved.** A Lean 4 / Mathlib formalization of a weaker, fixed-density form of Theorem 2.1 of P. Keevash, Counting designs (J. Eur. Math. Soc. 20, 2018). density G is |E(G)| / C(n, 2); IsTypical G c h says that every nonempty set S of at most h vertices has (1 ± |S| c) d(G)^|S| n common neighbours; Tridivisible G says that every degree is even and 3 divides |E(G)|; IsTriangleDecomposition G D says that D is a family of triangles of G and every edge lies in exactly one of them. typical_triangle_decomposition: there is h such that for every d0 > 0 there are c0 > 0 and n0 such that every (c0, h)-typical tridivisible graph on n ≥ n0 vertices with density at least d0 has a triangle decomposition. This is weaker than the article in two ways: the density is bounded below by a fixed constant (the article allows d(G) > n^(-10^-7) with c < c0 d(G)^(10^6)), and the typicality is (c, h)-typicality for an absolute, not explicit, h (the article assumes c-typicality, which concerns only degrees and pairs). One statement.

**Sources.**

* Peter Keevash, *Counting designs*, Journal of the European Mathematical Society 20 (2018), 903–927; Theorem 2.1 (numbering of arXiv:1504.02909). [doi:10.4171/JEMS/779](https://doi.org/10.4171/JEMS/779) · [free full text](https://arxiv.org/pdf/1504.02909) (arXiv)

## Baranyai's theorem

Palomar: [PALOMAR-2026-11-06-000003](https://palomar-registry.org/entry.html?id=PALOMAR-2026-11-06-000003&version=1) (version 1) · code: [jtraverso/baranyai-theorem @ 0ff6d6f](https://github.com/jtraverso/baranyai-theorem/tree/0ff6d6f4005b0b68114e0b99e6d342742918b629) · [archived copy](https://github.com/PalomarArchive/jtraverso--baranyai-theorem--0fb5997ac7ea/tree/palomar/PALOMAR-2026-11-06-000003-v1/0ff6d6f4005b0b68114e0b99e6d342742918b629)

**What is proved.** A Lean 4 / Mathlib formalization of Baranyai's theorem: if k divides n, the k-subsets of an n-set can be partitioned into (n−1 choose k−1) parallel classes, each a partition of the set into n/k blocks of size k (a 1-factorization of the complete k-uniform hypergraph); and of Baranyai's rounding lemma: every real matrix can be rounded entrywise to floors or ceilings so that all row sums, column sums and the total are also rounded. The proof includes the integral max-flow theorem for integer capacities. Mathlib has neither result.

**Sources.**

* Zsolt Baranyai, *On the factorization of the complete uniform hypergraph*, Infinite and Finite Sets (Proc. Colloq. Keszthely, 1973), Colloq. Math. Soc. János Bolyai 10, North-Holland (1975), 91–108.

<details><summary>Background references</summary>

* J. H. van Lint, R. M. Wilson, *A Course in Combinatorics (2nd edition)*, Cambridge University Press (2001), Chapter 38. [doi:10.1017/CBO9780511987045](https://doi.org/10.1017/CBO9780511987045)
* L. R. Ford, D. R. Fulkerson, *Maximal flow through a network*, Canadian Journal of Mathematics 8 (1956), 399–404. [doi:10.4153/CJM-1956-045-5](https://doi.org/10.4153/CJM-1956-045-5) · [free full text](https://www.cambridge.org/core/services/aop-cambridge-core/content/view/5D6E55D3B06C4F7B1043BC1D82D40764/S0008414X00036890a.pdf/div-class-title-maximal-flow-through-a-network-div.pdf)

</details>

[← Back to the list](../README.md)
