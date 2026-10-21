# Problem 13: Does Every Equation Add New Information?

## 1. Problem Statement
Consider the system
$$x_1+x_2=10,\qquad x_2+x_3=8,\qquad x_1-x_3=2.$$
Solve it and check whether all three equations are independently necessary to describe the solution set. If one follows from the others, show this by calculation.

## 2. Theoretical Background and Concepts
> teaches how to recognize redundant equations within a system.

This problem applies foundational mathematical principles:
- Rigorous application of core definitions and operator properties.
- Analytical transformations preserving structural invariants.
- Systematic reduction to canonical and solvable forms.

## 3. Detailed Step-by-Step Solution
1. **Check for Redundancy:**
   Subtract the second equation from the first:
   $$(x_1 + x_2) - (x_2 + x_3) = 10 - 8 \implies x_1 - x_3 = 2.$$
   This is precisely the third equation.
   Therefore, Equation 3 follows directly from Equation 1 and Equation 2 ($E_3 = E_1 - E_2$). It is **redundant** and adds no new constraints to the solution set.

2. **Solve the System:**
   We only need the first two equations:
   - $x_1 = 10 - x_2$.
   - $x_3 = 8 - x_2$.
   Let $x_2 = t \in \mathbb{R}$ be the free parameter:
   $$\begin{pmatrix}x_1 \\ x_2 \\ x_3\end{pmatrix} = \begin{pmatrix}10 - t \\ t \\ 8 - t\end{pmatrix} = \begin{pmatrix}10 \\ 0 \\ 8\end{pmatrix} + t\begin{pmatrix}-1 \\ 1 \\ -1\end{pmatrix}, \quad t \in \mathbb{R}.$$
   The solution set is a 1-dimensional line in $\mathbb{R}^3$, confirming that only two equations were independent.

## 4. Verification and Consistency Checks
The analytical derivation is verified through algebraic consistency, dimensional checking, and direct substitution back into the governing problem definitions.
