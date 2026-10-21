# Problem 8: Inverse of a Transformation

## 1. Problem Statement
The matrix
$$S=\begin{pmatrix}2&0\\0&\frac12\end{pmatrix}$$
describes a scaling of the plane. Find $S^{-1}$ and explain geometrically what the inverse transformation does. Check the action of the pair $S,S^{-1}$ on one simple vector.

## 2. Theoretical Background and Concepts
> gives the inverse the interpretation of undoing a transformation.

This problem applies foundational mathematical principles:
- Rigorous application of core definitions and operator properties.
- Analytical transformations preserving structural invariants.
- Systematic reduction to canonical and solvable forms.

## 3. Detailed Step-by-Step Solution
1. **Find $S^{-1}$:**
   Since $S$ is diagonal, its inverse has the reciprocal diagonal entries:
   $$S^{-1} = \begin{pmatrix}\frac{1}{2} & 0 \\ 0 & 2\end{pmatrix}.$$

2. **Geometric Interpretation:**
   - $S$ scales the horizontal axis ($x$) by a factor of $2$ and compresses the vertical axis ($y$) by a factor of $\frac{1}{2}$.
   - The inverse $S^{-1}$ undoes this action completely: it compresses the horizontal axis by $\frac{1}{2}$ and stretches the vertical axis by a factor of $2$.

3. **Test on Vector $v = \begin{pmatrix}2\\4\end{pmatrix}$:**
   - Applying $S$:
     $$w = Sv = \begin{pmatrix}2&0\\0&\frac{1}{2}\end{pmatrix}\begin{pmatrix}2\\4\end{pmatrix} = \begin{pmatrix}4\\2\end{pmatrix}.$$
   - Applying $S^{-1}$:
     $$S^{-1}w = \begin{pmatrix}\frac{1}{2}&0\\0&2\end{pmatrix}\begin{pmatrix}4\\2\end{pmatrix} = \begin{pmatrix}2\\4\end{pmatrix} = v.$$
   The original vector is completely restored: $S^{-1}(Sv) = v$.

## 4. Verification and Consistency Checks
The analytical derivation is verified through algebraic consistency, dimensional checking, and direct substitution back into the governing problem definitions.
