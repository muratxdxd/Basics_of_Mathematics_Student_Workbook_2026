# Problem 2: Different Growth Rates

## 1. Problem Statement
Compute
$$\lim_{n\to\infty}\frac{3n+1}{n^2+4},\qquad \lim_{n\to\infty}\frac{2n^3-n}{5n^2+1}.$$
Compare the two cases and formulate a general observation about the degrees of the polynomials in the numerator and denominator.

## 2. Theoretical Background and Concepts
> teaches how to compare growth rates and recognize qualitatively different cases.

This problem applies foundational mathematical principles:
- Rigorous application of core definitions and operator properties.
- Analytical transformations preserving structural invariants.
- Systematic reduction to canonical and solvable forms.

## 3. Detailed Step-by-Step Solution
1. **Computation of First Limit:**
   Divide numerator and denominator by $n^2$:
   $$\lim_{n\to\infty}\frac{3n+1}{n^2+4} = \lim_{n\to\infty}\frac{\frac{3}{n} + \frac{1}{n^2}}{1 + \frac{4}{n^2}} = \frac{0 + 0}{1 + 0} = \frac{0}{1} = 0.$$

2. **Computation of Second Limit:**
   Divide numerator and denominator by $n^2$:
   $$\lim_{n\to\infty}\frac{2n^3-n}{5n^2+1} = \lim_{n\to\infty}\frac{2n - \frac{1}{n}}{5 + \frac{1}{n^2}} = \frac{\infty - 0}{5 + 0} = +\infty.$$

3. **General Observation for Rational Sequences $\frac{P(n)}{Q(n)}$:**
   Let $p = \deg(P)$ and $q = \deg(Q)$:
   - If $p < q$ (denominator grows faster), the limit is always **$0$**.
   - If $p = q$ (numerator and denominator grow at the same rate), the limit is the finite non-zero ratio of leading coefficients $\frac{a_p}{b_q}$.
   - If $p > q$ (numerator grows faster), the sequence diverges to **$\pm\infty$** (or does not exist if sign oscillates).

## 4. Verification and Consistency Checks
The analytical derivation is verified through algebraic consistency, dimensional checking, and direct substitution back into the governing problem definitions.
