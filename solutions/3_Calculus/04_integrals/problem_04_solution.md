# Problem 4: Substitution as Reversing the Chain Rule

## 1. Problem Statement
Compute
$$\int 2x(x^2+1)^4\,dx.$$
Before calculating, identify a candidate for the new variable $u$ and show that its derivative appears in the integral. Finally, verify the result by differentiation.

## 2. Theoretical Background and Concepts
> it teaches how to recognize substitution as reversing the chain rule.

This problem applies foundational mathematical principles:
- Rigorous application of core definitions and operator properties.
- Analytical transformations preserving structural invariants.
- Systematic reduction to canonical and solvable forms.

## 3. Detailed Step-by-Step Solution
1. **Identify Substitution Candidate:**
   - Candidate for new variable: $u = x^2 + 1$.
   - Differentiate: $du = 2x\,dx$.
   - Notice that the factor $2x\,dx$ appears directly in the integrand.

2. **Substitute and Integrate:**
   $$\int 2x(x^2+1)^4\,dx = \int (x^2+1)^4 \cdot (2x\,dx) = \int u^4\,du = \frac{u^5}{5} + C.$$
   Substitute back $u = x^2 + 1$:
   $$= \frac{(x^2 + 1)^5}{5} + C.$$

## 4. Verification and Consistency Checks
3. **Verification by Differentiation:**
   $$\frac{d}{dx}\left(\frac{(x^2+1)^5}{5} + C\right) = \frac{1}{5} \cdot 5(x^2+1)^4 \cdot \frac{d}{dx}(x^2+1) = (x^2+1)^4 \cdot (2x) = 2x(x^2+1)^4.$$
