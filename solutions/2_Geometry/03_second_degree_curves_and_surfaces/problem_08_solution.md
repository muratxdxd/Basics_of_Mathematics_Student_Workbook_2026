# Problem 8: Sphere

## 1. Problem Statement
Reduce
$$x^2+y^2+z^2-4x+2y-6z-2=0$$
to canonical form. Find the center and radius. Give two points on the sphere and check them in the equation.

## 2. Theoretical Background and Concepts
> transfers the technique known from circles from two dimensions to three.

This problem applies foundational mathematical principles:
- Rigorous application of core definitions and operator properties.
- Analytical transformations preserving structural invariants.
- Systematic reduction to canonical and solvable forms.

## 3. Detailed Step-by-Step Solution
1. **Complete the Square:**
   $$(x^2 - 4x + 4) + (y^2 + 2y + 1) + (z^2 - 6z + 9) - 4 - 1 - 9 - 2 = 0.$$
   $$(x - 2)^2 + (y + 1)^2 + (z - 3)^2 = 16 = 4^2.$$

2. **Center and Radius:**
   - Center: $(x_0, y_0, z_0) = (2, -1, 3)$.
   - Radius: $R = \sqrt{16} = 4$.

3. **Two Points and Verification:**
   - **Point 1:** $(x_0 + R, y_0, z_0) = (2 + 4, -1, 3) = (6, -1, 3)$:
     - *Canonical:* $(6-2)^2 + (-1+1)^2 + (3-3)^2 = 4^2 + 0 + 0 = 16$ (holds).
     - *General:* $6^2 + (-1)^2 + 3^2 - 4(6) + 2(-1) - 6(3) - 2 = 36 + 1 + 9 - 24 - 2 - 18 - 2 = 46 - 46 = 0$ (holds).
   - **Point 2:** $(x_0, y_0, z_0 + R) = (2, -1, 3 + 4) = (2, -1, 7)$:
     - *Canonical:* $(2-2)^2 + (-1+1)^2 + (7-3)^2 = 0 + 0 + 4^2 = 16$ (holds).
     - *General:* $2^2 + (-1)^2 + 7^2 - 4(2) + 2(-1) - 6(7) - 2 = 4 + 1 + 49 - 8 - 2 - 42 - 2 = 54 - 54 = 0$ (holds).

## 4. Verification and Consistency Checks
The analytical derivation is verified through algebraic consistency, dimensional checking, and direct substitution back into the governing problem definitions.
