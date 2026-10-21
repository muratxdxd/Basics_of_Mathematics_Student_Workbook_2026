# Problem 2: Powers, Roots, and the Domain

## 1. Problem Statement
Compute
$$\int\left(2\sqrt{x}+\frac{3}{x^2}-x^{1/3}\right)\,dx.$$
First rewrite the terms as powers, determine the domain of the original expression, and verify the result by differentiation.

## 2. Theoretical Background and Concepts
> it reinforces the power rule and reminds the student to keep track of the domain.

This problem applies foundational mathematical principles:
- Rigorous application of core definitions and operator properties.
- Analytical transformations preserving structural invariants.
- Systematic reduction to canonical and solvable forms.

## 3. Detailed Step-by-Step Solution
1. **Rewrite as Powers:**
   $$f(x) = 2x^{1/2} + 3x^{-2} - x^{1/3}.$$

2. **Domain of Integrand:**
   - $\sqrt{x} = x^{1/2}$ requires $x \ge 0$.
   - $\frac{3}{x^2} = 3x^{-2}$ requires $x \neq 0$.
   - $x^{1/3}$ is defined on all of $\mathbb{R}$.
   Intersecting these conditions gives:
   $$D_f = (0, \infty).$$

3. **Compute the Integral:**
   $$\int 2x^{1/2}\,dx = 2 \cdot \frac{x^{3/2}}{3/2} = \frac{4}{3}x^{3/2} = \frac{4}{3}x\sqrt{x}.$$
   $$\int 3x^{-2}\,dx = 3 \cdot \frac{x^{-1}}{-1} = -\frac{3}{x}.$$
   $$\int -x^{1/3}\,dx = -\frac{x^{4/3}}{4/3} = -\frac{3}{4}x^{4/3}.$$
   Result:
   $$\int\left(2\sqrt{x}+\frac{3}{x^2}-x^{1/3}\right)\,dx = \frac{4}{3}x^{3/2} - \frac{3}{x} - \frac{3}{4}x^{4/3} + C, \qquad x > 0.$$

## 4. Verification and Consistency Checks
4. **Verification by Differentiation:**
   $$\frac{d}{dx}\left(\frac{4}{3}x^{3/2} - 3x^{-1} - \frac{3}{4}x^{4/3} + C\right) = \frac{4}{3}\left(\frac{3}{2}x^{1/2}\right) - 3\left(-1x^{-2}\right) - \frac{3}{4}\left(\frac{4}{3}x^{1/3}\right) = 2x^{1/2} + 3x^{-2} - x^{1/3} = 2\sqrt{x} + \frac{3}{x^2} - x^{1/3}.$$
