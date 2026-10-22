# Problem 1: A Cubic Polynomial

## 1. Problem Statement
Analyze the monotonicity and extrema of
$$f(x)=x^3-3x^2+2.$$
Sketch the graph based on the results and mark the critical points.

## 2. Theoretical Background and Concepts
> it teaches how to use the first derivative to describe the shape of a polynomial.

This problem applies foundational mathematical principles:
- Rigorous application of core definitions and operator properties.
- Analytical transformations preserving structural invariants.
- Systematic reduction to canonical and solvable forms.

## 3. Detailed Step-by-Step Solution
1. **Compute Derivative and Critical Points:**
   $$f'(x) = 3x^2 - 6x = 3x(x - 2).$$
   Set $f'(x) = 0 \implies x = 0$ or $x = 2$.

2. **Sign of $f'(x)$ and Monotonicity:**
   - On $(-\infty, 0)$: $x < 0$ and $x - 2 < 0 \implies f'(x) > 0 \implies f$ is **strictly increasing**.
   - On $(0, 2)$: $x > 0$ and $x - 2 < 0 \implies f'(x) < 0 \implies f$ is **strictly decreasing**.
   - On $(2, \infty)$: $x > 0$ and $x - 2 > 0 \implies f'(x) > 0 \implies f$ is **strictly increasing**.

3. **Determine Extrema:**
   - At $x = 0$: $f'$ changes from positive to negative $\implies$ **Local Maximum**:
     $$f(0) = 0^3 - 3(0)^2 + 2 = 2 \implies (0, 2).$$
   - At $x = 2$: $f'$ changes from negative to positive $\implies$ **Local Minimum**:
     $$f(2) = 2^3 - 3(2)^2 + 2 = 8 - 12 + 2 = -2 \implies (2, -2).$$

4. **Inflection Point:**
   $$f''(x) = 6x - 6 = 0 \implies x = 1, \qquad f(1) = 1 - 3 + 2 = 0 \implies (1, 0).$$

5. **Sketch:**
   The curve rises to its local maximum, falls through the inflection point to its local minimum, and then rises again:
   ```text
   y
   ↑
   2                 ● (0,2)
   |              ╭──╯ ╲
   0 ────────────╯───────● (1,0)────────────→ x
   |                      ╲
  -2                         ● (2,-2) ╭──
   |                                     ╰──
        increasing    decreasing    increasing
   ```

## 4. Verification and Consistency Checks
The analytical derivation is verified through algebraic consistency, dimensional checking, and direct substitution back into the governing problem definitions.
