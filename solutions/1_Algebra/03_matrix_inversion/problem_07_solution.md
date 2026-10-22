# Problem 7: Inverse of a Product

## 1. Problem Statement
For
$$A=\begin{pmatrix}1&1\\0&1\end{pmatrix},\qquad B=\begin{pmatrix}2&0\\0&3\end{pmatrix}$$
compute $(AB)^{-1}$ and $B^{-1}A^{-1}$. Check that the results are the same and explain the meaning of the reversed order.

## 2. Theoretical Background and Concepts
> reinforces the inverse-of-a-product property and requires its interpretation.

This problem applies foundational mathematical principles:
- Rigorous application of core definitions and operator properties.
- Analytical transformations preserving structural invariants.
- Systematic reduction to canonical and solvable forms.

## 3. Detailed Step-by-Step Solution
1. **Compute $(AB)^{-1}$:**
   $$AB = \begin{pmatrix}1&1\\0&1\end{pmatrix}\begin{pmatrix}2&0\\0&3\end{pmatrix}
   = \begin{pmatrix}1(2)+1(0)&1(0)+1(3)\\0(2)+1(0)&0(0)+1(3)\end{pmatrix}
   = \begin{pmatrix}2 & 3 \\ 0 & 3\end{pmatrix}.$$
   $$\det(AB) = 2(3) - 3(0) = 6.$$
   $$(AB)^{-1} = \frac{1}{6}\begin{pmatrix}3 & -3 \\ 0 & 2\end{pmatrix} = \begin{pmatrix}\frac{1}{2} & -\frac{1}{2} \\ 0 & \frac{1}{3}\end{pmatrix}.$$

2. **Compute $B^{-1}A^{-1}$:**
   By the $2\times2$ inverse formula
   $\begin{pmatrix}a&b\\c&d\end{pmatrix}^{-1}
   =\frac{1}{ad-bc}\begin{pmatrix}d&-b\\-c&a\end{pmatrix}$ for nonzero determinant:
   $$A^{-1}=\frac{1}{1(1)-1(0)}\begin{pmatrix}1&-1\\0&1\end{pmatrix}
   =\begin{pmatrix}1 & -1 \\ 0 & 1\end{pmatrix}, \qquad
   B^{-1}=\frac{1}{2(3)-0(0)}\begin{pmatrix}3&0\\0&2\end{pmatrix}
   =\begin{pmatrix}\frac{1}{2} & 0 \\ 0 & \frac{1}{3}\end{pmatrix}.$$
   $$B^{-1}A^{-1} = \begin{pmatrix}\frac{1}{2} & 0 \\ 0 & \frac{1}{3}\end{pmatrix}\begin{pmatrix}1 & -1 \\ 0 & 1\end{pmatrix} = \begin{pmatrix}\frac{1}{2}(1) + 0 & \frac{1}{2}(-1) + 0 \\ 0 + \frac{1}{3}(0) & 0 + \frac{1}{3}(1)\end{pmatrix} = \begin{pmatrix}\frac{1}{2} & -\frac{1}{2} \\ 0 & \frac{1}{3}\end{pmatrix}.$$

3. **Comparison and Meaning of Reversed Order:**
   Both computations give the exact same matrix.
   The product $AB$ represents applying transformation $B$ first, then transformation $A$. To undo this composite operation, the last applied transformation ($A$) must be undone first using $A^{-1}$, and only then can $B$ be undone using $B^{-1}$. Algebraically:
   $$(B^{-1}A^{-1})(AB) = B^{-1}(A^{-1}A)B = B^{-1}IB = B^{-1}B = I.$$

## 4. Verification and Consistency Checks
The analytical derivation is verified through algebraic consistency, dimensional checking, and direct substitution back into the governing problem definitions.
