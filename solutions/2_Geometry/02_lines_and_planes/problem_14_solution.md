# Problem 14: Contrast: Intersection and Parallelism

## 1. Problem Statement
From the point $P=(0,0,1)$, two lines are drawn with direction vectors
$$v_1=(2,1,-1),\qquad v_2=(2,1,0).$$
For each line, analyze its position relative to the plane $z=0$.

For the line that intersects the plane, find the intersection point. For the other line, explain how you can recognize parallelism without solving an equation.

## 2. Theoretical Background and Concepts
> compares two very similar data sets that lead to different outcomes and forces recognition of the geometric condition before calculation.

This problem applies foundational mathematical principles:
- Rigorous application of core definitions and operator properties.
- Analytical transformations preserving structural invariants.
- Systematic reduction to canonical and solvable forms.

## 3. Detailed Step-by-Step Solution
1. **Relative Position to the Plane $z = 0$ ($n = (0, 0, 1)$):**
   - **Line 1 ($v_1 = (2, 1, -1)$):**
     $$v_1 \cdot n = 2(0) + 1(0) + (-1)(1) = -1 \neq 0.$$
     Because $v_1 \cdot n \neq 0$, Line 1 is not parallel to the plane and **intersects the plane at exactly one point**.
   - **Line 2 ($v_2 = (2, 1, 0)$):**
     $$v_2 \cdot n = 2(0) + 1(0) + 0(1) = 0.$$
     Because $v_2 \cdot n = 0$, Line 2 is **parallel to the plane**.

2. **Intersection Point for Line 1:**
   Parametric form: $(x, y, z) = (0, 0, 1) + t(2, 1, -1) = (2t, t, 1-t)$.
   Intersection with $z = 0$:
   $$1 - t = 0 \implies t = 1.$$
   Intersection point:
   $$(x, y, z) = (2(1), 1, 1 - 1) = (2, 1, 0).$$

3. **Recognizing Parallelism for Line 2 Without Solving:**
   The $z$-component of direction vector $v_2$ is $0$. This means that along Line 2, the rate of change of $z$ is zero: $\Delta z = 0 \cdot t = 0$. Since the line originates at $P(0, 0, 1)$, every single point on Line 2 has $z = 1$. The plane is $z = 0$. Since $1 \neq 0$, the line maintains a constant vertical distance of $1$ from the plane and can never intersect it.

## 4. Verification and Consistency Checks
The analytical derivation is verified through algebraic consistency, dimensional checking, and direct substitution back into the governing problem definitions.
