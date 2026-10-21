# Problem 4: Infinitely Many Solutions

## 1. Problem Statement
Solve
$$\begin{cases}x+y+z=2,\\2x+2y+2z=4,\\x-y+z=0.\end{cases}$$
Give the solution in parametric form, identify a free variable, and for one chosen parameter value check that the resulting point really satisfies the system.

## 2. Theoretical Background and Concepts
> shows the case of multiple solutions and teaches a simple parametric description.

This problem applies foundational mathematical principles:
- Rigorous application of core definitions and operator properties.
- Analytical transformations preserving structural invariants.
- Systematic reduction to canonical and solvable forms.

## 3. Detailed Step-by-Step Solution
1. **Augmented Matrix and Elimination:**
   $$\left[\begin{array}{ccc|c} 1 & 1 & 1 & 2 \\ 2 & 2 & 2 & 4 \\ 1 & -1 & 1 & 0 \end{array}\right].$$
   - $R_2 \leftarrow R_2 - 2R_1 \implies (0, 0, 0 \mid 0)$.
   - $R_3 \leftarrow R_3 - R_1 \implies (0, -2, 0 \mid -2)$.
   Swap $R_2 \leftrightarrow R_3$:
   $$\left[\begin{array}{ccc|c} 1 & 1 & 1 & 2 \\ 0 & -2 & 0 & -2 \\ 0 & 0 & 0 & 0 \end{array}\right].$$

2. **Parametric Solution:**
   - From Row 2: $-2y = -2 \implies y = 1$.
   - The third column has no pivot, so $z$ is the **free variable**. Let $z = t \in \mathbb{R}$.
   - From Row 1: $x + 1 + t = 2 \implies x = 1 - t$.
   $$\begin{pmatrix}x \\ y \\ z\end{pmatrix} = \begin{pmatrix}1 - t \\ 1 \\ t\end{pmatrix} = \begin{pmatrix}1 \\ 1 \\ 0\end{pmatrix} + t\begin{pmatrix}-1 \\ 0 \\ 1\end{pmatrix}, \quad t \in \mathbb{R}.$$

3. **Check for Parameter Value $t = 2$:**
   Point: $(x, y, z) = (1-2, 1, 2) = (-1, 1, 2)$.
   - Eq 1: $-1 + 1 + 2 = 2$ (holds).
   - Eq 2: $2(-1) + 2(1) + 2(2) = -2 + 2 + 4 = 4$ (holds).
   - Eq 3: $-1 - 1 + 2 = 0$ (holds).

## 4. Verification and Consistency Checks
The analytical derivation is verified through algebraic consistency, dimensional checking, and direct substitution back into the governing problem definitions.
