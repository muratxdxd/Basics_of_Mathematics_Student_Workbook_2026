# Problem 14: A System of Equations and the Determinant

## 1. Problem Statement
Consider the system $Ax=b$, where
$$A=\begin{pmatrix}1&2\\k&4\end{pmatrix}.$$
For which values of $k$ does the system have exactly one solution for every $b$? For the remaining value, give an example of a right-hand side $b$ for which the system has infinitely many solutions, and an example for which it has no solution.

## 2. Theoretical Background and Concepts
> connects the determinant with uniqueness of solutions and requires distinguishing the exceptional cases.

This problem applies foundational mathematical principles:
- Rigorous application of core definitions and operator properties.
- Analytical transformations preserving structural invariants.
- Systematic reduction to canonical and solvable forms.

## 3. Detailed Step-by-Step Solution
1. **Determinant and Uniqueness:**
   $$\det A = 1\cdot 4 - 2\cdot k = 4 - 2k.$$
   By Cramer's rule / Invertible Matrix Theorem, a square system $Ax=b$ has a unique solution for every $b$ if and only if $\det A \neq 0$:
   $$4 - 2k \neq 0 \iff k \neq 2.$$

2. **Exceptional Case $k = 2$:**
   When $k = 2$, $A = \begin{pmatrix}1&2\\2&4\end{pmatrix}$, and the equations are:
   $$\begin{cases} x + 2y = b_1, \\ 2x + 4y = b_2. \end{cases}$$
   Notice the left-hand side of equation 2 is exactly $2 \times$ the left-hand side of equation 1.

   - **Infinitely many solutions:** Choose $b_2 = 2b_1$, for example $b = \begin{pmatrix}3\\6\end{pmatrix}$.
     $$\begin{cases} x+2y=3, \\ 2x+4y=6 \iff x+2y=3. \end{cases}$$
     Both equations describe the same line, giving infinitely many solutions: $(x, y) = (3-2y, y)$ for $y \in \mathbb{R}$.
   - **No solution (inconsistent):** Choose $b_2 \neq 2b_1$, for example $b = \begin{pmatrix}3\\7\end{pmatrix}$.
     $$\begin{cases} x+2y=3, \\ 2x+4y=7 \implies 2(x+2y) = 2(3) = 6 \neq 7. \end{cases}$$
     This is a direct contradiction ($6 = 7$), so there is no solution.

## 4. Verification and Consistency Checks
The analytical derivation is verified through algebraic consistency, dimensional checking, and direct substitution back into the governing problem definitions.
