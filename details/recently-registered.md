# Recently registered: details

[← Back to the list](../README.md)

## Lovász's (g,f)-factor theorem

Palomar: [PALOMAR-2026-11-12-000004](https://palomar-registry.org/entry.html?id=PALOMAR-2026-11-12-000004&version=1) (version 1) · code: [jtraverso/lovasz-gf-factor @ 87f7fef](https://github.com/jtraverso/lovasz-gf-factor/tree/87f7fef730446522d4f1eb27bc90d50b370e1574) · [archived copy](https://github.com/PalomarArchive/jtraverso--lovasz-gf-factor--5a6529cf49ee/tree/palomar/PALOMAR-2026-11-12-000004-v1/87f7fef730446522d4f1eb27bc90d50b370e1574)

**What is proved.** A Lean 4 / Mathlib proof of Lovász's (g,f)-factor theorem (1970): for a finite simple graph G and g ≤ f : V → ℕ, G has a spanning subgraph H with g(v) ≤ deg_H(v) ≤ f(v) for every vertex if and only if, for all disjoint vertex sets S and T, h(S,T) ≤ Σ_{v∈S} f(v) + Σ_{v∈T} (deg_{G−S}(v) − g(v)), where h(S,T) is the number of components C of G − (S ∪ T) with g = f on C and Σ_{v∈C} f(v) + e(C,T) odd (lovasz_gf_factor). As a corollary, the criterion of Heinrich, Hell, Kirkpatrick and Liu for g < f, without the component term (gf_factor_of_lt). The proof reduces the theorem to Tutte's f-factor theorem, imported as a lake dependency from PALOMAR-2026-10-18-000005, through a gadget: f(v) − g(v) slack vertices are joined to each vertex v, and the slack vertices together with one extra vertex form a clique, with target degree 1 on slack vertices and (Σ g) mod 2 on the extra vertex. One definition beyond Mathlib's (h(S,T), tightOddCount); g and f are natural-number valued.

**Sources.**

* László Lovász, *Subgraphs with prescribed valencies*, Journal of Combinatorial Theory 8 (1970), 391–416. [doi:10.1016/S0021-9800(70)80033-3](https://doi.org/10.1016/S0021-9800(70)80033-3) · [free full text](https://www.sciencedirect.com/science/article/pii/S0021980070800333/pdf)
* Katherine Heinrich, Pavol Hell, David G. Kirkpatrick, Guizhen Liu, *A simple existence criterion for (g < f)-factors*, Discrete Mathematics 85 (1990), 313–317. [doi:10.1016/0012-365X(90)90387-W](https://doi.org/10.1016/0012-365X(90)90387-W) · [free full text](https://doi.org/10.1016/0012-365x(90)90387-w)

<details><summary>Background references</summary>

* Mikio Kano, *[a,b]-factorization of a graph*, Thesis, Osaka University (1984), hdl:11094/27765, Lemma 2.2.

</details>

## Siegel's theorem on L(1, χ) for real Dirichlet characters

Palomar: [PALOMAR-2026-11-12-000005](https://palomar-registry.org/entry.html?id=PALOMAR-2026-11-12-000005&version=1) (version 1) · code: [jtraverso/siegel-theorem @ dbe9353](https://github.com/jtraverso/siegel-theorem/tree/dbe9353374a11317bdd2d436e264536258c5762f) · [archived copy](https://github.com/PalomarArchive/jtraverso--siegel-theorem--fcfb5ef237dc/tree/palomar/PALOMAR-2026-11-12-000005-v1/dbe9353374a11317bdd2d436e264536258c5762f)

**What is proved.** A Lean 4 / Mathlib proof of Siegel's theorem (1935): for every ε > 0 there is c > 0 with c·N^(-ε) ≤ ‖L(1, χ)‖ for every real non-principal Dirichlet character χ modulo N (SiegelThm.siegel, with Mathlib's DirichletCharacter.LFunction; χ need not be primitive). The proof is Goldfeld's (1974): F = ζ·L(χ₁)L(χ₂)L(χ₁χ₂) has non-negative Dirichlet coefficients with a₁ = 1; its regular part G = F − λ/(s−1) is expanded in a Taylor series at s = 2, with Cauchy's estimate on the circle |s−2| = 3/2 (where |G| ≤ 4000 (N₁N₂)²), giving ‖λ‖ ≥ (1−β)/2 · (50000 (N₁N₂)²)^(−4(1−β)) whenever Re F(β) ≤ 0 and 7/8 ≤ β < 1; Siegel's dichotomy (an exceptional zero in [1−ε/16, 1) or none, in which case χ₁ is the character mod 4) gives the ineffective constant. Characters that induce the same character as χ₁ are handled with the Euler factors (∏_{p∣n}(1−1/p) ≥ c(η)n^(−η)). Two auxiliary statements are also compared: the integral representation L(s, χ) = s∫_1^∞ A(t) t^(−s−1) dt on Re s > 0 (SiegelThm.LFunction_eq_integral, via Mathlib's Abel summation for Re s > 1, a Mellin-transform holomorphy argument and the identity theorem) and ‖∑_{k≤M} χ(k)‖ ≤ N (SiegelThm.norm_sum_Icc_le). Mathlib is the only dependency; Mathlib's continuation of ζ is not used (ζ(s) = 1/(s−1) + 1 − s∫_1^∞{t}t^(−s−1) dt is proved directly). Three statements; no definitions beyond Mathlib's.

**Sources.**

* Carl Ludwig Siegel, *Über die Classenzahl quadratischer Zahlkörper*, Acta Arithmetica 1 (1935), 83–86.
* Dorian Goldfeld, *A simple proof of Siegel's theorem*, Proc. Nat. Acad. Sci. USA 71 (1974), 1055. [doi:10.1073/pnas.71.4.1055](https://doi.org/10.1073/pnas.71.4.1055) · [free full text](https://pmc.ncbi.nlm.nih.gov/articles/PMC388160/)

<details><summary>Background references</summary>

* Hugh L. Montgomery, Robert C. Vaughan, *Multiplicative Number Theory I. Classical Theory*, Cambridge University Press, 2007, §11.2.

</details>

[← Back to the list](../README.md)
