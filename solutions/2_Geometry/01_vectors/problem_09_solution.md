# Problem 9: Cross Product as a Perpendicular Direction

## 1. Problem Statement
For $u=(1,2,0)$ and $v=(0,1,3)$ compute $u\times v$. Use dot products to check perpendicularity to both vectors, compute $v\times u$, and compare the results.

## 2. Theoretical Background and Concepts
> teaches the geometric meaning of the cross product and the effect of changing the order of its arguments.

This problem applies foundational mathematical principles:
- Rigorous application of core definitions and operator properties.
- Analytical transformations preserving structural invariants.
- Systematic reduction to canonical and solvable forms.

## 3. Detailed Step-by-Step Solution
1. **Compute $u \times v$:**
   $$u \times v = \det\begin{pmatrix}i & j & k \\ 1 & 2 & 0 \\ 0 & 1 & 3\end{pmatrix} = i(2\cdot 3 - 0\cdot 1) - j(1\cdot 3 - 0\cdot 0) + k(1\cdot 1 - 2\cdot 0) = 6i - 3j + k = (6, -3, 1).$$

2. **Perpendicularity Checks via Dot Products:**
   $$(u \times v) \cdot u = 6(1) + (-3)(2) + 1(0) = 6 - 6 + 0 = 0.$$
   $$(u \times v) \cdot v = 6(0) + (-3)(1) + 1(3) = 0 - 3 + 3 = 0.$$
   Both dot products are zero, verifying that $u \times v$ is strictly perpendicular to both $u$ and $v$.

3. **Compute $v \times u$ and Compare:**
   $$v \times u = \det\begin{pmatrix}i & j & k \\ 0 & 1 & 3 \\ 1 & 2 & 0\end{pmatrix} = i(0 - 6) - j(0 - 3) + k(0 - 1) = (-6, 3, -1) = -(u \times v).$$
   The cross product is **anticommutative**: $v \times u = -(u \times v)$. Reversing the order of vectors reverses the direction of the resulting vector by the right-hand rule.

## 4. Verification and Consistency Checks
The analytical derivation is verified through algebraic consistency, dimensional checking, and direct substitution back into the governing problem definitions.
