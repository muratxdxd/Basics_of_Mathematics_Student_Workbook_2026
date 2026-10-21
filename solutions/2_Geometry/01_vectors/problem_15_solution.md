# Problem 15: Comparing Directions Using the Cosine of the Angle

## 1. Problem Statement
Given
$$a=(1,2,1),\qquad b=(2,4,2),\qquad c=(2,0,3).$$
For each pair, compute
$$\frac{u\cdot v}{\|u\|\,\|v\|}.$$
Order the pairs by increasing angle between the vectors. Explain why for $a$ and $b$ the value is $1$ even though the vectors have different lengths.

## 2. Theoretical Background and Concepts
> reinforces the connection between the dot product and angle, and the distinction between direction and length.

This problem applies foundational mathematical principles:
- Rigorous application of core definitions and operator properties.
- Analytical transformations preserving structural invariants.
- Systematic reduction to canonical and solvable forms.

## 3. Detailed Step-by-Step Solution
1. **Magnitudes:**
   $$\|a\| = \sqrt{1^2 + 2^2 + 1^2} = \sqrt{6}.$$
   $$\|b\| = \sqrt{2^2 + 4^2 + 2^2} = \sqrt{4 + 16 + 4} = \sqrt{24} = 2\sqrt{6}.$$
   $$\|c\| = \sqrt{2^2 + 0^2 + 3^2} = \sqrt{4 + 9} = \sqrt{13}.$$

2. **Cosine Calculations:**
   - **Pair $(a, b)$:**
     $$a \cdot b = 1(2) + 2(4) + 1(2) = 12.$$
     $$\cos\theta_{ab} = \frac{12}{\sqrt{6} \cdot 2\sqrt{6}} = \frac{12}{2 \cdot 6} = \frac{12}{12} = 1 \implies \theta_{ab} = 0^\circ.$$
   - **Pair $(a, c)$:**
     $$a \cdot c = 1(2) + 2(0) + 1(3) = 2 + 0 + 3 = 5.$$
     $$\cos\theta_{ac} = \frac{5}{\sqrt{6}\sqrt{13}} = \frac{5}{\sqrt{78}} \approx 0.5661 \implies \theta_{ac} \approx 55.52^\circ.$$
   - **Pair $(b, c)$:**
     $$b \cdot c = 2(2) + 4(0) + 2(3) = 4 + 0 + 6 = 10.$$
     $$\cos\theta_{bc} = \frac{10}{2\sqrt{6}\sqrt{13}} = \frac{10}{2\sqrt{78}} = \frac{5}{\sqrt{78}} \approx 0.5661 \implies \theta_{bc} \approx 55.52^\circ.$$

3. **Ordering by Increasing Angle:**
   $$\theta_{ab} = 0^\circ < \theta_{ac} = \theta_{bc} \approx 55.52^\circ.$$
   Order: Pair $(a, b)$, followed by pairs $(a, c)$ and $(b, c)$.

4. **Why $\cos = 1$ for $a$ and $b$:**
   Notice $b = (2, 4, 2) = 2(1, 2, 1) = 2a$. Vector $b$ is a positive scalar multiple of $a$, meaning both vectors lie along the same line pointing in the exact same orientation. The cosine formula normalizes by the vector lengths ($\|b\| = 2\|a\|$), so the length factor of 2 cancels out entirely ($\frac{2\|a\|^2}{2\|a\|^2} = 1$). The cosine measures directional alignment, which is independent of magnitude.

## 4. Verification and Consistency Checks
The analytical derivation is verified through algebraic consistency, dimensional checking, and direct substitution back into the governing problem definitions.
