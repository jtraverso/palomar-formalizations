# Number theory: details

[← Back to the list](../README.md)

## Siegel's theorem on L(1, χ) for real Dirichlet characters

Palomar: [PALOMAR-2026-11-12-000005](https://palomar-registry.org/entry.html?id=PALOMAR-2026-11-12-000005&version=1) (version 1) · code: [jtraverso/siegel-theorem @ dbe9353](https://github.com/jtraverso/siegel-theorem/tree/dbe9353374a11317bdd2d436e264536258c5762f) · [archived copy](https://github.com/PalomarArchive/jtraverso--siegel-theorem--fcfb5ef237dc/tree/palomar/PALOMAR-2026-11-12-000005-v1/dbe9353374a11317bdd2d436e264536258c5762f)

**What is proved.** A Lean 4 / Mathlib proof of Siegel's theorem (1935): for every ε > 0 there is c > 0 with c·N^(-ε) ≤ ‖L(1, χ)‖ for every real non-principal Dirichlet character χ modulo N (SiegelThm.siegel, with Mathlib's DirichletCharacter.LFunction; χ need not be primitive). The proof is Goldfeld's (1974): F = ζ·L(χ₁)L(χ₂)L(χ₁χ₂) has non-negative Dirichlet coefficients with a₁ = 1; its regular part G = F − λ/(s−1) is expanded in a Taylor series at s = 2, with Cauchy's estimate on the circle |s−2| = 3/2 (where |G| ≤ 4000 (N₁N₂)²), giving ‖λ‖ ≥ (1−β)/2 · (50000 (N₁N₂)²)^(−4(1−β)) whenever Re F(β) ≤ 0 and 7/8 ≤ β < 1; Siegel's dichotomy (an exceptional zero in [1−ε/16, 1) or none, in which case χ₁ is the character mod 4) gives the ineffective constant. Characters that induce the same character as χ₁ are handled with the Euler factors (∏_{p∣n}(1−1/p) ≥ c(η)n^(−η)). Two auxiliary statements are also compared: the integral representation L(s, χ) = s∫_1^∞ A(t) t^(−s−1) dt on Re s > 0 (SiegelThm.LFunction_eq_integral, via Mathlib's Abel summation for Re s > 1, a Mellin-transform holomorphy argument and the identity theorem) and ‖∑_{k≤M} χ(k)‖ ≤ N (SiegelThm.norm_sum_Icc_le). Mathlib is the only dependency; Mathlib's continuation of ζ is not used (ζ(s) = 1/(s−1) + 1 − s∫_1^∞{t}t^(−s−1) dt is proved directly). Three statements; no definitions beyond Mathlib's.

**Sources.**

* Carl Ludwig Siegel, *Über die Classenzahl quadratischer Zahlkörper*, Acta Arithmetica 1 (1935), 83–86.
* Dorian Goldfeld, *A simple proof of Siegel's theorem*, Proc. Nat. Acad. Sci. USA 71 (1974), 1055. [doi:10.1073/pnas.71.4.1055](https://doi.org/10.1073/pnas.71.4.1055) · [free full text](https://pmc.ncbi.nlm.nih.gov/articles/PMC388160/)

<details><summary>Background references</summary>

* Hugh L. Montgomery, Robert C. Vaughan, *Multiplicative Number Theory I. Classical Theory*, Cambridge University Press, 2007, §11.2.

</details>

## The three squares theorem (Gauss–Legendre)

