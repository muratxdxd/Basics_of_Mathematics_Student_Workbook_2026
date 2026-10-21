# Problem 7: Using Properties Instead of Recomputing

## 1. Problem Statement
Suppose that for a $3\times3$ matrix, $\det A=-4$. Compute
$$\det(2A),\qquad \det(A^T),\qquad \det(A^2),\qquad \det(-A).$$
Justify each answer using the appropriate property.

## 2. Theoretical Background and Concepts
> teaches how to use determinant properties instead of repeating a full calculation.

This problem applies foundational mathematical principles:
- Rigorous application of core definitions and operator properties.
- Analytical transformations preserving structural invariants.
- Systematic reduction to canonical and solvable forms.

## 3. Detailed Step-by-Step Solution
1. **$\det(2A)$:**
   *Property:* For an $n\times n$ matrix, multiplying the matrix by scalar $c$ multiplies every row by $c$, so $\det(cA) = c^n \det A$.
   Here $n=3$, so:
   $$\det(2A) = 2^3 \det A = 8 \cdot (-4) = -32.$$

2. **$\det(A^T)$:**
   *Property:* Transposition does not alter the determinant: $\det(A^T) = \det A$.
   $$\det(A^T) = -4.$$

3. **$\det(A^2)$:**
   *Property:* Determinant of a product equals the product of determinants: $\det(XY) = \det(X)\det(Y)$.
   $$\det(A^2) = \det(A \cdot A) = (\det A)^2 = (-4)^2 = 16.$$

4. **$\det(-A)$:**
   *Property:* This is scalar multiplication by $c = -1$ for an $n=3$ matrix: $\det(-A) = (-1)^3 \det A$.
   $$\det(-A) = (-1) \cdot (-4) = 4.$$

## 4. Verification and Consistency Checks
The analytical derivation is verified through algebraic consistency, dimensional checking, and direct substitution back into the governing problem definitions.
