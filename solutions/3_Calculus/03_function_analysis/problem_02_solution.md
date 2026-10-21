# Problem 2: A Parabola from the Perspective of the Derivative

## 1. Problem Statement
For $f(x)=x^2-4x+1$, find the minimum using the derivative. Compare the result with the vertex form and explain why both approaches lead to the same point.

## 2. Theoretical Background and Concepts
> it connects a new tool with the familiar geometry of a parabola.

This problem applies foundational mathematical principles:
- Rigorous application of core definitions and operator properties.
- Analytical transformations preserving structural invariants.
- Systematic reduction to canonical and solvable forms.

## 3. Detailed Step-by-Step Solution
1. **Derivative Method:**
   $$f'(x) = 2x - 4.$$
   Setting $f'(x) = 0 \implies 2x = 4 \implies x = 2$.
   Second derivative: $f''(x) = 2 > 0$, confirming a local and global minimum.
   $$f(2) = 2^2 - 4(2) + 1 = 4 - 8 + 1 = -3.$$
   Minimum point: $(2, -3)$.

2. **Vertex Form Method:**
   Complete the square:
   $$f(x) = (x^2 - 4x + 4) - 4 + 1 = (x - 2)^2 - 3.$$
   Since $(x - 2)^2 \ge 0$ for all real $x$, the minimum value $-3$ is attained when $(x - 2)^2 = 0 \iff x = 2$.
   Vertex: $(2, -3)$.

3. **Why Both Approaches Agree:**
   The vertex of an upward-opening parabola is its turning point where the slope of the curve transitions from negative to positive. At this exact turning point, the tangent line is horizontal ($f'(x) = 0$). Differentiating identifies the location of zero slope, which is identical to setting the squared term in vertex form to zero.

## 4. Verification and Consistency Checks
The analytical derivation is verified through algebraic consistency, dimensional checking, and direct substitution back into the governing problem definitions.
