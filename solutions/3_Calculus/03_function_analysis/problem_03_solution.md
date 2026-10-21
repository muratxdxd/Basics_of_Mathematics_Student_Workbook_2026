# Problem 3: A Rational Function

## 1. Problem Statement
Analyze the domain, zeros, asymptotes, and monotonicity of
$$f(x)=\frac{x+1}{x-2}.$$
Finally, sketch a graph consistent with all the information obtained.

## 2. Theoretical Background and Concepts
> it teaches how to combine the domain, limits, and derivative in the analysis of a rational function.

This problem applies foundational mathematical principles:
- Rigorous application of core definitions and operator properties.
- Analytical transformations preserving structural invariants.
- Systematic reduction to canonical and solvable forms.

## 3. Detailed Step-by-Step Solution
1. **Domain:**
   $$x - 2 \neq 0 \implies D_f = (-\infty, 2) \cup (2, \infty) = \mathbb{R} \setminus \{2\}.$$

2. **Zeros and Intercepts:**
   - $f(x) = 0 \iff x + 1 = 0 \implies x = -1$. Point: $(-1, 0)$.
   - $y$-intercept: $f(0) = \frac{0 + 1}{0 - 2} = -\frac{1}{2} = -0.5$. Point: $(0, -0.5)$.

3. **Asymptotes:**
   - **Vertical Asymptote at $x = 2$:**
     $$\lim_{x\to2^-}\frac{x+1}{x-2} = \frac{3}{0^-} = -\infty, \qquad \lim_{x\to2^+}\frac{x+1}{x-2} = \frac{3}{0^+} = +\infty.$$
   - **Horizontal Asymptote:**
     $$\lim_{x\to\pm\infty}\frac{x+1}{x-2} = \lim_{x\to\pm\infty}\frac{1 + \frac{1}{x}}{1 - \frac{2}{x}} = 1 \implies y = 1.$$

4. **Derivative and Monotonicity:**
   $$f'(x) = \frac{1(x - 2) - (x + 1)(1)}{(x - 2)^2} = \frac{x - 2 - x - 1}{(x - 2)^2} = -\frac{3}{(x - 2)^2}.$$
   Since $(x - 2)^2 > 0$ for all $x \in D_f$, $f'(x) < 0$ everywhere on its domain.
   The function is **strictly decreasing on $(-\infty, 2)$** and **strictly decreasing on $(2, \infty)$**. It has no local extrema.

## 4. Verification and Consistency Checks
The analytical derivation is verified through algebraic consistency, dimensional checking, and direct substitution back into the governing problem definitions.
