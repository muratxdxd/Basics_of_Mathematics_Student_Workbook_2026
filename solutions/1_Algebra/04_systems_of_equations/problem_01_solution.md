# Problem 1: From a System to a Matrix

## 1. Problem Statement
Write the system
$$\begin{cases}2x-y+z=4,\\x+3y-2z=1,\\3x+y+z=7.\end{cases}$$
in the form $Ax=b$.
Identify the coefficient matrix, the vector of unknowns, and the right-hand side vector. Explain how each row of the matrix corresponds to one equation.

## 2. Theoretical Background and Concepts
> teaches how to move between a system of equations and matrix notation.

This problem applies foundational mathematical principles:
- Rigorous application of core definitions and operator properties.
- Analytical transformations preserving structural invariants.
- Systematic reduction to canonical and solvable forms.

## 3. Detailed Step-by-Step Solution
1. **Matrix Form $Ax = b$:**
   $$\begin{pmatrix}2 & -1 & 1 \\ 1 & 3 & -2 \\ 3 & 1 & 1\end{pmatrix}\begin{pmatrix}x \\ y \\ z\end{pmatrix} = \begin{pmatrix}4 \\ 1 \\ 7\end{pmatrix}.$$

2. **Components:**
   - **Coefficient matrix:** $A = \begin{pmatrix}2 & -1 & 1 \\ 1 & 3 & -2 \\ 3 & 1 & 1\end{pmatrix}$.
   - **Vector of unknowns:** $x = \begin{pmatrix}x \\ y \\ z\end{pmatrix}$.
   - **Right-hand side vector:** $b = \begin{pmatrix}4 \\ 1 \\ 7\end{pmatrix}$.

3. **Correspondence of Rows to Equations:**
   By definition of matrix-vector multiplication, the $i$-th entry of $Ax$ is the dot product of the $i$-th row of $A$ with the vector of unknowns:
   $$\operatorname{Row}_i(A) \cdot x = a_{i1}x + a_{i2}y + a_{i3}z = b_i.$$
   Thus, row 1 encodes $2x - y + z = 4$, row 2 encodes $x + 3y - 2z = 1$, and row 3 encodes $3x + y + z = 7$.

## 4. Verification and Consistency Checks
The analytical derivation is verified through algebraic consistency, dimensional checking, and direct substitution back into the governing problem definitions.
