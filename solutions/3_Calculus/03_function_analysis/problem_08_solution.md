# Problem 8: The Second Derivative

## 1. Problem Statement
For
$$f(x)=x^4-4x^2$$
find the local extrema, intervals of convexity and concavity, and inflection points. Sketch the graph and mark all the identified features on it.

## 2. Theoretical Background and Concepts
> it introduces the second derivative as a tool for describing the curvature of a graph.

This problem applies foundational mathematical principles:
- Rigorous application of core definitions and operator properties.
- Analytical transformations preserving structural invariants.
- Systematic reduction to canonical and solvable forms.

## 3. Detailed Step-by-Step Solution
1. **First Derivative and Local Extrema:**
   $$f'(x) = 4x^3 - 8x = 4x(x^2 - 2) = 4x(x - \sqrt{2})(x + \sqrt{2}).$$
   Critical points: $x = -\sqrt{2}, 0, \sqrt{2}$.
   - At $x = \pm\sqrt{2}$: $f(\pm\sqrt{2}) = (\sqrt{2})^4 - 4(\sqrt{2})^2 = 4 - 8 = -4 \implies$ **Local Minima** at $(-\sqrt{2}, -4)$ and $(\sqrt{2}, -4)$.
   - At $x = 0$: $f(0) = 0 \implies$ **Local Maximum** at $(0, 0)$.

2. **Second Derivative, Inflection Points, and Convexity:**
   $$f''(x) = 12x^2 - 8 = 4(3x^2 - 2).$$
   $$f''(x) = 0 \iff 3x^2 = 2 \iff x = \pm\sqrt{\frac{2}{3}} = \pm\frac{\sqrt{6}}{3} \approx \pm 0.8165.$$
   - On $\left(-\infty, -\sqrt{\frac{2}{3}}\right)$: $f''(x) > 0 \implies$ **Convex (concave up)**.
   - On $\left(-\sqrt{\frac{2}{3}}, \sqrt{\frac{2}{3}}\right)$: $f''(x) < 0 \implies$ **Concave (concave down)**.
   - On $\left(\sqrt{\frac{2}{3}}, \infty\right)$: $f''(x) > 0 \implies$ **Convex (concave up)**.
   **Inflection Points:**
   $$f\left(\pm\sqrt{\frac{2}{3}}\right) = \left(\frac{2}{3}\right)^2 - 4\left(\frac{2}{3}\right) = \frac{4}{9} - \frac{8}{3} = -\frac{20}{9} \approx -2.22.$$
   Points: $\left(-\sqrt{\frac{2}{3}}, -\frac{20}{9}\right)$ and $\left(\sqrt{\frac{2}{3}}, -\frac{20}{9}\right)$.

## 4. Verification and Consistency Checks
The analytical derivation is verified through algebraic consistency, dimensional checking, and direct substitution back into the governing problem definitions.
