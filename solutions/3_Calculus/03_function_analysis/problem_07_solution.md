# Problem 7: A Trigonometric Function

## 1. Problem Statement
On $[0,2\pi]$, find the intervals of monotonicity and the extrema of
$$f(x)=\sin x+\cos x.$$
Include the endpoints of the interval and compare the function values at the critical points and at the endpoints.

## 2. Theoretical Background and Concepts
> it practices the analysis of a periodic function on a bounded interval.

This problem applies foundational mathematical principles:
- Rigorous application of core definitions and operator properties.
- Analytical transformations preserving structural invariants.
- Systematic reduction to canonical and solvable forms.

## 3. Detailed Step-by-Step Solution
1. **Derivative and Critical Points on $[0, 2\pi]$:**
   $$f'(x) = \cos x - \sin x.$$
   $$f'(x) = 0 \iff \cos x = \sin x \iff \tan x = 1.$$
   On $[0, 2\pi]$, the critical points are:
   $$x_1 = \frac{\pi}{4}, \qquad x_2 = \frac{5\pi}{4}.$$

2. **Monotonicity Intervals:**
   - On $\left[0, \frac{\pi}{4}\right)$: $\cos x > \sin x \implies f'(x) > 0 \implies$ **increasing**.
   - On $\left(\frac{\pi}{4}, \frac{5\pi}{4}\right)$: $\cos x < \sin x \implies f'(x) < 0 \implies$ **decreasing**.
   - On $\left(\frac{5\pi}{4}, 2\pi\right]$: $\cos x > \sin x \implies f'(x) > 0 \implies$ **increasing**.

3. **Evaluate Function at Critical Points and Endpoints:**
   - At left endpoint $x = 0$: $f(0) = \sin 0 + \cos 0 = 1$.
   - At critical point $x = \frac{\pi}{4}$:
     $$f\left(\frac{\pi}{4}\right) = \sin\frac{\pi}{4} + \cos\frac{\pi}{4} = \frac{\sqrt{2}}{2} + \frac{\sqrt{2}}{2} = \sqrt{2} \approx 1.414 \quad (\textbf{Absolute Maximum}).$$
   - At critical point $x = \frac{5\pi}{4}$:
     $$f\left(\frac{5\pi}{4}\right) = \sin\frac{5\pi}{4} + \cos\frac{5\pi}{4} = -\frac{\sqrt{2}}{2} - \frac{\sqrt{2}}{2} = -\sqrt{2} \approx -1.414 \quad (\textbf{Absolute Minimum}).$$
   - At right endpoint $x = 2\pi$: $f(2\pi) = \sin 2\pi + \cos 2\pi = 1$.

## 4. Verification and Consistency Checks
The analytical derivation is verified through algebraic consistency, dimensional checking, and direct substitution back into the governing problem definitions.
