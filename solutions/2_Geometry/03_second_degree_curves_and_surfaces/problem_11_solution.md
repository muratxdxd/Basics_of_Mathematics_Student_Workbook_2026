# Problem 11: Two Similar Surfaces

## 1. Problem Statement
Compare
$$x^2+y^2-z^2=1$$
and
$$x^2+y^2-z^2=-1.$$
For several values $z=c$, check whether the cross-section exists and what its radius is. Based on this, describe qualitatively the difference between the surfaces and make sketches.

## 2. Theoretical Background and Concepts
> teaches how to recognize the shape of a surface from cross-sections instead of from a memorized catalog of names.

This problem applies foundational mathematical principles:
- Rigorous application of core definitions and operator properties.
- Analytical transformations preserving structural invariants.
- Systematic reduction to canonical and solvable forms.

## 3. Detailed Step-by-Step Solution
1. **Surface 1: $x^2 + y^2 - z^2 = 1 \iff x^2 + y^2 = 1 + z^2$ (Hyperboloid of One Sheet):**
   - For $z = 0$: $x^2 + y^2 = 1$, circle of radius $R = 1$.
   - For $z = \pm 1$: $x^2 + y^2 = 2$, circle of radius $R = \sqrt{2} \approx 1.414$.
   - For $z = \pm 2$: $x^2 + y^2 = 5$, circle of radius $R = \sqrt{5} \approx 2.236$.
   - For any $z = c \in \mathbb{R}$: $1 + c^2 \ge 1 > 0$, so cross-sections are **always non-empty circles** of radius $R(c) = \sqrt{1 + c^2}$.
   - **Qualitative shape:** A single, unbroken, connected tube with a narrow "waist" of radius $1$ at the equator $z = 0$, flaring outward as $|z| \to \infty$.

2. **Surface 2: $x^2 + y^2 - z^2 = -1 \iff x^2 + y^2 = z^2 - 1$ (Hyperboloid of Two Sheets):**
   - For $z = 0$: $x^2 + y^2 = -1 \implies$ **no real cross-section**.
   - For $|z| < 1$: $z^2 - 1 < 0 \implies$ no real points exist in the slab $-1 < z < 1$.
   - For $z = \pm 1$: $x^2 + y^2 = 0 \implies$ two isolated vertex points $(0, 0, 1)$ and $(0, 0, -1)$.
   - For $z = \pm 2$: $x^2 + y^2 = 3$, circle of radius $R = \sqrt{3} \approx 1.732$.
   - **Qualitative shape:** Two disconnected, separate sheets (an upper bowl for $z \ge 1$ opening upward, and a lower bowl for $z \le -1$ opening downward), separated by an empty gap of height $2$.

## 4. Verification and Consistency Checks
The analytical derivation is verified through algebraic consistency, dimensional checking, and direct substitution back into the governing problem definitions.
