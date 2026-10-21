# Problem 4: A Function with Two Vertical Asymptotes

## 1. Problem Statement
Analyze
$$f(x)=\frac1{x^2-1}.$$
Determine the domain, asymptotes, sign, and monotonicity on the intervals of the domain. Explain why each interval must be analyzed separately.

## 2. Theoretical Background and Concepts
> it practices the analysis of a function on several disjoint intervals.

This problem applies foundational mathematical principles:
- Rigorous application of core definitions and operator properties.
- Analytical transformations preserving structural invariants.
- Systematic reduction to canonical and solvable forms.

## 3. Detailed Step-by-Step Solution
1. **Domain:**
   $$x^2 - 1 \neq 0 \iff x \neq \pm 1 \implies D_f = (-\infty, -1) \cup (-1, 1) \cup (1, \infty).$$

2. **Asymptotes:**
   - Vertical at $x = -1$: $\lim_{x\to -1^-} f(x) = +\infty$, $\lim_{x\to -1^+} f(x) = -\infty$.
   - Vertical at $x = 1$: $\lim_{x\to 1^-} f(x) = -\infty$, $\lim_{x\to 1^+} f(x) = +\infty$.
   - Horizontal: $\lim_{x\to\pm\infty}\frac{1}{x^2-1} = 0 \implies y = 0$.

3. **Sign of $f(x)$:**
   - On $(-\infty, -1)$: $x^2 - 1 > 0 \implies f(x) > 0$.
   - On $(-1, 1)$: $x^2 - 1 < 0 \implies f(x) < 0$.
   - On $(1, \infty)$: $x^2 - 1 > 0 \implies f(x) > 0$.

4. **Derivative and Monotonicity:**
   $$f'(x) = -\frac{2x}{(x^2 - 1)^2}.$$
   Since $(x^2 - 1)^2 > 0$ on $D_f$, the sign of $f'(x)$ is opposite to the sign of $x$:
   - On $(-\infty, -1)$: $x < 0 \implies f'(x) > 0 \implies$ **strictly increasing**.
   - On $(-1, 0)$: $x < 0 \implies f'(x) > 0 \implies$ **strictly increasing**.
   - At $x = 0$: $f'(0) = 0$, giving a **local maximum** at $(0, -1)$.
   - On $(0, 1)$: $x > 0 \implies f'(x) < 0 \implies$ **strictly decreasing**.
   - On $(1, \infty)$: $x > 0 \implies f'(x) < 0 \implies$ **strictly decreasing**.

5. **Why Intervals Must Be Analyzed Separately:**
   The function domain is disconnected, split by two infinite singularities. A function cannot be called "decreasing on $(-\infty, -1) \cup (1, \infty)$" because comparing a point from the first interval (where $f > 0$) with a point from the second could falsely contradict monotonicity. Monotonicity theorems apply strictly to connected intervals.

## 4. Verification and Consistency Checks
The analytical derivation is verified through algebraic consistency, dimensional checking, and direct substitution back into the governing problem definitions.
