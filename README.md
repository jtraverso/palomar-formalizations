# Formalizations registered in Palomar

Lean 4 / Mathlib formalizations by **Juan Pablo Traverso Gianini** that have been accepted
and registered in the [Palomar registry](https://palomar-registry.org). Each entry links to its
Palomar record, where the audited statements (`Challenge.lean`), the proofs, the mechanical
verification evidence and the review are kept, and to the source repository at the registered
commit.

This list is updated after each accepted submission.

| Palomar entry | Result | Registered | Source |
|---|---|---|---|
| [PALOMAR-2026-10-13-000005](https://palomar-registry.org/entry.html?id=PALOMAR-2026-10-13-000005&version=1) (v1) | Grötzsch's theorem and Ore's conjecture for k = 4 (Kostochka–Yancey) | 2026-10-13 | [jtraverso/grotzsch-ore @ f923c45](https://github.com/jtraverso/grotzsch-ore/tree/f923c459969d4a0a50d034cc02d558c7d4937436) |
| [PALOMAR-2026-10-13-000007](https://palomar-registry.org/entry.html?id=PALOMAR-2026-10-13-000007&version=1) (v1) | The Hajnal–Szemerédi theorem on equitable colourings | 2026-10-13 | [jtraverso/hajnal-szemeredi @ ba34061](https://github.com/jtraverso/hajnal-szemeredi/tree/ba34061e3cf12dfc8297610d5d7b3f0afac7ec54) |

## Entries

### Grötzsch's theorem and Ore's conjecture for k = 4

[PALOMAR-2026-10-13-000005](https://palomar-registry.org/entry.html?id=PALOMAR-2026-10-13-000005&version=1)

Every finite triangle-free planar graph is 3-colourable (Grötzsch, 1959), deduced as in
Kostochka–Yancey (2014) from their proof of the case k = 4 of Ore's conjecture: every 4-critical
graph satisfies 3|E| ≥ 5|V| − 2, by the potential method. Planarity is defined combinatorially
(genus-zero rotation systems), and the topological crossing argument of the paper is replaced by
a K₅-minor argument with an apex inside a face. Sanity checks: K₄ is planar, K₅ and K₃,₃ are not.

### The Hajnal–Szemerédi theorem

[PALOMAR-2026-10-13-000007](https://palomar-registry.org/entry.html?id=PALOMAR-2026-10-13-000007&version=1)

Every finite graph of maximum degree at most r has an equitable (r + 1)-colouring: the colour
classes differ in size by at most one (Hajnal–Szemerédi, 1970), following the short proof of
Kierstead and Kostochka (2008). Also the exact form: if |V| = s(r + 1), there is a proper
(r + 1)-colouring whose classes all have exactly s vertices.

## Notes

* All entries are checked by Palomar's mechanical verification (Lean kernel and the independent
  nanoda checker); the proofs use only the axioms `propext`, `Classical.choice` and
  `Quot.sound`.
* The formalizations were written with AI assistance (Claude Code and Harmonic's Aristotle) under
  the author's direction; each entry's `formalization.yaml` describes the process.
