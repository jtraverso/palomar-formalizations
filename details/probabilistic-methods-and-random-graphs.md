# Probabilistic methods and random graphs: details

[← Back to the list](../README.md)

## Graphs of large girth and large chromatic number: Erdős, Mycielski, and the fractional chromatic number of Mycielski graphs

Palomar: [PALOMAR-2026-10-17-000009](https://palomar-registry.org/entry.html?id=PALOMAR-2026-10-17-000009&version=2) (version 2) · code: [jtraverso/erdos-girth-chromatic @ 05407c1](https://github.com/jtraverso/erdos-girth-chromatic/tree/05407c110b29ebb412667c688b2758d23bc744dd) · [archived copy](https://github.com/PalomarArchive/jtraverso--erdos-girth-chromatic--0532ff066cce/tree/palomar/PALOMAR-2026-10-17-000009-v2/05407c110b29ebb412667c688b2758d23bc744dd)

**What is proved.** A Lean 4 / Mathlib formalization of three classical results on graphs with large chromatic number. (1) Erdős' 1959 theorem: for every g and k there is a finite graph with girth greater than g and chromatic number greater than k, in the structural form given by the probabilistic argument (for every ε > 0 and all large n, a graph on n vertices with girth greater than g whose independent sets have fewer than εn vertices). (2) Mycielski's 1955 construction M(G): it preserves and reflects triangle-freeness, M(G) is (k+1)-colourable exactly when G is k-colourable, χ(M(G)) = χ(G) + 1 for every finite G, and iterating from K₂ gives triangle-free graphs with 3·2ⁿ − 1 vertices and chromatic number n + 2. (3) Larsen, Propp and Ullman (1995): for the fractional chromatic number χ_f (least total weight of a fractional colouring by independent sets), χ_f(M(G)) = χ_f(G) + 1/χ_f(G) for every finite graph G with at least one vertex. Version 2 adds (2) and (3); the statements of version 1 are unchanged. Mathlib has girth and chromatic number but none of these theorems, and no fractional chromatic number.

**Sources.**

* Paul Erdős, *Graph Theory and Probability*, Canadian Journal of Mathematics 11 (1959), 34–38. [doi:10.4153/CJM-1959-003-9](https://doi.org/10.4153/CJM-1959-003-9) · [free full text](https://www.cambridge.org/core/services/aop-cambridge-core/content/view/154EF813293BC7D0652C4CBCD9D18E84/S0008414X00002947a.pdf/div-class-title-graph-theory-and-probability-div.pdf)
* Jan Mycielski, *Sur le coloriage des graphs*, Colloquium Mathematicum 3 (1955), 161–162. [doi:10.4064/cm-3-2-161-162](https://doi.org/10.4064/cm-3-2-161-162) · [free full text](https://www.impan.pl/shop/publication/transaction/download/product/94136?download.pdf)
* Michael Larsen, James Propp, Daniel Ullman, *The fractional chromatic number of Mycielski's graphs*, Journal of Graph Theory 19 (1995), 411–416. [doi:10.1002/jgt.3190190313](https://doi.org/10.1002/jgt.3190190313)

## The Lovász Local Lemma and two applications

Palomar: [PALOMAR-2026-10-20-000004](https://palomar-registry.org/entry.html?id=PALOMAR-2026-10-20-000004&version=1) (version 1) · code: [jtraverso/lovasz-local-lemma @ 9d020fa](https://github.com/jtraverso/lovasz-local-lemma/tree/9d020fa8fb20e9426c2d6780a3cfab4a68794d89) · [archived copy](https://github.com/PalomarArchive/jtraverso--lovasz-local-lemma--3b6f209cddb3/tree/palomar/PALOMAR-2026-10-20-000004-v1/9d020fa8fb20e9426c2d6780a3cfab4a68794d89)

**What is proved.** A Lean 4 / Mathlib formalization of the Lovász Local Lemma for finitely many events in a probability space with a dependency graph (each event mutually independent, in the sense of Mathlib's `ProbabilityTheory.Indep` of generated σ-algebras, of its non-neighbours), in its general form (P(A_i) ≤ x_i ∏_{j∼i}(1 − x_j) implies P(no event) ≥ ∏(1 − x_i)) and its symmetric form (e p (d + 1) ≤ 1 implies P(no event) > 0); and of two applications: Spencer's Ramsey lower bound (if 2e(C(k,2)C(n,k−2) + 1) ≤ 2^C(k,2) then R(k,k) > n) and the Erdős–Lovász property B theorem for k-uniform hypergraphs (each edge meeting at most d others with e(d + 1) ≤ 2^(k−1); and the case where every vertex lies in at most k edges, for k ≥ 9). Mathlib has independence and product measures but not the Local Lemma.

**Sources.**

* P. Erdős, L. Lovász, *Problems and results on 3-chromatic hypergraphs and some related questions*, Infinite and Finite Sets (Colloq. Keszthely, 1973), Colloq. Math. Soc. János Bolyai 10, North-Holland (1975), 609–627.
* Joel Spencer, *Asymptotic lower bounds for Ramsey functions*, Discrete Mathematics 20 (1977), 69–76. [doi:10.1016/0012-365X(77)90044-9](https://doi.org/10.1016/0012-365X(77)90044-9) · [free full text](https://www.sciencedirect.com/science/article/pii/0012365X77900449/pdf)

<details><summary>Background references</summary>

* Noga Alon, Joel H. Spencer, *The Probabilistic Method (3rd edition)*, Wiley (2008), Chapter 5. [doi:10.1002/9780470277331](https://doi.org/10.1002/9780470277331)

</details>

## Hamiltonicity and connectivity thresholds of the random graph G(n, p)

Palomar: [PALOMAR-2026-10-28-000021](https://palomar-registry.org/entry.html?id=PALOMAR-2026-10-28-000021&version=1) (version 1) · code: [jtraverso/random-graph-thresholds @ 86325fa](https://github.com/jtraverso/random-graph-thresholds/tree/86325faff71fb76c0769963525b69095fa0a6241) · [archived copy](https://github.com/PalomarArchive/jtraverso--random-graph-thresholds--8101b919ee82/tree/palomar/PALOMAR-2026-10-28-000021-v1/86325faff71fb76c0769963525b69095fa0a6241)

**What is proved.** A Lean 4 / Mathlib formalization of two classical threshold results for the binomial random graph G(n, p), modelled as a finite product probability space with one independent Bernoulli(p) coin per pair of vertices: Pósa's theorem (1976) that G(n, p) with p ≥ C log n / n is Hamiltonian with probability tending to 1, also stated with the explicit constant C = 80 (posa_eighty), and both sides of the Erdős–Rényi connectivity threshold (1959): G(n, (log n ± ω(n))/n) with ω(n) → ∞, the edge probability clipped to [0, 1], is connected with probability tending to 1, resp. 0. Hamiltonicity and connectivity are Mathlib's SimpleGraph.IsHamiltonian and SimpleGraph.Connected. Mathlib defines the binomial random graph as a measure on graphs (SimpleGraph.binomialRandom); this project uses its own finite product model instead, and these threshold theorems are not in Mathlib.

**Sources.**

* L. Pósa, *Hamiltonian circuits in random graphs*, Discrete Mathematics 14 (1976), 359–364. [doi:10.1016/0012-365X(76)90068-6](https://doi.org/10.1016/0012-365X(76)90068-6) · [free full text](https://doi.org/10.1016/0012-365x(76)90068-6)
* P. Erdős, A. Rényi, *On random graphs I*, Publicationes Mathematicae Debrecen 6 (1959), 290–297. [doi:10.5486/PMD.1959.6.3-4.12](https://doi.org/10.5486/PMD.1959.6.3-4.12)

## Pseudorandom hypergraph matchings (Ehard–Glock–Joos)

Palomar: [PALOMAR-2026-10-17-000004](https://palomar-registry.org/entry.html?id=PALOMAR-2026-10-17-000004&version=1) (version 1) · code: [jtraverso/pseudorandom-hypergraph-matchings @ 3957f3c](https://github.com/jtraverso/pseudorandom-hypergraph-matchings/tree/3957f3c0dbc34fd310cb5fecf7941fddc9ef6c8f) · [archived copy](https://github.com/PalomarArchive/jtraverso--pseudorandom-hypergraph-matchings--40c1ca802506/tree/palomar/PALOMAR-2026-10-17-000004-v1/3957f3c0dbc34fd310cb5fecf7941fddc9ef6c8f)

**What is proved.** A Lean 4 / Mathlib formalization of the main results of Ehard, Glock and Joos, "Pseudorandom hypergraph matchings" (Combin. Probab. Comput. 2020): Pippenger's theorem on almost perfect matchings in almost regular hypergraphs with small codegrees (Theorem 1.1); the existence of a matching M in any r-uniform hypergraph with Δ(H) ≤ Δ, codegrees ≤ Δ^{1−δ} and at most exp(Δ^{ε²}) edges such that ω(M) = (1 ± Δ^{−ε}) ω(E(H))/Δ simultaneously for up to exp(Δ^{ε²}) weight functions (Theorem 1.2, with ε = δ/(50r²)); the generalization to weight functions on ℓ-tuples of edges, under the same exponential cap on the number of edges and of weight functions (Theorem 1.3, the main theorem, with ε = δ/(50L²r²)); the concentration inequality for pattern weights under a uniformly random colouring (Theorem 3.1); and the existence of partial Steiner systems whose subgraph counts behave as in the random model (Theorem 4.1). The formal proof is self-contained over Mathlib: Freedman's and Bernstein's inequalities are proved inside the project, and the Molloy–Reed colouring theorem used as a black box in the paper is replaced by a self-contained nibble.

**Sources.**

* Stefan Ehard, Stefan Glock, Felix Joos, *Pseudorandom hypergraph matchings*, Combinatorics, Probability and Computing 29 (2020), 868–885; arXiv:1907.09946. [doi:10.1017/S0963548320000280](https://doi.org/10.1017/S0963548320000280) · [free full text](https://arxiv.org/pdf/1907.09946) (arXiv)

<details><summary>Background references</summary>

* Nicholas Pippenger, Joel Spencer, *Asymptotic behavior of the chromatic index for hypergraphs*, Journal of Combinatorial Theory, Series A 51 (1989), 24–42. [doi:10.1016/0097-3165(89)90074-5](https://doi.org/10.1016/0097-3165(89)90074-5) · [free full text](https://doi.org/10.1016/0097-3165(89)90074-5)
* Noga Alon, Raphael Yuster, *On a Hypergraph Matching Problem*, Graphs and Combinatorics 21 (2005), 377–384. [doi:10.1007/s00373-005-0628-x](https://doi.org/10.1007/s00373-005-0628-x)
* David A. Freedman, *On Tail Probabilities for Martingales*, The Annals of Probability 3 (1975), 100–118. [doi:10.1214/aop/1176996452](https://doi.org/10.1214/aop/1176996452) · [free full text](https://projecteuclid.org/journals/annals-of-probability/volume-3/issue-1/On-Tail-Probabilities-for-Martingales/10.1214/aop/1176996452.pdf)
* Michael Molloy, Bruce Reed, *Near-optimal list colorings*, Random Structures and Algorithms 17 (2000), 376–402. [doi:10.1002/1098-2418(200010/12)17:3/4<376::AID-RSA10>3.0.CO;2-0](https://doi.org/10.1002/1098-2418(200010/12)17:3/4<376::AID-RSA10>3.0.CO;2-0)

</details>

## The Moser–Tardos theorem (algorithmic Lovász Local Lemma)

Palomar: [PALOMAR-2026-10-29-000008](https://palomar-registry.org/entry.html?id=PALOMAR-2026-10-29-000008&version=1) (version 1) · code: [jtraverso/moser-tardos @ 5a3024a](https://github.com/jtraverso/moser-tardos/tree/5a3024a6d3eb442ac6925f9b3660b93c36cfb8b4) · [archived copy](https://github.com/PalomarArchive/jtraverso--moser-tardos--5ec56ed9b1a0/tree/palomar/PALOMAR-2026-10-29-000008-v1/5a3024a6d3eb442ac6925f9b3660b93c36cfb8b4)

**What is proved.** A Lean 4 / Mathlib formalization of the Moser–Tardos theorem in the variable setting: finitely many independent random variables with finite ranges, n events each determined by a finite set of variables, neighbours sharing a variable. If P(A_j) ≤ x_j ∏_{k ∈ Γ(j)} (1 − x_k) with 0 ≤ x_j < 1, the resampling algorithm (always resampling the first violated event), run on a random resampling table, resamples A_j at most x_j / (1 − x_j) times in expectation among its first t steps, for every t; the expected total number of resamplings is at most ∑_j x_j / (1 − x_j); the probability that it has not stopped after t steps is at most (∑_j x_j / (1 − x_j)) / t; and some assignment avoids all events (the Lovász Local Lemma in the variable setting). The proof formalizes witness trees built from the log, the τ-check coupling with the resampling table, and the Galton–Watson bound.

**Sources.**

* Robin A. Moser, Gábor Tardos, *A constructive proof of the general Lovász Local Lemma*, Journal of the ACM 57 (2010), no. 2, Article 11. [doi:10.1145/1667053.1667060](https://doi.org/10.1145/1667053.1667060)

[← Back to the list](../README.md)
