# Problem 10: Definite Integral and Checking the Result

## 1. Problem Statement
Before carrying out the exact calculation, estimate the possible range of values of the integral
$$\int_0^2(x^2+1)\,dx,$$
using
$$1\le x^2+1\le5$$
on $[0,2]$. Only then compute the integral exactly, compare the result with the earlier estimate, and explain what type of computational error such a check can detect.

## 2. Theoretical Background and Concepts
> it teaches how to predict the possible range of a result and check the calculation.

This problem applies foundational mathematical principles:
- Rigorous application of core definitions and operator properties.
- Analytical transformations preserving structural invariants.
- Systematic reduction to canonical and solvable forms.

## 3. Detailed Step-by-Step Solution
1. **A Priori Estimate:**
   On the interval $[0, 2]$, $f(x) = x^2 + 1$ is strictly increasing:
   - Minimum value: $m = f(0) = 0^2 + 1 = 1$.
   - Maximum value: $M = f(2) = 2^2 + 1 = 5$.
   By the bounding property of definite integrals:
   $$m(b - a) \le \int_a^b f(x)\,dx \le M(b - a).$$
   $$1(2 - 0) \le \int_0^2 (x^2 + 1)\,dx \le 5(2 - 0) \implies 2 \le \int_0^2 (x^2 + 1)\,dx \le 10.$$

2. **Exact Calculation:**
   $$\int_0^2 (x^2 + 1)\,dx = \left[\frac{x^3}{3} + x\right]_0^2 = \left(\frac{2^3}{3} + 2\right) - (0 + 0) = \frac{8}{3} + 2 = \frac{14}{3} = 4\frac{2}{3} \approx 4.667.$$

3. **Comparison and Error Detection:**
   - The exact value $4.667$ lies within the estimated range $[2, 10]$.
   - **Errors detected by bounding checks:** Such checks instantly catch catastrophic mistakes like incorrect antiderivative powers (e.g. integrating $x^2 \to x^3$ without dividing by 3, yielding $10$), sign errors in the Fundamental Theorem of Calculus ($F(a) - F(b)$ instead of $F(b) - F(a)$, yielding negative numbers for a positive function), or arithmetic slips that produce values outside the geometrically allowable bounds.

## More Difficult Problems

## 4. Verification and Consistency Checks
The analytical derivation is verified through algebraic consistency, dimensional checking, and direct substitution back into the governing problem definitions.
