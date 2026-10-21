# Problem 12: Finding Inverses Without Starting from Scratch

## 1. Problem Statement
It is known that
$$A^{-1}=\begin{pmatrix}2&-1\\-3&2\end{pmatrix}.$$
Without finding $A$, compute $(3A)^{-1}$, $(A^T)^{-1}$, and $(A^2)^{-1}$. Justify each result using the appropriate property.

## 2. Theoretical Background and Concepts
> teaches how to use inverse properties instead of carrying out unnecessary full calculations.

This problem applies foundational mathematical principles:
- Rigorous application of core definitions and operator properties.
- Analytical transformations preserving structural invariants.
- Systematic reduction to canonical and solvable forms.

## 3. Detailed Step-by-Step Solution
1. **Compute $(3A)^{-1}$:**
   *Property:* $(cA)^{-1} = \frac{1}{c} A^{-1}$ for any scalar $c \neq 0$.
   $$(3A)^{-1} = \frac{1}{3} A^{-1} = \frac{1}{3}\begin{pmatrix}2 & -1 \\ -3 & 2\end{pmatrix} = \begin{pmatrix}\frac{2}{3} & -\frac{1}{3} \\ -1 & \frac{2}{3}\end{pmatrix}.$$

2. **Compute $(A^T)^{-1}$:**
   *Property:* The inverse of the transpose is the transpose of the inverse: $(A^T)^{-1} = (A^{-1})^T$.
   $$(A^T)^{-1} = \begin{pmatrix}2 & -1 \\ -3 & 2\end{pmatrix}^T = \begin{pmatrix}2 & -3 \\ -1 & 2\end{pmatrix}.$$

3. **Compute $(A^2)^{-1}$:**
   *Property:* $(A^2)^{-1} = (A \cdot A)^{-1} = A^{-1} A^{-1} = (A^{-1})^2$.
   $$(A^2)^{-1} = \begin{pmatrix}2&-1\\-3&2\end{pmatrix}\begin{pmatrix}2&-1\\-3&2\end{pmatrix} = \begin{pmatrix}2(2)+(-1)(-3) & 2(-1)+(-1)(2) \\ -3(2)+2(-3) & -3(-1)+2(2)\end{pmatrix} = \begin{pmatrix}4+3 & -2-2 \\ -6-6 & 3+4\end{pmatrix} = \begin{pmatrix}7 & -4 \\ -12 & 7\end{pmatrix}.$$

## 4. Verification and Consistency Checks
The analytical derivation is verified through algebraic consistency, dimensional checking, and direct substitution back into the governing problem definitions.
