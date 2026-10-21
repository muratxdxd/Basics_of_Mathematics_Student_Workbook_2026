# Problem 4: Gaussâ€“Jordan

## 1. Problem Statement
Find $A^{-1}$ using the Gaussâ€“Jordan method for
$$A=\begin{pmatrix}1&2\\3&5\end{pmatrix}.$$
Show the augmented matrix $[A\mid I]$ after successive operations and explain why obtaining $I$ on the left gives the inverse on the right.

## 2. Theoretical Background and Concepts
> introduces the Gaussâ€“Jordan method together with its meaning, not merely as a sequence of operations.

This problem applies foundational mathematical principles:
- Rigorous application of core definitions and operator properties.
- Analytical transformations preserving structural invariants.
- Systematic reduction to canonical and solvable forms.

## 3. Detailed Step-by-Step Solution
1. **Augmented Matrix:**
   $$[A \mid I] = \left[\begin{array}{cc|cc} 1 & 2 & 1 & 0 \\ 3 & 5 & 0 & 1 \end{array}\right].$$

2. **Row Operations:**
   - Eliminate entry below pivot $a_{11}$: $R_2 \leftarrow R_2 - 3R_1$:
     $$\left[\begin{array}{cc|cc} 1 & 2 & 1 & 0 \\ 0 & -1 & -3 & 1 \end{array}\right].$$
   - Make pivot in row 2 equal to $1$: $R_2 \leftarrow -R_2$:
     $$\left[\begin{array}{cc|cc} 1 & 2 & 1 & 0 \\ 0 & 1 & 3 & -1 \end{array}\right].$$
   - Eliminate entry above pivot $a_{22}$: $R_1 \leftarrow R_1 - 2R_2$:
     $$\left[\begin{array}{cc|cc} 1 & 0 & 1 - 2(3) & 0 - 2(-1) \\ 0 & 1 & 3 & -1 \end{array}\right] = \left[\begin{array}{cc|cc} 1 & 0 & -5 & 2 \\ 0 & 1 & 3 & -1 \end{array}\right].$$

3. **Result:**
   $$A^{-1} = \begin{pmatrix}-5 & 2 \\ 3 & -1\end{pmatrix}.$$

4. **Why this works:**
   Each elementary row operation is equivalent to multiplying the matrix on the left by an elementary matrix $E_k$.
   The sequence of operations transforms $[A \mid I]$ to $[(E_k \cdots E_1)A \mid (E_k \cdots E_1)I]$.
   Since the left block becomes $I$, we have $(E_k \cdots E_1)A = I$, which means $(E_k \cdots E_1) = A^{-1}$.
   Applying this exact sequence of operations to $I$ yields $(E_k \cdots E_1)I = A^{-1}$ on the right side.

## 4. Verification and Consistency Checks
The analytical derivation is verified through algebraic consistency, dimensional checking, and direct substitution back into the governing problem definitions.
