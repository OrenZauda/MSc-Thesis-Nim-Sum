# On Fraenkel's 3-Dimensional Wythoff Conjectures

**MSc Thesis in Computer Science, Ariel University (May 2024)**
**Author:** Oren Zauda · **Supervisor:** Dr. Gabriel Nivasch

📄 [Read the full thesis (PDF)](Oren_Zauda_Thesis.pdf)

---

## Background

**Wythoff's game** is a classic two-player combinatorial game. There are two piles of counters. On each turn a player removes any number of counters from one pile, or the same number from both piles. The player who takes the last counter wins.

The losing positions for the player about to move are called **P-positions**. They have a well-known closed form tied to the **golden ratio** φ = (1+√5)/2:

$$a_n = \lfloor \varphi n \rfloor, \qquad b_n = \lfloor \varphi^2 n \rfloor$$

In 2004, **Aviezri Fraenkel** proposed a generalization to N piles. A move removes counters from a single pile, or removes amounts from several piles whose **nim-sum (bitwise XOR) is zero**. Fraenkel conjectured that, in the 3-pile version, the P-positions in each layer stay close to the golden-ratio structure of the original game:

- **Conjecture 5:** for each layer *z*, the P-positions stay within a constant distance of (φn, φ²n).
- **Conjecture 6:** from some point on, the P-positions occupy diagonals in sequential order.

These conjectures are still open. Sun and Zeilberger proved them for the first 10 layers, and showed that Conjecture 5 implies Conjecture 6.

## Contributions

To study the problem abstractly, the thesis introduces **P-like sequences**. These are sequences of points in ℕ² that share the structural properties of each layer's P-position sequence. Every row, column and diagonal holds at most one point, and the rows and columns together cover ℕ. The main results are:

- **Theorem 12 (conditional result):** if a natural conjecture about *bounded* P-like sequences holds, then Fraenkel's Conjecture 5 holds for every layer, apart from the lower bound on bₙ.
- **Theorems 13 & 14 (equivalence):** for any P-like sequence, the following two kinds of conditions imply each other, with explicit constants in φ:
  - **Growth bounds:** |aₙ − φn| and bₙ − φ²n are bounded by a constant.
  - **Structural bounds:** each point skips a bounded number of diagonals, and consecutive rows have bounded gaps (aₙ₊₁ − aₙ).
- **Computational experiments:** P-positions were computed for layers 0, 1, 5 and 30. The data shows that the distance from (φn, φ²n) stays bounded and that diagonals are eventually filled in order. Both observations agree with Fraenkel's conjectures.

The full conjecture remains open. These results reduce it to a simpler statement about bounded P-like sequences.

## Thesis structure

1. **Introduction:** Wythoff's game, P/N-positions, Beatty's theorem, Fraenkel's generalization and conjectures, P-like sequences
2. **Proofs:** Theorems 12, 13 and 14
3. **Experimental Results:** distance from (φn, φ²n) and diagonal-occupation order in layers 0, 1, 5 and 30
4. **Bibliography**

## Key references

- A. S. Fraenkel, "Complexity, appeal and challenges of combinatorial games," *Theoretical Computer Science*, 313(3), 2004.
- X. Sun and D. Zeilberger, "On Fraenkel's n-heap Wythoff's conjectures," *Annals of Combinatorics*, 8(2), 2004.
- X. Sun, "Wythoff's sequence and n-heap Wythoff's conjectures," *Discrete Mathematics*, 300(1), 2005.
- G. Nivasch, "More on the Sprague-Grundy function for Wythoff's game," *Games of No Chance 3*, 2009.
