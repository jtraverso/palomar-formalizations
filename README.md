# Formalizations registered in Palomar

Lean 4 / Mathlib formalizations by **Juan Pablo Traverso Gianini** that have been accepted
and registered in the [Palomar registry](https://palomar-registry.org). Each entry links to its
Palomar record, where the audited statements (`Challenge.lean`), the proofs, the mechanical
verification evidence and the review are kept, and to the source repository at the registered
commit.

This list is updated after each accepted submission.

| Palomar entry | Result | Registered | Source |
|---|---|---|---|
| [PALOMAR-2026-10-13-000005](https://palomar-registry.org/entry.html?id=PALOMAR-2026-10-13-000005&version=2) (v2) | Grötzsch's theorem, Ore's conjecture for k = 4 (Kostochka–Yancey), and the Grünbaum–Aksenov theorem | v1 2026-10-13, v2 2026-10-15 | [jtraverso/grotzsch-ore @ ff6d512](https://github.com/jtraverso/grotzsch-ore/tree/ff6d5123c06e4c99bb6074e0a72e8be8d595eefa) (v1: [f923c45](https://github.com/jtraverso/grotzsch-ore/tree/f923c459969d4a0a50d034cc02d558c7d4937436)) |
| [PALOMAR-2026-10-13-000007](https://palomar-registry.org/entry.html?id=PALOMAR-2026-10-13-000007&version=1) (v1) | The Hajnal–Szemerédi theorem on equitable colourings | 2026-10-13 | [jtraverso/hajnal-szemeredi @ ba34061](https://github.com/jtraverso/hajnal-szemeredi/tree/ba34061e3cf12dfc8297610d5d7b3f0afac7ec54) |
| [PALOMAR-2026-10-15-000003](https://palomar-registry.org/entry.html?id=PALOMAR-2026-10-15-000003&version=1) (v1) | The list chromatic index of complete graphs (Häggkvist–Janssen) | 2026-10-15 | [jtraverso/haggkvist-janssen @ 807e08b](https://github.com/jtraverso/haggkvist-janssen/tree/807e08bd7c480d4fae80c1b78377d23989d39ab0) |
| [PALOMAR-2026-10-15-000004](https://palomar-registry.org/entry.html?id=PALOMAR-2026-10-15-000004&version=1) (v1) | Vizing's theorem and equitable edge colourings | 2026-10-15 | [jtraverso/vizing @ 01c72ed](https://github.com/jtraverso/vizing/tree/01c72ed7efde2353a4bb1654f69b5c0bc5038863) |
| [PALOMAR-2026-10-15-000005](https://palomar-registry.org/entry.html?id=PALOMAR-2026-10-15-000005&version=1) (v1) | Wagner's planarity criterion and list colouring of planar and K₅-minor-free graphs | 2026-10-15 | [jtraverso/planar-list-colouring @ ec1eafb](https://github.com/jtraverso/planar-list-colouring/tree/ec1eafbc091713857eb5683a46e460902b2d47b3) |

## Entries

### Grötzsch's theorem, Ore's conjecture for k = 4, and the Grünbaum–Aksenov theorem

[PALOMAR-2026-10-13-000005](https://palomar-registry.org/entry.html?id=PALOMAR-2026-10-13-000005&version=2)
(version 2; version 1 contained the first two results)

Every finite triangle-free planar graph is 3-colourable (Grötzsch, 1959), deduced as in
Kostochka–Yancey (2014) from their proof of the case k = 4 of Ore's conjecture: every 4-critical
graph satisfies 3|E| ≥ 5|V| − 2, by the potential method. Planarity is defined combinatorially
(genus-zero rotation systems), and the topological crossing argument of the paper is replaced by
a K₅-minor argument with an apex inside a face. Sanity checks: K₄ is planar, K₅ and K₃,₃ are not.
Version 2 adds the Grünbaum–Aksenov theorem (every planar graph with at most three triangles is
3-colourable), following Borodin–Kostochka–Lidický–Yancey, together with their precolouring
extension theorems for 4- and 5-cycles and a combinatorial Jordan-curve (region) theorem for
rotation systems.

### The Hajnal–Szemerédi theorem

[PALOMAR-2026-10-13-000007](https://palomar-registry.org/entry.html?id=PALOMAR-2026-10-13-000007&version=1)

Every finite graph of maximum degree at most r has an equitable (r + 1)-colouring: the colour
classes differ in size by at most one (Hajnal–Szemerédi, 1970), following the short proof of
Kierstead and Kostochka (2008). Also the exact form: if |V| = s(r + 1), there is a proper
(r + 1)-colouring whose classes all have exactly s vertices.

### The list chromatic index of complete graphs (Häggkvist–Janssen)

[PALOMAR-2026-10-15-000003](https://palomar-registry.org/entry.html?id=PALOMAR-2026-10-15-000003&version=1)

The complete graph Kₙ can be edge-coloured from lists of size n assigned to its edges
(Häggkvist–Janssen, 1997): its list chromatic index is at most n. The proof goes through the
Alon–Tarsi polynomial method with a certificate built from permutations.

### Vizing's theorem and equitable edge colourings

[PALOMAR-2026-10-15-000004](https://palomar-registry.org/entry.html?id=PALOMAR-2026-10-15-000004&version=1)

Every finite simple graph has a proper edge colouring with Δ + 1 colours (Vizing, 1964), proved
with fans and Kempe chains; moreover, for every c ≥ Δ + 1 there is a proper edge colouring with
c colours whose colour classes differ in size by at most one (McDiarmid, 1972).

### Wagner's planarity criterion and list colouring

[PALOMAR-2026-10-15-000005](https://palomar-registry.org/entry.html?id=PALOMAR-2026-10-15-000005&version=1)

A finite graph is planar if and only if it has neither K₅ nor K₃,₃ as a minor (Wagner, 1937).
Every K₅-minor-free graph is 5-choosable (Škrekovski) and DP-5-colourable (Li–Wang); hence planar
graphs are 5-choosable (Thomassen) and DP-5-colourable (Dvořák–Postle). Some planar graph is not
4-choosable (Voigt). The Four Colour Theorem is equivalent to Hadwiger's conjecture for K₅
(Wagner), neither side being proved.

## Notes

* All entries are checked by Palomar's mechanical verification (Lean kernel and the independent
  nanoda checker); the proofs use only the axioms `propext`, `Classical.choice` and
  `Quot.sound`.
* The formalizations were written with AI assistance (Claude Code and Harmonic's Aristotle) under
  the author's direction; each entry's `formalization.yaml` describes the process.
