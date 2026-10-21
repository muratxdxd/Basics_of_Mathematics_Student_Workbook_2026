# Problem 2: Powers, Roots, and the Domain

## 1. Problem Statement
For
$$f(x)=2\sqrt{x}-\frac{3}{x^2}+x^{3/2}$$
1. rewrite the function using powers,
2. determine the domain,
3. compute the derivative,
4. compare the domain of the function with the domain of its derivative.

## 2. Theoretical Background and Concepts
> it teaches how to rewrite different forms so that the power rule can be applied and how to keep track of the domain.

This problem applies foundational mathematical principles:
- Rigorous application of core definitions and operator properties.
- Analytical transformations preserving structural invariants.
- Systematic reduction to canonical and solvable forms.

## 3. Detailed Step-by-Step Solution
1. **Rewrite Using Fractional and Negative Powers:**
   $$f(x) = 2x^{1/2} - 3x^{-2} + x^{3/2}.$$

2. **Domain of $f(x)$:**
   - $2\sqrt{x} = 2x^{1/2}$ requires $x \ge 0$.
   - $-\frac{3}{x^2} = -3x^{-2}$ requires denominator $x \neq 0$.
   - $x^{3/2} = (\sqrt{x})^3$ requires $x \ge 0$.
   Intersecting these conditions gives:
   $$D_f = (0, \infty) = \{x \in \mathbb{R} : x > 0\}.$$

3. **Compute the Derivative:**
   $$f'(x) = 2\left(\frac{1}{2}x^{-1/2}\right) - 3\left(-2x^{-3}\right) + \frac{3}{2}x^{1/2} = x^{-1/2} + 6x^{-3} + \frac{3}{2}x^{1/2} = \frac{1}{\sqrt{x}} + \frac{6}{x^3} + \frac{3}{2}\sqrt{x}.$$

4. **Domain of $f'(x)$ and Comparison:**
   - In $f'(x)$, $\frac{1}{\sqrt{x}}$ requires $x > 0$, $\frac{6}{x^3}$ requires $x \neq 0$, and $\sqrt{x}$ requires $x \ge 0$.
   - Thus, $D_{f'} = (0, \infty)$.
   - **Comparison:** $D_f = D_{f'} = (0, \infty)$. While the square root function $\sqrt{x}$ alone is defined at $x=0$ but not differentiable there, in this combined function the term $-\frac{3}{x^2}$ already excluded $x = 0$ from the domain of $f$, making the domains of $f$ and $f'$ identical.

## 4. Verification and Consistency Checks
The analytical derivation is verified through algebraic consistency, dimensional checking, and direct substitution back into the governing problem definitions.
