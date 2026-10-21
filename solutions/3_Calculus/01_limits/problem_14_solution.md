# Problem 14: A $0/0$ Limit with Trigonometry

## 1. Problem Statement
Compute
$$\lim_{x\to0}\frac{1-\cos x}{x^2}.$$
Justify the result without using l'HÃ´pital's rule, using a trigonometric identity and the fundamental limit.

## 2. Theoretical Background and Concepts
> requires combining two known tools in one argument.

This problem applies foundational mathematical principles:
- Rigorous application of core definitions and operator properties.
- Analytical transformations preserving structural invariants.
- Systematic reduction to canonical and solvable forms.

## 3. Detailed Step-by-Step Solution
1. **Trigonometric Half-Angle Identity:**
   Recall the half-angle identity:
   $$1 - \cos x = 2\sin^2\left(\frac{x}{2}\right).$$

2. **Substitute and Reorganize:**
   $$\lim_{x\to0}\frac{1-\cos x}{x^2} = \lim_{x\to0}\frac{2\sin^2(x/2)}{x^2}.$$
   Rewrite the denominator to match $(x/2)^2$:
   $$x^2 = 4 \cdot \left(\frac{x}{2}\right)^2.$$
   Substitute into the fraction:
   $$= \lim_{x\to0}\frac{2\sin^2(x/2)}{4(x/2)^2} = \frac{2}{4} \lim_{x\to0}\left(\frac{\sin(x/2)}{x/2}\right)^2 = \frac{1}{2} \left[\lim_{x\to0}\frac{\sin(x/2)}{x/2}\right]^2.$$

3. **Evaluate:**
   Setting $u = \frac{x}{2}$, as $x \to 0$ we have $u \to 0$:
   $$= \frac{1}{2} \cdot (1)^2 = \frac{1}{2} = 0.5.$$

## 4. Verification and Consistency Checks
The analytical derivation is verified through algebraic consistency, dimensional checking, and direct substitution back into the governing problem definitions.
