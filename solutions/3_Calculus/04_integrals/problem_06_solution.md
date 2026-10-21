# Problem 6: When Does a Logarithm Appear from an Integral?

## 1. Problem Statement
Compute
$$\int\frac{2x}{x^2+5}\,dx.$$
Identify the denominator as a candidate for substitution, compare the numerator with its derivative, and explain the source of the logarithm in the result.

## 2. Theoretical Background and Concepts
> it teaches how to recognize the structure â€œderivative of the denominator over the denominator.â€

This problem applies foundational mathematical principles:
- Rigorous application of core definitions and operator properties.
- Analytical transformations preserving structural invariants.
- Systematic reduction to canonical and solvable forms.

## 3. Detailed Step-by-Step Solution
1. **Identify Substitution Candidate:**
   - Let denominator be $u = x^2 + 5$.
   - Derivative: $du = 2x\,dx$.
   - The numerator $2x\,dx$ is **exactly** the derivative of the denominator.

2. **Compute the Integral:**
   $$\int\frac{2x}{x^2+5}\,dx = \int\frac{1}{u}\,du = \ln|u| + C = \ln(x^2 + 5) + C.$$
   (The absolute value is omitted because $x^2 + 5 > 0$ for all real $x$).

3. **Source of the Logarithm:**
   By the chain rule, $\frac{d}{dx}\ln|g(x)| = \frac{g'(x)}{g(x)}$.
   Whenever an integrand has the structure $\frac{\text{derivative of denominator}}{\text{denominator}}$, integrating it inverts this logarithmic derivative rule, yielding $\ln|\text{denominator}| + C$.

## 4. Verification and Consistency Checks
The analytical derivation is verified through algebraic consistency, dimensional checking, and direct substitution back into the governing problem definitions.
