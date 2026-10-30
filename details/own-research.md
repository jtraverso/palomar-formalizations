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

## The Nash–Williams triangle-decomposition theorem

Palomar: [PALOMAR-2026-10-21-000009](https://palomar-registry.org/entry.html?id=PALOMAR-2026-10-21-000009&version=1) (version 1) · code: [jtraverso/nash-williams-lean @ 2603197](https://github.com/jtraverso/nash-williams-lean/tree/2603197abdbf0a600ec663f6f046f70fbd209d4a) · [archived copy](https://github.com/PalomarArchive/jtraverso--nash-williams-lean--252fc7828395/tree/palomar/PALOMAR-2026-10-21-000009-v1/2603197abdbf0a600ec663f6f046f70fbd209d4a)

**What is proved.** A Lean 4 / Mathlib formalization of the Nash–Williams theorem for large graphs proved by Delcourt and Postle: there is N such that every finite simple graph on n ≥ N vertices that is triangle-divisible (3 divides the number of edges and every degree is even) and has minimum degree at least 3n/4 has a triangle decomposition; together with Delcourt–Postle's fractional threshold (every graph with 3n ≤ 4δ has a fractional triangle decomposition) and their fractional stability theorem (with an additional order threshold). The proof follows their extremal/non-extremal case division but does not assume their Theorem 13.16, whose proof is assigned to an unpublished manuscript: the extremal residuals are decomposed with typed absorption results developed in the same project, and the non-extremal case with a protected covering-round argument. The development has 1,070 modules.

**Sources.**

* Michelle Delcourt, Luke Postle, *A Proof of Nash-Williams' Conjecture*, arXiv:2606.11178 (2026), Theorems 1.4, 1.6 and 1.8. [doi:10.48550/arXiv.2606.11178](https://doi.org/10.48550/arXiv.2606.11178) · [free full text](https://arxiv.org/pdf/2606.11178) (arXiv)
* Juan Pablo Traverso Gianini, *Triangle decompositions I: Formalizing the Nash–Williams theorem in Lean*, Preprint 1.0 (2026).
* Juan Pablo Traverso Gianini, *Triangle decompositions II: Robust absorption for typed triangles*, Preprint 1.0 (2026).

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

## Formalizing Delcourt–Postle’s refined absorption in Lean

Palomar: [PALOMAR-2026-10-29-000005](https://palomar-registry.org/entry.html?id=PALOMAR-2026-10-29-000005&version=1) (version 1) · code: [jtraverso/refined-absorption-lean @ 5bfe5c7](https://github.com/jtraverso/refined-absorption-lean/tree/5bfe5c7346a7b245581152dccebe363e22f072b6) · [archived copy](https://github.com/PalomarArchive/jtraverso--refined-absorption-lean--6accc6d51192/tree/palomar/PALOMAR-2026-10-29-000005-v1/5bfe5c7346a7b245581152dccebe363e22f072b6)

**What is proved.** One assembled Lean formalization of principal refined absorption results and their consequences. The selected results include refined omni-absorbers and refiners, labelled reserve matchings, dense compatible decompositions, an additive compatible-absorber interface retaining independence of the entire old ambient vertex set, and existence of simple designs for every fixed q > r ≥ 2 and index λ ≥ 1 at all sufficiently large admissible orders. The literal global embedding conclusion of the survey is refuted separately from a proved piecewise replacement. The research-note endpoints give completion avoiding an arbitrary forbidden partial Steiner system, sparse prescribed and finite embedded exact intersections, an initial polynomial intersection interval, and polynomial excess in partial parallel classes and Nash–Williams schedule rounds. Both external inputs are supplied by pinned proved theorems. The single comparison selects eighteen declarations from the existing aggregate proof root.

**Sources.**

* Michelle Delcourt, Luke Postle, *Refined Absorption: A New Proof of the Existence Conjecture*, arXiv:2402.17855v1 (2024). [doi:10.48550/arXiv.2402.17855](https://doi.org/10.48550/arXiv.2402.17855) · [free full text](https://arxiv.org/pdf/2402.17855) (arXiv)
* Luke Postle, *Refined Absorption: A New Proof of the Existence Conjecture and Its Applications to Extremal and Probabilistic Design Theory*, ICM 2026, Volume 6, pp. 212–231; statement baseline arXiv:2510.19978v1. [doi:10.1137/25M1805977](https://doi.org/10.1137/25M1805977) · [free full text](https://arxiv.org/pdf/2510.19978) (arXiv)
* Juan Pablo Traverso Gianini, *Formalizing Delcourt–Postle’s refined absorption in Lean*, Research note, version 1.0.1 (2026); editorial update, unchanged proof sources. [doi:10.5281/zenodo.23715622](https://doi.org/10.5281/zenodo.23715622) · [free full text](https://doi.org/10.5281/zenodo.23715622) (Zenodo)
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

[← Back to the list](../README.md)
