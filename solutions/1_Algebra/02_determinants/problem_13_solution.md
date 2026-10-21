# Problem 13: Determinant by Elimination

## 1. Problem Statement
Compute the determinant
$$A=\begin{pmatrix}1&2&3\\2&5&7\\1&0&2\end{pmatrix}$$
using elimination. Record the effect of every row operation used on the value of the determinant.

## 2. Theoretical Background and Concepts
> reinforces organizing a determinant calculation through row operations without introducing an unnecessary second procedure.

This problem applies foundational mathematical principles:
- Rigorous application of core definitions and operator properties.
- Analytical transformations preserving structural invariants.
- Systematic reduction to canonical and solvable forms.

## 3. Detailed Step-by-Step Solution
1. **Elimination Steps and Determinant Tracking:**
   - **Step 1:** $R_2 \leftarrow R_2 - 2R_1$.
     *Effect:* Row addition does not change the determinant ($\times 1$).
     New Row 2: $(2-2, 5-4, 7-6) = (0, 1, 1)$.
   - **Step 2:** $R_3 \leftarrow R_3 - R_1$.
     *Effect:* Row addition does not change the determinant ($\times 1$).
     New Row 3: $(1-1, 0-2, 2-3) = (0, -2, -1)$.
     $$\text{Matrix: } \begin{pmatrix}1&2&3\\0&1&1\\0&-2&-1\end{pmatrix}.$$
   - **Step 3:** $R_3 \leftarrow R_3 + 2R_2$.
     *Effect:* Row addition does not change the determinant ($\times 1$).
     New Row 3: $(0, -2+2, -1+2(1)) = (0, 0, 1)$.
     $$\text{Upper triangular matrix: } U = \begin{pmatrix}1&2&3\\0&1&1\\0&0&1\end{pmatrix}.$$

2. **Compute Result:**
   $$\det A = \det U = 1 \cdot 1 \cdot 1 = 1.$$

## 4. Verification and Consistency Checks
Cofactor expansion along column 1 of original matrix:
$$\det A = 1\cdot(10-0) - 2\cdot(4-0) + 1\cdot(14-15) = 10 - 8 - 1 = 1.$$
Confirmed.
