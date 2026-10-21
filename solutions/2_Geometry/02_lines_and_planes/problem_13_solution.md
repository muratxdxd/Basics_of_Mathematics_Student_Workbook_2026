# Problem 13: Closest Point on a Plane

## 1. Problem Statement
Find the point on the plane $x+2y+2z=4$ closest to $P=(3,0,0)$. Give the distance and check that the segment joining the two points is perpendicular to the plane.

## 2. Theoretical Background and Concepts
> combines projection, distance, and the normal direction in one problem.

This problem applies foundational mathematical principles:
- Rigorous application of core definitions and operator properties.
- Analytical transformations preserving structural invariants.
- Systematic reduction to canonical and solvable forms.

## 3. Detailed Step-by-Step Solution
1. **Find Closest Point $Q$:**
   The closest point is the orthogonal projection of $P$ onto the plane.
   Normal vector: $n = (1, 2, 2)$.
   Normal line through $P(3, 0, 0)$:
   $$(x, y, z) = (3 + t, 2t, 2t).$$
   Substitute into plane equation:
   $$(3 + t) + 2(2t) + 2(2t) = 4 \implies 3 + 9t = 4 \implies 9t = 1 \implies t = \frac{1}{9}.$$
   Closest point:
   $$Q = \left(3 + \frac{1}{9}, \frac{2}{9}, \frac{2}{9}\right) = \left(\frac{28}{9}, \frac{2}{9}, \frac{2}{9}\right).$$

2. **Distance:**
   $$d(P, \Pi) = \frac{|1(3) + 2(0) + 2(0) - 4|}{\sqrt{1^2 + 2^2 + 2^2}} = \frac{|-1|}{\sqrt{9}} = \frac{1}{3}.$$

3. **Perpendicularity Check:**
   Displacement segment:
   $$\overrightarrow{PQ} = Q - P = \left(\frac{28}{9} - 3, \frac{2}{9} - 0, \frac{2}{9} - 0\right) = \left(\frac{1}{9}, \frac{2}{9}, \frac{2}{9}\right) = \frac{1}{9}(1, 2, 2) = \frac{1}{9}n.$$
   Since $\overrightarrow{PQ}$ is a scalar multiple of the normal vector $n$, the line segment connecting $P$ and $Q$ is perpendicular to the plane.

## 4. Verification and Consistency Checks
The analytical derivation is verified through algebraic consistency, dimensional checking, and direct substitution back into the governing problem definitions.
