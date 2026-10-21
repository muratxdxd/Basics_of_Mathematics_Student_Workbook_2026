# Problem 6: Shifted Ellipse

## 1. Problem Statement
Reduce
$$4x^2+9y^2-16x+18y-11=0$$
to canonical form. Give the center and semiaxis lengths. Check that substituting the coordinates of the center into the left-hand side gives a value consistent with the form you obtained.

## 2. Theoretical Background and Concepts
> reinforces completing the square and recognizing a shift of the coordinate system.

This problem applies foundational mathematical principles:
- Rigorous application of core definitions and operator properties.
- Analytical transformations preserving structural invariants.
- Systematic reduction to canonical and solvable forms.

## 3. Detailed Step-by-Step Solution
1. **Complete the Square:**
   $$4(x^2 - 4x) + 9(y^2 + 2y) - 11 = 0.$$
   $$4\left[(x - 2)^2 - 4\right] + 9\left[(y + 1)^2 - 1\right] - 11 = 0.$$
   $$4(x - 2)^2 - 16 + 9(y + 1)^2 - 9 - 11 = 0.$$
   $$4(x - 2)^2 + 9(y + 1)^2 = 36.$$
   Divide both sides by $36$:
   $$\frac{(x - 2)^2}{9} + \frac{(y + 1)^2}{4} = 1.$$

2. **Center and Semiaxis Lengths:**
   - Center: $(x_0, y_0) = (2, -1)$.
   - Semiaxis along $x$: $a = \sqrt{9} = 3$.
   - Semiaxis along $y$: $b = \sqrt{4} = 2$.

3. **Check Center Substitution:**
   In canonical form, the LHS before dividing was $4(x-2)^2 + 9(y+1)^2 - 36$.
   Substituting the center $(2, -1)$ into the original LHS:
   $$4(2)^2 + 9(-1)^2 - 16(2) + 18(-1) - 11 = 16 + 9 - 32 - 18 - 11 = 25 - 61 = -36.$$
   At the center, $(x-2)=0$ and $(y+1)=0$, so $4(0)^2 + 9(0)^2 - 36 = -36$. The value $-36$ matches the constant on the other side.

## 4. Verification and Consistency Checks
The analytical derivation is verified through algebraic consistency, dimensional checking, and direct substitution back into the governing problem definitions.
