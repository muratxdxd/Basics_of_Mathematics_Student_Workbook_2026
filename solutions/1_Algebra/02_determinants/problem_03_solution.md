# Problem 3: Swapping Two Rows

## 1. Problem Statement
For
$$A=\begin{pmatrix}1&2&0\\0&3&1\\2&1&1\end{pmatrix}$$
compute $\det A$. Then form a matrix $B$ by swapping the first and second rows of $A$.

First predict $\det B$ using a determinant property, and then verify your prediction by calculation.

## 2. Theoretical Background and Concepts
> gives a second classical calculation with a $3\times3$ determinant while teaching the precise effect of a row swap on the sign of the determinant.

This problem applies foundational mathematical principles:
- Rigorous application of core definitions and operator properties.
- Analytical transformations preserving structural invariants.
- Systematic reduction to canonical and solvable forms.

## 3. Detailed Step-by-Step Solution
1. **Compute $\det A$:**
   Expanding along row 1:
   $$\det A = 1\cdot \det\begin{pmatrix}3&1\\1&1\end{pmatrix} - 2\cdot \det\begin{pmatrix}0&1\\2&1\end{pmatrix} + 0$$
   $$= 1(3-1) - 2(0-2) = 1(2) - 2(-2) = 2 + 4 = 6.$$

2. **Form Matrix $B$ and Predict $\det B$:**
   Swapping rows 1 and 2:
   $$B = \begin{pmatrix}0&3&1\\1&2&0\\2&1&1\end{pmatrix}.$$
   *Prediction:* Swapping two rows of a matrix negates its determinant. Therefore, $\det B = -\det A = -6$.

3. **Verify Prediction by Direct Calculation:**
   Expanding along row 1 of $B$:
   $$\det B = 0 - 3\cdot \det\begin{pmatrix}1&0\\2&1\end{pmatrix} + 1\cdot \det\begin{pmatrix}1&2\\2&1\end{pmatrix}$$
   $$= -3(1 - 0) + 1(1 - 4) = -3(1) + 1(-3) = -3 - 3 = -6.$$
   The prediction $\det B = -6$ is confirmed.

## 4. Verification and Consistency Checks
The analytical derivation is verified through algebraic consistency, dimensional checking, and direct substitution back into the governing problem definitions.
