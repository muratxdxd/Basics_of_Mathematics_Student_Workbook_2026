# Problem 11: When Do Matrices Commute?

## 1. Problem Statement
Given
$$A=\begin{pmatrix}1&1\\0&1\end{pmatrix},\qquad B=\begin{pmatrix}a&b\\c&d\end{pmatrix}.$$
Find the conditions on $a,b,c,d$ under which $AB=BA$. Describe the general form of all such matrices $B$.

## 2. Theoretical Background and Concepts
> deepens the idea of noncommutativity by finding the conditions under which commutativity does hold.

This problem applies foundational mathematical principles:
- Rigorous application of core definitions and operator properties.
- Analytical transformations preserving structural invariants.
- Systematic reduction to canonical and solvable forms.

## 3. Detailed Step-by-Step Solution
1. **Compute Both Products:**
   $$AB = \begin{pmatrix}1&1\\0&1\end{pmatrix}\begin{pmatrix}a&b\\c&d\end{pmatrix} = \begin{pmatrix}a+c & b+d \\ c & d\end{pmatrix}.$$
   $$BA = \begin{pmatrix}a&b\\c&d\end{pmatrix}\begin{pmatrix}1&1\\0&1\end{pmatrix} = \begin{pmatrix}a & a+b \\ c & c+d\end{pmatrix}.$$

2. **Equate Corresponding Entries ($AB = BA$):**
   - Entry $(1,1)$: $a + c = a \implies c = 0$.
   - Entry $(2,1)$: $c = c$ (identically true since $c=0$).
   - Entry $(2,2)$: $d = c + d \implies c = 0$ (consistent).
   - Entry $(1,2)$: $b + d = a + b \implies d = a$.

3. **Conclusion and General Form:**
   The matrices commute if and only if $c = 0$ and $d = a$. The parameter $b$ can be any real number.
   Thus, the general form of all matrices commuting with $A$ is:
   $$B = \begin{pmatrix}a & b \\ 0 & a\end{pmatrix} = a\begin{pmatrix}1&0\\0&1\end{pmatrix} + b\begin{pmatrix}0&1\\0&0\end{pmatrix} = a I + b(A - I), \quad \text{for any } a,b \in \mathbb{R}.$$

## 4. Verification and Consistency Checks
$$AB = \begin{pmatrix}1&1\\0&1\end{pmatrix}\begin{pmatrix}a&b\\0&a\end{pmatrix} = \begin{pmatrix}a & a+b \\ 0 & a\end{pmatrix},$$
$$BA = \begin{pmatrix}a&b\\0&a\end{pmatrix}\begin{pmatrix}1&1\\0&1\end{pmatrix} = \begin{pmatrix}a & a+b \\ 0 & a\end{pmatrix}.$$
Both products are identical, confirming the conditions.
