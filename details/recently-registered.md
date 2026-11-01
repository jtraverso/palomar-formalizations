# Recently registered: details

[← Back to the list](../README.md)

## Triangle decompositions of dense tripartite graphs

Palomar: [PALOMAR-2026-11-01-000005](https://palomar-registry.org/entry.html?id=PALOMAR-2026-11-01-000005&version=1) (version 1) · code: [jtraverso/triangle-decompositions-tripartite @ 57e6f36](https://github.com/jtraverso/triangle-decompositions-tripartite/tree/57e6f36ab132e0f559c43f689eb757e3848696b4) · [archived copy](https://github.com/PalomarArchive/jtraverso--triangle-decompositions-tripartite--9560d1b43409/tree/palomar/PALOMAR-2026-11-01-000005-v1/57e6f36ab132e0f559c43f689eb757e3848696b4)

**What is proved.** A Lean 4 / Mathlib formalization of Corollary 1.6 for r = 3 of Barber, Kühn, Lo, Osthus and Taylor, "Clique decompositions of multipartite graphs and completion of Latin squares" (J. Combin. Theory Ser. A 151 (2017), arXiv:1603.01043): fractional triangle decompositions above a threshold give triangle decompositions above the same threshold. Precisely: if δ ≥ 3/4 and, for every ε > 0, every K₃-divisible tripartite graph with three parts of size n ≥ n₀(ε) and minimum partite degree at least (δ + ε)n has a fractional triangle decomposition, then for every ε > 0 there is n₀ such that every K₃-divisible tripartite graph with parts of size n ≥ n₀ and minimum partite degree at least (δ + ε)n has a triangle decomposition (BKLOT2017.corollary_1_6). The hypothesis δ ≥ 3/4 is an extra assumption of the Lean statement: the article does not need it because the fractional threshold is known to be at least 3/4, which is not formalized here. Combined with the fractional bound of Allsop, Bowtell, Lesgourgues and Petrova (pinned entry PALOMAR-2026-10-30-000008), this gives the unconditional statement with threshold 0.769 − 1/20000 (BKLOT2017.corollary_1_6_ablp). The proof follows the iterative absorption of the article (absorbers, vortex of partitions with random reserves, cover-down, balancing graph, assembly) but replaces the regularity-based Section 8 by a route through the fractional threshold and the Haxell–Rödl transfer.

**Sources.**

* Ben Barber, Daniela Kühn, Allan Lo, Deryk Osthus, Amelia Taylor, *Clique decompositions of multipartite graphs and completion of Latin squares*, J. Combin. Theory Ser. A 151 (2017) 146–201; arXiv:1603.01043v2. Corollary 1.6 for r = 3, proved through Theorem 1.1 and Sections 5–11 (Lemmas 6.6, 7.2, 8.1, 9.1, 10.1, 11.1, 11.2, Corollaries 7.5 and 9.4) specialised to triangles. [doi:10.1016/j.jcta.2017.04.005](https://doi.org/10.1016/j.jcta.2017.04.005) · [free full text](https://arxiv.org/pdf/1603.01043) (arXiv)

<details><summary>Background references</summary>

* Jack Allsop, Candida Bowtell, Thomas Lesgourgues, Kalina Petrova, *Improved bounds on completion of partial Latin squares*, arXiv:2609.37877v1 (30 September 2026), Theorem 1.3. [free full text](https://arxiv.org/pdf/2609.37877) (arXiv)

</details>

[← Back to the list](../README.md)
