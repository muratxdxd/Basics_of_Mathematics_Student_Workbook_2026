# Problem 10: A Polynomial Through Three Points

## 1. Problem Statement
Find a polynomial $p(x)=ax^2+bx+c$ whose graph passes through $(0,1)$, $(1,3)$, and $(2,9)$. Reduce the problem to a system of equations and check the result by substituting all three points.

## 2. Theoretical Background and Concepts
> shows that finding unknown coefficients can be reduced to solving a linear system.

This problem applies foundational mathematical principles:
- Rigorous application of core definitions and operator properties.
- Analytical transformations preserving structural invariants.
- Systematic reduction to canonical and solvable forms.

## 3. Detailed Step-by-Step Solution
1. **Set Up the System:**
   Substitute each point $(x, y)$ into $p(x) = ax^2 + bx + c$:
   - For $(0, 1)$: $a(0)^2 + b(0) + c = 1 \implies c = 1$.
   - For $(1, 3)$: $a(1)^2 + b(1) + 1 = 3 \implies a + b = 2$.
   - For $(2, 9)$: $a(2)^2 + b(2) + 1 = 9 \implies 4a + 2b = 8 \iff 2a + b = 4$.

2. **Solve the System:**
   Subtract $(a+b=2)$ from $(2a+b=4)$:
   $$(2a + b) - (a + b) = 4 - 2 \implies a = 2.$$
   Then $b = 2 - a = 2 - 2 = 0$.
   The polynomial is:
   $$p(x) = 2x^2 + 1.$$

## 4. Verification and Consistency Checks
3. **Verification:**
   - $p(0) = 2(0)^2 + 1 = 1$ (matches $(0,1)$).
   - $p(1) = 2(1)^2 + 1 = 3$ (matches $(1,3)$).
   - $p(2) = 2(2)^2 + 1 = 2(4) + 1 = 9$ (matches $(2,9)$).
   All three points lie on the graph of $p(x)$.

## More Challenging Exercises
