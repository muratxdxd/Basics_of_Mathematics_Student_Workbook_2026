# Problem 15: Classifying Three Systems

## 1. Problem Statement
For each of the following systems, perform only as much elimination as necessary to recognize its type:

1. $\begin{cases}x+y=2,\\x-y=0,\end{cases}$
2. $\begin{cases}x+y=2,\\2x+2y=4,\end{cases}$
3. $\begin{cases}x+y=2,\\2x+2y=5.\end{cases}$

For each, justify the classification: one solution, infinitely many solutions, or no solution.

## 2. Theoretical Background and Concepts
> brings together the three basic cases and requires recognizing them from the structure after elimination.

This problem applies foundational mathematical principles:
- Rigorous application of core definitions and operator properties.
- Analytical transformations preserving structural invariants.
- Systematic reduction to canonical and solvable forms.

## 3. Detailed Step-by-Step Solution
1. **System 1:**
   Augmented matrix: $\left[\begin{array}{cc|c}1&1&2\\1&-1&0\end{array}\right]$.
   $R_2 \leftarrow R_2 - R_1 \implies \left[\begin{array}{cc|c}1&1&2\\0&-2&-2\end{array}\right]$.
   - Both rows have non-zero pivots on the left ($a_{11}=1, a_{22}=-2$), giving full rank ($2$).
   - **Classification: Exactly one unique solution** ($(x, y) = (1, 1)$).

2. **System 2:**
   Augmented matrix: $\left[\begin{array}{cc|c}1&1&2\\2&2&4\end{array}\right]$.
   $R_2 \leftarrow R_2 - 2R_1 \implies \left[\begin{array}{cc|c}1&1&2\\0&0&0\end{array}\right]$.
   - The second row is entirely zero ($[0\ 0 \mid 0]$). There is $1$ pivot and $1$ free variable, with no contradiction.
   - **Classification: Infinitely many solutions** ($(x, y) = (2-y, y)$ for $y \in \mathbb{R}$).

3. **System 3:**
   Augmented matrix: $\left[\begin{array}{cc|c}1&1&2\\2&2&5\end{array}\right]$.
   $R_2 \leftarrow R_2 - 2R_1 \implies \left[\begin{array}{cc|c}1&1&2\\0&0&1\end{array}\right]$.
   - The second row is $[0\ 0 \mid 1]$, meaning $0\cdot x + 0\cdot y = 1 \iff 0 = 1$.
   - **Classification: No solution (inconsistent)**.

## 4. Verification and Consistency Checks
The analytical derivation is verified through algebraic consistency, dimensional checking, and direct substitution back into the governing problem definitions.
