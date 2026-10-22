# Problem 12: Complete Model and Computer Verification

## 1. Problem Statement
A museum wants to create a rectangular exhibition room next to an existing straight wall. The side along the wall does not need to be built. The remaining three sides are to be constructed to two different standards: the two sides perpendicular to the wall cost $300\ \mathrm{PLN/m}$ each, while the side parallel to the wall costs $500\ \mathrm{PLN/m}$. The budget is $30\,000\ \mathrm{PLN}$.

Build a model that maximizes the area of the room and prepare a complete analysis containing:

- definition of variables and units,
- mathematical model,
- domain resulting from the problem statement,
- computation of the derivative,
- determination and verification of the optimum,
- interpretation of the result,
- graph of the objective function,
- numerical verification of several values near the optimum found.

Finally, indicate which part of the solution required modeling the problem and which part was only the execution of the calculation. Produce the graph and computer calculations only after completing the mathematical solution, and treat them as verification.

## 2. Theoretical Background and Concepts
> it checks full transfer to a new problem with unequal side costs and integrates the process from model construction to independent verification.

This problem applies foundational mathematical principles:
- Rigorous application of core definitions and operator properties.
- Analytical transformations preserving structural invariants.
- Systematic reduction to canonical and solvable forms.

## 3. Detailed Step-by-Step Solution
1. **Definition of Variables and Units:**
   - $x$: length of the side parallel to the existing wall, measured in meters ($\mathrm{m}$).
   - $y$: length of each of the two sides perpendicular to the existing wall, measured in meters ($\mathrm{m}$).
   - $A$: enclosed area of the room, measured in square meters ($\mathrm{m}^2$).
   - Costs: $c_{\parallel} = 500\ \mathrm{PLN/m}$, $c_{\perp} = 300\ \mathrm{PLN/m}$. Total budget $B = 30\,000\ \mathrm{PLN}$.

2. **Mathematical Model:**
   - Objective: Maximize Area $A = x y$.
   - Budget constraint:
     $$500x + 2(300)y = 30\,000 \implies 500x + 600y = 30\,000.$$
     Divide by $100$:
     $$5x + 6y = 300 \implies y = \frac{300 - 5x}{6} = 50 - \frac{5}{6}x.$$
   - Area objective function in one variable:
     $$A(x) = x\left(50 - \frac{5}{6}x\right) = 50x - \frac{5}{6}x^2.$$

3. **Domain:**
   Physical lengths must be strictly positive:
   $$x > 0 \quad \text{and} \quad y = 50 - \frac{5}{6}x > 0 \implies 5x < 300 \implies x < 60.$$
   $$D_A = (0, 60).$$

4. **Computation of the Derivative:**
   $$A'(x) = \frac{d}{dx}\left(50x - \frac{5}{6}x^2\right) = 50 - \frac{5}{3}x.$$

5. **Determination and Verification of the Optimum:**
   Set $A'(x) = 0$:
   $$50 - \frac{5}{3}x = 0 \implies \frac{5}{3}x = 50 \implies x = 50 \cdot \frac{3}{5} = 30\ \mathrm{m}.$$
   Corresponding perpendicular dimension:
   $$y = 50 - \frac{5}{6}(30) = 50 - 25 = 25\ \mathrm{m}.$$
   - Verification of Maximum:
     $$A''(x) = -\frac{5}{3} < 0 \quad \text{for all } x.$$
     Because $A''(x) < 0$ globally on $(0, 60)$, $x = 30\ \mathrm{m}$ yields a strict global maximum.
   - Maximum Area:
     $$A_{\max} = 30 \times 25 = 750\ \mathrm{m}^2.$$

6. **Interpretation of the Result:**
   - Cost of parallel side: $30\ \mathrm{m} \times 500\ \mathrm{PLN/m} = 15\,000\ \mathrm{PLN}$.
   - Cost of two perpendicular sides: $2 \times (25\ \mathrm{m} \times 300\ \mathrm{PLN/m}) = 15\,000\ \mathrm{PLN}$.
   - The optimum splits the budget exactly in half ($50\%$ to the parallel side, $50\%$ to the perpendicular sides combined).

7. **Objective Graph:**
   On the domain $0<x<60$, the objective is a downward-opening parabola with excluded endpoint values $A(0)=A(60)=0$ and vertex $(30,750)$:
   ```text
   A (m²)
   ↑
   750                         ● (30,750)
   |                       ╭───┴───╮
   |                    ╭──╯       ╰──╮
   |                ╭───╯               ╰───╮
   0 ·············○─────────────────────────○····→ x (m)
                 0                             60
              domain endpoints are open
   ```

8. **Computer Verification (not a proof):**
   After the mathematical analysis, the following reproducible Python calculation evaluates the objective at several points near the optimum:
   ```python
   for x in (26, 28, 30, 32, 34):
       print(x, 50*x - 5*x**2/6)
   ```
   Output (area in $\mathrm{m}^2$):
   ```text
   26 736.6666666666667
   28 746.6666666666667
   30 750.0
   32 746.6666666666667
   34 736.6666666666667
   ```
   These sampled values are consistent with a maximum at $x=30$; the derivative and concavity argument, not a finite numerical sample, proves global maximality.

9. **Modeling vs. Execution:**
   - **Modeling Phase:** Identifying the variables $x, y$, interpreting the verbal budget constraint ($500x + 600y = 30\,000$), expressing $y$ in terms of $x$, establishing the objective function $A(x) = 50x - \frac{5}{6}x^2$, and recognizing the geometric domain $x \in (0, 60)$. This requires mathematical abstraction and translation.
   - **Execution Phase:** Computing $A'(x)$, setting it to $0$, solving the linear equation $x = 30$, and evaluating $A''(x) = -5/3 < 0$. This is purely algorithmic calculation.

## 4. Verification and Consistency Checks
The analytical derivation is verified through algebraic consistency, dimensional checking, and direct substitution back into the governing problem definitions.
