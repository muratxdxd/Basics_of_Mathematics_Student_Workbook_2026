# Problem 11: Choose the Method First

## 1. Problem Statement
For each integral, first write which method you choose and how you recognize it, and then compute:
1. $\int\sin(3x)\,dx$,
2. $\int x\ln x\,dx$,
3. $\int\frac{x}{\sqrt{x^2+1}}\,dx$.

## 2. Theoretical Background and Concepts
> it tests the choice of method based on the structure of the problem.

This problem applies foundational mathematical principles:
- Rigorous application of core definitions and operator properties.
- Analytical transformations preserving structural invariants.
- Systematic reduction to canonical and solvable forms.

## 3. Detailed Step-by-Step Solution
1. **Integral 1: $\int\sin(3x)\,dx$:**
   - **Chosen Method:** Linear Substitution.
   - **Recognition:** The argument of the sine is a linear function $ax = 3x$.
   - **Computation:**
     Let $u = 3x \implies du = 3\,dx \implies dx = \frac{1}{3}du$.
     $$\int\sin(3x)\,dx = \frac{1}{3}\int\sin u\,du = -\frac{1}{3}\cos u + C = -\frac{1}{3}\cos(3x) + C.$$

2. **Integral 2: $\int x\ln x\,dx$:**
   - **Chosen Method:** Integration by Parts.
   - **Recognition:** Product of a polynomial ($x$) and a logarithm ($\ln x$). Logarithm cannot be easily integrated directly, but differentiating it yields an algebraic term $\frac{1}{x}$ that cancels powers of $x$.
   - **Computation:**
     Let $u = \ln x \implies u' = \frac{1}{x}$.
     Let $v' = x \implies v = \frac{x^2}{2}$.
     $$\int x\ln x\,dx = \frac{x^2}{2}\ln x - \int \frac{x^2}{2}\cdot\frac{1}{x}\,dx = \frac{x^2}{2}\ln x - \frac{1}{2}\int x\,dx = \frac{x^2}{2}\ln x - \frac{x^2}{4} + C = \frac{x^2}{4}(2\ln x - 1) + C.$$

3. **Integral 3: $\int\frac{x}{\sqrt{x^2+1}}\,dx$:**
   - **Chosen Method:** Substitution.
   - **Recognition:** The expression under the radical is quadratic ($x^2+1$), and the outside multiplying factor is linear ($x\,dx$), which is proportional to the derivative of the inner expression.
   - **Computation:**
     Let $u = x^2 + 1 \implies du = 2x\,dx \implies x\,dx = \frac{1}{2}du$.
     $$\int\frac{x}{\sqrt{x^2+1}}\,dx = \int\frac{\frac{1}{2}du}{\sqrt{u}} = \frac{1}{2}\int u^{-1/2}\,du = \frac{1}{2}\left(\frac{u^{1/2}}{1/2}\right) + C = \sqrt{u} + C = \sqrt{x^2 + 1} + C.$$

## 4. Verification and Consistency Checks
The analytical derivation is verified through algebraic consistency, dimensional checking, and direct substitution back into the governing problem definitions.
