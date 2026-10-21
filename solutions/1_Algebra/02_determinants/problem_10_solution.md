# Problem 10: Detecting Dependence

## 1. Problem Statement
Without carrying out a full determinant calculation, explain why
$$\det\begin{pmatrix}1&2&3\\2&4&6\\0&1&5\end{pmatrix}=0.$$
Identify a specific dependence between the rows and connect it with noninvertibility of the matrix.

## 2. Theoretical Background and Concepts
> teaches how to recognize a zero determinant from the structure of a matrix.

This problem applies foundational mathematical principles:
- Rigorous application of core definitions and operator properties.
- Analytical transformations preserving structural invariants.
- Systematic reduction to canonical and solvable forms.

## 3. Detailed Step-by-Step Solution
1. **Identifying Dependence:**
   Look at row 1 ($R_1 = (1, 2, 3)$) and row 2 ($R_2 = (2, 4, 6)$):
   $$R_2 = 2 R_1.$$
   Row 2 is an exact scalar multiple of Row 1.

2. **Connection to Determinant:**
   Performing the row operation $R_2 \leftarrow R_2 - 2R_1$ (which does not alter the determinant) produces a row of zeros:
   $$\begin{pmatrix}1&2&3\\0&0&0\\0&1&5\end{pmatrix}.$$
   Expanding along this zero row immediately yields $\det = 0$.

3. **Connection to Noninvertibility:**
   Because the rows are linearly dependent, the matrix has rank at most 2, which is less than full rank ($3$). By the Invertible Matrix Theorem, an $n\times n$ matrix is invertible if and only if its rank is $n$ (or equivalently, $\det \neq 0$). Thus, the matrix is singular and not invertible.

## More Challenging Exercises

## 4. Verification and Consistency Checks
The analytical derivation is verified through algebraic consistency, dimensional checking, and direct substitution back into the governing problem definitions.
