# Vertex colouring: details

[← Back to the list](../README.md)

## Grötzsch's theorem, Ore's conjecture for k = 4 (Kostochka–Yancey), and the Grünbaum–Aksenov theorem

Palomar: [PALOMAR-2026-10-13-000005](https://palomar-registry.org/entry.html?id=PALOMAR-2026-10-13-000005&version=2) (version 2) · code: [jtraverso/grotzsch-ore @ ff6d512](https://github.com/jtraverso/grotzsch-ore/tree/ff6d5123c06e4c99bb6074e0a72e8be8d595eefa) · [archived copy](https://github.com/PalomarArchive/jtraverso--grotzsch-ore--8ebd0df3e665/tree/palomar/PALOMAR-2026-10-13-000005-v2/ff6d5123c06e4c99bb6074e0a72e8be8d595eefa) (v1: [archive](https://github.com/PalomarArchive/jtraverso--grotzsch-ore--8ebd0df3e665/tree/palomar/PALOMAR-2026-10-13-000005-v1/f923c459969d4a0a50d034cc02d558c7d4937436))

**What is proved.** A Lean 4 / Mathlib formalization of results on 3-colourings of planar graphs. (1) Kostochka and Yancey's theorem, the case k = 4 of Ore's 1967 conjecture on the minimum number of edges of k-critical graphs: every finite 4-critical graph G satisfies 3|E(G)| ≥ 5|V(G)| - 2, by their potential method. (2) Grötzsch's theorem: every finite triangle-free planar graph is 3-colourable, deduced from (1) as in Kostochka–Yancey, with the topological crossing argument replaced by a K5-minor argument with an apex inside a face. (3) Aksenov's and Jensen–Thomassen's theorem: a triangle-free planar graph plus one edge is 3-colourable (Borodin–Kostochka–Lidický–Yancey, Theorem 2). (4) A triangle-free planar graph plus one vertex of degree at most 4 is 3-colourable (BKLY, Theorem 4). (5) The Grünbaum–Aksenov theorem: every finite planar graph with at most three triangles is 3-colourable, following BKLY's short proof (Theorem 7), with precolouring extension for 4- and 5-cycles (BKLY Theorem 5, for arbitrary cycles) and a combinatorial region (Jordan-type) theorem for rotation systems making the interiors and outer faces of the paper precise. Planarity is defined combinatorially, by rotation systems of genus zero (Euler defect 0); as sanity checks on this definition K4 is shown planar and K5 and K3,3 non-planar.

**Sources.**

* Alexandr Kostochka, Matthew Yancey, *Ore's conjecture for k = 4 and Grötzsch's theorem*, Combinatorica 34 (2014), no. 3, 323–329; https://arxiv.org/abs/1209.1173. [free full text](https://arxiv.org/pdf/1209.1173) (arXiv)
* Oleg V. Borodin, Alexandr V. Kostochka, Bernard Lidický, Matthew Yancey, *Short proofs of coloring theorems on planar graphs*, European Journal of Combinatorics 36 (2014), 314–321; https://arxiv.org/abs/1211.3981. [free full text](https://arxiv.org/pdf/1211.3981) (arXiv)
* Herbert Grötzsch, *Zur Theorie der diskreten Gebilde, VII: Ein Dreifarbensatz für dreikreisfreie Netze auf der Kugel*, Wiss. Z. Martin-Luther-Univ. Halle-Wittenberg Math.-Nat. Reihe 8 (1958/1959), 109–120.
* Branko Grünbaum, *Grötzsch's theorem on 3-colorings*, Michigan Mathematical Journal 10 (1963), 303–310.
* V. A. Aksenov, *On continuation of 3-colouring of planar graphs (Russian)*, Diskretnyi Analiz 26 (1974), 3–19.

<details><summary>Background references</summary>

* Oleg V. Borodin, *A new proof of Grünbaum's 3 color theorem*, Discrete Mathematics 169 (1997), 177–183.
* Tommy R. Jensen, Carsten Thomassen, *The color space of a graph*, Journal of Graph Theory 34 (2000), 234–245.
* Oystein Ore, *The Four Color Problem*, Academic Press, New York, 1967.
* Jack Edmonds, *A combinatorial representation for polyhedral surfaces*, Notices of the American Mathematical Society 7 (1960), 646.

</details>

## The Hajnal–Szemerédi theorem on equitable colourings

Palomar: [PALOMAR-2026-10-13-000007](https://palomar-registry.org/entry.html?id=PALOMAR-2026-10-13-000007&version=1) (version 1) · code: [jtraverso/hajnal-szemeredi @ ba34061](https://github.com/jtraverso/hajnal-szemeredi/tree/ba34061e3cf12dfc8297610d5d7b3f0afac7ec54) · [archived copy](https://github.com/PalomarArchive/jtraverso--hajnal-szemeredi--c11276c44bab/tree/palomar/PALOMAR-2026-10-13-000007-v1/ba34061e3cf12dfc8297610d5d7b3f0afac7ec54)

**What is proved.** A Lean 4 / Mathlib formalization of the Hajnal–Szemerédi theorem (1970), conjectured by Erdős in 1964: every finite graph with maximum degree at most r has an equitable proper colouring with r + 1 colours, i.e. a proper colouring whose colour classes differ in size by at most one. The exact form is also proved: if the number of vertices is s(r + 1), every colour class has exactly s vertices (the colouring form of Erdős Problem #914). The proof follows the short argument of Kierstead and Kostochka (2008): induction on the number of edges; after deleting an edge, a nearly equitable colouring is repaired by moving vertices along paths of an auxiliary digraph on the colour classes (Lemma 2.1); when the large class is inaccessible, a family of terminal classes, solo edges and a discharging count with weights q/|S_z| (Lemmas 2.2–2.3) produce a recolouring that either finishes the colouring or strictly increases the number of accessible classes, using the induction hypothesis on the inaccessible part. The general case is reduced to the divisible one by adding a disjoint complete graph.

**Sources.**

* H. A. Kierstead, A. V. Kostochka, *A short proof of the Hajnal–Szemerédi theorem on equitable colouring*, Combinatorics, Probability and Computing 17 (2008), 265–270. [doi:10.1017/S0963548307008619](https://doi.org/10.1017/S0963548307008619)
* András Hajnal, Endre Szemerédi, *Proof of a conjecture of P. Erdős*, Combinatorial Theory and its Applications II (P. Erdős, A. Rényi, V. T. Sós, eds.), North-Holland, 1970, 601–623.

<details><summary>Background references</summary>

* Paul Erdős, *Problem 9*, Theory of Graphs and its Applications (M. Fiedler, ed.), Czech. Academy of Sciences, Prague, 1964, p. 159.
* *Erdős Problem #914*, https://www.erdosproblems.com/914.

</details>

## Brooks' theorem, degree-choosability and blocks

Palomar: [PALOMAR-2026-10-16-000003](https://palomar-registry.org/entry.html?id=PALOMAR-2026-10-16-000003&version=2) (version 2) · code: [jtraverso/brooks @ b99e6f5](https://github.com/jtraverso/brooks/tree/b99e6f500256586626396de9c2d6fd4d96119d60) · [archived copy](https://github.com/PalomarArchive/jtraverso--brooks--c255f4f55cbf/tree/palomar/PALOMAR-2026-10-16-000003-v2/b99e6f500256586626396de9c2d6fd4d96119d60)

**What is proved.** A Lean 4 / Mathlib formalization of Brooks' theorem: for k ≥ 3, a finite graph of maximum degree at most k without a (k+1)-clique is k-colourable (no connectedness assumption), and a finite connected graph that is neither complete nor an odd cycle is colourable with as many colours as its maximum degree. The proof uses greedy colourings in Lovász's style and an induction on the number of edges with a separation-and-gluing step. Version 2 adds the Erdős–Rubin–Taylor / Borodin theorem (a finite connected graph is degree-choosable, i.e. colourable from any lists with |L(v)| ≥ deg(v), if and only if it is not a Gallai tree: some block is neither complete nor an odd cycle), Brooks' theorem for lists (Vizing 1976), and a library of blocks of graphs (blocks as maximal nonseparable vertex sets, cut vertices, unique block per edge, blocks meeting in at most one vertex, the block–cut tree of a connected graph, and the agreement of the block and induced-subgraph descriptions of Gallai trees).

**Sources.**

* R. L. Brooks, *On colouring the nodes of a network*, Mathematical Proceedings of the Cambridge Philosophical Society 37 (1941), 194–197. [doi:10.1017/S030500410002168X](https://doi.org/10.1017/S030500410002168X)
* P. Erdős, A. L. Rubin, H. Taylor, *Choosability in graphs*, Proceedings of the West Coast Conference on Combinatorics, Graph Theory and Computing, Congressus Numerantium 26 (1979), 125–157.
* O. V. Borodin, *Criteria of chromaticity of a degree prescription*, Abstracts of the IV All-Union Conference on Theoretical Cybernetics, Novosibirsk (1977), 127–128 (in Russian).
* V. G. Vizing, *Vertex colorings with given colors*, Metody Diskretnogo Analiza 29 (1976), 3–10 (in Russian).

<details><summary>Background references</summary>

* L. Lovász, *Three short proofs in graph theory*, Journal of Combinatorial Theory, Series B 19 (1975), 269–271. [doi:10.1016/0095-8956(75)90089-1](https://doi.org/10.1016/0095-8956(75)90089-1) · [free full text](https://www.sciencedirect.com/science/article/pii/0095895675900891/pdf)
* A. V. Kostochka, M. Stiebitz, B. Wirth, *The colour theorems of Brooks and Gallai extended*, Discrete Mathematics 162 (1996), 299–303. [doi:10.1016/0012-365X(95)00294-7](https://doi.org/10.1016/0012-365X(95)00294-7) · [free full text](https://www.sciencedirect.com/science/article/pii/0012365X95002947/pdf)
* Reinhard Diestel, *Graph Theory*, Graduate Texts in Mathematics 173, 5th edition, Springer (2017), Section 3.1. [doi:10.1007/978-3-662-53622-3](https://doi.org/10.1007/978-3-662-53622-3)

</details>

## The Gallai–Hasse–Roy–Vitaver theorem

Palomar: [PALOMAR-2026-10-16-000015](https://palomar-registry.org/entry.html?id=PALOMAR-2026-10-16-000015&version=1) (version 1) · code: [jtraverso/gallai-roy @ e737218](https://github.com/jtraverso/gallai-roy/tree/e737218bf80c3d3684d670f5f8aa9a8257e1a52f) · [archived copy](https://github.com/PalomarArchive/jtraverso--gallai-roy--242cd45a936c/tree/palomar/PALOMAR-2026-10-16-000015-v1/e737218bf80c3d3684d670f5f8aa9a8257e1a52f)

**What is proved.** A Lean 4 / Mathlib formalization of the Gallai–Hasse–Roy–Vitaver theorem: if an orientation of a finite graph has no directed path on more than k vertices, the graph is k-colourable; and conversely every k-colourable graph has such an orientation. Hence the chromatic number is the minimum over orientations of the number of vertices of a longest directed path.

**Sources.**

* B. Roy, *Nombre chromatique et plus longs chemins d'un graphe*, Revue française d'informatique et de recherche opérationnelle 1 (1967), 129–132. [doi:10.1051/m2an/1967010501291](https://doi.org/10.1051/m2an/1967010501291) · [free full text](https://www.esaim-m2an.org/articles/m2an/pdf/1967/03/m2an1967010501291.pdf)
* M. Hasse, *Zur algebraischen Begründung der Graphentheorie. I*, Mathematische Nachrichten 28 (1965), 275–290. [doi:10.1002/mana.19650280503](https://doi.org/10.1002/mana.19650280503)
* T. Gallai, *On directed paths and circuits*, Theory of Graphs (Proc. Colloq. Tihany, 1966), Academic Press (1968), 115–118.
* L. M. Vitaver, *Determination of minimal coloring of vertices of a graph by means of Boolean powers of the incidence matrix*, Doklady Akademii Nauk SSSR 147 (1962), 758–759.

## Kneser's conjecture and the octahedral Tucker lemma

Palomar: [PALOMAR-2026-10-20-000006](https://palomar-registry.org/entry.html?id=PALOMAR-2026-10-20-000006&version=1) (version 1) · code: [jtraverso/kneser-lovasz @ 6699c87](https://github.com/jtraverso/kneser-lovasz/tree/6699c87d87f4ddb159fc42271263fc429e63004a) · [archived copy](https://github.com/PalomarArchive/jtraverso--kneser-lovasz--c99016c66bcc/tree/palomar/PALOMAR-2026-10-20-000006-v1/6699c87d87f4ddb159fc42271263fc429e63004a)

**What is proved.** A Lean 4 / Mathlib formalization of Lovász's theorem (Kneser's conjecture): for 0 < k and 2k ≤ n the Kneser graph KG(n, k) of k-subsets of an n-set, adjacent when disjoint, has chromatic number exactly n − 2k + 2; proved combinatorially from the octahedral Tucker lemma (an antipodal labelling of the nonzero sign vectors of length n by nonzero integers in [−m, m] with m < n has a complementary pair x ≼ y with λ(x) = −λ(y)), which is itself proved by Ky Fan's parity argument. Mathlib has neither Kneser graphs nor Tucker's lemma.

**Sources.**

* L. Lovász, *Kneser's conjecture, chromatic number, and homotopy*, Journal of Combinatorial Theory, Series A 25 (1978), 319–324. [doi:10.1016/0097-3165(78)90022-5](https://doi.org/10.1016/0097-3165(78)90022-5) · [free full text](https://www.sciencedirect.com/science/article/pii/0097316578900225/pdf)
* Jiří Matoušek, *A combinatorial proof of Kneser's conjecture*, Combinatorica 24 (2004), 163–170. [doi:10.1007/s00493-004-0011-1](https://doi.org/10.1007/s00493-004-0011-1) · [free full text](http://hdl.handle.net/20.500.11850/50671)
* Robert M. Freund, Michael J. Todd, *A constructive proof of Tucker's combinatorial lemma*, Journal of Combinatorial Theory, Series A 30 (1981), 321–325. [doi:10.1016/0097-3165(81)90027-3](https://doi.org/10.1016/0097-3165(81)90027-3) · [free full text](https://doi.org/10.1016/0097-3165(81)90027-3)

<details><summary>Background references</summary>

* Ky Fan, *A generalization of Tucker's combinatorial lemma with topological applications*, Annals of Mathematics 56 (1952), 431–437. [doi:10.2307/1969651](https://doi.org/10.2307/1969651)
* Jiří Matoušek, *Using the Borsuk–Ulam Theorem*, Springer (2008), Sections 2.3 and 3.3. [doi:10.1007/978-3-540-76649-0](https://doi.org/10.1007/978-3-540-76649-0)

</details>

## Jin's theorem on dense triangle-free graphs

Palomar: [PALOMAR-2026-10-20-000012](https://palomar-registry.org/entry.html?id=PALOMAR-2026-10-20-000012&version=1) (version 1) · code: [jtraverso/jin-triangle-free @ ae47df0](https://github.com/jtraverso/jin-triangle-free/tree/ae47df0ddb29c58a71afed658f9bf74aef1b6e90) · [archived copy](https://github.com/PalomarArchive/jtraverso--jin-triangle-free--8d9fbb5efd5d/tree/palomar/PALOMAR-2026-10-20-000012-v1/ae47df0ddb29c58a71afed658f9bf74aef1b6e90)

**What is proved.** A Lean 4 / Mathlib formalization of Jin's theorem: a finite triangle-free graph on n vertices with minimum degree greater than 10n/29 is 3-colourable; and of its sharpness: for every m ≥ 1 the blow-up of the Grötzsch graph with weights 3m, 2m, 4m is a triangle-free 10m-regular graph on 29m vertices that is not 3-colourable (Häggkvist). This extends the case r = 2 of the Andrásfai–Erdős–Sós theorem, which is in Mathlib. Mathlib does not have Jin's theorem.

**Sources.**

* G. P. Jin, *Triangle-free four-chromatic graphs*, Discrete Mathematics 145 (1995), 151–170. [doi:10.1016/0012-365X(94)00063-O](https://doi.org/10.1016/0012-365X(94)00063-O) · [free full text](https://www.sciencedirect.com/science/article/pii/0012365X9400063O/pdf)
* R. Häggkvist, *Odd cycles of specified length in non-bipartite graphs*, Graph Theory (Cambridge, 1981), North-Holland Mathematics Studies 62 (1982), 89–99. [doi:10.1016/S0304-0208(08)73552-7](https://doi.org/10.1016/S0304-0208(08)73552-7)

<details><summary>Background references</summary>

* C. C. Chen, G. P. Jin, K. M. Koh, *Triangle-free graphs with large degree*, Combinatorics, Probability and Computing 6 (1997), 381–396. [doi:10.1017/S0963548397003167](https://doi.org/10.1017/S0963548397003167)
* B. Andrásfai, P. Erdős, V. T. Sós, *On the connection between chromatic number, maximal clique and minimal degree of a graph*, Discrete Mathematics 8 (1974), 205–218. [doi:10.1016/0012-365X(74)90133-2](https://doi.org/10.1016/0012-365X(74)90133-2) · [free full text](https://doi.org/10.1016/0012-365x(74)90133-2)

</details>

## Lovász's perfect graph theorems

Palomar: [PALOMAR-2026-10-21-000007](https://palomar-registry.org/entry.html?id=PALOMAR-2026-10-21-000007&version=1) (version 1) · code: [jtraverso/perfect-graphs @ 7969224](https://github.com/jtraverso/perfect-graphs/tree/796922460172c4e51c39c96575d03957652c0bab) · [archived copy](https://github.com/PalomarArchive/jtraverso--perfect-graphs--f01c6e39f696/tree/palomar/PALOMAR-2026-10-21-000007-v1/796922460172c4e51c39c96575d03957652c0bab)

**What is proved.** A Lean 4 / Mathlib formalization of Lovász's 1972 theorems on perfect graphs: a finite simple graph is perfect (every induced subgraph has chromatic number equal to its clique number) if and only if |S| ≤ α(G[S]) · ω(G[S]) for every vertex set S; and the perfect graph theorem conjectured by Berge, that a finite graph is perfect if and only if its complement is perfect. The proof follows Gasparian's linear-algebra argument. Mathlib has chromatic, clique and independence numbers but no perfect graphs.

**Sources.**

* L. Lovász, *Normal hypergraphs and the perfect graph conjecture*, Discrete Mathematics 2 (1972), 253–267. [doi:10.1016/0012-365X(72)90006-4](https://doi.org/10.1016/0012-365X(72)90006-4) · [free full text](https://www.sciencedirect.com/science/article/pii/0012365X72900064/pdf)
* L. Lovász, *A characterization of perfect graphs*, Journal of Combinatorial Theory, Series B 13 (1972), 95–98. [doi:10.1016/0095-8956(72)90045-7](https://doi.org/10.1016/0095-8956(72)90045-7) · [free full text](https://www.sciencedirect.com/science/article/pii/0095895672900457/pdf)

<details><summary>Background references</summary>

* G. S. Gasparian, *Minimal imperfect graphs: a simple approach*, Combinatorica 16 (1996), 209–212. [doi:10.1007/BF01844846](https://doi.org/10.1007/BF01844846)

</details>

## Stanley's acyclic orientations and chromatic reciprocity

Palomar: [PALOMAR-2026-10-28-000009](https://palomar-registry.org/entry.html?id=PALOMAR-2026-10-28-000009&version=1) (version 1) · code: [jtraverso/stanley @ 48d36cb](https://github.com/jtraverso/stanley/tree/48d36cbaa54d14443f99b57776ce65f1f31c8331) · [archived copy](https://github.com/PalomarArchive/jtraverso--stanley--df253fa631b4/tree/palomar/PALOMAR-2026-10-28-000009-v1/48d36cbaa54d14443f99b57776ce65f1f31c8331)

**What is proved.** For every finite simple graph and k ≥ 0, the signed evaluation (−1)^n χ_G(−k) counts acyclic orientations paired with weakly compatible Fin k colorings (Stanley 1973, Theorem 1.2); at k = 1 it counts acyclic orientations (Corollary 1.3). Includes positive-evaluation correctness, induced-subgraph convolution, and the finite equivalence between well-foundedness and no directed cycles.

**Sources.**

* Richard P. Stanley, *Acyclic orientations of graphs*, Discrete Mathematics 5 (1973), 171–178; author-hosted 2006 reprint at https://math.mit.edu/~rstan/pubs/pubfiles/18.pdf. [doi:10.1016/0012-365X(73)90108-8](https://doi.org/10.1016/0012-365X(73)90108-8) · [free full text](https://www.sciencedirect.com/science/article/pii/0012365X73901088/pdf)

[← Back to the list](../README.md)
