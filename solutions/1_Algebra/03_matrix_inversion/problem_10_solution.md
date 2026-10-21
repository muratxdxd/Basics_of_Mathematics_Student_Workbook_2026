# Problem 10: Inverse of a Diagonal Matrix

## 1. Problem Statement
Given
$$D=\begin{pmatrix}2&0&0\\0&-3&0\\0&0&5\end{pmatrix},\qquad E=\begin{pmatrix}2&0&0\\0&0&0\\0&0&5\end{pmatrix}.$$
Without using Gaussâ€“Jordan elimination, decide which matrix is invertible. For the invertible matrix, give the inverse and check the result by multiplication.

## 2. Theoretical Background and Concepts
> teaches how to recognize invertibility and the inverse without using a full procedure when the matrix structure gives the answer immediately.

This problem applies foundational mathematical principles:
- Rigorous application of core definitions and operator properties.
- Analytical transformations preserving structural invariants.
- Systematic reduction to canonical and solvable forms.

## 3. Detailed Step-by-Step Solution
1. **Deciding Invertibility:**
   For a diagonal matrix, the determinant is the product of its diagonal entries:
   - $\det D = 2 \cdot (-3) \cdot 5 = -30 \neq 0 \implies$ **$D$ is invertible**.
   - $\det E = 2 \cdot 0 \cdot 5 = 0 \implies$ **$E$ is not invertible** (singular, row 2 is all zeros).

2. **Inverse of $D$:**
   The inverse of an invertible diagonal matrix has entries equal to the reciprocals of the diagonal elements:
   $$D^{-1} = \begin{pmatrix}\frac{1}{2} & 0 & 0 \\ 0 & -\frac{1}{3} & 0 \\ 0 & 0 & \frac{1}{5}\end{pmatrix}.$$

## 4. Verification and Consistency Checks
3. **Verification by Multiplication:**
   $$D D^{-1} = \begin{pmatrix}2&0&0\\0&-3&0\\0&0&5\end{pmatrix}\begin{pmatrix}\frac{1}{2}&0&0\\0&-\frac{1}{3}&0\\0&0&\frac{1}{5}\end{pmatrix} = \begin{pmatrix}2\cdot\frac{1}{2} & 0 & 0 \\ 0 & (-3)\cdot\left(-\frac{1}{3}\right) & 0 \\ 0 & 0 & 5\cdot\frac{1}{5}\end{pmatrix} = \begin{pmatrix}1&0&0\\0&1&0\\0&0&1\end{pmatrix} = I.$$

## More Challenging Exercises
