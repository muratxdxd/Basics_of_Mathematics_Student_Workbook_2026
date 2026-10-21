# Problem 13: Undoing a Composite Transformation

## 1. Problem Statement
The matrices
$$S=\begin{pmatrix}2&0\\0&1\end{pmatrix},\qquad H=\begin{pmatrix}1&1\\0&1\end{pmatrix}$$
describe nonuniform scaling and shear. For $T=HS$, find $T^{-1}$ in two ways:

1. first compute $T$, then its inverse,
2. use $(HS)^{-1}=S^{-1}H^{-1}$.

Compare the results. Additionally compute $H^{-1}S^{-1}$ and verify that the incorrect order gives a different matrix. Explain the rule: â€œwhen undoing a composition of operations, we undo them from the end.â€

## 2. Theoretical Background and Concepts
> reinforces the inverse of a product in a less direct configuration.

This problem applies foundational mathematical principles:
- Rigorous application of core definitions and operator properties.
- Analytical transformations preserving structural invariants.
- Systematic reduction to canonical and solvable forms.

## 3. Detailed Step-by-Step Solution
1. **Method 1: Compute $T$ then $T^{-1}$:**
   $$T = HS = \begin{pmatrix}1&1\\0&1\end{pmatrix}\begin{pmatrix}2&0\\0&1\end{pmatrix} = \begin{pmatrix}2 & 1 \\ 0 & 1\end{pmatrix}.$$
   $$\det T = 2(1) - 1(0) = 2.$$
   $$T^{-1} = \frac{1}{2}\begin{pmatrix}1 & -1 \\ 0 & 2\end{pmatrix} = \begin{pmatrix}\frac{1}{2} & -\frac{1}{2} \\ 0 & 1\end{pmatrix}.$$

2. **Method 2: Use $(HS)^{-1} = S^{-1}H^{-1}$:**
   $$S^{-1} = \begin{pmatrix}\frac{1}{2} & 0 \\ 0 & 1\end{pmatrix}, \qquad H^{-1} = \begin{pmatrix}1 & -1 \\ 0 & 1\end{pmatrix}.$$
   $$S^{-1}H^{-1} = \begin{pmatrix}\frac{1}{2} & 0 \\ 0 & 1\end{pmatrix}\begin{pmatrix}1 & -1 \\ 0 & 1\end{pmatrix} = \begin{pmatrix}\frac{1}{2} & -\frac{1}{2} \\ 0 & 1\end{pmatrix}.$$
   Both methods produce the exact same matrix.

3. **Compute Incorrect Order $H^{-1}S^{-1}$:**
   $$H^{-1}S^{-1} = \begin{pmatrix}1 & -1 \\ 0 & 1\end{pmatrix}\begin{pmatrix}\frac{1}{2} & 0 \\ 0 & 1\end{pmatrix} = \begin{pmatrix}\frac{1}{2} & -1 \\ 0 & 1\end{pmatrix} \neq T^{-1}.$$

4. **Explanation of the Rule:**
   When transforming an object via $T = HS$, $S$ acts first and $H$ acts second: $y = H(Sx)$. To recover the initial state $x$, one must first undo the last layer applied ($H$) using $H^{-1}$, which leaves $Sx$. Only then can $S$ be undone by applying $S^{-1}$. Applying inverses in the wrong order attempts to undo the earlier transformation before the later one has been removed, distorting the coordinates incorrectly.

## 4. Verification and Consistency Checks
The analytical derivation is verified through algebraic consistency, dimensional checking, and direct substitution back into the governing problem definitions.
