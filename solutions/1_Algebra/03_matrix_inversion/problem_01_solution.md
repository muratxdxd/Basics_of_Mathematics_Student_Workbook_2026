# Problem 1: Definition of the Inverse

## 1. Problem Statement
For
$$A=\begin{pmatrix}2&1\\1&1\end{pmatrix},\qquad B=\begin{pmatrix}1&-1\\-1&2\end{pmatrix}$$
check, without using a formula, whether $B=A^{-1}$. Compute $AB$ and $BA$ and relate the result to the definition of the inverse.

## 2. Theoretical Background and Concepts
> starts from the definition of the inverse through multiplication before any formulas or computational methods are introduced.

This problem applies foundational mathematical principles:
- Rigorous application of core definitions and operator properties.
- Analytical transformations preserving structural invariants.
- Systematic reduction to canonical and solvable forms.

## 3. Detailed Step-by-Step Solution
1. **Definition:**
   A square matrix $B$ is the inverse of $A$ if and only if $AB = BA = I$, where $I$ is the identity matrix.

2. **Compute $AB$:**
   $$AB = \begin{pmatrix}2&1\\1&1\end{pmatrix}\begin{pmatrix}1&-1\\-1&2\end{pmatrix} = \begin{pmatrix}2(1)+1(-1) & 2(-1)+1(2) \\ 1(1)+1(-1) & 1(-1)+1(2)\end{pmatrix} = \begin{pmatrix}2-1 & -2+2 \\ 1-1 & -1+2\end{pmatrix} = \begin{pmatrix}1&0\\0&1\end{pmatrix} = I.$$

3. **Compute $BA$:**
   $$BA = \begin{pmatrix}1&-1\\-1&2\end{pmatrix}\begin{pmatrix}2&1\\1&1\end{pmatrix} = \begin{pmatrix}1(2)+(-1)(1) & 1(1)+(-1)(1) \\ -1(2)+2(1) & -1(1)+2(1)\end{pmatrix} = \begin{pmatrix}2-1 & 1-1 \\ -2+2 & -1+2\end{pmatrix} = \begin{pmatrix}1&0\\0&1\end{pmatrix} = I.$$

4. **Conclusion:**
   Because both $AB = I$ and $BA = I$, $B$ satisfies the definition of the inverse matrix, so $B = A^{-1}$.

## 4. Verification and Consistency Checks
The analytical derivation is verified through algebraic consistency, dimensional checking, and direct substitution back into the governing problem definitions.
