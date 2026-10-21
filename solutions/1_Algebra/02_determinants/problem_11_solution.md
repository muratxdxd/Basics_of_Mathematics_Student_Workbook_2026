# Problem 11: Shortening the Calculation with Row Operations

## 1. Problem Statement
Compute
$$\det\begin{pmatrix}1&2&3\\1&3&4\\1&4&6\end{pmatrix}$$
by first performing row operations that create as many zeros as possible. State which operations do not change the determinant.

## 2. Theoretical Background and Concepts
> develops planning instead of mechanically repeating the same procedure.

This problem applies foundational mathematical principles:
- Rigorous application of core definitions and operator properties.
- Analytical transformations preserving structural invariants.
- Systematic reduction to canonical and solvable forms.

## 3. Detailed Step-by-Step Solution
1. **Operations that do not change the determinant:**
   Replacing row $R_i$ with $R_i + c R_j$ ($i \neq j$) leaves the determinant unchanged.

2. **Step-by-step Elimination:**
   $$M = \begin{pmatrix}1&2&3\\1&3&4\\1&4&6\end{pmatrix}.$$
   - Subtract $R_1$ from $R_2$ ($R_2 \leftarrow R_2 - R_1$):
     Row 2 becomes $(1-1, 3-2, 4-3) = (0, 1, 1)$.
   - Subtract $R_1$ from $R_3$ ($R_3 \leftarrow R_3 - R_1$):
     Row 3 becomes $(1-1, 4-2, 6-3) = (0, 2, 3)$.
   $$M_1 = \begin{pmatrix}1&2&3\\0&1&1\\0&2&3\end{pmatrix}.$$
   - Subtract $2R_2$ from $R_3$ ($R_3 \leftarrow R_3 - 2R_2$):
     Row 3 becomes $(0, 2 - 2(1), 3 - 2(1)) = (0, 0, 1)$.
   $$M_2 = \begin{pmatrix}1&2&3\\0&1&1\\0&0&1\end{pmatrix}.$$

3. **Determinant:**
   $M_2$ is upper triangular. Since all row operations preserved the determinant:
   $$\det M = \det M_2 = 1 \cdot 1 \cdot 1 = 1.$$

## 4. Verification and Consistency Checks
The analytical derivation is verified through algebraic consistency, dimensional checking, and direct substitution back into the governing problem definitions.
