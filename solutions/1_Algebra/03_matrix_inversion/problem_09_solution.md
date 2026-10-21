# Problem 9: Matrix Equation

## 1. Problem Statement
Given
$$A=\begin{pmatrix}1&2\\0&1\end{pmatrix},\qquad B=\begin{pmatrix}3&1\\2&4\end{pmatrix}.$$
Solve the equation $AX=B$ for $X$. Before calculating, decide on which side of the equation $A^{-1}$ must be used. Then check the result by computing $AX$.

## 2. Theoretical Background and Concepts
> teaches that order matters in matrix equations and must guide the solution.

This problem applies foundational mathematical principles:
- Rigorous application of core definitions and operator properties.
- Analytical transformations preserving structural invariants.
- Systematic reduction to canonical and solvable forms.

## 3. Detailed Step-by-Step Solution
1. **Deciding the Multiplication Side:**
   In $AX = B$, matrix $A$ appears on the left of $X$. Since matrix multiplication is noncommutative, we must multiply both sides on the **left** by $A^{-1}$:
   $$A^{-1}(AX) = A^{-1}B \implies (A^{-1}A)X = A^{-1}B \implies IX = A^{-1}B \implies X = A^{-1}B.$$

2. **Find $A^{-1}$:**
   $$\det A = 1(1) - 2(0) = 1 \implies A^{-1} = \begin{pmatrix}1 & -2 \\ 0 & 1\end{pmatrix}.$$

3. **Compute $X = A^{-1}B$:**
   $$X = \begin{pmatrix}1 & -2 \\ 0 & 1\end{pmatrix}\begin{pmatrix}3 & 1 \\ 2 & 4\end{pmatrix} = \begin{pmatrix}1(3) + (-2)(2) & 1(1) + (-2)(4) \\ 0(3) + 1(2) & 0(1) + 1(4)\end{pmatrix} = \begin{pmatrix}3 - 4 & 1 - 8 \\ 2 & 4\end{pmatrix} = \begin{pmatrix}-1 & -7 \\ 2 & 4\end{pmatrix}.$$

## 4. Verification and Consistency Checks
4. **Verification via $AX$:**
   $$AX = \begin{pmatrix}1&2\\0&1\end{pmatrix}\begin{pmatrix}-1&-7\\2&4\end{pmatrix} = \begin{pmatrix}1(-1)+2(2) & 1(-7)+2(4) \\ 0(-1)+1(2) & 0(-7)+1(4)\end{pmatrix} = \begin{pmatrix}-1+4 & -7+8 \\ 2 & 4\end{pmatrix} = \begin{pmatrix}3 & 1 \\ 2 & 4\end{pmatrix} = B.$$
   Verified.
