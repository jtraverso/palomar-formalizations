# Extremal graph theory and Ramsey theory: details

[← Back to the list](../README.md)

## Classical bounds for graph Ramsey numbers

Palomar: [PALOMAR-2026-10-15-000021](https://palomar-registry.org/entry.html?id=PALOMAR-2026-10-15-000021&version=1) (version 1) · code: [jtraverso/ramsey-graph-bounds @ 562986a](https://github.com/jtraverso/ramsey-graph-bounds/tree/562986a7ce9edf086c20b3a2b8c7d5ace2ffd843) · [archived copy](https://github.com/PalomarArchive/jtraverso--ramsey-graph-bounds--d35ec49e7ff6/tree/palomar/PALOMAR-2026-10-15-000021-v1/562986a7ce9edf086c20b3a2b8c7d5ace2ffd843)

**What is proved.** A Lean 4 / Mathlib formalization of the classical bounds for graph Ramsey numbers: R(3, 3) = 6 (every graph on six vertices has a triangle or three independent vertices, and the pentagon has neither), the Erdős–Szekeres upper bound R(s, t) ≤ C(s + t − 2, s − 1), and Erdős's lower bound R(k, k) > 2^(k/2) for k ≥ 3, proved by a union bound over the edge sets of graphs on n vertices.

**Sources.**

* Paul Erdős, George Szekeres, *A combinatorial problem in geometry*, Compositio Mathematica 2 (1935), 463–470.
* Paul Erdős, *Some remarks on the theory of graphs*, Bulletin of the American Mathematical Society 53 (1947), 292–294. [doi:10.1090/S0002-9904-1947-08785-1](https://doi.org/10.1090/S0002-9904-1947-08785-1) · [free full text](https://www.ams.org/bull/1947-53-04/S0002-9904-1947-08785-1/S0002-9904-1947-08785-1.pdf)
* R. E. Greenwood, A. M. Gleason, *Combinatorial relations and chromatic graphs*, Canadian Journal of Mathematics 7 (1955), 1–7. [doi:10.4153/CJM-1955-001-4](https://doi.org/10.4153/CJM-1955-001-4) · [free full text](https://www.cambridge.org/core/services/aop-cambridge-core/content/view/BF0DEBC881488344266BCD77CBBCD86B/S0008414X00030091a.pdf/div-class-title-combinatorial-relations-and-chromatic-graphs-div.pdf)

## Füredi's stability theorem and the Erdős–Simonovits stability theorem

Palomar: [PALOMAR-2026-10-16-000024](https://palomar-registry.org/entry.html?id=PALOMAR-2026-10-16-000024&version=1) (version 1) · code: [jtraverso/turan-stability @ 3eb9903](https://github.com/jtraverso/turan-stability/tree/3eb99033cc931add291781f77b7446dcba8f5f9d) · [archived copy](https://github.com/PalomarArchive/jtraverso--turan-stability--e49ed8b57e3c/tree/palomar/PALOMAR-2026-10-16-000024-v1/3eb99033cc931add291781f77b7446dcba8f5f9d)

**What is proved.** A Lean 4 / Mathlib formalization of the stability theory of Turán's theorem. (1) Füredi's sharp stability theorem for cliques: a K_{p+1}-free graph on n vertices with at least t(n, p) − t edges (t(n, p) the number of edges of the Turán graph) has a p-partite subgraph with at least e(G) − t edges, via Füredi's partition inequality e(G) + Σᵢ e(G[Vᵢ]) ≤ e(K(V₁, …, V_p)); also edit distance at most 3t to a complete p-partite graph. (2) The Erdős–Simonovits stability theorem for every forbidden graph L with χ(L) ≤ p + 1: for every ε > 0 there are δ > 0 and n₀ such that every L-free graph on n ≥ n₀ vertices with at least (1 − 1/p) n²/2 − δn² edges differs from a complete p-partite graph in at most εn² edges, derived as in Füredi's paper from the regularity method. For this, the project extends Mathlib's regularity theory, which only treats triangles, with (3) the clique counting lemma in ε-uniform parts, (4) the clique removal lemma (fewer than δn^r copies of K_r can be destroyed by deleting fewer than εn² edges) and (5) the embedding lemma for any fixed graph with a proper colouring into pairwise uniform dense parts. Mathlib has Turán's theorem, Szemerédi's regularity lemma and triangle counting/removal, but none of (1)–(5).

**Sources.**

* Zoltán Füredi, *A proof of the stability of extremal graphs, Simonovits' stability from Szemerédi's regularity*, Journal of Combinatorial Theory, Series B 115 (2015), 66–71. [doi:10.1016/j.jctb.2015.05.001](https://doi.org/10.1016/j.jctb.2015.05.001) · [free full text](https://www.sciencedirect.com/science/article/pii/S0095895615000568/pdf)
* Miklós Simonovits, *A method for solving extremal problems in graph theory, stability problems*, Theory of Graphs (Proc. Colloq., Tihany, 1966), Academic Press, New York (1968), 279–319.
* Paul Erdős, *Some recent results on extremal problems in graph theory*, Theory of Graphs (Internat. Sympos., Rome, 1966), Gordon and Breach, New York (1967), 117–123.
* Paul Erdős, Péter Frankl, Vojtěch Rödl, *The asymptotic number of graphs not containing a fixed subgraph and a problem for hypergraphs having no exponent*, Graphs and Combinatorics 2 (1986), 113–121. [doi:10.1007/BF01788085](https://doi.org/10.1007/BF01788085)

<details><summary>Background references</summary>

* Yaël Dillies, Bhavik Mehta, *Formalising Szemerédi's Regularity Lemma in Lean*, 13th International Conference on Interactive Theorem Proving (ITP 2022), LIPIcs 237, 9:1–9:19. [doi:10.4230/LIPIcs.ITP.2022.9](https://doi.org/10.4230/LIPIcs.ITP.2022.9) · [free full text](https://drops.dagstuhl.de/storage/00lipics/lipics-vol237-itp2022/LIPIcs.ITP.2022.9/LIPIcs.ITP.2022.9.pdf)

</details>

## The graph removal lemma for every fixed graph

Palomar: [PALOMAR-2026-10-18-000002](https://palomar-registry.org/entry.html?id=PALOMAR-2026-10-18-000002&version=1) (version 1) · code: [jtraverso/graph-removal-lemma @ 589cf03](https://github.com/jtraverso/graph-removal-lemma/tree/589cf03ef1e4c80ea8cdd6be77778232c62dd37c) · [archived copy](https://github.com/PalomarArchive/jtraverso--graph-removal-lemma--03befbbe3fbf/tree/palomar/PALOMAR-2026-10-18-000002-v1/589cf03ef1e4c80ea8cdd6be77778232c62dd37c)

**What is proved.** A Lean 4 / Mathlib formalization of the graph removal lemma of Erdős, Frankl and Rödl for an arbitrary fixed finite graph H on k vertices: for every ε > 0 there is δ > 0, depending only on H and ε, such that every finite graph on n vertices with fewer than δ nᵏ labelled copies of H can be made H-free by deleting fewer than ε n² edges; equivalently (far form), a graph from which at least ε n² edges must be deleted to destroy all copies of H has at least δ nᵏ labelled copies. Also included is the counting lemma used in the proof: if parts s x (one for each vertex x of H) are robustly dense with density at least d along the edges of H, with 2kη ≤ dᵏ and #(s x) ≥ 4k/dᵏ, then at least (dᵏ/4)ᵏ ∏ #(s x) injective maps send H into G with f x ∈ s x. Mathlib has the regularity lemma and the triangle removal lemma, but not the removal lemma for a general H.

**Sources.**

* P. Erdős, P. Frankl, V. Rödl, *The asymptotic number of graphs not containing a fixed subgraph and a problem for hypergraphs having no exponent*, Graphs and Combinatorics 2 (1986), 113–121. [doi:10.1007/BF01788085](https://doi.org/10.1007/BF01788085)

<details><summary>Background references</summary>

* David Conlon, Jacob Fox, *Graph removal lemmas*, Surveys in Combinatorics 2013, London Math. Soc. Lecture Note Ser. 409; Section 2. [free full text](https://arxiv.org/pdf/1211.3487) (arXiv)

</details>

## The Bondy–Simonovits even cycle theorem

Palomar: [PALOMAR-2026-10-22-000043](https://palomar-registry.org/entry.html?id=PALOMAR-2026-10-22-000043&version=1) (version 1) · code: [jtraverso/bondy-simonovits @ a4ca4b2](https://github.com/jtraverso/bondy-simonovits/tree/a4ca4b28a0d82735316fd73a5a11303231109fc7) · [archived copy](https://github.com/PalomarArchive/jtraverso--bondy-simonovits--28aa00457e93/tree/palomar/PALOMAR-2026-10-22-000043-v1/a4ca4b28a0d82735316fd73a5a11303231109fc7)

**What is proved.** A Lean 4 / Mathlib formalization of the Bondy–Simonovits theorem: for every k ≥ 2 there is a constant C such that every finite simple graph on n vertices with no cycle of length exactly 2k has at most C·n^(1+1/k) edges, i.e. ex(n, C_2k) = O(n^(1+1/k)). The statement is existential in C (the proof gives C = 16k + 4); the sharper constants of later work and the full range of even cycle lengths in Bondy–Simonovits's paper are not stated. Mathlib has walks and cycles but not this theorem.

**Sources.**

* J. A. Bondy, M. Simonovits, *Cycles of even length in graphs*, Journal of Combinatorial Theory, Series B 16 (1974), 97–105. [doi:10.1016/0095-8956(74)90052-5](https://doi.org/10.1016/0095-8956(74)90052-5) · [free full text](https://doi.org/10.1016/0095-8956(74)90052-5)

<details><summary>Background references</summary>

* J. Verstraëte, *On arithmetic progressions of cycle lengths in graphs*, Combinatorics, Probability and Computing 9 (2000), 369–373. [doi:10.1017/S0963548300004478](https://doi.org/10.1017/S0963548300004478)
* O. Pikhurko, *A note on the Turán function of even cycles*, Proceedings of the American Mathematical Society 140 (2012), 3687–3692. [doi:10.1090/S0002-9939-2012-11274-2](https://doi.org/10.1090/S0002-9939-2012-11274-2) · [free full text](https://www.ams.org/proc/2012-140-11/S0002-9939-2012-11274-2/S0002-9939-2012-11274-2.pdf)

</details>

[← Back to the list](../README.md)
