# Problem 12: Recognizing a Surface from Cross-Sections

## 1. Problem Statement
A certain surface has the following properties:
- the cross-section $z=0$ is a point,
- for $z>0$, the cross-sections $z=\text{const}$ are circles with increasing radius,
- vertical cross-sections through the $Oz$ axis are parabolas.

Propose a simple equation for such a surface and justify your choice.

## 2. Theoretical Background and Concepts
> reverses the usual reasoning: from geometry to an equation.

This problem applies foundational mathematical principles:
- Rigorous application of core definitions and operator properties.
- Analytical transformations preserving structural invariants.
- Systematic reduction to canonical and solvable forms.

## 3. Detailed Step-by-Step Solution
1. **Proposed Equation:**
   $$z = x^2 + y^2.$$

2. **Justification of All Three Properties:**
   - **Property 1 ($z = 0$ is a point):**
     Substituting $z = 0$ gives $x^2 + y^2 = 0$. In real coordinates, this holds only when $x = 0$ and $y = 0$. Hence, the cross-section is the single point $(0, 0, 0)$.
   - **Property 2 ($z = \text{const} > 0$ are circles of increasing radius):**
     Setting $z = c > 0$ gives $x^2 + y^2 = c = (\sqrt{c})^2$. This is a circle in the plane $z = c$ centered on the $z$-axis with radius $R(c) = \sqrt{c}$. As $c$ increases, the radius $\sqrt{c}$ increases strictly monotonically.
   - **Property 3 (vertical cross-sections through $Oz$ are parabolas):**
     Any vertical plane through the $z$-axis can be parameterized by angle $\theta$: $x = r\cos\theta, y = r\sin\theta$.
     Substituting these into the surface equation:
     $$z = (r\cos\theta)^2 + (r\sin\theta)^2 = r^2(\cos^2\theta + \sin^2\theta) = r^2.$$
     In the coordinate plane $(r, z)$, the equation is $z = r^2$, which is an upward-opening parabola with vertex at the origin.
   This surface is an elliptic (circular) paraboloid of revolution.

## 4. Verification and Consistency Checks
The analytical derivation is verified through algebraic consistency, dimensional checking, and direct substitution back into the governing problem definitions.
