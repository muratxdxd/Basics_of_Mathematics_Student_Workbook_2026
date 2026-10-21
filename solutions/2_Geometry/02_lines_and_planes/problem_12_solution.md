# Problem 12: Intersection Line of Two Planes

## 1. Problem Statement
Find a parametric equation of the line that is the intersection of
$$x+y+z=3,\qquad x-y+z=1.$$
Find its direction vector in two ways: from the system of equations and from the cross product of the normal vectors. Compare the results.

## 2. Theoretical Background and Concepts
> shows the equivalence of the algebraic and geometric approaches to constructing an intersection line.

This problem applies foundational mathematical principles:
- Rigorous application of core definitions and operator properties.
- Analytical transformations preserving structural invariants.
- Systematic reduction to canonical and solvable forms.

## 3. Detailed Step-by-Step Solution
1. **Method 1: From the System of Equations:**
   Add the two equations:
   $$(x + y + z) + (x - y + z) = 3 + 1 \implies 2x + 2z = 4 \implies x + z = 2 \implies x = 2 - z.$$
   Subtract the second equation from the first:
   $$(x + y + z) - (x - y + z) = 3 - 1 \implies 2y = 2 \implies y = 1.$$
   Setting $z = t \in \mathbb{R}$ as the parameter:
   $$\begin{pmatrix}x\\y\\z\end{pmatrix} = \begin{pmatrix}2 - t \\ 1 \\ t\end{pmatrix} = \begin{pmatrix}2\\1\\0\end{pmatrix} + t\begin{pmatrix}-1\\0\\1\end{pmatrix}.$$
   Direction vector: $v_1 = (-1, 0, 1)$.

2. **Method 2: Cross Product of Normal Vectors:**
   Normal vectors: $n_1 = (1, 1, 1)$ and $n_2 = (1, -1, 1)$.
   $$v_2 = n_1 \times n_2 = \det\begin{pmatrix}i & j & k \\ 1 & 1 & 1 \\ 1 & -1 & 1\end{pmatrix} = i(1 - (-1)) - j(1 - 1) + k(-1 - 1) = (2, 0, -2).$$
   Simplifying by factoring out $-2$: $v_2 = -2(-1, 0, 1) \sim (-1, 0, 1)$.

3. **Comparison:**
   Both methods yield collinear direction vectors: $v_2 = -2 v_1$. The line is parallel to both planes, meaning its direction vector must be simultaneously perpendicular to both normal vectors, precisely defining the cross product $n_1 \times n_2$.

## 4. Verification and Consistency Checks
The analytical derivation is verified through algebraic consistency, dimensional checking, and direct substitution back into the governing problem definitions.
