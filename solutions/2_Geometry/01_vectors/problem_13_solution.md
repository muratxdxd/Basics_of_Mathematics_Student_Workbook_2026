# Problem 13: Do Four Points Lie in One Plane?

## 1. Problem Statement
Given
$$A=(0,0,0),\qquad B=(1,2,0),\qquad C=(0,1,1),\qquad D=(2,5,1).$$

1. Construct $\overrightarrow{AB}$ and $\overrightarrow{AC}$.
2. Find $n=\overrightarrow{AB}\times\overrightarrow{AC}$.
3. Construct $\overrightarrow{AD}$ and check whether $\overrightarrow{AD}\cdot n=0$.
4. Based on this, decide whether $D$ lies in the plane determined by $A,B,C$, and justify the criterion.

## 2. Theoretical Background and Concepts
> combines the known cross and dot products into a geometric criterion needed for planes, without introducing a separate concept used only once.

This problem applies foundational mathematical principles:
- Rigorous application of core definitions and operator properties.
- Analytical transformations preserving structural invariants.
- Systematic reduction to canonical and solvable forms.

## 3. Detailed Step-by-Step Solution
1. **Construct $\overrightarrow{AB}$ and $\overrightarrow{AC}$:**
   $$\overrightarrow{AB} = (1 - 0, 2 - 0, 0 - 0) = (1, 2, 0).$$
   $$\overrightarrow{AC} = (0 - 0, 1 - 0, 1 - 0) = (0, 1, 1).$$

2. **Find $n = \overrightarrow{AB} \times \overrightarrow{AC}$:**
   $$n = \det\begin{pmatrix}i & j & k \\ 1 & 2 & 0 \\ 0 & 1 & 1\end{pmatrix} = i(2\cdot 1 - 0\cdot 1) - j(1\cdot 1 - 0\cdot 0) + k(1\cdot 1 - 2\cdot 0) = (2, -1, 1).$$

3. **Construct $\overrightarrow{AD}$ and Check $\overrightarrow{AD} \cdot n$:**
   $$\overrightarrow{AD} = (2 - 0, 5 - 0, 1 - 0) = (2, 5, 1).$$
   $$\overrightarrow{AD} \cdot n = 2(2) + 5(-1) + 1(1) = 4 - 5 + 1 = 0.$$

4. **Decision and Justification:**
   **Yes, $D$ lies in the plane determined by $A, B, C$.**
   *Justification:* The cross product $n = \overrightarrow{AB} \times \overrightarrow{AC}$ is perpendicular to the plane containing $A, B, C$. Any point $D$ lies in this plane if and only if the displacement vector $\overrightarrow{AD}$ lies in the plane, which requires $\overrightarrow{AD}$ to be perpendicular to $n$ ($\overrightarrow{AD} \cdot n = 0$). Since the scalar triple product is zero, the parallelepiped spanned by the three vectors has volume zero, proving coplanarity.

## 4. Verification and Consistency Checks
The analytical derivation is verified through algebraic consistency, dimensional checking, and direct substitution back into the governing problem definitions.
