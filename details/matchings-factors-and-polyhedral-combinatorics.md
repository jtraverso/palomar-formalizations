# Matchings, factors and polyhedral combinatorics: details

[← Back to the list](../README.md)

## Petersen's theorem

Palomar: [PALOMAR-2026-10-16-000004](https://palomar-registry.org/entry.html?id=PALOMAR-2026-10-16-000004&version=1) (version 1) · code: [jtraverso/petersen-matching @ 77630d6](https://github.com/jtraverso/petersen-matching/tree/77630d6771d3f5a3da2185db2ff451f6c6ed5190) · [archived copy](https://github.com/PalomarArchive/jtraverso--petersen-matching--386afe9ae9e1/tree/palomar/PALOMAR-2026-10-16-000004-v1/77630d6771d3f5a3da2185db2ff451f6c6ed5190)

**What is proved.** A Lean 4 / Mathlib formalization of Petersen's theorem: a finite 3-regular graph in which no edge is a bridge has a perfect matching; moreover, every edge of such a graph lies in some perfect matching. Both statements are derived from Tutte's theorem (in Mathlib) by counting the edges that leave the odd components.

**Sources.**

* Julius Petersen, *Die Theorie der regulären graphs*, Acta Mathematica 15 (1891), 193–220. [doi:10.1007/BF02392606](https://doi.org/10.1007/BF02392606) · [free full text](https://projecteuclid.org/journals/acta-mathematica/volume-15/issue-none/Die-Theorie-der-regul%c3%a4ren-graphs/10.1007/BF02392606.pdf)

<details><summary>Background references</summary>

* W. T. Tutte, *The factorization of linear graphs*, Journal of the London Mathematical Society 22 (1947), 107–111. [doi:10.1112/jlms/s1-22.2.107](https://doi.org/10.1112/jlms/s1-22.2.107)

</details>

## Berge's theorem, the Tutte–Berge formula and the Gallai–Edmonds theorem

Palomar: [PALOMAR-2026-10-16-000011](https://palomar-registry.org/entry.html?id=PALOMAR-2026-10-16-000011&version=2) (version 2) · code: [jtraverso/berge-matching @ f01d042](https://github.com/jtraverso/berge-matching/tree/f01d042c071c778fb3f432312356136a92369076) · [archived copy](https://github.com/PalomarArchive/jtraverso--berge-matching--b269b121c46f/tree/palomar/PALOMAR-2026-10-16-000011-v2/f01d042c071c778fb3f432312356136a92369076)

**What is proved.** A Lean 4 / Mathlib formalization of Berge's augmenting path theorem (a matching is maximum if and only if there is no augmenting path) and of the Tutte–Berge formula (the maximum size of a matching is the minimum over vertex sets U of (|V| + |U| − odd(G − U)) / 2), with the weak inequality for all matchings and vertex sets; the formula is derived from Mathlib's Tutte theorem by adding universal vertices. Version 2 adds the Gallai–Edmonds structure theorem: with D the vertices missed by some maximum matching, A their neighbours outside D and C the rest, the components of G[D] are factor-critical, G[C] has a perfect matching, every maximum matching matches A into distinct components of G[D], and 2ν(G) = |V| + |A| − c(G[D]).

**Sources.**

* Claude Berge, *Two theorems in graph theory*, Proceedings of the National Academy of Sciences of the USA 43 (1957), 842–844. [doi:10.1073/pnas.43.9.842](https://doi.org/10.1073/pnas.43.9.842) · [free full text](http://europepmc.org/pmc/articles/PMC534337)
* Claude Berge, *Sur le couplage maximum d'un graphe*, Comptes Rendus de l'Académie des Sciences de Paris 247 (1958), 258–259.
* Jack Edmonds, *Paths, trees, and flowers*, Canadian Journal of Mathematics 17 (1965), 449–467. [doi:10.4153/CJM-1965-045-4](https://doi.org/10.4153/CJM-1965-045-4) · [free full text](https://www.cambridge.org/core/services/aop-cambridge-core/content/view/08B492B72322C4130AE800C0610E0E21/S0008414X00039419a.pdf/div-class-title-paths-trees-and-flowers-div.pdf)
* Tibor Gallai, *Maximale Systeme unabhängiger Kanten*, Magyar Tudományos Akadémia Matematikai Kutató Intézetének Közleményei 9 (1964), 401–413.

<details><summary>Background references</summary>

* László Lovász, Michael D. Plummer, *Matching Theory*, AMS Chelsea Publishing (2009), Chapter 3. [doi:10.1090/chel/367](https://doi.org/10.1090/chel/367)
* W. T. Tutte, *The factorization of linear graphs*, Journal of the London Mathematical Society 22 (1947), 107–111. [doi:10.1112/jlms/s1-22.2.107](https://doi.org/10.1112/jlms/s1-22.2.107)

</details>

## Euler's theorem on Eulerian circuits and trails, and Petersen's 2-factor theorem

Palomar: [PALOMAR-2026-10-16-000016](https://palomar-registry.org/entry.html?id=PALOMAR-2026-10-16-000016&version=1) (version 1) · code: [jtraverso/euler-petersen @ 02c3f1a](https://github.com/jtraverso/euler-petersen/tree/02c3f1a5327c5f066938860bb07e9fce226b36ca) · [archived copy](https://github.com/PalomarArchive/jtraverso--euler-petersen--780912a29df2/tree/palomar/PALOMAR-2026-10-16-000016-v1/02c3f1a5327c5f066938860bb07e9fce226b36ca)

**What is proved.** A Lean 4 / Mathlib formalization of the classical characterization of Eulerian graphs and of Petersen's 2-factor theorem, for finite simple graphs. (1) Euler–Hierholzer: a finite connected graph has an Eulerian circuit if and only if every vertex has even degree, and the circuit can start at any prescribed vertex. (2) Eulerian trails: a finite connected graph has an Eulerian trail if and only if it has 0 or 2 vertices of odd degree; when the odd vertices are exactly a and b, there is an Eulerian trail from a to b. (3) Eulerian orientations: if every degree is even, the edges can be oriented so that every vertex has equal in- and out-degree. (4) Petersen's 2-factor theorem (1891): every finite 2k-regular graph is the edge-disjoint union of k spanning 2-regular subgraphs. The proof of (4) is built on (1)–(3): the graph is decomposed into edge-disjoint closed trails (using the closed-trail lemma behind the Euler theorems), oriented along them, and the resulting k-regular digraph is split into k permutations by Hall's marriage theorem; each permutation yields a 2-factor. Mathlib already contained the necessity directions of (1) and (2); their sufficiency directions were listed there as open TODO items.

**Sources.**

* Leonhard Euler, *Solutio problematis ad geometriam situs pertinentis*, Commentarii academiae scientiarum Petropolitanae 8 (1741), 128–140; https://scholarlycommons.pacific.edu/euler-works/53/.
* Carl Hierholzer, *Ueber die Möglichkeit, einen Linienzug ohne Wiederholung und ohne Unterbrechung zu umfahren*, Mathematische Annalen 6 (1873), 30–32. [doi:10.1007/BF01442866](https://doi.org/10.1007/BF01442866) · [free full text](https://zenodo.org/record/1447429)
* Julius Petersen, *Die Theorie der regulären graphs*, Acta Mathematica 15 (1891), 193–220. [doi:10.1007/BF02392606](https://doi.org/10.1007/BF02392606) · [free full text](https://projecteuclid.org/journals/acta-mathematica/volume-15/issue-none/Die-Theorie-der-regul%c3%a4ren-graphs/10.1007/BF02392606.pdf)

<details><summary>Background references</summary>

* Philip Hall, *On representatives of subsets*, Journal of the London Mathematical Society 10 (1935), 26–30. [doi:10.1112/jlms/s1-10.37.26](https://doi.org/10.1112/jlms/s1-10.37.26)
* Tim Räz, *Mathematical Explanations in Euler's Königsberg*, https://philsci-archive.pitt.edu/11094/ (2014); later version: European Journal for Philosophy of Science (2018).

</details>

## Tutte's f-factor theorem

Palomar: [PALOMAR-2026-10-18-000005](https://palomar-registry.org/entry.html?id=PALOMAR-2026-10-18-000005&version=1) (version 1) · code: [jtraverso/tutte-f-factor @ dc3bbce](https://github.com/jtraverso/tutte-f-factor/tree/dc3bbce463c80c499d3e9fa072d13f9145d907d0) · [archived copy](https://github.com/PalomarArchive/jtraverso--tutte-f-factor--c791dc403ea0/tree/palomar/PALOMAR-2026-10-18-000005-v1/dc3bbce463c80c499d3e9fa072d13f9145d907d0)

**What is proved.** A Lean 4 / Mathlib formalization of Tutte's f-factor theorem: a finite simple graph G has a spanning subgraph H with deg_H v = f v for every vertex v if and only if, for all disjoint vertex sets S and T, q(S, T) ≤ ∑_{v ∈ S} f v − ∑_{v ∈ T} f v + ∑_{v ∈ T} deg_{G−S} v, where q(S, T) is the number of connected components C of G − (S ∪ T) for which ∑_{v ∈ C} f v + e(C, T) is odd and deg_{G−S} v is the number of neighbours of v outside S. Mathlib has Tutte's 1-factor theorem but not the f-factor theorem.

**Sources.**

* W. T. Tutte, *The Factors of Graphs*, Canadian Journal of Mathematics 4 (1952), 314–328. [doi:10.4153/CJM-1952-028-2](https://doi.org/10.4153/CJM-1952-028-2) · [free full text](https://www.cambridge.org/core/services/aop-cambridge-core/content/view/320CE524F3E9AA34F0BF6A824642C34B/S0008414X00036270a.pdf/div-class-title-the-factors-of-graphs-div.pdf)
* W. T. Tutte, *A Short Proof of the Factor Theorem for Finite Graphs*, Canadian Journal of Mathematics 6 (1954), 347–352. [doi:10.4153/CJM-1954-033-3](https://doi.org/10.4153/CJM-1954-033-3) · [free full text](https://www.cambridge.org/core/services/aop-cambridge-core/content/view/3785657C35F370E32E5AEAFC3D1B84CE/S0008414X00023774a.pdf/div-class-title-a-short-proof-of-the-factor-theorem-for-finite-graphs-div.pdf)

## Graphic sequences: the Erdős–Gallai and Havel–Hakimi theorems

Palomar: [PALOMAR-2026-10-16-000017](https://palomar-registry.org/entry.html?id=PALOMAR-2026-10-16-000017&version=1) (version 1) · code: [jtraverso/degree-sequences @ b49808e](https://github.com/jtraverso/degree-sequences/tree/b49808e0c0aade945472b777047148399a582858) · [archived copy](https://github.com/PalomarArchive/jtraverso--degree-sequences--21c02be05315/tree/palomar/PALOMAR-2026-10-16-000017-v1/b49808e0c0aade945472b777047148399a582858)

**What is proved.** A Lean 4 / Mathlib formalization of the two classical characterizations of degree sequences of finite simple graphs: the Erdős–Gallai theorem (a non-increasing sequence is graphic if and only if its sum is even and every initial segment satisfies the Erdős–Gallai inequality) and the Havel–Hakimi theorem (a non-increasing sequence is graphic if and only if its first term is at most the number of remaining terms, the next d₀ terms are positive, and the reduced sequence is graphic).

**Sources.**

* P. Erdős, T. Gallai, *Gráfok előírt fokú pontokkal (Graphs with prescribed degrees of vertices)*, Matematikai Lapok 11 (1960), 264–274.
* Václav Havel, *A remark on the existence of finite graphs*, Časopis pro pěstování matematiky 80 (1955), 477–480. [doi:10.21136/CPM.1955.108220](https://doi.org/10.21136/CPM.1955.108220) · [free full text](https://doi.org/10.21136/cpm.1955.108220)
* S. L. Hakimi, *On realizability of a set of integers as degrees of the vertices of a linear graph. I*, Journal of the Society for Industrial and Applied Mathematics 10 (1962), 496–506. [doi:10.1137/0110037](https://doi.org/10.1137/0110037)

<details><summary>Background references</summary>

* S. A. Choudum, *A simple proof of the Erdős–Gallai theorem on graph sequences*, Bulletin of the Australian Mathematical Society 33 (1986), 67–70. [doi:10.1017/S0004972700002872](https://doi.org/10.1017/S0004972700002872) · [free full text](https://www.cambridge.org/core/services/aop-cambridge-core/content/view/FCA8B7DC763D3D504C68E3A5FDD8DE45/S0004972700002872a.pdf/div-class-title-a-simple-proof-of-the-erdos-gallai-theorem-on-graph-sequences-div.pdf)

</details>

## Regular subgraphs of almost regular graphs (Alon–Friedland–Kalai)

Palomar: [PALOMAR-2026-10-26-000001](https://palomar-registry.org/entry.html?id=PALOMAR-2026-10-26-000001&version=1) (version 1) · code: [jtraverso/regular-subgraphs @ daea9b3](https://github.com/jtraverso/regular-subgraphs/tree/daea9b30d10bfae6c75ba7be5904080119bbbdba) · [archived copy](https://github.com/PalomarArchive/jtraverso--regular-subgraphs--8e423f4bda53/tree/palomar/PALOMAR-2026-10-26-000001-v1/daea9b30d10bfae6c75ba7be5904080119bbbdba)

**What is proved.** A Lean 4 / Mathlib formalization of the Alon–Friedland–Kalai theorem for primes: for a prime p, every finite simple graph with maximum degree at most 2p − 1 and average degree greater than 2p − 2 contains a p-regular subgraph (a nonempty subgraph with all degrees 0 or p); as a corollary, every 4-regular graph plus an edge contains a 3-regular subgraph. The prime-power case of the paper is not stated. The proof uses Mathlib's Chevalley–Warning theorem.

**Sources.**

* N. Alon, S. Friedland, G. Kalai, *Regular subgraphs of almost regular graphs*, Journal of Combinatorial Theory, Series B 37 (1984), 79–91. [doi:10.1016/0095-8956(84)90047-9](https://doi.org/10.1016/0095-8956(84)90047-9) · [free full text](https://doi.org/10.1016/0095-8956(84)90047-9)

## Edmonds cardinality matroid intersection

Palomar: [PALOMAR-2026-10-28-000005](https://palomar-registry.org/entry.html?id=PALOMAR-2026-10-28-000005&version=1) (version 1) · code: [jtraverso/edmonds-matroid-intersection @ 824e019](https://github.com/jtraverso/edmonds-matroid-intersection/tree/824e019d4c845e8d0ebd8638fd94f19040115cbd) · [archived copy](https://github.com/PalomarArchive/jtraverso--edmonds-matroid-intersection--3c509773d989/tree/palomar/PALOMAR-2026-10-28-000005-v1/824e019d4c845e8d0ebd8638fd94f19040115cbd)

**What is proved.** Cardinality min-max theorem for two finite Mathlib matroids with the same ground, attained primal-dual certificates, exact-size feasibility and the equal-rank common-base criterion.

**Sources.**

* Jack Edmonds, *Submodular Functions, Matroids, and Certain Polyhedra*, Combinatorial Structures and Their Applications (1970), 69–87; reprint LNCS 2570 (2003), 11–26. [doi:10.1007/3-540-36478-1_2](https://doi.org/10.1007/3-540-36478-1_2)
* Alexander Schrijver, *Combinatorial Optimization: Polyhedra and Efficiency*, Chapter 41, Theorem 41.1 and Corollary 41.1a, pp. 700–701.
* Tutte formalization contributors, *Lean Pool finite natural matroid rank interface*, LeanPool/lean-pool at edbe5bd56f476cc2965564676b66199f281ab714, LeanPool/TuttePath/FlatRank.lean.

## Edmonds' perfect matching polytope and matching polytope

Palomar: [PALOMAR-2026-10-28-000010](https://palomar-registry.org/entry.html?id=PALOMAR-2026-10-28-000010&version=1) (version 1) · code: [jtraverso/edmonds-matching-polytope @ 6198b83](https://github.com/jtraverso/edmonds-matching-polytope/tree/6198b8314ac88a5638120fcf15d5b58c024caaab) · [archived copy](https://github.com/PalomarArchive/jtraverso--edmonds-matching-polytope--a32c69454bfc/tree/palomar/PALOMAR-2026-10-28-000010-v1/6198b8314ac88a5638120fcf15d5b58c024caaab)

**What is proved.** A Lean 4 / Mathlib formalization of Edmonds' theorems (1965) for finite simple graphs: the convex hull of the incidence vectors of the perfect matchings is {x ≥ 0, x(δ(v)) = 1 for every vertex v, x(δ(S)) ≥ 1 for every odd set S}, and the convex hull of the incidence vectors of all matchings is {x ≥ 0, x(δ(v)) ≤ 1, x(E[S]) ≤ (|S| − 1)/2 for every odd S}. Vectors are indexed by the edges of the graph, the convex hull is Mathlib's convexHull, and matchings are Mathlib's Subgraph.IsMatching and Subgraph.IsPerfectMatching. The perfect matching theorem is proved for multigraphs by induction with shrinking of tight odd cuts; the matching polytope follows by the doubling construction. Mathlib does not contain these results.

**Sources.**

* J. Edmonds, *Maximum matching and a polyhedron with 0,1-vertices*, Journal of Research of the National Bureau of Standards, Section B 69B (1965), 125–130. [doi:10.6028/jres.069B.013](https://doi.org/10.6028/jres.069B.013) · [free full text](https://doi.org/10.6028/jres.069b.013)

<details><summary>Background references</summary>

* A. Schrijver, *Short proofs on the matching polyhedron*, Journal of Combinatorial Theory, Series B 34 (1983), 104–108. [doi:10.1016/0095-8956(83)90011-4](https://doi.org/10.1016/0095-8956(83)90011-4) · [free full text](https://www.sciencedirect.com/science/article/pii/0095895683900114/pdf)

</details>

[← Back to the list](../README.md)