Palomar: [PALOMAR-2026-11-07-000011](https://palomar-registry.org/entry.html?id=PALOMAR-2026-11-07-000011&version=1) (version 1) · code: [jtraverso/three-squares-gauss-legendre @ 783ec66](https://github.com/jtraverso/three-squares-gauss-legendre/tree/783ec66b0db2ff2acf75cc2cd22a9e69737411b5) · [archived copy](https://github.com/PalomarArchive/jtraverso--three-squares-gauss-legendre--2afaf7563d29/tree/palomar/PALOMAR-2026-11-07-000011-v1/783ec66b0db2ff2acf75cc2cd22a9e69737411b5)

**What is proved.** A Lean 4 / Mathlib proof of the three squares theorem of Legendre (1798) and Gauss (1801): a natural number is a sum of three squares if and only if it is not of the form 4^a (8 b + 7) (sum_three_sq_iff), with the corollary that every n ≡ 3 (mod 8) is x₀² + x₁² + x₂² for some x : Fin 3 → ℤ (exists_sum_sq_of_mod_eight_eq_three). The proof uses ternary quadratic forms of determinant one: a positive definite integral ternary form of determinant one is equivalent to x² + y² + z² (proved with Minkowski's convex body theorem), and for n ≢ 0 (mod 4), n ≢ 7 (mod 8) such a form with diagonal entry n is built from a prime in an arithmetic progression (Dirichlet's theorem, as in Mathlib) and quadratic reciprocity for the Jacobi symbol. Two statements; no definitions beyond Mathlib's.

**Sources.**

* Carl Friedrich Gauss, *Disquisitiones Arithmeticae*, Leipzig, 1801; articles 291–292 (numbers represented as sums of three squares).

<details><summary>Background references</summary>

* Melvyn B. Nathanson, *Additive Number Theory: The Classical Bases*, Graduate Texts in Mathematics 164, Springer (1996), Chapter 1 (Sums of polygons). [doi:10.1007/978-1-4757-3845-2](https://doi.org/10.1007/978-1-4757-3845-2)

</details>

## Duke–Schulze-Pillot bounds and squarefree three squares in fixed caps (H1)

Palomar: [PALOMAR-2026-11-07-000007](https://palomar-registry.org/entry.html?id=PALOMAR-2026-11-07-000007&version=2) (version 2) · code: [jtraverso/duke-schulze-pillot-ternary @ 21575ff](https://github.com/jtraverso/duke-schulze-pillot-ternary/tree/21575ff924c98165ea1b451f7cbcc27c016ebd3e) · [archived copy](https://github.com/PalomarArchive/jtraverso--duke-schulze-pillot-ternary--b885fd33e73a/tree/palomar/PALOMAR-2026-11-07-000007-v2/21575ff924c98165ea1b451f7cbcc27c016ebd3e)

**What is proved.** A Lean 4 / Mathlib formalization retaining the upper representation bounds and the conditional consequence of Duke–Schulze-Pillot (Invent. Math. 99, 1990), and adding an unconditional fixed-cap theorem for x^2+y^2+z^2. H1: for every unit vector u in R^3 and every epsilon > 0 there is T such that every squarefree t >= T with t congruent to 3 modulo 8 has an integer representation x with sum x_i^2=t and |x_i-sqrt(t)u_i| <= epsilon sqrt(t) for every coordinate. The new statement takes no analytic estimate as a hypothesis. Its proof combines finite-degree harmonic Weyl bounds, odd-degree cancellation, a positive minimum of finitely many degree-dependent savings, and a representation lower bound supplied by the verified Siegel theorem. The threshold is ineffective. The original three unconditional upper/divisor bounds and two conditional statements are retained unchanged; the latter still require hThm1 and hThm3i for general ternary forms. No unconditional general Duke–Schulze-Pillot theorem, sharp 1/175 exponent, spinor-genus lower bound or numerical cutoff is claimed.

**Sources.**

* W. Duke, R. Schulze-Pillot, *Representation of integers by positive ternary quadratic forms and equidistribution of lattice points on ellipsoids*, Inventiones Mathematicae 99 (1990), 49–57; Lemma 5(ii) and Theorem 3(ii). [doi:10.1007/BF01234411](https://doi.org/10.1007/BF01234411)
* W. Duke, *Hyperbolic distribution problems and half-integral weight Maass forms*, Inventiones Mathematicae 92 (1988), 73–90; spherical distribution consequence.
* Henryk Iwaniec, *Fourier coefficients of modular forms of half-integral weight*, Inventiones Mathematicae 87 (1987), 385–401. [doi:10.1007/BF01389423](https://doi.org/10.1007/BF01389423)

<details><summary>Background references</summary>

* Juan Pablo Traverso Gianini, *Siegel's theorem for real Dirichlet characters (Goldfeld's proof)*, https://github.com/jtraverso/siegel-theorem @ dbe9353.
* Charlie Dorsey, *Weil Bounds Toolkit*, https://github.com/charliedorsey/weil-bounds-toolkit @ 0f3e4c3.
* Juan Pablo Traverso Gianini, *The three squares theorem (Gauss–Legendre)*, https://github.com/jtraverso/three-squares-gauss-legendre @ 783ec66.
* Juan Pablo Traverso Gianini, *Four squares in caps and Jacobi's four-square theorem for odd N*, https://github.com/jtraverso/four-squares-in-caps @ a1fcaaf.

</details>

## Four squares in caps, and Jacobi's four-square theorem for odd N

Palomar: [PALOMAR-2026-11-08-000002](https://palomar-registry.org/entry.html?id=PALOMAR-2026-11-08-000002&version=1) (version 1) · code: [jtraverso/four-squares-in-caps @ a1fcaaf](https://github.com/jtraverso/four-squares-in-caps/tree/a1fcaafb270c099ea773706912192adbfec19a83) · [archived copy](https://github.com/PalomarArchive/jtraverso--four-squares-in-caps--308878e49a2e/tree/palomar/PALOMAR-2026-11-08-000002-v1/a1fcaafb270c099ea773706912192adbfec19a83)

**What is proved.** A Lean 4 / Mathlib proof of two results on sums of four squares. (1) Jacobi's four-square theorem for odd N: the number of x : Fin 4 → ℤ with x₀² + x₁² + x₂² + x₃² = N equals 8 ∑_{d ∣ N} d (jacobi_four_squares_odd), following the proof of Andrews, Ekhad and Zeilberger (1993): two finite q-series identities proved by WZ telescoping, combined into a finite identity that is read modulo X^{N+1} in ℚ⟦X⟧. (2) Four squares in caps (four_squares_in_caps): for every unit vector q ∈ ℝ⁴ and every δ > 0 there is M₀ such that every odd m ≥ M₀ is β₀² + β₁² + β₂² + β₃² with β : Fin 4 → ℤ and |βᵢ − √m qᵢ| ≤ δ √m for all i, i.e. the integer points of the sphere of radius √m meet every cap of fixed angular radius. The proof uses the Duke–Friedlander–Iwaniec delta method (in Heath-Brown's form) with Gaussian weights: an exact formula through the theta transformation, Fourier bounds for the cut-off weight, and the Weil bound for Kloosterman sums, imported from the Weil Bounds Toolkit (PALOMAR-2026-11-03-000018) as a lake dependency. The main term is not evaluated: it depends on the center of the cap only through its norm, so comparing caps with a grid of centers reduces the theorem to the lower bound r₄(m) ≥ 8m for odd m, which (1) provides. All constants are effective but not explicit in the statement (M₀ is existential). Two statements; no definitions beyond Mathlib's.

**Sources.**

* George E. Andrews, Shalosh B. Ekhad, Doron Zeilberger, *A short proof of Jacobi's formula for the number of representations of an integer as a sum of four squares*, Amer. Math. Monthly 100 (1993), 273–276; Lemma (a), (b) and identity (3). [free full text](https://arxiv.org/pdf/math/9206203) (arXiv)

<details><summary>Background references</summary>

* D. R. Heath-Brown, *A new form of the circle method, and its application to quadratic forms*, J. reine angew. Math. 481 (1996), 149–206. [doi:10.1515/crll.1996.481.149](https://doi.org/10.1515/crll.1996.481.149)
* H. D. Kloosterman, *On the representation of numbers in the form ax² + by² + cz² + dt²*, Acta Math. 49 (1926), 407–464. [doi:10.1007/BF02564115](https://doi.org/10.1007/BF02564115) · [free full text](https://projecteuclid.org/journals/acta-mathematica/volume-49/issue-3-4/Th%c3%a9orie-de-fermeture-et-le-probl%c3%a8me-de-repr%c3%a9sentation-approch%c3%a9e-des/10.1007/BF02564115.pdf)
* Charlie Dorsey, *Weil Bounds Toolkit*, https://github.com/charliedorsey/weil-bounds-toolkit @ 0f3e4c3.

</details>

[← Back to the list](../README.md)
