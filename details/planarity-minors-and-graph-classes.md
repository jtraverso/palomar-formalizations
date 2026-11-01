# Planarity, minors and graph classes: details

[← Back to the list](../README.md)

## Kuratowski's theorem

Palomar: [PALOMAR-2026-10-15-000018](https://palomar-registry.org/entry.html?id=PALOMAR-2026-10-15-000018&version=1) (version 1) · code: [jtraverso/kuratowski @ 696ec89](https://github.com/jtraverso/kuratowski/tree/696ec897a9b91933037767d897670aa30ba3683a) · [archived copy](https://github.com/PalomarArchive/jtraverso--kuratowski--c5380f41889a/tree/palomar/PALOMAR-2026-10-15-000018-v1/696ec897a9b91933037767d897670aa30ba3683a)

**What is proved.** A Lean 4 / Mathlib formalization of Kuratowski's theorem: a finite graph is planar if and only if it contains no subdivision of K5 and no subdivision of K3,3. Planarity is the combinatorial notion (a rotation system of genus zero). The proof combines Wagner's minor characterization (from the author's planarity library) with three new lemmas: a subdivision of any finite graph H gives H as a minor; a K3,3 minor gives a K3,3 subdivision; a K5 minor gives a K5 or a K3,3 subdivision. The last two rest on joining up to four terminals inside a connected branch set to one centre or to two adjacent centres by internally disjoint paths.

**Sources.**

* Kazimierz Kuratowski, *Sur le problème des courbes gauches en Topologie*, Fundamenta Mathematicae 15 (1930), 271–283. [doi:10.4064/fm-15-1-271-283](https://doi.org/10.4064/fm-15-1-271-283) · [free full text](https://www.impan.pl/shop/publication/transaction/download/product/92829?download.pdf)

<details><summary>Background references</summary>

* Klaus Wagner, *Über eine Eigenschaft der ebenen Komplexe*, Mathematische Annalen 114 (1937), 570–590.

</details>

## Kotzig's theorem on light edges of planar graphs

Palomar: [PALOMAR-2026-11-01-000023](https://palomar-registry.org/entry.html?id=PALOMAR-2026-11-01-000023&version=2) (version 2) · code: [jtraverso/kotzig-light-edges @ ccf55b1](https://github.com/jtraverso/kotzig-light-edges/tree/ccf55b1b968743ee5952ef4c9d78c88520f86bc2) · [archived copy](https://github.com/PalomarArchive/jtraverso--kotzig-light-edges--9922bf0b4bf4/tree/palomar/PALOMAR-2026-11-01-000023-v2/ccf55b1b968743ee5952ef4c9d78c88520f86bc2)

**What is proved.** A Lean 4 / Mathlib formalization of Kotzig's theorem on light edges and its relatives, for finite simple graphs with the combinatorial planarity (genus-zero rotation systems) of the registered entry Kuratowski's theorem. The weight of an edge uv is deg u + deg v. A planar graph of minimum degree at least three has an edge of weight at most 13 (kotzig_borodin; the form without 3-connectivity conjectured by Erdős and proved by Borodin); a planar graph of minimum degree at least four has an edge of weight at most 11 (light_edge_minDegree_four); Kotzig's theorem (1955): a 3-connected planar graph has an edge of weight at most 13, and at most 11 if it has no vertex of degree three (kotzig); Wernicke's theorem (1904): a planar graph of minimum degree at least five has a vertex of degree five adjacent to a vertex of degree at most six (wernicke). Four statements. The proof is a discharging argument carried out directly on the rotation system, without triangulating.

**Sources.**

* Anton Kotzig, *Príspevok k teórii eulerovských polyédrov (Contribution to the theory of Eulerian polyhedra)*, Mat.-Fyz. Časopis Slovensk. Akad. Vied 5 (1955) 101–113 (in Slovak): the light edge theorem for 3-connected planar graphs.
* Daniel W. Cranston, Douglas B. West, *An introduction to the discharging method via graph coloring*, arXiv:1306.4434v2, Section 3.1 (light edges), Lemma 3.2 and its proof; published in Discrete Math. 340 (2017) 766–793, doi:10.1016/j.disc.2016.11.022. [free full text](https://arxiv.org/pdf/1306.4434) (arXiv)
* Oleg V. Borodin, *On the total coloring of planar graphs*, J. Reine Angew. Math. 394 (1989) 180–185: the light edge theorem for planar graphs of minimum degree at least three. [doi:10.1515/crll.1989.394.180](https://doi.org/10.1515/crll.1989.394.180)
* Paul Wernicke, *Über den kartographischen Vierfarbensatz*, Math. Ann. 58 (1904) 413–426: a planar graph of minimum degree five has a 5-vertex adjacent to a 5- or 6-vertex. [doi:10.1007/BF01444968](https://doi.org/10.1007/BF01444968) · [free full text](https://zenodo.org/record/1428228)

## Borodin's light triangles in planar graphs of minimum degree five

Palomar: [PALOMAR-2026-11-01-000024](https://palomar-registry.org/entry.html?id=PALOMAR-2026-11-01-000024&version=2) (version 2) · code: [jtraverso/borodin-light-triangles @ 5a2639b](https://github.com/jtraverso/borodin-light-triangles/tree/5a2639b3fc7d14491f1c79de46fa49cb38c64ddf) · [archived copy](https://github.com/PalomarArchive/jtraverso--borodin-light-triangles--5777cc51dc6e/tree/palomar/PALOMAR-2026-11-01-000024-v2/5a2639b3fc7d14491f1c79de46fa49cb38c64ddf)

**What is proved.** A Lean 4 / Mathlib formalization of Borodin's theorem on light triangles, for finite simple graphs with the combinatorial planarity (genus-zero rotation systems) of the registered entry Kuratowski's theorem. The weight of a triangle is the sum of the degrees of its vertices. Every plane map of a graph of minimum degree at least five has a face of length three of weight at most 17 (light_face), and hence a planar graph of minimum degree at least five has a triangle of weight at most 17 (light_triangle). Two statements. The proof is a discharging argument run on the rotation system, with face charges in place of an edge-maximal counterexample; the local analysis at 5-vertices (32768 configurations of neighbour degrees capped at eight and corner types) is checked by decide in the kernel.

**Sources.**

* Oleg V. Borodin, *Solution of problems of Kotzig and Grünbaum concerning the isolation of cycles in planar graphs*, Mat. Zametki 46 (1989), no. 5, 9–12 (Russian); translated in Math. Notes 46 (1989) 835–837: a plane graph of minimum degree five has a 3-face of weight at most 17. [doi:10.1007/BF01139613](https://doi.org/10.1007/BF01139613)
* Daniel W. Cranston, Douglas B. West, *An introduction to the discharging method via graph coloring*, arXiv:1306.4434v2, Theorem 3.4 and its proof sketch (rules R1–R3); published in Discrete Math. 340 (2017) 766–793, doi:10.1016/j.disc.2016.11.022. [free full text](https://arxiv.org/pdf/1306.4434) (arXiv)

<details><summary>Background references</summary>

* Stanislav Jendrol', Heinz-Jürgen Voss, *Light subgraphs of graphs embedded in the plane—A survey*, Discrete Math. 313 (2013) 406–421. [doi:10.1016/j.disc.2012.11.007](https://doi.org/10.1016/j.disc.2012.11.007) · [free full text](https://www.sciencedirect.com/science/article/pii/S0012365X1200489X/pdf)

</details>

## Light stars and paths in planar graphs of minimum degree five (Jendrol'–Madaras)

Palomar: [PALOMAR-2026-11-01-000025](https://palomar-registry.org/entry.html?id=PALOMAR-2026-11-01-000025&version=1) (version 1) · code: [jtraverso/lebesgue-light-stars @ 76c43b6](https://github.com/jtraverso/lebesgue-light-stars/tree/76c43b645dc6dbf14dbf6d5151fac448a1c34835) · [archived copy](https://github.com/PalomarArchive/jtraverso--lebesgue-light-stars--768fd26189ef/tree/palomar/PALOMAR-2026-11-01-000025-v1/76c43b645dc6dbf14dbf6d5151fac448a1c34835)

**What is proved.** A Lean 4 / Mathlib formalization of Theorems 1, 2 and 3 of Jendrol' and Madaras (1996), for finite simple graphs with the combinatorial planarity (genus-zero rotation systems) of the registered entry Kuratowski's theorem. Every planar graph of minimum degree at least five has: a vertex X of degree five with three distinct neighbours A1, A2, A3 such that deg A1 = 5, deg A2 ≤ 6 and deg A3 ≤ 7, or deg A1 = deg A2 = deg A3 = 6 (light_star, Theorem 1; in particular a 5-vertex with three neighbours of degree at most seven, "Lebesgue's star"); a vertex of degree five with four distinct neighbours of degree at most ten (light_star4, Theorem 2); and a path on four vertices whose degrees sum to at most 23 (light_path4, Theorem 3). Three statements. The proofs are discharging arguments run on the rotation system with face charges instead of triangulating or using edge-maximal counterexamples; the local analyses (32768, 16384, 32768 and 100000 configurations) and the parity of an 11-cycle are checked by decide in the kernel.

**Sources.**

* Stanislav Jendrol', Tomáš Madaras, *On light subgraphs in plane graphs of minimum degree five*, Discuss. Math. Graph Theory 16 (1996) 207–217: Theorem 1 (light 3-stars, pp. 209–211), Theorem 2 (light 4-stars, pp. 211–213) and Theorem 3 (light 4-paths, pp. 213–214), with their proofs. [doi:10.7151/dmgt.1035](https://doi.org/10.7151/dmgt.1035)

<details><summary>Background references</summary>

* Stanislav Jendrol', Heinz-Jürgen Voss, *Light subgraphs of graphs embedded in the plane—A survey*, Discrete Math. 313 (2013) 406–421. [doi:10.1016/j.disc.2012.11.007](https://doi.org/10.1016/j.disc.2012.11.007) · [free full text](https://www.sciencedirect.com/science/article/pii/S0012365X1200489X/pdf)

</details>

## Mader's theorem and Hadwiger's conjecture for t ≤ 4

Palomar: [PALOMAR-2026-10-16-000001](https://palomar-registry.org/entry.html?id=PALOMAR-2026-10-16-000001&version=1) (version 1) · code: [jtraverso/hadwiger-mader @ cb10154](https://github.com/jtraverso/hadwiger-mader/tree/cb10154cd439a419d0bbf34052839dd27242b619) · [archived copy](https://github.com/PalomarArchive/jtraverso--hadwiger-mader--a4b96dfb7362/tree/palomar/PALOMAR-2026-10-16-000001-v1/cb10154cd439a419d0bbf34052839dd27242b619)

**What is proved.** A Lean 4 / Mathlib formalization of Mader's theorem (a nonempty finite graph of average degree at least 2^(r−2) has a K_r minor), of Dirac's lemma (a graph without a K4 minor has a vertex of degree at most two, hence at most 2n − 3 edges for n ≥ 2), and of Hadwiger's conjecture for t ≤ 4 (graphs without a K3 minor are 2-colourable, graphs without a K4 minor are 3-colourable). Minors are branch-set models.

**Sources.**

* W. Mader, *Homomorphieeigenschaften und mittlere Kantendichte von Graphen*, Mathematische Annalen 174 (1967), 265–268. [doi:10.1007/BF01364272](https://doi.org/10.1007/BF01364272)
* G. A. Dirac, *A property of 4-chromatic graphs and some remarks on critical graphs*, Journal of the London Mathematical Society 27 (1952), 85–92. [doi:10.1112/jlms/s1-27.1.85](https://doi.org/10.1112/jlms/s1-27.1.85)
* H. Hadwiger, *Über eine Klassifikation der Streckenkomplexe*, Vierteljahrsschrift der Naturforschenden Gesellschaft in Zürich 88 (1943), 133–142.

<details><summary>Background references</summary>

* Reinhard Diestel, *Graph Theory (5th edition)*, Graduate Texts in Mathematics 173, Springer (2017). [doi:10.1007/978-3-662-53622-3](https://doi.org/10.1007/978-3-662-53622-3)

</details>

## Chordal, split, threshold and cograph structure

Palomar: [PALOMAR-2026-10-18-000006](https://palomar-registry.org/entry.html?id=PALOMAR-2026-10-18-000006&version=1) (version 1) · code: [jtraverso/chordal-split-threshold-graphs @ ed65dcd](https://github.com/jtraverso/chordal-split-threshold-graphs/tree/ed65dcdc7339767d3e8e412420abbf54eae65ddb) · [archived copy](https://github.com/PalomarArchive/jtraverso--chordal-split-threshold-graphs--600d961f6749/tree/palomar/PALOMAR-2026-10-18-000006-v1/ed65dcdc7339767d3e8e412420abbf54eae65ddb)

**What is proved.** A Lean 4 / Mathlib formalization of classical structure theorems for finite simple graphs. Chordal graphs: every minimal a–b separator is a clique, a nonempty finite chordal graph has a simplicial vertex, and a connected non-complete one has two non-adjacent simplicial vertices (Dirac 1961); a finite graph is chordal iff it has a perfect elimination order (Fulkerson–Gross 1965), iff it is the intersection graph of subtrees of a finite tree (Gavril 1974); a nonempty finite chordal graph has treewidth ω − 1, and every finite graph has ω ≤ tw + 1. Split graphs: split iff the graph and its complement are chordal, iff no induced 2K₂, C₄ or C₅ (Földes–Hammer 1977). Threshold graphs: threshold iff no induced 2K₂, C₄ or P₄ (Chvátal–Hammer 1977), iff split and a cograph (no induced P₄). Mathlib has none of these graph classes; their definitions are stated in the Challenge.

**Sources.**

* G. A. Dirac, *On rigid circuit graphs*, Abhandlungen aus dem Mathematischen Seminar der Universität Hamburg 25 (1961), 71–76. [doi:10.1007/BF02992776](https://doi.org/10.1007/BF02992776)
* D. R. Fulkerson, O. A. Gross, *Incidence matrices and interval graphs*, Pacific Journal of Mathematics 15 (1965), 835–855. [doi:10.2140/pjm.1965.15.835](https://doi.org/10.2140/pjm.1965.15.835) · [free full text](http://msp.org/pjm/1965/15-3/pjm-v15-n3-p11-s.pdf)
* F. Gavril, *The intersection graphs of subtrees in trees are exactly the chordal graphs*, Journal of Combinatorial Theory, Series B 16 (1974), 47–56. [doi:10.1016/0095-8956(74)90094-X](https://doi.org/10.1016/0095-8956(74)90094-X) · [free full text](https://www.sciencedirect.com/science/article/pii/009589567490094X/pdf)
* S. Földes, P. L. Hammer, *Split graphs*, Proceedings of the 8th Southeastern Conference on Combinatorics, Graph Theory and Computing (1977), Congressus Numerantium XIX, 311–315.
* V. Chvátal, P. L. Hammer, *Aggregation of Inequalities in Integer Programming*, Annals of Discrete Mathematics 1 (1977), 145–162. [doi:10.1016/S0167-5060(08)70731-3](https://doi.org/10.1016/S0167-5060(08)70731-3)

<details><summary>Background references</summary>

* Reinhard Diestel, *Graph Theory*, Graduate Texts in Mathematics 173, 5th edition, Springer (2017), Chapter 12. [doi:10.1007/978-3-662-53622-3](https://doi.org/10.1007/978-3-662-53622-3)

</details>

[← Back to the list](../README.md)
