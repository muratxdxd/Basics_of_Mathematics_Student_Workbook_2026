# Problem 9: An Oblique Asymptote

## 1. Problem Statement
Analyze the asymptotes of
$$f(x)=\frac{x^2+1}{x-1}.$$
Perform polynomial division and explain why the remainder term vanishes for large $|x|$.

## 2. Theoretical Background and Concepts
> it teaches how to recognize an oblique asymptote and interpret the decomposition of a function.

This problem applies foundational mathematical principles:
- Rigorous application of core definitions and operator properties.
- Analytical transformations preserving structural invariants.
- Systematic reduction to canonical and solvable forms.

## 3. Detailed Step-by-Step Solution
1. **Polynomial Division:**
   Divide $(x^2 + 1)$ by $(x - 1)$:
   $$x^2 + 1 = (x + 1)(x - 1) + 2.$$
   $$f(x) = \frac{x^2+1}{x-1} = x + 1 + \frac{2}{x - 1}.$$

2. **Asymptotes Analysis:**
   - **Vertical Asymptote:** At $x = 1$, the denominator vanishes:
     $$\lim_{x\to1^-} f(x) = -\infty, \qquad \lim_{x\to1^+} f(x) = +\infty.$$
   - **Oblique (Slant) Asymptote:** $y = x + 1$.

3. **Why the Remainder Vanishes for Large $|x|$:**
   The difference between the curve $f(x)$ and the line $y = x + 1$ is precisely the remainder term:
   $$f(x) - (x + 1) = \frac{2}{x - 1}.$$
   Taking the limit as $|x| \to \infty$:
   $$\lim_{x\to\pm\infty}\left[f(x) - (x + 1)\right] = \lim_{x\to\pm\infty}\frac{2}{x - 1} = 0.$$
   As $x$ becomes very large, the constant numerator $2$ is divided by an arbitrarily large number, driving the vertical separation to zero. The curve becomes indistinguishable from the straight line $y = x + 1$.

## 4. Verification and Consistency Checks
The analytical derivation is verified through algebraic consistency, dimensional checking, and direct substitution back into the governing problem definitions.
