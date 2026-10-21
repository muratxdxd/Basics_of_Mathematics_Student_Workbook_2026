# Problem 14: Reconstructing Information from the Derivative

## 1. Problem Statement
It is known that
$$f'(x)=(x-1)(x+2).$$
Determine the monotonicity and the locations of the extrema, and sketch a possible qualitative shape of the function. Then, for
$$g(x)=\frac{x^3}{3}+\frac{x^2}{2}-2x$$
verify that $g'(x)=(x-1)(x+2)$, and compare the specific graph with the earlier qualitative sketch.

## 2. Theoretical Background and Concepts
> it teaches how to read the behavior of a function directly from its derivative.

This problem applies foundational mathematical principles:
- Rigorous application of core definitions and operator properties.
- Analytical transformations preserving structural invariants.
- Systematic reduction to canonical and solvable forms.

## 3. Detailed Step-by-Step Solution
1. **Monotonicity and Extrema from $f'(x) = (x - 1)(x + 2)$:**
   Roots of $f'(x)$: $x = -2$ and $x = 1$.
   The derivative is an upward-opening parabola ($x^2 + x - 2$):
   - On $(-\infty, -2)$: $f'(x) > 0 \implies f$ is **strictly increasing**.
   - On $(-2, 1)$: $f'(x) < 0 \implies f$ is **strictly decreasing**.
   - On $(1, \infty)$: $f'(x) > 0 \implies f$ is **strictly increasing**.
   **Extrema:**
   - At $x = -2$: $f'$ changes from $+$ to $-$ $\implies$ **Local Maximum**.
   - At $x = 1$: $f'$ changes from $-$ to $+$ $\implies$ **Local Minimum**.

2. **Qualitative Shape:**
   The function rises from $-\infty$ to a local peak at $x = -2$, drops down to a local valley at $x = 1$, and then rises toward $+\infty$.

3. **Verify $g'(x)$:**
   $$g(x) = \frac{x^3}{3} + \frac{x^2}{2} - 2x.$$
   $$g'(x) = \frac{3x^2}{3} + \frac{2x}{2} - 2 = x^2 + x - 2 = (x - 1)(x + 2).$$
   The derivative matches $f'(x)$ identically.

4. **Specific Values for $g(x)$:**
   - Local maximum value at $x = -2$:
     $$g(-2) = \frac{(-2)^3}{3} + \frac{(-2)^2}{2} - 2(-2) = -\frac{8}{3} + 2 + 4 = -\frac{8}{3} + 6 = \frac{10}{3} \approx 3.33.$$
   - Local minimum value at $x = 1$:
     $$g(1) = \frac{1}{3} + \frac{1}{2} - 2 = \frac{5}{6} - 2 = -\frac{7}{6} \approx -1.17.$$
   - Intercept: $g(0) = 0$.
   The concrete graph of $g(x)$ has its peak at $\left(-2, \frac{10}{3}\right)$ and its valley at $\left(1, -\frac{7}{6}\right)$, perfectly validating the qualitative sketch deduced from the derivative.

## 4. Verification and Consistency Checks
The analytical derivation is verified through algebraic consistency, dimensional checking, and direct substitution back into the governing problem definitions.
