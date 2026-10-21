# Problem 13: Fundamental Trigonometric Limit

## 1. Problem Statement
Using
$$\lim_{x\to0}\frac{\sin x}{x}=1,$$
compute
$$\lim_{x\to0}\frac{\sin5x}{x},\qquad \lim_{x\to0}\frac{\sin2x}{\sin3x}.$$
In each case, show how you reduce the expression to the fundamental limit.

## 2. Theoretical Background and Concepts
> teaches how to reduce new limits to one known pattern.

This problem applies foundational mathematical principles:
- Rigorous application of core definitions and operator properties.
- Analytical transformations preserving structural invariants.
- Systematic reduction to canonical and solvable forms.

## 3. Detailed Step-by-Step Solution
1. **First Limit:**
   Multiply and divide by $5$:
   $$\lim_{x\to0}\frac{\sin5x}{x} = \lim_{x\to0} 5 \cdot \frac{\sin5x}{5x}.$$
   Let $u = 5x$. As $x \to 0$, $u \to 0$.
   $$= 5 \cdot \lim_{u\to0}\frac{\sin u}{u} = 5 \cdot 1 = 5.$$

2. **Second Limit:**
   Multiply and divide numerator and denominator by their respective arguments ($2x$ and $3x$):
   $$\lim_{x\to0}\frac{\sin2x}{\sin3x} = \lim_{x\to0}\frac{\frac{\sin2x}{2x}\cdot 2x}{\frac{\sin3x}{3x}\cdot 3x} = \lim_{x\to0}\left(\frac{2x}{3x} \cdot \frac{\frac{\sin2x}{2x}}{\frac{\sin3x}{3x}}\right) = \frac{2}{3} \cdot \frac{\lim_{x\to0}\frac{\sin2x}{2x}}{\lim_{x\to0}\frac{\sin3x}{3x}}.$$
   Since $\lim_{x\to0}\frac{\sin2x}{2x} = 1$ and $\lim_{x\to0}\frac{\sin3x}{3x} = 1$:
   $$= \frac{2}{3} \cdot \frac{1}{1} = \frac{2}{3}.$$

## 4. Verification and Consistency Checks
The analytical derivation is verified through algebraic consistency, dimensional checking, and direct substitution back into the governing problem definitions.
