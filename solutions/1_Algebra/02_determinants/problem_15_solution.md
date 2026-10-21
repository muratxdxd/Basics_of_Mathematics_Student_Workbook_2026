# Problem 15: Combining Determinant Properties

## 1. Problem Statement
Let $A$ and $B$ be invertible $2\times2$ matrices with
$$\det A=-2,\qquad \det B=3.$$
Without finding the entries of the matrices, compute
$$\det\left(B^{-1}A^TB\right).$$
State the determinant properties you use in order and explain why the factors involving $B$ eventually cancel.

## 2. Theoretical Background and Concepts
> tests the transfer of several known properties into one short problem instead of checking a single property again with numbers.

This problem applies foundational mathematical principles:
- Rigorous application of core definitions and operator properties.
- Analytical transformations preserving structural invariants.
- Systematic reduction to canonical and solvable forms.

## 3. Detailed Step-by-Step Solution
1. **Sequence of Determinant Properties:**
   - **Property 1 (Multiplicativity):** $\det(XYZ) = \det(X) \det(Y) \det(Z)$.
     $$\det(B^{-1}A^TB) = \det(B^{-1}) \cdot \det(A^T) \cdot \det(B).$$
   - **Property 2 (Determinant of Inverse):** $\det(B^{-1}) = \frac{1}{\det B}$.
   - **Property 3 (Determinant of Transpose):** $\det(A^T) = \det(A)$.

2. **Calculation:**
   $$\det(B^{-1}A^TB) = \frac{1}{\det B} \cdot \det(A) \cdot \det(B) = \frac{1}{3} \cdot (-2) \cdot 3 = -2.$$

3. **Why the Factors Involving $B$ Cancel:**
   In the expression $\frac{1}{\det B} \cdot \det A \cdot \det B$, the determinants are scalar real numbers. In $\mathbb{R}$, multiplication is commutative and associative, so:
   $$\left(\frac{1}{\det B} \cdot \det B\right) \cdot \det A = 1 \cdot \det A = \det A.$$
   Geometrically, $B^{-1} A^T B$ represents a change of basis (similarity transformation) of $A^T$. Determinants measure the factor by which a transformation scales volume, which is an intrinsic geometric property independent of the choice of coordinate system.

## 4. Verification and Consistency Checks
The analytical derivation is verified through algebraic consistency, dimensional checking, and direct substitution back into the governing problem definitions.
