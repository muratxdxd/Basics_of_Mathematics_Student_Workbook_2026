# Problem 9: Distances

## 1. Problem Statement
Compute:
1. the distance from $P=(2,3)$ to the line $3x+4y-10=0$,
2. the distance from $Q=(2,-1,3)$ to the plane $2x-2y+z-4=0$.

Compare the two formulas and explain their common connection with the normal direction.

## 2. Theoretical Background and Concepts
> organizes two similar formulas through one geometric idea.

This problem applies foundational mathematical principles:
- Rigorous application of core definitions and operator properties.
- Analytical transformations preserving structural invariants.
- Systematic reduction to canonical and solvable forms.

## 3. Detailed Step-by-Step Solution
1. **Distance from Point to Line in $\mathbb{R}^2$:**
   $$d(P, L) = \frac{|A x_0 + B y_0 + C|}{\sqrt{A^2 + B^2}} = \frac{|3(2) + 4(3) - 10|}{\sqrt{3^2 + 4^2}} = \frac{|6 + 12 - 10|}{\sqrt{25}} = \frac{8}{5} = 1.6.$$

2. **Distance from Point to Plane in $\mathbb{R}^3$:**
   $$d(Q, \Pi) = \frac{|A x_0 + B y_0 + C z_0 + D|}{\sqrt{A^2 + B^2 + C^2}} = \frac{|2(2) - 2(-1) + 1(3) - 4|}{\sqrt{2^2 + (-2)^2 + 1^2}} = \frac{|4 + 2 + 3 - 4|}{\sqrt{4 + 4 + 1}} = \frac{5}{\sqrt{9}} = \frac{5}{3} \approx 1.667.$$

3. **Comparison and Common Connection:**
   Both formulas are instances of the exact same geometric projection:
   $$d = \frac{|\overrightarrow{P_0 P} \cdot n|}{\|n\|} = \left| \overrightarrow{P_0 P} \cdot \frac{n}{\|n\|} \right|.$$
   The shortest distance from a point to a hyperplane (a line in 2D or a plane in 3D) is measured along the perpendicular path, which is parallel to the normal vector $n$. The formula computes the scalar projection of the displacement vector onto the unit normal vector $\hat{n} = \frac{n}{\|n\|}$.

## 4. Verification and Consistency Checks
The analytical derivation is verified through algebraic consistency, dimensional checking, and direct substitution back into the governing problem definitions.
