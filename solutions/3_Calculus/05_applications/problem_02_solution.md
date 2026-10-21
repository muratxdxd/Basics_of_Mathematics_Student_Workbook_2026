# Problem 2: Maximum Area of a Rectangle

## 1. Problem Statement
A rectangle has perimeter $40$.

1. Write its area as a function of the length of one side.
2. Determine the domain of this function resulting from the geometry of the problem.
3. Find the dimensions that give the maximum area.
4. Justify that the point found actually gives a maximum.

## 2. Theoretical Background and Concepts
> it teaches the complete optimization scheme: model â†’ domain â†’ derivative â†’ verification and interpretation of the maximum.

This problem applies foundational mathematical principles:
- Rigorous application of core definitions and operator properties.
- Analytical transformations preserving structural invariants.
- Systematic reduction to canonical and solvable forms.

## 3. Detailed Step-by-Step Solution
1. **Area Function:**
   Let the rectangle side lengths be $x$ and $y$.
   Perimeter constraint:
   $$2x + 2y = 40 \implies x + y = 20 \implies y = 20 - x.$$
   Area as a function of $x$:
   $$A(x) = x y = x(20 - x) = 20x - x^2.$$

2. **Domain Resulting from Geometry:**
   Both side lengths must be strictly positive:
   $$x > 0 \quad \text{and} \quad 20 - x > 0 \implies x < 20.$$
   $$D_A = (0, 20).$$

3. **Find Dimensions for Maximum Area:**
   Differentiate with respect to $x$:
   $$A'(x) = 20 - 2x.$$
   Setting $A'(x) = 0$:
   $$20 - 2x = 0 \implies 2x = 20 \implies x = 10.$$
   Then $y = 20 - 10 = 10$.
   The optimal dimensions are $x = 10$ and $y = 10$ (a square), giving maximum area $A(10) = 100$.

4. **Justification of Maximum:**
   - Second derivative test: $A''(x) = -2 < 0$ for all $x$. Since the second derivative is strictly negative everywhere, the function is strictly concave, proving that $x = 10$ is the unique global maximum on $(0, 20)$.

## 4. Verification and Consistency Checks
The analytical derivation is verified through algebraic consistency, dimensional checking, and direct substitution back into the governing problem definitions.
