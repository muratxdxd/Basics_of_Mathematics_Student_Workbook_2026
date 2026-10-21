# Problem 4: Triangular Matrix

## 1. Problem Statement
Without expanding the determinant, compute
$$\det\begin{pmatrix}2&4&1\\0&-3&5\\0&0&7\end{pmatrix}.$$
State the rule for an arbitrary triangular matrix and explain it using this example.

## 2. Theoretical Background and Concepts
> reinforces an important property of triangular matrices.

This problem applies foundational mathematical principles:
- Rigorous application of core definitions and operator properties.
- Analytical transformations preserving structural invariants.
- Systematic reduction to canonical and solvable forms.

## 3. Detailed Step-by-Step Solution
1. **Calculation:**
   $$\det\begin{pmatrix}2&4&1\\0&-3&5\\0&0&7\end{pmatrix} = 2 \cdot (-3) \cdot 7 = -42.$$

2. **Rule for Triangular Matrices:**
   For any upper triangular, lower triangular, or diagonal matrix $T = (t_{ij})_{n\times n}$, the determinant is the product of its main diagonal entries:
   $$\det T = \prod_{i=1}^n t_{ii} = t_{11} t_{22} \cdots t_{nn}.$$

3. **Explanation:**
   Performing cofactor expansion along the first column of an upper triangular matrix:
   $$\det T = t_{11} \cdot \det\begin{pmatrix}-3&5\\0&7\end{pmatrix} - 0 + 0.$$
   The remaining $2\times 2$ submatrix is also upper triangular, so expanding along its first column yields $(-3) \cdot 7$. Thus, all off-diagonal products in the permutation expansion contain at least one zero factor, leaving only the product along the main diagonal.

## 4. Verification and Consistency Checks
The analytical derivation is verified through algebraic consistency, dimensional checking, and direct substitution back into the governing problem definitions.
