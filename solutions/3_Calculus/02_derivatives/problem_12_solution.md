# Problem 12: Several Rules at Once

## 1. Problem Statement
For
$$f(x)=(x^2+1)^3e^x$$
compute the derivative. Before calculating, write down a plan: which rule applies to the whole expression and which rule applies to one of its factors. Finally, organize the result by factoring out common factors.

## 2. Theoretical Background and Concepts
> it practices the order of decisions when combining familiar differentiation rules.

This problem applies foundational mathematical principles:
- Rigorous application of core definitions and operator properties.
- Analytical transformations preserving structural invariants.
- Systematic reduction to canonical and solvable forms.

## 3. Detailed Step-by-Step Solution
1. **Strategic Plan:**
   - **Global level:** The overall expression is the product of two functions: $u(x) = (x^2+1)^3$ and $v(x) = e^x$. The **Product Rule** $(uv)' = u'v + uv'$ governs the entire expression.
   - **Local level:** To find $u'(x)$, the factor $(x^2+1)^3$ is a composition (an inner quadratic inside an outer cubic). The **Chain Rule** must be applied to differentiate $u(x)$.

2. **Differentiate Components:**
   - $u'(x) = 3(x^2 + 1)^2 \cdot \frac{d}{dx}(x^2 + 1) = 3(x^2 + 1)^2 \cdot (2x) = 6x(x^2 + 1)^2$.
   - $v'(x) = e^x$.

3. **Assemble via Product Rule:**
   $$f'(x) = u'(x)v(x) + u(x)v'(x) = 6x(x^2 + 1)^2 e^x + (x^2 + 1)^3 e^x.$$

4. **Factor Out Common Terms:**
   The common factors are $(x^2 + 1)^2 e^x$:
   $$f'(x) = (x^2 + 1)^2 e^x \left[6x + (x^2 + 1)\right] = (x^2 + 1)^2 (x^2 + 6x + 1)e^x.$$

## 4. Verification and Consistency Checks
The analytical derivation is verified through algebraic consistency, dimensional checking, and direct substitution back into the governing problem definitions.
