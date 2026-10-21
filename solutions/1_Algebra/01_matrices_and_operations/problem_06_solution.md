# Problem 6: Transpose

## 1. Problem Statement
For
$$A=\begin{pmatrix}1&2&3\\4&5&6\end{pmatrix},\qquad B=\begin{pmatrix}1&0\\2&1\\-1&3\end{pmatrix}$$
compute $A^T$, $B^T$, and $AB$. Then verify in this example that
$$(AB)^T=B^TA^T.$$

## 2. Theoretical Background and Concepts
> teaches transposition and an important property that reverses the order of factors.

This problem applies foundational mathematical principles:
- Rigorous application of core definitions and operator properties.
- Analytical transformations preserving structural invariants.
- Systematic reduction to canonical and solvable forms.

## 3. Detailed Step-by-Step Solution
1. **Transposes:**
   $$A^T = \begin{pmatrix}1&4\\2&5\\3&6\end{pmatrix}_{3\times 2}, \qquad B^T = \begin{pmatrix}1&2&-1\\0&1&3\end{pmatrix}_{2\times 3}.$$

2. **Product $AB$:**
   $$AB = \begin{pmatrix}1&2&3\\4&5&6\end{pmatrix}\begin{pmatrix}1&0\\2&1\\-1&3\end{pmatrix} = \begin{pmatrix}1(1)+2(2)+3(-1) & 1(0)+2(1)+3(3) \\ 4(1)+5(2)+6(-1) & 4(0)+5(1)+6(3)\end{pmatrix} = \begin{pmatrix}1+4-3 & 0+2+9 \\ 4+10-6 & 0+5+18\end{pmatrix} = \begin{pmatrix}2 & 11 \\ 8 & 23\end{pmatrix}.$$

3. **Transpose $(AB)^T$:**
   $$(AB)^T = \begin{pmatrix}2 & 8 \\ 11 & 23\end{pmatrix}.$$

4. **Product $B^T A^T$:**
   $$B^T A^T = \begin{pmatrix}1&2&-1\\0&1&3\end{pmatrix}\begin{pmatrix}1&4\\2&5\\3&6\end{pmatrix} = \begin{pmatrix}1(1)+2(2)-1(3) & 1(4)+2(5)-1(6) \\ 0(1)+1(2)+3(3) & 0(4)+1(5)+3(6)\end{pmatrix} = \begin{pmatrix}2 & 8 \\ 11 & 23\end{pmatrix}.$$

## 4. Verification and Consistency Checks
$(AB)^T = \begin{pmatrix}2&8\\11&23\end{pmatrix} = B^T A^T$. The property $(AB)^T = B^T A^T$ holds.
