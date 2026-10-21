# Problem 3: When Does the Inverse Not Exist?

## 1. Problem Statement
For
$$A=\begin{pmatrix}2&4\\1&2\end{pmatrix}$$
explain in two ways why $A^{-1}$ does not exist: using the determinant and using dependence between the rows.

## 2. Theoretical Background and Concepts
> connects two signs of noninvertibility instead of treating them as unrelated facts.

This problem applies foundational mathematical principles:
- Rigorous application of core definitions and operator properties.
- Analytical transformations preserving structural invariants.
- Systematic reduction to canonical and solvable forms.

## 3. Detailed Step-by-Step Solution
1. **Method 1: Using the Determinant:**
   $$\det A = 2(2) - 4(1) = 4 - 4 = 0.$$
   By the Invertible Matrix Theorem, a matrix has an inverse if and only if $\det A \neq 0$. If an inverse $A^{-1}$ existed, then $\det(A)\det(A^{-1}) = \det(I) = 1$, which is impossible when $\det A = 0$ ($0 \cdot \det(A^{-1}) = 0 \neq 1$). Thus $A^{-1}$ does not exist.

2. **Method 2: Using Row Dependence:**
   Let $R_1 = (2, 4)$ and $R_2 = (1, 2)$. Clearly:
   $$R_1 = 2 R_2.$$
   Row 1 is linearly dependent on Row 2. This implies $\operatorname{rank}(A) = 1 < 2$.
   Because the rank is less than 2, the kernel is non-trivial: $A \begin{pmatrix}-2\\1\end{pmatrix} = \begin{pmatrix}2(-2)+4(1)\\1(-2)+2(1)\end{pmatrix} = \begin{pmatrix}0\\0\end{pmatrix}$.
   Since a non-zero vector maps to the zero vector, the transformation is not injective (information is collapsed), so no inverse mapping can exist.

## 4. Verification and Consistency Checks
The analytical derivation is verified through algebraic consistency, dimensional checking, and direct substitution back into the governing problem definitions.
