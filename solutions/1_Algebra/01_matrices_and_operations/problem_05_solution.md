# Problem 5: Matrix Times Vector

## 1. Problem Statement
Let
$$A=\begin{pmatrix}2&-1\\1&3\end{pmatrix},\qquad x=\begin{pmatrix}4\\2\end{pmatrix}.$$
Compute $Ax$. Then express $Ax$ as a linear combination of the columns of $A$, with coefficients coming from the vector $x$.

## 2. Theoretical Background and Concepts
> shows that multiplying a matrix by a vector can be understood as a linear combination of the matrix columns.

This problem applies foundational mathematical principles:
- Rigorous application of core definitions and operator properties.
- Analytical transformations preserving structural invariants.
- Systematic reduction to canonical and solvable forms.

## 3. Detailed Step-by-Step Solution
1. **Direct Computation (row-by-column):**
   $$Ax = \begin{pmatrix}2&-1\\1&3\end{pmatrix}\begin{pmatrix}4\\2\end{pmatrix} = \begin{pmatrix}2(4) + (-1)(2) \\ 1(4) + 3(2)\end{pmatrix} = \begin{pmatrix}8 - 2 \\ 4 + 6\end{pmatrix} = \begin{pmatrix}6 \\ 10\end{pmatrix}.$$

2. **Linear Combination of Columns:**
   Let the columns of $A$ be $a_1 = \begin{pmatrix}2\\1\end{pmatrix}$ and $a_2 = \begin{pmatrix}-1\\3\end{pmatrix}$.
   $$x_1 a_1 + x_2 a_2 = 4\begin{pmatrix}2\\1\end{pmatrix} + 2\begin{pmatrix}-1\\3\end{pmatrix} = \begin{pmatrix}8\\4\end{pmatrix} + \begin{pmatrix}-2\\6\end{pmatrix} = \begin{pmatrix}8 - 2 \\ 4 + 6\end{pmatrix} = \begin{pmatrix}6 \\ 10\end{pmatrix}.$$

## 4. Verification and Consistency Checks
Both methods yield identical results $\begin{pmatrix}6\\10\end{pmatrix}$, confirming that matrix-vector multiplication $Ax$ fundamentally represents a linear combination of the columns of $A$ weighted by the components of $x$.
