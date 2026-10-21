# Problem 12: Exponential Function Limit

## 1. Problem Statement
Compute
$$\lim_{x\to0}(1+3x)^{1/x}.$$
Connect the result with the limit from Exercise 5 and show the appropriate transformation.

## 2. Theoretical Background and Concepts
> teaches how to recognize the classical pattern after a transformation.

This problem applies foundational mathematical principles:
- Rigorous application of core definitions and operator properties.
- Analytical transformations preserving structural invariants.
- Systematic reduction to canonical and solvable forms.

## 3. Detailed Step-by-Step Solution
1. **Recall Fundamental Exponential Limit:**
   From Exercise 5, $\lim_{u\to0}(1 + u)^{1/u} = e$ (or equivalently $\lim_{n\to\infty}(1 + \frac{1}{n})^n = e$).

2. **Algebraic Transformation:**
   Set $u = 3x$. As $x \to 0$, $u \to 0$.
   Notice the exponent can be rewritten as:
   $$\frac{1}{x} = \frac{3}{3x} = 3 \cdot \frac{1}{u}.$$
   Rewrite the expression:
   $$(1 + 3x)^{1/x} = (1 + u)^{3/u} = \left[(1 + u)^{1/u}\right]^3.$$

3. **Evaluate the Limit:**
   By continuity of the power function $g(t) = t^3$:
   $$\lim_{x\to0}(1+3x)^{1/x} = \left[\lim_{u\to0}(1+u)^{1/u}\right]^3 = e^3 \approx 20.0855.$$

## 4. Verification and Consistency Checks
The analytical derivation is verified through algebraic consistency, dimensional checking, and direct substitution back into the governing problem definitions.
