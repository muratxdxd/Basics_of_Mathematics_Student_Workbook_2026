# Problem 1: Line Through Two Points

## 1. Problem Statement
Find the equation of the line through $A=(1,2)$ and $B=(4,-1)$ in parametric and general form. Identify a direction vector and an example of a normal vector. Check that both points satisfy the equation you obtain.

## 2. Theoretical Background and Concepts
> teaches how to move between equivalent descriptions of a line and connect them with the appropriate vectors.

This problem applies foundational mathematical principles:
- Rigorous application of core definitions and operator properties.
- Analytical transformations preserving structural invariants.
- Systematic reduction to canonical and solvable forms.

## 3. Detailed Step-by-Step Solution
1. **Direction Vector:**
   $$v = \overrightarrow{AB} = B - A = (4 - 1, -1 - 2) = (3, -3) \sim (1, -1).$$

2. **Parametric Form:**
   Using base point $A(1, 2)$ and simplified direction $v = (1, -1)$:
   $$\begin{pmatrix}x\\y\end{pmatrix} = \begin{pmatrix}1\\2\end{pmatrix} + t\begin{pmatrix}1\\-1\end{pmatrix} \iff \begin{cases} x = 1 + t, \\ y = 2 - t, \end{cases} \quad t \in \mathbb{R}.$$

3. **General Form:**
   Eliminating $t$: from $x = 1 + t \implies t = x - 1$.
   Substitute into $y$: $y = 2 - (x - 1) \implies y = 3 - x \implies x + y - 3 = 0$.

4. **Vectors:**
   - Direction vector: $v = (1, -1)$.
   - Normal vector: $n = (1, 1)$ (read directly from the coefficients of $Ax + By + C = 0$).
   - Check orthogonality: $n \cdot v = 1(1) + 1(-1) = 0$.

## 4. Verification and Consistency Checks
5. **Verification:**
   - For $A(1, 2)$: $1 + 2 - 3 = 0$ (holds).
   - For $B(4, -1)$: $4 + (-1) - 3 = 0$ (holds).
