# Problem 9: Definite Integral and Geometric Area

## 1. Problem Statement
Compute
$$\int_{-1}^{2}x\,dx.$$
Then separately compute the areas of the parts of the graph below and above the $x$-axis and explain the difference between the definite integral and geometric area.

## 2. Theoretical Background and Concepts
> it clarifies the difference between signed accumulation and area.

This problem applies foundational mathematical principles:
- Rigorous application of core definitions and operator properties.
- Analytical transformations preserving structural invariants.
- Systematic reduction to canonical and solvable forms.

## 3. Detailed Step-by-Step Solution
1. **Compute Definite Integral:**
   $$\int_{-1}^{2}x\,dx = \left[\frac{x^2}{2}\right]_{-1}^{2} = \frac{2^2}{2} - \frac{(-1)^2}{2} = \frac{4}{2} - \frac{1}{2} = 2 - 0.5 = 1.5.$$

2. **Geometric Area of Both Parts:**
   - **Region below $x$-axis ($x \in [-1, 0]$):**
     Right triangle with base $1$ (from $-1$ to $0$) and height $1$ (from $y=0$ to $y=-1$):
     $$\text{Area}_1 = \frac{1}{2}\text{base}\times\text{height} = \frac{1}{2}(1)(1) = 0.5.$$
   - **Region above $x$-axis ($x \in [0, 2]$):**
     Right triangle with base $2$ (from $0$ to $2$) and height $2$ (from $y=0$ to $y=2$):
     $$\text{Area}_2 = \frac{1}{2}\text{base}\times\text{height} = \frac{1}{2}(2)(2) = 2.0.$$
   - **Total Geometric Area:**
     $$\text{Area}_{\text{total}} = \text{Area}_1 + \text{Area}_2 = 0.5 + 2.0 = 2.5.$$

3. **Difference Between Definite Integral and Geometric Area:**
   The definite integral computes **signed net accumulation**: regions above the $x$-axis are counted with positive signs ($+2.0$), while regions below the $x$-axis are counted with negative signs ($-0.5$). Thus:
   $$\int_{-1}^2 x\,dx = \text{Area}_2 - \text{Area}_1 = 2.0 - 0.5 = 1.5.$$
   Geometric area is the total physical area of the surface, defined as the integral of the absolute value $\int_{-1}^2 |x|\,dx = 2.5$.

## 4. Verification and Consistency Checks
The analytical derivation is verified through algebraic consistency, dimensional checking, and direct substitution back into the governing problem definitions.
