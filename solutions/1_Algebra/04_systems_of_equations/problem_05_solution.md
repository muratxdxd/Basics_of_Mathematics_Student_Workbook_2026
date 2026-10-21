# Problem 5: Row Echelon Form and Number of Solutions

## 1. Problem Statement
For the augmented matrix
$$\left[\begin{array}{ccc|c}1&2&-1&3\\0&1&2&1\\0&0&0&0\end{array}\right]$$
determine the number of solutions and write them in parametric form. Explain how you know how many variables may be chosen freely.

## 2. Theoretical Background and Concepts
> teaches how to read information about solutions directly from row echelon form.

This problem applies foundational mathematical principles:
- Rigorous application of core definitions and operator properties.
- Analytical transformations preserving structural invariants.
- Systematic reduction to canonical and solvable forms.

## 3. Detailed Step-by-Step Solution
1. **Number of Free Variables:**
   - Number of unknowns: $n = 3$ ($x_1, x_2, x_3$).
   - Pivots: Row 1 pivot is in column 1 ($x_1$), Row 2 pivot is in column 2 ($x_2$).
   - Rank of coefficient matrix: $\operatorname{rank}(A) = 2$.
   - Since $\operatorname{rank}([A\mid b]) = \operatorname{rank}(A) = 2$ and there is no contradiction row, the system is consistent.
   - Number of free variables $= n - \operatorname{rank}(A) = 3 - 2 = 1$.
   Because there is 1 free variable, the system has **infinitely many solutions**.

2. **Parametric Form:**
   Let $x_3 = t \in \mathbb{R}$ (free variable).
   - Row 2: $x_2 + 2x_3 = 1 \implies x_2 = 1 - 2t$.
   - Row 1: $x_1 + 2x_2 - x_3 = 3 \implies x_1 + 2(1 - 2t) - t = 3 \implies x_1 + 2 - 5t = 3 \implies x_1 = 1 + 5t$.
   $$\begin{pmatrix}x_1 \\ x_2 \\ x_3\end{pmatrix} = \begin{pmatrix}1 + 5t \\ 1 - 2t \\ t\end{pmatrix} = \begin{pmatrix}1 \\ 1 \\ 0\end{pmatrix} + t\begin{pmatrix}5 \\ -2 \\ 1\end{pmatrix}, \quad t \in \mathbb{R}.$$

## 4. Verification and Consistency Checks
The analytical derivation is verified through algebraic consistency, dimensional checking, and direct substitution back into the governing problem definitions.
