# Problem 13: A Recurrence Written in Matrix Form

## 1. Problem Statement
Let
$$F=\begin{pmatrix}1&1\\1&0\end{pmatrix}.$$
Compute $F^2$, $F^3$, $F^4$, and $F^5$. Compare the numbers obtained with the sequence
$$0,1,1,2,3,5,8,\ldots$$
and describe the relationship you observe. Then compute
$$F\begin{pmatrix}a\\b\end{pmatrix}$$
and explain how this multiplication performs one recurrence step: it creates the sum of two consecutive terms and keeps one of them for the next step.

## 2. Theoretical Background and Concepts
> shows the connection between matrix powers and a simple numerical recurrence.

This problem applies foundational mathematical principles:
- Rigorous application of core definitions and operator properties.
- Analytical transformations preserving structural invariants.
- Systematic reduction to canonical and solvable forms.

## 3. Detailed Step-by-Step Solution
1. **Calculate Powers of $F$:**
   For any $\begin{pmatrix}r&s\\u&v\end{pmatrix}$, multiplying by $F$ gives
   $$\begin{pmatrix}r&s\\u&v\end{pmatrix}F
   =\begin{pmatrix}r(1)+s(1)&r(1)+s(0)\\u(1)+v(1)&u(1)+v(0)\end{pmatrix}
   =\begin{pmatrix}r+s&r\\u+v&u\end{pmatrix}.$$
   Applying this row-by-column rule successively:
   $$F^2 = \begin{pmatrix}1+1&1\\1+0&1\end{pmatrix} = \begin{pmatrix}2&1\\1&1\end{pmatrix}.$$
   $$F^3 = F^2F = \begin{pmatrix}2+1&2\\1+1&1\end{pmatrix} = \begin{pmatrix}3&2\\2&1\end{pmatrix}.$$
   $$F^4 = F^3F = \begin{pmatrix}3+2&3\\2+1&2\end{pmatrix} = \begin{pmatrix}5&3\\3&2\end{pmatrix}.$$
   $$F^5 = F^4F = \begin{pmatrix}5+3&5\\3+2&3\end{pmatrix} = \begin{pmatrix}8&5\\5&3\end{pmatrix}.$$

2. **Relationship with Fibonacci Sequence:**
   Let $f_0=0, f_1=1, f_2=1, f_3=2, f_4=3, f_5=5, f_6=8, \ldots$ where $f_{n+1} = f_n + f_{n-1}$.
   Comparing entries of $F^n$:
   $$F^n = \begin{pmatrix}f_{n+1} & f_n \\ f_n & f_{n-1}\end{pmatrix}.$$
   For $n=1$: $\begin{pmatrix}f_2&f_1\\f_1&f_0\end{pmatrix} = \begin{pmatrix}1&1\\1&0\end{pmatrix}$.
   For $n=5$: $\begin{pmatrix}f_6&f_5\\f_5&f_4\end{pmatrix} = \begin{pmatrix}8&5\\5&3\end{pmatrix}$.

3. **Recurrence Step:**
   $$F\begin{pmatrix}a\\b\end{pmatrix} = \begin{pmatrix}1&1\\1&0\end{pmatrix}\begin{pmatrix}a\\b\end{pmatrix} = \begin{pmatrix}a+b\\a\end{pmatrix}.$$
   - If the input vector represents two consecutive terms of the sequence $\begin{pmatrix}f_k \\ f_{k-1}\end{pmatrix}$, multiplication by $F$ generates:
     $$\begin{pmatrix}f_k + f_{k-1} \\ f_k\end{pmatrix} = \begin{pmatrix}f_{k+1} \\ f_k\end{pmatrix}.$$
   The first row creates the new term by summing the previous two, while the second row preserves the current term $f_k$ to serve as the previous term in the subsequent step.

## 4. Verification and Consistency Checks
The analytical derivation is verified through algebraic consistency, dimensional checking, and direct substitution back into the governing problem definitions.
