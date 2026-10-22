# Problem 8: Intersection Point of a Line and a Plane

## 1. Problem Statement
Find the intersection point of
$$(x,y,z)=(1,0,2)+t(1,2,-1)$$
with the plane $x+y+z=4$. Check the result by substituting it into both descriptions.

## 2. Theoretical Background and Concepts
> practices the most important computational case of the lineâ€“plane relationship.

This problem applies foundational mathematical principles:
- Rigorous application of core definitions and operator properties.
- Analytical transformations preserving structural invariants.
- Systematic reduction to canonical and solvable forms.

## 3. Detailed Step-by-Step Solution
1. **Substitute Parametric Coordinates into Plane Equation:**
   $$x = 1 + t, \qquad y = 2t, \qquad z = 2 - t.$$
   Each value of $t$ gives a point on the line with these coordinates. Substituting them into the plane equation selects the value of $t$ for which that line point also belongs to the plane:
   $$(1 + t) + (2t) + (2 - t) = 4.$$
   $$3 + 2t = 4 \implies 2t = 1 \implies t = \frac{1}{2} = 0.5.$$

2. **Compute the Intersection Point:**
   $$x = 1 + 0.5 = 1.5 = \frac{3}{2},$$
   $$y = 2(0.5) = 1,$$
   $$z = 2 - 0.5 = 1.5 = \frac{3}{2}.$$
   Intersection point: $P = \left(\frac{3}{2}, 1, \frac{3}{2}\right) = (1.5, 1, 1.5)$.

## 4. Verification and Consistency Checks
3. **Verification:**
   These two substitutions check membership in both sets:
   - **On the line:** For $t = 0.5$, $(1, 0, 2) + 0.5(1, 2, -1) = (1.5, 1, 1.5)$ (matches).
   - **In the plane:** $1.5 + 1 + 1.5 = 4$ (holds).
