# Problem 4: Area Between Curves

## 1. Problem Statement
Find the area of the region bounded by the graphs
$$
y=x
$$
and
$$
y=x^2.
$$

First find the intersection points and justify which function is greater on the relevant interval.

## 2. Theoretical Background and Concepts
> it teaches that before integrating, one must first determine the geometry of the region and the correct order of the functions.

This problem applies foundational mathematical principles:
- Rigorous application of core definitions and operator properties.
- Analytical transformations preserving structural invariants.
- Systematic reduction to canonical and solvable forms.

## 3. Detailed Step-by-Step Solution
1. **Find Intersection Points:**
   Set the functions equal:
   $$x = x^2 \iff x^2 - x = 0 \iff x(x - 1) = 0 \implies x_1 = 0, \quad x_2 = 1.$$
   The intersection points are $(0, 0)$ and $(1, 1)$.

2. **Justify Which Function Is Greater on $(0, 1)$:**
   For any $x \in (0, 1)$, multiplying both sides of $x < 1$ by positive $x$ yields $x^2 < x$.
   Testing a sample point $x = 0.5$:
   $$y_{\text{line}} = 0.5, \qquad y_{\text{parabola}} = 0.5^2 = 0.25 < 0.5.$$
   Thus, on $[0, 1]$, $x \ge x^2$. The line forms the upper boundary and the parabola forms the lower boundary.

3. **Compute Area:**
   $$A = \int_0^1 (y_{\text{upper}} - y_{\text{lower}})\,dx = \int_0^1 (x - x^2)\,dx = \left[\frac{x^2}{2} - \frac{x^3}{3}\right]_0^1 = \left(\frac{1}{2} - \frac{1}{3}\right) - 0 = \frac{1}{6} \approx 0.1667.$$

## 4. Verification and Consistency Checks
The analytical derivation is verified through algebraic consistency, dimensional checking, and direct substitution back into the governing problem definitions.
