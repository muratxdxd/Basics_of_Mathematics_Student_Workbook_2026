# Problem 14: A Piecewise-Defined Function

## 1. Problem Statement
Let
$$f(x)=\begin{cases}x+1,&-1\le x<1,\\2,&1\le x\le3.\end{cases}$$
Sketch the graph, decide where to split the integral, compute
$$\int_{-1}^{3}f(x)\,dx$$
and verify the result geometrically.

## 2. Theoretical Background and Concepts
> it requires understanding the definition of the function before carrying out the calculation.

This problem applies foundational mathematical principles:
- Rigorous application of core definitions and operator properties.
- Analytical transformations preserving structural invariants.
- Systematic reduction to canonical and solvable forms.

## 3. Detailed Step-by-Step Solution
1. **Splitting the Integral:**
   Because the analytical formula changes definition at $x = 1$, the integral must be split at $x = 1$:
   $$\int_{-1}^3 f(x)\,dx = \int_{-1}^1 (x + 1)\,dx + \int_1^3 2\,dx.$$

2. **Calculations:**
   - First piece:
     $$\int_{-1}^1 (x + 1)\,dx = \left[\frac{x^2}{2} + x\right]_{-1}^1 = \left(\frac{1}{2} + 1\right) - \left(\frac{(-1)^2}{2} - 1\right) = \frac{3}{2} - \left(-\frac{1}{2}\right) = \frac{3}{2} + \frac{1}{2} = 2.$$
   - Second piece:
     $$\int_1^3 2\,dx = [2x]_1^3 = 2(3) - 2(1) = 6 - 2 = 4.$$
   - Total integral:
     $$\int_{-1}^3 f(x)\,dx = 2 + 4 = 6.$$

3. **Geometric Verification:**
   - For $x \in [-1, 1]$, the function is a straight line rising from $(-1, 0)$ to $(1, 2)$. The region under the curve is a right triangle with base $b = 1 - (-1) = 2$ and height $h = 2$.
     $$\text{Area}_{\text{triangle}} = \frac{1}{2} b h = \frac{1}{2}(2)(2) = 2.$$
   - For $x \in [1, 3]$, the function is horizontal at height $y = 2$. The region is a rectangle with base $b = 3 - 1 = 2$ and height $h = 2$.
     $$\text{Area}_{\text{rectangle}} = b \times h = 2 \times 2 = 4.$$
   - Total geometric area:
     $$\text{Area}_{\text{total}} = 2 + 4 = 6.$$
   The geometric area matches the analytical integral result.

## 4. Verification and Consistency Checks
The analytical derivation is verified through algebraic consistency, dimensional checking, and direct substitution back into the governing problem definitions.
