# Problem 8: Two Systems with the Same Coefficient Matrix

## 1. Problem Statement
Solve by elimination the two systems
$$\begin{cases}2x+y=5,\\x-y=1,\end{cases}$$
$$\begin{cases}2x+y=1,\\x-y=4.\end{cases}$$
Compare the successive elimination steps. Which part of the calculation is the same in both cases, and why?

## 2. Theoretical Background and Concepts
> shows the role of the coefficient matrix independently of the right-hand side.

This problem applies foundational mathematical principles:
- Rigorous application of core definitions and operator properties.
- Analytical transformations preserving structural invariants.
- Systematic reduction to canonical and solvable forms.

## 3. Detailed Step-by-Step Solution
1. **Joint Augmented Matrix:**
   Since both systems share $A = \begin{pmatrix}2&1\\1&-1\end{pmatrix}$, we can solve them simultaneously using $[A \mid b_1 \mid b_2]$:
   $$\left[\begin{array}{cc|cc} 2 & 1 & 5 & 1 \\ 1 & -1 & 1 & 4 \end{array}\right].$$

2. **Elimination Steps:**
   - Swap $R_1 \leftrightarrow R_2$:
     $$\left[\begin{array}{cc|cc} 1 & -1 & 1 & 4 \\ 2 & 1 & 5 & 1 \end{array}\right].$$
   - $R_2 \leftarrow R_2 - 2R_1$:
     Row 2 left: $(2-2, 1-2(-1)) = (0, 3)$.
     Row 2 right for $b_1$: $5 - 2(1) = 3$.
     Row 2 right for $b_2$: $1 - 2(4) = -7$.
     $$\left[\begin{array}{cc|cc} 1 & -1 & 1 & 4 \\ 0 & 3 & 3 & -7 \end{array}\right].$$

3. **Back-Substitution:**
   - **System 1:** $3y = 3 \implies y = 1$. Then $x - 1 = 1 \implies x = 2$.
     Solution 1: $(x, y) = (2, 1)$.
   - **System 2:** $3y = -7 \implies y = -\frac{7}{3}$. Then $x - (-\frac{7}{3}) = 4 \implies x = 4 - \frac{7}{3} = \frac{5}{3}$.
     Solution 2: $(x, y) = \left(\frac{5}{3}, -\frac{7}{3}\right)$.

4. **Comparison:**
   The row operations applied to the coefficient columns (swapping rows, subtracting $2R_1$) were **identical** in both systems. This is because the row operations needed to produce pivots and zeros are determined entirely by the entries of $A$, completely independent of the right-hand side vector $b$.

## 4. Verification and Consistency Checks
The analytical derivation is verified through algebraic consistency, dimensional checking, and direct substitution back into the governing problem definitions.
