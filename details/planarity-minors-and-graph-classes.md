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
