# Recently registered: details

[← Back to the list](../README.md)

## Optimal clique partitions under local perturbations

Palomar: [PALOMAR-2026-11-01-000006](https://palomar-registry.org/entry.html?id=PALOMAR-2026-11-01-000006&version=1) (version 1) · code: [jtraverso/erdos81-optimal-clique-partitions @ 719e39b](https://github.com/jtraverso/erdos81-optimal-clique-partitions/tree/719e39baf9d0e356a13f6bfe36b60b4ad5e910d6) · [archived copy](https://github.com/PalomarArchive/jtraverso--erdos81-optimal-clique-partitions--2ba058ab4ee3/tree/palomar/PALOMAR-2026-11-01-000006-v1/719e39baf9d0e356a13f6bfe36b60b4ad5e910d6)

**What is proved.** A Lean 4 / Mathlib formalization of the main results of the author's preprint "Optimal Clique Partitions under Local Perturbations" (Erdős #81 series, Paper VI). For a graph G on n vertices with a core P of size p = ⌊(n+1)/3⌋, h = Δ(G △ (K_P ∨ I_O)) and u, s, m the numbers of core, crossing and exterior edges: if p ≥ 18h + 1 then cp(G) = cp_{≤4}(G) = s − u − 2m = M(n) + C − A − 2m with M(n) = ⌊n(n+1)/6⌋ (Theorem A), and cp_{≤3}(G) − cp(G) = m (Theorem B); if p ≥ 63h, every assignment of the orders 4 or 5 to the exterior edges is realized by an optimal partition (Theorem C); for p ≥ 16 each assignment has at least p^{⌊p²/64⌋} optimal partitions and 2^m p^{⌊p²/64⌋} ≤ N(G) ≤ (n+1)^{5e(G)} (Theorem E). Also: the formula for other core sizes in an explicit window (Proposition 2.1), the intrinsic maximum over all cores (§8.1), the exact optimum with one exceptional vertex, cp = cp_{≤4} = cp*_= = s − u − 2m + D(a,b), ν₃ = ν₃* = u + min(a,b) and the restriction gap (Theorem D), and the complete-join variant cp(G) = M(n) − 2m (Theorem A.1). Twelve statements in all. The constants 18, 63, 16 and 24 are those of the paper; their optimality is not claimed.

**Sources.**

* Juan Pablo Traverso Gianini, *Optimal Clique Partitions under Local Perturbations*, Erdős #81 series, Paper VI, preprint 1.0: Theorems A, B, C, D, E and A.1, Proposition 2.1 and the intrinsic formula of §8.1. In the series collection on Zenodo (series concept DOI 10.5281/zenodo.21273143) and in github.com/jtraverso/erdos-81-chordal-clique-partitions (preprints/PAPER_VI/01_manuscript/PAPER_VI_preprint_v1.0_en.pdf). [doi:10.5281/zenodo.23479507](https://doi.org/10.5281/zenodo.23479507) · [free full text](https://doi.org/10.5281/zenodo.23479507) (Zenodo)

<details><summary>Background references</summary>

* Paul Erdős, Ralph J. Faudree, Edward T. Ordman, *Clique partitions and clique coverings*, Discrete Mathematics 72 (1988) 93–101. [doi:10.1016/0012-365X(88)90197-5](https://doi.org/10.1016/0012-365X(88)90197-5) · [free full text](https://doi.org/10.1016/0012-365x(88)90197-5)

</details>

[← Back to the list](../README.md)
