# Recently registered: details

[← Back to the list](../README.md)

## Complete minors and average degree (Kostochka–Thomason)

Palomar: [PALOMAR-2026-11-04-000001](https://palomar-registry.org/entry.html?id=PALOMAR-2026-11-04-000001&version=1) (version 1) · code: [jtraverso/kostochka-thomason-minors @ c7ddf34](https://github.com/jtraverso/kostochka-thomason-minors/tree/c7ddf34b1e4f9ba71932003c91176e2e6bb92d9f) · [archived copy](https://github.com/PalomarArchive/jtraverso--kostochka-thomason-minors--045d5f0fff3c/tree/palomar/PALOMAR-2026-11-04-000001-v1/c7ddf34b1e4f9ba71932003c91176e2e6bb92d9f)

**What is proved.** A Lean 4 / Mathlib formalization of the Kostochka–Thomason theorem, following the short proof of Alon, Krivelevich and Sudakov. complete_minor_of_edges (their Theorem 1): there is d0 such that for every integer d ≥ d0, every nonempty finite simple graph with at least d·|V| edges has the complete graph K_t as a minor for every natural number t ≤ d / (10 √(ln d)). kostochka_thomason: there is a constant c > 0 such that for every integer d ≥ 2, every nonempty finite simple graph with at least d·|V| edges (average degree at least 2d) has a K_t minor for every t ≤ c·d / √(ln d). Minors are branch-set models, with the definition of the registered entry Mader's theorem and Hadwiger's conjecture for t ≤ 4, whose library is a pinned dependency. Two statements; the thresholds d0 and c are existential (the proof gives d0 = ⌈exp(R0²)⌉ + 1 with R0 ≥ 1400).

**Sources.**

* Noga Alon, Michael Krivelevich, Benny Sudakov, *Complete minors and average degree – a short proof*, Journal of Graph Theory 103 (2023), 599–602; arXiv:2202.08530v2: Theorem 1, Lemma 2 and the proof of Theorem 1. [free full text](https://arxiv.org/pdf/2202.08530) (arXiv)
* A. V. Kostochka, *A lower bound for the Hadwiger number of graphs by their average degree*, Combinatorica 4 (1984), 307–316; announced in Metody Diskret. Analiz. 38 (1982), 37–58 (in Russian).
* Andrew Thomason, *An extremal function for contractions of graphs*, Mathematical Proceedings of the Cambridge Philosophical Society 95 (1984), 261–265.

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

## Bicolouring Steiner triple systems (Colbourn–Dinitz–Rosa product, Dinitz–Stinson conditions)

Palomar: [PALOMAR-2026-11-04-000014](https://palomar-registry.org/entry.html?id=PALOMAR-2026-11-04-000014&version=1) (version 1) · code: [jtraverso/cdr-bicolouring-sts @ a768a98](https://github.com/jtraverso/cdr-bicolouring-sts/tree/a768a98a648e94ad38d0d84501867c999927c546) · [archived copy](https://github.com/PalomarArchive/jtraverso--cdr-bicolouring-sts--063de2d8ca97/tree/palomar/PALOMAR-2026-11-04-000014-v1/a768a98a648e94ad38d0d84501867c999927c546)

**What is proved.** A Lean 4 / Mathlib formalization of the product theorem of Colbourn, Dinitz and Rosa for bicoloured Steiner triple systems and of the necessary conditions of Dinitz and Stinson. A bicolouring of an STS colours the points so that every block receives exactly two colours. bicolourable3_mul (CDR 1999, Theorem 2.4): if there is an (a, b, c)-bicolourable STS(u) with c = max(a, b, c) and c ≤ a + b, and an (x, y, z)-bicolourable STS(v), then there is an (ax + by + cz, ay + bz + cx, az + bx + cy)-bicolourable STS(uv). Dinitz–Stinson Proposition 1.2: for a bicoloured STS on v points with colour classes of sizes c_k, 3 Σ c_k (c_k − 1) = v (v − 1) (IsSTS.three_mul_sum); no two distinct colour classes have size 2 (not_two_classes_of_size_two); and with three colour classes at most one class size is odd (Bicolourable3.not_two_odd). Four statements. The proof of Theorem 2.4 includes Lemma 2.3 of the article (forbidden latin squares exist when max(a, b, c) ≤ n/2), Ryser's theorem on completing latin arrays, and de Werra's equalized edge colourings of bipartite graphs.

**Sources.**

* Charles J. Colbourn, Jeffrey H. Dinitz, Alexander Rosa, *Bicoloring Steiner Triple Systems*, Electronic Journal of Combinatorics 6 (1999), #R25: Theorem 2.4, Lemma 2.3, Proposition 1.4. [doi:10.37236/1457](https://doi.org/10.37236/1457) · [free full text](https://www.combinatorics.org/ojs/index.php/eljc/article/download/v6i1r25/pdf)
* Jeffrey H. Dinitz, Douglas R. Stinson, *A Singular Direct Product for Bicolorable Steiner Triple Systems*, Author's copy, https://site.uvm.edu/jdinitz/files/2021/04/bicolor2.pdf: Proposition 1.2.
* H. J. Ryser, *A combinatorial theorem with an application to latin rectangles*, Proceedings of the American Mathematical Society 2 (1951), 550–552.
* D. de Werra, *Balanced schedules*, INFOR 9 (1971); the form used by Colbourn–Dinitz–Rosa.

## Plantholt's overfull criterion for graphs of high minimum degree, with a 1-factorization theorem for dense regular graphs

Palomar: [PALOMAR-2026-11-04-000016](https://palomar-registry.org/entry.html?id=PALOMAR-2026-11-04-000016&version=1) (version 1) · code: [jtraverso/plantholt-overfull-criterion @ 28ff33d](https://github.com/jtraverso/plantholt-overfull-criterion/tree/28ff33dd73fc858056ff0db75d5a6d6cef15c8b5) · [archived copy](https://github.com/PalomarArchive/jtraverso--plantholt-overfull-criterion--d61ff43b5134/tree/palomar/PALOMAR-2026-11-04-000016-v1/28ff33dd73fc858056ff0db75d5a6d6cef15c8b5)

**What is proved.** A Lean 4 / Mathlib formalization of Theorem 1.2 of M. Plantholt, Overfull conjecture for graphs with high minimum degree (J. Graph Theory 47, 2004), and of a 1-factorization theorem for dense regular graphs in the style of Chetwynd and Hilton (1989). theorem_1_2: if c ≥ 3/4 is such that every regular graph of even order n and degree at least c n is 1-factorizable, and G has even order n with (3δ − Δ)/2 ≥ c n, then G is Class 1 (χ′ = Δ) if and only if G has no Δ-overfull subgraph. lineGraph_colorable_of_isRegular: a d-regular graph of even order 2n with 11 n ≤ 6 d is d-edge-colourable, i.e. 1-factorizable; this is a weaker form of Chetwynd–Hilton 1989, Theorem 2 (d ≥ ½(√7 − 1)|V|), proved with the same architecture. overfull_criterion: Plantholt's theorem with c = 11/12, i.e. if G has even order n and 11 n ≤ 6 (3δ − Δ), then G is Class 1 if and only if it has no Δ-overfull subgraph. Three statements. A Δ-overfull subgraph has an odd number ≥ 3 of vertices and more than Δ ⌊|V(H)|/2⌋ edges; edge colourings are colourings of the line graph.

**Sources.**

* Michael J. Plantholt, *Overfull conjecture for graphs with high minimum degree*, Journal of Graph Theory 47 (2004), 73–80: Theorem 1.2, Lemma 2.1. [doi:10.1002/jgt.20013](https://doi.org/10.1002/jgt.20013)
* A. G. Chetwynd, A. J. W. Hilton, *1-factorizing regular graphs of high degree—an improved bound*, Discrete Mathematics 75 (1989), 103–112: §§2–4 (Lemma 1, Lemma 2, Theorems 4–5, proof of Theorem 1). [doi:10.1016/0012-365X(89)90082-4](https://doi.org/10.1016/0012-365X(89)90082-4) · [free full text](https://doi.org/10.1016/0012-365x(89)90082-4)

[← Back to the list](../README.md)
