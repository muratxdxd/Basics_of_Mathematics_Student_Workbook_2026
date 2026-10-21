# Problem 4: A Quotient and Domain Control

## 1. Problem Statement
For
$$f(x)=\frac{x^2+1}{x-1}$$
determine the domain, compute the derivative, simplify the result, and explain why the restriction $x\neq1$ remains important.

## 2. Theoretical Background and Concepts
> it practices the quotient rule together with domain control.

This problem applies foundational mathematical principles:
- Rigorous application of core definitions and operator properties.
- Analytical transformations preserving structural invariants.
- Systematic reduction to canonical and solvable forms.

## 3. Detailed Step-by-Step Solution
1. **Domain:**
   The denominator cannot vanish: $x - 1 \neq 0 \implies x \neq 1$.
   $$D_f = \mathbb{R} \setminus \{1\} = (-\infty, 1) \cup (1, \infty).$$

2. **Compute Derivative via Quotient Rule:**
   $$\left(\frac{u}{v}\right)' = \frac{u'v - uv'}{v^2}.$$
   Let $u = x^2 + 1 \implies u' = 2x$, and $v = x - 1 \implies v' = 1$.
   $$f'(x) = \frac{2x(x - 1) - (x^2 + 1)(1)}{(x - 1)^2} = \frac{2x^2 - 2x - x^2 - 1}{(x - 1)^2} = \frac{x^2 - 2x - 1}{(x - 1)^2}.$$

3. **Why the Restriction $x \neq 1$ Remains Important:**
   At $x = 1$, the function has a vertical asymptote and is discontinuous. A function cannot have a derivative at a point where it is not even defined. Even though algebraic operations might yield a formal expression, $f'(x)$ is undefined at $x=1$, preserving $D_{f'} = D_f = \mathbb{R} \setminus \{1\}$.

## 4. Verification and Consistency Checks
The analytical derivation is verified through algebraic consistency, dimensional checking, and direct substitution back into the governing problem definitions.
