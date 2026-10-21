# Problem 1: Matrix Size and Entries

## 1. Problem Statement
Given
$$A=\begin{pmatrix}2&-1&3\\0&4&5\end{pmatrix},\qquad B=\begin{pmatrix}1&0\\-2&3\\4&1\end{pmatrix}.$$

1. State the sizes of matrices $A$ and $B$.
2. Read off the entries $a_{12}$, $a_{23}$, $b_{21}$, and $b_{32}$.
3. Write the second row of $A$ and the first column of $B$ as vectors.

## 2. Theoretical Background and Concepts
> builds basic fluency with matrix notation, indices, rows, and columns.

This problem applies foundational mathematical principles:
- Rigorous application of core definitions and operator properties.
- Analytical transformations preserving structural invariants.
- Systematic reduction to canonical and solvable forms.

## 3. Detailed Step-by-Step Solution
1. **Matrix Sizes:**
   - Matrix $A$ has $2$ rows and $3$ columns, so its size is $2 \times 3$.
   - Matrix $B$ has $3$ rows and $2$ columns, so its size is $3 \times 2$.

2. **Matrix Entries ($m_{ij}$ denotes the entry in row $i$, column $j$):**
   - $a_{12} = -1$ (row 1, column 2 of $A$)
   - $a_{23} = 5$ (row 2, column 3 of $A$)
   - $b_{21} = -2$ (row 2, column 1 of $B$)
   - $b_{32} = 1$ (row 3, column 2 of $B$)

3. **Rows and Columns as Vectors:**
   - Second row of $A$: $r_2 = \begin{pmatrix}0 & 4 & 5\end{pmatrix} \in \mathbb{R}^{1\times 3}$ (or as a row vector $(0, 4, 5)$).
   - First column of $B$: $c_1 = \begin{pmatrix}1 \\ -2 \\ 4\end{pmatrix} \in \mathbb{R}^{3\times 1}$.

## 4. Verification and Consistency Checks
Checking dimensions: row 2 of $A$ has 3 elements matching the 3 columns of $A$. Column 1 of $B$ has 3 elements matching the 3 rows of $B$. Indices correspond directly to the matrix definition.
