# Problem 9: Composing Transformations

## 1. Problem Statement
Let
$$S=\begin{pmatrix}2&0\\0&1\end{pmatrix},\qquad R=\begin{pmatrix}0&-1\\1&0\end{pmatrix}.$$
The matrix $S$ describes nonuniform scaling, while $R$ describes a $90^\circ$ counterclockwise rotation.
For
$$x=\begin{pmatrix}1\\2\end{pmatrix}$$
compute $RSx$ and $SRx$. Compare the results and explain geometrically why the order of these transformations matters.

## 2. Theoretical Background and Concepts
> interprets matrix multiplication as composition of transformations.

This problem applies foundational mathematical principles:
- Rigorous application of core definitions and operator properties.
- Analytical transformations preserving structural invariants.
- Systematic reduction to canonical and solvable forms.

## 3. Detailed Step-by-Step Solution
1. **Computation of $RSx$ (Scale first, then Rotate):**
   $$Sx = \begin{pmatrix}2&0\\0&1\end{pmatrix}\begin{pmatrix}1\\2\end{pmatrix} = \begin{pmatrix}2\\2\end{pmatrix}.$$
   $$RSx = R(Sx) = \begin{pmatrix}0&-1\\1&0\end{pmatrix}\begin{pmatrix}2\\2\end{pmatrix} = \begin{pmatrix}-2\\2\end{pmatrix}.$$

2. **Computation of $SRx$ (Rotate first, then Scale):**
   $$Rx = \begin{pmatrix}0&-1\\1&0\end{pmatrix}\begin{pmatrix}1\\2\end{pmatrix} = \begin{pmatrix}-2\\1\end{pmatrix}.$$
   $$SRx = S(Rx) = \begin{pmatrix}2&0\\0&1\end{pmatrix}\begin{pmatrix}-2\\1\end{pmatrix} = \begin{pmatrix}-4\\1\end{pmatrix}.$$

3. **Geometric Explanation:**
   $RSx = \begin{pmatrix}-2\\2\end{pmatrix} \neq SRx = \begin{pmatrix}-4\\1\end{pmatrix}$.
   - In $RS$, the vector is first scaled horizontally by a factor of 2 (stretching the $x$-component $1 \to 2$), and then rotated $90^\circ$ counterclockwise, sending the stretched $x$-component to the positive $y$-axis.
   - In $SR$, the vector is rotated first, sending the original $y$-component ($2$) to the negative $x$-axis ($-2$). Then scaling by 2 doubles this new $x$-component from $-2$ to $-4$.
   Because scaling acts along the fixed coordinate axes, rotating before or after scaling completely alters which component receives the magnification.

## 4. Verification and Consistency Checks
The analytical derivation is verified through algebraic consistency, dimensional checking, and direct substitution back into the governing problem definitions.
