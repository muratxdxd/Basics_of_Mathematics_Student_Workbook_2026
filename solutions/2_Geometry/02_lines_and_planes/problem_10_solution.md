# Problem 10: Projection of a Point onto a Plane

## 1. Problem Statement
Find the orthogonal projection of $P=(2,1,3)$ onto the plane $x+y+z=3$, and then find the reflection of $P$ across this plane. Check that the midpoint of the segment joining the point and its reflection lies on the plane.

## 2. Theoretical Background and Concepts
> combines the normal, intersection, and distance into the construction of a projection and reflection.

This problem applies foundational mathematical principles:
- Rigorous application of core definitions and operator properties.
- Analytical transformations preserving structural invariants.
- Systematic reduction to canonical and solvable forms.

## 3. Detailed Step-by-Step Solution
1. **Orthogonal Projection $P_0$:**
   The line through $P(2, 1, 3)$ perpendicular to the plane has direction $n = (1, 1, 1)$:
   $$(x, y, z) = (2 + t, 1 + t, 3 + t).$$
   Substitute into $x + y + z = 3$:
   $$(2 + t) + (1 + t) + (3 + t) = 3 \implies 6 + 3t = 3 \implies 3t = -3 \implies t = -1.$$
   Thus, the projection point is:
   $$P_0 = (2 + (-1), 1 + (-1), 3 + (-1)) = (1, 0, 2).$$

2. **Reflection $P'$ Across the Plane:**
   The reflected point corresponds to stepping twice the distance along the normal line ($t = 2(-1) = -2$):
   $$P' = (2 - 2, 1 - 2, 3 - 2) = (0, -1, 1).$$

3. **Midpoint Verification:**
   $$M = \frac{P + P'}{2} = \left(\frac{2 + 0}{2}, \frac{1 + (-1)}{2}, \frac{3 + 1}{2}\right) = (1, 0, 2) = P_0.$$
   Substitute $M(1, 0, 2)$ into the plane equation:
   $$1 + 0 + 2 = 3.$$
   The midpoint coincides with the projection $P_0$ and lies on the plane.

## More Challenging Exercises

## 4. Verification and Consistency Checks
The analytical derivation is verified through algebraic consistency, dimensional checking, and direct substitution back into the governing problem definitions.
