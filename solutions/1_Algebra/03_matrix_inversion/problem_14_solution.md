# Problem 14: A Matrix That Is Its Own Inverse

## 1. Problem Statement
Assume that a square matrix $A$ satisfies
$$A^2=I.$$
Show that
$$A^{-1}=A.$$
Then give an example of a $2\times2$ matrix different from $I$ and $-I$ that satisfies this condition, and verify it by multiplication.

## 2. Theoretical Background and Concepts
> requires using the definition of the inverse in a short argument and constructing an example independently, without introducing a new topic.

This problem applies foundational mathematical principles:
- Rigorous application of core definitions and operator properties.
- Analytical transformations preserving structural invariants.
- Systematic reduction to canonical and solvable forms.

## 3. Detailed Step-by-Step Solution
1. **Proof:**
   By assumption, $A^2 = A \cdot A = I$.
   By the definition of the inverse matrix, if a matrix $B$ satisfies $A B = I$ and $B A = I$, then $B = A^{-1}$.
   Taking $B = A$, we have:
   $$A \cdot A = I.$$
   Therefore, by definition, $A^{-1} = A$. (Such a matrix is called *involutory*).

2. **Example Different from $\pm I$:**
   Consider the reflection matrix across the line $y = x$:
   $$A = \begin{pmatrix}0 & 1 \\ 1 & 0\end{pmatrix}.$$
   Notice $A \neq I$ and $A \neq -I$.

## 4. Verification and Consistency Checks
3. **Verification by Multiplication:**
   $$A^2 = \begin{pmatrix}0 & 1 \\ 1 & 0\end{pmatrix}\begin{pmatrix}0 & 1 \\ 1 & 0\end{pmatrix} = \begin{pmatrix}0(0) + 1(1) & 0(1) + 1(0) \\ 1(0) + 0(1) & 1(1) + 0(0)\end{pmatrix} = \begin{pmatrix}1 & 0 \\ 0 & 1\end{pmatrix} = I.$$
   Hence $A^{-1} = A$.
