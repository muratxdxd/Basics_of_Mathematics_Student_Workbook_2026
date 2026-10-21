# Problem 2: Formula for a 2Ã—2 Matrix

## 1. Problem Statement
Find the inverse of
$$A=\begin{pmatrix}3&2\\5&4\end{pmatrix}$$
using the formula for a $2\times2$ matrix. At the end, check the result by computing one product with $A$.

## 2. Theoretical Background and Concepts
> teaches the simplest explicit formula for an inverse and requires verification using the definition.

This problem applies foundational mathematical principles:
- Rigorous application of core definitions and operator properties.
- Analytical transformations preserving structural invariants.
- Systematic reduction to canonical and solvable forms.

## 3. Detailed Step-by-Step Solution
1. **Formula:**
   For $M = \begin{pmatrix}a&b\\c&d\end{pmatrix}$ with $\det M = ad - bc \neq 0$:
   $$M^{-1} = \frac{1}{\det M} \begin{pmatrix}d & -b \\ -c & a\end{pmatrix}.$$

2. **Determinant of $A$:**
   $$\det A = 3(4) - 2(5) = 12 - 10 = 2 \neq 0.$$

3. **Compute $A^{-1}$:**
   $$A^{-1} = \frac{1}{2} \begin{pmatrix}4 & -2 \\ -5 & 3\end{pmatrix} = \begin{pmatrix}2 & -1 \\ -\frac{5}{2} & \frac{3}{2}\end{pmatrix}.$$

## 4. Verification and Consistency Checks
4. **Verification via $AA^{-1}$:**
   $$A A^{-1} = \begin{pmatrix}3&2\\5&4\end{pmatrix} \begin{pmatrix}2&-1\\-\frac{5}{2}&\frac{3}{2}\end{pmatrix} = \begin{pmatrix}3(2) + 2\left(-\frac{5}{2}\right) & 3(-1) + 2\left(\frac{3}{2}\right) \\ 5(2) + 4\left(-\frac{5}{2}\right) & 5(-1) + 4\left(\frac{3}{2}\right)\end{pmatrix} = \begin{pmatrix}6 - 5 & -3 + 3 \\ 10 - 10 & -5 + 6\end{pmatrix} = \begin{pmatrix}1&0\\0&1\end{pmatrix} = I.$$
   The inverse is verified.
