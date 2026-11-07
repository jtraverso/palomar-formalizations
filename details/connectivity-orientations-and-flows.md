# Connectivity, orientations and flows: details

[← Back to the list](../README.md)

## Menger's theorem, Hamiltonian cycles, long cycles and pancyclicity

Palomar: [PALOMAR-2026-10-15-000020](https://palomar-registry.org/entry.html?id=PALOMAR-2026-10-15-000020&version=2) (version 2) · code: [jtraverso/menger-hamiltonian @ 35c5f68](https://github.com/jtraverso/menger-hamiltonian/tree/35c5f684f9bfbd244bd0999ce725623ab571adb6) · [archived copy](https://github.com/PalomarArchive/jtraverso--menger-hamiltonian--0fd5dfe41e84/tree/palomar/PALOMAR-2026-10-15-000020-v2/35c5f684f9bfbd244bd0999ce725623ab571adb6)

**What is proved.** A Lean 4 / Mathlib formalization of Menger's theorem for finite graphs (set form with a minimum separator and as many vertex-disjoint paths, two-vertex form, edge form for Mathlib's IsEdgeReachable, and the global edge form for Mathlib's IsEdgeConnected) and of classical sufficient conditions for Hamiltonian cycles: the Bondy–Chvátal closure step, Ore's and Dirac's theorems, and the Chvátal–Erdős theorem (k-connected with independence number at most k implies Hamiltonian), whose proof uses Menger's theorem through the fan lemma. Version 2 adds the Erdős–Gallai theorems on long paths and cycles (no path on k vertices implies 2e ≤ (k − 2)n; no cycle of length at least k ≥ 3 implies 2e ≤ (k − 1)(n − 1)) and Bondy's pancyclicity theorem (a Hamiltonian graph with at least n²/4 edges is pancyclic or is K_{n/2,n/2}), proved on top of the same library.

**Sources.**

* Karl Menger, *Zur allgemeinen Kurventheorie*, Fundamenta Mathematicae 10 (1927), 96–115. [doi:10.4064/fm-10-1-96-115](https://doi.org/10.4064/fm-10-1-96-115) · [free full text](https://www.impan.pl/shop/publication/transaction/download/product/92646?download.pdf)
* G. A. Dirac, *Some theorems on abstract graphs*, Proceedings of the London Mathematical Society (3) 2 (1952), 69–81. [doi:10.1112/plms/s3-2.1.69](https://doi.org/10.1112/plms/s3-2.1.69)
* Øystein Ore, *Note on Hamilton circuits*, American Mathematical Monthly 67 (1960), 55. [doi:10.2307/2308928](https://doi.org/10.2307/2308928)
* J. A. Bondy, V. Chvátal, *A method in graph theory*, Discrete Mathematics 15 (1976), 111–135. [doi:10.1016/0012-365X(76)90078-9](https://doi.org/10.1016/0012-365X(76)90078-9) · [free full text](https://doi.org/10.1016/0012-365x(76)90078-9)
* V. Chvátal, P. Erdős, *A note on Hamiltonian circuits*, Discrete Mathematics 2 (1972), 111–113. [doi:10.1016/0012-365X(72)90079-9](https://doi.org/10.1016/0012-365X(72)90079-9) · [free full text](https://doi.org/10.1016/0012-365x(72)90079-9)
* P. Erdős, T. Gallai, *On maximal paths and circuits of graphs*, Acta Mathematica Academiae Scientiarum Hungaricae 10 (1959), 337–356. [doi:10.1007/BF02024498](https://doi.org/10.1007/BF02024498)
* J. A. Bondy, *Pancyclic graphs I*, Journal of Combinatorial Theory, Series B 11 (1971), 80–84. [doi:10.1016/0095-8956(71)90016-5](https://doi.org/10.1016/0095-8956(71)90016-5) · [free full text](https://www.sciencedirect.com/science/article/pii/0095895671900165/pdf)

<details><summary>Background references</summary>

* Reinhard Diestel, *Graph Theory (5th edition)*, Graduate Texts in Mathematics 173, Springer (2017). [doi:10.1007/978-3-662-53622-3](https://doi.org/10.1007/978-3-662-53622-3)

</details>

## Mader's theorem on highly connected subgraphs

Palomar: [PALOMAR-2026-10-23-000016](https://palomar-registry.org/entry.html?id=PALOMAR-2026-10-23-000016&version=1) (version 1) · code: [jtraverso/mader-connectivity @ b471abc](https://github.com/jtraverso/mader-connectivity/tree/b471abcdfbb303aabc1af26f4531e080729bb469) · [archived copy](https://github.com/PalomarArchive/jtraverso--mader-connectivity--54c8125a286e/tree/palomar/PALOMAR-2026-10-23-000016-v1/b471abcdfbb303aabc1af26f4531e080729bb469)

**What is proved.** A Lean 4 / Mathlib formalization of Mader's 1972 theorem in the form of Diestel's Theorem 1.4.3: for k ≥ 1, every nonempty finite simple graph with average degree at least 4k has a (k + 1)-connected induced subgraph H with e(H)/|H| > e(G)/|G| − k. Vertex connectivity is defined by deletion of fewer than k vertices (same definition as in the Menger–Hamiltonicity entry). Mathlib does not contain vertex connectivity or this theorem.

**Sources.**

* W. Mader, *Existenz n-fach zusammenhängender Teilgraphen in Graphen genügend großer Kantendichte*, Abhandlungen aus dem Mathematischen Seminar der Universität Hamburg 37 (1972), 86–97. [doi:10.1007/BF02993903](https://doi.org/10.1007/BF02993903)
* R. Diestel, *Graph Theory*, Graduate Texts in Mathematics 173, Springer, Theorem 1.4.3.

## Robbins' theorem on strongly connected orientations

Palomar: [PALOMAR-2026-10-18-000022](https://palomar-registry.org/entry.html?id=PALOMAR-2026-10-18-000022&version=1) (version 1) · code: [jtraverso/robbins-strong-orientation @ 076e734](https://github.com/jtraverso/robbins-strong-orientation/tree/076e734e9949720d3e4fcc2cc3cad4284871442c) · [archived copy](https://github.com/PalomarArchive/jtraverso--robbins-strong-orientation--f05c2621ca9e/tree/palomar/PALOMAR-2026-10-18-000022-v1/076e734e9949720d3e4fcc2cc3cad4284871442c)

**What is proved.** A Lean 4 / Mathlib formalization of Robbins' theorem: a finite connected simple graph has a strongly connected orientation (a digraph with underlying graph G, never containing both u → v and v → u, in which every vertex reaches every other) if and only if no edge of it is a bridge. As a corollary, every finite 2-edge-connected graph on a nonempty vertex type has a strongly connected orientation. Mathlib has bridges, edge connectivity and digraphs, but not this theorem.

**Sources.**

* H. E. Robbins, *A Theorem on Graphs, with an Application to a Problem of Traffic Control*, The American Mathematical Monthly 46 (1939), 281–283. [doi:10.2307/2303897](https://doi.org/10.2307/2303897)

## Nash-Williams' weak orientation theorem

Palomar: [PALOMAR-2026-10-28-000004](https://palomar-registry.org/entry.html?id=PALOMAR-2026-10-28-000004&version=1) (version 1) · code: [jtraverso/nash-williams-orientation @ 3412d88](https://github.com/jtraverso/nash-williams-orientation/tree/3412d885cf3ba6680770cb8014df96af8fa3d042) · [archived copy](https://github.com/PalomarArchive/jtraverso--nash-williams-orientation--96d643fb4df4/tree/palomar/PALOMAR-2026-10-28-000004-v1/3412d885cf3ba6680770cb8014df96af8fa3d042)

**What is proved.** A Lean 4 / Mathlib formalization of Nash-Williams' weak orientation theorem (1960): every 2k-edge-connected finite graph has a k-arc-connected orientation, i.e. one in which every nonempty proper vertex set is left by at least k arcs. It is proved for finite loopless multigraphs given by an edge family, and stated for simple graphs with Mathlib's SimpleGraph.IsEdgeConnected and orientations as Mathlib Digraphs. The proof is by induction on the number of edges, with Mader's lemma (a minimally 2k-edge-connected multigraph has a vertex of degree 2k) and Lovász's splitting lemma, both proved in the project. Mathlib does not contain these results.

**Sources.**

* C. St. J. A. Nash-Williams, *On Orientations, Connectivity and Odd-Vertex-Pairings in Finite Graphs*, Canadian Journal of Mathematics 12 (1960), 555–567. [doi:10.4153/CJM-1960-049-6](https://doi.org/10.4153/CJM-1960-049-6) · [free full text](https://www.cambridge.org/core/services/aop-cambridge-core/content/view/2B39912D1666161E4200E61E8F65DE2B/S0008414X00010191a.pdf/div-class-title-on-orientations-connectivity-and-odd-vertex-pairings-in-finite-graphs-div.pdf)

<details><summary>Background references</summary>

* L. Lovász, *On some connectivity properties of Eulerian graphs*, Acta Mathematica Academiae Scientiarum Hungaricae 28 (1976), 129–138. [doi:10.1007/BF01902503](https://doi.org/10.1007/BF01902503)
* W. Mader, *A Reduction Method for Edge-Connectivity in Graphs*, Annals of Discrete Mathematics 3 (1978), 145–164. [doi:10.1016/S0167-5060(08)70504-1](https://doi.org/10.1016/S0167-5060(08)70504-1)

</details>

## Jaeger's 4-flow and 8-flow theorems and Seymour's 6-flow theorem

Palomar: [PALOMAR-2026-10-18-000009](https://palomar-registry.org/entry.html?id=PALOMAR-2026-10-18-000009&version=3) (version 3) · code: [jtraverso/jaeger-four-flow @ 623dd0d](https://github.com/jtraverso/jaeger-four-flow/tree/623dd0dd718f93de06d4dc792e116dd32ef97553) · [archived copy](https://github.com/PalomarArchive/jtraverso--jaeger-four-flow--4443e53b8984/tree/palomar/PALOMAR-2026-10-18-000009-v3/623dd0dd718f93de06d4dc792e116dd32ef97553)

**What is proved.** A Lean 4 / Mathlib formalization of Jaeger's 4-flow theorem: every finite 4-edge-connected simple graph has a nowhere-zero integer 4-flow, i.e. an antisymmetric function on darts with values in {±1, ±2, ±3} that is conserved at every vertex. Also proved: a graph with two edge-disjoint spanning trees has its edges covered by two even subgraphs (a nowhere-zero ℤ₂ × ℤ₂-flow) and has a nowhere-zero integer 4-flow. Version 2 adds Jaeger's 8-flow theorem: every finite bridgeless graph has its edges covered by three even subgraphs and has a nowhere-zero integer 8-flow; conversely a graph with a nowhere-zero flow has no bridge. Version 3 adds Seymour's 6-flow theorem (every finite bridgeless graph has a nowhere-zero integer 6-flow) and Tutte's theorem relating group and integer flows (for k > 0, every nowhere-zero ℤ/k-flow φ lifts to a nowhere-zero integer k-flow ψ with ψ ≡ φ mod k, and conversely an integer k-flow reduces modulo k to a nowhere-zero ℤ/k-flow). Mathlib has no flows.

**Sources.**

* F. Jaeger, *Flows and generalized coloring theorems in graphs*, Journal of Combinatorial Theory, Series B 26 (1979), 205–216. [doi:10.1016/0095-8956(79)90057-1](https://doi.org/10.1016/0095-8956(79)90057-1) · [free full text](https://doi.org/10.1016/0095-8956(79)90057-1)
* P. D. Seymour, *Nowhere-zero 6-flows*, Journal of Combinatorial Theory, Series B 30 (1981), 130–135. [doi:10.1016/0095-8956(81)90058-7](https://doi.org/10.1016/0095-8956(81)90058-7) · [free full text](https://www.sciencedirect.com/science/article/pii/0095895681900587/pdf)
* W. T. Tutte, *A contribution to the theory of chromatic polynomials*, Canadian Journal of Mathematics 6 (1954), 80–91. [doi:10.4153/CJM-1954-010-9](https://doi.org/10.4153/CJM-1954-010-9) · [free full text](https://www.cambridge.org/core/services/aop-cambridge-core/content/view/E1EE1F053B494D08746F0EE23F736CC2/S0008414X00023543a.pdf/div-class-title-a-contribution-to-the-theory-of-chromatic-polynomials-div.pdf)

<details><summary>Background references</summary>

* P. A. Kilpatrick, *Tutte's first colour-cycle conjecture*, Ph.D. thesis, University of Cape Town (1975).

</details>

## Nowhere-zero 3-flows in 6-edge-connected graphs

Palomar: [PALOMAR-2026-10-28-000022](https://palomar-registry.org/entry.html?id=PALOMAR-2026-10-28-000022&version=1) (version 1) · code: [jtraverso/three-flows @ 2e0bc7c](https://github.com/jtraverso/three-flows/tree/2e0bc7c111b2e6d05d81ce9bd1c2dc58a4184f4c) · [archived copy](https://github.com/PalomarArchive/jtraverso--three-flows--4989d8f20572/tree/palomar/PALOMAR-2026-10-28-000022-v1/2e0bc7c111b2e6d05d81ce9bd1c2dc58a4184f4c)

**What is proved.** A Lean 4 / Mathlib formalization of the theorem of Lovász, Thomassen, Wu and Zhang: every finite 6-edge-connected simple graph has a nowhere-zero integer 3-flow (the weak 3-flow conjecture). The proof formalizes Theorem 3.1 of the paper (β-orientations of multigraphs modulo 3) and Tutte's lifting theorem. Only simple graphs are stated; the paper's multigraph version and its results on modulo k-orientations for k > 3 are not stated. Mathlib does not contain this theorem.

**Sources.**

* L. M. Lovász, C. Thomassen, Y. Wu, C.-Q. Zhang, *Nowhere-zero 3-flows and modulo k-orientations*, Journal of Combinatorial Theory, Series B 103 (2013), 587–598. [doi:10.1016/j.jctb.2013.06.003](https://doi.org/10.1016/j.jctb.2013.06.003) · [free full text](https://www.sciencedirect.com/science/article/pii/S0095895613000506/pdf)

<details><summary>Background references</summary>

* C. Thomassen, *The weak 3-flow conjecture and the weak circular flow conjecture*, Journal of Combinatorial Theory, Series B 102 (2012), 521–529. [doi:10.1016/j.jctb.2011.09.003](https://doi.org/10.1016/j.jctb.2011.09.003) · [free full text](https://www.sciencedirect.com/science/article/pii/S0095895611000955/pdf)
* W. T. Tutte, *A contribution to the theory of chromatic polynomials*, Canadian Journal of Mathematics 6 (1954), 80–91. [doi:10.4153/CJM-1954-010-9](https://doi.org/10.4153/CJM-1954-010-9) · [free full text](https://www.cambridge.org/core/services/aop-cambridge-core/content/view/E1EE1F053B494D08746F0EE23F736CC2/S0008414X00023543a.pdf/div-class-title-a-contribution-to-the-theory-of-chromatic-polynomials-div.pdf)

</details>

## Gale's feasibility theorem, the Gale–Ryser theorem and Hoffman's circulation theorem

Palomar: [PALOMAR-2026-11-06-000015](https://palomar-registry.org/entry.html?id=PALOMAR-2026-11-06-000015&version=1) (version 1) · code: [jtraverso/gale-hoffman-feasibility @ fa52c29](https://github.com/jtraverso/gale-hoffman-feasibility/tree/fa52c29c24edf7e9afdb487df3764affd43c51c7) · [archived copy](https://github.com/PalomarArchive/jtraverso--gale-hoffman-feasibility--31485ec5ef29/tree/palomar/PALOMAR-2026-11-06-000015-v1/fa52c29c24edf7e9afdb487df3764affd43c51c7)

**What is proved.** A Lean 4 / Mathlib formalization of D. Gale, A theorem on flows in networks (Pacific J. Math. 7, 1957) and of Hoffman's circulation theorem (A. J. Hoffman, 1960, in the form of A. Schrijver, A Course in Combinatorial Optimization, Theorems 4.6 and 4.7). A network is a finite node type N with capacities c : N → N → ℝ, c ≥ 0 (finite capacities only); a flow is f : N → N → ℝ with f x y + f y x = 0 and f ≤ c; a demand d : N → ℝ is feasible if some flow has net inflow ∑_y f y x ≥ d x at every node. feasibility: d is feasible if and only if d(Sᶜ) ≤ c(S, Sᶜ) for every S ⊆ N (Gale's Feasibility Theorem). feasibility_int: the same for integer c and d with an integer flow (Gale's remark). feasibility_second: Gale's second formulation (for every set Y of nodes of positive demand, some flow meets the demand at all nodes of nonpositive demand and the aggregate demand of Y). gale_ryser_unsorted, gale_ryser: for a : Fin m → ℕ and b : Fin n → ℕ, a 0-1 matrix with row sums at most a i and column sums b j exists if and only if ∑_{j∈Y} b j ≤ ∑_i min(a i, |Y|) for all column sets Y, equivalently, for b nonincreasing, ∑_{j<k} b j ≤ ∑_{j<k} #{i | j < a i} for all k ≤ n (Gale's Problem I, §3). gale_ryser_exact: if moreover ∑ a = ∑ b, the row sums can be made exactly a (the Gale–Ryser theorem). hoffman, hoffman_int: on a finite directed multigraph (arc type A, tail and head maps src, tgt : A → V) with bounds d ≤ c on the arcs (real, respectively integer), there is a circulation f (real, respectively integer) with d ≤ f ≤ c if and only if d(δ^in(U)) ≤ c(δ^out(U)) for every U ⊆ V. Eight statements; no definitions beyond Mathlib's.

**Sources.**

* David Gale, *A theorem on flows in networks*, Pacific Journal of Mathematics 7 (1957), 1073–1082; Feasibility Theorem, Remark, second formulation (§2) and the theorem on Problem I (§3). [doi:10.2140/pjm.1957.7.1073](https://doi.org/10.2140/pjm.1957.7.1073) · [free full text](http://msp.org/pjm/1957/7-2/pjm-v7-n2-p04-s.pdf)
* A. J. Hoffman, *Some recent applications of the theory of linear inequalities to extremal combinatorial analysis*, Combinatorial Analysis, Proceedings of Symposia in Applied Mathematics 10, American Mathematical Society (1960), 113–127. [doi:10.1090/psapm/010/0114759](https://doi.org/10.1090/psapm/010/0114759)
* Alexander Schrijver, *A Course in Combinatorial Optimization*, Lecture notes, version of 23 March 2017, https://homepages.cwi.nl/~lex/files/dict.pdf, Section 4.5, Theorems 4.6 and 4.7.

<details><summary>Background references</summary>

* H. J. Ryser, *Combinatorial properties of matrices of zeros and ones*, Canadian Journal of Mathematics 9 (1957), 371–377. [doi:10.4153/CJM-1957-044-3](https://doi.org/10.4153/CJM-1957-044-3) · [free full text](https://www.cambridge.org/core/services/aop-cambridge-core/content/view/4BE766CCFDF1704C196AA182C0C5EC88/S0008414X00044734a.pdf/div-class-title-combinatorial-properties-of-matrices-of-zeros-and-ones-div.pdf)
* L. R. Ford, D. R. Fulkerson, *Maximal flow through a network*, Canadian Journal of Mathematics 8 (1956), 399–404. [doi:10.4153/CJM-1956-045-5](https://doi.org/10.4153/CJM-1956-045-5) · [free full text](https://www.cambridge.org/core/services/aop-cambridge-core/content/view/5D6E55D3B06C4F7B1043BC1D82D40764/S0008414X00036890a.pdf/div-class-title-maximal-flow-through-a-network-div.pdf)

</details>

[← Back to the list](../README.md)
