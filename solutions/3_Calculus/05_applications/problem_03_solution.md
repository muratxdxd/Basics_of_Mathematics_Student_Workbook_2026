# Problem 3: A Box Made from Cardboard

## 1. Problem Statement
From a $30\text{ cm}\times40\text{ cm}$ sheet, squares of side length $x$ are cut from the corners and the edges are folded up to form an open box.

Write the volume as a function of $x$, determine the physically meaningful domain, and find the value of $x$ for which the volume is greatest.

## 2. Theoretical Background and Concepts
> it develops optimization modeling in a situation where the objective function is not given and must be built independently from the geometry.

This problem applies foundational mathematical principles:
- Rigorous application of core definitions and operator properties.
- Analytical transformations preserving structural invariants.
- Systematic reduction to canonical and solvable forms.

## 3. Detailed Step-by-Step Solution
1. **Volume Function:**
   Cutting squares of side $x$ from each corner and folding creates a box with:
   - Height: $h = x$
   - Width: $w = 30 - 2x$
   - Length: $l = 40 - 2x$
   $$V(x) = x(30 - 2x)(40 - 2x) = x(1200 - 140x + 4x^2) = 4x^3 - 140x^2 + 1200x.$$

2. **Domain:**
   All physical dimensions must be strictly positive:
   $$x > 0, \qquad 30 - 2x > 0 \implies x < 15, \qquad 40 - 2x > 0 \implies x < 20.$$
   Intersecting these conditions yields:
   $$D_V = (0, 15).$$

3. **Find Maximum Volume:**
   $$V'(x) = 12x^2 - 280x + 1200 = 4(3x^2 - 70x + 300) = 0.$$
   Solve the quadratic equation $3x^2 - 70x + 300 = 0$:
   $$\Delta = (-70)^2 - 4(3)(300) = 4900 - 3600 = 1300.$$
   $$\sqrt{\Delta} = 10\sqrt{13} \approx 36.0555.$$
   $$x = \frac{70 \pm 10\sqrt{13}}{2(3)} = \frac{35 \pm 5\sqrt{13}}{3}.$$
   - Candidate 1: $x_1 = \frac{35 - 5\sqrt{13}}{3} \approx \frac{35 - 18.028}{3} \approx 5.657\text{ cm} \in (0, 15)$.
   - Candidate 2: $x_2 = \frac{35 + 5\sqrt{13}}{3} \approx \frac{35 + 18.028}{3} \approx 17.676\text{ cm} \notin (0, 15)$.
   Check second derivative at $x_1$:
   $$V''(x) = 24x - 280 \implies V''(5.657) \approx 24(5.657) - 280 = 135.77 - 280 = -144.23 < 0.$$
   The maximum volume occurs at $x = \frac{35 - 5\sqrt{13}}{3} \approx 5.66\text{ cm}$, yielding volume $V \approx 3032.3\text{ cm}^3$.

## 4. Verification and Consistency Checks
The analytical derivation is verified through algebraic consistency, dimensional checking, and direct substitution back into the governing problem definitions.
