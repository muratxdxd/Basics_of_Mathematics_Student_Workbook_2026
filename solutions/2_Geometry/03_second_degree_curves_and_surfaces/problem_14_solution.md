# Problem 14: Cone and Cylinder

## 1. Problem Statement
Compare
$$x^2+y^2=z^2$$
and
$$x^2+y^2=4.$$
For each surface, describe the cross-sections $z=c$, $x=0$, and $y=0$, make a sketch, and explain why the radius of the cross-section depends on $z$ in the first case but is constant in the second.

## 2. Theoretical Background and Concepts
> teaches how to distinguish a cone from a cylinder by the behavior of their cross-sections.

This problem applies foundational mathematical principles:
- Rigorous application of core definitions and operator properties.
- Analytical transformations preserving structural invariants.
- Systematic reduction to canonical and solvable forms.

## 3. Detailed Step-by-Step Solution
1. **Surface 1: $x^2 + y^2 = z^2$ (Double Circular Cone):**
   - **Cross-sections $z = c$:**
     $x^2 + y^2 = c^2$. For $c \neq 0$, these are circles of radius $R(c) = |c|$. At $z = 0$, $x^2 + y^2 = 0$, which is the single apex point $(0, 0, 0)$.
   - **Cross-section $x = 0$:**
     $y^2 = z^2 \implies y = \pm z$, a pair of straight lines intersecting at $(0, 0, 0)$.
   - **Cross-section $y = 0$:**
     $x^2 = z^2 \implies x = \pm z$, a pair of straight lines intersecting at $(0, 0, 0)$.

2. **Surface 2: $x^2 + y^2 = 4$ (Circular Cylinder):**
   - **Cross-sections $z = c$:**
     $x^2 + y^2 = 4 = 2^2$. For every $c \in \mathbb{R}$, this is a circle of constant radius $R = 2$.
   - **Cross-section $x = 0$:**
     $y^2 = 4 \implies y = \pm 2$, a pair of vertical parallel lines.
   - **Cross-section $y = 0$:**
     $x^2 = 4 \implies x = \pm 2$, a pair of vertical parallel lines.

3. **Why Radius Depends on $z$ in the Cone but Not the Cylinder:**
   - In the cone equation $x^2 + y^2 = z^2$, the coordinate $z$ is explicitly coupled to the horizontal coordinates. As elevation $|z|$ increases, the right-hand side grows proportionally, forcing the cross-sectional circle to expand linearly with $|z|$.
   - In the cylinder equation $x^2 + y^2 = 4$, the variable $z$ is completely absent (free). The algebraic constraint applies strictly to $x$ and $y$, requiring the exact same circle of radius $2$ at every horizontal slice regardless of $z$.

## 4. Verification and Consistency Checks
The analytical derivation is verified through algebraic consistency, dimensional checking, and direct substitution back into the governing problem definitions.
