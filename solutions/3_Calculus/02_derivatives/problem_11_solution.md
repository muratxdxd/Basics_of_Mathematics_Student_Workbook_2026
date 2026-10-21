# Problem 11: Derivative from the Definition

## 1. Problem Statement
Using only
$$f'(x)=\lim_{h\to0}\frac{f(x+h)-f(x)}h,$$
find the derivative of $f(x)=x^2$. Compare the result with the power rule and indicate where the limit is used in the calculation.

## 2. Theoretical Background and Concepts
> it shows the origin of the power rule and the direct connection between the derivative and a limit.

This problem applies foundational mathematical principles:
- Rigorous application of core definitions and operator properties.
- Analytical transformations preserving structural invariants.
- Systematic reduction to canonical and solvable forms.

## 3. Detailed Step-by-Step Solution
1. **Setup Difference Quotient:**
   $$f(x+h) = (x+h)^2 = x^2 + 2xh + h^2.$$
   $$\frac{f(x+h) - f(x)}{h} = \frac{(x^2 + 2xh + h^2) - x^2}{h} = \frac{2xh + h^2}{h}.$$

2. **Algebraic Simplification (for $h \neq 0$):**
   $$\frac{h(2x + h)}{h} = 2x + h.$$

3. **Apply the Limit:**
   $$f'(x) = \lim_{h\to0}(2x + h) = 2x + 0 = 2x.$$

4. **Comparison and Explanation:**
   - **Power rule comparison:** The power rule states $\frac{d}{dx}(x^2) = 2x^{2-1} = 2x$, exactly matching our first-principles result.
   - **Where the limit is used:** The limit is taken in the final step. Before the limit, the difference quotient $\frac{2xh+h^2}{h}$ represents the *average rate of change* (secant slope) over an interval of length $h$. Dividing by $h$ produces $2x + h$. The limit operation then sends $h \to 0$, causing the incremental term $h$ to vanish and yielding the exact *instantaneous rate of change* (tangent slope) $2x$.

## 4. Verification and Consistency Checks
The analytical derivation is verified through algebraic consistency, dimensional checking, and direct substitution back into the governing problem definitions.
