# Problem 10: Continuity of a Piecewise Function

## 1. Problem Statement
Find $a$ so that
$$f(x)=\begin{cases}ax+1,&x<2,\\x^2-1,&x\ge2\end{cases}$$
is continuous at $x=2$. Explicitly compare the left-hand limit, right-hand limit, and function value.

## 2. Theoretical Background and Concepts
> organizes the definition of continuity as agreement among three quantities.

This problem applies foundational mathematical principles:
- Rigorous application of core definitions and operator properties.
- Analytical transformations preserving structural invariants.
- Systematic reduction to canonical and solvable forms.

## 3. Detailed Step-by-Step Solution
1. **Definition of Continuity:**
   A function $f$ is continuous at $x = c$ if and only if:
   $$\lim_{x\to c^-} f(x) = \lim_{x\to c^+} f(x) = f(c).$$

2. **Evaluate the Three Quantities at $x = 2$:**
   - **Left-hand limit:**
     $$\lim_{x\to2^-} f(x) = \lim_{x\to2^-}(ax + 1) = a(2) + 1 = 2a + 1.$$
   - **Right-hand limit:**
     $$\lim_{x\to2^+} f(x) = \lim_{x\to2^+}(x^2 - 1) = 2^2 - 1 = 4 - 1 = 3.$$
   - **Function value:**
     $$f(2) = 2^2 - 1 = 3.$$

3. **Solve for $a$:**
   Equating the left-hand limit to the right-hand limit and function value:
   $$2a + 1 = 3 \implies 2a = 2 \implies a = 1.$$
   For $a = 1$, the two pieces meet seamlessly at the point $(2, 3)$, making $f(x)$ continuous on all of $\mathbb{R}$.

## More Challenging Exercises

## 4. Verification and Consistency Checks
The analytical derivation is verified through algebraic consistency, dimensional checking, and direct substitution back into the governing problem definitions.
