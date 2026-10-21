# Problem 14: Rotation Matrices

## 1. Problem Statement
The matrix for a rotation through an angle $\theta$ is
$$R(\theta)=\begin{pmatrix}\cos\theta&-\sin\theta\\\sin\theta&\cos\theta\end{pmatrix}.$$
Compute $R(\alpha)R(\beta)$ and, using the angle-sum formulas for sine and cosine, show that
$$R(\alpha)R(\beta)=R(\alpha+\beta).$$
Explain the result geometrically.

## 2. Theoretical Background and Concepts
> shows the consistency between matrix algebra and the geometry of composing rotations.

This problem applies foundational mathematical principles:
- Rigorous application of core definitions and operator properties.
- Analytical transformations preserving structural invariants.
- Systematic reduction to canonical and solvable forms.

## 3. Detailed Step-by-Step Solution
1. **Matrix Multiplication:**
   $$R(\alpha)R(\beta) = \begin{pmatrix}\cos\alpha & -\sin\alpha \\ \sin\alpha & \cos\alpha\end{pmatrix}\begin{pmatrix}\cos\beta & -\sin\beta \\ \sin\beta & \cos\beta\end{pmatrix}$$
   $$= \begin{pmatrix}\cos\alpha\cos\beta - \sin\alpha\sin\beta & -(\cos\alpha\sin\beta + \sin\alpha\cos\beta) \\ \sin\alpha\cos\beta + \cos\alpha\sin\beta & -\sin\alpha\sin\beta + \cos\alpha\cos\beta\end{pmatrix}.$$

2. **Angle-Sum Trigonometric Identities:**
   Recall:
   $$\cos(\alpha+\beta) = \cos\alpha\cos\beta - \sin\alpha\sin\beta,$$
   $$\sin(\alpha+\beta) = \sin\alpha\cos\beta + \cos\alpha\sin\beta.$$
   Substituting these identities into the product:
   $$R(\alpha)R(\beta) = \begin{pmatrix}\cos(\alpha+\beta) & -\sin(\alpha+\beta) \\ \sin(\alpha+\beta) & \cos(\alpha+\beta)\end{pmatrix} = R(\alpha+\beta).$$

3. **Geometric Explanation:**
   Multiplying a vector $v$ by $R(\beta)$ rotates it counterclockwise by an angle $\beta$ about the origin. Multiplying the result by $R(\alpha)$ rotates it further counterclockwise by an angle $\alpha$. The net effect is a single rotation about the origin through the combined angle $\alpha+\beta$, which is precisely represented by $R(\alpha+\beta)$.

## 4. Verification and Consistency Checks
The analytical derivation is verified through algebraic consistency, dimensional checking, and direct substitution back into the governing problem definitions.
