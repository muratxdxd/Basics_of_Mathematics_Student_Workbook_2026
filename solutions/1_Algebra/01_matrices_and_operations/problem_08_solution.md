# Problem 8: Row Operations and Their Reversibility

## 1. Problem Statement
For
$$A=\begin{pmatrix}1&2&-1\\2&4&1\\-1&1&3\end{pmatrix}$$
perform, in order:
1. $R_2\leftarrow R_2-2R_1$,
2. $R_3\leftarrow R_3+R_1$,
3. interchange $R_2$ and $R_3$.

Write the matrix after each step. Then, for each of the three operations, state an operation that reverses it.

## 2. Theoretical Background and Concepts
> prepares for elimination by showing that row operations are controlled and reversible transformations of a matrix.

This problem applies foundational mathematical principles:
- Rigorous application of core definitions and operator properties.
- Analytical transformations preserving structural invariants.
- Systematic reduction to canonical and solvable forms.

## 3. Detailed Step-by-Step Solution
1. **Step 1: $R_2 \leftarrow R_2 - 2R_1$:**
   New Row 2: $\begin{pmatrix}2 - 2(1) & 4 - 2(2) & 1 - 2(-1)\end{pmatrix} = \begin{pmatrix}0 & 0 & 3\end{pmatrix}$.
   $$A_1 = \begin{pmatrix}1 & 2 & -1 \\ 0 & 0 & 3 \\ -1 & 1 & 3\end{pmatrix}.$$
   *Reverse operation:* $R_2 \leftarrow R_2 + 2R_1$.

2. **Step 2: $R_3 \leftarrow R_3 + R_1$:**
   New Row 3: $\begin{pmatrix}-1 + 1 & 1 + 2 & 3 + (-1)\end{pmatrix} = \begin{pmatrix}0 & 3 & 2\end{pmatrix}$.
   $$A_2 = \begin{pmatrix}1 & 2 & -1 \\ 0 & 0 & 3 \\ 0 & 3 & 2\end{pmatrix}.$$
   *Reverse operation:* $R_3 \leftarrow R_3 - R_1$.

3. **Step 3: Interchange $R_2 \leftrightarrow R_3$:**
   $$A_3 = \begin{pmatrix}1 & 2 & -1 \\ 0 & 3 & 2 \\ 0 & 0 & 3\end{pmatrix}.$$
   *Reverse operation:* Interchange $R_2 \leftrightarrow R_3$ (swapping two rows is its own inverse).

## 4. Verification and Consistency Checks
Applying the reverse operations in reverse order to $A_3$:
- Swap $R_2 \leftrightarrow R_3 \implies \begin{pmatrix}1&2&-1\\0&0&3\\0&3&2\end{pmatrix} = A_2$.
- $R_3 \leftarrow R_3 - R_1 \implies \begin{pmatrix}1&2&-1\\0&0&3\\-1&1&3\end{pmatrix} = A_1$.
- $R_2 \leftarrow R_2 + 2R_1 \implies \begin{pmatrix}1&2&-1\\2&4&1\\-1&1&3\end{pmatrix} = A$.
The original matrix is fully restored.
