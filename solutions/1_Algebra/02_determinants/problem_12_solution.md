# Problem 12: A Parameter Revealed by a Row Operation

## 1. Problem Statement
For
$$A(t)=\begin{pmatrix}1&2&3\\2&4&t\\0&1&1\end{pmatrix}$$
find the values of $t$ for which the matrix is not invertible.

Before computing the determinant, perform the operation
$$R_2\leftarrow R_2-2R_1$$
and use the resulting structure. At the end, explain what special thing happens to the rows for the value of the parameter you found.

## 2. Theoretical Background and Concepts
> combines a parameter, row operations, and recognition of dependence in one short argument.

This problem applies foundational mathematical principles:
- Rigorous application of core definitions and operator properties.
- Analytical transformations preserving structural invariants.
- Systematic reduction to canonical and solvable forms.

## 3. Detailed Step-by-Step Solution
1. **Perform $R_2 \leftarrow R_2 - 2R_1$:**
   Row 2 becomes:
   $$(2 - 2(1), 4 - 2(2), t - 2(3)) = (0, 0, t-6).$$
   The determinant is unchanged:
   $$A_1(t) = \begin{pmatrix}1&2&3\\0&0&t-6\\0&1&1\end{pmatrix}.$$

2. **Compute Determinant:**
   Expand along Row 2 (which has two zeros):
   $$\det A(t) = -(0) + 0 - (t-6)\cdot \det\begin{pmatrix}1&2\\0&1\end{pmatrix} = -(t-6)(1\cdot 1 - 2\cdot 0) = -(t-6) = 6-t.$$

3. **Find Non-Invertible Values:**
   The matrix is not invertible $\iff \det A(t) = 0 \iff 6 - t = 0 \iff t = 6$.

4. **Row Behavior at $t=6$:**
   When $t=6$, Row 2 of the original matrix is $(2, 4, 6) = 2(1, 2, 3) = 2R_1$. Row 2 is exactly twice Row 1. The rows are linearly dependent, producing the all-zero row $(0, 0, 0)$ after the row operation.

## 4. Verification and Consistency Checks
The analytical derivation is verified through algebraic consistency, dimensional checking, and direct substitution back into the governing problem definitions.
