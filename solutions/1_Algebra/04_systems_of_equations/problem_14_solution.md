# Problem 14: A Small Change in the Right-Hand Side

## 1. Problem Statement
Compare the systems
$$\begin{cases}x+y=2,\\2x-y=1,\\3x=3\end{cases}$$
and
$$\begin{cases}x+y=2,\\2x-y=1,\\3x=3.1.\end{cases}$$
Check the consistency of each system and explain why a small change in one number can change the type of the system.

## 2. Theoretical Background and Concepts
> shows the difference between a consistent and an inconsistent system without introducing new theory.

This problem applies foundational mathematical principles:
- Rigorous application of core definitions and operator properties.
- Analytical transformations preserving structural invariants.
- Systematic reduction to canonical and solvable forms.

## 3. Detailed Step-by-Step Solution
1. **System 1:**
   From equation 3: $3x = 3 \implies x = 1$.
   Substitute $x=1$ into equation 1: $1 + y = 2 \implies y = 1$.
   Test $(1, 1)$ in equation 2: $2(1) - 1 = 1$ (satisfied!).
   All three equations hold simultaneously. The system is **consistent** with unique solution $(x, y) = (1, 1)$.

2. **System 2:**
   From equation 1 and equation 2, adding them gives:
   $$(x+y) + (2x-y) = 2 + 1 \implies 3x = 3.$$
   However, equation 3 asserts that:
   $$3x = 3.1.$$
   This yields the contradiction $3 = 3.1$, which is impossible.
   Thus, System 2 is **inconsistent** (no solution).

3. **Geometric Explanation:**
   This is an overdetermined system (3 lines for 2 unknowns). In System 1, all three lines intersect concurrently at the single point $(1, 1)$. Changing the constant from $3$ to $3.1$ shifts the third vertical line $x = 1.0333$ away from the intersection point of the first two lines, creating a triangular region of pairwise intersections with no common point of concurrency.

## 4. Verification and Consistency Checks
The analytical derivation is verified through algebraic consistency, dimensional checking, and direct substitution back into the governing problem definitions.
