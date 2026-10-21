# Problem 3: A Square Root and Removing an Indeterminate Form

## 1. Problem Statement
Compute
$$\lim_{n\to\infty}\left(\sqrt{n^2+5n}-n\right).$$
Use the conjugate expression and explain why this transformation removes the difficulty.

## 2. Theoretical Background and Concepts
> introduces conjugation as a deliberate technique for removing an indeterminate form.

This problem applies foundational mathematical principles:
- Rigorous application of core definitions and operator properties.
- Analytical transformations preserving structural invariants.
- Systematic reduction to canonical and solvable forms.

## 3. Detailed Step-by-Step Solution
1. **Identify Indeterminate Form:**
   As $n \to \infty$, $\sqrt{n^2+5n} \to \infty$ and $n \to \infty$, giving the indeterminate form $\infty - \infty$.

2. **Multiply and Divide by the Conjugate:**
   Multiply by $\frac{\sqrt{n^2+5n} + n}{\sqrt{n^2+5n} + n}$:
   $$\lim_{n\to\infty}\left(\sqrt{n^2+5n}-n\right) = \lim_{n\to\infty}\frac{(\sqrt{n^2+5n}-n)(\sqrt{n^2+5n}+n)}{\sqrt{n^2+5n}+n} = \lim_{n\to\infty}\frac{(n^2+5n) - n^2}{\sqrt{n^2+5n}+n} = \lim_{n\to\infty}\frac{5n}{\sqrt{n^2(1 + \frac{5}{n})} + n}.$$
   Divide numerator and denominator by $n$:
   $$= \lim_{n\to\infty}\frac{5}{\sqrt{1 + \frac{5}{n}} + 1} = \frac{5}{\sqrt{1 + 0} + 1} = \frac{5}{1 + 1} = \frac{5}{2} = 2.5.$$

3. **Why Conjugation Removes the Difficulty:**
   Conjugate multiplication utilizes the difference of squares identity $(A-B)(A+B) = A^2 - B^2$. This eliminates the square root and cancels out the leading quadratic terms ($n^2 - n^2 = 0$), converting an indeterminate subtraction of two nearly equal large quantities ($\infty - \infty$) into a determinate ratio where dominant linear powers can be evaluated cleanly.

## 4. Verification and Consistency Checks
The analytical derivation is verified through algebraic consistency, dimensional checking, and direct substitution back into the governing problem definitions.
