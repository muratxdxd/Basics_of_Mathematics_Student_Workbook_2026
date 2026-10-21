# Problem 15: Two Methods for Solving the Same System

## 1. Problem Statement
For
$$A=\begin{pmatrix}2&1\\1&3\end{pmatrix},\qquad b=\begin{pmatrix}7\\8\end{pmatrix}$$
solve $Ax=b$ in two ways:
1. using $A^{-1}b$,
2. using Gaussian elimination.

Compare both solutions, the number of essential steps, and state which method was simpler in this example.

## 2. Theoretical Background and Concepts
> compares two known methods and prepares the student to choose a solution method consciously.

This problem applies foundational mathematical principles:
- Rigorous application of core definitions and operator properties.
- Analytical transformations preserving structural invariants.
- Systematic reduction to canonical and solvable forms.

## 3. Detailed Step-by-Step Solution
1. **Method 1: Using $A^{-1}b$:**
   - $\det A = 2(3) - 1(1) = 5$.
   - $A^{-1} = \frac{1}{5}\begin{pmatrix}3 & -1 \\ -1 & 2\end{pmatrix}$.
   - $x = A^{-1}b = \frac{1}{5}\begin{pmatrix}3 & -1 \\ -1 & 2\end{pmatrix}\begin{pmatrix}7 \\ 8\end{pmatrix} = \frac{1}{5}\begin{pmatrix}3(7)-1(8) \\ -1(7)+2(8)\end{pmatrix} = \frac{1}{5}\begin{pmatrix}13 \\ 9\end{pmatrix} = \begin{pmatrix}2.6 \\ 1.8\end{pmatrix}$.

2. **Method 2: Using Gaussian Elimination:**
   - Augmented matrix:
     $$\left[\begin{array}{cc|c} 2 & 1 & 7 \\ 1 & 3 & 8 \end{array}\right].$$
   - Swap $R_1 \leftrightarrow R_2$:
     $$\left[\begin{array}{cc|c} 1 & 3 & 8 \\ 2 & 1 & 7 \end{array}\right].$$
   - Eliminate below pivot: $R_2 \leftarrow R_2 - 2R_1$:
     $$\left[\begin{array}{cc|c} 1 & 3 & 8 \\ 0 & -5 & -9 \end{array}\right].$$
   - Back-substitution:
     $$-5y = -9 \implies y = \frac{9}{5} = 1.8.$$
     $$x + 3y = 8 \implies x = 8 - 3(1.8) = 8 - 5.4 = 2.6 = \frac{13}{5}.$$
     $$x = \begin{pmatrix}2.6 \\ 1.8\end{pmatrix}.$$

3. **Comparison:**
   - Both methods produce identical results: $x = 2.6, y = 1.8$.
   - **Simplicity:** Gaussian elimination was simpler here because it directly solved the specific system in just two row operations and back-substitution. Finding $A^{-1}$ required computing the determinant, finding all four matrix entries, and then performing an additional matrix-vector product.
   - Finding $A^{-1}$ is only preferred when one needs to solve $Ax = b$ for many different vectors $b$.

## 4. Verification and Consistency Checks
The analytical derivation is verified through algebraic consistency, dimensional checking, and direct substitution back into the governing problem definitions.
