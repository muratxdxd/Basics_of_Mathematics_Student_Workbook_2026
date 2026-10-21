# Problem 8: Linear Combination and Checking the Result

## 1. Problem Statement
Check whether $w=(5,1)$ can be written as
$$w=au+bv,$$
where $u=(1,1)$ and $v=(2,-1)$. If so, find $a,b$, reconstruct $w$ from them, and explain the geometric meaning of the existence of such coefficients.

## 2. Theoretical Background and Concepts
> connects linear combinations with the geometry of directions.

This problem applies foundational mathematical principles:
- Rigorous application of core definitions and operator properties.
- Analytical transformations preserving structural invariants.
- Systematic reduction to canonical and solvable forms.

## 3. Detailed Step-by-Step Solution
1. **Set Up the System:**
   $$a\begin{pmatrix}1\\1\end{pmatrix} + b\begin{pmatrix}2\\-1\end{pmatrix} = \begin{pmatrix}5\\1\end{pmatrix} \iff \begin{cases} a + 2b = 5, \\ a - b = 1. \end{cases}$$

2. **Solve for $a$ and $b$:**
   Subtract the second equation from the first:
   $$(a + 2b) - (a - b) = 5 - 1 \implies 3b = 4 \implies b = \frac{4}{3}.$$
   From the second equation:
   $$a = 1 + b = 1 + \frac{4}{3} = \frac{7}{3}.$$

3. **Reconstruction Check:**
   $$\frac{7}{3}u + \frac{4}{3}v = \frac{7}{3}\begin{pmatrix}1\\1\end{pmatrix} + \frac{4}{3}\begin{pmatrix}2\\-1\end{pmatrix} = \begin{pmatrix}\frac{7}{3} + \frac{8}{3} \\ \frac{7}{3} - \frac{4}{3}\end{pmatrix} = \begin{pmatrix}\frac{15}{3} \\ \frac{3}{3}\end{pmatrix} = \begin{pmatrix}5\\1\end{pmatrix} = w.$$

4. **Geometric Meaning:**
   Vectors $u$ and $v$ are not collinear (they point in different directions, $\det(u, v) = 1(-1)-1(2) = -3 \neq 0$), so they span the entire 2D plane $\mathbb{R}^2$ as a basis. The existence of unique scalars $a = 7/3, b = 4/3$ means $w$ is the diagonal of a parallelogram whose sides are along the axes determined by directions $u$ and $v$.

## 4. Verification and Consistency Checks
The analytical derivation is verified through algebraic consistency, dimensional checking, and direct substitution back into the governing problem definitions.
