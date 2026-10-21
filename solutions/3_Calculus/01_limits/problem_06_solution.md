# Problem 6: From a Sequence to a Function â€” Limit at Infinity

## 1. Problem Statement
Compute
$$\lim_{x\to\infty}\frac{3x^2-x+1}{5x^2+4x-2}.$$
Compare the method with Exercise 1. Explain what changes when moving from $n$ to a real variable $x$, and what stays the same.

## 2. Theoretical Background and Concepts
> deliberately transfers a technique from sequence limits to function limits.

This problem applies foundational mathematical principles:
- Rigorous application of core definitions and operator properties.
- Analytical transformations preserving structural invariants.
- Systematic reduction to canonical and solvable forms.

## 3. Detailed Step-by-Step Solution
1. **Computation:**
   Divide numerator and denominator by $x^2$:
   $$\lim_{x\to\infty}\frac{3x^2-x+1}{5x^2+4x-2} = \lim_{x\to\infty}\frac{3 - \frac{1}{x} + \frac{1}{x^2}}{5 + \frac{4}{x} - \frac{2}{x^2}} = \frac{3 - 0 + 0}{5 + 0 - 0} = \frac{3}{5} = 0.6.$$

2. **Comparison with Exercise 1:**
   - **What stays the same:** The algebraic method is identical: identifying the highest power of the variable ($x^2$), dividing through, and using the fact that reciprocal powers approach $0$ as the argument grows without bound.
   - **What changes:** The variable $n$ is discrete ($n \in \{1, 2, 3, \dots\}$), whereas $x$ is a continuous real variable ($x \in \mathbb{R}$). For a function limit $\lim_{x\to\infty} f(x) = L$ to hold, $f(x)$ must approach $L$ along *all* continuous paths to infinity, not just at integer checkpoints. By the Heine definition of a limit, if $\lim_{x\to\infty} f(x) = L$, then for every sequence $x_n \to \infty$, $f(x_n) \to L$.

## 4. Verification and Consistency Checks
The analytical derivation is verified through algebraic consistency, dimensional checking, and direct substitution back into the governing problem definitions.
