# Problem 5: Relative Position of Two Lines

## 1. Problem Statement
Analyze the position of
$$L_1:(x,y,z)=(1,1,0)+t(1,2,1),$$
$$L_2:(x,y,z)=(2,0,1)+s(0,1,-1).$$
If they intersect, give the intersection point. If not, determine whether they are parallel or skew. Justify the classification.

## 2. Theoretical Background and Concepts
> teaches how to distinguish qualitatively different relationships between lines in space.

This problem applies foundational mathematical principles:
- Rigorous application of core definitions and operator properties.
- Analytical transformations preserving structural invariants.
- Systematic reduction to canonical and solvable forms.

## 3. Detailed Step-by-Step Solution
1. **Direction Vectors and Parallelism Check:**
   - Direction of $L_1$: $v_1 = (1, 2, 1)$.
   - Direction of $L_2$: $v_2 = (0, 1, -1)$.
   Since $v_1$ has a non-zero $x$-component ($1$) while $v_2$ has $0$, $v_1 \neq c v_2$ for any scalar $c$. The lines are **not parallel**.

2. **Test for Intersection:**
   Equate the coordinates:
   $$\begin{cases} 1 + t = 2, \\ 1 + 2t = s, \\ t = 1 - s. \end{cases}$$
   - From equation 1: $t = 2 - 1 = 1$.
   - Substitute $t = 1$ into equation 3: $1 = 1 - s \implies s = 0$.
   - Test candidate $(t=1, s=0)$ in equation 2:
     $$\text{LHS} = 1 + 2(1) = 3, \qquad \text{RHS} = s = 0.$$
     $3 \neq 0$, which is a contradiction.

3. **Classification:**
   Because the system is inconsistent, the lines have no points in common. Since they are neither parallel nor intersecting, $L_1$ and $L_2$ are **skew lines**.

## 4. Verification and Consistency Checks
The analytical derivation is verified through algebraic consistency, dimensional checking, and direct substitution back into the governing problem definitions.
