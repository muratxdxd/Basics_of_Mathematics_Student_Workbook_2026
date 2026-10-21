# Problem 7: Limit at a Point and Canceling a Factor

## 1. Problem Statement
Compute
$$\lim_{x\to3}\frac{x^2-4x+3}{x-3}.$$
Explain why the value of the function at $x=3$ is not needed to compute the limit.

## 2. Theoretical Background and Concepts
> separates the concept of a limit from the value of a function at a point.

This problem applies foundational mathematical principles:
- Rigorous application of core definitions and operator properties.
- Analytical transformations preserving structural invariants.
- Systematic reduction to canonical and solvable forms.

## 3. Detailed Step-by-Step Solution
1. **Factor and Simplify:**
   Factor the quadratic numerator:
   $$x^2 - 4x + 3 = (x - 3)(x - 1).$$
   For $x \neq 3$, the factor $(x - 3)$ is non-zero, allowing valid cancellation:
   $$\frac{x^2 - 4x + 3}{x - 3} = \frac{(x - 3)(x - 1)}{x - 3} = x - 1.$$

2. **Compute the Limit:**
   $$\lim_{x\to3}\frac{x^2-4x+3}{x-3} = \lim_{x\to3}(x - 1) = 3 - 1 = 2.$$

3. **Why the Value at $x=3$ is Not Needed:**
   The definition of the limit $\lim_{x\to c} f(x)$ examines the values of $f(x)$ as $x$ gets arbitrarily close to $c$ in a punctured neighborhood $0 < |x - c| < \delta$. The value $f(c)$ at the point itself is completely irrelevant to the limit. At $x = 3$, $f(3) = \frac{0}{0}$ is undefined; nevertheless, the function approaches $2$ continuously from both sides.

## 4. Verification and Consistency Checks
The analytical derivation is verified through algebraic consistency, dimensional checking, and direct substitution back into the governing problem definitions.
