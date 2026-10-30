# Lean formalizations registered in Palomar

Computer-checked proofs, written in [Lean 4](https://lean-lang.org) with the [Mathlib](https://github.com/leanprover-community/mathlib4) library, by **Juan Pablo Traverso Gianini**. Every entry below has been accepted by the [Palomar registry](https://palomar-registry.org), which keeps the exact statements, the proofs and the record of their verification.

**68 entries:** 6 from my own research and 62 formalizations of results by other authors, mostly in graph theory and combinatorics.

In the tables, the title leads to a page with the details of the entry (what is proved, the sources, the code); **Paper** opens a free copy of the original paper when there is one; **DOI** is the publisher's link; **Palomar** is the registered entry.

## Contents

* [My own research](#my-own-research)
  * [Erdős Problem #81 series](#erdős-problem-81-series) (3)
  * [Triangle decompositions series](#triangle-decompositions-series) (3)
* [Results by other authors](#results-by-other-authors)
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
* [All entries by registration date](registration-log.md)
* [Notes](#notes)
* [arXiv endorsement](#arxiv-endorsement)

## My own research

### Erdős Problem #81 series

Clique partitions of chordal graphs and split graphs (Erdős Problem #81). Series repository [jtraverso/erdos-81-chordal-clique-partitions](https://github.com/jtraverso/erdos-81-chordal-clique-partitions); series concept DOI [10.5281/zenodo.21273143](https://doi.org/10.5281/zenodo.21273143); current PDF collection [10.5281/zenodo.23479507](https://doi.org/10.5281/zenodo.23479507) (open access).

| Result | Paper | DOI | Palomar |
|---|---|---|---|
| [Affine profile reduction for fractional triangle packings in split graphs](details/own-research.md#affine-profile-reduction-for-fractional-triangle-packings-in-split-graphs) | [PDF](https://doi.org/10.5281/zenodo.23478825) | [10.5281/zenodo.23478825](https://doi.org/10.5281/zenodo.23478825) | [PALOMAR-2026-10-28-000028](https://palomar-registry.org/entry.html?id=PALOMAR-2026-10-28-000028&version=2) (v2) |
| [Complete-split extremizers for the fractional triangle-cover deficit on chordal graphs](details/own-research.md#complete-split-extremizers-for-the-fractional-triangle-cover-deficit-on-chordal-graphs) | [PDF](https://doi.org/10.5281/zenodo.23478825) | [10.5281/zenodo.23478825](https://doi.org/10.5281/zenodo.23478825) | [PALOMAR-2026-10-29-000004](https://palomar-registry.org/entry.html?id=PALOMAR-2026-10-29-000004&version=1) |
| [Linear-error clique partitions of split graphs](details/own-research.md#linear-error-clique-partitions-of-split-graphs) | [PDF](https://doi.org/10.5281/zenodo.23478825) | [10.5281/zenodo.23478825](https://doi.org/10.5281/zenodo.23478825) | [PALOMAR-2026-10-29-000006](https://palomar-registry.org/entry.html?id=PALOMAR-2026-10-29-000006&version=1) |

### Triangle decompositions series

The Nash–Williams triangle-decomposition problem. Publication home [jtraverso/nash-williams-triangle-decompositions-release](https://github.com/jtraverso/nash-williams-triangle-decompositions-release).

| Result | Paper | DOI | Palomar |
|---|---|---|---|
| [The Nash–Williams triangle-decomposition theorem](details/own-research.md#the-nashwilliams-triangle-decomposition-theorem) | [PDF](https://arxiv.org/pdf/2606.11178) | [10.48550/arXiv.2606.11178](https://doi.org/10.48550/arXiv.2606.11178) | [PALOMAR-2026-10-21-000009](https://palomar-registry.org/entry.html?id=PALOMAR-2026-10-21-000009&version=1) |
| [Robust absorption for typed triangles (Triangle decompositions II)](details/own-research.md#robust-absorption-for-typed-triangles-triangle-decompositions-ii) | [PDF](https://doi.org/10.5281/zenodo.23502224) | [10.5281/zenodo.23502224](https://doi.org/10.5281/zenodo.23502224) | [PALOMAR-2026-10-23-000013](https://palomar-registry.org/entry.html?id=PALOMAR-2026-10-23-000013&version=1) |
| [Formalizing Delcourt–Postle’s refined absorption in Lean](details/own-research.md#formalizing-delcourtpostles-refined-absorption-in-lean) | [PDF](https://arxiv.org/pdf/2402.17855) | [10.48550/arXiv.2402.17855](https://doi.org/10.48550/arXiv.2402.17855) | [PALOMAR-2026-10-29-000005](https://palomar-registry.org/entry.html?id=PALOMAR-2026-10-29-000005&version=1) |

## Results by other authors

Grouped by subject. **Authors** are those of the main source.

### Vertex colouring

| Result | Authors | Paper | DOI | Palomar |
|---|---|---|---|---|
| [Grötzsch's theorem, Ore's conjecture for k = 4 (Kostochka–Yancey), and the Grünbaum–Aksenov theorem](details/vertex-colouring.md#grötzschs-theorem-ores-conjecture-for-k--4-kostochkayancey-and-the-grünbaumaksenov-theorem) | Kostochka, Yancey | [PDF](https://arxiv.org/pdf/1209.1173) | — | [PALOMAR-2026-10-13-000005](https://palomar-registry.org/entry.html?id=PALOMAR-2026-10-13-000005&version=2) (v2) |
| [The Hajnal–Szemerédi theorem on equitable colourings](details/vertex-colouring.md#the-hajnalszemerédi-theorem-on-equitable-colourings) | Kierstead, Kostochka | — | [10.1017/S0963548307008619](https://doi.org/10.1017/S0963548307008619) | [PALOMAR-2026-10-13-000007](https://palomar-registry.org/entry.html?id=PALOMAR-2026-10-13-000007&version=1) |
| [Brooks' theorem, degree-choosability and blocks](details/vertex-colouring.md#brooks-theorem-degree-choosability-and-blocks) | Brooks | — | [10.1017/S030500410002168X](https://doi.org/10.1017/S030500410002168X) | [PALOMAR-2026-10-16-000003](https://palomar-registry.org/entry.html?id=PALOMAR-2026-10-16-000003&version=2) (v2) |
| [The Gallai–Hasse–Roy–Vitaver theorem](details/vertex-colouring.md#the-gallaihasseroyvitaver-theorem) | Roy | [PDF](https://www.esaim-m2an.org/articles/m2an/pdf/1967/03/m2an1967010501291.pdf) | [10.1051/m2an/1967010501291](https://doi.org/10.1051/m2an/1967010501291) | [PALOMAR-2026-10-16-000015](https://palomar-registry.org/entry.html?id=PALOMAR-2026-10-16-000015&version=1) |
| [Kneser's conjecture and the octahedral Tucker lemma](details/vertex-colouring.md#knesers-conjecture-and-the-octahedral-tucker-lemma) | Lovász | [PDF](https://www.sciencedirect.com/science/article/pii/0097316578900225/pdf) | [10.1016/0097-3165(78)90022-5](https://doi.org/10.1016/0097-3165(78)90022-5) | [PALOMAR-2026-10-20-000006](https://palomar-registry.org/entry.html?id=PALOMAR-2026-10-20-000006&version=1) |
| [Jin's theorem on dense triangle-free graphs](details/vertex-colouring.md#jins-theorem-on-dense-triangle-free-graphs) | Jin | [PDF](https://www.sciencedirect.com/science/article/pii/0012365X9400063O/pdf) | [10.1016/0012-365X(94)00063-O](https://doi.org/10.1016/0012-365X(94)00063-O) | [PALOMAR-2026-10-20-000012](https://palomar-registry.org/entry.html?id=PALOMAR-2026-10-20-000012&version=1) |
| [Lovász's perfect graph theorems](details/vertex-colouring.md#lovászs-perfect-graph-theorems) | Lovász | [PDF](https://www.sciencedirect.com/science/article/pii/0012365X72900064/pdf) | [10.1016/0012-365X(72)90006-4](https://doi.org/10.1016/0012-365X(72)90006-4) | [PALOMAR-2026-10-21-000007](https://palomar-registry.org/entry.html?id=PALOMAR-2026-10-21-000007&version=1) |
| [Stanley's acyclic orientations and chromatic reciprocity](details/vertex-colouring.md#stanleys-acyclic-orientations-and-chromatic-reciprocity) | Stanley | [PDF](https://www.sciencedirect.com/science/article/pii/0012365X73901088/pdf) | [10.1016/0012-365X(73)90108-8](https://doi.org/10.1016/0012-365X(73)90108-8) | [PALOMAR-2026-10-28-000009](https://palomar-registry.org/entry.html?id=PALOMAR-2026-10-28-000009&version=1) |

### Edge colouring and list colouring

| Result | Authors | Paper | DOI | Palomar |
|---|---|---|---|---|
| [Vizing's theorem and equitable edge colourings](details/edge-colouring-and-list-colouring.md#vizings-theorem-and-equitable-edge-colourings) | Vizing | — | [10.1093/imamat/9.1.23](https://doi.org/10.1093/imamat/9.1.23) | [PALOMAR-2026-10-15-000004](https://palomar-registry.org/entry.html?id=PALOMAR-2026-10-15-000004&version=2) (v2) |
| [Kőnig's theorems and Dilworth's theorem](details/edge-colouring-and-list-colouring.md#kőnigs-theorems-and-dilworths-theorem) | Kőnig | [PDF](https://zenodo.org/record/2395248) | [10.1007/BF01456961](https://doi.org/10.1007/BF01456961) | [PALOMAR-2026-10-15-000019](https://palomar-registry.org/entry.html?id=PALOMAR-2026-10-15-000019&version=1) |
| [Galvin's theorem for bipartite multigraphs, the Dinitz problem and stable matchings](details/edge-colouring-and-list-colouring.md#galvins-theorem-for-bipartite-multigraphs-the-dinitz-problem-and-stable-matchings) | Galvin | [PDF](https://doi.org/10.1006/jctb.1995.1011) | [10.1006/jctb.1995.1011](https://doi.org/10.1006/jctb.1995.1011) | [PALOMAR-2026-10-18-000029](https://palomar-registry.org/entry.html?id=PALOMAR-2026-10-18-000029&version=2) (v2) |
| [The list chromatic index of complete graphs (Häggkvist–Janssen)](details/edge-colouring-and-list-colouring.md#the-list-chromatic-index-of-complete-graphs-häggkvistjanssen) | Häggkvist, Janssen | — | [10.1017/S0963548397002927](https://doi.org/10.1017/S0963548397002927) | [PALOMAR-2026-10-15-000003](https://palomar-registry.org/entry.html?id=PALOMAR-2026-10-15-000003&version=1) |
| [Wagner's planarity criterion and list colouring of planar and K₅-minor-free graphs](details/edge-colouring-and-list-colouring.md#wagners-planarity-criterion-and-list-colouring-of-planar-and-k₅-minor-free-graphs) | Wagner | [PDF](https://www.sciencedirect.com/science/article/pii/S0012365X98001587/pdf) | [10.1016/S0012-365X(98)00158-7](https://doi.org/10.1016/S0012-365X(98)00158-7) | [PALOMAR-2026-10-15-000005](https://palomar-registry.org/entry.html?id=PALOMAR-2026-10-15-000005&version=1) |
| [The Alon–Tarsi theorem and 3-choosability of planar bipartite graphs](details/edge-colouring-and-list-colouring.md#the-alontarsi-theorem-and-3-choosability-of-planar-bipartite-graphs) | Alon, Tarsi | — | [10.1007/BF01204715](https://doi.org/10.1007/BF01204715) | [PALOMAR-2026-10-19-000013](https://palomar-registry.org/entry.html?id=PALOMAR-2026-10-19-000013&version=1) |
| [Thomassen: planar graphs of girth at least five are 3-choosable](details/edge-colouring-and-list-colouring.md#thomassen-planar-graphs-of-girth-at-least-five-are-3-choosable) | Thomassen | [PDF](https://doi.org/10.1006/jctb.1995.1027) | [10.1006/jctb.1995.1027](https://doi.org/10.1006/jctb.1995.1027) | [PALOMAR-2026-10-28-000023](https://palomar-registry.org/entry.html?id=PALOMAR-2026-10-28-000023&version=1) |
| [The Pippenger–Spencer theorem on the chromatic index of hypergraphs](details/edge-colouring-and-list-colouring.md#the-pippengerspencer-theorem-on-the-chromatic-index-of-hypergraphs) | Pippenger, Spencer | [PDF](https://doi.org/10.1016/0097-3165(89)90074-5) | [10.1016/0097-3165(89)90074-5](https://doi.org/10.1016/0097-3165(89)90074-5) | [PALOMAR-2026-10-28-000018](https://palomar-registry.org/entry.html?id=PALOMAR-2026-10-28-000018&version=1) |
| [Shannon's theorem on edge colourings of multigraphs](details/edge-colouring-and-list-colouring.md#shannons-theorem-on-edge-colourings-of-multigraphs) | Shannon | — | [10.1002/sapm1949281148](https://doi.org/10.1002/sapm1949281148) | [PALOMAR-2026-10-29-000023](https://palomar-registry.org/entry.html?id=PALOMAR-2026-10-29-000023&version=1) |

### Planarity, minors and graph classes

| Result | Authors | Paper | DOI | Palomar |
|---|---|---|---|---|
| [Kuratowski's theorem](details/planarity-minors-and-graph-classes.md#kuratowskis-theorem) | Kuratowski | [PDF](https://www.impan.pl/shop/publication/transaction/download/product/92829?download.pdf) | [10.4064/fm-15-1-271-283](https://doi.org/10.4064/fm-15-1-271-283) | [PALOMAR-2026-10-15-000018](https://palomar-registry.org/entry.html?id=PALOMAR-2026-10-15-000018&version=1) |
| [Mader's theorem and Hadwiger's conjecture for t ≤ 4](details/planarity-minors-and-graph-classes.md#maders-theorem-and-hadwigers-conjecture-for-t--4) | Mader | — | [10.1007/BF01364272](https://doi.org/10.1007/BF01364272) | [PALOMAR-2026-10-16-000001](https://palomar-registry.org/entry.html?id=PALOMAR-2026-10-16-000001&version=1) |
| [Chordal, split, threshold and cograph structure](details/planarity-minors-and-graph-classes.md#chordal-split-threshold-and-cograph-structure) | Dirac | [PDF](http://msp.org/pjm/1965/15-3/pjm-v15-n3-p11-s.pdf) | [10.1007/BF02992776](https://doi.org/10.1007/BF02992776) | [PALOMAR-2026-10-18-000006](https://palomar-registry.org/entry.html?id=PALOMAR-2026-10-18-000006&version=1) |

### Connectivity, orientations and flows

| Result | Authors | Paper | DOI | Palomar |
|---|---|---|---|---|
| [Menger's theorem, Hamiltonian cycles, long cycles and pancyclicity](details/connectivity-orientations-and-flows.md#mengers-theorem-hamiltonian-cycles-long-cycles-and-pancyclicity) | Menger | [PDF](https://www.impan.pl/shop/publication/transaction/download/product/92646?download.pdf) | [10.4064/fm-10-1-96-115](https://doi.org/10.4064/fm-10-1-96-115) | [PALOMAR-2026-10-15-000020](https://palomar-registry.org/entry.html?id=PALOMAR-2026-10-15-000020&version=2) (v2) |
| [Mader's theorem on highly connected subgraphs](details/connectivity-orientations-and-flows.md#maders-theorem-on-highly-connected-subgraphs) | Mader | — | [10.1007/BF02993903](https://doi.org/10.1007/BF02993903) | [PALOMAR-2026-10-23-000016](https://palomar-registry.org/entry.html?id=PALOMAR-2026-10-23-000016&version=1) |
| [Robbins' theorem on strongly connected orientations](details/connectivity-orientations-and-flows.md#robbins-theorem-on-strongly-connected-orientations) | Robbins | — | [10.2307/2303897](https://doi.org/10.2307/2303897) | [PALOMAR-2026-10-18-000022](https://palomar-registry.org/entry.html?id=PALOMAR-2026-10-18-000022&version=1) |
| [Nash-Williams' weak orientation theorem](details/connectivity-orientations-and-flows.md#nash-williams-weak-orientation-theorem) | Nash-Williams | [PDF](https://www.cambridge.org/core/services/aop-cambridge-core/content/view/2B39912D1666161E4200E61E8F65DE2B/S0008414X00010191a.pdf/div-class-title-on-orientations-connectivity-and-odd-vertex-pairings-in-finite-graphs-div.pdf) | [10.4153/CJM-1960-049-6](https://doi.org/10.4153/CJM-1960-049-6) | [PALOMAR-2026-10-28-000004](https://palomar-registry.org/entry.html?id=PALOMAR-2026-10-28-000004&version=1) |
| [Jaeger's 4-flow and 8-flow theorems and Seymour's 6-flow theorem](details/connectivity-orientations-and-flows.md#jaegers-4-flow-and-8-flow-theorems-and-seymours-6-flow-theorem) | Jaeger | [PDF](https://doi.org/10.1016/0095-8956(79)90057-1) | [10.1016/0095-8956(79)90057-1](https://doi.org/10.1016/0095-8956(79)90057-1) | [PALOMAR-2026-10-18-000009](https://palomar-registry.org/entry.html?id=PALOMAR-2026-10-18-000009&version=3) (v3) |
| [Nowhere-zero 3-flows in 6-edge-connected graphs](details/connectivity-orientations-and-flows.md#nowhere-zero-3-flows-in-6-edge-connected-graphs) | Lovász et al. | [PDF](https://www.sciencedirect.com/science/article/pii/S0095895613000506/pdf) | [10.1016/j.jctb.2013.06.003](https://doi.org/10.1016/j.jctb.2013.06.003) | [PALOMAR-2026-10-28-000022](https://palomar-registry.org/entry.html?id=PALOMAR-2026-10-28-000022&version=1) |

### Cycles and Hamiltonicity

| Result | Authors | Paper | DOI | Palomar |
|---|---|---|---|---|
| [Chvátal's and Pósa's degree conditions for Hamiltonian cycles](details/cycles-and-hamiltonicity.md#chvátals-and-pósas-degree-conditions-for-hamiltonian-cycles) | Chvátal | [PDF](https://www.sciencedirect.com/science/article/pii/0095895672900202/pdf) | [10.1016/0095-8956(72)90020-2](https://doi.org/10.1016/0095-8956(72)90020-2) | [PALOMAR-2026-10-18-000001](https://palomar-registry.org/entry.html?id=PALOMAR-2026-10-18-000001&version=1) |
| [Dirac's theorem: k vertices of a k-connected graph lie on a common cycle](details/cycles-and-hamiltonicity.md#diracs-theorem-k-vertices-of-a-k-connected-graph-lie-on-a-common-cycle) | Dirac | — | [10.1002/mana.19600220107](https://doi.org/10.1002/mana.19600220107) | [PALOMAR-2026-10-18-000011](https://palomar-registry.org/entry.html?id=PALOMAR-2026-10-18-000011&version=1) |
| [The Erdős–Pósa theorem for cycles](details/cycles-and-hamiltonicity.md#the-erdőspósa-theorem-for-cycles) | Erdős, Pósa | [PDF](https://www.cambridge.org/core/services/aop-cambridge-core/content/view/00E165DD4E460BE00867629661177985/S0008414X00039316a.pdf/div-class-title-on-independent-circuits-contained-in-a-graph-div.pdf) | [10.4153/CJM-1965-035-8](https://doi.org/10.4153/CJM-1965-035-8) | [PALOMAR-2026-10-20-000003](https://palomar-registry.org/entry.html?id=PALOMAR-2026-10-20-000003&version=1) |
| [The Corrádi–Hajnal theorem on vertex-disjoint cycles](details/cycles-and-hamiltonicity.md#the-corrádihajnal-theorem-on-vertex-disjoint-cycles) | Corrádi, Hajnal | — | [10.1007/BF01895727](https://doi.org/10.1007/BF01895727) | [PALOMAR-2026-10-29-000007](https://palomar-registry.org/entry.html?id=PALOMAR-2026-10-29-000007&version=1) |

### Matchings, factors and polyhedral combinatorics

| Result | Authors | Paper | DOI | Palomar |
|---|---|---|---|---|
| [Petersen's theorem](details/matchings-factors-and-polyhedral-combinatorics.md#petersens-theorem) | Petersen | [PDF](https://projecteuclid.org/journals/acta-mathematica/volume-15/issue-none/Die-Theorie-der-regul%c3%a4ren-graphs/10.1007/BF02392606.pdf) | [10.1007/BF02392606](https://doi.org/10.1007/BF02392606) | [PALOMAR-2026-10-16-000004](https://palomar-registry.org/entry.html?id=PALOMAR-2026-10-16-000004&version=1) |
| [Berge's theorem, the Tutte–Berge formula and the Gallai–Edmonds theorem](details/matchings-factors-and-polyhedral-combinatorics.md#berges-theorem-the-tutteberge-formula-and-the-gallaiedmonds-theorem) | Berge | [PDF](http://europepmc.org/pmc/articles/PMC534337) | [10.1073/pnas.43.9.842](https://doi.org/10.1073/pnas.43.9.842) | [PALOMAR-2026-10-16-000011](https://palomar-registry.org/entry.html?id=PALOMAR-2026-10-16-000011&version=2) (v2) |
| [Euler's theorem on Eulerian circuits and trails, and Petersen's 2-factor theorem](details/matchings-factors-and-polyhedral-combinatorics.md#eulers-theorem-on-eulerian-circuits-and-trails-and-petersens-2-factor-theorem) | Euler | [PDF](https://zenodo.org/record/1447429) | [10.1007/BF01442866](https://doi.org/10.1007/BF01442866) | [PALOMAR-2026-10-16-000016](https://palomar-registry.org/entry.html?id=PALOMAR-2026-10-16-000016&version=1) |
| [Tutte's f-factor theorem](details/matchings-factors-and-polyhedral-combinatorics.md#tuttes-f-factor-theorem) | Tutte | [PDF](https://www.cambridge.org/core/services/aop-cambridge-core/content/view/320CE524F3E9AA34F0BF6A824642C34B/S0008414X00036270a.pdf/div-class-title-the-factors-of-graphs-div.pdf) | [10.4153/CJM-1952-028-2](https://doi.org/10.4153/CJM-1952-028-2) | [PALOMAR-2026-10-18-000005](https://palomar-registry.org/entry.html?id=PALOMAR-2026-10-18-000005&version=1) |
| [Graphic sequences: the Erdős–Gallai and Havel–Hakimi theorems](details/matchings-factors-and-polyhedral-combinatorics.md#graphic-sequences-the-erdősgallai-and-havelhakimi-theorems) | Erdős, Gallai | [PDF](https://doi.org/10.21136/cpm.1955.108220) | [10.21136/CPM.1955.108220](https://doi.org/10.21136/CPM.1955.108220) | [PALOMAR-2026-10-16-000017](https://palomar-registry.org/entry.html?id=PALOMAR-2026-10-16-000017&version=1) |
| [Regular subgraphs of almost regular graphs (Alon–Friedland–Kalai)](details/matchings-factors-and-polyhedral-combinatorics.md#regular-subgraphs-of-almost-regular-graphs-alonfriedlandkalai) | Alon, Friedland, Kalai | [PDF](https://doi.org/10.1016/0095-8956(84)90047-9) | [10.1016/0095-8956(84)90047-9](https://doi.org/10.1016/0095-8956(84)90047-9) | [PALOMAR-2026-10-26-000001](https://palomar-registry.org/entry.html?id=PALOMAR-2026-10-26-000001&version=1) |
| [Edmonds cardinality matroid intersection](details/matchings-factors-and-polyhedral-combinatorics.md#edmonds-cardinality-matroid-intersection) | Edmonds | — | [10.1007/3-540-36478-1_2](https://doi.org/10.1007/3-540-36478-1_2) | [PALOMAR-2026-10-28-000005](https://palomar-registry.org/entry.html?id=PALOMAR-2026-10-28-000005&version=1) |
| [Edmonds' perfect matching polytope and matching polytope](details/matchings-factors-and-polyhedral-combinatorics.md#edmonds-perfect-matching-polytope-and-matching-polytope) | Edmonds | [PDF](https://doi.org/10.6028/jres.069b.013) | [10.6028/jres.069B.013](https://doi.org/10.6028/jres.069B.013) | [PALOMAR-2026-10-28-000010](https://palomar-registry.org/entry.html?id=PALOMAR-2026-10-28-000010&version=1) |

### Extremal graph theory and Ramsey theory

| Result | Authors | Paper | DOI | Palomar |
|---|---|---|---|---|
| [Classical bounds for graph Ramsey numbers](details/extremal-graph-theory-and-ramsey-theory.md#classical-bounds-for-graph-ramsey-numbers) | Erdős, Szekeres | [PDF](https://www.ams.org/bull/1947-53-04/S0002-9904-1947-08785-1/S0002-9904-1947-08785-1.pdf) | [10.1090/S0002-9904-1947-08785-1](https://doi.org/10.1090/S0002-9904-1947-08785-1) | [PALOMAR-2026-10-15-000021](https://palomar-registry.org/entry.html?id=PALOMAR-2026-10-15-000021&version=1) |
| [Füredi's stability theorem and the Erdős–Simonovits stability theorem](details/extremal-graph-theory-and-ramsey-theory.md#füredis-stability-theorem-and-the-erdőssimonovits-stability-theorem) | Füredi | [PDF](https://www.sciencedirect.com/science/article/pii/S0095895615000568/pdf) | [10.1016/j.jctb.2015.05.001](https://doi.org/10.1016/j.jctb.2015.05.001) | [PALOMAR-2026-10-16-000024](https://palomar-registry.org/entry.html?id=PALOMAR-2026-10-16-000024&version=1) |
| [The graph removal lemma for every fixed graph](details/extremal-graph-theory-and-ramsey-theory.md#the-graph-removal-lemma-for-every-fixed-graph) | Erdős, Frankl, Rödl | — | [10.1007/BF01788085](https://doi.org/10.1007/BF01788085) | [PALOMAR-2026-10-18-000002](https://palomar-registry.org/entry.html?id=PALOMAR-2026-10-18-000002&version=1) |
| [The Bondy–Simonovits even cycle theorem](details/extremal-graph-theory-and-ramsey-theory.md#the-bondysimonovits-even-cycle-theorem) | Bondy, Simonovits | [PDF](https://doi.org/10.1016/0095-8956(74)90052-5) | [10.1016/0095-8956(74)90052-5](https://doi.org/10.1016/0095-8956(74)90052-5) | [PALOMAR-2026-10-22-000043](https://palomar-registry.org/entry.html?id=PALOMAR-2026-10-22-000043&version=1) |

### Probabilistic methods and random graphs

| Result | Authors | Paper | DOI | Palomar |
|---|---|---|---|---|
| [Graphs of large girth and large chromatic number: Erdős, Mycielski, and the fractional chromatic number of Mycielski graphs](details/probabilistic-methods-and-random-graphs.md#graphs-of-large-girth-and-large-chromatic-number-erdős-mycielski-and-the-fractional-chromatic-number-of-mycielski-graphs) | Erdős | [PDF](https://www.cambridge.org/core/services/aop-cambridge-core/content/view/154EF813293BC7D0652C4CBCD9D18E84/S0008414X00002947a.pdf/div-class-title-graph-theory-and-probability-div.pdf) | [10.4153/CJM-1959-003-9](https://doi.org/10.4153/CJM-1959-003-9) | [PALOMAR-2026-10-17-000009](https://palomar-registry.org/entry.html?id=PALOMAR-2026-10-17-000009&version=2) (v2) |
| [The Lovász Local Lemma and two applications](details/probabilistic-methods-and-random-graphs.md#the-lovász-local-lemma-and-two-applications) | Erdős, Lovász | [PDF](https://www.sciencedirect.com/science/article/pii/0012365X77900449/pdf) | [10.1016/0012-365X(77)90044-9](https://doi.org/10.1016/0012-365X(77)90044-9) | [PALOMAR-2026-10-20-000004](https://palomar-registry.org/entry.html?id=PALOMAR-2026-10-20-000004&version=1) |
| [Hamiltonicity and connectivity thresholds of the random graph G(n, p)](details/probabilistic-methods-and-random-graphs.md#hamiltonicity-and-connectivity-thresholds-of-the-random-graph-gn-p) | Pósa | [PDF](https://doi.org/10.1016/0012-365x(76)90068-6) | [10.1016/0012-365X(76)90068-6](https://doi.org/10.1016/0012-365X(76)90068-6) | [PALOMAR-2026-10-28-000021](https://palomar-registry.org/entry.html?id=PALOMAR-2026-10-28-000021&version=1) |
| [Pseudorandom hypergraph matchings (Ehard–Glock–Joos)](details/probabilistic-methods-and-random-graphs.md#pseudorandom-hypergraph-matchings-ehardglockjoos) | Ehard, Glock, Joos | [PDF](https://arxiv.org/pdf/1907.09946) | [10.1017/S0963548320000280](https://doi.org/10.1017/S0963548320000280) | [PALOMAR-2026-10-17-000004](https://palomar-registry.org/entry.html?id=PALOMAR-2026-10-17-000004&version=1) |
| [The Moser–Tardos theorem (algorithmic Lovász Local Lemma)](details/probabilistic-methods-and-random-graphs.md#the-mosertardos-theorem-algorithmic-lovász-local-lemma) | Moser, Tardos | — | [10.1145/1667053.1667060](https://doi.org/10.1145/1667053.1667060) | [PALOMAR-2026-10-29-000008](https://palomar-registry.org/entry.html?id=PALOMAR-2026-10-29-000008&version=1) |

### Decompositions and packings

| Result | Authors | Paper | DOI | Palomar |
|---|---|---|---|---|
| [Dross's theorem on fractional triangle decompositions](details/decompositions-and-packings.md#drosss-theorem-on-fractional-triangle-decompositions) | Dross | [PDF](https://hal-lirmm.ccsd.cnrs.fr/lirmm-01336680v1/document) | [10.1137/15M1014310](https://doi.org/10.1137/15M1014310) | [PALOMAR-2026-10-15-000008](https://palomar-registry.org/entry.html?id=PALOMAR-2026-10-15-000008&version=1) |
| [Near-regular hypergraph matchings and the asymptotic triangle-packing gap](details/decompositions-and-packings.md#near-regular-hypergraph-matchings-and-the-asymptotic-triangle-packing-gap) | Haxell, Rödl | — | [10.1007/s004930170003](https://doi.org/10.1007/s004930170003) | [PALOMAR-2026-10-15-000011](https://palomar-registry.org/entry.html?id=PALOMAR-2026-10-15-000011&version=2) (v2) |
| [The Nash-Williams–Tutte tree packing theorem and Nash-Williams' arboricity theorem](details/decompositions-and-packings.md#the-nash-williamstutte-tree-packing-theorem-and-nash-williams-arboricity-theorem) | Nash-Williams | — | [10.1112/jlms/s1-36.1.445](https://doi.org/10.1112/jlms/s1-36.1.445) | [PALOMAR-2026-10-17-000008](https://palomar-registry.org/entry.html?id=PALOMAR-2026-10-17-000008&version=1) |
| [Fractional triangle decompositions of dense tripartite graphs](details/decompositions-and-packings.md#fractional-triangle-decompositions-of-dense-tripartite-graphs) | Allsop et al. | [PDF](https://arxiv.org/pdf/2609.37877) | — | [PALOMAR-2026-10-30-000008](https://palomar-registry.org/entry.html?id=PALOMAR-2026-10-30-000008&version=1) |

### Designs, set systems and discrepancy

| Result | Authors | Paper | DOI | Palomar |
|---|---|---|---|---|
| [Kirkman's theorem on Steiner triple systems](details/designs-set-systems-and-discrepancy.md#kirkmans-theorem-on-steiner-triple-systems) | Kirkman | — | — | [PALOMAR-2026-10-28-000003](https://palomar-registry.org/entry.html?id=PALOMAR-2026-10-28-000003&version=1) |
| [Counting Steiner triple systems: Wilson (1974) and Linial–Luria (2013)](details/designs-set-systems-and-discrepancy.md#counting-steiner-triple-systems-wilson-1974-and-linialluria-2013) | Wilson | [PDF](https://www.tandfonline.com/doi/abs/10.4169/000298910X523380) | [10.1007/BF01215371](https://doi.org/10.1007/BF01215371) | [PALOMAR-2026-10-22-000017](https://palomar-registry.org/entry.html?id=PALOMAR-2026-10-22-000017&version=2) (v2) |
| [The Hilton–Milner theorem](details/designs-set-systems-and-discrepancy.md#the-hiltonmilner-theorem) | Hilton, Milner | — | [10.1093/qmath/18.1.369](https://doi.org/10.1093/qmath/18.1.369) | [PALOMAR-2026-10-28-000001](https://palomar-registry.org/entry.html?id=PALOMAR-2026-10-28-000001&version=1) |
| [Ray-Chaudhuri–Wilson: uniform families with restricted intersections](details/designs-set-systems-and-discrepancy.md#ray-chaudhuriwilson-uniform-families-with-restricted-intersections) | Ray-Chaudhuri, Wilson | [PDF](https://ir.library.osaka-u.ac.jp/repo/ouka/all/7296/ojm12_03_15.pdf) | [10.18910/7296](https://doi.org/10.18910/7296) | [PALOMAR-2026-10-28-000012](https://palomar-registry.org/entry.html?id=PALOMAR-2026-10-28-000012&version=1) |
| [The Beck–Fiala integer-making theorem](details/designs-set-systems-and-discrepancy.md#the-beckfiala-integer-making-theorem) | Beck, Fiala | [PDF](https://doi.org/10.1016/0166-218x(81)90022-6) | [10.1016/0166-218X(81)90022-6](https://doi.org/10.1016/0166-218X(81)90022-6) | [PALOMAR-2026-10-15-000009](https://palomar-registry.org/entry.html?id=PALOMAR-2026-10-15-000009&version=1) |

### Algebraic and spectral graph theory

| Result | Authors | Paper | DOI | Palomar |
|---|---|---|---|---|
| [The Cauchy–Binet formula, Kirchhoff's matrix-tree theorem and Cayley's formula](details/algebraic-and-spectral-graph-theory.md#the-cauchybinet-formula-kirchhoffs-matrix-tree-theorem-and-cayleys-formula) | Kirchhoff | [PDF](https://zenodo.org/record/2242265) | [10.1002/andp.18471481202](https://doi.org/10.1002/andp.18471481202) | [PALOMAR-2026-10-16-000019](https://palomar-registry.org/entry.html?id=PALOMAR-2026-10-16-000019&version=1) |
| [Moore graphs of diameter two: the Hoffman–Singleton theorem](details/algebraic-and-spectral-graph-theory.md#moore-graphs-of-diameter-two-the-hoffmansingleton-theorem) | Hoffman, Singleton | — | [10.1147/rd.45.0497](https://doi.org/10.1147/rd.45.0497) | [PALOMAR-2026-10-17-000018](https://palomar-registry.org/entry.html?id=PALOMAR-2026-10-17-000018&version=1) |
| [Spectral bounds on the chromatic and independence numbers](details/algebraic-and-spectral-graph-theory.md#spectral-bounds-on-the-chromatic-and-independence-numbers) | Collatz, Sinogowitz | — | [10.1007/BF02941924](https://doi.org/10.1007/BF02941924) | [PALOMAR-2026-10-18-000016](https://palomar-registry.org/entry.html?id=PALOMAR-2026-10-18-000016&version=1) |
| [Lovász's bound on the Shannon capacity](details/algebraic-and-spectral-graph-theory.md#lovászs-bound-on-the-shannon-capacity) | Lovász | — | [10.1109/TIT.1979.1055985](https://doi.org/10.1109/TIT.1979.1055985) | [PALOMAR-2026-10-21-000003](https://palomar-registry.org/entry.html?id=PALOMAR-2026-10-21-000003&version=1) |
| [The expander mixing lemma and the Alon–Boppana bound](details/algebraic-and-spectral-graph-theory.md#the-expander-mixing-lemma-and-the-alonboppana-bound) | Alon, Chung | [PDF](https://doi.org/10.1016/0012-365x(88)90189-6) | [10.1016/0012-365X(88)90189-6](https://doi.org/10.1016/0012-365X(88)90189-6) | [PALOMAR-2026-10-22-000035](https://palomar-registry.org/entry.html?id=PALOMAR-2026-10-22-000035&version=1) |
| [The Graham–Pollak theorem](details/algebraic-and-spectral-graph-theory.md#the-grahampollak-theorem) | Graham, Pollak | — | [10.1002/j.1538-7305.1971.tb02618.x](https://doi.org/10.1002/j.1538-7305.1971.tb02618.x) | [PALOMAR-2026-10-23-000006](https://palomar-registry.org/entry.html?id=PALOMAR-2026-10-23-000006&version=1) |

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
