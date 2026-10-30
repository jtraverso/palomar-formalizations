# Designs, set systems and discrepancy: details

[← Back to the list](../README.md)

## Kirkman's theorem on Steiner triple systems

Palomar: [PALOMAR-2026-10-28-000003](https://palomar-registry.org/entry.html?id=PALOMAR-2026-10-28-000003&version=1) (version 1) · code: [jtraverso/kirkman-steiner-triple-systems @ 1855141](https://github.com/jtraverso/kirkman-steiner-triple-systems/tree/18551414d822f7fa4fb7535dc43733c4b316c3a8) · [archived copy](https://github.com/PalomarArchive/jtraverso--kirkman-steiner-triple-systems--37adc3898c80/tree/palomar/PALOMAR-2026-10-28-000003-v1/18551414d822f7fa4fb7535dc43733c4b316c3a8)

**What is proved.** A Lean 4 / Mathlib formalization of Kirkman's 1847 theorem: for v ≥ 1, a Steiner triple system on v points (a family of 3-subsets covering every pair of distinct points exactly once) exists if and only if v ≡ 1 or 3 (mod 6). Sufficiency is proved by Bose's and Skolem's constructions from Steiner quasigroups. Mathlib does not contain Steiner triple systems.

**Sources.**

* T. P. Kirkman, *On a problem in combinations*, Cambridge and Dublin Mathematical Journal 2 (1847), 191–204.

<details><summary>Background references</summary>

* R. C. Bose, *On the construction of balanced incomplete block designs*, Annals of Eugenics 9 (1939), 353–399. [doi:10.1111/j.1469-1809.1939.tb02219.x](https://doi.org/10.1111/j.1469-1809.1939.tb02219.x)
* Th. Skolem, *Some remarks on the triple systems of Steiner*, Mathematica Scandinavica 6 (1958), 273–280. [doi:10.7146/math.scand.a-10551](https://doi.org/10.7146/math.scand.a-10551) · [free full text](https://www.mscand.dk/article/download/10551/8572)

</details>

## Counting Steiner triple systems: Wilson (1974) and Linial–Luria (2013)

Palomar: [PALOMAR-2026-10-22-000017](https://palomar-registry.org/entry.html?id=PALOMAR-2026-10-22-000017&version=2) (version 2) · code: [jtraverso/counting-steiner-triple-systems @ 52fda83](https://github.com/jtraverso/counting-steiner-triple-systems/tree/52fda83038df7442c576e17edffba591db703cb8) · [archived copy](https://github.com/PalomarArchive/jtraverso--counting-steiner-triple-systems--25dd3ac3d9ea/tree/palomar/PALOMAR-2026-10-22-000017-v1/52fda83038df7442c576e17edffba591db703cb8)

**What is proved.** A complete Lean 4 / Mathlib formalization of R. M. Wilson's "Nonisomorphic Steiner triple systems" (inequality (2.1), Theorems 1–4, Lemmas 3–5, including the exact numbers of Latin squares of orders 6, 7 and 8 and the bounds N(19) ≥ 2450, N(21) ≥ 2160980, N(25) ≥ 163929929318400) and of N. Linial and Z. Luria's "An upper bound on the number of Steiner triple systems" (Theorems 1.1 and 1.2 with explicit error terms). Version 2 adds a proof of the van der Waerden permanent theorem (Egorychev, Falikman), following Gurvits's proof as simplified by Laurent and Schrijver. The parts of Wilson's Theorems 2 and 3 that rely on it are stated both as implications from the hypothesis vdWPC, as in the paper, and unconditionally (theorem2_full, theorem3_full). Finite computations are kernel-checked certificates (no native_decide). Mathlib does not contain these results.

**Sources.**

* R. M. Wilson, *Nonisomorphic Steiner triple systems*, Mathematische Zeitschrift 135 (1974), 303–313. [doi:10.1007/BF01215371](https://doi.org/10.1007/BF01215371)
* N. Linial, Z. Luria, *An upper bound on the number of Steiner triple systems*, Random Structures & Algorithms 43 (2013), 399–406. [doi:10.1002/rsa.20487](https://doi.org/10.1002/rsa.20487)
* M. Laurent, A. Schrijver, *On Leonid Gurvits's proof for permanents*, The American Mathematical Monthly 117 (2010), 903–911. [doi:10.4169/000298910X523380](https://doi.org/10.4169/000298910X523380) · [free full text](https://www.tandfonline.com/doi/abs/10.4169/000298910X523380)

<details><summary>Background references</summary>

* J. Doyen, R. M. Wilson, *Embeddings of Steiner triple systems*, Discrete Mathematics 5 (1973), 229–239. [doi:10.1016/0012-365X(73)90139-8](https://doi.org/10.1016/0012-365X(73)90139-8) · [free full text](https://doi.org/10.1016/0012-365x(73)90139-8)
* M. B. Wells, *The number of latin squares of order eight*, Journal of Combinatorial Theory 3 (1967), 98–99. [doi:10.1016/S0021-9800(67)80021-8](https://doi.org/10.1016/S0021-9800(67)80021-8) · [free full text](https://www.sciencedirect.com/science/article/pii/S0021980067800218/pdf)
* L. Gurvits, *Van der Waerden/Schrijver-Valiant like conjectures and stable (aka hyperbolic) homogeneous polynomials: one theorem for all*, The Electronic Journal of Combinatorics 15 (2008), R66. [doi:10.37236/790](https://doi.org/10.37236/790) · [free full text](https://www.combinatorics.org/ojs/index.php/eljc/article/download/v15i1r66/pdf)
* G. P. Egorychev, *The solution of van der Waerden's problem for permanents*, Advances in Mathematics 42 (1981), 299–305. [doi:10.1016/0001-8708(81)90044-X](https://doi.org/10.1016/0001-8708(81)90044-X) · [free full text](https://www.sciencedirect.com/science/article/pii/000187088190044X/pdf)
* D. I. Falikman, *Proof of the van der Waerden conjecture regarding the permanent of a doubly stochastic matrix*, Mathematical Notes of the Academy of Sciences of the USSR 29 (1981), 475–479. [doi:10.1007/BF01163285](https://doi.org/10.1007/BF01163285)

</details>

## The Hilton–Milner theorem

Palomar: [PALOMAR-2026-10-28-000001](https://palomar-registry.org/entry.html?id=PALOMAR-2026-10-28-000001&version=1) (version 1) · code: [jtraverso/hilton-milner @ 6059a0d](https://github.com/jtraverso/hilton-milner/tree/6059a0d6f13378b9a92fba297f2d774598ee0f7d) · [archived copy](https://github.com/PalomarArchive/jtraverso--hilton-milner--c43d1f8a75cc/tree/palomar/PALOMAR-2026-10-28-000001-v1/6059a0d6f13378b9a92fba297f2d774598ee0f7d)

**What is proved.** A Lean 4 / Mathlib formalization of the Hilton–Milner theorem: for k ≥ 2 and n > 2k, a nontrivial intersecting family of k-subsets of an n-set (no element lies in all members) has at most C(n−1, k−1) − C(n−k−1, k−1) + 1 members, and this bound is attained. Intersecting is Mathlib's Set.Intersecting. Mathlib contains the Erdős–Ko–Rado theorem but not this result.

**Sources.**

* A. J. W. Hilton, E. C. Milner, *Some intersection theorems for systems of finite sets*, The Quarterly Journal of Mathematics 18 (1967), 369–384. [doi:10.1093/qmath/18.1.369](https://doi.org/10.1093/qmath/18.1.369)

<details><summary>Background references</summary>

* P. Frankl, Z. Füredi, *Non-trivial intersecting families*, Journal of Combinatorial Theory, Series A 41 (1986), 150–153. [doi:10.1016/0097-3165(86)90121-4](https://doi.org/10.1016/0097-3165(86)90121-4) · [free full text](https://doi.org/10.1016/0097-3165(86)90121-4)

</details>

## Ray-Chaudhuri–Wilson: uniform families with restricted intersections

Palomar: [PALOMAR-2026-10-28-000012](https://palomar-registry.org/entry.html?id=PALOMAR-2026-10-28-000012&version=1) (version 1) · code: [jtraverso/restricted-intersections @ ebb9080](https://github.com/jtraverso/restricted-intersections/tree/ebb90800eda4ec83cc18c6da2135b8718757f6e2) · [archived copy](https://github.com/PalomarArchive/jtraverso--restricted-intersections--ad53241811dd/tree/palomar/PALOMAR-2026-10-28-000012-v1/ebb90800eda4ec83cc18c6da2135b8718757f6e2)

**What is proved.** Formalizes Theorem 3 of On t-designs (1975): a k-uniform family of subsets of an n-element ground set whose distinct-pair intersection sizes lie in L ⊆ {0,...,k−1} has at most binomial(n,|L|) members. Includes the actual-intersection-spectrum formulation, the uniform one-intersection bound, and equality examples consisting of all s-subsets.

**Sources.**

* Dijen K. Ray-Chaudhuri, Richard M. Wilson, *On t-designs*, Osaka Journal of Mathematics 12(3) (1975), 737–744, Theorem 3. [doi:10.18910/7296](https://doi.org/10.18910/7296) · [free full text](https://ir.library.osaka-u.ac.jp/repo/ouka/all/7296/ojm12_03_15.pdf)

## The Beck–Fiala integer-making theorem

Palomar: [PALOMAR-2026-10-15-000009](https://palomar-registry.org/entry.html?id=PALOMAR-2026-10-15-000009&version=1) (version 1) · code: [jtraverso/beck-fiala @ 52f1a12](https://github.com/jtraverso/beck-fiala/tree/52f1a12a140b0589ac39619dfd07807d98fdbaf5) · [archived copy](https://github.com/PalomarArchive/jtraverso--beck-fiala--f2fa29dec96f/tree/palomar/PALOMAR-2026-10-15-000009-v1/52f1a12a140b0589ac39619dfd07807d98fdbaf5)

**What is proved.** A Lean 4 / Mathlib formalization of the Beck–Fiala integer-making theorem in its rational unit-cube form: if A is a 0/1 matrix in which every column has at most t ≥ 1 ones and x ∈ [0,1]^N has rational coordinates, then x can be rounded to y ∈ {0,1}^N with |∑ᵢ A j i (y i − x i)| < t for every row j; moreover the rounding can keep every coordinate of x that is already 0 or 1. The proof is the floating-coordinates argument: while some coordinates are strictly between 0 and 1, the rows with more than t floating coordinates are fewer than the floating coordinates, so a nonzero direction keeps their sums fixed, and moving along it makes a coordinate integral; induction on the number of floating coordinates.

**Sources.**

* József Beck, Tibor Fiala, *“Integer-making” theorems*, Discrete Applied Mathematics 3 (1981), no. 1, 1–8. [doi:10.1016/0166-218X(81)90022-6](https://doi.org/10.1016/0166-218X(81)90022-6) · [free full text](https://doi.org/10.1016/0166-218x(81)90022-6)

[← Back to the list](../README.md)
