# Problem 12: Symmetry, Sign, and Absolute Value

## 1. Problem Statement
Compare
$$\int_{-2}^{2}x\,dx$$
and
$$\int_{-2}^{2}|x|\,dx.$$
Before calculating, predict the results from symmetry and a sketch, then carry out the calculation and explain the difference.

## 2. Theoretical Background and Concepts
> it teaches how to use symmetry and geometry before applying a computational procedure.

This problem applies foundational mathematical principles:
- Rigorous application of core definitions and operator properties.
- Analytical transformations preserving structural invariants.
- Systematic reduction to canonical and solvable forms.

## 3. Detailed Step-by-Step Solution
1. **Prediction from Symmetry:**
   - $f(x) = x$ is an **odd function** ($f(-x) = -f(x)$). Its graph is symmetric with respect to the origin $(0, 0)$. Over the symmetric interval $[-2, 2]$, the negative signed area on $[-2, 0]$ cancels the positive signed area on $[0, 2]$. **Prediction: $0$**.
   - $g(x) = |x|$ is an **even function** ($g(-x) = g(x)$). Its graph is symmetric with respect to the $y$-axis, and $g(x) \ge 0$ everywhere. The area on $[-2, 0]$ equals the area on $[0, 2]$. Each side is a triangle of base $2$ and height $2$ (area $2$). **Prediction: $2 + 2 = 4$**.

2. **Calculations:**
   $$\int_{-2}^{2}x\,dx = \left[\frac{x^2}{2}\right]_{-2}^{2} = \frac{2^2}{2} - \frac{(-2)^2}{2} = 2 - 2 = 0.$$
   For $|x|$, split at $x = 0$:
   $$\int_{-2}^{2}|x|\,dx = \int_{-2}^0 (-x)\,dx + \int_0^2 x\,dx = \left[-\frac{x^2}{2}\right]_{-2}^0 + \left[\frac{x^2}{2}\right]_0^2 = \left(0 - \left(-\frac{4}{2}\right)\right) + \left(\frac{4}{2} - 0\right) = 2 + 2 = 4.$$

3. **Explanation of the Difference:**
   The absolute value operator acts as a geometric reflector: it flips the negative left triangle from below the $x$-axis to above the $x$-axis. This turns destructive cancellation (where $-2$ canceled $+2$ to yield $0$) into constructive accumulation (where $+2$ adds to $+2$ to yield $4$).

## 4. Verification and Consistency Checks
The analytical derivation is verified through algebraic consistency, dimensional checking, and direct substitution back into the governing problem definitions.
