# A conditional construction of a hereditarily atomic domain without ACCP

This repository contains an AI-written mathematics manuscript, as LaTeX source (`main.tex`) and as a compiled PDF. The PDF was compiled with Tectonic 0.17.0. It addresses a conjecture of Coykendall, Gotti and Hasenauer: every hereditarily atomic integral domain satisfies the ascending chain condition on principal ideals (ACCP).

**The main result is conditional.** The manuscript does not claim a counterexample to the conjecture. It reduces one to an explicit arithmetic existence problem, stated in the manuscript's final section as a one-step extension hypothesis, that remains open.

The existence problem is expected to have a positive answer on heuristic grounds. In random-matrix models, supported by computations in model towers over the first few steps (some conditional on GRH), the Selmer condition holds at a positive proportion of candidate steps. For steps of the kind the construction uses, the models predict a proportion that does not decay from step to step. The odd unit condition rarely fails. Each step has infinitely many candidates, so one expects a successful step at every stage. These heuristics are not part of the manuscript, and no independence result for the relevant units is proved. In the maintainer's view, a proof appears to be beyond current methods in algebraic number theory. The conditional construction does not disprove the conjecture, but it is evidence that the conjecture is likely false.

## Background

- A domain is **atomic** if every nonzero nonunit can be written as a finite product of irreducible elements.
- A domain satisfies **ACCP** if every ascending chain of principal ideals stabilizes. ACCP implies atomicity, but the converse fails.
- A domain is **hereditarily atomic** if all of its subrings are atomic.

Coykendall, Gotti and Hasenauer conjectured that every hereditarily atomic domain satisfies ACCP ([Hereditarily atomic integral domains](https://arxiv.org/abs/2112.00264v1), Conjecture 6.1). The manuscript looks for a counterexample among rings of algebraic integers.

Theorem A also answers a question raised by Coykendall and Hasenauer at the end of Section 7 of [Norms, Normsets, and Factorization](https://arxiv.org/abs/2406.14803v1): are atomicity, ACCP and the bounded factorization property equivalent for almost Dedekind domains? They are not: Theorem A gives an almost Dedekind domain that is atomic but does not satisfy ACCP.

## Results

**Theorem A (unconditional).** There is a tower
$\mathbb Q(\sqrt{65})=F_0\subset F_1\subset F_2\subset\cdots$
of totally real number fields with $[F_n:F_{n-1}]=2$ such that the ring of integers $D$ of $\bigcup_n F_n$:

- is an almost Dedekind domain;
- is atomic;
- does not satisfy ACCP;
- has exactly two non-invertible maximal ideals, with residue fields $\mathbb F_{47}$ and $\mathbb F_7$.

**Theorem B (conditional).** Suppose the tower is built from the manuscript's "scaled steps" and satisfies its structural hypotheses (T1)–(T6). Suppose further that every sufficiently late step $F_n/F_{n-1}$ satisfies two arithmetic conditions:

- **(S)** a Selmer condition: an explicit $\mathbb F_2$-linear map, defined by Hilbert symbols at the two dyadic primes, is injective;
- **(O)** an odd unit condition: for each odd prime $p$ ramified in $F_n$, one explicit vector lies in the $\mathbb Z_p$-span of the images of certain relative units in a product of local unit quotients.

Then $D$ is hereditarily atomic and does not satisfy ACCP; such a tower would disprove the conjecture.

## Authorship and verification status

The manuscript, including all exposition and proofs, was jointly produced by the AI models GPT-6 Astra and Claude Opus 5.5 under human coordination. The author field is intentionally blank.

**No human verification is claimed.**

The manuscript was thoroughly and carefully audited by separate instances of GPT-6 Astra and Claude Opus 5.5, the same models that wrote it, but it has not been verified by a human. The repository's maintainer is an algebraist, not a number theorist, and lacks the background to verify many of the claims. Independent checks and corrections are welcome; please report them as GitHub issues.

## Lean formalization

The unconditional construction (Theorem A) and the conditional implication (from the simultaneous-extension hypothesis to a hereditarily atomic domain without ACCP) have been formalized in Lean 4, in code written by GPT-6 Astra. The hypothesis itself is not proved. No human has yet checked that the formal statements match the manuscript's statements. The Lean code will be added to this repository.

## License

This work is dedicated to the public domain under [CC0 1.0 Universal](https://creativecommons.org/publicdomain/zero/1.0/); the full legal code is in [`LICENSE`](LICENSE). The manuscript is AI-generated and may not be protected by copyright in some jurisdictions. To the extent possible under law, all copyright and related or neighboring rights in the manuscript and this repository are waived. You may copy, modify, distribute and use the work, including commercially, without asking permission.
