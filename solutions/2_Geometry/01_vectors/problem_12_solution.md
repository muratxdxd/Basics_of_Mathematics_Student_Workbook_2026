# Problem 12: A Normal Vector to a Plane

## 1. Problem Statement
Given $A=(1,0,2)$, $B=(2,1,0)$, and $C=(0,3,1)$. Construct two vectors lying in the plane, find a vector perpendicular to both, and check the perpendicularity using dot products.

## 2. Theoretical Background and Concepts
> creates a direct bridge from vectors to the description of a plane.

This problem applies foundational mathematical principles:
- Rigorous application of core definitions and operator properties.
- Analytical transformations preserving structural invariants.
- Systematic reduction to canonical and solvable forms.

## 3. Detailed Step-by-Step Solution
1. **Construct Two In-Plane Vectors:**
   $$u = \overrightarrow{AB} = B - A = (2 - 1, 1 - 0, 0 - 2) = (1, 1, -2).$$
   $$v = \overrightarrow{AC} = C - A = (0 - 1, 3 - 0, 1 - 2) = (-1, 3, -1).$$

2. **Find Normal Vector $n = u \times v$:**
   $$n = \det\begin{pmatrix}i & j & k \\ 1 & 1 & -2 \\ -1 & 3 & -1\end{pmatrix} = i(1(-1) - (-2)(3)) - j(1(-1) - (-2)(-1)) + k(1(3) - 1(-1))$$
   $$= i(-1 + 6) - j(-1 - 2) + k(3 + 1) = 5i + 3j + 4k = (5, 3, 4).$$

3. **Check Perpendicularity:**
   $$n \cdot u = 5(1) + 3(1) + 4(-2) = 5 + 3 - 8 = 0.$$
   $$n \cdot v = 5(-1) + 3(3) + 4(-1) = -5 + 9 - 4 = 0.$$
   Vector $n = (5, 3, 4)$ is perpendicular to both in-plane directions, serving as a valid normal vector to the plane.

## 4. Verification and Consistency Checks
The analytical derivation is verified through algebraic consistency, dimensional checking, and direct substitution back into the governing problem definitions.
