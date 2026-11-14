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

## Wagner's planarity criterion and list colouring of planar and K5-minor-free graphs

Palomar: [PALOMAR-2026-10-15-000005](https://palomar-registry.org/entry.html?id=PALOMAR-2026-10-15-000005&version=2) (version 2) · code: [jtraverso/planar-list-colouring @ 5b26212](https://github.com/jtraverso/planar-list-colouring/tree/5b262124ae6c99661cf1e75bd0351cc7faab80c5) · [archived copy](https://github.com/PalomarArchive/jtraverso--planar-list-colouring--03a15f1929ab/tree/palomar/PALOMAR-2026-10-15-000005-v2/5b262124ae6c99661cf1e75bd0351cc7faab80c5)

**What is proved.** A Lean 4 / Mathlib formalization of classical results on planar graphs and graphs without a K5 minor. (1) Wagner's theorem (1937): a finite graph is planar if and only if it has neither K5 nor K3,3 as a minor. (2) Škrekovski's theorem (1998): every finite graph without a K5 minor is 5-choosable, proved along the route of Wood and Linusson, and Thomassen's theorem (1994) that every finite planar graph is 5-choosable, as a corollary. (3) DP-colouring: every finite graph without a K5 minor (Li–Wang, 2022), hence every finite planar graph (Dvořák–Postle, 2018), is DP-5-colourable. (4) Voigt's theorem (1993): an explicit planar graph on 238 vertices with lists of four colours has no proper list colouring, so 5 cannot be lowered to 4; its planarity and non-colourability are checked by kernel reduction. (5) Wagner's equivalence of the Four Colour Theorem with Hadwiger's conjecture for K5 (neither side is proved). (6) Wagner's structure theorem (1937, added in version 2): a finite graph has no K5 minor if and only if it is a spanning subgraph of a graph obtained by clique-sums of order at most three, keeping the clique edges, from planar graphs and copies of the Wagner graph V8. Planarity is defined combinatorially, by rotation systems of genus zero (Euler defect 0); as sanity checks K4 is planar and K5, K3,3 are not.

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

## Balanced edge colourings: Balister–Kostochka–Li–Schelp 2004, Theorems 1, 6, 10(2) and Corollary 12

Palomar: [PALOMAR-2026-11-06-000002](https://palomar-registry.org/entry.html?id=PALOMAR-2026-11-06-000002&version=1) (version 1) · code: [jtraverso/balanced-edge-colourings @ 736c78e](https://github.com/jtraverso/balanced-edge-colourings/tree/736c78e6addcdb77e95cd83e4e44c5c0700f13ef) · [archived copy](https://github.com/PalomarArchive/jtraverso--balanced-edge-colourings--a527efb7f56f/tree/palomar/PALOMAR-2026-11-06-000002-v1/736c78e6addcdb77e95cd83e4e44c5c0700f13ef)

**What is proved.** A Lean 4 / Mathlib formalization of four results of P. N. Balister, A. V. Kostochka, H. Li and R. H. Schelp, Balanced edge colorings (J. Combin. Theory Ser. B 90, 2004). Edge colourings with k colours are colourings of the line graph with Fin k; the palette of a vertex is the set of colours of its edges; numPal C S counts the vertices with palette S and cost C is the sum of the squares of these counts. theorem1 (Theorem 1): in a k-colouring of least cost, palettes of the same size are used numbers of times differing by at most two. theorem6 (Theorem 6): a proper 3-colouring of the edges (a map Sym2 V → Fin 3 proper at every vertex) can be replaced by a proper 4-colouring in which distinct vertices with the same key see different colour sets, when two distinct vertices with equal key, degree and colour set have degree 3 and no three distinct vertices of degree 3 share a key. theorem10 (Theorem 10, part 2): if 3 ≤ k, Δ(G) ≤ k, n_0, n_1, n_2 ≤ 1, n_3, n_4, n_k ≤ 2, n_{k-1} ≤ k + 1 and n_d ≤ (d-4)/(d-3) · min(2 C(k-3, d-3), C(k, d)) - 2 for 5 ≤ d ≤ k - 2 (n_d the number of vertices of degree d), then G has a strong (vertex-distinguishing) edge colouring with k + 1 colours. corollary12 (Corollary 12): if Δ(G) ≥ √(2n) + 4 (n vertices), δ(G) ≥ 5 and k is least with n_d ≤ C(k, d) for all d, then G has a strong edge colouring with k + 1 colours and every strong edge colouring uses at least k colours. Four statements.

**Sources.**

* P. N. Balister, A. V. Kostochka, Hao Li, R. H. Schelp, *Balanced edge colorings*, Journal of Combinatorial Theory, Series B 90 (2004), 3–20: Theorem 1, Theorem 6, Theorem 10 (part 2), Corollary 12. [doi:10.1016/S0095-8956(03)00073-X](https://doi.org/10.1016/S0095-8956(03)00073-X) · [free full text](https://www.sciencedirect.com/science/article/pii/S009589560300073X/pdf)

## Equitable strong (vertex-distinguishing) edge colourings: Rudašová–Soták, Theorem 3.1

Palomar: [PALOMAR-2026-11-05-000001](https://palomar-registry.org/entry.html?id=PALOMAR-2026-11-05-000001&version=1) (version 1) · code: [jtraverso/rudasova-sotak-equitable-strong @ 57535a7](https://github.com/jtraverso/rudasova-sotak-equitable-strong/tree/57535a7c821a3186349a815482b5e3a4b987d9d6) · [archived copy](https://github.com/PalomarArchive/jtraverso--rudasova-sotak-equitable-strong--3f0f0beea131/tree/palomar/PALOMAR-2026-11-05-000001-v1/57535a7c821a3186349a815482b5e3a4b987d9d6)

**What is proved.** A Lean 4 / Mathlib formalization of Theorem 3.1 of J. Rudašová and R. Soták, Vertex-distinguishing proper edge colourings of some regular graphs (Discrete Math. 308, 2008). exists_equitable_strong: if a finite simple graph G has a strong (vertex-distinguishing) proper edge colouring with m colours and m ≤ k, then G has an equitable strong proper edge colouring with k colours. One statement. Edge colourings are colourings of the line graph; the palette of a vertex is the set of colours of its edges; strong means distinct vertices have distinct palettes; equitable means the colour classes differ in size by at most one.

**Sources.**

* Janka Rudašová, Roman Soták, *Vertex-distinguishing proper edge colourings of some regular graphs*, Discrete Mathematics 308 (2008), 795–802: Theorem 3.1. [doi:10.1016/j.disc.2007.07.019](https://doi.org/10.1016/j.disc.2007.07.019) · [free full text](https://www.sciencedirect.com/science/article/pii/S0012365X07005237/pdf)

## Overfullness of critical graphs with small minimum degree (Cao–Chen–Jing–Shan; Chen–Cao)

Palomar: [PALOMAR-2026-11-04-000009](https://palomar-registry.org/entry.html?id=PALOMAR-2026-11-04-000009&version=2) (version 2) · code: [jtraverso/overfull-critical-graphs @ b85da9a](https://github.com/jtraverso/overfull-critical-graphs/tree/b85da9ac66e0fb8b9873a8bea0c057f78c9d186c) · [archived copy](https://github.com/PalomarArchive/jtraverso--overfull-critical-graphs--d8fd3a0c3ee4/tree/palomar/PALOMAR-2026-11-04-000009-v2/b85da9ac66e0fb8b9873a8bea0c057f78c9d186c)

**What is proved.** A Lean 4 / Mathlib formalization of Theorem 1.2 of Cao, Chen, Jing and Shan with a weaker constant. overfull_of_critical: if a finite simple graph G is Δ-critical (connected, its line graph is not Δ(G)-colourable, and G − e is Δ(G)-edge-colourable for every edge e) and 3|V(G)| + 7δ(G) ≤ 4Δ(G) + 10, then G is overfull: |E(G)| > Δ(G)·⌊|V(G)|/2⌋. The article assumes 4Δ − 7δ ≥ 3n − 17; the hypothesis here is 4Δ − 7δ ≥ 3n − 10, stronger by 7, because two common-neighbour counts in the article's proof (Case 2 of Section 3 and the fork branch of Case 1) use one more unit of degree than is available and are short by 2 under the article's constant. With the constant −10 every count closes, and the proof needs neither n ≥ 13 nor the Chetwynd–Hilton theorem for Δ ≥ n − 3. One statement. The proof includes the lemmas the article imports: Vizing's adjacency lemma, the multifan lemma, Kierstead paths on four vertices, the fork lemma of Cao and Chen, the short-kite lemma of Cao, Chen and Shan, and the kite lemma (Lemma 2.8, in the form used by Theorem 1.2), with proofs written from scratch where the article only cites them. Version 2 adds two statements. overfull_of_critical_cc: Theorem 1.3 of Chen and Cao (arXiv:2512.07252) with a weaker constant: a Δ-critical graph with 2|V(G)| + 5δ(G) ≤ 3Δ(G) + 6 is overfull (the article assumes 3Δ ≥ 2n + 5δ − 12; the constant −6 comes from counting common neighbours of three vertices without the article's refinements). overfull_of_critical_ccjs: CCJS Theorem 1.2 with its original constant: a Δ-critical graph with 4Δ − 7δ ≥ 3n − 17 and n + δ ≥ 27 is overfull (then 3Δ ≥ 2n + 5δ − 6). Three statements.

**Sources.**

* Yan Cao, Guantao Chen, Guangming Jing, Songling Shan, *The overfullness of graphs with small minimum degree and large maximum degree*, SIAM Journal on Discrete Mathematics 36 (2022), 2258–2270; arXiv:2105.05333v1: Theorem 1.2, Lemmas 2.1–2.8, 3.1, 4.1, Section 3 (proof of Theorem 1.2) and Section 4 (proof of Lemma 2.8). [free full text](https://arxiv.org/pdf/2105.05333) (arXiv)
* Yonglei Chen, Yan Cao, *Short brooms in edge-chromatic critical graphs*, arXiv:2512.07252v2: Theorem 1.3, Lemma 3.1, Lemma 4.2 and Section 4. [free full text](https://arxiv.org/pdf/2512.07252) (arXiv)
* Yan Cao, Guantao Chen, *On the average degree of edge chromatic critical graphs II*, Journal of Combinatorial Theory, Series B 145 (2020), 470–486: Proposition B and Claims 5.6–5.10.
* Yan Cao, Guantao Chen, Songling Shan, *An improvement to the vertex-splitting conjecture*, arXiv:2103.05171 (the short-kite lemma, CCJS Lemma 2.7). [free full text](https://arxiv.org/pdf/2103.05171) (arXiv)
* H. A. Kierstead, *On the chromatic index of multigraphs without large triangles*, Journal of Combinatorial Theory, Series B 36 (1984): Lemma 2; with the observation of L. Zhang, Graphs and Combinatorics 16 (2000), for Δ colours.
* V. G. Vizing, *Critical graphs with given chromatic class*, Diskretnyi Analiz 5 (1965), 9–17 (in Russian): Vizing's adjacency lemma (CCJS Lemma 2.1).

<details><summary>Background references</summary>

* Michael Stiebitz, Diego Scheide, Bjarne Toft, Lene M. Favrholdt, *Graph Edge Coloring: Vizing's Theorem and Goldberg's Conjecture*, Wiley, 2012: Theorem 2.1 (multifans) and Theorem 3.3 (Kierstead paths), cited by CCJS as Lemmas 2.2 and 2.4.

</details>

## Plantholt's overfull criterion for graphs of high minimum degree, with 1-factorization theorems for dense regular graphs (6/7 and 11/12)

Palomar: [PALOMAR-2026-11-04-000016](https://palomar-registry.org/entry.html?id=PALOMAR-2026-11-04-000016&version=2) (version 2) · code: [jtraverso/plantholt-overfull-criterion @ f890094](https://github.com/jtraverso/plantholt-overfull-criterion/tree/f8900944da7743b1facd771139c9ebdbfd8aaa28) · [archived copy](https://github.com/PalomarArchive/jtraverso--plantholt-overfull-criterion--d61ff43b5134/tree/palomar/PALOMAR-2026-11-04-000016-v2/f8900944da7743b1facd771139c9ebdbfd8aaa28)

**What is proved.** A Lean 4 / Mathlib formalization of Theorem 1.2 of M. Plantholt, Overfull conjecture for graphs with high minimum degree (J. Graph Theory 47, 2004), and of a 1-factorization theorem for dense regular graphs in the style of Chetwynd and Hilton (1989). theorem_1_2: if c ≥ 3/4 is such that every regular graph of even order n and degree at least c n is 1-factorizable, and G has even order n with (3δ − Δ)/2 ≥ c n, then G is Class 1 (χ′ = Δ) if and only if G has no Δ-overfull subgraph. lineGraph_colorable_of_isRegular: a d-regular graph of even order 2n with 11 n ≤ 6 d is d-edge-colourable, i.e. 1-factorizable; this is a weaker form of Chetwynd–Hilton 1989, Theorem 2 (d ≥ ½(√7 − 1)|V|), proved with the same architecture. overfull_criterion: Plantholt's theorem with c = 11/12, i.e. if G has even order n and 11 n ≤ 6 (3δ − Δ), then G is Class 1 if and only if it has no Δ-overfull subgraph. lineGraph_colorable_of_isRegular67: the theorem of Chetwynd and Hilton (Proc. London Math. Soc. 50, 1985) that a d-regular graph of even order 2n with 12 n ≤ 7 d (degree at least 6/7 of the order) is 1-factorizable. overfull_criterion67: Plantholt's theorem with c = 6/7, i.e. even order n and 12 n ≤ 7 (3δ − Δ). Five statements. A Δ-overfull subgraph has an odd number ≥ 3 of vertices and more than Δ ⌊|V(H)|/2⌋ edges; edge colourings are colourings of the line graph.

**Sources.**

* Michael J. Plantholt, *Overfull conjecture for graphs with high minimum degree*, Journal of Graph Theory 47 (2004), 73–80: Theorem 1.2, Lemma 2.1. [doi:10.1002/jgt.20013](https://doi.org/10.1002/jgt.20013)
* A. G. Chetwynd, A. J. W. Hilton, *Regular graphs of high degree are 1-factorizable*, Proceedings of the London Mathematical Society (3) 50 (1985), 193–206: the theorem for d ≥ (6/7)|V(G)|. [doi:10.1112/plms/s3-50.2.193](https://doi.org/10.1112/plms/s3-50.2.193)
* A. G. Chetwynd, A. J. W. Hilton, *1-factorizing regular graphs of high degree—an improved bound*, Discrete Mathematics 75 (1989), 103–112: §§2–4 (Lemma 1, Lemma 2, Theorems 4–5, proof of Theorem 1). [doi:10.1016/0012-365X(89)90082-4](https://doi.org/10.1016/0012-365X(89)90082-4) · [free full text](https://doi.org/10.1016/0012-365x(89)90082-4)

## Thomassen: exponentially many 5-list-colourings of planar graphs

Palomar: [PALOMAR-2026-11-07-000009](https://palomar-registry.org/entry.html?id=PALOMAR-2026-11-07-000009&version=1) (version 1) · code: [jtraverso/thomassen-many-list-colourings @ 109f88e](https://github.com/jtraverso/thomassen-many-list-colourings/tree/109f88ec9084d00e523bbc7fc558faa86428da52) · [archived copy](https://github.com/PalomarArchive/jtraverso--thomassen-many-list-colourings--2e1f89cb92de/tree/palomar/PALOMAR-2026-11-07-000009-v1/109f88ec9084d00e523bbc7fc558faa86428da52)

**What is proved.** A Lean 4 / Mathlib formalization of C. Thomassen, Exponentially many 5-list-colorings of planar graphs (J. Combin. Theory Ser. B 97, 2007): a finite planar graph with n vertices, every vertex of which has a list of at least five colours, has at least 2^{n/9} distinct list colourings (two_rpow_card_div_nine_le_ncard_listColourings: (2 : ℝ) ^ (n / 9) ≤ the number of maps f : V → C with f v ∈ L v and f u ≠ f v on every edge). Planarity is combinatorial: a plane map is a rotation system whose hypermap with the dart reversal has Euler defect 0 (definitions copied verbatim from the registered entry thomassen-girth-five, PALOMAR-2026-10-28-000023, so that the Challenge depends on Mathlib only). The proof follows the paper: Theorems 1–4, Claims 8–13 and the lemmas on generalized wheels they use are proved for an abstract interface of near-triangulations, which is realised by plane near-triangulations using the separation theorems of the dependency; every planar graph is a spanning subgraph of a plane near-triangulation. One statement; the definitions of the Challenge are compared with those of the Solution.

**Sources.**

* Carsten Thomassen, *Exponentially many 5-list-colorings of planar graphs*, Journal of Combinatorial Theory, Series B 97 (2007), 571–583; the main result (abstract and Section 6), with Theorems 1–4, Lemmas 1, 3, 4, 5 and Claims 8–13. [doi:10.1016/j.jctb.2006.09.002](https://doi.org/10.1016/j.jctb.2006.09.002) · [free full text](https://www.sciencedirect.com/science/article/pii/S0095895606001055/pdf)

<details><summary>Background references</summary>

* Rikke Langhede, Carsten Thomassen, *Exponentially many Z5-colorings in simple planar graphs*, arXiv:2011.12163. [free full text](https://arxiv.org/pdf/2011.12163) (arXiv)
* Carsten Thomassen, *Every planar graph is 5-choosable*, Journal of Combinatorial Theory, Series B 62 (1994), 180–181. [doi:10.1006/jctb.1994.1062](https://doi.org/10.1006/jctb.1994.1062) · [free full text](https://doi.org/10.1006/jctb.1994.1062)

</details>

## Overfull criteria for edge colouring (Plantholt; Chen–Cao; Cao–Chen–Jing–Shan), unified

Palomar: [PALOMAR-2026-11-08-000004](https://palomar-registry.org/entry.html?id=PALOMAR-2026-11-08-000004&version=1) (version 1) · code: [jtraverso/overfull-criteria @ 2af917d](https://github.com/jtraverso/overfull-criteria/tree/2af917da6f41ebf2275c4ee4b21d5861e02fac49) · [archived copy](https://github.com/PalomarArchive/jtraverso--overfull-criteria--2e39e1179caf/tree/palomar/PALOMAR-2026-11-08-000004-v1/2af917da6f41ebf2275c4ee4b21d5861e02fac49)

**What is proved.** A thin wrapper that restates, in one vocabulary and with Mathlib definitions only, the overfull criteria proved in PALOMAR-2026-11-04-000016 and PALOMAR-2026-11-04-000009. class_two_iff_overfull_subgraph: a finite simple graph of even order n with 12 n ≤ 7 (3δ − Δ) is of class two (its line graph is not Δ-colourable) iff it has a Δ-overfull subgraph (odd order at least 3, more than Δ (|V(H)| − 1)/2 edges); this is Plantholt's criterion with Chetwynd–Hilton's 6/7. critical_overfull: a Δ-critical graph (connected, class two, every edge-deleted subgraph Δ-colourable) with 2n + 5δ ≤ 3Δ + 6 (Chen–Cao), or 3n + 7δ ≤ 4Δ + 10 (Cao–Chen–Jing–Shan, variant), or 3n + 7δ ≤ 4Δ + 17 and n + δ ≥ 27 (Cao–Chen–Jing–Shan) has odd order, is overfull (|E| > Δ ⌊n/2⌋), and so is a Δ-overfull subgraph of itself. The only new proof is the elementary step from overfullness to odd order at least 3 (degree sum) and the conversion to the subgraph form. Two statements; no definitions beyond Mathlib's.

**Sources.**

* Michael J. Plantholt, *Overfull conjecture for graphs with high minimum degree*, Journal of Graph Theory 47 (2004), 73–80: Theorem 1.2. [doi:10.1002/jgt.20013](https://doi.org/10.1002/jgt.20013)
* Yan Cao, Guantao Chen, Guangming Jing, Songling Shan, *The overfullness of graphs with small minimum degree and large maximum degree*, SIAM Journal on Discrete Mathematics 36 (2022), 2258–2270: Theorem 1.2. [free full text](https://arxiv.org/pdf/2105.05333) (arXiv)
* Yonglei Chen, Yan Cao, *Short brooms in edge-chromatic critical graphs*, arXiv:2512.07252v2: Theorem 1.3. [free full text](https://arxiv.org/pdf/2512.07252) (arXiv)

## Walecki's decompositions of complete graphs into Hamiltonian cycles and paths

Palomar: [PALOMAR-2026-11-08-000007](https://palomar-registry.org/entry.html?id=PALOMAR-2026-11-08-000007&version=1) (version 1) · code: [jtraverso/walecki-decompositions @ 5e8a6ea](https://github.com/jtraverso/walecki-decompositions/tree/5e8a6eab7b0c8dacc4eb41b5c480bb90ed449a0e) · [archived copy](https://github.com/PalomarArchive/jtraverso--walecki-decompositions--15ec67c941b9/tree/palomar/PALOMAR-2026-11-08-000007-v1/5e8a6eab7b0c8dacc4eb41b5c480bb90ed449a0e)

**What is proved.** A Lean 4 / Mathlib proof of Walecki's theorem: for every m, the complete graph on 2m + 1 vertices is the edge-disjoint union of m Hamiltonian cycles (hamiltonian_cycles_odd), and the complete graph on 2m vertices is the edge-disjoint union of m Hamiltonian paths (hamiltonian_paths_even). Both are stated for an arbitrary finite vertex type of the given cardinality, with Mathlib's Walk.IsHamiltonianCycle and Walk.IsHamiltonian, pairwise disjoint edge lists, and every edge of the complete graph on some cycle (path). The proof is Walecki's zig-zag construction: on ZMod (2m) the paths i, i+1, i−1, i+2, i−2, …, i+m (0 ≤ i < m) are Hamiltonian; an edge {x, y} of the i-th path has x + y ∈ {2i, 2i+1}, which makes the paths edge-disjoint, and m (2m − 1) = C(2m, 2) shows that they cover all edges; closing each path through a new vertex gives the cycles. Two statements; no definitions beyond Mathlib's.

**Sources.**

* Édouard Lucas, *Récréations mathématiques, tome II*, Gauthier-Villars, Paris, 1883: the decomposition of the complete graph into Hamiltonian cycles, credited by Lucas to Walecki.

<details><summary>Background references</summary>

* Brian Alspach, *The wonderful Walecki construction*, Bulletin of the Institute of Combinatorics and its Applications 52 (2008), 7–20.

</details>

## Fournier's theorem: graphs whose maximum-degree vertices induce a forest are of class one

Palomar: [PALOMAR-2026-11-08-000009](https://palomar-registry.org/entry.html?id=PALOMAR-2026-11-08-000009&version=1) (version 1) · code: [jtraverso/fournier-class-one @ b7baf7b](https://github.com/jtraverso/fournier-class-one/tree/b7baf7b17023d2a2a6dd9650c0706fcabb3bc227) · [archived copy](https://github.com/PalomarArchive/jtraverso--fournier-class-one--5f73bebe9b0a/tree/palomar/PALOMAR-2026-11-08-000009-v1/b7baf7b17023d2a2a6dd9650c0706fcabb3bc227)

**What is proved.** A Lean 4 / Mathlib proof of Fournier's theorem (1973): if the vertices of maximum degree of a finite simple graph G induce a forest, then G has a proper edge colouring with Δ(G) colours (fournier: G.lineGraph.Colorable G.maxDegree under (G.induce {v | G.degree v = G.maxDegree}).IsAcyclic). The proof takes an edge-minimal subgraph H of G that is not Δ(G)-edge-colourable; Vizing's theorem gives Δ(H) = Δ(G), and Vizing's adjacency lemma applied to every edge xy of H gives a neighbour of x of maximum degree other than y, so the maximum-degree vertices of H span a subgraph of minimum degree at least 2 inside the forest, which is impossible (the end of a longest path). Vizing's theorem and the adjacency lemma are imported as lake dependencies from PALOMAR-2026-10-15-000004 and PALOMAR-2026-11-04-000009. One statement; no definitions beyond Mathlib's.

**Sources.**

* Jean-Claude Fournier, *Colorations des arêtes d'un graphe*, Cahiers du Centre d'Études de Recherche Opérationnelle 15 (1973), 311–314.

<details><summary>Background references</summary>

* Michael Stiebitz, Diego Scheide, Bjarne Toft, Lene M. Favrholdt, *Graph Edge Coloring: Vizing's Theorem and Goldberg's Conjecture*, Wiley, 2012: Vizing's adjacency lemma and its corollaries for critical graphs. [doi:10.1002/9781118205587](https://doi.org/10.1002/9781118205587)

</details>

## Chetwynd–Hilton 1989: regular graphs of degree at least ½(√7 − 1)|V| are 1-factorizable

Palomar: [PALOMAR-2026-11-12-000006](https://palomar-registry.org/entry.html?id=PALOMAR-2026-11-12-000006&version=1) (version 1) · code: [jtraverso/chetwynd-hilton-1989 @ 0f6e485](https://github.com/jtraverso/chetwynd-hilton-1989/tree/0f6e485529e810843ea13814d19c8d67b15568b9) · [archived copy](https://github.com/PalomarArchive/jtraverso--chetwynd-hilton-1989--88e35be60ebe/tree/palomar/PALOMAR-2026-11-12-000006-v1/0f6e485529e810843ea13814d19c8d67b15568b9)

**What is proved.** A Lean 4 / Mathlib proof of Theorem 2 of Chetwynd and Hilton, "1-factorizing regular graphs of high degree — an improved bound" (Discrete Math. 75 (1989)): a d-regular simple graph of even order with d ≥ ½(√7 − 1)|V| (≈ 0.823|V|) is d-edge-colourable (CH89.lineGraph_colorable_of_isRegular_sqrt7), with the integer form |V| = 2n, 7n² ≤ (d + n)² (CH89.lineGraph_colorable_of_isRegular_nat). The article's proof of Theorem 1 contains an unjustified step ("we may moreover suppose that x_j comes before w_j in the list (r_m, …, r_t, l_1, …, l_m)"), which fails for an arbitrary maximal matching M₀; the formalization repairs it by choosing M₀ to minimize −K·#covered + max(T, T′), T = u_Y − u_X − μ, ordering the edges of M₀ (mixed ones outside, XX/YY alternately) and pairing X with Y by Hall's theorem with one dummy, so that at most one pair is bad, which the article's extra step q + 1 absorbs. The constant ½(√7 − 1) of the article is obtained exactly. Theorem 1 (staircase classes peeled off as near 1-factors, core of Theorem 5, re-insertion of v* and w) is assembled from the pinned dependency PALOMAR-2026-11-04-000016; Lemma 3 (a pair with r(r − 1) ≤ (2n − 1)p common non-neighbours) and the parameter inequality r(r − 1) − (2n − 1)(5n − 3d − 1) = (d + n)² − 7n² + n + 1 are proved here. Two statements; no definitions beyond Mathlib's.

**Sources.**

* A. G. Chetwynd, A. J. W. Hilton, *1-factorizing regular graphs of high degree — an improved bound*, Discrete Mathematics 75 (1989), 103–112: Theorems 1 and 2, Lemma 3. [doi:10.1016/0012-365X(89)90082-4](https://doi.org/10.1016/0012-365X(89)90082-4) · [free full text](https://doi.org/10.1016/0012-365x(89)90082-4)

## Graphs whose core has maximum degree two: Hilton–Zhao structure and the Cariolaro–Cariolaro theorem

Palomar: [PALOMAR-2026-11-12-000007](https://palomar-registry.org/entry.html?id=PALOMAR-2026-11-12-000007&version=1) (version 1) · code: [jtraverso/hilton-zhao-cariolaro @ 9cc9a2c](https://github.com/jtraverso/hilton-zhao-cariolaro/tree/9cc9a2c48913f6a8feeb266416ea6517f52eed51) · [archived copy](https://github.com/PalomarArchive/jtraverso--hilton-zhao-cariolaro--88e275c68991/tree/palomar/PALOMAR-2026-11-12-000007-v1/9cc9a2c48913f6a8feeb266416ea6517f52eed51)

**What is proved.** A Lean 4 / Mathlib formalization of results on finite simple graphs G whose core (the vertices of maximum degree Δ) has maximum degree at most two, stated as: every vertex of degree Δ has at most two neighbours of degree Δ. Hilton–Zhao (1992): if G is connected and not Δ-edge-colourable, then G − e is Δ-edge-colourable for every edge e, every vertex has at least two neighbours of degree Δ (so the core is 2-regular), and every vertex has degree at least Δ − 1, with equality somewhere when Δ ≥ 3 (hiltonZhao_critical, hiltonZhao_two_le, hiltonZhao_core_regular, hiltonZhao_min_degree, hiltonZhao_min_degree_eq); corollaries: class one when some vertex of degree Δ has at most one neighbour of degree Δ, or some vertex has degree at most Δ − 2. For Δ = 3: a connected class-two graph is a petal graph (Cariolaro–Cariolaro Lemma 3: degrees 2 or 3, the degree-3 vertices induce a 2-regular graph, degree-2 vertices have only degree-3 neighbours) and 3|E| = 4|V|; and if some component of the core carries no internal petal (no vertex of degree below 3 adjacent to two of its vertices) then G is 3-edge-colourable (Cariolaro–Cariolaro Lemma 7, for a single core cycle). The graph P* (Petersen minus a vertex) is defined on Fin 9, proved isomorphic to the Petersen graph minus a vertex, and shown to satisfy the hypotheses, to be connected, of class two and not overfull. Cariolaro–Cariolaro (2003): a connected graph with Δ = 3 whose core has maximum degree at most two is not 3-edge-colourable if and only if it is isomorphic to P* (cariolaro_iff, cariolaro). The proof recolours one core cycle with its petals in a colouring of G − e (criticality): a combinatorial chorded-cycle lemma (a cyclic sequence of vertices with chords and external restrictions has a proper 3-edge-colouring whose missing colours differ along chords and avoid the restrictions, unless it is the hexagon with three antipodal chords or a chordless odd cycle with constant restrictions) proved by induction with safe local reductions; the arc reduction rests on a finite automaton whose reachable states are checked by decide. Vizing's theorem and Vizing's adjacency lemma are lake dependencies on PALOMAR-2026-10-15-000004 and PALOMAR-2026-11-04-000009; Kempe chains and their end-point lemma come from the former.

**Sources.**

* Anthony J. W. Hilton, Cheng Zhao, *The chromatic index of a graph whose core has maximum degree two*, Discrete Mathematics 101 (1992), 135–147.
* David Cariolaro, Gianfranco Cariolaro, *Colouring the petals of a graph*, Electronic Journal of Combinatorics 10 (2003), #R6.

<details><summary>Background references</summary>

* Anthony J. W. Hilton, Cheng Zhao, *On the edge-colouring of graphs whose core has maximum degree two*, J. Combin. Math. Combin. Comput. 21 (1996), 97–108.
* Daniel W. Cranston, Landon Rabern, *The Hilton–Zhao conjecture is true for graphs with maximum degree 4*, SIAM J. Discrete Math. 33 (2019); Lemma 1. [free full text](https://arxiv.org/pdf/1703.00959) (arXiv)

</details>

## Erdős–Wilson: almost every graph is of class one

Palomar: [PALOMAR-2026-11-12-000008](https://palomar-registry.org/entry.html?id=PALOMAR-2026-11-12-000008&version=1) (version 1) · code: [jtraverso/erdos-wilson-class-one @ e24f896](https://github.com/jtraverso/erdos-wilson-class-one/tree/e24f896005a8678e16ac1c7ac943184fdda6d852) · [archived copy](https://github.com/PalomarArchive/jtraverso--erdos-wilson-class-one--4c8ce3683ee9/tree/palomar/PALOMAR-2026-11-12-000008-v1/e24f896005a8678e16ac1c7ac943184fdda6d852)

**What is proved.** A Lean 4 / Mathlib proof of the theorem of Erdős and Wilson (1977) that almost every graph is of class one: among the 2^C(n,2) labelled graphs on Fin n, the proportion whose line graph is Δ(G)-colourable tends to 1 (erdos_wilson). On the way it proves that almost every graph has a unique vertex of maximum degree (tendsto_unique_maxDegree) and that a graph with at most one vertex of maximum degree is of class one (colorable_of_subsingleton_maxDegree, the special case of Fournier's theorem imported from PALOMAR-2026-11-08-000009). The probabilistic part is a second-moment argument with explicit binomial estimates: with X the number of vertices of degree at least a threshold k, P(X = 0) ≤ 1/(n tl_k) + bp_{k-1}^2/(4 tl_k^2) and P(two distinct vertices of equal degree ≥ k) ≤ n^2 Σ_{i ≥ k-1} bp_i^2, where bp, tl are the point probabilities and upper tails of Bin(n-2, 1/2); the joint law of two degrees is computed exactly by a symmetric-difference (translation) argument on the set of graphs, and k is chosen adaptively. Only qualitative statements (limits) are stated; no rate of convergence is claimed. Three statements; no definitions beyond Mathlib's.

**Sources.**

* Paul Erdős, Robin J. Wilson, *On the chromatic index of almost all graphs*, Journal of Combinatorial Theory, Series B 23 (1977), no. 2-3, 255–257. [doi:10.1016/0095-8956(77)90039-9](https://doi.org/10.1016/0095-8956(77)90039-9) · [free full text](https://doi.org/10.1016/0095-8956(77)90039-9)

## Vizing's adjacency lemma, the multifan lemma and Kierstead's lemma, as a standalone module

Palomar: [PALOMAR-2026-11-12-000012](https://palomar-registry.org/entry.html?id=PALOMAR-2026-11-12-000012&version=1) (version 1) · code: [jtraverso/vizing-adjacency-lemmas @ ef2c05c](https://github.com/jtraverso/vizing-adjacency-lemmas/tree/ef2c05cff377f965f9274b578b96133bf42b52af) · [archived copy](https://github.com/PalomarArchive/jtraverso--vizing-adjacency-lemmas--9a689d4f8f8e/tree/palomar/PALOMAR-2026-11-12-000012-v1/ef2c05cff377f965f9274b578b96133bf42b52af)

**What is proved.** A thin wrapper that exposes, with Mathlib definitions only, the basic recolouring lemmas of edge-colouring theory proved inside PALOMAR-2026-11-04-000009 (overfull-critical-graphs). vizing_adjacency_lemma (Vizing 1965): if G is of class two (its line graph is not Δ(G)-colourable) and G − xy is Δ(G)-edge-colourable, then x has at least Δ − d(y) + 1 neighbours of degree Δ other than y. critical_two_maxDegree_neighbours: every vertex of a Δ-critical graph has at least two neighbours of degree Δ. multifan_lemma (Stiebitz–Scheide–Toft–Favrholdt, Theorem 2.1): for a Δ(G)-colouring of G − x y₀ of a class-two graph, a multifan at x is elementary and x is joined to every fan vertex by a path coloured with any colour free at x and any colour free at that vertex. kierstead_lemma (Kierstead 1984): a Kierstead path whose interior vertices y₂, …, y_{L−2} have degree below Δ is elementary. Partial edge colourings are symmetric functions V → V → Option (Fin k); five definitions (proper partial edge colouring, colouring of G − ab, free colour, multifan, Kierstead path). The only new proof is the corollary (from Vizing's lemma) and the translation to the colourings of the Vizing entry.

**Sources.**

* V. G. Vizing, *Critical graphs with given chromatic class*, Diskretnyi Analiz 5 (1965), 9–17 (in Russian): Vizing's adjacency lemma.
* H. A. Kierstead, *On the chromatic index of multigraphs without large triangles*, Journal of Combinatorial Theory, Series B 36 (1984), 156–160: Lemma 2, with Δ colours as observed by L. Zhang (Graphs and Combinatorics 16 (2000)). [doi:10.1016/0095-8956(84)90022-4](https://doi.org/10.1016/0095-8956(84)90022-4) · [free full text](https://www.sciencedirect.com/science/article/pii/0095895684900224/pdf)
* Michael Stiebitz, Diego Scheide, Bjarne Toft, Lene M. Favrholdt, *Graph Edge Coloring: Vizing's Theorem and Goldberg's Conjecture*, Wiley, 2012: Theorem 2.1 (multifans).

## Asymptotic 1-factorization of dense regular graphs (Perković–Reed, via Vaughan)

Palomar: [PALOMAR-2026-11-12-000014](https://palomar-registry.org/entry.html?id=PALOMAR-2026-11-12-000014&version=1) (version 1) · code: [jtraverso/asymptotic-one-factorization @ 50bc0b3](https://github.com/jtraverso/asymptotic-one-factorization/tree/50bc0b383e5447dc4b70db20e3af1c6c5efc1c2f) · [archived copy](https://github.com/PalomarArchive/jtraverso--asymptotic-one-factorization--a4d202c2f8f3/tree/palomar/PALOMAR-2026-11-12-000014-v1/50bc0b383e5447dc4b70db20e3af1c6c5efc1c2f)

**What is proved.** A Lean 4 / Mathlib proof of the asymptotic form of the Chetwynd–Hilton 1-factorization conjecture (Perković and Reed 1997, Häggkvist): for every ε > 0 there is N such that every d-regular simple graph on 2n vertices with n ≥ N and d ≥ (1 + ε) n is 1-factorizable, i.e. its line graph is d-colourable (one_factorization); the integer form with (q + 1) n ≤ q d for q ≥ 1 is one_factorization_of_ge. The proof follows Vaughan (arXiv:1010.5192) for multiplicity 1: a balanced bipartition A, Aᶜ with |d_A(v) − d_{Aᶜ}(v)| < s for every vertex (Lemma 13, here by a counting Chernoff bound with no probability theory), equitable colourings of the two sides with matched class sizes (Vizing and McDiarmid's equalisation, from the registered Vizing entry), 5-edge alternating-path exchanges until every colour class is a perfect matching, completion of the classes of the leftover inside edges by Hall's theorem, and a decomposition of the remaining regular bipartite graph into perfect matchings (Hall). Vaughan's sizes n^{2/3} and n^{5/6} are replaced by linear sizes s = ⌊a/(200q)⌋ and t = ⌊a/6⌋ with a = ⌊n/q⌋; N is explicit, N = L (512 L³ + 4) with L = 200 q² for d ≥ (1 + 1/q) n (very large). No definitions beyond Mathlib's. Two statements.

**Sources.**

* Ljubomir Perković, Bruce Reed, *Edge coloring regular graphs of high degree*, Discrete Mathematics 165/166 (1997), 567–578. [doi:10.1016/S0012-365X(96)00202-6](https://doi.org/10.1016/S0012-365X(96)00202-6) · [free full text](https://www.sciencedirect.com/science/article/pii/S0012365X96002026/pdf)
* E. R. Vaughan, *An Asymptotic Version of the Multigraph 1-Factorization Conjecture*, arXiv:1010.5192v1 (2010): Theorem 4 with r = 1, Lemmas 9, 13, 14. [free full text](https://arxiv.org/pdf/1010.5192) (arXiv)

<details><summary>Background references</summary>

* A. G. Chetwynd, A. J. W. Hilton, *Regular graphs of high degree are 1-factorizable*, Proceedings of the London Mathematical Society 50 (1985), 193–206. [doi:10.1112/plms/s3-50.2.193](https://doi.org/10.1112/plms/s3-50.2.193)

</details>

## Plantholt–Shan: the overfull conjecture for graphs of minimum degree at least (1 + ε) n

Palomar: [PALOMAR-2026-11-12-000016](https://palomar-registry.org/entry.html?id=PALOMAR-2026-11-12-000016&version=2) (version 2) · code: [jtraverso/plantholt-shan-overfull @ 39cf759](https://github.com/jtraverso/plantholt-shan-overfull/tree/39cf759850c7911f75fbf32d8e003a04578f9866) · [archived copy](https://github.com/PalomarArchive/jtraverso--plantholt-shan-overfull--1a3be3444c4d/tree/palomar/PALOMAR-2026-11-12-000016-v2/39cf759850c7911f75fbf32d8e003a04578f9866)

**What is proved.** M. J. Plantholt and S. Shan, Edge coloring graphs with large minimum degree (arXiv:2105.05286), in Lean 4 / Mathlib. theorem_1_2 (Theorem 1.2): for every ε > 0 there is N such that a graph G on 2n vertices, n ≥ N, with δ(G) ≥ (1 + ε) n is Δ(G)-edge-colourable iff it has no Δ(G)-overfull subgraph (PlantholtShan.HasOverfullSubgraph, the definition of the registered plantholt-overfull-criterion entry restated in the challenge: an odd set of at least three vertices spanning more than Δ(G)(|S| − 1)/2 edges). theorem_1_3b (Theorem 1.3, Condition (b)): two vertices x ≠ y with d(x) = d(y) ≥ (1/2 + 3ε/2) n, all other vertices of degree Δ(G) ≥ (1 + ε) n and Δ(G) − δ(G) ≤ (1/2 − ε/2) n give χ′ = Δ for n ≥ N. theorem_1_3c (Condition (c)): Δ(G) − δ(G) ≥ n^{6/7}, at least n^{6/7} vertices of degree δ(G), at least n + 1 of degree Δ(G) and δ(G) ≥ (1 + ε) n give χ′ = Δ for n ≥ N (n^{6/7} as a real power). Condition (a) (regular graphs) is the registered asymptotic-one-factorization entry. lemma_2_11 (Lemma 2.11): a bipartite graph with sides of size n, all degrees at least t and at most t vertices of degree below n/2 has a perfect matching. Kept from version 1: hakimi (Theorem 2.5), hamiltonConnected_of_minDegree (Theorem 2.6, δ ≥ n/2 + 1) and exists_spanning_paths (Lemma 2.12). The thresholds N are explicit but huge (e.g. (2^60 q + 1)^21 with 1/q < ε) and not optimized. Two definitions (IsMultigraph, HasOverfullSubgraph). Seven statements.

**Sources.**

* Michael J. Plantholt, Songling Shan, *Edge coloring graphs with large minimum degree*, arXiv:2105.05286v2: Theorems 1.2 and 1.3 (b), (c); Theorem 2.5, Theorem 2.6 (second part), Lemmas 2.11 and 2.12; Section 4. [free full text](https://arxiv.org/pdf/2105.05286) (arXiv)
* S. L. Hakimi, *On Realizability of a Set of Integers as Degrees of the Vertices of a Linear Graph. I*, Journal of the Society for Industrial and Applied Mathematics 10 (1962), 496–506. [doi:10.1137/0110037](https://doi.org/10.1137/0110037)
* Colin McDiarmid, *The chromatic index of multigraphs that are nearly full*, The equalization lemma for multigraph edge colourings (Plantholt–Shan, Lemma 2.3).

<details><summary>Background references</summary>

* E. R. Vaughan, *An asymptotic version of the multigraph 1-factorization conjecture*, arXiv:1010.5192, Lemma 14 (the scheme extended in Plantholt–Shan, Section 4). [free full text](https://arxiv.org/pdf/1010.5192) (arXiv)
* Øystein Ore, *Hamilton connected graphs*, Journal de Mathématiques Pures et Appliquées 42 (1963), 21–27.

</details>

## Elementary graphs are chromatic-choosable

Palomar: [PALOMAR-2026-11-14-000002](https://palomar-registry.org/entry.html?id=PALOMAR-2026-11-14-000002&version=1) (version 1) · code: [jtraverso/elementary-graphs-choosable @ 01fb4e5](https://github.com/jtraverso/elementary-graphs-choosable/tree/01fb4e5b5cecc9d86b577a1c6cc2c05eac6c3245) · [archived copy](https://github.com/PalomarArchive/jtraverso--elementary-graphs-choosable--87711d57fda6/tree/palomar/PALOMAR-2026-11-14-000002-v1/01fb4e5b5cecc9d86b577a1c6cc2c05eac6c3245)

**What is proved.** A Lean 4 / Mathlib formalization of the theorem of Narayanan, Vasudevan and Somasundaram (arXiv:2610.16258) that every finite elementary graph satisfies ch(G) = χ(G) = ω(G) (chromaticChoosable_of_isElementary; clique number at most k implies k-choosability for every colour type, choosable_of_isElementary), together with the structure theorem of Maffray and Reed (JCTB 75, 1999, Theorem 2, (i) ⇒ (iii)) that the proof starts from: every finite elementary graph is an augmentation of the line graph of a bipartite multigraph, given by an explicit edge representation (rep_of_isElementary; IsAugLineGraphRep: vertex v is the edge {a v, b v} of a bipartite multigraph; non-adjacent pairs sharing an end share exactly one end, which is a hub with at most two neighbours; no edge joins two hubs). The earlier statements for the representation class are kept (choosable_of_rep, chromaticChoosable_of_rep, isElementary_of_rep, rep_of_lineGraph, rep_of_cobipartite). The choosability proof follows the paper (Hall, the Deficiency Lemma, saturation, Proposition 3.7, Galvin; Kőnig avoided). The Maffray–Reed proof follows the paper's induction by compression of strong homogeneous pairs (growth procedure from an induced D, claims (1)–(2), A-components, Theorem 5), with every forbidden-subgraph step done as a parity argument on a fixed elementary colouring; Theorems 3–4 are replaced by a "bend" lemma, and two exposition gaps of the paper (p. 143 and Case 3 of claim (2)) are repaired. Galvin's theorem for bipartite multigraphs is imported as a lake dependency from PALOMAR-2026-10-18-000029 v2.

**Sources.**

* Narayanan N, Nandana K. Vasudevan, K. Somasundaram, *Elementary graphs are chromatic-choosable*, arXiv:2610.16258v1 (2026): Theorems 1.1 and 3.4, Lemmas 2.1–2.5, 3.3–3.8, Proposition 3.7. [free full text](https://arxiv.org/pdf/2610.16258) (arXiv)
* Frédéric Maffray, Bruce A. Reed, *A description of claw-free perfect graphs*, J. Combin. Theory Ser. B 75 (1999), 134–156: Theorem 2, (i) ⇒ (iii), with Theorem 5 and the growth procedure of Section 5. [doi:10.1006/jctb.1998.1872](https://doi.org/10.1006/jctb.1998.1872) · [free full text](https://doi.org/10.1006/jctb.1998.1872)

[← Back to the list](../README.md)
