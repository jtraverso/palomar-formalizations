# Number theory: details

[← Back to the list](../README.md)

## The three squares theorem (Gauss–Legendre)

Palomar: [PALOMAR-2026-11-07-000011](https://palomar-registry.org/entry.html?id=PALOMAR-2026-11-07-000011&version=1) (version 1) · code: [jtraverso/three-squares-gauss-legendre @ 783ec66](https://github.com/jtraverso/three-squares-gauss-legendre/tree/783ec66b0db2ff2acf75cc2cd22a9e69737411b5) · [archived copy](https://github.com/PalomarArchive/jtraverso--three-squares-gauss-legendre--2afaf7563d29/tree/palomar/PALOMAR-2026-11-07-000011-v1/783ec66b0db2ff2acf75cc2cd22a9e69737411b5)

**What is proved.** A Lean 4 / Mathlib proof of the three squares theorem of Legendre (1798) and Gauss (1801): a natural number is a sum of three squares if and only if it is not of the form 4^a (8 b + 7) (sum_three_sq_iff), with the corollary that every n ≡ 3 (mod 8) is x₀² + x₁² + x₂² for some x : Fin 3 → ℤ (exists_sum_sq_of_mod_eight_eq_three). The proof uses ternary quadratic forms of determinant one: a positive definite integral ternary form of determinant one is equivalent to x² + y² + z² (proved with Minkowski's convex body theorem), and for n ≢ 0 (mod 4), n ≢ 7 (mod 8) such a form with diagonal entry n is built from a prime in an arithmetic progression (Dirichlet's theorem, as in Mathlib) and quadratic reciprocity for the Jacobi symbol. Two statements; no definitions beyond Mathlib's.

**Sources.**

* Carl Friedrich Gauss, *Disquisitiones Arithmeticae*, Leipzig, 1801; articles 291–292 (numbers represented as sums of three squares).

<details><summary>Background references</summary>

* Melvyn B. Nathanson, *Additive Number Theory: The Classical Bases*, Graduate Texts in Mathematics 164, Springer (1996), Chapter 1 (Sums of polygons). [doi:10.1007/978-1-4757-3845-2](https://doi.org/10.1007/978-1-4757-3845-2)

</details>

## Duke–Schulze-Pillot: the upper bound of Lemma 5(ii) and a conditional Theorem 3(ii)

Palomar: [PALOMAR-2026-11-07-000007](https://palomar-registry.org/entry.html?id=PALOMAR-2026-11-07-000007&version=1) (version 1) · code: [jtraverso/duke-schulze-pillot-ternary @ 4b684f4](https://github.com/jtraverso/duke-schulze-pillot-ternary/tree/4b684f4624fcd9ca4f7fb1e281d6e92024979465) · [archived copy](https://github.com/PalomarArchive/jtraverso--duke-schulze-pillot-ternary--b885fd33e73a/tree/palomar/PALOMAR-2026-11-07-000007-v1/4b684f4624fcd9ca4f7fb1e281d6e92024979465)

**What is proved.** A Lean 4 / Mathlib formalization around W. Duke and R. Schulze-Pillot, Representation of integers by positive ternary quadratic forms and equidistribution of lattice points on ellipsoids (Invent. Math. 99, 1990). q(x) = ½ xᵗAx for a symmetric integer 3 × 3 matrix A with q > 0 on ℚ³ \ {0}, h ∈ ℚ³, r(q, h, n) = #{x ∈ h + ℤ³ : q(x) = n} and, for F ⊆ ℝ³, r(q, F, h, n) = #{x ∈ h + ℤ³ : q(x) = n, x/√n ∈ F}. Unconditional results: card_divisors_le_rpow (d(n) ≤ C_ε n^ε); repCount_le (r(q, h, n) ≤ C_ε n^{1/2+ε} for n ≥ 1); average_le (the same bound for every nonnegatively weighted average of such counts, which includes r(spn_N q, h, n): this is the upper half of Lemma 5(ii)). Conditional results: thm3_ii (Theorem 3(ii), r(q, F, h, n) = R(n) μ(F) + O(n^{1/2 − 1/175 + ε}) for n ≥ 1 in a set S) and spn_upper (R(n) ≤ C_ε n^{1/2+ε}) are proved under two hypotheses that are NOT proved here: hThm1, the estimate of Theorem 1 of the paper (|r(q, F, h, n) − r(q, h, n) μ(F)| ≤ C (n^{−1/175} r(q, h, n) + n^{1/2−1/175+ε}) on S), and hThm3i, the estimate of Theorem 3(i) (|r(q, h, n) − R(n)| ≤ C n^{1/2−1/28+ε} on S); R stands for r(spn_N q, h, n), μF ∈ [0, 1] for μ(F), and S for the restricted set of n. The lower bound n^{1/2−ε} ≪ r(spn_N q, h, n) of Lemma 5(ii) (Siegel's ineffective bound) is not formalized.

**Sources.**

* W. Duke, R. Schulze-Pillot, *Representation of integers by positive ternary quadratic forms and equidistribution of lattice points on ellipsoids*, Inventiones Mathematicae 99 (1990), 49–57; Lemma 5(ii) and Theorem 3(ii). [doi:10.1007/BF01234411](https://doi.org/10.1007/BF01234411)

[← Back to the list](../README.md)
