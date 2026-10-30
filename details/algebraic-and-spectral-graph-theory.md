# Algebraic and spectral graph theory: details

[← Back to the list](../README.md)

## The Cauchy–Binet formula, Kirchhoff's matrix-tree theorem and Cayley's formula

Palomar: [PALOMAR-2026-10-16-000019](https://palomar-registry.org/entry.html?id=PALOMAR-2026-10-16-000019&version=1) (version 1) · code: [jtraverso/matrix-tree @ aeab0f2](https://github.com/jtraverso/matrix-tree/tree/aeab0f267c523dd3cac9a287b589f65a99d20d01) · [archived copy](https://github.com/PalomarArchive/jtraverso--matrix-tree--5efe2b63de2b/tree/palomar/PALOMAR-2026-10-16-000019-v1/aeab0f267c523dd3cac9a287b589f65a99d20d01)

**What is proved.** A Lean 4 / Mathlib formalization of the Cauchy–Binet formula for determinants of products of rectangular matrices over commutative rings (not in Mathlib), of Kirchhoff's matrix-tree theorem (the number of spanning trees of a finite graph is any principal cofactor of Mathlib's Laplacian matrix), and of Cayley's formula (n^(n−2) labelled trees on n ≥ 1 vertices), derived from the matrix-tree theorem for the complete graph.

**Sources.**

