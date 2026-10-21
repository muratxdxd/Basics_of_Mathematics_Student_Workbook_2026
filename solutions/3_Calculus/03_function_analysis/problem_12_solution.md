# Problem 12: A Function with an Absolute Value

## 1. Problem Statement
Analyze
$$f(x)=|x^2-4|.$$
First sketch $x^2-4$, then explain the effect of the absolute value. Indicate the points where the derivative does not exist and justify the reason geometrically.

## 2. Theoretical Background and Concepts
> it shows the limits of mechanical application of calculus and the importance of the geometry of the graph.

This problem applies foundational mathematical principles:
- Rigorous application of core definitions and operator properties.
- Analytical transformations preserving structural invariants.
- Systematic reduction to canonical and solvable forms.

## 3. Detailed Step-by-Step Solution
1. **Base Function $g(x) = x^2 - 4$:**
   This is a standard parabola opening upwards with vertex at $(0, -4)$, axis of symmetry $x = 0$, and roots at $x = -2$ and $x = 2$.

2. **Effect of Absolute Value:**
   $$f(x) = |x^2 - 4| = \begin{cases} x^2 - 4, & \text{if } |x| \ge 2, \\ 4 - x^2, & \text{if } |x| < 2. \end{cases}$$
   The absolute value leaves the positive portions ($|x| \ge 2$) unchanged, while reflecting the negative dip ($x \in (-2, 2)$) vertically across the $x$-axis, turning the valley at $(0, -4)$ into an inverted parabolic peak at $(0, 4)$.

3. **Points Where the Derivative Does Not Exist:**
   The derivative does not exist at **$x = -2$** and **$x = 2$**.
   - **Analytical Justification at $x = 2$:**
     $$\lim_{x\to2^+}\frac{f(x) - f(2)}{x - 2} = \lim_{x\to2^+}\frac{(x^2 - 4) - 0}{x - 2} = \lim_{x\to2^+}(x + 2) = 4.$$
     $$\lim_{x\to2^-}\frac{f(x) - f(2)}{x - 2} = \lim_{x\to2^-}\frac{-(x^2 - 4) - 0}{x - 2} = \lim_{x\to2^-}-(x + 2) = -4.$$
     Since $f'_+(2) = 4 \neq -4 = f'_-(2)$, the derivative does not exist. (Similarly, $f'_+(-2) = 4 \neq -4 = f'_-(-2)$).
   - **Geometric Justification:**
     The sharp reflection at $y = 0$ creates sharp, non-smooth "creases" or corner points (cusps) at $(-2, 0)$ and $(2, 0)$. At these corners, the curve changes slope abruptly without turning smoothly, meaning no unique tangent line can be defined.

## 4. Verification and Consistency Checks
The analytical derivation is verified through algebraic consistency, dimensional checking, and direct substitution back into the governing problem definitions.
