# Problem 5: A 3Ã—3 Matrix

## 1. Problem Statement
Use Gaussâ€“Jordan elimination to find the inverse of
$$A=\begin{pmatrix}1&1&0\\0&1&1\\1&0&1\end{pmatrix}.$$
Check the result by multiplication.

## 2. Theoretical Background and Concepts
> provides necessary practice with the full method in a situation where the $2\times2$ formula no longer applies.

This problem applies foundational mathematical principles:
- Rigorous application of core definitions and operator properties.
- Analytical transformations preserving structural invariants.
- Systematic reduction to canonical and solvable forms.

## 3. Detailed Step-by-Step Solution
1. **Set up the Augmented Matrix:**
   $$[A \mid I] = \left[\begin{array}{ccc|ccc} 1&1&0 & 1&0&0 \\ 0&1&1 & 0&1&0 \\ 1&0&1 & 0&0&1 \end{array}\right].$$
   Each elementary row operation is left multiplication by an elementary matrix, so applying the same operation to both blocks is precisely multiplying both $A$ and $I$ on the left. If the product of these elementary matrices is $E$, the final left block is $EA=I$, hence $E=A^{-1}$. The right block is $EI=A^{-1}$, which is why the row operations produce the inverse.

2. **Forward Elimination:**
   - $R_3 \leftarrow R_3 - R_1$:
     $$\left[\begin{array}{ccc|ccc} 1&1&0 & 1&0&0 \\ 0&1&1 & 0&1&0 \\ 0&-1&1 & -1&0&1 \end{array}\right].$$
   - $R_3 \leftarrow R_3 + R_2$:
     $$\left[\begin{array}{ccc|ccc} 1&1&0 & 1&0&0 \\ 0&1&1 & 0&1&0 \\ 0&0&2 & -1&1&1 \end{array}\right].$$

3. **Scale Pivot and Back Substitution:**
   - $R_3 \leftarrow \frac{1}{2} R_3$:
     $$\left[\begin{array}{ccc|ccc} 1&1&0 & 1&0&0 \\ 0&1&1 & 0&1&0 \\ 0&0&1 & -\frac{1}{2}&\frac{1}{2}&\frac{1}{2} \end{array}\right].$$
   - $R_2 \leftarrow R_2 - R_3$:
     $$\left[\begin{array}{ccc|ccc} 1&1&0 & 1&0&0 \\ 0&1&0 & \frac{1}{2}&\frac{1}{2}&-\frac{1}{2} \\ 0&0&1 & -\frac{1}{2}&\frac{1}{2}&\frac{1}{2} \end{array}\right].$$
   - $R_1 \leftarrow R_1 - R_2$:
     $$\left[\begin{array}{ccc|ccc} 1&0&0 & \frac{1}{2}&-\frac{1}{2}&\frac{1}{2} \\ 0&1&0 & \frac{1}{2}&\frac{1}{2}&-\frac{1}{2} \\ 0&0&1 & -\frac{1}{2}&\frac{1}{2}&\frac{1}{2} \end{array}\right].$$

4. **Result:**
   $$A^{-1} = \frac{1}{2} \begin{pmatrix}1 & -1 & 1 \\ 1 & 1 & -1 \\ -1 & 1 & 1\end{pmatrix}.$$

## 4. Verification and Consistency Checks
5. **Verification via $AA^{-1}$:**
   $$AA^{-1} = \begin{pmatrix}1&1&0\\0&1&1\\1&0&1\end{pmatrix} \cdot \frac{1}{2}\begin{pmatrix}1&-1&1\\1&1&-1\\-1&1&1\end{pmatrix} = \frac{1}{2}\begin{pmatrix}1+1+0 & -1+1+0 & 1-1+0 \\ 0+1-1 & 0+1+1 & 0-1+1 \\ 1+0-1 & -1+0+1 & 1+0+1\end{pmatrix} = \frac{1}{2}\begin{pmatrix}2&0&0\\0&2&0\\0&0&2\end{pmatrix} = I.$$
   This product check confirms that the computed matrix is a right inverse; for a square matrix, this verifies it is the inverse of $A$.
