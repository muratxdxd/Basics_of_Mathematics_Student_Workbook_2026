# Problem 1: Determinant of a 2Ã—2 Matrix

## 1. Problem Statement
Compute
$$\det\begin{pmatrix}3&-2\\5&4\end{pmatrix},\qquad \det\begin{pmatrix}1&7\\2&14\end{pmatrix}.$$
Which matrix is invertible? Justify your answer.

## 2. Theoretical Background and Concepts
> introduces the simplest determinant calculation and immediately connects it with invertibility.

This problem applies foundational mathematical principles:
- Rigorous application of core definitions and operator properties.
- Analytical transformations preserving structural invariants.
- Systematic reduction to canonical and solvable forms.

## 3. Detailed Step-by-Step Solution
1. **Calculations:**
   $$\det\begin{pmatrix}3&-2\\5&4\end{pmatrix} = 3\cdot 4 - (-2)\cdot 5 = 12 - (-10) = 12 + 10 = 22.$$
   $$\det\begin{pmatrix}1&7\\2&14\end{pmatrix} = 1\cdot 14 - 7\cdot 2 = 14 - 14 = 0.$$

2. **Invertibility:**
   - A square matrix $M$ is invertible if and only if $\det M \neq 0$.
   - $\begin{pmatrix}3&-2\\5&4\end{pmatrix}$ is **invertible** because its determinant is $22 \neq 0$.
   - $\begin{pmatrix}1&7\\2&14\end{pmatrix}$ is **not invertible** (singular) because its determinant is $0$.

## 4. Verification and Consistency Checks
For the second matrix, Row 2 is exactly twice Row 1: $(2, 14) = 2(1, 7)$. Linear dependence between rows confirms the determinant must be 0 and the matrix is non-invertible.
