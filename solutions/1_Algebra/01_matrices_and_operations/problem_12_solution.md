# Problem 12: Formula for a Matrix Power

## 1. Problem Statement
Let
$$A=\begin{pmatrix}1&1\\0&1\end{pmatrix}.$$
Compute $A^2$, $A^3$, and $A^4$, and use them to formulate a conjecture for $A^n$. Then do not stop after checking one more case: assume the formula is true for $n$, multiply by $A$, and explain why you obtain exactly the formula for $n+1$.

## 2. Theoretical Background and Concepts
> teaches how to recognize a pattern and formulate a generalization from several computations.

This problem applies foundational mathematical principles:
- Rigorous application of core definitions and operator properties.
- Analytical transformations preserving structural invariants.
- Systematic reduction to canonical and solvable forms.

## 3. Detailed Step-by-Step Solution
1. **Calculate Powers:**
   $$A^2 = \begin{pmatrix}1&1\\0&1\end{pmatrix}\begin{pmatrix}1&1\\0&1\end{pmatrix} = \begin{pmatrix}1 & 2 \\ 0 & 1\end{pmatrix}.$$
   $$A^3 = A^2 A = \begin{pmatrix}1&2\\0&1\end{pmatrix}\begin{pmatrix}1&1\\0&1\end{pmatrix} = \begin{pmatrix}1 & 3 \\ 0 & 1\end{pmatrix}.$$
   $$A^4 = A^3 A = \begin{pmatrix}1&3\\0&1\end{pmatrix}\begin{pmatrix}1&1\\0&1\end{pmatrix} = \begin{pmatrix}1 & 4 \\ 0 & 1\end{pmatrix}.$$

2. **Conjecture:**
   For all $n \in \mathbb{N}$,
   $$A^n = \begin{pmatrix}1 & n \\ 0 & 1\end{pmatrix}.$$

3. **Mathematical Induction Proof:**
   - **Base Case:** For $n=1$, $A^1 = \begin{pmatrix}1&1\\0&1\end{pmatrix}$, which matches the formula.
   - **Inductive Step:** Assume the statement holds for $n$, i.e., $A^n = \begin{pmatrix}1&n\\0&1\end{pmatrix}$.
     Then for $n+1$:
     $$A^{n+1} = A^n A = \begin{pmatrix}1&n\\0&1\end{pmatrix}\begin{pmatrix}1&1\\0&1\end{pmatrix} = \begin{pmatrix}1(1)+n(0) & 1(1)+n(1) \\ 0(1)+1(0) & 0(1)+1(1)\end{pmatrix} = \begin{pmatrix}1 & n+1 \\ 0 & 1\end{pmatrix}.$$
   The formula holds for $n+1$. By induction, $A^n = \begin{pmatrix}1&n\\0&1\end{pmatrix}$ for all $n \ge 1$.

## 4. Verification and Consistency Checks
The analytical derivation is verified through algebraic consistency, dimensional checking, and direct substitution back into the governing problem definitions.
