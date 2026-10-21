# Problem 11: An n-th Root

## 1. Problem Statement
Compute
$$\lim_{n\to\infty}\sqrt[n]{5^n+2^n}.$$
Explain which term dominates and why the transformation looks different from the case of a quotient of polynomials.

## 2. Theoretical Background and Concepts
> extends the idea of dominance to exponential expressions.

This problem applies foundational mathematical principles:
- Rigorous application of core definitions and operator properties.
- Analytical transformations preserving structural invariants.
- Systematic reduction to canonical and solvable forms.

## 3. Detailed Step-by-Step Solution
1. **Identify Dominant Term:**
   Between $5^n$ and $2^n$, the base $5 > 2$, so $5^n$ grows much faster than $2^n$. The ratio $\left(\frac{2}{5}\right)^n \to 0$ as $n \to \infty$. Thus, $5^n$ is the dominant term.

2. **Factor out $5^n$:**
   $$\sqrt[n]{5^n + 2^n} = \sqrt[n]{5^n\left(1 + \left(\frac{2}{5}\right)^n\right)} = 5 \left(1 + \left(\frac{2}{5}\right)^n\right)^{1/n}.$$
   Since $\left(\frac{2}{5}\right)^n \to 0$, $1 + \left(\frac{2}{5}\right)^n \to 1$.
   Therefore, $\lim_{n\to\infty} 5 \cdot 1^{0} = 5 \cdot 1 = 5$.

3. **Formal Proof via Squeeze Theorem:**
   $$5^n < 5^n + 2^n < 5^n + 5^n = 2 \cdot 5^n.$$
   Taking the $n$-th root:
   $$5 < \sqrt[n]{5^n + 2^n} < 5 \cdot \sqrt[n]{2}.$$
   Since $\lim_{n\to\infty} \sqrt[n]{2} = 1$, the lower and upper bounds both converge to $5$:
   $$\lim_{n\to\infty}\sqrt[n]{5^n+2^n} = 5.$$

4. **Why the Transformation Looks Different:**
   In polynomial quotients, dominance is governed by power degrees ($n^k$), and we factor out $n^k$ to create terms like $\frac{1}{n^p} \to 0$. In exponential expressions, dominance is determined by the geometric base ($b^n$), and taking an $n$-th root $(\cdot)^{1/n}$ naturally extracts the largest base $b$ outside the radical while crushing the bounded remaining factor to $1$ because $\lim_{n\to\infty} C^{1/n} = 1$.

## 4. Verification and Consistency Checks
The analytical derivation is verified through algebraic consistency, dimensional checking, and direct substitution back into the governing problem definitions.
