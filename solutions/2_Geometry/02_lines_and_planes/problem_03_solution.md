# Problem 3: Plane Through a Point with a Given Normal Vector

## 1. Problem Statement
Find the equation of the plane through $P=(1,-2,3)$ and perpendicular to $n=(2,1,-1)$. Check the result by substituting the point $P$ and explain the role of the normal vector.

## 2. Theoretical Background and Concepts
> shows the basic construction of a plane from a point and a normal vector.

This problem applies foundational mathematical principles:
- Rigorous application of core definitions and operator properties.
- Analytical transformations preserving structural invariants.
- Systematic reduction to canonical and solvable forms.

## 3. Detailed Step-by-Step Solution
1. **Equation of the Plane:**
   A point $(x, y, z)$ lies in the plane if and only if the displacement vector from $P$ to $(x, y, z)$ is orthogonal to the normal vector $n$:
   $$n \cdot \begin{pmatrix}x - x_0 \\ y - y_0 \\ z - z_0\end{pmatrix} = 0.$$
   $$2(x - 1) + 1(y - (-2)) - 1(z - 3) = 0$$
   $$2x - 2 + y + 2 - z + 3 = 0 \implies 2x + y - z + 3 = 0.$$

2. **Check with Point $P(1, -2, 3)$:**
   $$2(1) + (-2) - (3) + 3 = 2 - 2 - 3 + 3 = 0.$$
   The equation is satisfied.

3. **Role of the Normal Vector:**
   The normal vector $n$ establishes the spatial tilt and orientation of the plane. Any vector lying entirely within the plane is orthogonal to $n$. Once the orientation is fixed by $n$, specifying the point $P$ fixes the plane's precise position in space.

## 4. Verification and Consistency Checks
The analytical derivation is verified through algebraic consistency, dimensional checking, and direct substitution back into the governing problem definitions.
