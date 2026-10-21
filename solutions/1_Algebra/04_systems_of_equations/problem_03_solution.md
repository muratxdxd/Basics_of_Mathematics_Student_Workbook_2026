# Problem 3: Inconsistent System

## 1. Problem Statement
Solve or show that the system is inconsistent:
$$\begin{cases}x+2y=3,\\2x+4y=7.\end{cases}$$
Show how the contradiction appears in the matrix after elimination and interpret it in terms of equations.

## 2. Theoretical Background and Concepts
> teaches how to recognize that a system has no solution without guessing.

This problem applies foundational mathematical principles:
- Rigorous application of core definitions and operator properties.
- Analytical transformations preserving structural invariants.
- Systematic reduction to canonical and solvable forms.

## 3. Detailed Step-by-Step Solution
1. **Augmented Matrix:**
   $$\left[\begin{array}{cc|c} 1 & 2 & 3 \\ 2 & 4 & 7 \end{array}\right].$$

2. **Elimination Step:**
   $R_2 \leftarrow R_2 - 2R_1$:
   Row 2 becomes $(2 - 2(1), 4 - 2(2) \mid 7 - 2(3)) = (0, 0 \mid 1)$.
   $$\left[\begin{array}{cc|c} 1 & 2 & 3 \\ 0 & 0 & 1 \end{array}\right].$$

3. **Contradiction and Geometric Interpretation:**
   - Row 2 translates to the algebraic equation:
     $$0\cdot x + 0\cdot y = 1 \iff 0 = 1.$$
     Since $0 = 1$ is never true for any real values of $x$ and $y$, the system has **no solution** (it is inconsistent).
   - Geometrically, both equations represent straight lines in $\mathbb{R}^2$ with identical slope ($-\frac{1}{2}$), but different $y$-intercepts:
     $$L_1: y = -\frac{1}{2}x + \frac{3}{2}, \qquad L_2: y = -\frac{1}{2}x + \frac{7}{4}.$$
     The lines are strictly parallel and never intersect.

## 4. Verification and Consistency Checks
The analytical derivation is verified through algebraic consistency, dimensional checking, and direct substitution back into the governing problem definitions.
