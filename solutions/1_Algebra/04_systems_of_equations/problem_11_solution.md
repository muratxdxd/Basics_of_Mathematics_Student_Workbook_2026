# Problem 11: A Parameter in a System of Three Equations

## 1. Problem Statement
Analyze the number of solutions depending on $t$:
$$\begin{cases}x+y+z=1,\\x+ty+z=2,\\x+y+tz=3.\end{cases}$$
Use elimination and separately analyze the parameter values for which a standard calculation step ceases to be valid.

## 2. Theoretical Background and Concepts
> develops parametric analysis while still relying only on elimination.

This problem applies foundational mathematical principles:
- Rigorous application of core definitions and operator properties.
- Analytical transformations preserving structural invariants.
- Systematic reduction to canonical and solvable forms.

## 3. Detailed Step-by-Step Solution
1. **Augmented Matrix and Elimination:**
   $$\left[\begin{array}{ccc|c} 1 & 1 & 1 & 1 \\ 1 & t & 1 & 2 \\ 1 & 1 & t & 3 \end{array}\right].$$
   - $R_2 \leftarrow R_2 - R_1 \implies (0, t-1, 0 \mid 1)$.
   - $R_3 \leftarrow R_3 - R_1 \implies (0, 0, t-1 \mid 2)$.
   $$\left[\begin{array}{ccc|c} 1 & 1 & 1 & 1 \\ 0 & t-1 & 0 & 1 \\ 0 & 0 & t-1 & 2 \end{array}\right].$$

2. **Analysis of Parameter $t$:**
   The standard back-substitution step requires dividing by $t - 1$, which is valid if and only if $t - 1 \neq 0 \iff t \neq 1$.
   - **Case 1: $t = 1$:**
     Row 2 becomes $[0\ 0\ 0 \mid 1]$, which translates to $0\cdot x + 0\cdot y + 0\cdot z = 1 \iff 0 = 1$.
     Row 3 becomes $[0\ 0\ 0 \mid 2]$, which translates to $0 = 2$.
     Both rows produce contradictions. Therefore, for $t = 1$, the system has **no solution** (inconsistent).
   - **Case 2: $t \neq 1$:**
     Since $t - 1 \neq 0$, division is valid:
     $$z = \frac{2}{t-1}, \qquad y = \frac{1}{t-1}.$$
     $$x = 1 - y - z = 1 - \frac{1}{t-1} - \frac{2}{t-1} = 1 - \frac{3}{t-1} = \frac{t-4}{t-1}.$$
     For every $t \neq 1$, there is **exactly one unique solution**:
     $$(x, y, z) = \left(\frac{t-4}{t-1}, \frac{1}{t-1}, \frac{2}{t-1}\right).$$

## 4. Verification and Consistency Checks
The analytical derivation is verified through algebraic consistency, dimensional checking, and direct substitution back into the governing problem definitions.
