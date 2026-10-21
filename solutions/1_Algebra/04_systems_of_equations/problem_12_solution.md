# Problem 12: Homogeneous System

## 1. Problem Statement
Solve
$$\begin{cases}x+2y-z=0,\\2x+4y-2z=0,\\x-y+2z=0.\end{cases}$$
Give all solutions in parametric form and explain why $(0,0,0)$ always satisfies a homogeneous system.

## 2. Theoretical Background and Concepts
> shows the special case of a system with a zero right-hand side without introducing additional theory.

This problem applies foundational mathematical principles:
- Rigorous application of core definitions and operator properties.
- Analytical transformations preserving structural invariants.
- Systematic reduction to canonical and solvable forms.

## 3. Detailed Step-by-Step Solution
1. **Augmented Matrix and Elimination:**
   $$\left[\begin{array}{ccc|c} 1 & 2 & -1 & 0 \\ 2 & 4 & -2 & 0 \\ 1 & -1 & 2 & 0 \end{array}\right].$$
   - $R_2 \leftarrow R_2 - 2R_1 \implies (0, 0, 0 \mid 0)$.
   - $R_3 \leftarrow R_3 - R_1 \implies (0, -3, 3 \mid 0)$.
   Swap $R_2 \leftrightarrow R_3$ and divide new $R_2$ by $-3$:
   $$\left[\begin{array}{ccc|c} 1 & 2 & -1 & 0 \\ 0 & 1 & -1 & 0 \\ 0 & 0 & 0 & 0 \end{array}\right].$$

2. **Parametric Solution:**
   - From Row 2: $y - z = 0 \implies y = z$.
   - Free variable: $z = t \in \mathbb{R}$.
   - From Row 1: $x + 2y - z = 0 \implies x + 2t - t = 0 \implies x = -t$.
   $$\begin{pmatrix}x \\ y \\ z\end{pmatrix} = t \begin{pmatrix}-1 \\ 1 \\ 1\end{pmatrix}, \quad t \in \mathbb{R}.$$

3. **Why $(0,0,0)$ Always Satisfies a Homogeneous System:**
   In matrix notation, a homogeneous system is $Ax = 0$. For any matrix $A$:
   $$A \cdot \mathbf{0} = \mathbf{0}$$
   because each entry is a sum of products where every product involves 0: $\sum_j a_{ij}\cdot 0 = 0$. Hence $x = (0,0,0)$ is always a solution (the trivial solution).

## 4. Verification and Consistency Checks
The analytical derivation is verified through algebraic consistency, dimensional checking, and direct substitution back into the governing problem definitions.
