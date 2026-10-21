# Problem 10: Columns of a Matrix Product

## 1. Problem Statement
Given
$$A=\begin{pmatrix}1&2&0\\0&1&1\end{pmatrix},\qquad B=\begin{pmatrix}1&2\\-1&0\\3&1\end{pmatrix}.$$
Denote the columns of $B$ by $b_1,b_2$.

1. Compute $Ab_1$ and $Ab_2$.
2. Compute the matrix $AB$.
3. Compare the results and explain why the columns of $AB$ are exactly the vectors $Ab_1$ and $Ab_2$.

## 2. Theoretical Background and Concepts
> extends the interpretation of matrix-vector multiplication to a full product of two matrices instead of simply repeating another $Ax$ exercise.

This problem applies foundational mathematical principles:
- Rigorous application of core definitions and operator properties.
- Analytical transformations preserving structural invariants.
- Systematic reduction to canonical and solvable forms.

## 3. Detailed Step-by-Step Solution
1. **Compute $Ab_1$ and $Ab_2$:**
   $$b_1 = \begin{pmatrix}1\\-1\\3\end{pmatrix}, \qquad b_2 = \begin{pmatrix}2\\0\\1\end{pmatrix}.$$
   $$Ab_1 = \begin{pmatrix}1&2&0\\0&1&1\end{pmatrix}\begin{pmatrix}1\\-1\\3\end{pmatrix} = \begin{pmatrix}1(1) + 2(-1) + 0(3) \\ 0(1) + 1(-1) + 1(3)\end{pmatrix} = \begin{pmatrix}1 - 2 + 0 \\ 0 - 1 + 3\end{pmatrix} = \begin{pmatrix}-1 \\ 2\end{pmatrix}.$$
   $$Ab_2 = \begin{pmatrix}1&2&0\\0&1&1\end{pmatrix}\begin{pmatrix}2\\0\\1\end{pmatrix} = \begin{pmatrix}1(2) + 2(0) + 0(1) \\ 0(2) + 1(0) + 1(1)\end{pmatrix} = \begin{pmatrix}2 + 0 + 0 \\ 0 + 0 + 1\end{pmatrix} = \begin{pmatrix}2 \\ 1\end{pmatrix}.$$

2. **Compute $AB$:**
   $$AB = \begin{pmatrix}1(1)+2(-1)+0(3) & 1(2)+2(0)+0(1) \\ 0(1)+1(-1)+1(3) & 0(2)+1(0)+1(1)\end{pmatrix} = \begin{pmatrix}-1 & 2 \\ 2 & 1\end{pmatrix}.$$

3. **Comparison and Explanation:**
   The columns of $AB$ are $\operatorname{col}_1(AB) = \begin{pmatrix}-1\\2\end{pmatrix} = Ab_1$ and $\operatorname{col}_2(AB) = \begin{pmatrix}2\\1\end{pmatrix} = Ab_2$.
   By the column-partition definition of matrix multiplication:
   $$A B = A \begin{pmatrix} b_1 & b_2 \end{pmatrix} = \begin{pmatrix} A b_1 & A b_2 \end{pmatrix}.$$
   Each column $j$ of the product $AB$ is the transformation of the $j$-th column of $B$ under matrix $A$.

## More Challenging Exercises

## 4. Verification and Consistency Checks
The analytical derivation is verified through algebraic consistency, dimensional checking, and direct substitution back into the governing problem definitions.
