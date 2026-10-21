# Problem 13: Intersection of a Sphere and a Plane

## 1. Problem Statement
Given the sphere
$$x^2+y^2+z^2=25$$
and the plane $z=3$, find the equation of the intersection curve and its radius. Then describe what happens for $z=c$ depending on $c$.

## 2. Theoretical Background and Concepts
> connects a surface equation with the geometry of its intersection.

This problem applies foundational mathematical principles:
- Rigorous application of core definitions and operator properties.
- Analytical transformations preserving structural invariants.
- Systematic reduction to canonical and solvable forms.

## 3. Detailed Step-by-Step Solution
1. **Intersection with $z = 3$:**
   Substitute $z = 3$ into the sphere equation:
   $$x^2 + y^2 + 3^2 = 25 \implies x^2 + y^2 + 9 = 25 \implies x^2 + y^2 = 16 = 4^2.$$
   - **Equation of the curve:** $x^2 + y^2 = 16$ lying in the plane $z = 3$.
   - **Center:** $(0, 0, 3)$.
   - **Radius:** $R = \sqrt{16} = 4$.

2. **General Behavior for Plane $z = c$:**
   Substitute $z = c$:
   $$x^2 + y^2 = 25 - c^2.$$
   - **Case $|c| < 5$ (Secant Plane):**
     $25 - c^2 > 0$. The intersection is a **circle** in the plane $z = c$ centered at $(0, 0, c)$ with radius $R = \sqrt{25 - c^2}$. (The maximum radius $R = 5$ occurs at the equator $c = 0$).
   - **Case $|c| = 5$ (Tangent Plane):**
     $25 - (\pm 5)^2 = 0 \implies x^2 + y^2 = 0$. The plane touches the sphere at a single point: the north pole $(0, 0, 5)$ for $c = 5$ or the south pole $(0, 0, -5)$ for $c = -5$.
   - **Case $|c| > 5$ (Disjoint Plane):**
     $25 - c^2 < 0$. The equation has no real solutions; the plane does not intersect the sphere.

## 4. Verification and Consistency Checks
The analytical derivation is verified through algebraic consistency, dimensional checking, and direct substitution back into the governing problem definitions.
