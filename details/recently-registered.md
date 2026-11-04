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

[← Back to the list](../README.md)
