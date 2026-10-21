# Problem 9: One-Sided Limits and an Asymptote

## 1. Problem Statement
Analyze the left-hand and right-hand limits of
$$f(x)=\frac1{x-2}$$
as $x\to2$. Does the two-sided limit exist? Interpret the result on a sketch of the graph and identify the vertical asymptote.

## 2. Theoretical Background and Concepts
> teaches how to distinguish one-sided limits and connect them with the geometry of an asymptote.

This problem applies foundational mathematical principles:
- Rigorous application of core definitions and operator properties.
- Analytical transformations preserving structural invariants.
- Systematic reduction to canonical and solvable forms.

## 3. Detailed Step-by-Step Solution
1. **One-Sided Limits:**
   - **Left-hand limit ($x \to 2^-$):**
     As $x$ approaches $2$ from below ($x < 2$), $(x - 2)$ is negative and approaches $0$:
     $$\lim_{x\to2^-}\frac{1}{x-2} = \frac{1}{0^-} = -\infty.$$
   - **Right-hand limit ($x \to 2^+$):**
     As $x$ approaches $2$ from above ($x > 2$), $(x - 2)$ is positive and approaches $0$:
     $$\lim_{x\to2^+}\frac{1}{x-2} = \frac{1}{0^+} = +\infty.$$

2. **Existence of Two-Sided Limit:**
   A two-sided limit exists if and only if both one-sided limits exist and are equal. Since $\lim_{x\to2^-} f(x) = -\infty \neq +\infty = \lim_{x\to2^+} f(x)$, the two-sided limit **does not exist**.

3. **Geometric Interpretation and Asymptote:**
   The line $x = 2$ is a **vertical asymptote**.
   On a graph, as the curve approaches $x = 2$ from the left, it plunges steeply downwards toward $-\infty$. As it approaches from the right, it shoots steeply upwards toward $+\infty$, forming the characteristic opposing branches of a hyperbola.

## 4. Verification and Consistency Checks
The analytical derivation is verified through algebraic consistency, dimensional checking, and direct substitution back into the governing problem definitions.
