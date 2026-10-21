# Problem 4: Matrix Multiplication and Noncommutativity

## 1. Problem Statement
For
$$A=\begin{pmatrix}1&2\\0&1\end{pmatrix},\qquad B=\begin{pmatrix}2&0\\3&1\end{pmatrix}$$
compute $AB$ and $BA$. Is $AB=BA$? Use this example to explain what noncommutativity of matrix multiplication means.

## 2. Theoretical Background and Concepts
> shows one of the most important differences between matrix multiplication and multiplication of numbers.

This problem applies foundational mathematical principles:
- Rigorous application of core definitions and operator properties.
- Analytical transformations preserving structural invariants.
- Systematic reduction to canonical and solvable forms.

## 3. Detailed Step-by-Step Solution
1. **Computation of $AB$:**
   $$AB = \begin{pmatrix}1&2\\0&1\end{pmatrix}\begin{pmatrix}2&0\\3&1\end{pmatrix} = \begin{pmatrix}1(2)+2(3) & 1(0)+2(1) \\ 0(2)+1(3) & 0(0)+1(1)\end{pmatrix} = \begin{pmatrix}2+6 & 0+2 \\ 0+3 & 0+1\end{pmatrix} = \begin{pmatrix}8 & 2 \\ 3 & 1\end{pmatrix}.$$

2. **Computation of $BA$:**
   $$BA = \begin{pmatrix}2&0\\3&1\end{pmatrix}\begin{pmatrix}1&2\\0&1\end{pmatrix} = \begin{pmatrix}2(1)+0(0) & 2(2)+0(1) \\ 3(1)+1(0) & 3(2)+1(1)\end{pmatrix} = \begin{pmatrix}2+0 & 4+0 \\ 3+0 & 6+1\end{pmatrix} = \begin{pmatrix}2 & 4 \\ 3 & 7\end{pmatrix}.$$

3. **Comparison and Noncommutativity:**
   $AB = \begin{pmatrix}8&2\\3&1\end{pmatrix} \neq BA = \begin{pmatrix}2&4\\3&7\end{pmatrix}$.
   Therefore, $AB \neq BA$. Noncommutativity means that the order of operations in matrix multiplication matters; changing the order of the factors generally yields an entirely different matrix (or may even make multiplication impossible due to mismatched dimensions).

## 4. Verification and Consistency Checks
Determinants: $\det(A) = 1(1)-2(0) = 1$, $\det(B) = 2(1)-0(3) = 2$.
$\det(AB) = 8(1)-2(3) = 2 = \det(A)\det(B)$.
$\det(BA) = 2(7)-4(3) = 2 = \det(B)\det(A)$.
Both determinants match $\det(A)\det(B)=2$, verifying algebraic correctness.
