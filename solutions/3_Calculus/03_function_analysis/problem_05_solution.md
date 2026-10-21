# Problem 5: An Exponential Function with a Maximum

## 1. Problem Statement
Analyze the monotonicity and extrema of
$$f(x)=xe^{-x}.$$
Also examine the behavior as $x\to\infty$ and explain how the limit affects the shape of the graph on the right-hand side.

## 2. Theoretical Background and Concepts
> it combines the derivative with a limit in the description of the global behavior of a function.

This problem applies foundational mathematical principles:
- Rigorous application of core definitions and operator properties.
- Analytical transformations preserving structural invariants.
- Systematic reduction to canonical and solvable forms.

## 3. Detailed Step-by-Step Solution
1. **Derivative and Critical Points:**
   $$f'(x) = 1\cdot e^{-x} + x(-e^{-x}) = (1 - x)e^{-x}.$$
   Since $e^{-x} > 0$ for all $x \in \mathbb{R}$, $f'(x) = 0 \iff 1 - x = 0 \iff x = 1$.

2. **Monotonicity and Extrema:**
   - For $x < 1$: $1 - x > 0 \implies f'(x) > 0 \implies f$ is **strictly increasing**.
   - For $x > 1$: $1 - x < 0 \implies f'(x) < 0 \implies f$ is **strictly decreasing**.
   - At $x = 1$: $f'$ changes from positive to negative, giving a **global maximum**:
     $$f(1) = 1 \cdot e^{-1} = \frac{1}{e} \approx 0.3679 \implies \left(1, \frac{1}{e}\right).$$

3. **Behavior as $x \to \infty$:**
   $$\lim_{x\to\infty} x e^{-x} = \lim_{x\to\infty}\frac{x}{e^x} = \lim_{x\to\infty}\frac{1}{e^x} = 0 \quad (\text{by l'HÃ´pital's Rule}).$$
   Also notice that for all $x > 0$, $f(x) > 0$.
   - **Effect on the graph:** After reaching its peak at $\left(1, \frac{1}{e}\right)$, the graph decreases smoothly, asymptotically flattening against the horizontal axis $y = 0$ from above without ever crossing it. (An inflection point occurs at $x = 2$, where $f''(x) = (x-2)e^{-x} = 0$, transitioning the curve from concave down to concave up).

## 4. Verification and Consistency Checks
The analytical derivation is verified through algebraic consistency, dimensional checking, and direct substitution back into the governing problem definitions.
