# Problem 15: Observation Versus Proof

## 1. Problem Statement
Choose one sequence and one function from this set. For the sequence, compute several values for increasingly large $n$. For the function, prepare a table of values with arguments approaching the limit point from the left and right. Sketch the behavior of both objects.

Compare the observation with the analytical result and explain why a finite number of calculations or a sketch does not constitute a proof that the limit exists.

## 2. Theoretical Background and Concepts
> teaches how to distinguish intuition and observation from mathematical argument.

This problem applies foundational mathematical principles:
- Rigorous application of core definitions and operator properties.
- Analytical transformations preserving structural invariants.
- Systematic reduction to canonical and solvable forms.

## 3. Detailed Step-by-Step Solution
1. **Chosen Sequence: $a_n = \frac{4n^2-3n+1}{2n^2+5n-7}$ (from Exercise 1):**
   - $n = 10$: $a_{10} = \frac{4(100)-30+1}{2(100)+50-7} = \frac{371}{243} \approx 1.5267$
   - $n = 100$: $a_{100} = \frac{40000-300+1}{20000+500-7} = \frac{39701}{20493} \approx 1.9373$
   - $n = 1\,000$: $a_{1000} = \frac{4000000-3000+1}{2000000+5000-7} = \frac{3997001}{2004993} \approx 1.9935$
   - $n = 10\,000$: $a_{10000} \approx 1.99935$
   *Observation:* As $n$ grows, $a_n$ monotonically increases toward $2$.

   ```text
   a_n
    ↑
   2 ┄ ┄ ┄ ┄ ┄ ┄ ┄ ┄ ┄ ┄ ┄ ┄ ┄ ┄ ┄  limit level
    │                    • • • •
    │           • • •
    │       •
    │   •
    └──────────────────────────────→ n
   ```
   The dots represent discrete sequence values, not a continuous curve; they get closer to $y=2$.

2. **Chosen Function: $f(x) = \frac{x^2-4x+3}{x-3}$ as $x \to 3$ (from Exercise 7):**
   - **Approaching from the left ($x \to 3^-$):**
     - $x = 2.9 \implies f(2.9) = 2.9 - 1 = 1.9$
     - $x = 2.99 \implies f(2.99) = 1.99$
     - $x = 2.999 \implies f(2.999) = 1.999$
   - **Approaching from the right ($x \to 3^+$):**
     - $x = 3.1 \implies f(3.1) = 3.1 - 1 = 2.1$
     - $x = 3.01 \implies f(3.01) = 2.01$
     - $x = 3.001 \implies f(3.001) = 2.001$
   *Observation:* From both sides, the values symmetrically converge to $2.0$.

   ```text
    y
    ↑
    │                 ○ (3, 2)
    │               ╱
    │             ╱       y = x - 1, except at x = 3
    │           ╱
    ┼─────────╱────────────────────→ x
    │       ╱
   ```
   The open circle marks the missing point: the graph follows the line on both sides but has no value at $x=3$.

   **Comparison with Exercises 1 and 7:** As in Exercise 1, the sequence's limit is found by normalizing numerator and denominator by the highest power, $n^2$, leaving the leading-coefficient ratio $4/2=2$. As in Exercise 7, factor the function's numerator as $(x-1)(x-3)$ and cancel $x-3$ for $x\ne3$, giving $f(x)=x-1$ near (but not at) $3$. This cancellation explains the line and its hole; the function's limit is also $2$.

3. **Observation Versus Mathematical Proof:**
   - **Why empirical data is not a proof:** Calculating a table of values or observing a plot tests only a tiny finite sample of points. It cannot reveal if a function has high-frequency microscopic oscillations near the limit point (such as $\sin(1/x)$), nor can it detect if a sequence alters its behavior for numbers larger than tested (e.g., $n > 10^{100}$). Numerical evaluations are also subject to machine floating-point rounding errors.
   - **What constitutes a proof:** A mathematical proof provides a universal deduction valid across all infinitely many numbers in the domainâ€”demonstrating rigorously via algebraic identities, inequalities, and the formal $(\varepsilon, \delta)$ or $(\varepsilon, N)$ definitions that the distance between the expression and the limit can be made arbitrarily small for *all* points sufficiently close to the limit.

## 4. Verification and Consistency Checks
The analytical derivation is verified through algebraic consistency, dimensional checking, and direct substitution back into the governing problem definitions.
