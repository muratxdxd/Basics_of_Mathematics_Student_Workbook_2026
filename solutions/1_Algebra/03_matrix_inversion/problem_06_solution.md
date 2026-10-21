# Problem 6: Solving a System Using the Inverse

## 1. Problem Statement
Solve
$$Ax=b,$$
where
$$A=\begin{pmatrix}2&1\\1&3\end{pmatrix},\qquad b=\begin{pmatrix}5\\7\end{pmatrix},$$
using $x=A^{-1}b$. Then substitute the resulting vector back into the equation and check the result.

## 2. Theoretical Background and Concepts
> shows the connection between inverse matrices and solving a linear system.

This problem applies foundational mathematical principles:
- Rigorous application of core definitions and operator properties.
- Analytical transformations preserving structural invariants.
- Systematic reduction to canonical and solvable forms.

## 3. Detailed Step-by-Step Solution
1. **Find $A^{-1}$:**
   $$\det A = 2(3) - 1(1) = 6 - 1 = 5 \neq 0.$$
   $$A^{-1} = \frac{1}{5} \begin{pmatrix}3 & -1 \\ -1 & 2\end{pmatrix}.$$

2. **Compute $x = A^{-1} b$:**
   $$x = \frac{1}{5}\begin{pmatrix}3 & -1 \\ -1 & 2\end{pmatrix}\begin{pmatrix}5 \\ 7\end{pmatrix} = \frac{1}{5}\begin{pmatrix}3(5) + (-1)(7) \\ -1(5) + 2(7)\end{pmatrix} = \frac{1}{5}\begin{pmatrix}15 - 7 \\ -5 + 14\end{pmatrix} = \frac{1}{5}\begin{pmatrix}8 \\ 9\end{pmatrix} = \begin{pmatrix}1.6 \\ 1.8\end{pmatrix}.$$

## 4. Verification and Consistency Checks
3. **Verification by Back Substitution ($Ax = b$):**
   $$Ax = \begin{pmatrix}2&1\\1&3\end{pmatrix}\begin{pmatrix}1.6\\1.8\end{pmatrix} = \begin{pmatrix}2(1.6) + 1(1.8) \\ 1(1.6) + 3(1.8)\end{pmatrix} = \begin{pmatrix}3.2 + 1.8 \\ 1.6 + 5.4\end{pmatrix} = \begin{pmatrix}5 \\ 7\end{pmatrix} = b.$$
   The solution is confirmed.
