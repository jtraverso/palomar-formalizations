# Cycles and Hamiltonicity: details

[← Back to the list](../README.md)

## Chvátal's and Pósa's degree conditions for Hamiltonian cycles

Palomar: [PALOMAR-2026-10-18-000001](https://palomar-registry.org/entry.html?id=PALOMAR-2026-10-18-000001&version=1) (version 1) · code: [jtraverso/chvatal-posa-hamiltonian @ 6be0ebd](https://github.com/jtraverso/chvatal-posa-hamiltonian/tree/6be0ebda7b457b85ad400f6d7f92ad156d6e7712) · [archived copy](https://github.com/PalomarArchive/jtraverso--chvatal-posa-hamiltonian--3158a08a16e2/tree/palomar/PALOMAR-2026-10-18-000001-v1/6be0ebda7b457b85ad400f6d7f92ad156d6e7712)

**What is proved.** A Lean 4 / Mathlib formalization of two classical degree-sequence conditions for Hamiltonicity of a finite simple graph on n ≥ 3 vertices with degrees d₁ ≤ ⋯ ≤ dₙ. Chvátal's theorem (1972): if for every i < n/2, dᵢ ≤ i implies d_{n−i} ≥ n − i, then the graph is Hamiltonian (stated without sorting: if at least i vertices have degree at most i, then at least i + 1 vertices have degree at least n − i). Pósa's theorem (1962): if for every k with 1 ≤ k < (n − 1)/2 fewer than k vertices have degree at most k, and, for odd n, at most (n − 1)/2 vertices have degree at most (n − 1)/2, then the graph is Hamiltonian. Mathlib has Hamiltonian cycles but neither theorem.

**Sources.**

* V. Chvátal, *On Hamilton's ideals*, Journal of Combinatorial Theory, Series B 12 (1972), 163–168. [doi:10.1016/0095-8956(72)90020-2](https://doi.org/10.1016/0095-8956(72)90020-2) · [free full text](https://www.sciencedirect.com/science/article/pii/0095895672900202/pdf)
* L. Pósa, *A theorem concerning Hamilton lines*, Magyar Tudományos Akadémia Matematikai Kutató Intézetének Közleményei 7 (1962), 225–226.

<details><summary>Background references</summary>

* J. A. Bondy, V. Chvátal, *A method in graph theory*, Discrete Mathematics 15 (1976), 111–135. [doi:10.1016/0012-365X(76)90078-9](https://doi.org/10.1016/0012-365X(76)90078-9) · [free full text](https://doi.org/10.1016/0012-365x(76)90078-9)

</details>

## Dirac's theorem: k vertices of a k-connected graph lie on a common cycle

Palomar: [PALOMAR-2026-10-18-000011](https://palomar-registry.org/entry.html?id=PALOMAR-2026-10-18-000011&version=1) (version 1) · code: [jtraverso/dirac-common-cycle @ 3c9e996](https://github.com/jtraverso/dirac-common-cycle/tree/3c9e9966662cb99c0e4f11d771011bc904dc627f) · [archived copy](https://github.com/PalomarArchive/jtraverso--dirac-common-cycle--7eeee5978914/tree/palomar/PALOMAR-2026-10-18-000011-v1/3c9e9966662cb99c0e4f11d771011bc904dc627f)

**What is proved.** A Lean 4 / Mathlib formalization of Dirac's 1960 theorem: in a k-connected finite simple graph with k ≥ 2 (more than k vertices, and connected after deleting any set of fewer than k vertices), any set of at most k vertices lies on a common cycle. In particular, in a 2-connected finite graph any two vertices lie on a common cycle. Cycles are Mathlib's `SimpleGraph.Walk.IsCycle`. Mathlib does not have this theorem.

**Sources.**

* G. A. Dirac, *In abstrakten Graphen vorhandene vollständige 4-Graphen und ihre Unterteilungen*, Mathematische Nachrichten 22 (1960), 61–85. [doi:10.1002/mana.19600220107](https://doi.org/10.1002/mana.19600220107)

## The Erdős–Pósa theorem for cycles

Palomar: [PALOMAR-2026-10-20-000003](https://palomar-registry.org/entry.html?id=PALOMAR-2026-10-20-000003&version=1) (version 1) · code: [jtraverso/erdos-posa-cycles @ 67bfea6](https://github.com/jtraverso/erdos-posa-cycles/tree/67bfea6b3893ffdf57e76cd83c9c3538647bdec8) · [archived copy](https://github.com/PalomarArchive/jtraverso--erdos-posa-cycles--495ed139acca/tree/palomar/PALOMAR-2026-10-20-000003-v1/67bfea6b3893ffdf57e76cd83c9c3538647bdec8)

**What is proved.** A Lean 4 / Mathlib formalization of the Erdős–Pósa theorem: for every k, every finite simple graph either contains k vertex-disjoint cycles or has a set of at most c (k + 1)(log₂(k + 1) + 1) vertices meeting every cycle, for a fixed constant c (the proof gives c = 65); together with the qualitative Erdős–Pósa property and the easy converse that a feedback vertex set of size s rules out s + 1 disjoint cycles. Mathlib has acyclic graphs but not this theorem.

**Sources.**

* P. Erdős, L. Pósa, *On independent circuits contained in a graph*, Canadian Journal of Mathematics 17 (1965), 347–352. [doi:10.4153/CJM-1965-035-8](https://doi.org/10.4153/CJM-1965-035-8) · [free full text](https://www.cambridge.org/core/services/aop-cambridge-core/content/view/00E165DD4E460BE00867629661177985/S0008414X00039316a.pdf/div-class-title-on-independent-circuits-contained-in-a-graph-div.pdf)

<details><summary>Background references</summary>

* M. Simonovits, *A new proof and generalizations of a theorem of Erdős and Pósa on graphs without k+1 independent circuits*, Acta Mathematica Academiae Scientiarum Hungaricae 18 (1967), 191–206. [doi:10.1007/BF02020974](https://doi.org/10.1007/BF02020974)
* Reinhard Diestel, *Graph Theory (5th edition)*, Graduate Texts in Mathematics 173, Springer (2017), Section 2.3. [doi:10.1007/978-3-662-53622-3](https://doi.org/10.1007/978-3-662-53622-3)

</details>

## The Corrádi–Hajnal theorem on vertex-disjoint cycles

Palomar: [PALOMAR-2026-10-29-000007](https://palomar-registry.org/entry.html?id=PALOMAR-2026-10-29-000007&version=1) (version 1) · code: [jtraverso/corradi-hajnal @ 2b85adc](https://github.com/jtraverso/corradi-hajnal/tree/2b85adcc37a9a057fb0cb72bc08774027f9ea077) · [archived copy](https://github.com/PalomarArchive/jtraverso--corradi-hajnal--20f84b4c2e6d/tree/palomar/PALOMAR-2026-10-29-000007-v1/2b85adcc37a9a057fb0cb72bc08774027f9ea077)

**What is proved.** A Lean 4 / Mathlib formalization of the Corrádi–Hajnal theorem (1963): every finite simple graph on at least 3k vertices with minimum degree at least 2k contains k vertex-disjoint cycles. Cycles are closed walks that are cycles in Mathlib's sense; the theorem is also stated with the definition of disjoint cycles of the registered Erdős–Pósa entry (k pairwise disjoint vertex sets, each inducing a subgraph that is not acyclic). Both hypotheses are shown to be needed: for k ≥ 2 the complete graph on 3k − 1 vertices has minimum degree 3k − 2 ≥ 2k and no k disjoint cycles, and for m ≥ 2k the complete bipartite graph K_{2k−1, m} has at least 3k vertices and minimum degree 2k − 1 and no k disjoint cycles. Mathlib has cycles and minimum degree but not this theorem.

**Sources.**

* K. Corrádi, A. Hajnal, *On the maximal number of independent circuits in a graph*, Acta Mathematica Academiae Scientiarum Hungaricae 14 (1963), 423–439. [doi:10.1007/BF01895727](https://doi.org/10.1007/BF01895727)

[← Back to the list](../README.md)
