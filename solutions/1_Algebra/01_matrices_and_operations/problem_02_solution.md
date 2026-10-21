# Problem 2: Addition and Scalar Multiplication

## 1. Problem Statement
For
$$A=\begin{pmatrix}1&2\\-1&3\end{pmatrix},\qquad B=\begin{pmatrix}4&-2\\0&5\end{pmatrix}$$
compute
$$A+B,\qquad A-B,\qquad 3A-2B.$$
Explain why matrix addition is possible only for matrices of the same size.

## 2. Theoretical Background and Concepts
> reinforces entry-by-entry operations and the importance of compatible dimensions.

This problem applies foundational mathematical principles:
- Rigorous application of core definitions and operator properties.
- Analytical transformations preserving structural invariants.
- Systematic reduction to canonical and solvable forms.

## 3. Detailed Step-by-Step Solution
1. **Computation of $A+B$:**
   $$A+B = \begin{pmatrix}1+4 & 2+(-2) \\ -1+0 & 3+5\end{pmatrix} = \begin{pmatrix}5 & 0 \\ -1 & 8\end{pmatrix}.$$

2. **Computation of $A-B$:**
   $$A-B = \begin{pmatrix}1-4 & 2-(-2) \\ -1-0 & 3-5\end{pmatrix} = \begin{pmatrix}-3 & 4 \\ -1 & -2\end{pmatrix}.$$

3. **Computation of $3A-2B$:**
   $$3A = 3\begin{pmatrix}1&2\\-1&3\end{pmatrix} = \begin{pmatrix}3&6\\-3&9\end{pmatrix}, \qquad 2B = 2\begin{pmatrix}4&-2\\0&5\end{pmatrix} = \begin{pmatrix}8&-4\\0&10\end{pmatrix}.$$
   $$3A - 2B = \begin{pmatrix}3-8 & 6-(-4) \\ -3-0 & 9-10\end{pmatrix} = \begin{pmatrix}-5 & 10 \\ -3 & -1\end{pmatrix}.$$

4. **Why matrix addition requires the same size:**
   Matrix addition is defined element-wise: $(A+B)_{ij} = a_{ij} + b_{ij}$. If two matrices have different dimensions, there exist entries in one matrix that have no corresponding counterpart in the other, leaving the sum undefined.

## 4. Verification and Consistency Checks
$(A+B) - A = \begin{pmatrix}5-1 & 0-2 \\ -1-(-1) & 8-3\end{pmatrix} = \begin{pmatrix}4 & -2 \\ 0 & 5\end{pmatrix} = B$, which confirms consistency.
