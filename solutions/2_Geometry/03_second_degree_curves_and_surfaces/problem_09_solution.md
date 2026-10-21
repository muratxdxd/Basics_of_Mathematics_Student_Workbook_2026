# Problem 9: Ellipsoid and Its Cross-Sections

## 1. Problem Statement
Consider
$$\frac{x^2}{9}+\frac{y^2}{4}+\frac{z^2}{16}=1.$$
Give the semiaxis lengths, describe the cross-section $z=0$, and explain how the cross-sections $z=c$ change for $|c|<4$.

## 2. Theoretical Background and Concepts
> teaches how to understand a 3D surface through a family of simpler 2D cross-sections.

This problem applies foundational mathematical principles:
- Rigorous application of core definitions and operator properties.
- Analytical transformations preserving structural invariants.
- Systematic reduction to canonical and solvable forms.

## 3. Detailed Step-by-Step Solution
1. **Semiaxis Lengths:**
   - Along $x$: $a = \sqrt{9} = 3$.
   - Along $y$: $b = \sqrt{4} = 2$.
   - Along $z$: $c_0 = \sqrt{16} = 4$.

2. **Cross-Section $z = 0$ (the $xy$-plane):**
   $$\frac{x^2}{9} + \frac{y^2}{4} = 1.$$
   This is an **ellipse** in the $xy$-plane with semiaxes $3$ and $2$.

3. **Cross-Sections $z = c$ for $|c| < 4$:**
   $$\frac{x^2}{9} + \frac{y^2}{4} = 1 - \frac{c^2}{16}.$$
   Since $|c| < 4$, the factor $k^2 = 1 - \frac{c^2}{16}$ is strictly positive ($0 < k^2 \le 1$).
   Dividing through by $k^2$:
   $$\frac{x^2}{9k^2} + \frac{y^2}{4k^2} = 1.$$
   Each cross-section is an ellipse with semiaxes $a(c) = 3\sqrt{1 - \frac{c^2}{16}}$ and $b(c) = 2\sqrt{1 - \frac{c^2}{16}}$.
   - At $c = 0$, the cross-sectional ellipse has maximum area.
   - As $|c|$ increases towards $4$, the semiaxes shrink continuously.
   - At $|c| = 4$, the semiaxes become $0$, reducing the ellipse to a single point $(0, 0, \pm 4)$ (the north and south poles).
   - For $|c| > 4$, the RHS is negative, so there are no real points.

## 4. Verification and Consistency Checks
The analytical derivation is verified through algebraic consistency, dimensional checking, and direct substitution back into the governing problem definitions.
