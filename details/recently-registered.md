# Recently registered: details

[← Back to the list](../README.md)

## Complete minors and average degree (Kostochka–Thomason)

Palomar: [PALOMAR-2026-11-04-000001](https://palomar-registry.org/entry.html?id=PALOMAR-2026-11-04-000001&version=1) (version 1) · code: [jtraverso/kostochka-thomason-minors @ c7ddf34](https://github.com/jtraverso/kostochka-thomason-minors/tree/c7ddf34b1e4f9ba71932003c91176e2e6bb92d9f) · [archived copy](https://github.com/PalomarArchive/jtraverso--kostochka-thomason-minors--045d5f0fff3c/tree/palomar/PALOMAR-2026-11-04-000001-v1/c7ddf34b1e4f9ba71932003c91176e2e6bb92d9f)

**What is proved.** A Lean 4 / Mathlib formalization of the Kostochka–Thomason theorem, following the short proof of Alon, Krivelevich and Sudakov. complete_minor_of_edges (their Theorem 1): there is d0 such that for every integer d ≥ d0, every nonempty finite simple graph with at least d·|V| edges has the complete graph K_t as a minor for every natural number t ≤ d / (10 √(ln d)). kostochka_thomason: there is a constant c > 0 such that for every integer d ≥ 2, every nonempty finite simple graph with at least d·|V| edges (average degree at least 2d) has a K_t minor for every t ≤ c·d / √(ln d). Minors are branch-set models, with the definition of the registered entry Mader's theorem and Hadwiger's conjecture for t ≤ 4, whose library is a pinned dependency. Two statements; the thresholds d0 and c are existential (the proof gives d0 = ⌈exp(R0²)⌉ + 1 with R0 ≥ 1400).

**Sources.**

* Noga Alon, Michael Krivelevich, Benny Sudakov, *Complete minors and average degree – a short proof*, Journal of Graph Theory 103 (2023), 599–602; arXiv:2202.08530v2: Theorem 1, Lemma 2 and the proof of Theorem 1. [free full text](https://arxiv.org/pdf/2202.08530) (arXiv)
* A. V. Kostochka, *A lower bound for the Hadwiger number of graphs by their average degree*, Combinatorica 4 (1984), 307–316; announced in Metody Diskret. Analiz. 38 (1982), 37–58 (in Russian).
* Andrew Thomason, *An extremal function for contractions of graphs*, Mathematical Proceedings of the Cambridge Philosophical Society 95 (1984), 261–265.

[← Back to the list](../README.md)
