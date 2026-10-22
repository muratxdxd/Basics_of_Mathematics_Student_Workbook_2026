# Problem 2: Gaussian Elimination â€” One Solution

## 1. Problem Statement
Solve using Gaussian elimination:
$$\begin{cases}x+y+z=6,\\2x-y+z=3,\\x+2y-z=2.\end{cases}$$
After solving, substitute the result into all equations and check consistency.

## 2. Theoretical Background and Concepts
> introduces the basic method for solving a system and builds the habit of checking the result.

This problem applies foundational mathematical principles:
- Rigorous application of core definitions and operator properties.
- Analytical transformations preserving structural invariants.
- Systematic reduction to canonical and solvable forms.

## 3. Detailed Step-by-Step Solution
1. **Augmented Matrix:**
   $$\left[\begin{array}{ccc|c} 1 & 1 & 1 & 6 \\ 2 & -1 & 1 & 3 \\ 1 & 2 & -1 & 2 \end{array}\right].$$

2. **Forward Elimination:**
   Each row replacement adds a multiple of one equation to another, and swapping rows only changes their order; both operations preserve the system's solution set because they are reversible.
   - $R_2 \leftarrow R_2 - 2R_1$:
     Row 2 becomes $(2-2, -1-2, 1-2 \mid 3-12) = (0, -3, -1 \mid -9)$.
   - $R_3 \leftarrow R_3 - R_1$:
     Row 3 becomes $(1-1, 2-1, -1-1 \mid 2-6) = (0, 1, -2 \mid -4)$.
     $$\left[\begin{array}{ccc|c} 1 & 1 & 1 & 6 \\ 0 & -3 & -1 & -9 \\ 0 & 1 & -2 & -4 \end{array}\right].$$
   - Swap $R_2 \leftrightarrow R_3$:
     $$\left[\begin{array}{ccc|c} 1 & 1 & 1 & 6 \\ 0 & 1 & -2 & -4 \\ 0 & -3 & -1 & -9 \end{array}\right].$$
   - $R_3 \leftarrow R_3 + 3R_2$:
     Row 3 becomes $(0, -3+3, -1+3(-2) \mid -9+3(-4)) = (0, 0, -7 \mid -21)$.
     $$\left[\begin{array}{ccc|c} 1 & 1 & 1 & 6 \\ 0 & 1 & -2 & -4 \\ 0 & 0 & -7 & -21 \end{array}\right].$$

3. **Back-Substitution:**
   The elimination has produced a triangular system, so solve from its last equation upward:
   - From Row 3: $-7z = -21 \implies z = 3$.
   - From Row 2: $y - 2(3) = -4 \implies y - 6 = -4 \implies y = 2$.
   - From Row 1: $x + 2 + 3 = 6 \implies x + 5 = 6 \implies x = 1$.
   Unique solution: $(x, y, z) = (1, 2, 3)$.

## 4. Verification and Consistency Checks
4. **Consistency Verification:**
   Substituting the result into every original equation confirms it satisfies the original system, not just the transformed equations:
   - Equation 1: $1 + 2 + 3 = 6$ (holds).
   - Equation 2: $2(1) - 2 + 3 = 2 - 2 + 3 = 3$ (holds).
   - Equation 3: $1 + 2(2) - 3 = 1 + 4 - 3 = 2$ (holds).
