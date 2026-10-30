# Formalizations registered in Palomar

Lean 4 / Mathlib formalizations by **Juan Pablo Traverso Gianini** that have been accepted
and registered in the [Palomar registry](https://palomar-registry.org). Each entry links to its
Palomar record, where the audited statements (`Challenge.lean`), the proofs, the mechanical
verification evidence and the review are kept, and to the source repository at the registered
commit.

This list is updated after each accepted submission. Each registered commit is also preserved by
Palomar in an archive copy under the [PalomarArchive](https://github.com/PalomarArchive) organization
(linked for every entry), so the registered sources remain available independently of the original
repositories.

## Contents

68 registered entries.

* [Original research by the author](#original-research-by-the-author)
  * [Erdős Problem #81 series](#erdős-problem-81-series)
  * [Triangle decompositions series](#triangle-decompositions-series)
* [Classical and recent results, by area](#classical-and-recent-results-by-area)
  * [Vertex colouring](#vertex-colouring) (8)
  * [Edge colouring and list colouring](#edge-colouring-and-list-colouring) (9)
  * [Planarity, minors and graph classes](#planarity-minors-and-graph-classes) (3)
  * [Connectivity, orientations and flows](#connectivity-orientations-and-flows) (6)
  * [Cycles and Hamiltonicity](#cycles-and-hamiltonicity) (4)
  * [Matchings, factors and polyhedral combinatorics](#matchings-factors-and-polyhedral-combinatorics) (8)
  * [Extremal graph theory and Ramsey theory](#extremal-graph-theory-and-ramsey-theory) (4)
  * [Probabilistic methods and random graphs](#probabilistic-methods-and-random-graphs) (5)
  * [Decompositions and packings](#decompositions-and-packings) (4)
  * [Designs, set systems and discrepancy](#designs-set-systems-and-discrepancy) (5)
  * [Algebraic and spectral graph theory](#algebraic-and-spectral-graph-theory) (6)
* [Registration log](#registration-log)
* [Notes](#notes)
* [arXiv endorsement](#arxiv-endorsement)

## Original research by the author

Formalizations of the author's own results, grouped by research series.

### Erdős Problem #81 series

Clique partitions of chordal graphs and split graphs (Erdős Problem #81). Series repository [jtraverso/erdos-81-chordal-clique-partitions](https://github.com/jtraverso/erdos-81-chordal-clique-partitions); series concept DOI [10.5281/zenodo.21273143](https://doi.org/10.5281/zenodo.21273143); current PDF collection [10.5281/zenodo.23479507](https://doi.org/10.5281/zenodo.23479507) (open access).

#### Affine profile reduction for fractional triangle packings in split graphs

[PALOMAR-2026-10-28-000028](https://palomar-registry.org/entry.html?id=PALOMAR-2026-10-28-000028&version=2) (v2) · [jtraverso/erdos81-fractional-split-profiles @ f8690bc](https://github.com/jtraverso/erdos81-fractional-split-profiles/tree/f8690bcba57bddc5deefd8626f5b07e0d63e6086) · [archived copy](https://github.com/PalomarArchive/jtraverso--erdos81-fractional-split-profiles--2f8b880d7704/tree/palomar/PALOMAR-2026-10-28-000028-v2/f8690bcba57bddc5deefd8626f5b07e0d63e6086)

**Sources:**

* Juan Pablo Traverso Gianini, *Affine Profile Reduction for Fractional Triangle Packings in Split Graphs*, Erdős #81 series, Paper I, preprint v1.4 (19 October 2026), Theorem 1.1 and its finite consequence; deposited in the series collection on Zenodo (series concept DOI 10.5281/zenodo.21273143) and in github.com/jtraverso/erdos-81-chordal-clique-partitions. [doi:10.5281/zenodo.23478825](https://doi.org/10.5281/zenodo.23478825) · open access (Zenodo)
* Juan Pablo Traverso Gianini, *Colorability and Realizability (Erdős #81 series, Paper V)*, Erdős #81 series, Paper V, preprint 1.0, in the 32-PDF series collection on Zenodo; Lean sources in github.com/jtraverso/erdos-81-chordal-clique-partitions. [doi:10.5281/zenodo.23479507](https://doi.org/10.5281/zenodo.23479507) · open access (Zenodo)

<details><summary>Background references</summary>

* Julius Farkas, *Theorie der einfachen Ungleichungen*, Journal für die reine und angewandte Mathematik 124 (1902), 1–27. [doi:10.1515/crll.1902.124.1](https://doi.org/10.1515/crll.1902.124.1)

</details>

<details><summary>What is formalized</summary>

A Lean 4 / Mathlib formalization of the main result of the author's preprint "Affine Profile Reduction for Fractional Triangle Packings in Split Graphs" (Erdős #81 series, Paper I): for every finite split graph G on n vertices, |E(G)| − 2ν₃*(G) ≤ n²/6 + n/2, where ν₃* is the fractional triangle packing number (the maximum total weight of a nonnegative weighting of the triangles with load at most one on every edge). It is stated both for the paper's finite split model (clique Fin p, independent vertices, neighbourhoods) and for every split graph in Mathlib's SimpleGraph, with the definitions of split graphs and fractional triangle packings of two registered entries; the weaker bound n²/6 + n of the first edition is also included. The proof reduces the fractional packing problem to neighbourhood profiles and a three-variable linear program, using finite LP duality. Version 2 states the finite LP duality used in the series as results of its own, over ℝ (Farkas' lemma in inequality form and covering/packing strong duality, from this proof) and over ℚ (Farkas' lemma by Fourier–Motzkin elimination and strong duality for the rational packing LP, from the author's Paper V).

</details>

#### Complete-split extremizers for the fractional triangle-cover deficit on chordal graphs

[PALOMAR-2026-10-29-000004](https://palomar-registry.org/entry.html?id=PALOMAR-2026-10-29-000004&version=1) (v1) · [jtraverso/erdos81-complete-split-extremizers @ 7961c3a](https://github.com/jtraverso/erdos81-complete-split-extremizers/tree/7961c3aba6062b03de3df28f42d339c1aec145d8) · [archived copy](https://github.com/PalomarArchive/jtraverso--erdos81-complete-split-extremizers--398c83aea952/tree/palomar/PALOMAR-2026-10-29-000004-v1/7961c3aba6062b03de3df28f42d339c1aec145d8)

**Sources:**

* Juan Pablo Traverso Gianini, *Complete-Split Extremizers for a Fractional Triangle-Cover Functional on Chordal Graphs*, Erdős #81 series, Paper II, preprint v1.3 (19 October 2026), Theorem 1.2; deposited in the series collection on Zenodo (series concept DOI 10.5281/zenodo.21273143) and in github.com/jtraverso/erdos-81-chordal-clique-partitions. [doi:10.5281/zenodo.23478825](https://doi.org/10.5281/zenodo.23478825) · open access (Zenodo)

<details><summary>What is formalized</summary>

A Lean 4 / Mathlib formalization of the main result of the author's preprint "Complete-Split Extremizers for a Fractional Triangle-Cover Functional on Chordal Graphs" (Erdős #81 series, Paper II). For a finite simple graph G let τ₃*(G) be its fractional triangle cover number (the least total weight of a nonnegative weighting of vertex pairs giving every triangle weight at least one on its edges) and Φ_τ(G) = |E(G)| − 2τ₃*(G). For every n ≥ 1, every chordal graph on n vertices satisfies Φ_τ(G) ≤ ⌊(2n + 1)²/24⌋, and equality is attained by a complete-split graph K_p ∨ K̄_q with p + q = n (Theorem 1.2). Chordality and fractional triangle covers use the definitions of two registered entries.

</details>

#### Linear-error clique partitions of split graphs

[PALOMAR-2026-10-29-000006](https://palomar-registry.org/entry.html?id=PALOMAR-2026-10-29-000006&version=1) (v1) · [jtraverso/erdos81-split-clique-partitions @ a98dfa4](https://github.com/jtraverso/erdos81-split-clique-partitions/tree/a98dfa413428b3c532174575a39f89eb32b268b8) · [archived copy](https://github.com/PalomarArchive/jtraverso--erdos81-split-clique-partitions--91b4db9f18d8/tree/palomar/PALOMAR-2026-10-29-000006-v1/a98dfa413428b3c532174575a39f89eb32b268b8)

**Sources:**

* Juan Pablo Traverso Gianini, *Linear-Error Clique Partitions of Split Graphs via Structured Triangle Packing*, Erdős #81 series, Paper III, preprint v1.6 (19 October 2026), Theorem 1.1 and Corollary 1.2; deposited in the series collection on Zenodo (series concept DOI 10.5281/zenodo.21273143) and in github.com/jtraverso/erdos-81-chordal-clique-partitions. [doi:10.5281/zenodo.23478825](https://doi.org/10.5281/zenodo.23478825) · open access (Zenodo)

<details><summary>What is formalized</summary>

A Lean 4 / Mathlib formalization of the main results of the author's preprint "Linear-Error Clique Partitions of Split Graphs via Structured Triangle Packing" (Erdős #81 series, Paper III): there is an absolute constant C such that every finite split graph G on n vertices satisfies |E(G)| − 2ν₃(G) ≤ n²/6 + C·n, where ν₃(G) is the maximum number of pairwise edge-disjoint triangles (Theorem 1.1); consequently G has a clique partition (a family of cliques covering every edge exactly once) with at most n²/6 + C·n cliques (Corollary 1.2). The quadratic coefficient 1/6 is the sharp one for split graphs. The constant C is existential and not explicit. Two ingredients of the proof, the asymptotic gap between fractional and integral triangle packings and exact triangle decompositions of dense triangle-divisible graphs, are taken from two registered formalizations (see related_formalizations).

</details>

### Triangle decompositions series

The Nash–Williams triangle-decomposition problem. Publication home [jtraverso/nash-williams-triangle-decompositions-release](https://github.com/jtraverso/nash-williams-triangle-decompositions-release).

#### The Nash–Williams triangle-decomposition theorem

[PALOMAR-2026-10-21-000009](https://palomar-registry.org/entry.html?id=PALOMAR-2026-10-21-000009&version=1) (v1) · [jtraverso/nash-williams-lean @ 2603197](https://github.com/jtraverso/nash-williams-lean/tree/2603197abdbf0a600ec663f6f046f70fbd209d4a) · [archived copy](https://github.com/PalomarArchive/jtraverso--nash-williams-lean--252fc7828395/tree/palomar/PALOMAR-2026-10-21-000009-v1/2603197abdbf0a600ec663f6f046f70fbd209d4a)

**Sources:**

* Michelle Delcourt, Luke Postle, *A Proof of Nash-Williams' Conjecture*, arXiv:2606.11178 (2026), Theorems 1.4, 1.6 and 1.8. [doi:10.48550/arXiv.2606.11178](https://doi.org/10.48550/arXiv.2606.11178) · [open PDF](https://arxiv.org/pdf/2606.11178) (arXiv (Cornell University)) · [arXiv:2606.11178](https://arxiv.org/abs/2606.11178) ([PDF](https://arxiv.org/pdf/2606.11178))
* Juan Pablo Traverso Gianini, *Triangle decompositions I: Formalizing the Nash–Williams theorem in Lean*, Preprint 1.0 (2026).
* Juan Pablo Traverso Gianini, *Triangle decompositions II: Robust absorption for typed triangles*, Preprint 1.0 (2026).

<details><summary>Background references</summary>

* C. St. J. A. Nash-Williams, *An unsolved problem concerning decomposition of graphs into triangles*, Combinatorial Theory and its Applications III, North-Holland (1970), 1179–1183.

</details>

<details><summary>What is formalized</summary>

A Lean 4 / Mathlib formalization of the Nash–Williams theorem for large graphs proved by Delcourt and Postle: there is N such that every finite simple graph on n ≥ N vertices that is triangle-divisible (3 divides the number of edges and every degree is even) and has minimum degree at least 3n/4 has a triangle decomposition; together with Delcourt–Postle's fractional threshold (every graph with 3n ≤ 4δ has a fractional triangle decomposition) and their fractional stability theorem (with an additional order threshold). The proof follows their extremal/non-extremal case division but does not assume their Theorem 13.16, whose proof is assigned to an unpublished manuscript: the extremal residuals are decomposed with typed absorption results developed in the same project, and the non-extremal case with a protected covering-round argument. The development has 1,070 modules.

</details>

#### Robust absorption for typed triangles (Triangle decompositions II)

[PALOMAR-2026-10-23-000013](https://palomar-registry.org/entry.html?id=PALOMAR-2026-10-23-000013&version=1) (v1) · [jtraverso/typed-triangle-absorption @ 673c6d4](https://github.com/jtraverso/typed-triangle-absorption/tree/673c6d4118b5679783bafa7606fd2c611161a254) · [archived copy](https://github.com/PalomarArchive/jtraverso--typed-triangle-absorption--055c1b37404f/tree/palomar/PALOMAR-2026-10-23-000013-v1/673c6d4118b5679783bafa7606fd2c611161a254)

**Sources:**

* Juan Pablo Traverso Gianini, *Triangle decompositions II: Robust absorption for typed triangles*, Preprint 1.0, 20 October 2026; Theorems A–D, balanced consequence of B and Lemma SC. [doi:10.5281/zenodo.23502224](https://doi.org/10.5281/zenodo.23502224) · open access (Zenodo)

<details><summary>Background references</summary>

* Peter Keevash, *The existence of designs II*, arXiv:1802.05900, Theorem 3.1. [doi:10.48550/arXiv.1802.05900](https://doi.org/10.48550/arXiv.1802.05900) · [open PDF](https://arxiv.org/pdf/1802.05900) (arXiv (Cornell University)) · [arXiv:1802.05900](https://arxiv.org/abs/1802.05900) ([PDF](https://arxiv.org/pdf/1802.05900))
* Michelle Delcourt, Luke Postle, *Refined Absorption: A New Proof of the Existence Conjecture*, arXiv:2402.17855. [doi:10.48550/arXiv.2402.17855](https://doi.org/10.48550/arXiv.2402.17855) · [open PDF](https://arxiv.org/pdf/2402.17855) (arXiv (Cornell University)) · [arXiv:2402.17855](https://arxiv.org/abs/2402.17855) ([PDF](https://arxiv.org/pdf/2402.17855))
* Michelle Delcourt, Luke Postle, *A Proof of Nash-Williams' Conjecture*, arXiv:2606.11178, partitioned residual applications. [doi:10.48550/arXiv.2606.11178](https://doi.org/10.48550/arXiv.2606.11178) · [open PDF](https://arxiv.org/pdf/2606.11178) (arXiv (Cornell University)) · [arXiv:2606.11178](https://arxiv.org/abs/2606.11178) ([PDF](https://arxiv.org/pdf/2606.11178))
* Ben Barber, Daniela Kühn, Allan Lo, Deryk Osthus, Amelia Taylor, *Clique decompositions of multipartite graphs and completion of Latin squares*, Journal of Combinatorial Theory, Series A 151 (2017). [doi:10.1016/j.jcta.2017.04.005](https://doi.org/10.1016/j.jcta.2017.04.005) · [open PDF](https://www.sciencedirect.com/science/article/pii/S0097316517300432/pdf) (Journal of Combinatorial Theory Series A)

</details>

<details><summary>What is formalized</summary>

Typed triangle decomposition results from Paper II: a typical-host theorem under three-step links for four-label families; its nearly complete and balanced deductions with explicit type-weight hypotheses; a semidense two-label mixed-triangle theorem; a computer-assisted typical-host theorem for every admissible four-label family; and a terminal absorber obtained from a bounded signed certificate and explicit physical hinge supply. Divisibility includes global edge counts and local degree profiles. The typical-host hypotheses are retained; the result is not asserted for arbitrary divisible hosts. The repository contains the substantive proof development, including the finite family census and conserved-family constructions, with a small independent Mathlib-only Challenge.

</details>

#### Formalizing Delcourt–Postle’s refined absorption in Lean

[PALOMAR-2026-10-29-000005](https://palomar-registry.org/entry.html?id=PALOMAR-2026-10-29-000005&version=1) (v1) · [jtraverso/refined-absorption-lean @ 5bfe5c7](https://github.com/jtraverso/refined-absorption-lean/tree/5bfe5c7346a7b245581152dccebe363e22f072b6) · [archived copy](https://github.com/PalomarArchive/jtraverso--refined-absorption-lean--6accc6d51192/tree/palomar/PALOMAR-2026-10-29-000005-v1/5bfe5c7346a7b245581152dccebe363e22f072b6)

**Sources:**

* Michelle Delcourt, Luke Postle, *Refined Absorption: A New Proof of the Existence Conjecture*, arXiv:2402.17855v1 (2024). [doi:10.48550/arXiv.2402.17855](https://doi.org/10.48550/arXiv.2402.17855) · [open PDF](https://arxiv.org/pdf/2402.17855) (arXiv (Cornell University)) · [arXiv:2402.17855](https://arxiv.org/abs/2402.17855) ([PDF](https://arxiv.org/pdf/2402.17855))
* Luke Postle, *Refined Absorption: A New Proof of the Existence Conjecture and Its Applications to Extremal and Probabilistic Design Theory*, ICM 2026, Volume 6, pp. 212–231; statement baseline arXiv:2510.19978v1. [doi:10.1137/25M1805977](https://doi.org/10.1137/25M1805977) · [arXiv:2510.19978](https://arxiv.org/abs/2510.19978) ([PDF](https://arxiv.org/pdf/2510.19978))
* Juan Pablo Traverso Gianini, *Formalizing Delcourt–Postle’s refined absorption in Lean*, Research note, version 1.0.1 (2026); editorial update, unchanged proof sources. [doi:10.5281/zenodo.23715622](https://doi.org/10.5281/zenodo.23715622) · open access (Zenodo)
* Stefan Ehard, Stefan Glock, Felix Joos, *Pseudorandom hypergraph matchings*. [doi:10.1017/S0963548320000280](https://doi.org/10.1017/S0963548320000280) · [open PDF](https://www.cambridge.org/core/services/aop-cambridge-core/content/view/AE0DE17C95900E7DD3F221E2C17FE203/S0963548320000280a.pdf/div-class-title-pseudorandom-hypergraph-matchings-div.pdf) (Combinatorics Probability Computing)
* Michelle Delcourt, Luke Postle, *A Proof of Nash-Williams' Conjecture*. [doi:10.48550/arXiv.2606.11178](https://doi.org/10.48550/arXiv.2606.11178) · [open PDF](https://arxiv.org/pdf/2606.11178) (arXiv (Cornell University))

<details><summary>Background references</summary>

* Nicholas Pippenger, Joel Spencer, *Asymptotic behavior of the chromatic index for hypergraphs*. [doi:10.1016/0097-3165(89)90074-5](https://doi.org/10.1016/0097-3165(89)90074-5) · free to read at the publisher
* Juan Pablo Traverso Gianini, *Triangle decompositions I: Formalizing the Nash–Williams theorem in Lean*. [doi:10.5281/zenodo.23428173](https://doi.org/10.5281/zenodo.23428173) · open access (Zenodo)
* Juan Pablo Traverso Gianini, *Triangle decompositions II: Robust absorption for typed triangles*. [doi:10.5281/zenodo.23502224](https://doi.org/10.5281/zenodo.23502224) · open access (Zenodo)
* C. C. Lindner, A. Rosa, *Steiner triple systems having a prescribed number of triples in common*. [doi:10.4153/CJM-1975-122-4](https://doi.org/10.4153/CJM-1975-122-4)
* C. C. Lindner, A. Rosa, *Steiner triple systems having a prescribed number of triples in common (corrigendum)*, Canadian Journal of Mathematics 30 (1978), p. 896. [doi:10.4153/CJM-1978-077-9](https://doi.org/10.4153/CJM-1978-077-9)
* Michelle Delcourt, Cicely (Cece) Henderson, Thomas Lesgourgues, Luke Postle, *Erdős meets Nash-Williams*, arXiv:2507.23624v1, Appendix B. [doi:10.48550/arXiv.2507.23624](https://doi.org/10.48550/arXiv.2507.23624) · [arXiv:2507.23624](https://arxiv.org/abs/2507.23624) ([PDF](https://arxiv.org/pdf/2507.23624))

</details>

<details><summary>What is formalized</summary>

One assembled Lean formalization of principal refined absorption results and their consequences. The selected results include refined omni-absorbers and refiners, labelled reserve matchings, dense compatible decompositions, an additive compatible-absorber interface retaining independence of the entire old ambient vertex set, and existence of simple designs for every fixed q > r ≥ 2 and index λ ≥ 1 at all sufficiently large admissible orders. The literal global embedding conclusion of the survey is refuted separately from a proved piecewise replacement. The research-note endpoints give completion avoiding an arbitrary forbidden partial Steiner system, sparse prescribed and finite embedded exact intersections, an initial polynomial intersection interval, and polynomial excess in partial parallel classes and Nash–Williams schedule rounds. Both external inputs are supplied by pinned proved theorems. The single comparison selects eighteen declarations from the existing aggregate proof root.

</details>

## Classical and recent results, by area

Formalizations of published results of other authors, grouped by subject area (MSC 2020 classes as a guide). For every entry: the Palomar record, the source repository at the registered commit, the archived copy, and the original sources with their DOI and, when one exists, a link to a legally open version (from OpenAlex).

### Vertex colouring

#### Grötzsch's theorem, Ore's conjecture for k = 4 (Kostochka–Yancey), and the Grünbaum–Aksenov theorem

[PALOMAR-2026-10-13-000005](https://palomar-registry.org/entry.html?id=PALOMAR-2026-10-13-000005&version=2) (v2) · [jtraverso/grotzsch-ore @ ff6d512](https://github.com/jtraverso/grotzsch-ore/tree/ff6d5123c06e4c99bb6074e0a72e8be8d595eefa) · [archived copy](https://github.com/PalomarArchive/jtraverso--grotzsch-ore--8ebd0df3e665/tree/palomar/PALOMAR-2026-10-13-000005-v2/ff6d5123c06e4c99bb6074e0a72e8be8d595eefa) (v1: [archive](https://github.com/PalomarArchive/jtraverso--grotzsch-ore--8ebd0df3e665/tree/palomar/PALOMAR-2026-10-13-000005-v1/f923c459969d4a0a50d034cc02d558c7d4937436))

**Sources:**

* Alexandr Kostochka, Matthew Yancey, *Ore's conjecture for k = 4 and Grötzsch's theorem*, Combinatorica 34 (2014), no. 3, 323–329; https://arxiv.org/abs/1209.1173. [arXiv:1209.1173](https://arxiv.org/abs/1209.1173) ([PDF](https://arxiv.org/pdf/1209.1173))
* Oleg V. Borodin, Alexandr V. Kostochka, Bernard Lidický, Matthew Yancey, *Short proofs of coloring theorems on planar graphs*, European Journal of Combinatorics 36 (2014), 314–321; https://arxiv.org/abs/1211.3981. [arXiv:1211.3981](https://arxiv.org/abs/1211.3981) ([PDF](https://arxiv.org/pdf/1211.3981))
* Herbert Grötzsch, *Zur Theorie der diskreten Gebilde, VII: Ein Dreifarbensatz für dreikreisfreie Netze auf der Kugel*, Wiss. Z. Martin-Luther-Univ. Halle-Wittenberg Math.-Nat. Reihe 8 (1958/1959), 109–120.
* Branko Grünbaum, *Grötzsch's theorem on 3-colorings*, Michigan Mathematical Journal 10 (1963), 303–310.
* V. A. Aksenov, *On continuation of 3-colouring of planar graphs (Russian)*, Diskretnyi Analiz 26 (1974), 3–19.

<details><summary>Background references</summary>

* Oleg V. Borodin, *A new proof of Grünbaum's 3 color theorem*, Discrete Mathematics 169 (1997), 177–183.
* Tommy R. Jensen, Carsten Thomassen, *The color space of a graph*, Journal of Graph Theory 34 (2000), 234–245.
* Oystein Ore, *The Four Color Problem*, Academic Press, New York, 1967.
* Jack Edmonds, *A combinatorial representation for polyhedral surfaces*, Notices of the American Mathematical Society 7 (1960), 646.

</details>

<details><summary>What is formalized</summary>

A Lean 4 / Mathlib formalization of results on 3-colourings of planar graphs. (1) Kostochka and Yancey's theorem, the case k = 4 of Ore's 1967 conjecture on the minimum number of edges of k-critical graphs: every finite 4-critical graph G satisfies 3|E(G)| ≥ 5|V(G)| - 2, by their potential method. (2) Grötzsch's theorem: every finite triangle-free planar graph is 3-colourable, deduced from (1) as in Kostochka–Yancey, with the topological crossing argument replaced by a K5-minor argument with an apex inside a face. (3) Aksenov's and Jensen–Thomassen's theorem: a triangle-free planar graph plus one edge is 3-colourable (Borodin–Kostochka–Lidický–Yancey, Theorem 2). (4) A triangle-free planar graph plus one vertex of degree at most 4 is 3-colourable (BKLY, Theorem 4). (5) The Grünbaum–Aksenov theorem: every finite planar graph with at most three triangles is 3-colourable, following BKLY's short proof (Theorem 7), with precolouring extension for 4- and 5-cycles (BKLY Theorem 5, for arbitrary cycles) and a combinatorial region (Jordan-type) theorem for rotation systems making the interiors and outer faces of the paper precise. Planarity is defined combinatorially, by rotation systems of genus zero (Euler defect 0); as sanity checks on this definition K4 is shown planar and K5 and K3,3 non-planar.

</details>

#### The Hajnal–Szemerédi theorem on equitable colourings

[PALOMAR-2026-10-13-000007](https://palomar-registry.org/entry.html?id=PALOMAR-2026-10-13-000007&version=1) (v1) · [jtraverso/hajnal-szemeredi @ ba34061](https://github.com/jtraverso/hajnal-szemeredi/tree/ba34061e3cf12dfc8297610d5d7b3f0afac7ec54) · [archived copy](https://github.com/PalomarArchive/jtraverso--hajnal-szemeredi--c11276c44bab/tree/palomar/PALOMAR-2026-10-13-000007-v1/ba34061e3cf12dfc8297610d5d7b3f0afac7ec54)

**Sources:**

* H. A. Kierstead, A. V. Kostochka, *A short proof of the Hajnal–Szemerédi theorem on equitable colouring*, Combinatorics, Probability and Computing 17 (2008), 265–270. [doi:10.1017/S0963548307008619](https://doi.org/10.1017/S0963548307008619)
* András Hajnal, Endre Szemerédi, *Proof of a conjecture of P. Erdős*, Combinatorial Theory and its Applications II (P. Erdős, A. Rényi, V. T. Sós, eds.), North-Holland, 1970, 601–623.

<details><summary>Background references</summary>

* Paul Erdős, *Problem 9*, Theory of Graphs and its Applications (M. Fiedler, ed.), Czech. Academy of Sciences, Prague, 1964, p. 159.
* *Erdős Problem #914*, https://www.erdosproblems.com/914.

</details>

<details><summary>What is formalized</summary>

A Lean 4 / Mathlib formalization of the Hajnal–Szemerédi theorem (1970), conjectured by Erdős in 1964: every finite graph with maximum degree at most r has an equitable proper colouring with r + 1 colours, i.e. a proper colouring whose colour classes differ in size by at most one. The exact form is also proved: if the number of vertices is s(r + 1), every colour class has exactly s vertices (the colouring form of Erdős Problem #914). The proof follows the short argument of Kierstead and Kostochka (2008): induction on the number of edges; after deleting an edge, a nearly equitable colouring is repaired by moving vertices along paths of an auxiliary digraph on the colour classes (Lemma 2.1); when the large class is inaccessible, a family of terminal classes, solo edges and a discharging count with weights q/|S_z| (Lemmas 2.2–2.3) produce a recolouring that either finishes the colouring or strictly increases the number of accessible classes, using the induction hypothesis on the inaccessible part. The general case is reduced to the divisible one by adding a disjoint complete graph.

</details>

#### Brooks' theorem, degree-choosability and blocks

[PALOMAR-2026-10-16-000003](https://palomar-registry.org/entry.html?id=PALOMAR-2026-10-16-000003&version=2) (v2) · [jtraverso/brooks @ b99e6f5](https://github.com/jtraverso/brooks/tree/b99e6f500256586626396de9c2d6fd4d96119d60) · [archived copy](https://github.com/PalomarArchive/jtraverso--brooks--c255f4f55cbf/tree/palomar/PALOMAR-2026-10-16-000003-v2/b99e6f500256586626396de9c2d6fd4d96119d60)

**Sources:**

* R. L. Brooks, *On colouring the nodes of a network*, Mathematical Proceedings of the Cambridge Philosophical Society 37 (1941), 194–197. [doi:10.1017/S030500410002168X](https://doi.org/10.1017/S030500410002168X)
* P. Erdős, A. L. Rubin, H. Taylor, *Choosability in graphs*, Proceedings of the West Coast Conference on Combinatorics, Graph Theory and Computing, Congressus Numerantium 26 (1979), 125–157.
* O. V. Borodin, *Criteria of chromaticity of a degree prescription*, Abstracts of the IV All-Union Conference on Theoretical Cybernetics, Novosibirsk (1977), 127–128 (in Russian).
* V. G. Vizing, *Vertex colorings with given colors*, Metody Diskretnogo Analiza 29 (1976), 3–10 (in Russian).

<details><summary>Background references</summary>

* L. Lovász, *Three short proofs in graph theory*, Journal of Combinatorial Theory, Series B 19 (1975), 269–271. [doi:10.1016/0095-8956(75)90089-1](https://doi.org/10.1016/0095-8956(75)90089-1) · [open PDF](https://www.sciencedirect.com/science/article/pii/0095895675900891/pdf) (Journal of Combinatorial Theory Series B)
* A. V. Kostochka, M. Stiebitz, B. Wirth, *The colour theorems of Brooks and Gallai extended*, Discrete Mathematics 162 (1996), 299–303. [doi:10.1016/0012-365X(95)00294-7](https://doi.org/10.1016/0012-365X(95)00294-7) · [open PDF](https://www.sciencedirect.com/science/article/pii/0012365X95002947/pdf) (Discrete Mathematics)
* Reinhard Diestel, *Graph Theory*, Graduate Texts in Mathematics 173, 5th edition, Springer (2017), Section 3.1. [doi:10.1007/978-3-662-53622-3](https://doi.org/10.1007/978-3-662-53622-3)

</details>

<details><summary>What is formalized</summary>

A Lean 4 / Mathlib formalization of Brooks' theorem: for k ≥ 3, a finite graph of maximum degree at most k without a (k+1)-clique is k-colourable (no connectedness assumption), and a finite connected graph that is neither complete nor an odd cycle is colourable with as many colours as its maximum degree. The proof uses greedy colourings in Lovász's style and an induction on the number of edges with a separation-and-gluing step. Version 2 adds the Erdős–Rubin–Taylor / Borodin theorem (a finite connected graph is degree-choosable, i.e. colourable from any lists with |L(v)| ≥ deg(v), if and only if it is not a Gallai tree: some block is neither complete nor an odd cycle), Brooks' theorem for lists (Vizing 1976), and a library of blocks of graphs (blocks as maximal nonseparable vertex sets, cut vertices, unique block per edge, blocks meeting in at most one vertex, the block–cut tree of a connected graph, and the agreement of the block and induced-subgraph descriptions of Gallai trees).

</details>

#### The Gallai–Hasse–Roy–Vitaver theorem

[PALOMAR-2026-10-16-000015](https://palomar-registry.org/entry.html?id=PALOMAR-2026-10-16-000015&version=1) (v1) · [jtraverso/gallai-roy @ e737218](https://github.com/jtraverso/gallai-roy/tree/e737218bf80c3d3684d670f5f8aa9a8257e1a52f) · [archived copy](https://github.com/PalomarArchive/jtraverso--gallai-roy--242cd45a936c/tree/palomar/PALOMAR-2026-10-16-000015-v1/e737218bf80c3d3684d670f5f8aa9a8257e1a52f)

**Sources:**

* B. Roy, *Nombre chromatique et plus longs chemins d'un graphe*, Revue française d'informatique et de recherche opérationnelle 1 (1967), 129–132. [doi:10.1051/m2an/1967010501291](https://doi.org/10.1051/m2an/1967010501291) · [open PDF](https://www.esaim-m2an.org/articles/m2an/pdf/1967/03/m2an1967010501291.pdf) (Revue française d informatique et de recherche opérationnelle)
* M. Hasse, *Zur algebraischen Begründung der Graphentheorie. I*, Mathematische Nachrichten 28 (1965), 275–290. [doi:10.1002/mana.19650280503](https://doi.org/10.1002/mana.19650280503)
* T. Gallai, *On directed paths and circuits*, Theory of Graphs (Proc. Colloq. Tihany, 1966), Academic Press (1968), 115–118.
* L. M. Vitaver, *Determination of minimal coloring of vertices of a graph by means of Boolean powers of the incidence matrix*, Doklady Akademii Nauk SSSR 147 (1962), 758–759.

<details><summary>What is formalized</summary>

A Lean 4 / Mathlib formalization of the Gallai–Hasse–Roy–Vitaver theorem: if an orientation of a finite graph has no directed path on more than k vertices, the graph is k-colourable; and conversely every k-colourable graph has such an orientation. Hence the chromatic number is the minimum over orientations of the number of vertices of a longest directed path.

</details>

#### Kneser's conjecture and the octahedral Tucker lemma

[PALOMAR-2026-10-20-000006](https://palomar-registry.org/entry.html?id=PALOMAR-2026-10-20-000006&version=1) (v1) · [jtraverso/kneser-lovasz @ 6699c87](https://github.com/jtraverso/kneser-lovasz/tree/6699c87d87f4ddb159fc42271263fc429e63004a) · [archived copy](https://github.com/PalomarArchive/jtraverso--kneser-lovasz--c99016c66bcc/tree/palomar/PALOMAR-2026-10-20-000006-v1/6699c87d87f4ddb159fc42271263fc429e63004a)

**Sources:**

* L. Lovász, *Kneser's conjecture, chromatic number, and homotopy*, Journal of Combinatorial Theory, Series A 25 (1978), 319–324. [doi:10.1016/0097-3165(78)90022-5](https://doi.org/10.1016/0097-3165(78)90022-5) · [open PDF](https://www.sciencedirect.com/science/article/pii/0097316578900225/pdf) (Journal of Combinatorial Theory Series A)
* Jiří Matoušek, *A combinatorial proof of Kneser's conjecture*, Combinatorica 24 (2004), 163–170. [doi:10.1007/s00493-004-0011-1](https://doi.org/10.1007/s00493-004-0011-1) · [open version](http://hdl.handle.net/20.500.11850/50671) (Repository for Publications and Research Data (ETH Zurich))
* Robert M. Freund, Michael J. Todd, *A constructive proof of Tucker's combinatorial lemma*, Journal of Combinatorial Theory, Series A 30 (1981), 321–325. [doi:10.1016/0097-3165(81)90027-3](https://doi.org/10.1016/0097-3165(81)90027-3) · free to read at the publisher

<details><summary>Background references</summary>

* Ky Fan, *A generalization of Tucker's combinatorial lemma with topological applications*, Annals of Mathematics 56 (1952), 431–437. [doi:10.2307/1969651](https://doi.org/10.2307/1969651)
* Jiří Matoušek, *Using the Borsuk–Ulam Theorem*, Springer (2008), Sections 2.3 and 3.3. [doi:10.1007/978-3-540-76649-0](https://doi.org/10.1007/978-3-540-76649-0)

</details>

<details><summary>What is formalized</summary>

A Lean 4 / Mathlib formalization of Lovász's theorem (Kneser's conjecture): for 0 < k and 2k ≤ n the Kneser graph KG(n, k) of k-subsets of an n-set, adjacent when disjoint, has chromatic number exactly n − 2k + 2; proved combinatorially from the octahedral Tucker lemma (an antipodal labelling of the nonzero sign vectors of length n by nonzero integers in [−m, m] with m < n has a complementary pair x ≼ y with λ(x) = −λ(y)), which is itself proved by Ky Fan's parity argument. Mathlib has neither Kneser graphs nor Tucker's lemma.

</details>

#### Jin's theorem on dense triangle-free graphs

[PALOMAR-2026-10-20-000012](https://palomar-registry.org/entry.html?id=PALOMAR-2026-10-20-000012&version=1) (v1) · [jtraverso/jin-triangle-free @ ae47df0](https://github.com/jtraverso/jin-triangle-free/tree/ae47df0ddb29c58a71afed658f9bf74aef1b6e90) · [archived copy](https://github.com/PalomarArchive/jtraverso--jin-triangle-free--8d9fbb5efd5d/tree/palomar/PALOMAR-2026-10-20-000012-v1/ae47df0ddb29c58a71afed658f9bf74aef1b6e90)

**Sources:**

* G. P. Jin, *Triangle-free four-chromatic graphs*, Discrete Mathematics 145 (1995), 151–170. [doi:10.1016/0012-365X(94)00063-O](https://doi.org/10.1016/0012-365X(94)00063-O) · [open PDF](https://www.sciencedirect.com/science/article/pii/0012365X9400063O/pdf) (Discrete Mathematics)
* R. Häggkvist, *Odd cycles of specified length in non-bipartite graphs*, Graph Theory (Cambridge, 1981), North-Holland Mathematics Studies 62 (1982), 89–99. [doi:10.1016/S0304-0208(08)73552-7](https://doi.org/10.1016/S0304-0208(08)73552-7)

<details><summary>Background references</summary>

* C. C. Chen, G. P. Jin, K. M. Koh, *Triangle-free graphs with large degree*, Combinatorics, Probability and Computing 6 (1997), 381–396. [doi:10.1017/S0963548397003167](https://doi.org/10.1017/S0963548397003167)
* B. Andrásfai, P. Erdős, V. T. Sós, *On the connection between chromatic number, maximal clique and minimal degree of a graph*, Discrete Mathematics 8 (1974), 205–218. [doi:10.1016/0012-365X(74)90133-2](https://doi.org/10.1016/0012-365X(74)90133-2) · free to read at the publisher

</details>

<details><summary>What is formalized</summary>

A Lean 4 / Mathlib formalization of Jin's theorem: a finite triangle-free graph on n vertices with minimum degree greater than 10n/29 is 3-colourable; and of its sharpness: for every m ≥ 1 the blow-up of the Grötzsch graph with weights 3m, 2m, 4m is a triangle-free 10m-regular graph on 29m vertices that is not 3-colourable (Häggkvist). This extends the case r = 2 of the Andrásfai–Erdős–Sós theorem, which is in Mathlib. Mathlib does not have Jin's theorem.

</details>

#### Lovász's perfect graph theorems

[PALOMAR-2026-10-21-000007](https://palomar-registry.org/entry.html?id=PALOMAR-2026-10-21-000007&version=1) (v1) · [jtraverso/perfect-graphs @ 7969224](https://github.com/jtraverso/perfect-graphs/tree/796922460172c4e51c39c96575d03957652c0bab) · [archived copy](https://github.com/PalomarArchive/jtraverso--perfect-graphs--f01c6e39f696/tree/palomar/PALOMAR-2026-10-21-000007-v1/796922460172c4e51c39c96575d03957652c0bab)

**Sources:**

* L. Lovász, *Normal hypergraphs and the perfect graph conjecture*, Discrete Mathematics 2 (1972), 253–267. [doi:10.1016/0012-365X(72)90006-4](https://doi.org/10.1016/0012-365X(72)90006-4) · [open PDF](https://www.sciencedirect.com/science/article/pii/0012365X72900064/pdf) (Discrete Mathematics)
* L. Lovász, *A characterization of perfect graphs*, Journal of Combinatorial Theory, Series B 13 (1972), 95–98. [doi:10.1016/0095-8956(72)90045-7](https://doi.org/10.1016/0095-8956(72)90045-7) · [open PDF](https://www.sciencedirect.com/science/article/pii/0095895672900457/pdf) (Journal of Combinatorial Theory Series B)

<details><summary>Background references</summary>

* G. S. Gasparian, *Minimal imperfect graphs: a simple approach*, Combinatorica 16 (1996), 209–212. [doi:10.1007/BF01844846](https://doi.org/10.1007/BF01844846)

</details>

<details><summary>What is formalized</summary>

A Lean 4 / Mathlib formalization of Lovász's 1972 theorems on perfect graphs: a finite simple graph is perfect (every induced subgraph has chromatic number equal to its clique number) if and only if |S| ≤ α(G[S]) · ω(G[S]) for every vertex set S; and the perfect graph theorem conjectured by Berge, that a finite graph is perfect if and only if its complement is perfect. The proof follows Gasparian's linear-algebra argument. Mathlib has chromatic, clique and independence numbers but no perfect graphs.

</details>

#### Stanley's acyclic orientations and chromatic reciprocity

[PALOMAR-2026-10-28-000009](https://palomar-registry.org/entry.html?id=PALOMAR-2026-10-28-000009&version=1) (v1) · [jtraverso/stanley @ 48d36cb](https://github.com/jtraverso/stanley/tree/48d36cbaa54d14443f99b57776ce65f1f31c8331) · [archived copy](https://github.com/PalomarArchive/jtraverso--stanley--df253fa631b4/tree/palomar/PALOMAR-2026-10-28-000009-v1/48d36cbaa54d14443f99b57776ce65f1f31c8331)

**Sources:**

* Richard P. Stanley, *Acyclic orientations of graphs*, Discrete Mathematics 5 (1973), 171–178; author-hosted 2006 reprint at https://math.mit.edu/~rstan/pubs/pubfiles/18.pdf. [doi:10.1016/0012-365X(73)90108-8](https://doi.org/10.1016/0012-365X(73)90108-8) · [open PDF](https://www.sciencedirect.com/science/article/pii/0012365X73901088/pdf) (Discrete Mathematics)

<details><summary>What is formalized</summary>

For every finite simple graph and k ≥ 0, the signed evaluation (−1)^n χ_G(−k) counts acyclic orientations paired with weakly compatible Fin k colorings (Stanley 1973, Theorem 1.2); at k = 1 it counts acyclic orientations (Corollary 1.3). Includes positive-evaluation correctness, induced-subgraph convolution, and the finite equivalence between well-foundedness and no directed cycles.

</details>

### Edge colouring and list colouring

#### Vizing's theorem and equitable edge colourings

[PALOMAR-2026-10-15-000004](https://palomar-registry.org/entry.html?id=PALOMAR-2026-10-15-000004&version=2) (v2) · [jtraverso/vizing @ 33b2de8](https://github.com/jtraverso/vizing/tree/33b2de836095cf92bc1dec33b6f8787e4036bbc6) · [archived copy](https://github.com/PalomarArchive/jtraverso--vizing--01fa5f875100/tree/palomar/PALOMAR-2026-10-15-000004-v2/33b2de836095cf92bc1dec33b6f8787e4036bbc6)

**Sources:**

* Vadim G. Vizing, *On an estimate of the chromatic class of a p-graph (Russian)*, Diskretnyi Analiz 3 (1964), 25–30.
* Colin McDiarmid, *The Solution of a Timetabling Problem*, IMA Journal of Applied Mathematics 9 (1972), 23–34. [doi:10.1093/imamat/9.1.23](https://doi.org/10.1093/imamat/9.1.23)

<details><summary>Background references</summary>

* Dominique de Werra, *Equitable colorations of graphs*, Revue française d'informatique et de recherche opérationnelle, Série rouge 5 (1971), no. R3, 3–8. [doi:10.1051/m2an/197105r300031](https://doi.org/10.1051/m2an/197105r300031) · [open PDF](https://www.esaim-m2an.org/articles/m2an/pdf/1971/03/m2an197105R300031.pdf) (Revue française d informatique et de recherche opérationnelle Série rouge)
* Juan Pablo Traverso Gianini, *Paper IV (Erdős problem #81 for chordal graphs), Lean formalization freeze*, https://github.com/jtraverso/erdos-81-chordal-clique-partitions at ff2019f56a50cf300a6531c9f8d4a8fb1a541e3d, preprints/PAPER_IV/05_formalization.

</details>

<details><summary>What is formalized</summary>

A Lean 4 / Mathlib formalization of Vizing's theorem: every finite simple graph G has a proper edge colouring with Δ(G) + 1 colours, stated with Mathlib's line graph (G.lineGraph is (Δ(G) + 1)-colourable, hence χ'(G) ≤ Δ(G) + 1), proved with fans and Kempe chain exchanges. It also proves the equitable refinement: for every c ≥ Δ(G) + 1 there is a proper edge colouring with colours Fin c in which any two colour classes (including unused colours) differ in size by at most one (McDiarmid 1972), obtained by balancing a Vizing colouring with alternating-component moves that strictly decrease a square energy. Version 2 adds the lower bound Δ(G) ≤ χ'(G) (the edges at a vertex of maximum degree form a clique of the line graph) and hence the dichotomy χ'(G) ∈ {Δ(G), Δ(G) + 1} (class 1 / class 2).

</details>

#### Kőnig's theorems and Dilworth's theorem

[PALOMAR-2026-10-15-000019](https://palomar-registry.org/entry.html?id=PALOMAR-2026-10-15-000019&version=1) (v1) · [jtraverso/konig-edge-colouring @ 7c60f7e](https://github.com/jtraverso/konig-edge-colouring/tree/7c60f7efb69c1747aaf39e5dfa7a89d907cd84ef) · [archived copy](https://github.com/PalomarArchive/jtraverso--konig-edge-colouring--5e0f844003ab/tree/palomar/PALOMAR-2026-10-15-000019-v1/7c60f7efb69c1747aaf39e5dfa7a89d907cd84ef)

**Sources:**

* Dénes Kőnig, *Über Graphen und ihre Anwendung auf Determinantentheorie und Mengenlehre*, Mathematische Annalen 77 (1916), 453–465. [doi:10.1007/BF01456961](https://doi.org/10.1007/BF01456961) · [open version](https://zenodo.org/record/2395248) (Zenodo (CERN European Organization for Nuclear Research))
* Dénes Kőnig, *Gráfok és mátrixok*, Matematikai és Fizikai Lapok 38 (1931), 116–119.
* R. P. Dilworth, *A decomposition theorem for partially ordered sets*, Annals of Mathematics 51 (1950), 161–166. [doi:10.2307/1969503](https://doi.org/10.2307/1969503)
* L. Mirsky, *A dual of Dilworth's decomposition theorem*, American Mathematical Monthly 78 (1971), 876–877. [doi:10.1080/00029890.1971.11992886](https://doi.org/10.1080/00029890.1971.11992886)

<details><summary>Background references</summary>

* Fred Galvin, *A proof of Dilworth's chain decomposition theorem*, American Mathematical Monthly 101 (1994), 352–353. [doi:10.1080/00029890.1994.11996954](https://doi.org/10.1080/00029890.1994.11996954)

</details>

<details><summary>What is formalized</summary>

A Lean 4 / Mathlib formalization of Kőnig's edge-colouring theorem: the line graph of a finite bipartite graph G is Δ(G)-colourable, and its chromatic number (the chromatic index of G) equals Δ(G). The proof colours edges one at a time with partial proper edge colourings, recolouring by an a/b Kempe-chain swap whose correctness rests on a parity argument in the bipartite graph; the lower bound comes from the edges at a vertex of maximum degree, which are pairwise adjacent in the line graph. Also formalized: the Kőnig–Egerváry theorem (a finite bipartite graph has a matching and a vertex cover of the same size, via Hall's theorem with deficiency, plus weak duality for all finite graphs), Dilworth's theorem (an antichain A and a partition into |A| chains, by Galvin's induction) and Mirsky's dual theorem (a chain C and a partition into |C| antichains, by the height function).

</details>

#### Galvin's theorem for bipartite multigraphs, the Dinitz problem and stable matchings

[PALOMAR-2026-10-18-000029](https://palomar-registry.org/entry.html?id=PALOMAR-2026-10-18-000029&version=2) (v2) · [jtraverso/galvin-dinitz @ 84dcda4](https://github.com/jtraverso/galvin-dinitz/tree/84dcda4c2a760f2b52b7e813affe7e6968f8bfce) · [archived copy](https://github.com/PalomarArchive/jtraverso--galvin-dinitz--befd03f21f2b/tree/palomar/PALOMAR-2026-10-18-000029-v2/84dcda4c2a760f2b52b7e813affe7e6968f8bfce)

**Sources:**

* F. Galvin, *The List Chromatic Index of a Bipartite Multigraph*, Journal of Combinatorial Theory, Series B 63 (1995), 153–158. [doi:10.1006/jctb.1995.1011](https://doi.org/10.1006/jctb.1995.1011) · free to read at the publisher
* O. V. Borodin, A. V. Kostochka, D. R. Woodall, *List Edge and List Total Colourings of Multigraphs*, Journal of Combinatorial Theory, Series B 71 (1997), 184–204. [doi:10.1006/jctb.1997.1780](https://doi.org/10.1006/jctb.1997.1780)
* D. Gale, L. S. Shapley, *College Admissions and the Stability of Marriage*, The American Mathematical Monthly 69 (1962), 9–15. [doi:10.1080/00029890.1962.11989827](https://doi.org/10.1080/00029890.1962.11989827)

<details><summary>What is formalized</summary>

A Lean 4 / Mathlib formalization of Galvin’s theorem for finite bipartite multigraphs: every assignment of finite edge lists of size at least the maximum incidence degree admits a proper edge coloring, with parallel edges counted separately. It includes ordinary edge coloring with Δ colors and the matching lower bound, and the Borodin–Kostochka–Woodall theorem for local lists (lists of size at least the larger degree of the two ends of each edge suffice). The previously registered simple-graph Galvin theorem, Dinitz problem and Gale–Shapley stable matching theorem are retained.

</details>

#### The list chromatic index of complete graphs (Häggkvist–Janssen)

[PALOMAR-2026-10-15-000003](https://palomar-registry.org/entry.html?id=PALOMAR-2026-10-15-000003&version=1) (v1) · [jtraverso/haggkvist-janssen @ 807e08b](https://github.com/jtraverso/haggkvist-janssen/tree/807e08bd7c480d4fae80c1b78377d23989d39ab0) · [archived copy](https://github.com/PalomarArchive/jtraverso--haggkvist-janssen--3449623606b5/tree/palomar/PALOMAR-2026-10-15-000003-v1/807e08bd7c480d4fae80c1b78377d23989d39ab0)

**Sources:**

* Roland Häggkvist, Jeannette C. M. Janssen, *New Bounds on the List-Chromatic Index of the Complete Graph and Other Simple Graphs*, Combinatorics, Probability and Computing 6 (1997), 295–313. [doi:10.1017/S0963548397002927](https://doi.org/10.1017/S0963548397002927)

<details><summary>Background references</summary>

* Noga Alon, *Combinatorial Nullstellensatz*, Combinatorics, Probability and Computing 8 (1999), 7–29.

</details>

<details><summary>What is formalized</summary>

A Lean 4 / Mathlib formalization of the Häggkvist–Janssen theorem χ′ₗ(Kₙ) ≤ n: for arbitrary lists of at least n colours on the edges of the complete graph on n vertices (from an arbitrary colour type), there is a proper edge colouring, i.e. a colouring of Mathlib's line graph of ⊤, choosing every colour from the list of its edge. Orders 0 and 1 are included. The proof constructs an explicit local-rank certificate, shows by a forced-choice induction that the corresponding coefficient of an extended-star polynomial is nonzero, and applies Mathlib's combinatorial Nullstellensatz; it is an alternative presentation, not a literal translation of the article's argument.

</details>

#### Wagner's planarity criterion and list colouring of planar and K₅-minor-free graphs

[PALOMAR-2026-10-15-000005](https://palomar-registry.org/entry.html?id=PALOMAR-2026-10-15-000005&version=1) (v1) · [jtraverso/planar-list-colouring @ ec1eafb](https://github.com/jtraverso/planar-list-colouring/tree/ec1eafbc091713857eb5683a46e460902b2d47b3) · [archived copy](https://github.com/PalomarArchive/jtraverso--planar-list-colouring--03a15f1929ab/tree/palomar/PALOMAR-2026-10-15-000005-v1/ec1eafbc091713857eb5683a46e460902b2d47b3)

**Sources:**

* Klaus Wagner, *Über eine Eigenschaft der ebenen Komplexe*, Mathematische Annalen 114 (1937), 570–590.
* Riste Škrekovski, *Choosability of K5-minor-free graphs*, Discrete Mathematics 190 (1998), 223–226. [doi:10.1016/S0012-365X(98)00158-7](https://doi.org/10.1016/S0012-365X(98)00158-7) · [open PDF](https://www.sciencedirect.com/science/article/pii/S0012365X98001587/pdf) (Discrete Mathematics)
* David R. Wood, Svante Linusson, *Thomassen's Choosability Argument Revisited*, SIAM Journal on Discrete Mathematics 24 (2010), no. 4, 1632–1637. [arXiv:1005.5194](https://arxiv.org/abs/1005.5194) ([PDF](https://arxiv.org/pdf/1005.5194))
* Carsten Thomassen, *Every planar graph is 5-choosable*, Journal of Combinatorial Theory, Series B 62 (1994), 180–181.
* Zdeněk Dvořák, Luke Postle, *Correspondence coloring and its application to list-coloring planar graphs without cycles of lengths 4 to 8*, Journal of Combinatorial Theory, Series B 129 (2018), 38–54.
* Lingxi Li, Tao Wang, *An extension of Thomassen's result on choosability*, Applied Mathematics and Computation 425 (2022), 127100. [arXiv:2111.15220](https://arxiv.org/abs/2111.15220) ([PDF](https://arxiv.org/pdf/2111.15220))
* Margit Voigt, *List colourings of planar graphs*, Discrete Mathematics 120 (1993), 215–219. [doi:10.1016/0012-365X(93)90579-I](https://doi.org/10.1016/0012-365X(93)90579-I) · free to read at the publisher

<details><summary>Background references</summary>

* Kazimierz Kuratowski, *Sur le problème des courbes gauches en topologie*, Fundamenta Mathematicae 15 (1930), 271–283.
* Jack Edmonds, *A combinatorial representation for polyhedral surfaces*, Notices of the American Mathematical Society 7 (1960), 646.

</details>

<details><summary>What is formalized</summary>

A Lean 4 / Mathlib formalization of classical results on planar graphs and graphs without a K5 minor. (1) Wagner's theorem (1937): a finite graph is planar if and only if it has neither K5 nor K3,3 as a minor. (2) Škrekovski's theorem (1998): every finite graph without a K5 minor is 5-choosable, proved along the route of Wood and Linusson, and Thomassen's theorem (1994) that every finite planar graph is 5-choosable, as a corollary. (3) DP-colouring: every finite graph without a K5 minor (Li–Wang, 2022), hence every finite planar graph (Dvořák–Postle, 2018), is DP-5-colourable. (4) Voigt's theorem (1993): an explicit planar graph on 238 vertices with lists of four colours has no proper list colouring, so 5 cannot be lowered to 4; its planarity and non-colourability are checked by kernel reduction. (5) Wagner's equivalence of the Four Colour Theorem with Hadwiger's conjecture for K5 (neither side is proved). Planarity is defined combinatorially, by rotation systems of genus zero (Euler defect 0); as sanity checks K4 is planar and K5, K3,3 are not.

</details>

#### The Alon–Tarsi theorem and 3-choosability of planar bipartite graphs

[PALOMAR-2026-10-19-000013](https://palomar-registry.org/entry.html?id=PALOMAR-2026-10-19-000013&version=1) (v1) · [jtraverso/alon-tarsi-choosability @ 4ab98b1](https://github.com/jtraverso/alon-tarsi-choosability/tree/4ab98b11f340ea2160b34d0b57ef7102452b98cc) · [archived copy](https://github.com/PalomarArchive/jtraverso--alon-tarsi-choosability--e8601c7736f7/tree/palomar/PALOMAR-2026-10-19-000013-v1/4ab98b11f340ea2160b34d0b57ef7102452b98cc)

**Sources:**

* N. Alon, M. Tarsi, *Colorings and orientations of graphs*, Combinatorica 12 (1992), 125–134. [doi:10.1007/BF01204715](https://doi.org/10.1007/BF01204715)

<details><summary>Background references</summary>

* N. Alon, *Combinatorial Nullstellensatz*, Combinatorics, Probability and Computing 8 (1999), 7–29. [doi:10.1017/S0963548398003411](https://doi.org/10.1017/S0963548398003411)
* S. L. Hakimi, *On the degrees of the vertices of a directed graph*, Journal of the Franklin Institute 279 (1965), 290–308. [doi:10.1016/0016-0032(65)90340-6](https://doi.org/10.1016/0016-0032(65)90340-6)

</details>

<details><summary>What is formalized</summary>

A Lean 4 / Mathlib formalization of the Alon–Tarsi theorem: if a finite simple graph has an orientation whose numbers of even and odd Eulerian subdigraphs differ, then it can be properly coloured from any lists larger than the out-degrees; and of its corollary that every finite planar bipartite graph is 3-choosable. Planarity is the combinatorial notion of a plane map (a rotation system of genus zero) of the registered entry PALOMAR-2026-10-15-000005, whose definitions are reproduced verbatim in the Challenge. The proof uses the graph polynomial and Mathlib's Combinatorial Nullstellensatz, Euler's formula for plane maps, and an out-degree-2 orientation obtained from Hall's theorem.

</details>

#### Thomassen: planar graphs of girth at least five are 3-choosable

[PALOMAR-2026-10-28-000023](https://palomar-registry.org/entry.html?id=PALOMAR-2026-10-28-000023&version=1) (v1) · [jtraverso/thomassen-girth-five @ 12765f3](https://github.com/jtraverso/thomassen-girth-five/tree/12765f3362b48fbae04ac467d33873a4f2234083) · [archived copy](https://github.com/PalomarArchive/jtraverso--thomassen-girth-five--a221bbfeb126/tree/palomar/PALOMAR-2026-10-28-000023-v1/12765f3362b48fbae04ac467d33873a4f2234083)

**Sources:**

* Carsten Thomassen, *3-List-Coloring Planar Graphs of Girth 5*, Journal of Combinatorial Theory, Series B 64 (1995), 101–107. [doi:10.1006/jctb.1995.1027](https://doi.org/10.1006/jctb.1995.1027) · free to read at the publisher
* Ligang Jin, Yingli Kang, Eckhard Steffen, *Choosability in signed planar graphs*, Appendix, Theorem 5.1, pp. 11–13. [arXiv:1502.04561](https://arxiv.org/abs/1502.04561) ([PDF](https://arxiv.org/pdf/1502.04561))
* Daniel W. Cranston, *Graph Coloring Methods*, 2024, section 11.4, Theorem 11.13, printed pp. 322–328.
* Juan Pablo Traverso Gianini, *planar-list-colouring and grotzsch-ore registered Lean libraries*, jtraverso/planar-list-colouring at ec1eafbc091713857eb5683a46e460902b2d47b3; jtraverso/grotzsch-ore at ff6d5123c06e4c99bb6074e0a72e8be8d595eefa.
* Zdeněk Dvořák, Ken-ichi Kawarabayashi, *Choosability of planar graphs of girth 5*, 2011 preprint, Theorem 1 (attributed there to Thomassen). [arXiv:1109.2976](https://arxiv.org/abs/1109.2976) ([PDF](https://arxiv.org/pdf/1109.2976))
* Richard Rado, *Axiomatic Treatment of Rank in Infinite Sets*, Canadian Journal of Mathematics 1 (1949), 337–343. [doi:10.4153/CJM-1949-031-1](https://doi.org/10.4153/CJM-1949-031-1) · [open PDF](https://www.cambridge.org/core/services/aop-cambridge-core/content/view/93214C375DB3E3D1839423F445075EEB/S0008414X00037135a.pdf/div-class-title-axiomatic-treatment-of-rank-in-infinite-sets-div.pdf) (Canadian Journal of Mathematics)
* N. G. de Bruijn, Paul Erdős, *A colour problem for infinite graphs and a problem in the theory of relations*, Proceedings KNAW, Series A 54 (1951), 371–373.
* Nabiha Asghar, *Grötzsch's Theorem*, University of Waterloo MMath research essay (2012), Lemma 3.2.3, seven-cycle specialization.

<details><summary>What is formalized</summary>

Finite planar simple graphs of extended girth at least five are 3-choosable over arbitrary colour types. Includes a complete six-vertex boundary-extension induction, actual induced-face geometry and residual list-colouring infrastructure. Additional results expose the short-path theorem, derive an infinite finite-list compactness consequence, extend arbitrary five/six-cycles, and extend outer seven-cycles. The full original Theorem 2.1 and Corollary 2.2 are also proved, including arbitrary allowed fixed-edge colours and all exterior components.

</details>

#### The Pippenger–Spencer theorem on the chromatic index of hypergraphs

[PALOMAR-2026-10-28-000018](https://palomar-registry.org/entry.html?id=PALOMAR-2026-10-28-000018&version=1) (v1) · [jtraverso/pippenger-spencer @ 4cca4e3](https://github.com/jtraverso/pippenger-spencer/tree/4cca4e3c641619b1622ea60f58c57dc0c28ffdbb) · [archived copy](https://github.com/PalomarArchive/jtraverso--pippenger-spencer--aaba98952e76/tree/palomar/PALOMAR-2026-10-28-000018-v1/4cca4e3c641619b1622ea60f58c57dc0c28ffdbb)

**Sources:**

* Nicholas Pippenger, Joel Spencer, *Asymptotic behavior of the chromatic index for hypergraphs*, Journal of Combinatorial Theory, Series A 51 (1989), 24–42. [doi:10.1016/0097-3165(89)90074-5](https://doi.org/10.1016/0097-3165(89)90074-5) · free to read at the publisher

<details><summary>Background references</summary>

* Stefan Ehard, Stefan Glock, Felix Joos, *Pseudorandom hypergraph matchings*, Combinatorics, Probability and Computing 29 (2020), 868–885; arXiv:1907.09946. [doi:10.1017/S0963548320000280](https://doi.org/10.1017/S0963548320000280) · [open PDF](https://www.cambridge.org/core/services/aop-cambridge-core/content/view/AE0DE17C95900E7DD3F221E2C17FE203/S0963548320000280a.pdf/div-class-title-pseudorandom-hypergraph-matchings-div.pdf) (Combinatorics Probability Computing) · [arXiv:1907.09946](https://arxiv.org/abs/1907.09946) ([PDF](https://arxiv.org/pdf/1907.09946))

</details>

<details><summary>What is formalized</summary>

A Lean 4 / Mathlib formalization of the theorem of Pippenger and Spencer (1989): for r ≥ 2 and ε > 0 there are μ > 0 and D₀ such that every r-uniform hypergraph whose degrees lie in [(1 − μ)D, D] and whose codegrees are at most μD, with D ≥ D₀, has chromatic index at most (1 + ε)D. A second theorem gives an explicit polynomial error: if the maximum degree is at most D, the codegrees are at most D^{1−δ} and there are at most exp(D^γ) edges, then the chromatic index is at most D + D^{1−γ} for some γ = γ(r, δ) > 0. The proofs build on the author's registered formalization of Ehard–Glock–Joos (PALOMAR-2026-10-17-000004): batches of the trimmed Rödl nibble with the Lovász Local Lemma for the first theorem, and the pseudorandom matching theorem (Ehard–Glock–Joos, Theorem 1.2) applied to an auxiliary colour hypergraph for the second. Mathlib does not contain these results.

</details>

#### Shannon's theorem on edge colourings of multigraphs

[PALOMAR-2026-10-29-000023](https://palomar-registry.org/entry.html?id=PALOMAR-2026-10-29-000023&version=1) (v1) · [jtraverso/shannon-edge-colouring @ d590cfe](https://github.com/jtraverso/shannon-edge-colouring/tree/d590cfeb50d88710b454905f896aab928fcb5156) · [archived copy](https://github.com/PalomarArchive/jtraverso--shannon-edge-colouring--7112faf48c4d/tree/palomar/PALOMAR-2026-10-29-000023-v1/d590cfeb50d88710b454905f896aab928fcb5156)

**Sources:**

* Claude E. Shannon, *A theorem on coloring the lines of a network*, Journal of Mathematics and Physics 28 (1949), 148–152. [doi:10.1002/sapm1949281148](https://doi.org/10.1002/sapm1949281148)

<details><summary>What is formalized</summary>

A Lean 4 / Mathlib formalization of Shannon's theorem (1949): every finite loopless multigraph of maximum degree at most Δ has a proper edge colouring with ⌊3Δ/2⌋ colours; and its sharpness: for every Δ the Shannon triangle (three vertices with ⌊Δ/2⌋, ⌊Δ/2⌋ and ⌈Δ/2⌉ parallel edges between the three pairs) has maximum degree at most Δ and no proper edge colouring with fewer than ⌊3Δ/2⌋ colours. Multigraphs are edge families ends : ι → V × V (parallel edges allowed), a lighter representation than Mathlib's multigraph structure Graph α β (Mathlib.Combinatorics.Graph.Basic: vertex and edge sets with an incidence relation IsLink), which at the pinned revision has no degrees or edge colourings; no bridge to Graph α β is proved. Neither result is in Mathlib.

</details>

### Planarity, minors and graph classes

#### Kuratowski's theorem

[PALOMAR-2026-10-15-000018](https://palomar-registry.org/entry.html?id=PALOMAR-2026-10-15-000018&version=1) (v1) · [jtraverso/kuratowski @ 696ec89](https://github.com/jtraverso/kuratowski/tree/696ec897a9b91933037767d897670aa30ba3683a) · [archived copy](https://github.com/PalomarArchive/jtraverso--kuratowski--c5380f41889a/tree/palomar/PALOMAR-2026-10-15-000018-v1/696ec897a9b91933037767d897670aa30ba3683a)

**Sources:**

* Kazimierz Kuratowski, *Sur le problème des courbes gauches en Topologie*, Fundamenta Mathematicae 15 (1930), 271–283. [doi:10.4064/fm-15-1-271-283](https://doi.org/10.4064/fm-15-1-271-283) · [open PDF](https://www.impan.pl/shop/publication/transaction/download/product/92829?download.pdf) (Fundamenta Mathematicae)

<details><summary>Background references</summary>

* Klaus Wagner, *Über eine Eigenschaft der ebenen Komplexe*, Mathematische Annalen 114 (1937), 570–590.

</details>

<details><summary>What is formalized</summary>

A Lean 4 / Mathlib formalization of Kuratowski's theorem: a finite graph is planar if and only if it contains no subdivision of K5 and no subdivision of K3,3. Planarity is the combinatorial notion (a rotation system of genus zero). The proof combines Wagner's minor characterization (from the author's planarity library) with three new lemmas: a subdivision of any finite graph H gives H as a minor; a K3,3 minor gives a K3,3 subdivision; a K5 minor gives a K5 or a K3,3 subdivision. The last two rest on joining up to four terminals inside a connected branch set to one centre or to two adjacent centres by internally disjoint paths.

</details>

#### Mader's theorem and Hadwiger's conjecture for t ≤ 4

[PALOMAR-2026-10-16-000001](https://palomar-registry.org/entry.html?id=PALOMAR-2026-10-16-000001&version=1) (v1) · [jtraverso/hadwiger-mader @ cb10154](https://github.com/jtraverso/hadwiger-mader/tree/cb10154cd439a419d0bbf34052839dd27242b619) · [archived copy](https://github.com/PalomarArchive/jtraverso--hadwiger-mader--a4b96dfb7362/tree/palomar/PALOMAR-2026-10-16-000001-v1/cb10154cd439a419d0bbf34052839dd27242b619)

**Sources:**

* W. Mader, *Homomorphieeigenschaften und mittlere Kantendichte von Graphen*, Mathematische Annalen 174 (1967), 265–268. [doi:10.1007/BF01364272](https://doi.org/10.1007/BF01364272)
* G. A. Dirac, *A property of 4-chromatic graphs and some remarks on critical graphs*, Journal of the London Mathematical Society 27 (1952), 85–92. [doi:10.1112/jlms/s1-27.1.85](https://doi.org/10.1112/jlms/s1-27.1.85)
* H. Hadwiger, *Über eine Klassifikation der Streckenkomplexe*, Vierteljahrsschrift der Naturforschenden Gesellschaft in Zürich 88 (1943), 133–142.

<details><summary>Background references</summary>

* Reinhard Diestel, *Graph Theory (5th edition)*, Graduate Texts in Mathematics 173, Springer (2017). [doi:10.1007/978-3-662-53622-3](https://doi.org/10.1007/978-3-662-53622-3)

</details>

<details><summary>What is formalized</summary>

A Lean 4 / Mathlib formalization of Mader's theorem (a nonempty finite graph of average degree at least 2^(r−2) has a K_r minor), of Dirac's lemma (a graph without a K4 minor has a vertex of degree at most two, hence at most 2n − 3 edges for n ≥ 2), and of Hadwiger's conjecture for t ≤ 4 (graphs without a K3 minor are 2-colourable, graphs without a K4 minor are 3-colourable). Minors are branch-set models.

</details>

#### Chordal, split, threshold and cograph structure

[PALOMAR-2026-10-18-000006](https://palomar-registry.org/entry.html?id=PALOMAR-2026-10-18-000006&version=1) (v1) · [jtraverso/chordal-split-threshold-graphs @ ed65dcd](https://github.com/jtraverso/chordal-split-threshold-graphs/tree/ed65dcdc7339767d3e8e412420abbf54eae65ddb) · [archived copy](https://github.com/PalomarArchive/jtraverso--chordal-split-threshold-graphs--600d961f6749/tree/palomar/PALOMAR-2026-10-18-000006-v1/ed65dcdc7339767d3e8e412420abbf54eae65ddb)

**Sources:**

* G. A. Dirac, *On rigid circuit graphs*, Abhandlungen aus dem Mathematischen Seminar der Universität Hamburg 25 (1961), 71–76. [doi:10.1007/BF02992776](https://doi.org/10.1007/BF02992776)
* D. R. Fulkerson, O. A. Gross, *Incidence matrices and interval graphs*, Pacific Journal of Mathematics 15 (1965), 835–855. [doi:10.2140/pjm.1965.15.835](https://doi.org/10.2140/pjm.1965.15.835) · [open PDF](http://msp.org/pjm/1965/15-3/pjm-v15-n3-p11-s.pdf) (Pacific Journal of Mathematics)
* F. Gavril, *The intersection graphs of subtrees in trees are exactly the chordal graphs*, Journal of Combinatorial Theory, Series B 16 (1974), 47–56. [doi:10.1016/0095-8956(74)90094-X](https://doi.org/10.1016/0095-8956(74)90094-X) · [open PDF](https://www.sciencedirect.com/science/article/pii/009589567490094X/pdf) (Journal of Combinatorial Theory Series B)
* S. Földes, P. L. Hammer, *Split graphs*, Proceedings of the 8th Southeastern Conference on Combinatorics, Graph Theory and Computing (1977), Congressus Numerantium XIX, 311–315.
* V. Chvátal, P. L. Hammer, *Aggregation of Inequalities in Integer Programming*, Annals of Discrete Mathematics 1 (1977), 145–162. [doi:10.1016/S0167-5060(08)70731-3](https://doi.org/10.1016/S0167-5060(08)70731-3)

<details><summary>Background references</summary>

* Reinhard Diestel, *Graph Theory*, Graduate Texts in Mathematics 173, 5th edition, Springer (2017), Chapter 12. [doi:10.1007/978-3-662-53622-3](https://doi.org/10.1007/978-3-662-53622-3)

</details>

<details><summary>What is formalized</summary>

A Lean 4 / Mathlib formalization of classical structure theorems for finite simple graphs. Chordal graphs: every minimal a–b separator is a clique, a nonempty finite chordal graph has a simplicial vertex, and a connected non-complete one has two non-adjacent simplicial vertices (Dirac 1961); a finite graph is chordal iff it has a perfect elimination order (Fulkerson–Gross 1965), iff it is the intersection graph of subtrees of a finite tree (Gavril 1974); a nonempty finite chordal graph has treewidth ω − 1, and every finite graph has ω ≤ tw + 1. Split graphs: split iff the graph and its complement are chordal, iff no induced 2K₂, C₄ or C₅ (Földes–Hammer 1977). Threshold graphs: threshold iff no induced 2K₂, C₄ or P₄ (Chvátal–Hammer 1977), iff split and a cograph (no induced P₄). Mathlib has none of these graph classes; their definitions are stated in the Challenge.

</details>

### Connectivity, orientations and flows

#### Menger's theorem, Hamiltonian cycles, long cycles and pancyclicity

[PALOMAR-2026-10-15-000020](https://palomar-registry.org/entry.html?id=PALOMAR-2026-10-15-000020&version=2) (v2) · [jtraverso/menger-hamiltonian @ 35c5f68](https://github.com/jtraverso/menger-hamiltonian/tree/35c5f684f9bfbd244bd0999ce725623ab571adb6) · [archived copy](https://github.com/PalomarArchive/jtraverso--menger-hamiltonian--0fd5dfe41e84/tree/palomar/PALOMAR-2026-10-15-000020-v2/35c5f684f9bfbd244bd0999ce725623ab571adb6)

**Sources:**

* Karl Menger, *Zur allgemeinen Kurventheorie*, Fundamenta Mathematicae 10 (1927), 96–115. [doi:10.4064/fm-10-1-96-115](https://doi.org/10.4064/fm-10-1-96-115) · [open PDF](https://www.impan.pl/shop/publication/transaction/download/product/92646?download.pdf) (Fundamenta Mathematicae)
* G. A. Dirac, *Some theorems on abstract graphs*, Proceedings of the London Mathematical Society (3) 2 (1952), 69–81. [doi:10.1112/plms/s3-2.1.69](https://doi.org/10.1112/plms/s3-2.1.69)
* Øystein Ore, *Note on Hamilton circuits*, American Mathematical Monthly 67 (1960), 55. [doi:10.2307/2308928](https://doi.org/10.2307/2308928)
* J. A. Bondy, V. Chvátal, *A method in graph theory*, Discrete Mathematics 15 (1976), 111–135. [doi:10.1016/0012-365X(76)90078-9](https://doi.org/10.1016/0012-365X(76)90078-9) · free to read at the publisher
* V. Chvátal, P. Erdős, *A note on Hamiltonian circuits*, Discrete Mathematics 2 (1972), 111–113. [doi:10.1016/0012-365X(72)90079-9](https://doi.org/10.1016/0012-365X(72)90079-9) · free to read at the publisher
* P. Erdős, T. Gallai, *On maximal paths and circuits of graphs*, Acta Mathematica Academiae Scientiarum Hungaricae 10 (1959), 337–356. [doi:10.1007/BF02024498](https://doi.org/10.1007/BF02024498)
* J. A. Bondy, *Pancyclic graphs I*, Journal of Combinatorial Theory, Series B 11 (1971), 80–84. [doi:10.1016/0095-8956(71)90016-5](https://doi.org/10.1016/0095-8956(71)90016-5) · [open PDF](https://www.sciencedirect.com/science/article/pii/0095895671900165/pdf) (Journal of Combinatorial Theory Series B)

<details><summary>Background references</summary>

* Reinhard Diestel, *Graph Theory (5th edition)*, Graduate Texts in Mathematics 173, Springer (2017). [doi:10.1007/978-3-662-53622-3](https://doi.org/10.1007/978-3-662-53622-3)

</details>

<details><summary>What is formalized</summary>

A Lean 4 / Mathlib formalization of Menger's theorem for finite graphs (set form with a minimum separator and as many vertex-disjoint paths, two-vertex form, edge form for Mathlib's IsEdgeReachable, and the global edge form for Mathlib's IsEdgeConnected) and of classical sufficient conditions for Hamiltonian cycles: the Bondy–Chvátal closure step, Ore's and Dirac's theorems, and the Chvátal–Erdős theorem (k-connected with independence number at most k implies Hamiltonian), whose proof uses Menger's theorem through the fan lemma. Version 2 adds the Erdős–Gallai theorems on long paths and cycles (no path on k vertices implies 2e ≤ (k − 2)n; no cycle of length at least k ≥ 3 implies 2e ≤ (k − 1)(n − 1)) and Bondy's pancyclicity theorem (a Hamiltonian graph with at least n²/4 edges is pancyclic or is K_{n/2,n/2}), proved on top of the same library.

</details>

#### Mader's theorem on highly connected subgraphs

[PALOMAR-2026-10-23-000016](https://palomar-registry.org/entry.html?id=PALOMAR-2026-10-23-000016&version=1) (v1) · [jtraverso/mader-connectivity @ b471abc](https://github.com/jtraverso/mader-connectivity/tree/b471abcdfbb303aabc1af26f4531e080729bb469) · [archived copy](https://github.com/PalomarArchive/jtraverso--mader-connectivity--54c8125a286e/tree/palomar/PALOMAR-2026-10-23-000016-v1/b471abcdfbb303aabc1af26f4531e080729bb469)

**Sources:**

* W. Mader, *Existenz n-fach zusammenhängender Teilgraphen in Graphen genügend großer Kantendichte*, Abhandlungen aus dem Mathematischen Seminar der Universität Hamburg 37 (1972), 86–97. [doi:10.1007/BF02993903](https://doi.org/10.1007/BF02993903)
* R. Diestel, *Graph Theory*, Graduate Texts in Mathematics 173, Springer, Theorem 1.4.3.

<details><summary>What is formalized</summary>

A Lean 4 / Mathlib formalization of Mader's 1972 theorem in the form of Diestel's Theorem 1.4.3: for k ≥ 1, every nonempty finite simple graph with average degree at least 4k has a (k + 1)-connected induced subgraph H with e(H)/|H| > e(G)/|G| − k. Vertex connectivity is defined by deletion of fewer than k vertices (same definition as in the Menger–Hamiltonicity entry). Mathlib does not contain vertex connectivity or this theorem.

</details>

#### Robbins' theorem on strongly connected orientations

[PALOMAR-2026-10-18-000022](https://palomar-registry.org/entry.html?id=PALOMAR-2026-10-18-000022&version=1) (v1) · [jtraverso/robbins-strong-orientation @ 076e734](https://github.com/jtraverso/robbins-strong-orientation/tree/076e734e9949720d3e4fcc2cc3cad4284871442c) · [archived copy](https://github.com/PalomarArchive/jtraverso--robbins-strong-orientation--f05c2621ca9e/tree/palomar/PALOMAR-2026-10-18-000022-v1/076e734e9949720d3e4fcc2cc3cad4284871442c)

**Sources:**

* H. E. Robbins, *A Theorem on Graphs, with an Application to a Problem of Traffic Control*, The American Mathematical Monthly 46 (1939), 281–283. [doi:10.2307/2303897](https://doi.org/10.2307/2303897)

<details><summary>What is formalized</summary>

A Lean 4 / Mathlib formalization of Robbins' theorem: a finite connected simple graph has a strongly connected orientation (a digraph with underlying graph G, never containing both u → v and v → u, in which every vertex reaches every other) if and only if no edge of it is a bridge. As a corollary, every finite 2-edge-connected graph on a nonempty vertex type has a strongly connected orientation. Mathlib has bridges, edge connectivity and digraphs, but not this theorem.

</details>

#### Nash-Williams' weak orientation theorem

[PALOMAR-2026-10-28-000004](https://palomar-registry.org/entry.html?id=PALOMAR-2026-10-28-000004&version=1) (v1) · [jtraverso/nash-williams-orientation @ 3412d88](https://github.com/jtraverso/nash-williams-orientation/tree/3412d885cf3ba6680770cb8014df96af8fa3d042) · [archived copy](https://github.com/PalomarArchive/jtraverso--nash-williams-orientation--96d643fb4df4/tree/palomar/PALOMAR-2026-10-28-000004-v1/3412d885cf3ba6680770cb8014df96af8fa3d042)

**Sources:**

* C. St. J. A. Nash-Williams, *On Orientations, Connectivity and Odd-Vertex-Pairings in Finite Graphs*, Canadian Journal of Mathematics 12 (1960), 555–567. [doi:10.4153/CJM-1960-049-6](https://doi.org/10.4153/CJM-1960-049-6) · [open PDF](https://www.cambridge.org/core/services/aop-cambridge-core/content/view/2B39912D1666161E4200E61E8F65DE2B/S0008414X00010191a.pdf/div-class-title-on-orientations-connectivity-and-odd-vertex-pairings-in-finite-graphs-div.pdf) (Canadian Journal of Mathematics)

<details><summary>Background references</summary>

* L. Lovász, *On some connectivity properties of Eulerian graphs*, Acta Mathematica Academiae Scientiarum Hungaricae 28 (1976), 129–138. [doi:10.1007/BF01902503](https://doi.org/10.1007/BF01902503)
* W. Mader, *A Reduction Method for Edge-Connectivity in Graphs*, Annals of Discrete Mathematics 3 (1978), 145–164. [doi:10.1016/S0167-5060(08)70504-1](https://doi.org/10.1016/S0167-5060(08)70504-1)

</details>

<details><summary>What is formalized</summary>

A Lean 4 / Mathlib formalization of Nash-Williams' weak orientation theorem (1960): every 2k-edge-connected finite graph has a k-arc-connected orientation, i.e. one in which every nonempty proper vertex set is left by at least k arcs. It is proved for finite loopless multigraphs given by an edge family, and stated for simple graphs with Mathlib's SimpleGraph.IsEdgeConnected and orientations as Mathlib Digraphs. The proof is by induction on the number of edges, with Mader's lemma (a minimally 2k-edge-connected multigraph has a vertex of degree 2k) and Lovász's splitting lemma, both proved in the project. Mathlib does not contain these results.

</details>

#### Jaeger's 4-flow and 8-flow theorems and Seymour's 6-flow theorem

[PALOMAR-2026-10-18-000009](https://palomar-registry.org/entry.html?id=PALOMAR-2026-10-18-000009&version=3) (v3) · [jtraverso/jaeger-four-flow @ 623dd0d](https://github.com/jtraverso/jaeger-four-flow/tree/623dd0dd718f93de06d4dc792e116dd32ef97553) · [archived copy](https://github.com/PalomarArchive/jtraverso--jaeger-four-flow--4443e53b8984/tree/palomar/PALOMAR-2026-10-18-000009-v3/623dd0dd718f93de06d4dc792e116dd32ef97553)

**Sources:**

* F. Jaeger, *Flows and generalized coloring theorems in graphs*, Journal of Combinatorial Theory, Series B 26 (1979), 205–216. [doi:10.1016/0095-8956(79)90057-1](https://doi.org/10.1016/0095-8956(79)90057-1) · free to read at the publisher
* P. D. Seymour, *Nowhere-zero 6-flows*, Journal of Combinatorial Theory, Series B 30 (1981), 130–135. [doi:10.1016/0095-8956(81)90058-7](https://doi.org/10.1016/0095-8956(81)90058-7) · [open PDF](https://www.sciencedirect.com/science/article/pii/0095895681900587/pdf) (Journal of Combinatorial Theory Series B)
* W. T. Tutte, *A contribution to the theory of chromatic polynomials*, Canadian Journal of Mathematics 6 (1954), 80–91. [doi:10.4153/CJM-1954-010-9](https://doi.org/10.4153/CJM-1954-010-9) · [open PDF](https://www.cambridge.org/core/services/aop-cambridge-core/content/view/E1EE1F053B494D08746F0EE23F736CC2/S0008414X00023543a.pdf/div-class-title-a-contribution-to-the-theory-of-chromatic-polynomials-div.pdf) (Canadian Journal of Mathematics)

<details><summary>Background references</summary>

* P. A. Kilpatrick, *Tutte's first colour-cycle conjecture*, Ph.D. thesis, University of Cape Town (1975).

</details>

<details><summary>What is formalized</summary>

A Lean 4 / Mathlib formalization of Jaeger's 4-flow theorem: every finite 4-edge-connected simple graph has a nowhere-zero integer 4-flow, i.e. an antisymmetric function on darts with values in {±1, ±2, ±3} that is conserved at every vertex. Also proved: a graph with two edge-disjoint spanning trees has its edges covered by two even subgraphs (a nowhere-zero ℤ₂ × ℤ₂-flow) and has a nowhere-zero integer 4-flow. Version 2 adds Jaeger's 8-flow theorem: every finite bridgeless graph has its edges covered by three even subgraphs and has a nowhere-zero integer 8-flow; conversely a graph with a nowhere-zero flow has no bridge. Version 3 adds Seymour's 6-flow theorem (every finite bridgeless graph has a nowhere-zero integer 6-flow) and Tutte's theorem relating group and integer flows (for k > 0, every nowhere-zero ℤ/k-flow φ lifts to a nowhere-zero integer k-flow ψ with ψ ≡ φ mod k, and conversely an integer k-flow reduces modulo k to a nowhere-zero ℤ/k-flow). Mathlib has no flows.

</details>

#### Nowhere-zero 3-flows in 6-edge-connected graphs

[PALOMAR-2026-10-28-000022](https://palomar-registry.org/entry.html?id=PALOMAR-2026-10-28-000022&version=1) (v1) · [jtraverso/three-flows @ 2e0bc7c](https://github.com/jtraverso/three-flows/tree/2e0bc7c111b2e6d05d81ce9bd1c2dc58a4184f4c) · [archived copy](https://github.com/PalomarArchive/jtraverso--three-flows--4989d8f20572/tree/palomar/PALOMAR-2026-10-28-000022-v1/2e0bc7c111b2e6d05d81ce9bd1c2dc58a4184f4c)

**Sources:**

* L. M. Lovász, C. Thomassen, Y. Wu, C.-Q. Zhang, *Nowhere-zero 3-flows and modulo k-orientations*, Journal of Combinatorial Theory, Series B 103 (2013), 587–598. [doi:10.1016/j.jctb.2013.06.003](https://doi.org/10.1016/j.jctb.2013.06.003) · [open PDF](https://www.sciencedirect.com/science/article/pii/S0095895613000506/pdf) (Journal of Combinatorial Theory Series B)

<details><summary>Background references</summary>

* C. Thomassen, *The weak 3-flow conjecture and the weak circular flow conjecture*, Journal of Combinatorial Theory, Series B 102 (2012), 521–529. [doi:10.1016/j.jctb.2011.09.003](https://doi.org/10.1016/j.jctb.2011.09.003) · [open PDF](https://www.sciencedirect.com/science/article/pii/S0095895611000955/pdf) (Journal of Combinatorial Theory Series B)
* W. T. Tutte, *A contribution to the theory of chromatic polynomials*, Canadian Journal of Mathematics 6 (1954), 80–91. [doi:10.4153/CJM-1954-010-9](https://doi.org/10.4153/CJM-1954-010-9) · [open PDF](https://www.cambridge.org/core/services/aop-cambridge-core/content/view/E1EE1F053B494D08746F0EE23F736CC2/S0008414X00023543a.pdf/div-class-title-a-contribution-to-the-theory-of-chromatic-polynomials-div.pdf) (Canadian Journal of Mathematics)

</details>

<details><summary>What is formalized</summary>

A Lean 4 / Mathlib formalization of the theorem of Lovász, Thomassen, Wu and Zhang: every finite 6-edge-connected simple graph has a nowhere-zero integer 3-flow (the weak 3-flow conjecture). The proof formalizes Theorem 3.1 of the paper (β-orientations of multigraphs modulo 3) and Tutte's lifting theorem. Only simple graphs are stated; the paper's multigraph version and its results on modulo k-orientations for k > 3 are not stated. Mathlib does not contain this theorem.

</details>

### Cycles and Hamiltonicity

#### Chvátal's and Pósa's degree conditions for Hamiltonian cycles

[PALOMAR-2026-10-18-000001](https://palomar-registry.org/entry.html?id=PALOMAR-2026-10-18-000001&version=1) (v1) · [jtraverso/chvatal-posa-hamiltonian @ 6be0ebd](https://github.com/jtraverso/chvatal-posa-hamiltonian/tree/6be0ebda7b457b85ad400f6d7f92ad156d6e7712) · [archived copy](https://github.com/PalomarArchive/jtraverso--chvatal-posa-hamiltonian--3158a08a16e2/tree/palomar/PALOMAR-2026-10-18-000001-v1/6be0ebda7b457b85ad400f6d7f92ad156d6e7712)

**Sources:**

* V. Chvátal, *On Hamilton's ideals*, Journal of Combinatorial Theory, Series B 12 (1972), 163–168. [doi:10.1016/0095-8956(72)90020-2](https://doi.org/10.1016/0095-8956(72)90020-2) · [open PDF](https://www.sciencedirect.com/science/article/pii/0095895672900202/pdf) (Journal of Combinatorial Theory Series B)
* L. Pósa, *A theorem concerning Hamilton lines*, Magyar Tudományos Akadémia Matematikai Kutató Intézetének Közleményei 7 (1962), 225–226.

<details><summary>Background references</summary>

* J. A. Bondy, V. Chvátal, *A method in graph theory*, Discrete Mathematics 15 (1976), 111–135. [doi:10.1016/0012-365X(76)90078-9](https://doi.org/10.1016/0012-365X(76)90078-9) · free to read at the publisher

</details>

<details><summary>What is formalized</summary>

A Lean 4 / Mathlib formalization of two classical degree-sequence conditions for Hamiltonicity of a finite simple graph on n ≥ 3 vertices with degrees d₁ ≤ ⋯ ≤ dₙ. Chvátal's theorem (1972): if for every i < n/2, dᵢ ≤ i implies d_{n−i} ≥ n − i, then the graph is Hamiltonian (stated without sorting: if at least i vertices have degree at most i, then at least i + 1 vertices have degree at least n − i). Pósa's theorem (1962): if for every k with 1 ≤ k < (n − 1)/2 fewer than k vertices have degree at most k, and, for odd n, at most (n − 1)/2 vertices have degree at most (n − 1)/2, then the graph is Hamiltonian. Mathlib has Hamiltonian cycles but neither theorem.

</details>

#### Dirac's theorem: k vertices of a k-connected graph lie on a common cycle

[PALOMAR-2026-10-18-000011](https://palomar-registry.org/entry.html?id=PALOMAR-2026-10-18-000011&version=1) (v1) · [jtraverso/dirac-common-cycle @ 3c9e996](https://github.com/jtraverso/dirac-common-cycle/tree/3c9e9966662cb99c0e4f11d771011bc904dc627f) · [archived copy](https://github.com/PalomarArchive/jtraverso--dirac-common-cycle--7eeee5978914/tree/palomar/PALOMAR-2026-10-18-000011-v1/3c9e9966662cb99c0e4f11d771011bc904dc627f)

**Sources:**

* G. A. Dirac, *In abstrakten Graphen vorhandene vollständige 4-Graphen und ihre Unterteilungen*, Mathematische Nachrichten 22 (1960), 61–85. [doi:10.1002/mana.19600220107](https://doi.org/10.1002/mana.19600220107)

<details><summary>What is formalized</summary>

A Lean 4 / Mathlib formalization of Dirac's 1960 theorem: in a k-connected finite simple graph with k ≥ 2 (more than k vertices, and connected after deleting any set of fewer than k vertices), any set of at most k vertices lies on a common cycle. In particular, in a 2-connected finite graph any two vertices lie on a common cycle. Cycles are Mathlib's `SimpleGraph.Walk.IsCycle`. Mathlib does not have this theorem.

</details>

#### The Erdős–Pósa theorem for cycles

[PALOMAR-2026-10-20-000003](https://palomar-registry.org/entry.html?id=PALOMAR-2026-10-20-000003&version=1) (v1) · [jtraverso/erdos-posa-cycles @ 67bfea6](https://github.com/jtraverso/erdos-posa-cycles/tree/67bfea6b3893ffdf57e76cd83c9c3538647bdec8) · [archived copy](https://github.com/PalomarArchive/jtraverso--erdos-posa-cycles--495ed139acca/tree/palomar/PALOMAR-2026-10-20-000003-v1/67bfea6b3893ffdf57e76cd83c9c3538647bdec8)

**Sources:**

* P. Erdős, L. Pósa, *On independent circuits contained in a graph*, Canadian Journal of Mathematics 17 (1965), 347–352. [doi:10.4153/CJM-1965-035-8](https://doi.org/10.4153/CJM-1965-035-8) · [open PDF](https://www.cambridge.org/core/services/aop-cambridge-core/content/view/00E165DD4E460BE00867629661177985/S0008414X00039316a.pdf/div-class-title-on-independent-circuits-contained-in-a-graph-div.pdf) (Canadian Journal of Mathematics)

<details><summary>Background references</summary>

* M. Simonovits, *A new proof and generalizations of a theorem of Erdős and Pósa on graphs without k+1 independent circuits*, Acta Mathematica Academiae Scientiarum Hungaricae 18 (1967), 191–206. [doi:10.1007/BF02020974](https://doi.org/10.1007/BF02020974)
* Reinhard Diestel, *Graph Theory (5th edition)*, Graduate Texts in Mathematics 173, Springer (2017), Section 2.3. [doi:10.1007/978-3-662-53622-3](https://doi.org/10.1007/978-3-662-53622-3)

</details>

<details><summary>What is formalized</summary>

A Lean 4 / Mathlib formalization of the Erdős–Pósa theorem: for every k, every finite simple graph either contains k vertex-disjoint cycles or has a set of at most c (k + 1)(log₂(k + 1) + 1) vertices meeting every cycle, for a fixed constant c (the proof gives c = 65); together with the qualitative Erdős–Pósa property and the easy converse that a feedback vertex set of size s rules out s + 1 disjoint cycles. Mathlib has acyclic graphs but not this theorem.

</details>

#### The Corrádi–Hajnal theorem on vertex-disjoint cycles

[PALOMAR-2026-10-29-000007](https://palomar-registry.org/entry.html?id=PALOMAR-2026-10-29-000007&version=1) (v1) · [jtraverso/corradi-hajnal @ 2b85adc](https://github.com/jtraverso/corradi-hajnal/tree/2b85adcc37a9a057fb0cb72bc08774027f9ea077) · [archived copy](https://github.com/PalomarArchive/jtraverso--corradi-hajnal--20f84b4c2e6d/tree/palomar/PALOMAR-2026-10-29-000007-v1/2b85adcc37a9a057fb0cb72bc08774027f9ea077)

**Sources:**

* K. Corrádi, A. Hajnal, *On the maximal number of independent circuits in a graph*, Acta Mathematica Academiae Scientiarum Hungaricae 14 (1963), 423–439. [doi:10.1007/BF01895727](https://doi.org/10.1007/BF01895727)

<details><summary>What is formalized</summary>

A Lean 4 / Mathlib formalization of the Corrádi–Hajnal theorem (1963): every finite simple graph on at least 3k vertices with minimum degree at least 2k contains k vertex-disjoint cycles. Cycles are closed walks that are cycles in Mathlib's sense; the theorem is also stated with the definition of disjoint cycles of the registered Erdős–Pósa entry (k pairwise disjoint vertex sets, each inducing a subgraph that is not acyclic). Both hypotheses are shown to be needed: for k ≥ 2 the complete graph on 3k − 1 vertices has minimum degree 3k − 2 ≥ 2k and no k disjoint cycles, and for m ≥ 2k the complete bipartite graph K_{2k−1, m} has at least 3k vertices and minimum degree 2k − 1 and no k disjoint cycles. Mathlib has cycles and minimum degree but not this theorem.

</details>

### Matchings, factors and polyhedral combinatorics

#### Petersen's theorem

[PALOMAR-2026-10-16-000004](https://palomar-registry.org/entry.html?id=PALOMAR-2026-10-16-000004&version=1) (v1) · [jtraverso/petersen-matching @ 77630d6](https://github.com/jtraverso/petersen-matching/tree/77630d6771d3f5a3da2185db2ff451f6c6ed5190) · [archived copy](https://github.com/PalomarArchive/jtraverso--petersen-matching--386afe9ae9e1/tree/palomar/PALOMAR-2026-10-16-000004-v1/77630d6771d3f5a3da2185db2ff451f6c6ed5190)

**Sources:**

* Julius Petersen, *Die Theorie der regulären graphs*, Acta Mathematica 15 (1891), 193–220. [doi:10.1007/BF02392606](https://doi.org/10.1007/BF02392606) · [open PDF](https://projecteuclid.org/journals/acta-mathematica/volume-15/issue-none/Die-Theorie-der-regul%c3%a4ren-graphs/10.1007/BF02392606.pdf) (Acta Mathematica)

<details><summary>Background references</summary>

* W. T. Tutte, *The factorization of linear graphs*, Journal of the London Mathematical Society 22 (1947), 107–111. [doi:10.1112/jlms/s1-22.2.107](https://doi.org/10.1112/jlms/s1-22.2.107)

</details>

<details><summary>What is formalized</summary>

A Lean 4 / Mathlib formalization of Petersen's theorem: a finite 3-regular graph in which no edge is a bridge has a perfect matching; moreover, every edge of such a graph lies in some perfect matching. Both statements are derived from Tutte's theorem (in Mathlib) by counting the edges that leave the odd components.

</details>

#### Berge's theorem, the Tutte–Berge formula and the Gallai–Edmonds theorem

[PALOMAR-2026-10-16-000011](https://palomar-registry.org/entry.html?id=PALOMAR-2026-10-16-000011&version=2) (v2) · [jtraverso/berge-matching @ f01d042](https://github.com/jtraverso/berge-matching/tree/f01d042c071c778fb3f432312356136a92369076) · [archived copy](https://github.com/PalomarArchive/jtraverso--berge-matching--b269b121c46f/tree/palomar/PALOMAR-2026-10-16-000011-v2/f01d042c071c778fb3f432312356136a92369076)

**Sources:**

* Claude Berge, *Two theorems in graph theory*, Proceedings of the National Academy of Sciences of the USA 43 (1957), 842–844. [doi:10.1073/pnas.43.9.842](https://doi.org/10.1073/pnas.43.9.842) · [open version](http://europepmc.org/pmc/articles/PMC534337) (Europe PMC (PubMed Central))
* Claude Berge, *Sur le couplage maximum d'un graphe*, Comptes Rendus de l'Académie des Sciences de Paris 247 (1958), 258–259.
* Jack Edmonds, *Paths, trees, and flowers*, Canadian Journal of Mathematics 17 (1965), 449–467. [doi:10.4153/CJM-1965-045-4](https://doi.org/10.4153/CJM-1965-045-4) · [open PDF](https://www.cambridge.org/core/services/aop-cambridge-core/content/view/08B492B72322C4130AE800C0610E0E21/S0008414X00039419a.pdf/div-class-title-paths-trees-and-flowers-div.pdf) (Canadian Journal of Mathematics)
* Tibor Gallai, *Maximale Systeme unabhängiger Kanten*, Magyar Tudományos Akadémia Matematikai Kutató Intézetének Közleményei 9 (1964), 401–413.

<details><summary>Background references</summary>

* László Lovász, Michael D. Plummer, *Matching Theory*, AMS Chelsea Publishing (2009), Chapter 3. [doi:10.1090/chel/367](https://doi.org/10.1090/chel/367)
* W. T. Tutte, *The factorization of linear graphs*, Journal of the London Mathematical Society 22 (1947), 107–111. [doi:10.1112/jlms/s1-22.2.107](https://doi.org/10.1112/jlms/s1-22.2.107)

</details>

<details><summary>What is formalized</summary>

A Lean 4 / Mathlib formalization of Berge's augmenting path theorem (a matching is maximum if and only if there is no augmenting path) and of the Tutte–Berge formula (the maximum size of a matching is the minimum over vertex sets U of (|V| + |U| − odd(G − U)) / 2), with the weak inequality for all matchings and vertex sets; the formula is derived from Mathlib's Tutte theorem by adding universal vertices. Version 2 adds the Gallai–Edmonds structure theorem: with D the vertices missed by some maximum matching, A their neighbours outside D and C the rest, the components of G[D] are factor-critical, G[C] has a perfect matching, every maximum matching matches A into distinct components of G[D], and 2ν(G) = |V| + |A| − c(G[D]).

</details>

#### Euler's theorem on Eulerian circuits and trails, and Petersen's 2-factor theorem

[PALOMAR-2026-10-16-000016](https://palomar-registry.org/entry.html?id=PALOMAR-2026-10-16-000016&version=1) (v1) · [jtraverso/euler-petersen @ 02c3f1a](https://github.com/jtraverso/euler-petersen/tree/02c3f1a5327c5f066938860bb07e9fce226b36ca) · [archived copy](https://github.com/PalomarArchive/jtraverso--euler-petersen--780912a29df2/tree/palomar/PALOMAR-2026-10-16-000016-v1/02c3f1a5327c5f066938860bb07e9fce226b36ca)

**Sources:**

* Leonhard Euler, *Solutio problematis ad geometriam situs pertinentis*, Commentarii academiae scientiarum Petropolitanae 8 (1741), 128–140; https://scholarlycommons.pacific.edu/euler-works/53/.
* Carl Hierholzer, *Ueber die Möglichkeit, einen Linienzug ohne Wiederholung und ohne Unterbrechung zu umfahren*, Mathematische Annalen 6 (1873), 30–32. [doi:10.1007/BF01442866](https://doi.org/10.1007/BF01442866) · [open version](https://zenodo.org/record/1447429) (Zenodo (CERN European Organization for Nuclear Research))
* Julius Petersen, *Die Theorie der regulären graphs*, Acta Mathematica 15 (1891), 193–220. [doi:10.1007/BF02392606](https://doi.org/10.1007/BF02392606) · [open PDF](https://projecteuclid.org/journals/acta-mathematica/volume-15/issue-none/Die-Theorie-der-regul%c3%a4ren-graphs/10.1007/BF02392606.pdf) (Acta Mathematica)

<details><summary>Background references</summary>

* Philip Hall, *On representatives of subsets*, Journal of the London Mathematical Society 10 (1935), 26–30. [doi:10.1112/jlms/s1-10.37.26](https://doi.org/10.1112/jlms/s1-10.37.26)
* Tim Räz, *Mathematical Explanations in Euler's Königsberg*, https://philsci-archive.pitt.edu/11094/ (2014); later version: European Journal for Philosophy of Science (2018).

</details>

<details><summary>What is formalized</summary>

A Lean 4 / Mathlib formalization of the classical characterization of Eulerian graphs and of Petersen's 2-factor theorem, for finite simple graphs. (1) Euler–Hierholzer: a finite connected graph has an Eulerian circuit if and only if every vertex has even degree, and the circuit can start at any prescribed vertex. (2) Eulerian trails: a finite connected graph has an Eulerian trail if and only if it has 0 or 2 vertices of odd degree; when the odd vertices are exactly a and b, there is an Eulerian trail from a to b. (3) Eulerian orientations: if every degree is even, the edges can be oriented so that every vertex has equal in- and out-degree. (4) Petersen's 2-factor theorem (1891): every finite 2k-regular graph is the edge-disjoint union of k spanning 2-regular subgraphs. The proof of (4) is built on (1)–(3): the graph is decomposed into edge-disjoint closed trails (using the closed-trail lemma behind the Euler theorems), oriented along them, and the resulting k-regular digraph is split into k permutations by Hall's marriage theorem; each permutation yields a 2-factor. Mathlib already contained the necessity directions of (1) and (2); their sufficiency directions were listed there as open TODO items.

</details>

#### Tutte's f-factor theorem

[PALOMAR-2026-10-18-000005](https://palomar-registry.org/entry.html?id=PALOMAR-2026-10-18-000005&version=1) (v1) · [jtraverso/tutte-f-factor @ dc3bbce](https://github.com/jtraverso/tutte-f-factor/tree/dc3bbce463c80c499d3e9fa072d13f9145d907d0) · [archived copy](https://github.com/PalomarArchive/jtraverso--tutte-f-factor--c791dc403ea0/tree/palomar/PALOMAR-2026-10-18-000005-v1/dc3bbce463c80c499d3e9fa072d13f9145d907d0)

**Sources:**

* W. T. Tutte, *The Factors of Graphs*, Canadian Journal of Mathematics 4 (1952), 314–328. [doi:10.4153/CJM-1952-028-2](https://doi.org/10.4153/CJM-1952-028-2) · [open PDF](https://www.cambridge.org/core/services/aop-cambridge-core/content/view/320CE524F3E9AA34F0BF6A824642C34B/S0008414X00036270a.pdf/div-class-title-the-factors-of-graphs-div.pdf) (Canadian Journal of Mathematics)
* W. T. Tutte, *A Short Proof of the Factor Theorem for Finite Graphs*, Canadian Journal of Mathematics 6 (1954), 347–352. [doi:10.4153/CJM-1954-033-3](https://doi.org/10.4153/CJM-1954-033-3) · [open PDF](https://www.cambridge.org/core/services/aop-cambridge-core/content/view/3785657C35F370E32E5AEAFC3D1B84CE/S0008414X00023774a.pdf/div-class-title-a-short-proof-of-the-factor-theorem-for-finite-graphs-div.pdf) (Canadian Journal of Mathematics)

<details><summary>What is formalized</summary>

A Lean 4 / Mathlib formalization of Tutte's f-factor theorem: a finite simple graph G has a spanning subgraph H with deg_H v = f v for every vertex v if and only if, for all disjoint vertex sets S and T, q(S, T) ≤ ∑_{v ∈ S} f v − ∑_{v ∈ T} f v + ∑_{v ∈ T} deg_{G−S} v, where q(S, T) is the number of connected components C of G − (S ∪ T) for which ∑_{v ∈ C} f v + e(C, T) is odd and deg_{G−S} v is the number of neighbours of v outside S. Mathlib has Tutte's 1-factor theorem but not the f-factor theorem.

</details>

#### Graphic sequences: the Erdős–Gallai and Havel–Hakimi theorems

[PALOMAR-2026-10-16-000017](https://palomar-registry.org/entry.html?id=PALOMAR-2026-10-16-000017&version=1) (v1) · [jtraverso/degree-sequences @ b49808e](https://github.com/jtraverso/degree-sequences/tree/b49808e0c0aade945472b777047148399a582858) · [archived copy](https://github.com/PalomarArchive/jtraverso--degree-sequences--21c02be05315/tree/palomar/PALOMAR-2026-10-16-000017-v1/b49808e0c0aade945472b777047148399a582858)

**Sources:**

* P. Erdős, T. Gallai, *Gráfok előírt fokú pontokkal (Graphs with prescribed degrees of vertices)*, Matematikai Lapok 11 (1960), 264–274.
* Václav Havel, *A remark on the existence of finite graphs*, Časopis pro pěstování matematiky 80 (1955), 477–480. [doi:10.21136/CPM.1955.108220](https://doi.org/10.21136/CPM.1955.108220) · free to read at the publisher
* S. L. Hakimi, *On realizability of a set of integers as degrees of the vertices of a linear graph. I*, Journal of the Society for Industrial and Applied Mathematics 10 (1962), 496–506. [doi:10.1137/0110037](https://doi.org/10.1137/0110037)

<details><summary>Background references</summary>

* S. A. Choudum, *A simple proof of the Erdős–Gallai theorem on graph sequences*, Bulletin of the Australian Mathematical Society 33 (1986), 67–70. [doi:10.1017/S0004972700002872](https://doi.org/10.1017/S0004972700002872) · [open PDF](https://www.cambridge.org/core/services/aop-cambridge-core/content/view/FCA8B7DC763D3D504C68E3A5FDD8DE45/S0004972700002872a.pdf/div-class-title-a-simple-proof-of-the-erdos-gallai-theorem-on-graph-sequences-div.pdf) (Bulletin of the Australian Mathematical Society)

</details>

<details><summary>What is formalized</summary>

A Lean 4 / Mathlib formalization of the two classical characterizations of degree sequences of finite simple graphs: the Erdős–Gallai theorem (a non-increasing sequence is graphic if and only if its sum is even and every initial segment satisfies the Erdős–Gallai inequality) and the Havel–Hakimi theorem (a non-increasing sequence is graphic if and only if its first term is at most the number of remaining terms, the next d₀ terms are positive, and the reduced sequence is graphic).

</details>

#### Regular subgraphs of almost regular graphs (Alon–Friedland–Kalai)

[PALOMAR-2026-10-26-000001](https://palomar-registry.org/entry.html?id=PALOMAR-2026-10-26-000001&version=1) (v1) · [jtraverso/regular-subgraphs @ daea9b3](https://github.com/jtraverso/regular-subgraphs/tree/daea9b30d10bfae6c75ba7be5904080119bbbdba) · [archived copy](https://github.com/PalomarArchive/jtraverso--regular-subgraphs--8e423f4bda53/tree/palomar/PALOMAR-2026-10-26-000001-v1/daea9b30d10bfae6c75ba7be5904080119bbbdba)

**Sources:**

* N. Alon, S. Friedland, G. Kalai, *Regular subgraphs of almost regular graphs*, Journal of Combinatorial Theory, Series B 37 (1984), 79–91. [doi:10.1016/0095-8956(84)90047-9](https://doi.org/10.1016/0095-8956(84)90047-9) · free to read at the publisher

<details><summary>What is formalized</summary>

A Lean 4 / Mathlib formalization of the Alon–Friedland–Kalai theorem for primes: for a prime p, every finite simple graph with maximum degree at most 2p − 1 and average degree greater than 2p − 2 contains a p-regular subgraph (a nonempty subgraph with all degrees 0 or p); as a corollary, every 4-regular graph plus an edge contains a 3-regular subgraph. The prime-power case of the paper is not stated. The proof uses Mathlib's Chevalley–Warning theorem.

</details>

#### Edmonds cardinality matroid intersection

[PALOMAR-2026-10-28-000005](https://palomar-registry.org/entry.html?id=PALOMAR-2026-10-28-000005&version=1) (v1) · [jtraverso/edmonds-matroid-intersection @ 824e019](https://github.com/jtraverso/edmonds-matroid-intersection/tree/824e019d4c845e8d0ebd8638fd94f19040115cbd) · [archived copy](https://github.com/PalomarArchive/jtraverso--edmonds-matroid-intersection--3c509773d989/tree/palomar/PALOMAR-2026-10-28-000005-v1/824e019d4c845e8d0ebd8638fd94f19040115cbd)

**Sources:**

* Jack Edmonds, *Submodular Functions, Matroids, and Certain Polyhedra*, Combinatorial Structures and Their Applications (1970), 69–87; reprint LNCS 2570 (2003), 11–26. [doi:10.1007/3-540-36478-1_2](https://doi.org/10.1007/3-540-36478-1_2)
* Alexander Schrijver, *Combinatorial Optimization: Polyhedra and Efficiency*, Chapter 41, Theorem 41.1 and Corollary 41.1a, pp. 700–701.
* Tutte formalization contributors, *Lean Pool finite natural matroid rank interface*, LeanPool/lean-pool at edbe5bd56f476cc2965564676b66199f281ab714, LeanPool/TuttePath/FlatRank.lean.

<details><summary>What is formalized</summary>

Cardinality min-max theorem for two finite Mathlib matroids with the same ground, attained primal-dual certificates, exact-size feasibility and the equal-rank common-base criterion.

</details>

#### Edmonds' perfect matching polytope and matching polytope

[PALOMAR-2026-10-28-000010](https://palomar-registry.org/entry.html?id=PALOMAR-2026-10-28-000010&version=1) (v1) · [jtraverso/edmonds-matching-polytope @ 6198b83](https://github.com/jtraverso/edmonds-matching-polytope/tree/6198b8314ac88a5638120fcf15d5b58c024caaab) · [archived copy](https://github.com/PalomarArchive/jtraverso--edmonds-matching-polytope--a32c69454bfc/tree/palomar/PALOMAR-2026-10-28-000010-v1/6198b8314ac88a5638120fcf15d5b58c024caaab)

**Sources:**

* J. Edmonds, *Maximum matching and a polyhedron with 0,1-vertices*, Journal of Research of the National Bureau of Standards, Section B 69B (1965), 125–130. [doi:10.6028/jres.069B.013](https://doi.org/10.6028/jres.069B.013) · free to read at the publisher

<details><summary>Background references</summary>

* A. Schrijver, *Short proofs on the matching polyhedron*, Journal of Combinatorial Theory, Series B 34 (1983), 104–108. [doi:10.1016/0095-8956(83)90011-4](https://doi.org/10.1016/0095-8956(83)90011-4) · [open PDF](https://www.sciencedirect.com/science/article/pii/0095895683900114/pdf) (Journal of Combinatorial Theory Series B)

</details>

<details><summary>What is formalized</summary>

A Lean 4 / Mathlib formalization of Edmonds' theorems (1965) for finite simple graphs: the convex hull of the incidence vectors of the perfect matchings is {x ≥ 0, x(δ(v)) = 1 for every vertex v, x(δ(S)) ≥ 1 for every odd set S}, and the convex hull of the incidence vectors of all matchings is {x ≥ 0, x(δ(v)) ≤ 1, x(E[S]) ≤ (|S| − 1)/2 for every odd S}. Vectors are indexed by the edges of the graph, the convex hull is Mathlib's convexHull, and matchings are Mathlib's Subgraph.IsMatching and Subgraph.IsPerfectMatching. The perfect matching theorem is proved for multigraphs by induction with shrinking of tight odd cuts; the matching polytope follows by the doubling construction. Mathlib does not contain these results.

</details>

### Extremal graph theory and Ramsey theory

#### Classical bounds for graph Ramsey numbers

[PALOMAR-2026-10-15-000021](https://palomar-registry.org/entry.html?id=PALOMAR-2026-10-15-000021&version=1) (v1) · [jtraverso/ramsey-graph-bounds @ 562986a](https://github.com/jtraverso/ramsey-graph-bounds/tree/562986a7ce9edf086c20b3a2b8c7d5ace2ffd843) · [archived copy](https://github.com/PalomarArchive/jtraverso--ramsey-graph-bounds--d35ec49e7ff6/tree/palomar/PALOMAR-2026-10-15-000021-v1/562986a7ce9edf086c20b3a2b8c7d5ace2ffd843)

**Sources:**

* Paul Erdős, George Szekeres, *A combinatorial problem in geometry*, Compositio Mathematica 2 (1935), 463–470.
* Paul Erdős, *Some remarks on the theory of graphs*, Bulletin of the American Mathematical Society 53 (1947), 292–294. [doi:10.1090/S0002-9904-1947-08785-1](https://doi.org/10.1090/S0002-9904-1947-08785-1) · [open PDF](https://www.ams.org/bull/1947-53-04/S0002-9904-1947-08785-1/S0002-9904-1947-08785-1.pdf) (Bulletin of the American Mathematical Society)
* R. E. Greenwood, A. M. Gleason, *Combinatorial relations and chromatic graphs*, Canadian Journal of Mathematics 7 (1955), 1–7. [doi:10.4153/CJM-1955-001-4](https://doi.org/10.4153/CJM-1955-001-4) · [open PDF](https://www.cambridge.org/core/services/aop-cambridge-core/content/view/BF0DEBC881488344266BCD77CBBCD86B/S0008414X00030091a.pdf/div-class-title-combinatorial-relations-and-chromatic-graphs-div.pdf) (Canadian Journal of Mathematics)

<details><summary>What is formalized</summary>

A Lean 4 / Mathlib formalization of the classical bounds for graph Ramsey numbers: R(3, 3) = 6 (every graph on six vertices has a triangle or three independent vertices, and the pentagon has neither), the Erdős–Szekeres upper bound R(s, t) ≤ C(s + t − 2, s − 1), and Erdős's lower bound R(k, k) > 2^(k/2) for k ≥ 3, proved by a union bound over the edge sets of graphs on n vertices.

</details>

#### Füredi's stability theorem and the Erdős–Simonovits stability theorem

[PALOMAR-2026-10-16-000024](https://palomar-registry.org/entry.html?id=PALOMAR-2026-10-16-000024&version=1) (v1) · [jtraverso/turan-stability @ 3eb9903](https://github.com/jtraverso/turan-stability/tree/3eb99033cc931add291781f77b7446dcba8f5f9d) · [archived copy](https://github.com/PalomarArchive/jtraverso--turan-stability--e49ed8b57e3c/tree/palomar/PALOMAR-2026-10-16-000024-v1/3eb99033cc931add291781f77b7446dcba8f5f9d)

**Sources:**

* Zoltán Füredi, *A proof of the stability of extremal graphs, Simonovits' stability from Szemerédi's regularity*, Journal of Combinatorial Theory, Series B 115 (2015), 66–71. [doi:10.1016/j.jctb.2015.05.001](https://doi.org/10.1016/j.jctb.2015.05.001) · [open PDF](https://www.sciencedirect.com/science/article/pii/S0095895615000568/pdf) (Journal of Combinatorial Theory Series B)
* Miklós Simonovits, *A method for solving extremal problems in graph theory, stability problems*, Theory of Graphs (Proc. Colloq., Tihany, 1966), Academic Press, New York (1968), 279–319.
* Paul Erdős, *Some recent results on extremal problems in graph theory*, Theory of Graphs (Internat. Sympos., Rome, 1966), Gordon and Breach, New York (1967), 117–123.
* Paul Erdős, Péter Frankl, Vojtěch Rödl, *The asymptotic number of graphs not containing a fixed subgraph and a problem for hypergraphs having no exponent*, Graphs and Combinatorics 2 (1986), 113–121. [doi:10.1007/BF01788085](https://doi.org/10.1007/BF01788085)

<details><summary>Background references</summary>

* Yaël Dillies, Bhavik Mehta, *Formalising Szemerédi's Regularity Lemma in Lean*, 13th International Conference on Interactive Theorem Proving (ITP 2022), LIPIcs 237, 9:1–9:19. [doi:10.4230/LIPIcs.ITP.2022.9](https://doi.org/10.4230/LIPIcs.ITP.2022.9) · [open PDF](https://drops.dagstuhl.de/storage/00lipics/lipics-vol237-itp2022/LIPIcs.ITP.2022.9/LIPIcs.ITP.2022.9.pdf) (DROPS (Schloss Dagstuhl – Leibniz Center for Informatics))

</details>

<details><summary>What is formalized</summary>

A Lean 4 / Mathlib formalization of the stability theory of Turán's theorem. (1) Füredi's sharp stability theorem for cliques: a K_{p+1}-free graph on n vertices with at least t(n, p) − t edges (t(n, p) the number of edges of the Turán graph) has a p-partite subgraph with at least e(G) − t edges, via Füredi's partition inequality e(G) + Σᵢ e(G[Vᵢ]) ≤ e(K(V₁, …, V_p)); also edit distance at most 3t to a complete p-partite graph. (2) The Erdős–Simonovits stability theorem for every forbidden graph L with χ(L) ≤ p + 1: for every ε > 0 there are δ > 0 and n₀ such that every L-free graph on n ≥ n₀ vertices with at least (1 − 1/p) n²/2 − δn² edges differs from a complete p-partite graph in at most εn² edges, derived as in Füredi's paper from the regularity method. For this, the project extends Mathlib's regularity theory, which only treats triangles, with (3) the clique counting lemma in ε-uniform parts, (4) the clique removal lemma (fewer than δn^r copies of K_r can be destroyed by deleting fewer than εn² edges) and (5) the embedding lemma for any fixed graph with a proper colouring into pairwise uniform dense parts. Mathlib has Turán's theorem, Szemerédi's regularity lemma and triangle counting/removal, but none of (1)–(5).

</details>

#### The graph removal lemma for every fixed graph

[PALOMAR-2026-10-18-000002](https://palomar-registry.org/entry.html?id=PALOMAR-2026-10-18-000002&version=1) (v1) · [jtraverso/graph-removal-lemma @ 589cf03](https://github.com/jtraverso/graph-removal-lemma/tree/589cf03ef1e4c80ea8cdd6be77778232c62dd37c) · [archived copy](https://github.com/PalomarArchive/jtraverso--graph-removal-lemma--03befbbe3fbf/tree/palomar/PALOMAR-2026-10-18-000002-v1/589cf03ef1e4c80ea8cdd6be77778232c62dd37c)

**Sources:**

* P. Erdős, P. Frankl, V. Rödl, *The asymptotic number of graphs not containing a fixed subgraph and a problem for hypergraphs having no exponent*, Graphs and Combinatorics 2 (1986), 113–121. [doi:10.1007/BF01788085](https://doi.org/10.1007/BF01788085)

<details><summary>Background references</summary>

* David Conlon, Jacob Fox, *Graph removal lemmas*, Surveys in Combinatorics 2013, London Math. Soc. Lecture Note Ser. 409; Section 2. [arXiv:1211.3487](https://arxiv.org/abs/1211.3487) ([PDF](https://arxiv.org/pdf/1211.3487))

</details>

<details><summary>What is formalized</summary>

A Lean 4 / Mathlib formalization of the graph removal lemma of Erdős, Frankl and Rödl for an arbitrary fixed finite graph H on k vertices: for every ε > 0 there is δ > 0, depending only on H and ε, such that every finite graph on n vertices with fewer than δ nᵏ labelled copies of H can be made H-free by deleting fewer than ε n² edges; equivalently (far form), a graph from which at least ε n² edges must be deleted to destroy all copies of H has at least δ nᵏ labelled copies. Also included is the counting lemma used in the proof: if parts s x (one for each vertex x of H) are robustly dense with density at least d along the edges of H, with 2kη ≤ dᵏ and #(s x) ≥ 4k/dᵏ, then at least (dᵏ/4)ᵏ ∏ #(s x) injective maps send H into G with f x ∈ s x. Mathlib has the regularity lemma and the triangle removal lemma, but not the removal lemma for a general H.

</details>

#### The Bondy–Simonovits even cycle theorem

[PALOMAR-2026-10-22-000043](https://palomar-registry.org/entry.html?id=PALOMAR-2026-10-22-000043&version=1) (v1) · [jtraverso/bondy-simonovits @ a4ca4b2](https://github.com/jtraverso/bondy-simonovits/tree/a4ca4b28a0d82735316fd73a5a11303231109fc7) · [archived copy](https://github.com/PalomarArchive/jtraverso--bondy-simonovits--28aa00457e93/tree/palomar/PALOMAR-2026-10-22-000043-v1/a4ca4b28a0d82735316fd73a5a11303231109fc7)

**Sources:**

* J. A. Bondy, M. Simonovits, *Cycles of even length in graphs*, Journal of Combinatorial Theory, Series B 16 (1974), 97–105. [doi:10.1016/0095-8956(74)90052-5](https://doi.org/10.1016/0095-8956(74)90052-5) · free to read at the publisher

<details><summary>Background references</summary>

* J. Verstraëte, *On arithmetic progressions of cycle lengths in graphs*, Combinatorics, Probability and Computing 9 (2000), 369–373. [doi:10.1017/S0963548300004478](https://doi.org/10.1017/S0963548300004478)
* O. Pikhurko, *A note on the Turán function of even cycles*, Proceedings of the American Mathematical Society 140 (2012), 3687–3692. [doi:10.1090/S0002-9939-2012-11274-2](https://doi.org/10.1090/S0002-9939-2012-11274-2) · [open PDF](https://www.ams.org/proc/2012-140-11/S0002-9939-2012-11274-2/S0002-9939-2012-11274-2.pdf) (Proceedings of the American Mathematical Society)

</details>

<details><summary>What is formalized</summary>

A Lean 4 / Mathlib formalization of the Bondy–Simonovits theorem: for every k ≥ 2 there is a constant C such that every finite simple graph on n vertices with no cycle of length exactly 2k has at most C·n^(1+1/k) edges, i.e. ex(n, C_2k) = O(n^(1+1/k)). The statement is existential in C (the proof gives C = 16k + 4); the sharper constants of later work and the full range of even cycle lengths in Bondy–Simonovits's paper are not stated. Mathlib has walks and cycles but not this theorem.

</details>

### Probabilistic methods and random graphs

#### Graphs of large girth and large chromatic number: Erdős, Mycielski, and the fractional chromatic number of Mycielski graphs

[PALOMAR-2026-10-17-000009](https://palomar-registry.org/entry.html?id=PALOMAR-2026-10-17-000009&version=2) (v2) · [jtraverso/erdos-girth-chromatic @ 05407c1](https://github.com/jtraverso/erdos-girth-chromatic/tree/05407c110b29ebb412667c688b2758d23bc744dd) · [archived copy](https://github.com/PalomarArchive/jtraverso--erdos-girth-chromatic--0532ff066cce/tree/palomar/PALOMAR-2026-10-17-000009-v2/05407c110b29ebb412667c688b2758d23bc744dd)

**Sources:**

* Paul Erdős, *Graph Theory and Probability*, Canadian Journal of Mathematics 11 (1959), 34–38. [doi:10.4153/CJM-1959-003-9](https://doi.org/10.4153/CJM-1959-003-9) · [open PDF](https://www.cambridge.org/core/services/aop-cambridge-core/content/view/154EF813293BC7D0652C4CBCD9D18E84/S0008414X00002947a.pdf/div-class-title-graph-theory-and-probability-div.pdf) (Canadian Journal of Mathematics)
* Jan Mycielski, *Sur le coloriage des graphs*, Colloquium Mathematicum 3 (1955), 161–162. [doi:10.4064/cm-3-2-161-162](https://doi.org/10.4064/cm-3-2-161-162) · [open PDF](https://www.impan.pl/shop/publication/transaction/download/product/94136?download.pdf) (Colloquium Mathematicum)
* Michael Larsen, James Propp, Daniel Ullman, *The fractional chromatic number of Mycielski's graphs*, Journal of Graph Theory 19 (1995), 411–416. [doi:10.1002/jgt.3190190313](https://doi.org/10.1002/jgt.3190190313)

<details><summary>What is formalized</summary>

A Lean 4 / Mathlib formalization of three classical results on graphs with large chromatic number. (1) Erdős' 1959 theorem: for every g and k there is a finite graph with girth greater than g and chromatic number greater than k, in the structural form given by the probabilistic argument (for every ε > 0 and all large n, a graph on n vertices with girth greater than g whose independent sets have fewer than εn vertices). (2) Mycielski's 1955 construction M(G): it preserves and reflects triangle-freeness, M(G) is (k+1)-colourable exactly when G is k-colourable, χ(M(G)) = χ(G) + 1 for every finite G, and iterating from K₂ gives triangle-free graphs with 3·2ⁿ − 1 vertices and chromatic number n + 2. (3) Larsen, Propp and Ullman (1995): for the fractional chromatic number χ_f (least total weight of a fractional colouring by independent sets), χ_f(M(G)) = χ_f(G) + 1/χ_f(G) for every finite graph G with at least one vertex. Version 2 adds (2) and (3); the statements of version 1 are unchanged. Mathlib has girth and chromatic number but none of these theorems, and no fractional chromatic number.

</details>

#### The Lovász Local Lemma and two applications

[PALOMAR-2026-10-20-000004](https://palomar-registry.org/entry.html?id=PALOMAR-2026-10-20-000004&version=1) (v1) · [jtraverso/lovasz-local-lemma @ 9d020fa](https://github.com/jtraverso/lovasz-local-lemma/tree/9d020fa8fb20e9426c2d6780a3cfab4a68794d89) · [archived copy](https://github.com/PalomarArchive/jtraverso--lovasz-local-lemma--3b6f209cddb3/tree/palomar/PALOMAR-2026-10-20-000004-v1/9d020fa8fb20e9426c2d6780a3cfab4a68794d89)

**Sources:**

* P. Erdős, L. Lovász, *Problems and results on 3-chromatic hypergraphs and some related questions*, Infinite and Finite Sets (Colloq. Keszthely, 1973), Colloq. Math. Soc. János Bolyai 10, North-Holland (1975), 609–627.
* Joel Spencer, *Asymptotic lower bounds for Ramsey functions*, Discrete Mathematics 20 (1977), 69–76. [doi:10.1016/0012-365X(77)90044-9](https://doi.org/10.1016/0012-365X(77)90044-9) · [open PDF](https://www.sciencedirect.com/science/article/pii/0012365X77900449/pdf) (Discrete Mathematics)

<details><summary>Background references</summary>

* Noga Alon, Joel H. Spencer, *The Probabilistic Method (3rd edition)*, Wiley (2008), Chapter 5. [doi:10.1002/9780470277331](https://doi.org/10.1002/9780470277331)

</details>

<details><summary>What is formalized</summary>

A Lean 4 / Mathlib formalization of the Lovász Local Lemma for finitely many events in a probability space with a dependency graph (each event mutually independent, in the sense of Mathlib's `ProbabilityTheory.Indep` of generated σ-algebras, of its non-neighbours), in its general form (P(A_i) ≤ x_i ∏_{j∼i}(1 − x_j) implies P(no event) ≥ ∏(1 − x_i)) and its symmetric form (e p (d + 1) ≤ 1 implies P(no event) > 0); and of two applications: Spencer's Ramsey lower bound (if 2e(C(k,2)C(n,k−2) + 1) ≤ 2^C(k,2) then R(k,k) > n) and the Erdős–Lovász property B theorem for k-uniform hypergraphs (each edge meeting at most d others with e(d + 1) ≤ 2^(k−1); and the case where every vertex lies in at most k edges, for k ≥ 9). Mathlib has independence and product measures but not the Local Lemma.

</details>

#### Hamiltonicity and connectivity thresholds of the random graph G(n, p)

[PALOMAR-2026-10-28-000021](https://palomar-registry.org/entry.html?id=PALOMAR-2026-10-28-000021&version=1) (v1) · [jtraverso/random-graph-thresholds @ 86325fa](https://github.com/jtraverso/random-graph-thresholds/tree/86325faff71fb76c0769963525b69095fa0a6241) · [archived copy](https://github.com/PalomarArchive/jtraverso--random-graph-thresholds--8101b919ee82/tree/palomar/PALOMAR-2026-10-28-000021-v1/86325faff71fb76c0769963525b69095fa0a6241)

**Sources:**

* L. Pósa, *Hamiltonian circuits in random graphs*, Discrete Mathematics 14 (1976), 359–364. [doi:10.1016/0012-365X(76)90068-6](https://doi.org/10.1016/0012-365X(76)90068-6) · free to read at the publisher
* P. Erdős, A. Rényi, *On random graphs I*, Publicationes Mathematicae Debrecen 6 (1959), 290–297. [doi:10.5486/PMD.1959.6.3-4.12](https://doi.org/10.5486/PMD.1959.6.3-4.12)

<details><summary>What is formalized</summary>

A Lean 4 / Mathlib formalization of two classical threshold results for the binomial random graph G(n, p), modelled as a finite product probability space with one independent Bernoulli(p) coin per pair of vertices: Pósa's theorem (1976) that G(n, p) with p ≥ C log n / n is Hamiltonian with probability tending to 1, also stated with the explicit constant C = 80 (posa_eighty), and both sides of the Erdős–Rényi connectivity threshold (1959): G(n, (log n ± ω(n))/n) with ω(n) → ∞, the edge probability clipped to [0, 1], is connected with probability tending to 1, resp. 0. Hamiltonicity and connectivity are Mathlib's SimpleGraph.IsHamiltonian and SimpleGraph.Connected. Mathlib defines the binomial random graph as a measure on graphs (SimpleGraph.binomialRandom); this project uses its own finite product model instead, and these threshold theorems are not in Mathlib.

</details>

#### Pseudorandom hypergraph matchings (Ehard–Glock–Joos)

[PALOMAR-2026-10-17-000004](https://palomar-registry.org/entry.html?id=PALOMAR-2026-10-17-000004&version=1) (v1) · [jtraverso/pseudorandom-hypergraph-matchings @ 3957f3c](https://github.com/jtraverso/pseudorandom-hypergraph-matchings/tree/3957f3c0dbc34fd310cb5fecf7941fddc9ef6c8f) · [archived copy](https://github.com/PalomarArchive/jtraverso--pseudorandom-hypergraph-matchings--40c1ca802506/tree/palomar/PALOMAR-2026-10-17-000004-v1/3957f3c0dbc34fd310cb5fecf7941fddc9ef6c8f)

**Sources:**

* Stefan Ehard, Stefan Glock, Felix Joos, *Pseudorandom hypergraph matchings*, Combinatorics, Probability and Computing 29 (2020), 868–885; arXiv:1907.09946. [doi:10.1017/S0963548320000280](https://doi.org/10.1017/S0963548320000280) · [open PDF](https://www.cambridge.org/core/services/aop-cambridge-core/content/view/AE0DE17C95900E7DD3F221E2C17FE203/S0963548320000280a.pdf/div-class-title-pseudorandom-hypergraph-matchings-div.pdf) (Combinatorics Probability Computing) · [arXiv:1907.09946](https://arxiv.org/abs/1907.09946) ([PDF](https://arxiv.org/pdf/1907.09946))

<details><summary>Background references</summary>

* Nicholas Pippenger, Joel Spencer, *Asymptotic behavior of the chromatic index for hypergraphs*, Journal of Combinatorial Theory, Series A 51 (1989), 24–42. [doi:10.1016/0097-3165(89)90074-5](https://doi.org/10.1016/0097-3165(89)90074-5) · free to read at the publisher
* Noga Alon, Raphael Yuster, *On a Hypergraph Matching Problem*, Graphs and Combinatorics 21 (2005), 377–384. [doi:10.1007/s00373-005-0628-x](https://doi.org/10.1007/s00373-005-0628-x)
* David A. Freedman, *On Tail Probabilities for Martingales*, The Annals of Probability 3 (1975), 100–118. [doi:10.1214/aop/1176996452](https://doi.org/10.1214/aop/1176996452) · [open PDF](https://projecteuclid.org/journals/annals-of-probability/volume-3/issue-1/On-Tail-Probabilities-for-Martingales/10.1214/aop/1176996452.pdf) (The Annals of Probability)
* Michael Molloy, Bruce Reed, *Near-optimal list colorings*, Random Structures and Algorithms 17 (2000), 376–402. [doi:10.1002/1098-2418(200010/12)17:3/4<376::AID-RSA10>3.0.CO;2-0](https://doi.org/10.1002/1098-2418(200010/12)17:3/4<376::AID-RSA10>3.0.CO;2-0)

</details>

<details><summary>What is formalized</summary>

A Lean 4 / Mathlib formalization of the main results of Ehard, Glock and Joos, "Pseudorandom hypergraph matchings" (Combin. Probab. Comput. 2020): Pippenger's theorem on almost perfect matchings in almost regular hypergraphs with small codegrees (Theorem 1.1); the existence of a matching M in any r-uniform hypergraph with Δ(H) ≤ Δ, codegrees ≤ Δ^{1−δ} and at most exp(Δ^{ε²}) edges such that ω(M) = (1 ± Δ^{−ε}) ω(E(H))/Δ simultaneously for up to exp(Δ^{ε²}) weight functions (Theorem 1.2, with ε = δ/(50r²)); the generalization to weight functions on ℓ-tuples of edges, under the same exponential cap on the number of edges and of weight functions (Theorem 1.3, the main theorem, with ε = δ/(50L²r²)); the concentration inequality for pattern weights under a uniformly random colouring (Theorem 3.1); and the existence of partial Steiner systems whose subgraph counts behave as in the random model (Theorem 4.1). The formal proof is self-contained over Mathlib: Freedman's and Bernstein's inequalities are proved inside the project, and the Molloy–Reed colouring theorem used as a black box in the paper is replaced by a self-contained nibble.

</details>

#### The Moser–Tardos theorem (algorithmic Lovász Local Lemma)

[PALOMAR-2026-10-29-000008](https://palomar-registry.org/entry.html?id=PALOMAR-2026-10-29-000008&version=1) (v1) · [jtraverso/moser-tardos @ 5a3024a](https://github.com/jtraverso/moser-tardos/tree/5a3024a6d3eb442ac6925f9b3660b93c36cfb8b4) · [archived copy](https://github.com/PalomarArchive/jtraverso--moser-tardos--5ec56ed9b1a0/tree/palomar/PALOMAR-2026-10-29-000008-v1/5a3024a6d3eb442ac6925f9b3660b93c36cfb8b4)

**Sources:**

* Robin A. Moser, Gábor Tardos, *A constructive proof of the general Lovász Local Lemma*, Journal of the ACM 57 (2010), no. 2, Article 11. [doi:10.1145/1667053.1667060](https://doi.org/10.1145/1667053.1667060)

<details><summary>What is formalized</summary>

A Lean 4 / Mathlib formalization of the Moser–Tardos theorem in the variable setting: finitely many independent random variables with finite ranges, n events each determined by a finite set of variables, neighbours sharing a variable. If P(A_j) ≤ x_j ∏_{k ∈ Γ(j)} (1 − x_k) with 0 ≤ x_j < 1, the resampling algorithm (always resampling the first violated event), run on a random resampling table, resamples A_j at most x_j / (1 − x_j) times in expectation among its first t steps, for every t; the expected total number of resamplings is at most ∑_j x_j / (1 − x_j); the probability that it has not stopped after t steps is at most (∑_j x_j / (1 − x_j)) / t; and some assignment avoids all events (the Lovász Local Lemma in the variable setting). The proof formalizes witness trees built from the log, the τ-check coupling with the resampling table, and the Galton–Watson bound.

</details>

### Decompositions and packings

#### Dross's theorem on fractional triangle decompositions

[PALOMAR-2026-10-15-000008](https://palomar-registry.org/entry.html?id=PALOMAR-2026-10-15-000008&version=1) (v1) · [jtraverso/dross-fractional-triangle-decomposition @ 7720b7b](https://github.com/jtraverso/dross-fractional-triangle-decomposition/tree/7720b7b591e606d5a56f1d935d8be650dcbf6c6f) · [archived copy](https://github.com/PalomarArchive/jtraverso--dross-fractional-triangle-decomposition--f57504b1525c/tree/palomar/PALOMAR-2026-10-15-000008-v1/7720b7b591e606d5a56f1d935d8be650dcbf6c6f)

**Sources:**

* François Dross, *Fractional Triangle Decompositions in Graphs with Large Minimum Degree*, SIAM Journal on Discrete Mathematics 30 (2016), no. 1, 36–42. [doi:10.1137/15M1014310](https://doi.org/10.1137/15M1014310) · [open PDF](https://hal-lirmm.ccsd.cnrs.fr/lirmm-01336680v1/document) (HAL)

<details><summary>What is formalized</summary>

A Lean 4 / Mathlib formalization of Dross's theorem: every finite graph on n vertices with minimum degree at least 9n/10 has a fractional triangle decomposition, i.e. nonnegative real weights on its triangles such that every edge lies in triangles of total weight exactly one. The threshold 9/10 is the exact one of the paper. The proof follows the max-flow/min-cut approach: the existence of the weights is reduced to a flow problem, a finite max-flow/min-cut theorem (included) is applied, and every cut is bounded below by counting triangles and K4s, with a peeling reduction for heavy triangles.

</details>

#### Near-regular hypergraph matchings and the asymptotic triangle-packing gap

[PALOMAR-2026-10-15-000011](https://palomar-registry.org/entry.html?id=PALOMAR-2026-10-15-000011&version=2) (v2) · [jtraverso/asymptotic-triangle-packing @ 760e503](https://github.com/jtraverso/asymptotic-triangle-packing/tree/760e503972aad8ca9da7904ce72e5cce405f5991) · [archived copy](https://github.com/PalomarArchive/jtraverso--asymptotic-triangle-packing--a2c3300bc8ff/tree/palomar/PALOMAR-2026-10-15-000011-v2/760e503972aad8ca9da7904ce72e5cce405f5991)

**Sources:**

* P. E. Haxell, V. Rödl, *Integer and fractional packings in dense graphs*, Combinatorica 21 (2001), no. 1, 13–38. [doi:10.1007/s004930170003](https://doi.org/10.1007/s004930170003)

<details><summary>Background references</summary>

* Raphael Yuster, *Integer and fractional packing of families of graphs*, Random Structures & Algorithms 26 (2005), no. 1–2, 110–118. [doi:10.1002/rsa.20048](https://doi.org/10.1002/rsa.20048) · [open PDF](https://arxiv.org/pdf/math/0305350) (arXiv (Cornell University))
* P. Frankl, V. Rödl, *Near perfect coverings in graphs and hypergraphs*, European Journal of Combinatorics 6 (1985), no. 4, 317–326. [doi:10.1016/S0195-6698(85)80045-7](https://doi.org/10.1016/S0195-6698(85)80045-7) · free to read at the publisher
* Nicholas Pippenger, Joel Spencer, *Asymptotic behavior of the chromatic index for hypergraphs*, Journal of Combinatorial Theory, Series A 51 (1989), no. 1, 24–42. [doi:10.1016/0097-3165(89)90074-5](https://doi.org/10.1016/0097-3165(89)90074-5) · free to read at the publisher
* Juan Pablo Traverso Gianini, *Linear-Error Clique Partitions of Split Graphs via Structured Triangle Packing (Paper III of the preprint series)*, GitHub repository jtraverso/erdos-81-chordal-clique-partitions, preprints/PAPER_III.
* Ben Barber, Daniela Kühn, Allan Lo, Deryk Osthus, Amelia Taylor, *Clique decompositions of multipartite graphs and completion of Latin squares*, Journal of Combinatorial Theory, Series A 151 (2017), 146–201; arXiv:1603.01043. [doi:10.1016/j.jcta.2017.04.005](https://doi.org/10.1016/j.jcta.2017.04.005) · [open PDF](https://www.sciencedirect.com/science/article/pii/S0097316517300432/pdf) (Journal of Combinatorial Theory Series A) · [arXiv:1603.01043](https://arxiv.org/abs/1603.01043) ([PDF](https://arxiv.org/pdf/1603.01043))

</details>

<details><summary>What is formalized</summary>

A Lean 4 / Mathlib formalization of four results. (1) A finite nibble theorem: r-uniform hypergraphs whose degrees are at most (1+μ)d everywhere and at least (1−μ)d outside an exceptional set of at most η|V| vertices, with codegrees at most μd, have matchings with at least (1−β)|V|/r edges. (2) The fractional–integral triangle-packing gap is o(n²) uniformly over finite graphs: every large graph has an edge-disjoint triangle family P such that every fractional triangle packing has weight at most |P| + εn² (the triangle case of Haxell–Rödl). (3) The cover form: a fractional triangle cover of weight at most |P| + εn² exists. (4) Version 2, the transfer form used in decomposition theory: every large graph on n vertices that has a fractional triangle decomposition has an edge-disjoint triangle family covering all but at most ηn² edges; it follows from (2), since a fractional decomposition is a fractional packing of weight e(G)/3 and a packing P covers exactly 3|P| edges. The proof of (1)–(3) combines a nibble with second-moment and Freedman-type concentration, a low-degree core reduction, Mathlib's Szemerédi regularity lemma with a cluster linear program rounded by explicit designs, and LP duality.

</details>

#### The Nash-Williams–Tutte tree packing theorem and Nash-Williams' arboricity theorem

[PALOMAR-2026-10-17-000008](https://palomar-registry.org/entry.html?id=PALOMAR-2026-10-17-000008&version=1) (v1) · [jtraverso/nash-williams-trees @ 101e488](https://github.com/jtraverso/nash-williams-trees/tree/101e48847a929dd8102521f57723e2137989ce2e) · [archived copy](https://github.com/PalomarArchive/jtraverso--nash-williams-trees--9280327cd578/tree/palomar/PALOMAR-2026-10-17-000008-v1/101e48847a929dd8102521f57723e2137989ce2e)

**Sources:**

* C. St. J. A. Nash-Williams, *Edge-Disjoint Spanning Trees of Finite Graphs*, Journal of the London Mathematical Society s1-36 (1961), 445–450. [doi:10.1112/jlms/s1-36.1.445](https://doi.org/10.1112/jlms/s1-36.1.445)
* W. T. Tutte, *On the Problem of Decomposing a Graph into n Connected Factors*, Journal of the London Mathematical Society s1-36 (1961), 221–230. [doi:10.1112/jlms/s1-36.1.221](https://doi.org/10.1112/jlms/s1-36.1.221)
* C. St. J. A. Nash-Williams, *Decomposition of Finite Graphs Into Forests*, Journal of the London Mathematical Society s1-39 (1964), 12. [doi:10.1112/jlms/s1-39.1.12](https://doi.org/10.1112/jlms/s1-39.1.12)

<details><summary>Background references</summary>

* B. Chen, M. Matsumoto, J. Wang, Z. Zhang, J. Zhang, *A short proof of Nash-Williams' theorem for the arboricity of a graph*, Graphs and Combinatorics 10 (1994), 27–28. [doi:10.1007/BF01202467](https://doi.org/10.1007/BF01202467)
* Reinhard Diestel, *Graph Theory*, Graduate Texts in Mathematics 173, 5th edition, Springer (2017), Section 2.4 (Theorem 2.4.1 and its proof). [doi:10.1007/978-3-662-53622-3](https://doi.org/10.1007/978-3-662-53622-3)

</details>

<details><summary>What is formalized</summary>

A Lean 4 / Mathlib formalization of three classical results on edge-disjoint trees and forests in finite simple graphs, none of which is in Mathlib. (1) The Nash-Williams–Tutte tree packing theorem: a graph has k edge-disjoint spanning trees if and only if every partition of its vertices into m parts has at least k(m − 1) edges between different parts. (2) Nash-Williams' arboricity theorem: the edges can be covered by k forests if and only if every nonempty vertex set S spans at most k(|S| − 1) edges. (3) The corollary that every 2k-edge-connected graph has k edge-disjoint spanning trees. Mathlib has no matroid union theorem and no graphic matroid; the proofs are direct edge-exchange arguments.

</details>

#### Fractional triangle decompositions of dense tripartite graphs

[PALOMAR-2026-10-30-000008](https://palomar-registry.org/entry.html?id=PALOMAR-2026-10-30-000008&version=1) (v1) · [jtraverso/fractional-triangle-decompositions-tripartite @ d233113](https://github.com/jtraverso/fractional-triangle-decompositions-tripartite/tree/d2331132eac8b9c9c1891ba14162745d567ebfdb) · [archived copy](https://github.com/PalomarArchive/jtraverso--fractional-triangle-decompositions-tripartite--1b438fcdd323/tree/palomar/PALOMAR-2026-10-30-000008-v1/d2331132eac8b9c9c1891ba14162745d567ebfdb)

**Sources:**

* Jack Allsop, Candida Bowtell, Thomas Lesgourgues, Kalina Petrova, *Improved bounds on completion of partial Latin squares*, arXiv:2609.37877v1 (30 September 2026), Theorem 1.3, Lemma 2.1, Proposition 3.1, Corollary 3.5, Definition 4.1, Propositions 4.2, 4.3 and 4.4, and Appendix A. [arXiv:2609.37877](https://arxiv.org/abs/2609.37877) ([PDF](https://arxiv.org/pdf/2609.37877))

<details><summary>What is formalized</summary>

A Lean 4 / Mathlib formalization of the main results of Allsop, Bowtell, Lesgourgues and Petrova, "Improved bounds on completion of partial Latin squares" (arXiv:2609.37877, 2026): there is η > 0 (here η = 1/20000) such that every K₃-divisible spanning subgraph of K_{n,n,n} with minimum partite degree at least (0.769 − η)n has a fractional triangle decomposition (Theorem 1.3). Also formalized: the Farkas characterization (Lemma 2.1); the reduction to triangle-covered, balanced, untied and nonzero edge weightings (Proposition 3.1, Corollary 3.5), with Lemma 3.4 proved through an integral maximum flow; the non-uniform proportional discharging (Definition 4.1) and its two estimates (Propositions 4.2 and 4.3); and the numerical inequality g_d ≥ 1 for the article's piecewise-linear f (Proposition 4.4). The two-variable inequalities of Proposition 4.4, which the article settles by numerical minimisation, are proved exactly by Bernstein certificates checked in Lean. Not formalized: the article's Corollary 1.4 (completion of partial Latin squares), which also needs the fractional-to-exact transfer of Barber, Kühn, Lo, Osthus and Taylor for tripartite graphs.

</details>

### Designs, set systems and discrepancy

#### Kirkman's theorem on Steiner triple systems

[PALOMAR-2026-10-28-000003](https://palomar-registry.org/entry.html?id=PALOMAR-2026-10-28-000003&version=1) (v1) · [jtraverso/kirkman-steiner-triple-systems @ 1855141](https://github.com/jtraverso/kirkman-steiner-triple-systems/tree/18551414d822f7fa4fb7535dc43733c4b316c3a8) · [archived copy](https://github.com/PalomarArchive/jtraverso--kirkman-steiner-triple-systems--37adc3898c80/tree/palomar/PALOMAR-2026-10-28-000003-v1/18551414d822f7fa4fb7535dc43733c4b316c3a8)

**Sources:**

* T. P. Kirkman, *On a problem in combinations*, Cambridge and Dublin Mathematical Journal 2 (1847), 191–204.

<details><summary>Background references</summary>

* R. C. Bose, *On the construction of balanced incomplete block designs*, Annals of Eugenics 9 (1939), 353–399. [doi:10.1111/j.1469-1809.1939.tb02219.x](https://doi.org/10.1111/j.1469-1809.1939.tb02219.x)
* Th. Skolem, *Some remarks on the triple systems of Steiner*, Mathematica Scandinavica 6 (1958), 273–280. [doi:10.7146/math.scand.a-10551](https://doi.org/10.7146/math.scand.a-10551) · [open PDF](https://www.mscand.dk/article/download/10551/8572) (MATHEMATICA SCANDINAVICA)

</details>

<details><summary>What is formalized</summary>

A Lean 4 / Mathlib formalization of Kirkman's 1847 theorem: for v ≥ 1, a Steiner triple system on v points (a family of 3-subsets covering every pair of distinct points exactly once) exists if and only if v ≡ 1 or 3 (mod 6). Sufficiency is proved by Bose's and Skolem's constructions from Steiner quasigroups. Mathlib does not contain Steiner triple systems.

</details>

#### Counting Steiner triple systems: Wilson (1974) and Linial–Luria (2013)

[PALOMAR-2026-10-22-000017](https://palomar-registry.org/entry.html?id=PALOMAR-2026-10-22-000017&version=2) (v2) · [jtraverso/counting-steiner-triple-systems @ 52fda83](https://github.com/jtraverso/counting-steiner-triple-systems/tree/52fda83038df7442c576e17edffba591db703cb8) · [archived copy](https://github.com/PalomarArchive/jtraverso--counting-steiner-triple-systems--25dd3ac3d9ea/tree/palomar/PALOMAR-2026-10-22-000017-v1/52fda83038df7442c576e17edffba591db703cb8)

**Sources:**

* R. M. Wilson, *Nonisomorphic Steiner triple systems*, Mathematische Zeitschrift 135 (1974), 303–313. [doi:10.1007/BF01215371](https://doi.org/10.1007/BF01215371)
* N. Linial, Z. Luria, *An upper bound on the number of Steiner triple systems*, Random Structures & Algorithms 43 (2013), 399–406. [doi:10.1002/rsa.20487](https://doi.org/10.1002/rsa.20487)
* M. Laurent, A. Schrijver, *On Leonid Gurvits's proof for permanents*, The American Mathematical Monthly 117 (2010), 903–911. [doi:10.4169/000298910X523380](https://doi.org/10.4169/000298910X523380) · [open PDF](https://www.tandfonline.com/doi/abs/10.4169/000298910X523380) (American Mathematical Monthly)

<details><summary>Background references</summary>

* J. Doyen, R. M. Wilson, *Embeddings of Steiner triple systems*, Discrete Mathematics 5 (1973), 229–239. [doi:10.1016/0012-365X(73)90139-8](https://doi.org/10.1016/0012-365X(73)90139-8) · free to read at the publisher
* M. B. Wells, *The number of latin squares of order eight*, Journal of Combinatorial Theory 3 (1967), 98–99. [doi:10.1016/S0021-9800(67)80021-8](https://doi.org/10.1016/S0021-9800(67)80021-8) · [open PDF](https://www.sciencedirect.com/science/article/pii/S0021980067800218/pdf) (Journal of Combinatorial Theory)
* L. Gurvits, *Van der Waerden/Schrijver-Valiant like conjectures and stable (aka hyperbolic) homogeneous polynomials: one theorem for all*, The Electronic Journal of Combinatorics 15 (2008), R66. [doi:10.37236/790](https://doi.org/10.37236/790) · [open PDF](https://www.combinatorics.org/ojs/index.php/eljc/article/download/v15i1r66/pdf) (The Electronic Journal of Combinatorics)
* G. P. Egorychev, *The solution of van der Waerden's problem for permanents*, Advances in Mathematics 42 (1981), 299–305. [doi:10.1016/0001-8708(81)90044-X](https://doi.org/10.1016/0001-8708(81)90044-X) · [open PDF](https://www.sciencedirect.com/science/article/pii/000187088190044X/pdf) (Advances in Mathematics)
* D. I. Falikman, *Proof of the van der Waerden conjecture regarding the permanent of a doubly stochastic matrix*, Mathematical Notes of the Academy of Sciences of the USSR 29 (1981), 475–479. [doi:10.1007/BF01163285](https://doi.org/10.1007/BF01163285)

</details>

<details><summary>What is formalized</summary>

A complete Lean 4 / Mathlib formalization of R. M. Wilson's "Nonisomorphic Steiner triple systems" (inequality (2.1), Theorems 1–4, Lemmas 3–5, including the exact numbers of Latin squares of orders 6, 7 and 8 and the bounds N(19) ≥ 2450, N(21) ≥ 2160980, N(25) ≥ 163929929318400) and of N. Linial and Z. Luria's "An upper bound on the number of Steiner triple systems" (Theorems 1.1 and 1.2 with explicit error terms). Version 2 adds a proof of the van der Waerden permanent theorem (Egorychev, Falikman), following Gurvits's proof as simplified by Laurent and Schrijver. The parts of Wilson's Theorems 2 and 3 that rely on it are stated both as implications from the hypothesis vdWPC, as in the paper, and unconditionally (theorem2_full, theorem3_full). Finite computations are kernel-checked certificates (no native_decide). Mathlib does not contain these results.

</details>

#### The Hilton–Milner theorem

[PALOMAR-2026-10-28-000001](https://palomar-registry.org/entry.html?id=PALOMAR-2026-10-28-000001&version=1) (v1) · [jtraverso/hilton-milner @ 6059a0d](https://github.com/jtraverso/hilton-milner/tree/6059a0d6f13378b9a92fba297f2d774598ee0f7d) · [archived copy](https://github.com/PalomarArchive/jtraverso--hilton-milner--c43d1f8a75cc/tree/palomar/PALOMAR-2026-10-28-000001-v1/6059a0d6f13378b9a92fba297f2d774598ee0f7d)

**Sources:**

* A. J. W. Hilton, E. C. Milner, *Some intersection theorems for systems of finite sets*, The Quarterly Journal of Mathematics 18 (1967), 369–384. [doi:10.1093/qmath/18.1.369](https://doi.org/10.1093/qmath/18.1.369)

<details><summary>Background references</summary>

* P. Frankl, Z. Füredi, *Non-trivial intersecting families*, Journal of Combinatorial Theory, Series A 41 (1986), 150–153. [doi:10.1016/0097-3165(86)90121-4](https://doi.org/10.1016/0097-3165(86)90121-4) · free to read at the publisher

</details>

<details><summary>What is formalized</summary>

A Lean 4 / Mathlib formalization of the Hilton–Milner theorem: for k ≥ 2 and n > 2k, a nontrivial intersecting family of k-subsets of an n-set (no element lies in all members) has at most C(n−1, k−1) − C(n−k−1, k−1) + 1 members, and this bound is attained. Intersecting is Mathlib's Set.Intersecting. Mathlib contains the Erdős–Ko–Rado theorem but not this result.

</details>

#### Ray-Chaudhuri–Wilson: uniform families with restricted intersections

[PALOMAR-2026-10-28-000012](https://palomar-registry.org/entry.html?id=PALOMAR-2026-10-28-000012&version=1) (v1) · [jtraverso/restricted-intersections @ ebb9080](https://github.com/jtraverso/restricted-intersections/tree/ebb90800eda4ec83cc18c6da2135b8718757f6e2) · [archived copy](https://github.com/PalomarArchive/jtraverso--restricted-intersections--ad53241811dd/tree/palomar/PALOMAR-2026-10-28-000012-v1/ebb90800eda4ec83cc18c6da2135b8718757f6e2)

**Sources:**

* Dijen K. Ray-Chaudhuri, Richard M. Wilson, *On t-designs*, Osaka Journal of Mathematics 12(3) (1975), 737–744, Theorem 3. [doi:10.18910/7296](https://doi.org/10.18910/7296) · [open PDF](https://ir.library.osaka-u.ac.jp/repo/ouka/all/7296/ojm12_03_15.pdf) (Institutional Repositories DataBase (IRDB))

<details><summary>What is formalized</summary>

Formalizes Theorem 3 of On t-designs (1975): a k-uniform family of subsets of an n-element ground set whose distinct-pair intersection sizes lie in L ⊆ {0,...,k−1} has at most binomial(n,|L|) members. Includes the actual-intersection-spectrum formulation, the uniform one-intersection bound, and equality examples consisting of all s-subsets.

</details>

#### The Beck–Fiala integer-making theorem

[PALOMAR-2026-10-15-000009](https://palomar-registry.org/entry.html?id=PALOMAR-2026-10-15-000009&version=1) (v1) · [jtraverso/beck-fiala @ 52f1a12](https://github.com/jtraverso/beck-fiala/tree/52f1a12a140b0589ac39619dfd07807d98fdbaf5) · [archived copy](https://github.com/PalomarArchive/jtraverso--beck-fiala--f2fa29dec96f/tree/palomar/PALOMAR-2026-10-15-000009-v1/52f1a12a140b0589ac39619dfd07807d98fdbaf5)

**Sources:**

* József Beck, Tibor Fiala, *“Integer-making” theorems*, Discrete Applied Mathematics 3 (1981), no. 1, 1–8. [doi:10.1016/0166-218X(81)90022-6](https://doi.org/10.1016/0166-218X(81)90022-6) · free to read at the publisher

<details><summary>What is formalized</summary>

A Lean 4 / Mathlib formalization of the Beck–Fiala integer-making theorem in its rational unit-cube form: if A is a 0/1 matrix in which every column has at most t ≥ 1 ones and x ∈ [0,1]^N has rational coordinates, then x can be rounded to y ∈ {0,1}^N with |∑ᵢ A j i (y i − x i)| < t for every row j; moreover the rounding can keep every coordinate of x that is already 0 or 1. The proof is the floating-coordinates argument: while some coordinates are strictly between 0 and 1, the rows with more than t floating coordinates are fewer than the floating coordinates, so a nonzero direction keeps their sums fixed, and moving along it makes a coordinate integral; induction on the number of floating coordinates.

</details>

### Algebraic and spectral graph theory

#### The Cauchy–Binet formula, Kirchhoff's matrix-tree theorem and Cayley's formula

[PALOMAR-2026-10-16-000019](https://palomar-registry.org/entry.html?id=PALOMAR-2026-10-16-000019&version=1) (v1) · [jtraverso/matrix-tree @ aeab0f2](https://github.com/jtraverso/matrix-tree/tree/aeab0f267c523dd3cac9a287b589f65a99d20d01) · [archived copy](https://github.com/PalomarArchive/jtraverso--matrix-tree--5efe2b63de2b/tree/palomar/PALOMAR-2026-10-16-000019-v1/aeab0f267c523dd3cac9a287b589f65a99d20d01)

**Sources:**

* G. Kirchhoff, *Ueber die Auflösung der Gleichungen, auf welche man bei der Untersuchung der linearen Vertheilung galvanischer Ströme geführt wird*, Annalen der Physik und Chemie 148 (1847), 497–508. [doi:10.1002/andp.18471481202](https://doi.org/10.1002/andp.18471481202) · [open version](https://zenodo.org/record/2242265) (Zenodo (CERN European Organization for Nuclear Research))
* Arthur Cayley, *A theorem on trees*, Quarterly Journal of Pure and Applied Mathematics 23 (1889), 376–378.
* J. P. M. Binet, *Mémoire sur un système de formules analytiques, et leur application à des considérations géométriques*, Journal de l'École Polytechnique 9 (1813), 280–302.
* A.-L. Cauchy, *Mémoire sur les fonctions qui ne peuvent obtenir que deux valeurs égales et de signes contraires par suite des transpositions opérées entre les variables qu'elles renferment*, Journal de l'École Polytechnique 10 (1815), 29–112.

<details><summary>What is formalized</summary>

A Lean 4 / Mathlib formalization of the Cauchy–Binet formula for determinants of products of rectangular matrices over commutative rings (not in Mathlib), of Kirchhoff's matrix-tree theorem (the number of spanning trees of a finite graph is any principal cofactor of Mathlib's Laplacian matrix), and of Cayley's formula (n^(n−2) labelled trees on n ≥ 1 vertices), derived from the matrix-tree theorem for the complete graph.

</details>

#### Moore graphs of diameter two: the Hoffman–Singleton theorem

[PALOMAR-2026-10-17-000018](https://palomar-registry.org/entry.html?id=PALOMAR-2026-10-17-000018&version=1) (v1) · [jtraverso/moore-graphs-hoffman-singleton @ 8819ccf](https://github.com/jtraverso/moore-graphs-hoffman-singleton/tree/8819ccfea5474fab3d1cbc17e703860a4e008254) · [archived copy](https://github.com/PalomarArchive/jtraverso--moore-graphs-hoffman-singleton--c0de8dabed2e/tree/palomar/PALOMAR-2026-10-17-000018-v1/8819ccfea5474fab3d1cbc17e703860a4e008254)

**Sources:**

* A. J. Hoffman, R. R. Singleton, *On Moore Graphs with Diameters 2 and 3*, IBM Journal of Research and Development 4 (1960), 497–504. [doi:10.1147/rd.45.0497](https://doi.org/10.1147/rd.45.0497)

<details><summary>What is formalized</summary>

A Lean 4 / Mathlib formalization of the Hoffman–Singleton theorem on Moore graphs of diameter two. For a finite k-regular graph of diameter at most two: the Moore bound n ≤ k² + 1; if moreover the girth is at least five, then n = k² + 1 and the graph is strongly regular with parameters (k² + 1, k, 0, 1); and, if k ≥ 2, then k ∈ {2, 3, 7, 57}. Mathlib has strongly regular graphs and the spectral theorem for Hermitian matrices, but not this theorem.

</details>

#### Spectral bounds on the chromatic and independence numbers

[PALOMAR-2026-10-18-000016](https://palomar-registry.org/entry.html?id=PALOMAR-2026-10-18-000016&version=1) (v1) · [jtraverso/spectral-graph-bounds @ 8d8b4ce](https://github.com/jtraverso/spectral-graph-bounds/tree/8d8b4ce17e56165b5f1ad3b285fb141666804e1c) · [archived copy](https://github.com/PalomarArchive/jtraverso--spectral-graph-bounds--08d3a675ea5f/tree/palomar/PALOMAR-2026-10-18-000016-v1/8d8b4ce17e56165b5f1ad3b285fb141666804e1c)

**Sources:**

* L. Collatz, U. Sinogowitz, *Spektren endlicher Grafen*, Abhandlungen aus dem Mathematischen Seminar der Universität Hamburg 21 (1957), 63–77. [doi:10.1007/BF02941924](https://doi.org/10.1007/BF02941924)
* H. S. Wilf, *The Eigenvalues of a Graph and Its Chromatic Number*, Journal of the London Mathematical Society 42 (1967), 330–332. [doi:10.1112/jlms/s1-42.1.330](https://doi.org/10.1112/jlms/s1-42.1.330)
* A. J. Hoffman, *On eigenvalues and colorings of graphs*, In: B. Harris (ed.), Graph Theory and its Applications, Academic Press, New York (1970), 79–91.

<details><summary>Background references</summary>

* L. Lovász, *On the Shannon capacity of a graph*, IEEE Transactions on Information Theory 25 (1979), 1–7. [doi:10.1109/TIT.1979.1055985](https://doi.org/10.1109/TIT.1979.1055985)

</details>

<details><summary>What is formalized</summary>

A Lean 4 / Mathlib formalization of classical eigenvalue bounds for a finite simple graph G on a nonempty vertex type, with λ_max and λ_min the largest and smallest eigenvalues of its real adjacency matrix: the average degree is at most λ_max and λ_max is at most the maximum degree (Collatz–Sinogowitz); G is (⌊λ_max⌋ + 1)-colourable (Wilf 1967); if G has an edge, every proper colouring uses at least 1 − λ_max/λ_min colours (Hoffman 1970); and if G is k-regular with k ≥ 1, every independent set has at most n(−λ_min)/(k − λ_min) vertices (Hoffman's ratio bound). Mathlib has the spectral theorem for Hermitian matrices but none of these bounds.

</details>

#### Lovász's bound on the Shannon capacity

[PALOMAR-2026-10-21-000003](https://palomar-registry.org/entry.html?id=PALOMAR-2026-10-21-000003&version=1) (v1) · [jtraverso/lovasz-theta @ 2d506b5](https://github.com/jtraverso/lovasz-theta/tree/2d506b5abca378d9133b5e3f1264a5316843c9a7) · [archived copy](https://github.com/PalomarArchive/jtraverso--lovasz-theta--8c936f7e6f5c/tree/palomar/PALOMAR-2026-10-21-000003-v1/2d506b5abca378d9133b5e3f1264a5316843c9a7)

**Sources:**

* L. Lovász, *On the Shannon capacity of a graph*, IEEE Transactions on Information Theory 25 (1979), 1–7. [doi:10.1109/TIT.1979.1055985](https://doi.org/10.1109/TIT.1979.1055985)
* C. E. Shannon, *The zero error capacity of a noisy channel*, IRE Transactions on Information Theory 2 (1956), 8–19. [doi:10.1109/TIT.1956.1056798](https://doi.org/10.1109/TIT.1956.1056798)

<details><summary>What is formalized</summary>

A Lean 4 / Mathlib formalization of Lovász's orthonormal-representation bound on the independence number (if u is an orthonormal representation of G with handle c and 1 ≤ t (c·u_i)² for every vertex, then α(G) ≤ t), of its multiplicativity under strong powers (α(G^⊠k) ≤ t^k), and of its application to the pentagon: α(C₅^⊠k)² ≤ 5^k for every k, Shannon's α(C₅^⊠2) = 5, and hence the Shannon capacity Θ(C₅) = √5. Mathlib has independence numbers but neither strong graph products nor the Shannon capacity.

</details>

#### The expander mixing lemma and the Alon–Boppana bound

[PALOMAR-2026-10-22-000035](https://palomar-registry.org/entry.html?id=PALOMAR-2026-10-22-000035&version=1) (v1) · [jtraverso/expander-spectral @ f96a998](https://github.com/jtraverso/expander-spectral/tree/f96a99893d4d31495af5f8d9e6181f7b4c91e0ba) · [archived copy](https://github.com/PalomarArchive/jtraverso--expander-spectral--c7934103ea1e/tree/palomar/PALOMAR-2026-10-22-000035-v1/f96a99893d4d31495af5f8d9e6181f7b4c91e0ba)

**Sources:**

* N. Alon, F. R. K. Chung, *Explicit construction of linear sized tolerant networks*, Discrete Mathematics 72 (1988), 15–19. [doi:10.1016/0012-365X(88)90189-6](https://doi.org/10.1016/0012-365X(88)90189-6) · free to read at the publisher
* A. Nilli, *On the second eigenvalue of a graph*, Discrete Mathematics 91 (1991), 207–210. [doi:10.1016/0012-365X(91)90112-F](https://doi.org/10.1016/0012-365X(91)90112-F) · free to read at the publisher

<details><summary>Background references</summary>

* S. Hoory, N. Linial, A. Wigderson, *Expander graphs and their applications*, Bulletin of the American Mathematical Society 43 (2006), 439–561. [doi:10.1090/S0273-0979-06-01126-8](https://doi.org/10.1090/S0273-0979-06-01126-8) · free to read at the publisher

</details>

<details><summary>What is formalized</summary>

A Lean 4 / Mathlib formalization of two basic results of spectral graph theory, stated through the adjacency quadratic form on vectors orthogonal to the all-ones vector: the expander mixing lemma of Alon and Chung (for a d-regular graph on n ≥ 2 vertices with |x·Ax| ≤ μ‖x‖² on 𝟙⊥, |e(S,T) − d|S||T|/n| ≤ μ√(|S||T|)), and the Alon–Boppana bound in Nilli's form (a d-regular graph, d ≥ 2, with two vertices at distance at least 2k + 4 has a nonzero x ⟂ 𝟙 with x·Ax ≥ (2√(d−1) − (2√(d−1) − 1)/(k+1))‖x‖²). Mathlib has adjacency matrices but neither result.

</details>

#### The Graham–Pollak theorem

[PALOMAR-2026-10-23-000006](https://palomar-registry.org/entry.html?id=PALOMAR-2026-10-23-000006&version=1) (v1) · [jtraverso/graham-pollak @ 68d32f0](https://github.com/jtraverso/graham-pollak/tree/68d32f0faf102fc1716ac89ffc861eefe897e749) · [archived copy](https://github.com/PalomarArchive/jtraverso--graham-pollak--3485c9d9d4a5/tree/palomar/PALOMAR-2026-10-23-000006-v1/68d32f0faf102fc1716ac89ffc861eefe897e749)

**Sources:**

* R. L. Graham, H. O. Pollak, *On the addressing problem for loop switching*, Bell System Technical Journal 50 (1971), 2495–2519. [doi:10.1002/j.1538-7305.1971.tb02618.x](https://doi.org/10.1002/j.1538-7305.1971.tb02618.x)

<details><summary>Background references</summary>

* H. Tverberg, *On the decomposition of K_n into complete bipartite graphs*, Journal of Graph Theory 6 (1982), 493–494. [doi:10.1002/jgt.3190060414](https://doi.org/10.1002/jgt.3190060414)

</details>

<details><summary>What is formalized</summary>

A Lean 4 / Mathlib formalization of the Graham–Pollak theorem: the edge set of the complete graph K_n cannot be partitioned into fewer than n − 1 complete bipartite graphs, together with the matching construction by n − 1 stars. Biclique decompositions are encoded by families of pairs of disjoint vertex sets covering every pair of distinct vertices exactly once. Mathlib does not contain this theorem.

</details>

## Registration log

All entries in order of registration.

| Palomar entry | Result | Registered | Source | Archived copy |
|---|---|---|---|---|
| [PALOMAR-2026-10-13-000005](https://palomar-registry.org/entry.html?id=PALOMAR-2026-10-13-000005&version=2) (v2) | Grötzsch's theorem, Ore's conjecture for k = 4 (Kostochka–Yancey), and the Grünbaum–Aksenov theorem | v1 2026-10-13, v2 2026-10-15 | [jtraverso/grotzsch-ore @ ff6d512](https://github.com/jtraverso/grotzsch-ore/tree/ff6d5123c06e4c99bb6074e0a72e8be8d595eefa) (v1: [f923c45](https://github.com/jtraverso/grotzsch-ore/tree/f923c459969d4a0a50d034cc02d558c7d4937436)) | [PalomarArchive](https://github.com/PalomarArchive/jtraverso--grotzsch-ore--8ebd0df3e665/tree/palomar/PALOMAR-2026-10-13-000005-v2/ff6d5123c06e4c99bb6074e0a72e8be8d595eefa) (v1: [archive](https://github.com/PalomarArchive/jtraverso--grotzsch-ore--8ebd0df3e665/tree/palomar/PALOMAR-2026-10-13-000005-v1/f923c459969d4a0a50d034cc02d558c7d4937436)) |
| [PALOMAR-2026-10-13-000007](https://palomar-registry.org/entry.html?id=PALOMAR-2026-10-13-000007&version=1) (v1) | The Hajnal–Szemerédi theorem on equitable colourings | 2026-10-13 | [jtraverso/hajnal-szemeredi @ ba34061](https://github.com/jtraverso/hajnal-szemeredi/tree/ba34061e3cf12dfc8297610d5d7b3f0afac7ec54) | [PalomarArchive](https://github.com/PalomarArchive/jtraverso--hajnal-szemeredi--c11276c44bab/tree/palomar/PALOMAR-2026-10-13-000007-v1/ba34061e3cf12dfc8297610d5d7b3f0afac7ec54) |
| [PALOMAR-2026-10-15-000003](https://palomar-registry.org/entry.html?id=PALOMAR-2026-10-15-000003&version=1) (v1) | The list chromatic index of complete graphs (Häggkvist–Janssen) | 2026-10-15 | [jtraverso/haggkvist-janssen @ 807e08b](https://github.com/jtraverso/haggkvist-janssen/tree/807e08bd7c480d4fae80c1b78377d23989d39ab0) | [PalomarArchive](https://github.com/PalomarArchive/jtraverso--haggkvist-janssen--3449623606b5/tree/palomar/PALOMAR-2026-10-15-000003-v1/807e08bd7c480d4fae80c1b78377d23989d39ab0) |
| [PALOMAR-2026-10-15-000004](https://palomar-registry.org/entry.html?id=PALOMAR-2026-10-15-000004&version=2) (v2) | Vizing's theorem and equitable edge colourings | 2026-10-15, v2 2026-10-29 | [jtraverso/vizing @ 33b2de8](https://github.com/jtraverso/vizing/tree/33b2de836095cf92bc1dec33b6f8787e4036bbc6) | [PalomarArchive](https://github.com/PalomarArchive/jtraverso--vizing--01fa5f875100/tree/palomar/PALOMAR-2026-10-15-000004-v2/33b2de836095cf92bc1dec33b6f8787e4036bbc6) |
| [PALOMAR-2026-10-15-000005](https://palomar-registry.org/entry.html?id=PALOMAR-2026-10-15-000005&version=1) (v1) | Wagner's planarity criterion and list colouring of planar and K₅-minor-free graphs | 2026-10-15 | [jtraverso/planar-list-colouring @ ec1eafb](https://github.com/jtraverso/planar-list-colouring/tree/ec1eafbc091713857eb5683a46e460902b2d47b3) | [PalomarArchive](https://github.com/PalomarArchive/jtraverso--planar-list-colouring--03a15f1929ab/tree/palomar/PALOMAR-2026-10-15-000005-v1/ec1eafbc091713857eb5683a46e460902b2d47b3) |
| [PALOMAR-2026-10-15-000008](https://palomar-registry.org/entry.html?id=PALOMAR-2026-10-15-000008&version=1) (v1) | Dross's theorem on fractional triangle decompositions | 2026-10-15 | [jtraverso/dross-fractional-triangle-decomposition @ 7720b7b](https://github.com/jtraverso/dross-fractional-triangle-decomposition/tree/7720b7b591e606d5a56f1d935d8be650dcbf6c6f) | [PalomarArchive](https://github.com/PalomarArchive/jtraverso--dross-fractional-triangle-decomposition--f57504b1525c/tree/palomar/PALOMAR-2026-10-15-000008-v1/7720b7b591e606d5a56f1d935d8be650dcbf6c6f) |
| [PALOMAR-2026-10-15-000009](https://palomar-registry.org/entry.html?id=PALOMAR-2026-10-15-000009&version=1) (v1) | The Beck–Fiala integer-making theorem | 2026-10-15 | [jtraverso/beck-fiala @ 52f1a12](https://github.com/jtraverso/beck-fiala/tree/52f1a12a140b0589ac39619dfd07807d98fdbaf5) | [PalomarArchive](https://github.com/PalomarArchive/jtraverso--beck-fiala--f2fa29dec96f/tree/palomar/PALOMAR-2026-10-15-000009-v1/52f1a12a140b0589ac39619dfd07807d98fdbaf5) |
| [PALOMAR-2026-10-15-000011](https://palomar-registry.org/entry.html?id=PALOMAR-2026-10-15-000011&version=2) (v2) | Near-regular hypergraph matchings and the asymptotic triangle-packing gap | 2026-10-15, v2 2026-10-30 | [jtraverso/asymptotic-triangle-packing @ 760e503](https://github.com/jtraverso/asymptotic-triangle-packing/tree/760e503972aad8ca9da7904ce72e5cce405f5991) | [PalomarArchive](https://github.com/PalomarArchive/jtraverso--asymptotic-triangle-packing--a2c3300bc8ff/tree/palomar/PALOMAR-2026-10-15-000011-v2/760e503972aad8ca9da7904ce72e5cce405f5991) |
| [PALOMAR-2026-10-15-000018](https://palomar-registry.org/entry.html?id=PALOMAR-2026-10-15-000018&version=1) (v1) | Kuratowski's theorem | 2026-10-15 | [jtraverso/kuratowski @ 696ec89](https://github.com/jtraverso/kuratowski/tree/696ec897a9b91933037767d897670aa30ba3683a) | [PalomarArchive](https://github.com/PalomarArchive/jtraverso--kuratowski--c5380f41889a/tree/palomar/PALOMAR-2026-10-15-000018-v1/696ec897a9b91933037767d897670aa30ba3683a) |
| [PALOMAR-2026-10-15-000019](https://palomar-registry.org/entry.html?id=PALOMAR-2026-10-15-000019&version=1) (v1) | Kőnig's theorems and Dilworth's theorem | 2026-10-15 | [jtraverso/konig-edge-colouring @ 7c60f7e](https://github.com/jtraverso/konig-edge-colouring/tree/7c60f7efb69c1747aaf39e5dfa7a89d907cd84ef) | [PalomarArchive](https://github.com/PalomarArchive/jtraverso--konig-edge-colouring--5e0f844003ab/tree/palomar/PALOMAR-2026-10-15-000019-v1/7c60f7efb69c1747aaf39e5dfa7a89d907cd84ef) |
| [PALOMAR-2026-10-15-000020](https://palomar-registry.org/entry.html?id=PALOMAR-2026-10-15-000020&version=2) (v2) | Menger's theorem, Hamiltonian cycles, long cycles and pancyclicity | 2026-10-19 | [jtraverso/menger-hamiltonian @ 35c5f68](https://github.com/jtraverso/menger-hamiltonian/tree/35c5f684f9bfbd244bd0999ce725623ab571adb6) | [PalomarArchive](https://github.com/PalomarArchive/jtraverso--menger-hamiltonian--0fd5dfe41e84/tree/palomar/PALOMAR-2026-10-15-000020-v2/35c5f684f9bfbd244bd0999ce725623ab571adb6) |
| [PALOMAR-2026-10-15-000021](https://palomar-registry.org/entry.html?id=PALOMAR-2026-10-15-000021&version=1) (v1) | Classical bounds for graph Ramsey numbers | 2026-10-15 | [jtraverso/ramsey-graph-bounds @ 562986a](https://github.com/jtraverso/ramsey-graph-bounds/tree/562986a7ce9edf086c20b3a2b8c7d5ace2ffd843) | [PalomarArchive](https://github.com/PalomarArchive/jtraverso--ramsey-graph-bounds--d35ec49e7ff6/tree/palomar/PALOMAR-2026-10-15-000021-v1/562986a7ce9edf086c20b3a2b8c7d5ace2ffd843) |
| [PALOMAR-2026-10-16-000001](https://palomar-registry.org/entry.html?id=PALOMAR-2026-10-16-000001&version=1) (v1) | Mader's theorem and Hadwiger's conjecture for t ≤ 4 | 2026-10-16 | [jtraverso/hadwiger-mader @ cb10154](https://github.com/jtraverso/hadwiger-mader/tree/cb10154cd439a419d0bbf34052839dd27242b619) | [PalomarArchive](https://github.com/PalomarArchive/jtraverso--hadwiger-mader--a4b96dfb7362/tree/palomar/PALOMAR-2026-10-16-000001-v1/cb10154cd439a419d0bbf34052839dd27242b619) |
| [PALOMAR-2026-10-16-000003](https://palomar-registry.org/entry.html?id=PALOMAR-2026-10-16-000003&version=2) (v2) | Brooks' theorem, degree-choosability and blocks | 2026-10-19 | [jtraverso/brooks @ b99e6f5](https://github.com/jtraverso/brooks/tree/b99e6f500256586626396de9c2d6fd4d96119d60) | [PalomarArchive](https://github.com/PalomarArchive/jtraverso--brooks--c255f4f55cbf/tree/palomar/PALOMAR-2026-10-16-000003-v2/b99e6f500256586626396de9c2d6fd4d96119d60) |
| [PALOMAR-2026-10-16-000004](https://palomar-registry.org/entry.html?id=PALOMAR-2026-10-16-000004&version=1) (v1) | Petersen's theorem | 2026-10-16 | [jtraverso/petersen-matching @ 77630d6](https://github.com/jtraverso/petersen-matching/tree/77630d6771d3f5a3da2185db2ff451f6c6ed5190) | [PalomarArchive](https://github.com/PalomarArchive/jtraverso--petersen-matching--386afe9ae9e1/tree/palomar/PALOMAR-2026-10-16-000004-v1/77630d6771d3f5a3da2185db2ff451f6c6ed5190) |
| [PALOMAR-2026-10-16-000011](https://palomar-registry.org/entry.html?id=PALOMAR-2026-10-16-000011&version=2) (v2) | Berge's theorem, the Tutte–Berge formula and the Gallai–Edmonds theorem | 2026-10-19 | [jtraverso/berge-matching @ f01d042](https://github.com/jtraverso/berge-matching/tree/f01d042c071c778fb3f432312356136a92369076) | [PalomarArchive](https://github.com/PalomarArchive/jtraverso--berge-matching--b269b121c46f/tree/palomar/PALOMAR-2026-10-16-000011-v2/f01d042c071c778fb3f432312356136a92369076) |
| [PALOMAR-2026-10-16-000015](https://palomar-registry.org/entry.html?id=PALOMAR-2026-10-16-000015&version=1) (v1) | The Gallai–Hasse–Roy–Vitaver theorem | 2026-10-16 | [jtraverso/gallai-roy @ e737218](https://github.com/jtraverso/gallai-roy/tree/e737218bf80c3d3684d670f5f8aa9a8257e1a52f) | [PalomarArchive](https://github.com/PalomarArchive/jtraverso--gallai-roy--242cd45a936c/tree/palomar/PALOMAR-2026-10-16-000015-v1/e737218bf80c3d3684d670f5f8aa9a8257e1a52f) |
| [PALOMAR-2026-10-16-000016](https://palomar-registry.org/entry.html?id=PALOMAR-2026-10-16-000016&version=1) (v1) | Euler's theorem on Eulerian circuits and trails, and Petersen's 2-factor theorem | 2026-10-16 | [jtraverso/euler-petersen @ 02c3f1a](https://github.com/jtraverso/euler-petersen/tree/02c3f1a5327c5f066938860bb07e9fce226b36ca) | [PalomarArchive](https://github.com/PalomarArchive/jtraverso--euler-petersen--780912a29df2/tree/palomar/PALOMAR-2026-10-16-000016-v1/02c3f1a5327c5f066938860bb07e9fce226b36ca) |
| [PALOMAR-2026-10-16-000017](https://palomar-registry.org/entry.html?id=PALOMAR-2026-10-16-000017&version=1) (v1) | Graphic sequences: the Erdős–Gallai and Havel–Hakimi theorems | 2026-10-16 | [jtraverso/degree-sequences @ b49808e](https://github.com/jtraverso/degree-sequences/tree/b49808e0c0aade945472b777047148399a582858) | [PalomarArchive](https://github.com/PalomarArchive/jtraverso--degree-sequences--21c02be05315/tree/palomar/PALOMAR-2026-10-16-000017-v1/b49808e0c0aade945472b777047148399a582858) |
| [PALOMAR-2026-10-16-000019](https://palomar-registry.org/entry.html?id=PALOMAR-2026-10-16-000019&version=1) (v1) | The Cauchy–Binet formula, Kirchhoff's matrix-tree theorem and Cayley's formula | 2026-10-16 | [jtraverso/matrix-tree @ aeab0f2](https://github.com/jtraverso/matrix-tree/tree/aeab0f267c523dd3cac9a287b589f65a99d20d01) | [PalomarArchive](https://github.com/PalomarArchive/jtraverso--matrix-tree--5efe2b63de2b/tree/palomar/PALOMAR-2026-10-16-000019-v1/aeab0f267c523dd3cac9a287b589f65a99d20d01) |
| [PALOMAR-2026-10-16-000024](https://palomar-registry.org/entry.html?id=PALOMAR-2026-10-16-000024&version=1) (v1) | Füredi's stability theorem and the Erdős–Simonovits stability theorem | 2026-10-16 | [jtraverso/turan-stability @ 3eb9903](https://github.com/jtraverso/turan-stability/tree/3eb99033cc931add291781f77b7446dcba8f5f9d) | [PalomarArchive](https://github.com/PalomarArchive/jtraverso--turan-stability--e49ed8b57e3c/tree/palomar/PALOMAR-2026-10-16-000024-v1/3eb99033cc931add291781f77b7446dcba8f5f9d) |
| [PALOMAR-2026-10-17-000004](https://palomar-registry.org/entry.html?id=PALOMAR-2026-10-17-000004&version=1) (v1) | Pseudorandom hypergraph matchings (Ehard–Glock–Joos) | 2026-10-17 | [jtraverso/pseudorandom-hypergraph-matchings @ 3957f3c](https://github.com/jtraverso/pseudorandom-hypergraph-matchings/tree/3957f3c0dbc34fd310cb5fecf7941fddc9ef6c8f) | [PalomarArchive](https://github.com/PalomarArchive/jtraverso--pseudorandom-hypergraph-matchings--40c1ca802506/tree/palomar/PALOMAR-2026-10-17-000004-v1/3957f3c0dbc34fd310cb5fecf7941fddc9ef6c8f) |
| [PALOMAR-2026-10-17-000008](https://palomar-registry.org/entry.html?id=PALOMAR-2026-10-17-000008&version=1) (v1) | The Nash-Williams–Tutte tree packing theorem and Nash-Williams' arboricity theorem | 2026-10-17 | [jtraverso/nash-williams-trees @ 101e488](https://github.com/jtraverso/nash-williams-trees/tree/101e48847a929dd8102521f57723e2137989ce2e) | [PalomarArchive](https://github.com/PalomarArchive/jtraverso--nash-williams-trees--9280327cd578/tree/palomar/PALOMAR-2026-10-17-000008-v1/101e48847a929dd8102521f57723e2137989ce2e) |
| [PALOMAR-2026-10-17-000009](https://palomar-registry.org/entry.html?id=PALOMAR-2026-10-17-000009&version=2) (v2) | Graphs of large girth and large chromatic number: Erdős, Mycielski, and the fractional chromatic number of Mycielski graphs | 2026-10-17, v2 2026-10-28 | [jtraverso/erdos-girth-chromatic @ 05407c1](https://github.com/jtraverso/erdos-girth-chromatic/tree/05407c110b29ebb412667c688b2758d23bc744dd) | [PalomarArchive](https://github.com/PalomarArchive/jtraverso--erdos-girth-chromatic--0532ff066cce/tree/palomar/PALOMAR-2026-10-17-000009-v2/05407c110b29ebb412667c688b2758d23bc744dd) |
| [PALOMAR-2026-10-17-000018](https://palomar-registry.org/entry.html?id=PALOMAR-2026-10-17-000018&version=1) (v1) | Moore graphs of diameter two: the Hoffman–Singleton theorem | 2026-10-17 | [jtraverso/moore-graphs-hoffman-singleton @ 8819ccf](https://github.com/jtraverso/moore-graphs-hoffman-singleton/tree/8819ccfea5474fab3d1cbc17e703860a4e008254) | [PalomarArchive](https://github.com/PalomarArchive/jtraverso--moore-graphs-hoffman-singleton--c0de8dabed2e/tree/palomar/PALOMAR-2026-10-17-000018-v1/8819ccfea5474fab3d1cbc17e703860a4e008254) |
| [PALOMAR-2026-10-18-000001](https://palomar-registry.org/entry.html?id=PALOMAR-2026-10-18-000001&version=1) (v1) | Chvátal's and Pósa's degree conditions for Hamiltonian cycles | 2026-10-18 | [jtraverso/chvatal-posa-hamiltonian @ 6be0ebd](https://github.com/jtraverso/chvatal-posa-hamiltonian/tree/6be0ebda7b457b85ad400f6d7f92ad156d6e7712) | [PalomarArchive](https://github.com/PalomarArchive/jtraverso--chvatal-posa-hamiltonian--3158a08a16e2/tree/palomar/PALOMAR-2026-10-18-000001-v1/6be0ebda7b457b85ad400f6d7f92ad156d6e7712) |
| [PALOMAR-2026-10-18-000002](https://palomar-registry.org/entry.html?id=PALOMAR-2026-10-18-000002&version=1) (v1) | The graph removal lemma for every fixed graph | 2026-10-18 | [jtraverso/graph-removal-lemma @ 589cf03](https://github.com/jtraverso/graph-removal-lemma/tree/589cf03ef1e4c80ea8cdd6be77778232c62dd37c) | [PalomarArchive](https://github.com/PalomarArchive/jtraverso--graph-removal-lemma--03befbbe3fbf/tree/palomar/PALOMAR-2026-10-18-000002-v1/589cf03ef1e4c80ea8cdd6be77778232c62dd37c) |
| [PALOMAR-2026-10-18-000005](https://palomar-registry.org/entry.html?id=PALOMAR-2026-10-18-000005&version=1) (v1) | Tutte's f-factor theorem | 2026-10-18 | [jtraverso/tutte-f-factor @ dc3bbce](https://github.com/jtraverso/tutte-f-factor/tree/dc3bbce463c80c499d3e9fa072d13f9145d907d0) | [PalomarArchive](https://github.com/PalomarArchive/jtraverso--tutte-f-factor--c791dc403ea0/tree/palomar/PALOMAR-2026-10-18-000005-v1/dc3bbce463c80c499d3e9fa072d13f9145d907d0) |
| [PALOMAR-2026-10-18-000006](https://palomar-registry.org/entry.html?id=PALOMAR-2026-10-18-000006&version=1) (v1) | Chordal, split, threshold and cograph structure | 2026-10-18 | [jtraverso/chordal-split-threshold-graphs @ ed65dcd](https://github.com/jtraverso/chordal-split-threshold-graphs/tree/ed65dcdc7339767d3e8e412420abbf54eae65ddb) | [PalomarArchive](https://github.com/PalomarArchive/jtraverso--chordal-split-threshold-graphs--600d961f6749/tree/palomar/PALOMAR-2026-10-18-000006-v1/ed65dcdc7339767d3e8e412420abbf54eae65ddb) |
| [PALOMAR-2026-10-18-000009](https://palomar-registry.org/entry.html?id=PALOMAR-2026-10-18-000009&version=3) (v3) | Jaeger's 4-flow and 8-flow theorems and Seymour's 6-flow theorem | 2026-10-21 | [jtraverso/jaeger-four-flow @ 623dd0d](https://github.com/jtraverso/jaeger-four-flow/tree/623dd0dd718f93de06d4dc792e116dd32ef97553) | [PalomarArchive](https://github.com/PalomarArchive/jtraverso--jaeger-four-flow--4443e53b8984/tree/palomar/PALOMAR-2026-10-18-000009-v3/623dd0dd718f93de06d4dc792e116dd32ef97553) |
| [PALOMAR-2026-10-18-000011](https://palomar-registry.org/entry.html?id=PALOMAR-2026-10-18-000011&version=1) (v1) | Dirac's theorem: k vertices of a k-connected graph lie on a common cycle | 2026-10-18 | [jtraverso/dirac-common-cycle @ 3c9e996](https://github.com/jtraverso/dirac-common-cycle/tree/3c9e9966662cb99c0e4f11d771011bc904dc627f) | [PalomarArchive](https://github.com/PalomarArchive/jtraverso--dirac-common-cycle--7eeee5978914/tree/palomar/PALOMAR-2026-10-18-000011-v1/3c9e9966662cb99c0e4f11d771011bc904dc627f) |
| [PALOMAR-2026-10-18-000016](https://palomar-registry.org/entry.html?id=PALOMAR-2026-10-18-000016&version=1) (v1) | Spectral bounds on the chromatic and independence numbers | 2026-10-18 | [jtraverso/spectral-graph-bounds @ 8d8b4ce](https://github.com/jtraverso/spectral-graph-bounds/tree/8d8b4ce17e56165b5f1ad3b285fb141666804e1c) | [PalomarArchive](https://github.com/PalomarArchive/jtraverso--spectral-graph-bounds--08d3a675ea5f/tree/palomar/PALOMAR-2026-10-18-000016-v1/8d8b4ce17e56165b5f1ad3b285fb141666804e1c) |
| [PALOMAR-2026-10-18-000022](https://palomar-registry.org/entry.html?id=PALOMAR-2026-10-18-000022&version=1) (v1) | Robbins' theorem on strongly connected orientations | 2026-10-18 | [jtraverso/robbins-strong-orientation @ 076e734](https://github.com/jtraverso/robbins-strong-orientation/tree/076e734e9949720d3e4fcc2cc3cad4284871442c) | [PalomarArchive](https://github.com/PalomarArchive/jtraverso--robbins-strong-orientation--f05c2621ca9e/tree/palomar/PALOMAR-2026-10-18-000022-v1/076e734e9949720d3e4fcc2cc3cad4284871442c) |
| [PALOMAR-2026-10-18-000029](https://palomar-registry.org/entry.html?id=PALOMAR-2026-10-18-000029&version=2) (v2) | Galvin's theorem for bipartite multigraphs, the Dinitz problem and stable matchings | 2026-10-18, v2 2026-10-29 | [jtraverso/galvin-dinitz @ 84dcda4](https://github.com/jtraverso/galvin-dinitz/tree/84dcda4c2a760f2b52b7e813affe7e6968f8bfce) | [PalomarArchive](https://github.com/PalomarArchive/jtraverso--galvin-dinitz--befd03f21f2b/tree/palomar/PALOMAR-2026-10-18-000029-v2/84dcda4c2a760f2b52b7e813affe7e6968f8bfce) |
| [PALOMAR-2026-10-19-000013](https://palomar-registry.org/entry.html?id=PALOMAR-2026-10-19-000013&version=1) (v1) | The Alon–Tarsi theorem and 3-choosability of planar bipartite graphs | 2026-10-19 | [jtraverso/alon-tarsi-choosability @ 4ab98b1](https://github.com/jtraverso/alon-tarsi-choosability/tree/4ab98b11f340ea2160b34d0b57ef7102452b98cc) | [PalomarArchive](https://github.com/PalomarArchive/jtraverso--alon-tarsi-choosability--e8601c7736f7/tree/palomar/PALOMAR-2026-10-19-000013-v1/4ab98b11f340ea2160b34d0b57ef7102452b98cc) |
| [PALOMAR-2026-10-20-000003](https://palomar-registry.org/entry.html?id=PALOMAR-2026-10-20-000003&version=1) (v1) | The Erdős–Pósa theorem for cycles | 2026-10-20 | [jtraverso/erdos-posa-cycles @ 67bfea6](https://github.com/jtraverso/erdos-posa-cycles/tree/67bfea6b3893ffdf57e76cd83c9c3538647bdec8) | [PalomarArchive](https://github.com/PalomarArchive/jtraverso--erdos-posa-cycles--495ed139acca/tree/palomar/PALOMAR-2026-10-20-000003-v1/67bfea6b3893ffdf57e76cd83c9c3538647bdec8) |
| [PALOMAR-2026-10-20-000004](https://palomar-registry.org/entry.html?id=PALOMAR-2026-10-20-000004&version=1) (v1) | The Lovász Local Lemma and two applications | 2026-10-20 | [jtraverso/lovasz-local-lemma @ 9d020fa](https://github.com/jtraverso/lovasz-local-lemma/tree/9d020fa8fb20e9426c2d6780a3cfab4a68794d89) | [PalomarArchive](https://github.com/PalomarArchive/jtraverso--lovasz-local-lemma--3b6f209cddb3/tree/palomar/PALOMAR-2026-10-20-000004-v1/9d020fa8fb20e9426c2d6780a3cfab4a68794d89) |
| [PALOMAR-2026-10-20-000006](https://palomar-registry.org/entry.html?id=PALOMAR-2026-10-20-000006&version=1) (v1) | Kneser's conjecture and the octahedral Tucker lemma | 2026-10-20 | [jtraverso/kneser-lovasz @ 6699c87](https://github.com/jtraverso/kneser-lovasz/tree/6699c87d87f4ddb159fc42271263fc429e63004a) | [PalomarArchive](https://github.com/PalomarArchive/jtraverso--kneser-lovasz--c99016c66bcc/tree/palomar/PALOMAR-2026-10-20-000006-v1/6699c87d87f4ddb159fc42271263fc429e63004a) |
| [PALOMAR-2026-10-20-000012](https://palomar-registry.org/entry.html?id=PALOMAR-2026-10-20-000012&version=1) (v1) | Jin's theorem on dense triangle-free graphs | 2026-10-20 | [jtraverso/jin-triangle-free @ ae47df0](https://github.com/jtraverso/jin-triangle-free/tree/ae47df0ddb29c58a71afed658f9bf74aef1b6e90) | [PalomarArchive](https://github.com/PalomarArchive/jtraverso--jin-triangle-free--8d9fbb5efd5d/tree/palomar/PALOMAR-2026-10-20-000012-v1/ae47df0ddb29c58a71afed658f9bf74aef1b6e90) |
| [PALOMAR-2026-10-21-000003](https://palomar-registry.org/entry.html?id=PALOMAR-2026-10-21-000003&version=1) (v1) | Lovász's bound on the Shannon capacity | 2026-10-21 | [jtraverso/lovasz-theta @ 2d506b5](https://github.com/jtraverso/lovasz-theta/tree/2d506b5abca378d9133b5e3f1264a5316843c9a7) | [PalomarArchive](https://github.com/PalomarArchive/jtraverso--lovasz-theta--8c936f7e6f5c/tree/palomar/PALOMAR-2026-10-21-000003-v1/2d506b5abca378d9133b5e3f1264a5316843c9a7) |
| [PALOMAR-2026-10-21-000007](https://palomar-registry.org/entry.html?id=PALOMAR-2026-10-21-000007&version=1) (v1) | Lovász's perfect graph theorems | 2026-10-21 | [jtraverso/perfect-graphs @ 7969224](https://github.com/jtraverso/perfect-graphs/tree/796922460172c4e51c39c96575d03957652c0bab) | [PalomarArchive](https://github.com/PalomarArchive/jtraverso--perfect-graphs--f01c6e39f696/tree/palomar/PALOMAR-2026-10-21-000007-v1/796922460172c4e51c39c96575d03957652c0bab) |
| [PALOMAR-2026-10-21-000009](https://palomar-registry.org/entry.html?id=PALOMAR-2026-10-21-000009&version=1) (v1) | The Nash–Williams triangle-decomposition theorem | 2026-10-21 | [jtraverso/nash-williams-lean @ 2603197](https://github.com/jtraverso/nash-williams-lean/tree/2603197abdbf0a600ec663f6f046f70fbd209d4a) | [PalomarArchive](https://github.com/PalomarArchive/jtraverso--nash-williams-lean--252fc7828395/tree/palomar/PALOMAR-2026-10-21-000009-v1/2603197abdbf0a600ec663f6f046f70fbd209d4a) |
| [PALOMAR-2026-10-22-000017](https://palomar-registry.org/entry.html?id=PALOMAR-2026-10-22-000017&version=2) (v2) | Counting Steiner triple systems: Wilson (1974) and Linial–Luria (2013) | 2026-10-22 | [jtraverso/counting-steiner-triple-systems @ 52fda83](https://github.com/jtraverso/counting-steiner-triple-systems/tree/52fda83038df7442c576e17edffba591db703cb8) | [PalomarArchive](https://github.com/PalomarArchive/jtraverso--counting-steiner-triple-systems--25dd3ac3d9ea/tree/palomar/PALOMAR-2026-10-22-000017-v1/52fda83038df7442c576e17edffba591db703cb8) |
| [PALOMAR-2026-10-22-000035](https://palomar-registry.org/entry.html?id=PALOMAR-2026-10-22-000035&version=1) (v1) | The expander mixing lemma and the Alon–Boppana bound | 2026-10-22 | [jtraverso/expander-spectral @ f96a998](https://github.com/jtraverso/expander-spectral/tree/f96a99893d4d31495af5f8d9e6181f7b4c91e0ba) | [PalomarArchive](https://github.com/PalomarArchive/jtraverso--expander-spectral--c7934103ea1e/tree/palomar/PALOMAR-2026-10-22-000035-v1/f96a99893d4d31495af5f8d9e6181f7b4c91e0ba) |
| [PALOMAR-2026-10-22-000043](https://palomar-registry.org/entry.html?id=PALOMAR-2026-10-22-000043&version=1) (v1) | The Bondy–Simonovits even cycle theorem | 2026-10-22 | [jtraverso/bondy-simonovits @ a4ca4b2](https://github.com/jtraverso/bondy-simonovits/tree/a4ca4b28a0d82735316fd73a5a11303231109fc7) | [PalomarArchive](https://github.com/PalomarArchive/jtraverso--bondy-simonovits--28aa00457e93/tree/palomar/PALOMAR-2026-10-22-000043-v1/a4ca4b28a0d82735316fd73a5a11303231109fc7) |
| [PALOMAR-2026-10-23-000006](https://palomar-registry.org/entry.html?id=PALOMAR-2026-10-23-000006&version=1) (v1) | The Graham–Pollak theorem | 2026-10-23 | [jtraverso/graham-pollak @ 68d32f0](https://github.com/jtraverso/graham-pollak/tree/68d32f0faf102fc1716ac89ffc861eefe897e749) | [PalomarArchive](https://github.com/PalomarArchive/jtraverso--graham-pollak--3485c9d9d4a5/tree/palomar/PALOMAR-2026-10-23-000006-v1/68d32f0faf102fc1716ac89ffc861eefe897e749) |
| [PALOMAR-2026-10-23-000013](https://palomar-registry.org/entry.html?id=PALOMAR-2026-10-23-000013&version=1) (v1) | Robust absorption for typed triangles (Triangle decompositions II) | 2026-10-23 | [jtraverso/typed-triangle-absorption @ 673c6d4](https://github.com/jtraverso/typed-triangle-absorption/tree/673c6d4118b5679783bafa7606fd2c611161a254) | [PalomarArchive](https://github.com/PalomarArchive/jtraverso--typed-triangle-absorption--055c1b37404f/tree/palomar/PALOMAR-2026-10-23-000013-v1/673c6d4118b5679783bafa7606fd2c611161a254) |
| [PALOMAR-2026-10-23-000016](https://palomar-registry.org/entry.html?id=PALOMAR-2026-10-23-000016&version=1) (v1) | Mader's theorem on highly connected subgraphs | 2026-10-23 | [jtraverso/mader-connectivity @ b471abc](https://github.com/jtraverso/mader-connectivity/tree/b471abcdfbb303aabc1af26f4531e080729bb469) | [PalomarArchive](https://github.com/PalomarArchive/jtraverso--mader-connectivity--54c8125a286e/tree/palomar/PALOMAR-2026-10-23-000016-v1/b471abcdfbb303aabc1af26f4531e080729bb469) |
| [PALOMAR-2026-10-26-000001](https://palomar-registry.org/entry.html?id=PALOMAR-2026-10-26-000001&version=1) (v1) | Regular subgraphs of almost regular graphs (Alon–Friedland–Kalai) | 2026-10-26 | [jtraverso/regular-subgraphs @ daea9b3](https://github.com/jtraverso/regular-subgraphs/tree/daea9b30d10bfae6c75ba7be5904080119bbbdba) | [PalomarArchive](https://github.com/PalomarArchive/jtraverso--regular-subgraphs--8e423f4bda53/tree/palomar/PALOMAR-2026-10-26-000001-v1/daea9b30d10bfae6c75ba7be5904080119bbbdba) |
| [PALOMAR-2026-10-28-000001](https://palomar-registry.org/entry.html?id=PALOMAR-2026-10-28-000001&version=1) (v1) | The Hilton–Milner theorem | 2026-10-28 | [jtraverso/hilton-milner @ 6059a0d](https://github.com/jtraverso/hilton-milner/tree/6059a0d6f13378b9a92fba297f2d774598ee0f7d) | [PalomarArchive](https://github.com/PalomarArchive/jtraverso--hilton-milner--c43d1f8a75cc/tree/palomar/PALOMAR-2026-10-28-000001-v1/6059a0d6f13378b9a92fba297f2d774598ee0f7d) |
| [PALOMAR-2026-10-28-000003](https://palomar-registry.org/entry.html?id=PALOMAR-2026-10-28-000003&version=1) (v1) | Kirkman's theorem on Steiner triple systems | 2026-10-28 | [jtraverso/kirkman-steiner-triple-systems @ 1855141](https://github.com/jtraverso/kirkman-steiner-triple-systems/tree/18551414d822f7fa4fb7535dc43733c4b316c3a8) | [PalomarArchive](https://github.com/PalomarArchive/jtraverso--kirkman-steiner-triple-systems--37adc3898c80/tree/palomar/PALOMAR-2026-10-28-000003-v1/18551414d822f7fa4fb7535dc43733c4b316c3a8) |
| [PALOMAR-2026-10-28-000004](https://palomar-registry.org/entry.html?id=PALOMAR-2026-10-28-000004&version=1) (v1) | Nash-Williams' weak orientation theorem | 2026-10-28 | [jtraverso/nash-williams-orientation @ 3412d88](https://github.com/jtraverso/nash-williams-orientation/tree/3412d885cf3ba6680770cb8014df96af8fa3d042) | [PalomarArchive](https://github.com/PalomarArchive/jtraverso--nash-williams-orientation--96d643fb4df4/tree/palomar/PALOMAR-2026-10-28-000004-v1/3412d885cf3ba6680770cb8014df96af8fa3d042) |
| [PALOMAR-2026-10-28-000005](https://palomar-registry.org/entry.html?id=PALOMAR-2026-10-28-000005&version=1) (v1) | Edmonds cardinality matroid intersection | 2026-10-28 | [jtraverso/edmonds-matroid-intersection @ 824e019](https://github.com/jtraverso/edmonds-matroid-intersection/tree/824e019d4c845e8d0ebd8638fd94f19040115cbd) | [PalomarArchive](https://github.com/PalomarArchive/jtraverso--edmonds-matroid-intersection--3c509773d989/tree/palomar/PALOMAR-2026-10-28-000005-v1/824e019d4c845e8d0ebd8638fd94f19040115cbd) |
| [PALOMAR-2026-10-28-000009](https://palomar-registry.org/entry.html?id=PALOMAR-2026-10-28-000009&version=1) (v1) | Stanley's acyclic orientations and chromatic reciprocity | 2026-10-28 | [jtraverso/stanley @ 48d36cb](https://github.com/jtraverso/stanley/tree/48d36cbaa54d14443f99b57776ce65f1f31c8331) | [PalomarArchive](https://github.com/PalomarArchive/jtraverso--stanley--df253fa631b4/tree/palomar/PALOMAR-2026-10-28-000009-v1/48d36cbaa54d14443f99b57776ce65f1f31c8331) |
| [PALOMAR-2026-10-28-000010](https://palomar-registry.org/entry.html?id=PALOMAR-2026-10-28-000010&version=1) (v1) | Edmonds' perfect matching polytope and matching polytope | 2026-10-28 | [jtraverso/edmonds-matching-polytope @ 6198b83](https://github.com/jtraverso/edmonds-matching-polytope/tree/6198b8314ac88a5638120fcf15d5b58c024caaab) | [PalomarArchive](https://github.com/PalomarArchive/jtraverso--edmonds-matching-polytope--a32c69454bfc/tree/palomar/PALOMAR-2026-10-28-000010-v1/6198b8314ac88a5638120fcf15d5b58c024caaab) |
| [PALOMAR-2026-10-28-000012](https://palomar-registry.org/entry.html?id=PALOMAR-2026-10-28-000012&version=1) (v1) | Ray-Chaudhuri–Wilson: uniform families with restricted intersections | 2026-10-28 | [jtraverso/restricted-intersections @ ebb9080](https://github.com/jtraverso/restricted-intersections/tree/ebb90800eda4ec83cc18c6da2135b8718757f6e2) | [PalomarArchive](https://github.com/PalomarArchive/jtraverso--restricted-intersections--ad53241811dd/tree/palomar/PALOMAR-2026-10-28-000012-v1/ebb90800eda4ec83cc18c6da2135b8718757f6e2) |
| [PALOMAR-2026-10-28-000018](https://palomar-registry.org/entry.html?id=PALOMAR-2026-10-28-000018&version=1) (v1) | The Pippenger–Spencer theorem on the chromatic index of hypergraphs | 2026-10-28 | [jtraverso/pippenger-spencer @ 4cca4e3](https://github.com/jtraverso/pippenger-spencer/tree/4cca4e3c641619b1622ea60f58c57dc0c28ffdbb) | [PalomarArchive](https://github.com/PalomarArchive/jtraverso--pippenger-spencer--aaba98952e76/tree/palomar/PALOMAR-2026-10-28-000018-v1/4cca4e3c641619b1622ea60f58c57dc0c28ffdbb) |
| [PALOMAR-2026-10-28-000023](https://palomar-registry.org/entry.html?id=PALOMAR-2026-10-28-000023&version=1) (v1) | Thomassen: planar graphs of girth at least five are 3-choosable | 2026-10-28 | [jtraverso/thomassen-girth-five @ 12765f3](https://github.com/jtraverso/thomassen-girth-five/tree/12765f3362b48fbae04ac467d33873a4f2234083) | [PalomarArchive](https://github.com/PalomarArchive/jtraverso--thomassen-girth-five--a221bbfeb126/tree/palomar/PALOMAR-2026-10-28-000023-v1/12765f3362b48fbae04ac467d33873a4f2234083) |
| [PALOMAR-2026-10-28-000021](https://palomar-registry.org/entry.html?id=PALOMAR-2026-10-28-000021&version=1) (v1) | Hamiltonicity and connectivity thresholds of the random graph G(n, p) | 2026-10-28 | [jtraverso/random-graph-thresholds @ 86325fa](https://github.com/jtraverso/random-graph-thresholds/tree/86325faff71fb76c0769963525b69095fa0a6241) | [PalomarArchive](https://github.com/PalomarArchive/jtraverso--random-graph-thresholds--8101b919ee82/tree/palomar/PALOMAR-2026-10-28-000021-v1/86325faff71fb76c0769963525b69095fa0a6241) |
| [PALOMAR-2026-10-28-000022](https://palomar-registry.org/entry.html?id=PALOMAR-2026-10-28-000022&version=1) (v1) | Nowhere-zero 3-flows in 6-edge-connected graphs | 2026-10-28 | [jtraverso/three-flows @ 2e0bc7c](https://github.com/jtraverso/three-flows/tree/2e0bc7c111b2e6d05d81ce9bd1c2dc58a4184f4c) | [PalomarArchive](https://github.com/PalomarArchive/jtraverso--three-flows--4989d8f20572/tree/palomar/PALOMAR-2026-10-28-000022-v1/2e0bc7c111b2e6d05d81ce9bd1c2dc58a4184f4c) |
| [PALOMAR-2026-10-28-000028](https://palomar-registry.org/entry.html?id=PALOMAR-2026-10-28-000028&version=2) (v2) | Affine profile reduction for fractional triangle packings in split graphs | 2026-10-28, v2 2026-10-29 | [jtraverso/erdos81-fractional-split-profiles @ f8690bc](https://github.com/jtraverso/erdos81-fractional-split-profiles/tree/f8690bcba57bddc5deefd8626f5b07e0d63e6086) | [PalomarArchive](https://github.com/PalomarArchive/jtraverso--erdos81-fractional-split-profiles--2f8b880d7704/tree/palomar/PALOMAR-2026-10-28-000028-v2/f8690bcba57bddc5deefd8626f5b07e0d63e6086) |
| [PALOMAR-2026-10-29-000004](https://palomar-registry.org/entry.html?id=PALOMAR-2026-10-29-000004&version=1) (v1) | Complete-split extremizers for the fractional triangle-cover deficit on chordal graphs | 2026-10-29 | [jtraverso/erdos81-complete-split-extremizers @ 7961c3a](https://github.com/jtraverso/erdos81-complete-split-extremizers/tree/7961c3aba6062b03de3df28f42d339c1aec145d8) | [PalomarArchive](https://github.com/PalomarArchive/jtraverso--erdos81-complete-split-extremizers--398c83aea952/tree/palomar/PALOMAR-2026-10-29-000004-v1/7961c3aba6062b03de3df28f42d339c1aec145d8) |
| [PALOMAR-2026-10-29-000006](https://palomar-registry.org/entry.html?id=PALOMAR-2026-10-29-000006&version=1) (v1) | Linear-error clique partitions of split graphs | 2026-10-29 | [jtraverso/erdos81-split-clique-partitions @ a98dfa4](https://github.com/jtraverso/erdos81-split-clique-partitions/tree/a98dfa413428b3c532174575a39f89eb32b268b8) | [PalomarArchive](https://github.com/PalomarArchive/jtraverso--erdos81-split-clique-partitions--91b4db9f18d8/tree/palomar/PALOMAR-2026-10-29-000006-v1/a98dfa413428b3c532174575a39f89eb32b268b8) |
| [PALOMAR-2026-10-29-000005](https://palomar-registry.org/entry.html?id=PALOMAR-2026-10-29-000005&version=1) (v1) | Formalizing Delcourt–Postle’s refined absorption in Lean | 2026-10-29 | [jtraverso/refined-absorption-lean @ 5bfe5c7](https://github.com/jtraverso/refined-absorption-lean/tree/5bfe5c7346a7b245581152dccebe363e22f072b6) | [PalomarArchive](https://github.com/PalomarArchive/jtraverso--refined-absorption-lean--6accc6d51192/tree/palomar/PALOMAR-2026-10-29-000005-v1/5bfe5c7346a7b245581152dccebe363e22f072b6) |
| [PALOMAR-2026-10-29-000007](https://palomar-registry.org/entry.html?id=PALOMAR-2026-10-29-000007&version=1) (v1) | The Corrádi–Hajnal theorem on vertex-disjoint cycles | 2026-10-29 | [jtraverso/corradi-hajnal @ 2b85adc](https://github.com/jtraverso/corradi-hajnal/tree/2b85adcc37a9a057fb0cb72bc08774027f9ea077) | [PalomarArchive](https://github.com/PalomarArchive/jtraverso--corradi-hajnal--20f84b4c2e6d/tree/palomar/PALOMAR-2026-10-29-000007-v1/2b85adcc37a9a057fb0cb72bc08774027f9ea077) |
| [PALOMAR-2026-10-29-000008](https://palomar-registry.org/entry.html?id=PALOMAR-2026-10-29-000008&version=1) (v1) | The Moser–Tardos theorem (algorithmic Lovász Local Lemma) | 2026-10-29 | [jtraverso/moser-tardos @ 5a3024a](https://github.com/jtraverso/moser-tardos/tree/5a3024a6d3eb442ac6925f9b3660b93c36cfb8b4) | [PalomarArchive](https://github.com/PalomarArchive/jtraverso--moser-tardos--5ec56ed9b1a0/tree/palomar/PALOMAR-2026-10-29-000008-v1/5a3024a6d3eb442ac6925f9b3660b93c36cfb8b4) |
| [PALOMAR-2026-10-29-000023](https://palomar-registry.org/entry.html?id=PALOMAR-2026-10-29-000023&version=1) (v1) | Shannon's theorem on edge colourings of multigraphs | 2026-10-29 | [jtraverso/shannon-edge-colouring @ d590cfe](https://github.com/jtraverso/shannon-edge-colouring/tree/d590cfeb50d88710b454905f896aab928fcb5156) | [PalomarArchive](https://github.com/PalomarArchive/jtraverso--shannon-edge-colouring--7112faf48c4d/tree/palomar/PALOMAR-2026-10-29-000023-v1/d590cfeb50d88710b454905f896aab928fcb5156) |
| [PALOMAR-2026-10-30-000008](https://palomar-registry.org/entry.html?id=PALOMAR-2026-10-30-000008&version=1) (v1) | Fractional triangle decompositions of dense tripartite graphs | 2026-10-30 | [jtraverso/fractional-triangle-decompositions-tripartite @ d233113](https://github.com/jtraverso/fractional-triangle-decompositions-tripartite/tree/d2331132eac8b9c9c1891ba14162745d567ebfdb) | [PalomarArchive](https://github.com/PalomarArchive/jtraverso--fractional-triangle-decompositions-tripartite--1b438fcdd323/tree/palomar/PALOMAR-2026-10-30-000008-v1/d2331132eac8b9c9c1891ba14162745d567ebfdb) |

## Notes

* All entries are checked by Palomar's mechanical verification (Lean kernel and the independent
  nanoda checker); the proofs use only the axioms `propext`, `Classical.choice` and
  `Quot.sound`.
* The formalizations were written with AI assistance (Claude Code and Harmonic's Aristotle) under
  the author's direction; each entry's `formalization.yaml` describes the process.

## arXiv endorsement

Some of these formalizations grew out of my work on Erdős Problem #81, whose preprint series
([erdos-81-chordal-clique-partitions](https://github.com/jtraverso/erdos-81-chordal-clique-partitions))
I am preparing to submit to arXiv (math.CO); the others are independent formalizations of classical
and recent results in graph theory and combinatorics. If you are an arXiv author eligible to endorse
in math.CO and found this work valuable, you can endorse me at https://arxiv.org/auth/endorse?x=N8V4R6 (code `N8V4R6`). An
endorsement only confirms that the work is appropriate for the subject area; it is not a review of
the results. Thank you.

*En español:* algunas de estas formalizaciones surgieron de mi trabajo sobre el problema #81 de
Erdős, cuya serie de preprints preparo para enviar a arXiv (math.CO); las demás son formalizaciones
independientes de resultados clásicos y recientes de teoría de grafos y combinatoria. Si eres autor de arXiv habilitado para dar endorsement
en math.CO y este trabajo te pareció valioso, puedes dármelo en https://arxiv.org/auth/endorse?x=N8V4R6 (código `N8V4R6`). El
endorsement solo confirma que el trabajo es adecuado para el área; no es una revisión de los
resultados. ¡Gracias!
