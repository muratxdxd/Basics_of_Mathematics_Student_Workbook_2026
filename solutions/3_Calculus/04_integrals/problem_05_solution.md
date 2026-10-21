# Problem 5: The Same Substitution in a Different Context

## 1. Problem Statement
Compute
$$\int xe^{x^2}\,dx.$$
First compare the structure with Problem 4 and explain what is common despite the different appearance of the function.

## 2. Theoretical Background and Concepts
> it shows that the substitution mechanism is recognized by structure, not by the type of function.

This problem applies foundational mathematical principles:
- Rigorous application of core definitions and operator properties.
- Analytical transformations preserving structural invariants.
- Systematic reduction to canonical and solvable forms.

## 3. Detailed Step-by-Step Solution
1. **Structural Comparison with Problem 4:**
   In both problems, the integrand contains an inner expression $g(x) = x^2$ (or $x^2+1$) encapsulated inside an outer function (a power $(\cdot)^4$ in Problem 4, an exponential $e^{(\cdot)}$ here), multiplied by a factor $x$ proportional to the inner derivative $g'(x) = 2x$. Even though the outer functions are different, both integrals possess the universal substitution structure $\int f(g(x))g'(x)\,dx$.

2. **Compute via Substitution:**
   Let $u = x^2 \implies du = 2x\,dx \implies x\,dx = \frac{1}{2}du$.
   $$\int x e^{x^2}\,dx = \int e^{x^2}(x\,dx) = \int e^u \left(\frac{1}{2}du\right) = \frac{1}{2}\int e^u\,du = \frac{1}{2}e^u + C = \frac{1}{2}e^{x^2} + C.$$

## 4. Verification and Consistency Checks
3. **Verification:**
   $$\frac{d}{dx}\left(\frac{1}{2}e^{x^2} + C\right) = \frac{1}{2}e^{x^2}\cdot(2x) = x e^{x^2}.$$
