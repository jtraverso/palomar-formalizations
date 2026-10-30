# Edge colouring and list colouring: details

[← Back to the list](../README.md)

## Vizing's theorem and equitable edge colourings

Palomar: [PALOMAR-2026-10-15-000004](https://palomar-registry.org/entry.html?id=PALOMAR-2026-10-15-000004&version=2) (version 2) · code: [jtraverso/vizing @ 33b2de8](https://github.com/jtraverso/vizing/tree/33b2de836095cf92bc1dec33b6f8787e4036bbc6) · [archived copy](https://github.com/PalomarArchive/jtraverso--vizing--01fa5f875100/tree/palomar/PALOMAR-2026-10-15-000004-v2/33b2de836095cf92bc1dec33b6f8787e4036bbc6)

**What is proved.** A Lean 4 / Mathlib formalization of Vizing's theorem: every finite simple graph G has a proper edge colouring with Δ(G) + 1 colours, stated with Mathlib's line graph (G.lineGraph is (Δ(G) + 1)-colourable, hence χ'(G) ≤ Δ(G) + 1), proved with fans and Kempe chain exchanges. It also proves the equitable refinement: for every c ≥ Δ(G) + 1 there is a proper edge colouring with colours Fin c in which any two colour classes (including unused colours) differ in size by at most one (McDiarmid 1972), obtained by balancing a Vizing colouring with alternating-component moves that strictly decrease a square energy. Version 2 adds the lower bound Δ(G) ≤ χ'(G) (the edges at a vertex of maximum degree form a clique of the line graph) and hence the dichotomy χ'(G) ∈ {Δ(G), Δ(G) + 1} (class 1 / class 2).

**Sources.**

* Vadim G. Vizing, *On an estimate of the chromatic class of a p-graph (Russian)*, Diskretnyi Analiz 3 (1964), 25–30.
* Colin McDiarmid, *The Solution of a Timetabling Problem*, IMA Journal of Applied Mathematics 9 (1972), 23–34. [doi:10.1093/imamat/9.1.23](https://doi.org/10.1093/imamat/9.1.23)

<details><summary>Background references</summary>

* Dominique de Werra, *Equitable colorations of graphs*, Revue française d'informatique et de recherche opérationnelle, Série rouge 5 (1971), no. R3, 3–8. [doi:10.1051/m2an/197105r300031](https://doi.org/10.1051/m2an/197105r300031) · [free full text](https://www.esaim-m2an.org/articles/m2an/pdf/1971/03/m2an197105R300031.pdf)
* Juan Pablo Traverso Gianini, *Paper IV (Erdős problem #81 for chordal graphs), Lean formalization freeze*, https://github.com/jtraverso/erdos-81-chordal-clique-partitions at ff2019f56a50cf300a6531c9f8d4a8fb1a541e3d, preprints/PAPER_IV/05_formalization.

</details>

## Kőnig's theorems and Dilworth's theorem

Palomar: [PALOMAR-2026-10-15-000019](https://palomar-registry.org/entry.html?id=PALOMAR-2026-10-15-000019&version=1) (version 1) · code: [jtraverso/konig-edge-colouring @ 7c60f7e](https://github.com/jtraverso/konig-edge-colouring/tree/7c60f7efb69c1747aaf39e5dfa7a89d907cd84ef) · [archived copy](https://github.com/PalomarArchive/jtraverso--konig-edge-colouring--5e0f844003ab/tree/palomar/PALOMAR-2026-10-15-000019-v1/7c60f7efb69c1747aaf39e5dfa7a89d907cd84ef)

**What is proved.** A Lean 4 / Mathlib formalization of Kőnig's edge-colouring theorem: the line graph of a finite bipartite graph G is Δ(G)-colourable, and its chromatic number (the chromatic index of G) equals Δ(G). The proof colours edges one at a time with partial proper edge colourings, recolouring by an a/b Kempe-chain swap whose correctness rests on a parity argument in the bipartite graph; the lower bound comes from the edges at a vertex of maximum degree, which are pairwise adjacent in the line graph. Also formalized: the Kőnig–Egerváry theorem (a finite bipartite graph has a matching and a vertex cover of the same size, via Hall's theorem with deficiency, plus weak duality for all finite graphs), Dilworth's theorem (an antichain A and a partition into |A| chains, by Galvin's induction) and Mirsky's dual theorem (a chain C and a partition into |C| antichains, by the height function).

**Sources.**

* Dénes Kőnig, *Über Graphen und ihre Anwendung auf Determinantentheorie und Mengenlehre*, Mathematische Annalen 77 (1916), 453–465. [doi:10.1007/BF01456961](https://doi.org/10.1007/BF01456961) · [free full text](https://zenodo.org/record/2395248)
* Dénes Kőnig, *Gráfok és mátrixok*, Matematikai és Fizikai Lapok 38 (1931), 116–119.
* R. P. Dilworth, *A decomposition theorem for partially ordered sets*, Annals of Mathematics 51 (1950), 161–166. [doi:10.2307/1969503](https://doi.org/10.2307/1969503)
* L. Mirsky, *A dual of Dilworth's decomposition theorem*, American Mathematical Monthly 78 (1971), 876–877. [doi:10.1080/00029890.1971.11992886](https://doi.org/10.1080/00029890.1971.11992886)

<details><summary>Background references</summary>

* Fred Galvin, *A proof of Dilworth's chain decomposition theorem*, American Mathematical Monthly 101 (1994), 352–353. [doi:10.1080/00029890.1994.11996954](https://doi.org/10.1080/00029890.1994.11996954)

</details>

## Galvin's theorem for bipartite multigraphs, the Dinitz problem and stable matchings

Palomar: [PALOMAR-2026-10-18-000029](https://palomar-registry.org/entry.html?id=PALOMAR-2026-10-18-000029&version=2) (version 2) · code: [jtraverso/galvin-dinitz @ 84dcda4](https://github.com/jtraverso/galvin-dinitz/tree/84dcda4c2a760f2b52b7e813affe7e6968f8bfce) · [archived copy](https://github.com/PalomarArchive/jtraverso--galvin-dinitz--befd03f21f2b/tree/palomar/PALOMAR-2026-10-18-000029-v2/84dcda4c2a760f2b52b7e813affe7e6968f8bfce)

**What is proved.** A Lean 4 / Mathlib formalization of Galvin’s theorem for finite bipartite multigraphs: every assignment of finite edge lists of size at least the maximum incidence degree admits a proper edge coloring, with parallel edges counted separately. It includes ordinary edge coloring with Δ colors and the matching lower bound, and the Borodin–Kostochka–Woodall theorem for local lists (lists of size at least the larger degree of the two ends of each edge suffice). The previously registered simple-graph Galvin theorem, Dinitz problem and Gale–Shapley stable matching theorem are retained.

**Sources.**

* F. Galvin, *The List Chromatic Index of a Bipartite Multigraph*, Journal of Combinatorial Theory, Series B 63 (1995), 153–158. [doi:10.1006/jctb.1995.1011](https://doi.org/10.1006/jctb.1995.1011) · [free full text](https://doi.org/10.1006/jctb.1995.1011)
* O. V. Borodin, A. V. Kostochka, D. R. Woodall, *List Edge and List Total Colourings of Multigraphs*, Journal of Combinatorial Theory, Series B 71 (1997), 184–204. [doi:10.1006/jctb.1997.1780](https://doi.org/10.1006/jctb.1997.1780) · [free full text](https://doi.org/10.1006/jctb.1997.1780)
* D. Gale, L. S. Shapley, *College Admissions and the Stability of Marriage*, The American Mathematical Monthly 69 (1962), 9–15. [doi:10.1080/00029890.1962.11989827](https://doi.org/10.1080/00029890.1962.11989827)

## The list chromatic index of complete graphs (Häggkvist–Janssen)

Palomar: [PALOMAR-2026-10-15-000003](https://palomar-registry.org/entry.html?id=PALOMAR-2026-10-15-000003&version=1) (version 1) · code: [jtraverso/haggkvist-janssen @ 807e08b](https://github.com/jtraverso/haggkvist-janssen/tree/807e08bd7c480d4fae80c1b78377d23989d39ab0) · [archived copy](https://github.com/PalomarArchive/jtraverso--haggkvist-janssen--3449623606b5/tree/palomar/PALOMAR-2026-10-15-000003-v1/807e08bd7c480d4fae80c1b78377d23989d39ab0)

**What is proved.** A Lean 4 / Mathlib formalization of the Häggkvist–Janssen theorem χ′ₗ(Kₙ) ≤ n: for arbitrary lists of at least n colours on the edges of the complete graph on n vertices (from an arbitrary colour type), there is a proper edge colouring, i.e. a colouring of Mathlib's line graph of ⊤, choosing every colour from the list of its edge. Orders 0 and 1 are included. The proof constructs an explicit local-rank certificate, shows by a forced-choice induction that the corresponding coefficient of an extended-star polynomial is nonzero, and applies Mathlib's combinatorial Nullstellensatz; it is an alternative presentation, not a literal translation of the article's argument.

**Sources.**

* Roland Häggkvist, Jeannette C. M. Janssen, *New Bounds on the List-Chromatic Index of the Complete Graph and Other Simple Graphs*, Combinatorics, Probability and Computing 6 (1997), 295–313. [doi:10.1017/S0963548397002927](https://doi.org/10.1017/S0963548397002927)

<details><summary>Background references</summary>

* Noga Alon, *Combinatorial Nullstellensatz*, Combinatorics, Probability and Computing 8 (1999), 7–29.

</details>

## Wagner's planarity criterion and list colouring of planar and K₅-minor-free graphs

Palomar: [PALOMAR-2026-10-15-000005](https://palomar-registry.org/entry.html?id=PALOMAR-2026-10-15-000005&version=1) (version 1) · code: [jtraverso/planar-list-colouring @ ec1eafb](https://github.com/jtraverso/planar-list-colouring/tree/ec1eafbc091713857eb5683a46e460902b2d47b3) · [archived copy](https://github.com/PalomarArchive/jtraverso--planar-list-colouring--03a15f1929ab/tree/palomar/PALOMAR-2026-10-15-000005-v1/ec1eafbc091713857eb5683a46e460902b2d47b3)

**What is proved.** A Lean 4 / Mathlib formalization of classical results on planar graphs and graphs without a K5 minor. (1) Wagner's theorem (1937): a finite graph is planar if and only if it has neither K5 nor K3,3 as a minor. (2) Škrekovski's theorem (1998): every finite graph without a K5 minor is 5-choosable, proved along the route of Wood and Linusson, and Thomassen's theorem (1994) that every finite planar graph is 5-choosable, as a corollary. (3) DP-colouring: every finite graph without a K5 minor (Li–Wang, 2022), hence every finite planar graph (Dvořák–Postle, 2018), is DP-5-colourable. (4) Voigt's theorem (1993): an explicit planar graph on 238 vertices with lists of four colours has no proper list colouring, so 5 cannot be lowered to 4; its planarity and non-colourability are checked by kernel reduction. (5) Wagner's equivalence of the Four Colour Theorem with Hadwiger's conjecture for K5 (neither side is proved). Planarity is defined combinatorially, by rotation systems of genus zero (Euler defect 0); as sanity checks K4 is planar and K5, K3,3 are not.

**Sources.**

* Klaus Wagner, *Über eine Eigenschaft der ebenen Komplexe*, Mathematische Annalen 114 (1937), 570–590.
* Riste Škrekovski, *Choosability of K5-minor-free graphs*, Discrete Mathematics 190 (1998), 223–226. [doi:10.1016/S0012-365X(98)00158-7](https://doi.org/10.1016/S0012-365X(98)00158-7) · [free full text](https://www.sciencedirect.com/science/article/pii/S0012365X98001587/pdf)
* David R. Wood, Svante Linusson, *Thomassen's Choosability Argument Revisited*, SIAM Journal on Discrete Mathematics 24 (2010), no. 4, 1632–1637. [free full text](https://arxiv.org/pdf/1005.5194) (arXiv)
* Carsten Thomassen, *Every planar graph is 5-choosable*, Journal of Combinatorial Theory, Series B 62 (1994), 180–181.
* Zdeněk Dvořák, Luke Postle, *Correspondence coloring and its application to list-coloring planar graphs without cycles of lengths 4 to 8*, Journal of Combinatorial Theory, Series B 129 (2018), 38–54.
* Lingxi Li, Tao Wang, *An extension of Thomassen's result on choosability*, Applied Mathematics and Computation 425 (2022), 127100. [free full text](https://arxiv.org/pdf/2111.15220) (arXiv)
* Margit Voigt, *List colourings of planar graphs*, Discrete Mathematics 120 (1993), 215–219. [doi:10.1016/0012-365X(93)90579-I](https://doi.org/10.1016/0012-365X(93)90579-I) · [free full text](https://doi.org/10.1016/0012-365x(93)90579-i)

<details><summary>Background references</summary>

* Kazimierz Kuratowski, *Sur le problème des courbes gauches en topologie*, Fundamenta Mathematicae 15 (1930), 271–283.
* Jack Edmonds, *A combinatorial representation for polyhedral surfaces*, Notices of the American Mathematical Society 7 (1960), 646.

</details>

## The Alon–Tarsi theorem and 3-choosability of planar bipartite graphs

Palomar: [PALOMAR-2026-10-19-000013](https://palomar-registry.org/entry.html?id=PALOMAR-2026-10-19-000013&version=1) (version 1) · code: [jtraverso/alon-tarsi-choosability @ 4ab98b1](https://github.com/jtraverso/alon-tarsi-choosability/tree/4ab98b11f340ea2160b34d0b57ef7102452b98cc) · [archived copy](https://github.com/PalomarArchive/jtraverso--alon-tarsi-choosability--e8601c7736f7/tree/palomar/PALOMAR-2026-10-19-000013-v1/4ab98b11f340ea2160b34d0b57ef7102452b98cc)

**What is proved.** A Lean 4 / Mathlib formalization of the Alon–Tarsi theorem: if a finite simple graph has an orientation whose numbers of even and odd Eulerian subdigraphs differ, then it can be properly coloured from any lists larger than the out-degrees; and of its corollary that every finite planar bipartite graph is 3-choosable. Planarity is the combinatorial notion of a plane map (a rotation system of genus zero) of the registered entry PALOMAR-2026-10-15-000005, whose definitions are reproduced verbatim in the Challenge. The proof uses the graph polynomial and Mathlib's Combinatorial Nullstellensatz, Euler's formula for plane maps, and an out-degree-2 orientation obtained from Hall's theorem.

**Sources.**

* N. Alon, M. Tarsi, *Colorings and orientations of graphs*, Combinatorica 12 (1992), 125–134. [doi:10.1007/BF01204715](https://doi.org/10.1007/BF01204715)

<details><summary>Background references</summary>

* N. Alon, *Combinatorial Nullstellensatz*, Combinatorics, Probability and Computing 8 (1999), 7–29. [doi:10.1017/S0963548398003411](https://doi.org/10.1017/S0963548398003411)
* S. L. Hakimi, *On the degrees of the vertices of a directed graph*, Journal of the Franklin Institute 279 (1965), 290–308. [doi:10.1016/0016-0032(65)90340-6](https://doi.org/10.1016/0016-0032(65)90340-6)

</details>

## Thomassen: planar graphs of girth at least five are 3-choosable

Palomar: [PALOMAR-2026-10-28-000023](https://palomar-registry.org/entry.html?id=PALOMAR-2026-10-28-000023&version=1) (version 1) · code: [jtraverso/thomassen-girth-five @ 12765f3](https://github.com/jtraverso/thomassen-girth-five/tree/12765f3362b48fbae04ac467d33873a4f2234083) · [archived copy](https://github.com/PalomarArchive/jtraverso--thomassen-girth-five--a221bbfeb126/tree/palomar/PALOMAR-2026-10-28-000023-v1/12765f3362b48fbae04ac467d33873a4f2234083)

**What is proved.** Finite planar simple graphs of extended girth at least five are 3-choosable over arbitrary colour types. Includes a complete six-vertex boundary-extension induction, actual induced-face geometry and residual list-colouring infrastructure. Additional results expose the short-path theorem, derive an infinite finite-list compactness consequence, extend arbitrary five/six-cycles, and extend outer seven-cycles. The full original Theorem 2.1 and Corollary 2.2 are also proved, including arbitrary allowed fixed-edge colours and all exterior components.

**Sources.**

* Carsten Thomassen, *3-List-Coloring Planar Graphs of Girth 5*, Journal of Combinatorial Theory, Series B 64 (1995), 101–107. [doi:10.1006/jctb.1995.1027](https://doi.org/10.1006/jctb.1995.1027) · [free full text](https://doi.org/10.1006/jctb.1995.1027)
* Ligang Jin, Yingli Kang, Eckhard Steffen, *Choosability in signed planar graphs*, Appendix, Theorem 5.1, pp. 11–13. [free full text](https://arxiv.org/pdf/1502.04561) (arXiv)
* Daniel W. Cranston, *Graph Coloring Methods*, 2024, section 11.4, Theorem 11.13, printed pp. 322–328.
* Juan Pablo Traverso Gianini, *planar-list-colouring and grotzsch-ore registered Lean libraries*, jtraverso/planar-list-colouring at ec1eafbc091713857eb5683a46e460902b2d47b3; jtraverso/grotzsch-ore at ff6d5123c06e4c99bb6074e0a72e8be8d595eefa.
* Zdeněk Dvořák, Ken-ichi Kawarabayashi, *Choosability of planar graphs of girth 5*, 2011 preprint, Theorem 1 (attributed there to Thomassen). [free full text](https://arxiv.org/pdf/1109.2976) (arXiv)
* Richard Rado, *Axiomatic Treatment of Rank in Infinite Sets*, Canadian Journal of Mathematics 1 (1949), 337–343. [doi:10.4153/CJM-1949-031-1](https://doi.org/10.4153/CJM-1949-031-1) · [free full text](https://www.cambridge.org/core/services/aop-cambridge-core/content/view/93214C375DB3E3D1839423F445075EEB/S0008414X00037135a.pdf/div-class-title-axiomatic-treatment-of-rank-in-infinite-sets-div.pdf)
* N. G. de Bruijn, Paul Erdős, *A colour problem for infinite graphs and a problem in the theory of relations*, Proceedings KNAW, Series A 54 (1951), 371–373.
* Nabiha Asghar, *Grötzsch's Theorem*, University of Waterloo MMath research essay (2012), Lemma 3.2.3, seven-cycle specialization.

## The Pippenger–Spencer theorem on the chromatic index of hypergraphs

Palomar: [PALOMAR-2026-10-28-000018](https://palomar-registry.org/entry.html?id=PALOMAR-2026-10-28-000018&version=1) (version 1) · code: [jtraverso/pippenger-spencer @ 4cca4e3](https://github.com/jtraverso/pippenger-spencer/tree/4cca4e3c641619b1622ea60f58c57dc0c28ffdbb) · [archived copy](https://github.com/PalomarArchive/jtraverso--pippenger-spencer--aaba98952e76/tree/palomar/PALOMAR-2026-10-28-000018-v1/4cca4e3c641619b1622ea60f58c57dc0c28ffdbb)

**What is proved.** A Lean 4 / Mathlib formalization of the theorem of Pippenger and Spencer (1989): for r ≥ 2 and ε > 0 there are μ > 0 and D₀ such that every r-uniform hypergraph whose degrees lie in [(1 − μ)D, D] and whose codegrees are at most μD, with D ≥ D₀, has chromatic index at most (1 + ε)D. A second theorem gives an explicit polynomial error: if the maximum degree is at most D, the codegrees are at most D^{1−δ} and there are at most exp(D^γ) edges, then the chromatic index is at most D + D^{1−γ} for some γ = γ(r, δ) > 0. The proofs build on the author's registered formalization of Ehard–Glock–Joos (PALOMAR-2026-10-17-000004): batches of the trimmed Rödl nibble with the Lovász Local Lemma for the first theorem, and the pseudorandom matching theorem (Ehard–Glock–Joos, Theorem 1.2) applied to an auxiliary colour hypergraph for the second. Mathlib does not contain these results.

**Sources.**

* Nicholas Pippenger, Joel Spencer, *Asymptotic behavior of the chromatic index for hypergraphs*, Journal of Combinatorial Theory, Series A 51 (1989), 24–42. [doi:10.1016/0097-3165(89)90074-5](https://doi.org/10.1016/0097-3165(89)90074-5) · [free full text](https://doi.org/10.1016/0097-3165(89)90074-5)

<details><summary>Background references</summary>

* Stefan Ehard, Stefan Glock, Felix Joos, *Pseudorandom hypergraph matchings*, Combinatorics, Probability and Computing 29 (2020), 868–885; arXiv:1907.09946. [doi:10.1017/S0963548320000280](https://doi.org/10.1017/S0963548320000280) · [free full text](https://arxiv.org/pdf/1907.09946) (arXiv)

</details>

## Shannon's theorem on edge colourings of multigraphs

Palomar: [PALOMAR-2026-10-29-000023](https://palomar-registry.org/entry.html?id=PALOMAR-2026-10-29-000023&version=1) (version 1) · code: [jtraverso/shannon-edge-colouring @ d590cfe](https://github.com/jtraverso/shannon-edge-colouring/tree/d590cfeb50d88710b454905f896aab928fcb5156) · [archived copy](https://github.com/PalomarArchive/jtraverso--shannon-edge-colouring--7112faf48c4d/tree/palomar/PALOMAR-2026-10-29-000023-v1/d590cfeb50d88710b454905f896aab928fcb5156)

**What is proved.** A Lean 4 / Mathlib formalization of Shannon's theorem (1949): every finite loopless multigraph of maximum degree at most Δ has a proper edge colouring with ⌊3Δ/2⌋ colours; and its sharpness: for every Δ the Shannon triangle (three vertices with ⌊Δ/2⌋, ⌊Δ/2⌋ and ⌈Δ/2⌉ parallel edges between the three pairs) has maximum degree at most Δ and no proper edge colouring with fewer than ⌊3Δ/2⌋ colours. Multigraphs are edge families ends : ι → V × V (parallel edges allowed), a lighter representation than Mathlib's multigraph structure Graph α β (Mathlib.Combinatorics.Graph.Basic: vertex and edge sets with an incidence relation IsLink), which at the pinned revision has no degrees or edge colourings; no bridge to Graph α β is proved. Neither result is in Mathlib.

**Sources.**

* Claude E. Shannon, *A theorem on coloring the lines of a network*, Journal of Mathematics and Physics 28 (1949), 148–152. [doi:10.1002/sapm1949281148](https://doi.org/10.1002/sapm1949281148)

[← Back to the list](../README.md)
