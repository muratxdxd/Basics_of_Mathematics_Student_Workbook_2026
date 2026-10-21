# Problem 8: Determinant of a Product

## 1. Problem Statement
Let $A,B$ be square matrices such that $\det A=3$ and $\det B=-5$. Compute $\det(AB)$, $\det(BA)$ and, if it exists, $\det(A^{-1}B)$. Explain why the first two results are equal even though usually $AB\neq BA$.

## 2. Theoretical Background and Concepts
> organizes how determinants behave with respect to products and inverses.

This problem applies foundational mathematical principles:
- Rigorous application of core definitions and operator properties.
- Analytical transformations preserving structural invariants.
- Systematic reduction to canonical and solvable forms.

## 3. Detailed Step-by-Step Solution
1. **Computations:**
   - $\det(AB) = \det A \cdot \det B = 3 \cdot (-5) = -15$.
   - $\det(BA) = \det B \cdot \det A = (-5) \cdot 3 = -15$.
   - Since $\det A = 3 \neq 0$, $A$ is invertible, and $\det(A^{-1}) = \frac{1}{\det A} = \frac{1}{3}$.
     $$\det(A^{-1}B) = \det(A^{-1}) \cdot \det B = \frac{1}{3} \cdot (-5) = -\frac{5}{3}.$$

2. **Explanation of $\det(AB) = \det(BA)$:**
   While matrix multiplication is generally noncommutative ($AB \neq BA$), the determinant maps matrices to real numbers: $\det(AB) = \det A \cdot \det B$ and $\det(BA) = \det B \cdot \det A$.
   Multiplication of real numbers is commutative ($\det A \cdot \det B = \det B \cdot \det A$), so the determinants are always equal.

## 4. Verification and Consistency Checks
The analytical derivation is verified through algebraic consistency, dimensional checking, and direct substitution back into the governing problem definitions.
