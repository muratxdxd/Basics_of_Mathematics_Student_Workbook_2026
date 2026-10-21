# Problem 5: Row Operations

## 1. Problem Statement
For
$$A=\begin{pmatrix}1&2&3\\2&1&0\\-1&4&2\end{pmatrix}$$
find $\det A$ by simplifying the matrix with row operations. At each step, indicate whether and how the determinant changes.

## 2. Theoretical Background and Concepts
> connects determinants with row operations and requires conscious tracking of every step.

This problem applies foundational mathematical principles:
- Rigorous application of core definitions and operator properties.
- Analytical transformations preserving structural invariants.
- Systematic reduction to canonical and solvable forms.

## 3. Detailed Step-by-Step Solution
1. **Step 1: Eliminate below $a_{11}$:**
   - $R_2 \leftarrow R_2 - 2R_1$: Adding a multiple of one row to another **leaves the determinant unchanged** ($\det A_1 = \det A$).
     Row 2: $(2 - 2, 1 - 4, 0 - 6) = (0, -3, -6)$.
   - $R_3 \leftarrow R_3 + R_1$: **Determinant unchanged** ($\det A_2 = \det A_1$).
     Row 3: $(-1 + 1, 4 + 2, 2 + 3) = (0, 6, 5)$.
   $$A_2 = \begin{pmatrix}1&2&3\\0&-3&-6\\0&6&5\end{pmatrix}.$$

2. **Step 2: Eliminate below $a_{22}$:**
   - $R_3 \leftarrow R_3 + 2R_2$: **Determinant unchanged**.
     Row 3: $(0 + 0, 6 + 2(-3), 5 + 2(-6)) = (0, 0, -7)$.
   $$A_3 = \begin{pmatrix}1&2&3\\0&-3&-6\\0&0&-7\end{pmatrix}.$$

3. **Compute Determinant of the Upper Triangular Matrix:**
   Since no row swaps or row scalings were used, the determinant is unchanged throughout:
   $$\det A = \det A_3 = 1 \cdot (-3) \cdot (-7) = 21.$$

## 4. Verification and Consistency Checks
Via Sarrus' Rule: $(1\cdot 1\cdot 2 + 2\cdot 0\cdot (-1) + 3\cdot 2\cdot 4) - (3\cdot 1\cdot (-1) + 1\cdot 0\cdot 4 + 2\cdot 2\cdot 2) = (2 + 0 + 24) - (-3 + 0 + 8) = 26 - 5 = 21$. Confirmed.
