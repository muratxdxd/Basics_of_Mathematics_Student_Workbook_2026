# Problem 11: Parameter and Invertibility

## 1. Problem Statement
For
$$A(t)=\begin{pmatrix}1&t\\t&1\end{pmatrix}$$
find all $t$ for which the matrix is invertible, and then give a formula for $A(t)^{-1}$. Explain what happens to this formula at the excluded values.

## 2. Theoretical Background and Concepts
> combines a parameter, determinant, and an explicit inverse formula in one problem.

This problem applies foundational mathematical principles:
- Rigorous application of core definitions and operator properties.
- Analytical transformations preserving structural invariants.
- Systematic reduction to canonical and solvable forms.

## 3. Detailed Step-by-Step Solution
1. **Determinant and Invertibility Condition:**
   $$\det A(t) = 1(1) - t(t) = 1 - t^2.$$
   $A(t)$ is invertible if and only if $\det A(t) \neq 0$:
   $$1 - t^2 \neq 0 \iff t^2 \neq 1 \iff t \neq 1 \quad \text{and} \quad t \neq -1.$$

2. **Formula for $A(t)^{-1}$:**
   Using the $2\times 2$ inverse formula:
   $$A(t)^{-1} = \frac{1}{1 - t^2} \begin{pmatrix}1 & -t \\ -t & 1\end{pmatrix}.$$

3. **Behavior at Excluded Values:**
   - At $t = 1$: $A(1) = \begin{pmatrix}1&1\\1&1\end{pmatrix}$. The rows are identical ($R_1 = R_2$), meaning they are linearly dependent. In the formula, the denominator $1-t^2 = 1 - 1 = 0$, leading to division by zero.
   - At $t = -1$: $A(-1) = \begin{pmatrix}1&-1\\-1&1\end{pmatrix}$. Row 2 is $-1 \times$ Row 1 ($R_2 = -R_1$), so the rows are again dependent. In the formula, $1 - (-1)^2 = 0$, again causing division by zero.
   In both cases, the image of $\mathbb{R}^2$ collapses to a line, so the map is non-invertible.

## 4. Verification and Consistency Checks
The analytical derivation is verified through algebraic consistency, dimensional checking, and direct substitution back into the governing problem definitions.
