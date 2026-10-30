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

[← Back to the list](../README.md)