* G. Kirchhoff, *Ueber die Auflösung der Gleichungen, auf welche man bei der Untersuchung der linearen Vertheilung galvanischer Ströme geführt wird*, Annalen der Physik und Chemie 148 (1847), 497–508. [doi:10.1002/andp.18471481202](https://doi.org/10.1002/andp.18471481202) · [free full text](https://zenodo.org/record/2242265)
* Arthur Cayley, *A theorem on trees*, Quarterly Journal of Pure and Applied Mathematics 23 (1889), 376–378.
* J. P. M. Binet, *Mémoire sur un système de formules analytiques, et leur application à des considérations géométriques*, Journal de l'École Polytechnique 9 (1813), 280–302.
* A.-L. Cauchy, *Mémoire sur les fonctions qui ne peuvent obtenir que deux valeurs égales et de signes contraires par suite des transpositions opérées entre les variables qu'elles renferment*, Journal de l'École Polytechnique 10 (1815), 29–112.

## Moore graphs of diameter two: the Hoffman–Singleton theorem

Palomar: [PALOMAR-2026-10-17-000018](https://palomar-registry.org/entry.html?id=PALOMAR-2026-10-17-000018&version=1) (version 1) · code: [jtraverso/moore-graphs-hoffman-singleton @ 8819ccf](https://github.com/jtraverso/moore-graphs-hoffman-singleton/tree/8819ccfea5474fab3d1cbc17e703860a4e008254) · [archived copy](https://github.com/PalomarArchive/jtraverso--moore-graphs-hoffman-singleton--c0de8dabed2e/tree/palomar/PALOMAR-2026-10-17-000018-v1/8819ccfea5474fab3d1cbc17e703860a4e008254)

**What is proved.** A Lean 4 / Mathlib formalization of the Hoffman–Singleton theorem on Moore graphs of diameter two. For a finite k-regular graph of diameter at most two: the Moore bound n ≤ k² + 1; if moreover the girth is at least five, then n = k² + 1 and the graph is strongly regular with parameters (k² + 1, k, 0, 1); and, if k ≥ 2, then k ∈ {2, 3, 7, 57}. Mathlib has strongly regular graphs and the spectral theorem for Hermitian matrices, but not this theorem.

**Sources.**

* A. J. Hoffman, R. R. Singleton, *On Moore Graphs with Diameters 2 and 3*, IBM Journal of Research and Development 4 (1960), 497–504. [doi:10.1147/rd.45.0497](https://doi.org/10.1147/rd.45.0497)

## Spectral bounds on the chromatic and independence numbers

Palomar: [PALOMAR-2026-10-18-000016](https://palomar-registry.org/entry.html?id=PALOMAR-2026-10-18-000016&version=1) (version 1) · code: [jtraverso/spectral-graph-bounds @ 8d8b4ce](https://github.com/jtraverso/spectral-graph-bounds/tree/8d8b4ce17e56165b5f1ad3b285fb141666804e1c) · [archived copy](https://github.com/PalomarArchive/jtraverso--spectral-graph-bounds--08d3a675ea5f/tree/palomar/PALOMAR-2026-10-18-000016-v1/8d8b4ce17e56165b5f1ad3b285fb141666804e1c)

**What is proved.** A Lean 4 / Mathlib formalization of classical eigenvalue bounds for a finite simple graph G on a nonempty vertex type, with λ_max and λ_min the largest and smallest eigenvalues of its real adjacency matrix: the average degree is at most λ_max and λ_max is at most the maximum degree (Collatz–Sinogowitz); G is (⌊λ_max⌋ + 1)-colourable (Wilf 1967); if G has an edge, every proper colouring uses at least 1 − λ_max/λ_min colours (Hoffman 1970); and if G is k-regular with k ≥ 1, every independent set has at most n(−λ_min)/(k − λ_min) vertices (Hoffman's ratio bound). Mathlib has the spectral theorem for Hermitian matrices but none of these bounds.

**Sources.**

* L. Collatz, U. Sinogowitz, *Spektren endlicher Grafen*, Abhandlungen aus dem Mathematischen Seminar der Universität Hamburg 21 (1957), 63–77. [doi:10.1007/BF02941924](https://doi.org/10.1007/BF02941924)
* H. S. Wilf, *The Eigenvalues of a Graph and Its Chromatic Number*, Journal of the London Mathematical Society 42 (1967), 330–332. [doi:10.1112/jlms/s1-42.1.330](https://doi.org/10.1112/jlms/s1-42.1.330)
* A. J. Hoffman, *On eigenvalues and colorings of graphs*, In: B. Harris (ed.), Graph Theory and its Applications, Academic Press, New York (1970), 79–91.

<details><summary>Background references</summary>

* L. Lovász, *On the Shannon capacity of a graph*, IEEE Transactions on Information Theory 25 (1979), 1–7. [doi:10.1109/TIT.1979.1055985](https://doi.org/10.1109/TIT.1979.1055985)

</details>

## Lovász's bound on the Shannon capacity

Palomar: [PALOMAR-2026-10-21-000003](https://palomar-registry.org/entry.html?id=PALOMAR-2026-10-21-000003&version=1) (version 1) · code: [jtraverso/lovasz-theta @ 2d506b5](https://github.com/jtraverso/lovasz-theta/tree/2d506b5abca378d9133b5e3f1264a5316843c9a7) · [archived copy](https://github.com/PalomarArchive/jtraverso--lovasz-theta--8c936f7e6f5c/tree/palomar/PALOMAR-2026-10-21-000003-v1/2d506b5abca378d9133b5e3f1264a5316843c9a7)

**What is proved.** A Lean 4 / Mathlib formalization of Lovász's orthonormal-representation bound on the independence number (if u is an orthonormal representation of G with handle c and 1 ≤ t (c·u_i)² for every vertex, then α(G) ≤ t), of its multiplicativity under strong powers (α(G^⊠k) ≤ t^k), and of its application to the pentagon: α(C₅^⊠k)² ≤ 5^k for every k, Shannon's α(C₅^⊠2) = 5, and hence the Shannon capacity Θ(C₅) = √5. Mathlib has independence numbers but neither strong graph products nor the Shannon capacity.

**Sources.**

* L. Lovász, *On the Shannon capacity of a graph*, IEEE Transactions on Information Theory 25 (1979), 1–7. [doi:10.1109/TIT.1979.1055985](https://doi.org/10.1109/TIT.1979.1055985)
* C. E. Shannon, *The zero error capacity of a noisy channel*, IRE Transactions on Information Theory 2 (1956), 8–19. [doi:10.1109/TIT.1956.1056798](https://doi.org/10.1109/TIT.1956.1056798)

## The expander mixing lemma and the Alon–Boppana bound

Palomar: [PALOMAR-2026-10-22-000035](https://palomar-registry.org/entry.html?id=PALOMAR-2026-10-22-000035&version=1) (version 1) · code: [jtraverso/expander-spectral @ f96a998](https://github.com/jtraverso/expander-spectral/tree/f96a99893d4d31495af5f8d9e6181f7b4c91e0ba) · [archived copy](https://github.com/PalomarArchive/jtraverso--expander-spectral--c7934103ea1e/tree/palomar/PALOMAR-2026-10-22-000035-v1/f96a99893d4d31495af5f8d9e6181f7b4c91e0ba)

**What is proved.** A Lean 4 / Mathlib formalization of two basic results of spectral graph theory, stated through the adjacency quadratic form on vectors orthogonal to the all-ones vector: the expander mixing lemma of Alon and Chung (for a d-regular graph on n ≥ 2 vertices with |x·Ax| ≤ μ‖x‖² on 𝟙⊥, |e(S,T) − d|S||T|/n| ≤ μ√(|S||T|)), and the Alon–Boppana bound in Nilli's form (a d-regular graph, d ≥ 2, with two vertices at distance at least 2k + 4 has a nonzero x ⟂ 𝟙 with x·Ax ≥ (2√(d−1) − (2√(d−1) − 1)/(k+1))‖x‖²). Mathlib has adjacency matrices but neither result.

**Sources.**

* N. Alon, F. R. K. Chung, *Explicit construction of linear sized tolerant networks*, Discrete Mathematics 72 (1988), 15–19. [doi:10.1016/0012-365X(88)90189-6](https://doi.org/10.1016/0012-365X(88)90189-6) · [free full text](https://doi.org/10.1016/0012-365x(88)90189-6)
* A. Nilli, *On the second eigenvalue of a graph*, Discrete Mathematics 91 (1991), 207–210. [doi:10.1016/0012-365X(91)90112-F](https://doi.org/10.1016/0012-365X(91)90112-F) · [free full text](https://doi.org/10.1016/0012-365x(91)90112-f)

<details><summary>Background references</summary>

* S. Hoory, N. Linial, A. Wigderson, *Expander graphs and their applications*, Bulletin of the American Mathematical Society 43 (2006), 439–561. [doi:10.1090/S0273-0979-06-01126-8](https://doi.org/10.1090/S0273-0979-06-01126-8) · [free full text](https://doi.org/10.1090/s0273-0979-06-01126-8)

</details>

## The Graham–Pollak theorem

Palomar: [PALOMAR-2026-10-23-000006](https://palomar-registry.org/entry.html?id=PALOMAR-2026-10-23-000006&version=1) (version 1) · code: [jtraverso/graham-pollak @ 68d32f0](https://github.com/jtraverso/graham-pollak/tree/68d32f0faf102fc1716ac89ffc861eefe897e749) · [archived copy](https://github.com/PalomarArchive/jtraverso--graham-pollak--3485c9d9d4a5/tree/palomar/PALOMAR-2026-10-23-000006-v1/68d32f0faf102fc1716ac89ffc861eefe897e749)

**What is proved.** A Lean 4 / Mathlib formalization of the Graham–Pollak theorem: the edge set of the complete graph K_n cannot be partitioned into fewer than n − 1 complete bipartite graphs, together with the matching construction by n − 1 stars. Biclique decompositions are encoded by families of pairs of disjoint vertex sets covering every pair of distinct vertices exactly once. Mathlib does not contain this theorem.

**Sources.**

* R. L. Graham, H. O. Pollak, *On the addressing problem for loop switching*, Bell System Technical Journal 50 (1971), 2495–2519. [doi:10.1002/j.1538-7305.1971.tb02618.x](https://doi.org/10.1002/j.1538-7305.1971.tb02618.x)

<details><summary>Background references</summary>

* H. Tverberg, *On the decomposition of K_n into complete bipartite graphs*, Journal of Graph Theory 6 (1982), 493–494. [doi:10.1002/jgt.3190060414](https://doi.org/10.1002/jgt.3190060414)

</details>

[← Back to the list](../README.md)
