# Problem 5: Angle Between Vectors

## 1. Problem Statement
Given $u=(1,1,0)$ and $v=(1,0,1)$:

1. Use the sign of $u\cdot v$ to predict the type of angle.
2. Compute the angle.
3. Compare the result with the prediction.

## 2. Theoretical Background and Concepts
> teaches how to extract qualitative information first and only then perform the exact calculation.

This problem applies foundational mathematical principles:
- Rigorous application of core definitions and operator properties.
- Analytical transformations preserving structural invariants.
- Systematic reduction to canonical and solvable forms.

## 3. Detailed Step-by-Step Solution
1. **Predict Type of Angle from Sign of $u \cdot v$:**
   $$u \cdot v = 1(1) + 1(0) + 0(1) = 1.$$
   Since $u \cdot v > 0$, $\cos\theta = \frac{u \cdot v}{\|u\|\|v\|} > 0$. Therefore, the angle $\theta$ must be **acute** ($0^\circ \le \theta < 90^\circ$).

2. **Compute the Exact Angle:**
   $$\|u\| = \sqrt{1^2 + 1^2 + 0^2} = \sqrt{2}, \qquad \|v\| = \sqrt{1^2 + 0^2 + 1^2} = \sqrt{2}.$$
   $$\cos\theta = \frac{u \cdot v}{\|u\|\|v\|} = \frac{1}{\sqrt{2}\sqrt{2}} = \frac{1}{2}.$$
   $$\theta = \arccos\left(\frac{1}{2}\right) = 60^\circ = \frac{\pi}{3}\text{ rad}.$$

3. **Comparison:**
   The angle $60^\circ$ is strictly between $0^\circ$ and $90^\circ$, matching the acute angle prediction.

## 4. Verification and Consistency Checks
The analytical derivation is verified through algebraic consistency, dimensional checking, and direct substitution back into the governing problem definitions.
