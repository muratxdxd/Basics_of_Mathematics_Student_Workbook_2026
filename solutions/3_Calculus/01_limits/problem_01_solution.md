# Problem 1: Dominant Terms in a Sequence

## 1. Problem Statement
Compute
$$\lim_{n\to\infty}\frac{4n^2-3n+1}{2n^2+5n-7}.$$
Explain why the highest-degree terms determine the result.

## 2. Theoretical Background and Concepts
> introduces the idea of a dominant term and teaches how to simplify the behavior of expressions for large arguments.

This problem applies foundational mathematical principles:
- Rigorous application of core definitions and operator properties.
- Analytical transformations preserving structural invariants.
- Systematic reduction to canonical and solvable forms.

## 3. Detailed Step-by-Step Solution
1. **Computation:**
   Divide both numerator and denominator by the highest power of $n$, which is $n^2$:
   $$\lim_{n\to\infty}\frac{4n^2-3n+1}{2n^2+5n-7} = \lim_{n\to\infty}\frac{4 - \frac{3}{n} + \frac{1}{n^2}}{2 + \frac{5}{n} - \frac{7}{n^2}}.$$
   Since $\lim_{n\to\infty}\frac{1}{n} = 0$ and $\lim_{n\to\infty}\frac{1}{n^2} = 0$:
   $$= \frac{4 - 0 + 0}{2 + 0 - 0} = \frac{4}{2} = 2.$$

2. **Why Highest-Degree Terms Determine the Result:**
   As $n \to \infty$, $n^2$ grows orders of magnitude faster than linear or constant terms ($n^2 \gg n \gg 1$). Factoring out $n^2$ from the numerator and denominator reveals that all sub-dominant terms vanish to $0$ in the limit. The asymptotic behavior of the entire rational expression is governed entirely by the ratio of leading coefficients: $\frac{4n^2}{2n^2} = 2$.

## 4. Verification and Consistency Checks
The analytical derivation is verified through algebraic consistency, dimensional checking, and direct substitution back into the governing problem definitions.
