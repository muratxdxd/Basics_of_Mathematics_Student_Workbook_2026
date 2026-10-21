# Problem 9: Area and the Determinant

## 1. Problem Statement
The vectors
$$u=\begin{pmatrix}3\\1\end{pmatrix},\qquad v=\begin{pmatrix}1\\4\end{pmatrix}$$
span a parallelogram. Compute its area using a determinant. Then reverse the order of the vectors and explain what changes in the determinant and what does not change in the area.

## 2. Theoretical Background and Concepts
> gives the determinant a geometric interpretation and distinguishes its sign from the value of the area.

This problem applies foundational mathematical principles:
- Rigorous application of core definitions and operator properties.
- Analytical transformations preserving structural invariants.
- Systematic reduction to canonical and solvable forms.

## 3. Detailed Step-by-Step Solution
1. **Area Computation:**
   Form the matrix with columns $u$ and $v$:
   $$\det \begin{pmatrix}3&1\\1&4\end{pmatrix} = 3(4) - 1(1) = 12 - 1 = 11.$$
   $$\text{Area} = |\det(u, v)| = |11| = 11.$$

2. **Reversing the Order:**
   $$\det \begin{pmatrix}1&3\\4&1\end{pmatrix} = 1(1) - 3(4) = 1 - 12 = -11.$$
   $$\text{Area} = |-11| = 11.$$

3. **Comparison:**
   - **What changes:** The sign of the determinant reverses from $+11$ to $-11$. The determinant computes *signed area*: a positive sign indicates a counterclockwise orientation from the first vector to the second, while a negative sign indicates a clockwise orientation.
   - **What does not change:** The geometric area remains $11$, because geometric area is the absolute magnitude $|\det|$, which is unaffected by orientation.

## 4. Verification and Consistency Checks
The analytical derivation is verified through algebraic consistency, dimensional checking, and direct substitution back into the governing problem definitions.
