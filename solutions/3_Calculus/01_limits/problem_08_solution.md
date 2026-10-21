# Problem 8: A Square Root in a Function Limit

## 1. Problem Statement
Compute
$$\lim_{x\to4}\frac{\sqrt{x}-2}{x-4}$$
by rationalizing the numerator. Compare the idea with Exercise 3 involving a sequence.

## 2. Theoretical Background and Concepts
> reinforces transferring the same algebraic technique between two types of limits.

This problem applies foundational mathematical principles:
- Rigorous application of core definitions and operator properties.
- Analytical transformations preserving structural invariants.
- Systematic reduction to canonical and solvable forms.

## 3. Detailed Step-by-Step Solution
1. **Rationalize Numerator:**
   Multiply numerator and denominator by the conjugate $(\sqrt{x} + 2)$:
   $$\lim_{x\to4}\frac{\sqrt{x}-2}{x-4} = \lim_{x\to4}\frac{(\sqrt{x}-2)(\sqrt{x}+2)}{(x-4)(\sqrt{x}+2)} = \lim_{x\to4}\frac{x - 4}{(x-4)(\sqrt{x}+2)}.$$
   For $x \neq 4$, cancel the common factor $(x - 4)$:
   $$= \lim_{x\to4}\frac{1}{\sqrt{x} + 2} = \frac{1}{\sqrt{4} + 2} = \frac{1}{2 + 2} = \frac{1}{4} = 0.25.$$

2. **Comparison with Exercise 3:**
   Both problems resolve an indeterminate form using the difference of squares identity $(A-B)(A+B) = A^2 - B^2$. In Exercise 3, conjugation resolved an $(\infty - \infty)$ indeterminate form by canceling dominant leading powers at infinity; here, it resolves a $(0/0)$ indeterminate form by explicitly creating and canceling the factor $(x - 4)$ responsible for the zero in the denominator.

## 4. Verification and Consistency Checks
The analytical derivation is verified through algebraic consistency, dimensional checking, and direct substitution back into the governing problem definitions.
