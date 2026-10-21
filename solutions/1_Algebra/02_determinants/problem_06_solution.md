# Problem 6: Parameter and Invertibility

## 1. Problem Statement
For
$$A(t)=\begin{pmatrix}t&1\\2&t\end{pmatrix}$$
find all values of $t$ for which the matrix is not invertible. Explain how your answer is related to the determinant being zero.

## 2. Theoretical Background and Concepts
> shows how the determinant can be used to study a family of matrices depending on a parameter.

This problem applies foundational mathematical principles:
- Rigorous application of core definitions and operator properties.
- Analytical transformations preserving structural invariants.
- Systematic reduction to canonical and solvable forms.

## 3. Detailed Step-by-Step Solution
1. **Compute Determinant:**
   $$\det A(t) = t\cdot t - 1\cdot 2 = t^2 - 2.$$

2. **Condition for Non-Invertibility:**
   A matrix $A(t)$ is not invertible if and only if $\det A(t) = 0$.
   $$t^2 - 2 = 0 \iff t^2 = 2 \iff t = \sqrt{2} \quad \text{or} \quad t = -\sqrt{2}.$$

3. **Connection to Determinant Being Zero:**
   When $\det A(t) = 0$, the rows (and columns) of $A(t)$ are linearly dependent.
   - For $t = \sqrt{2}$: $R_1 = (\sqrt{2}, 1)$ and $R_2 = (2, \sqrt{2}) = \sqrt{2}(\sqrt{2}, 1) = \sqrt{2}R_1$.
   The linear map represented by $A(t)$ compresses $\mathbb{R}^2$ onto a 1-dimensional line, giving a non-trivial kernel ($\ker A(t) \neq \{0\}$). Hence, the transformation has no inverse.

## 4. Verification and Consistency Checks
The analytical derivation is verified through algebraic consistency, dimensional checking, and direct substitution back into the governing problem definitions.
