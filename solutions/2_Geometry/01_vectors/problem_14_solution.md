# Problem 14: Closest Point on a Line

## 1. Problem Statement
Given a point $P=(4,1)$ and a line through the origin with direction $v=(1,2)$. Using projection, find the closest point on the line, the distance from $P$ to the line, and verify that the appropriate vector is perpendicular to the direction of the line.

## 2. Theoretical Background and Concepts
> shows projection as a complete solution to a minimum-distance problem.

This problem applies foundational mathematical principles:
- Rigorous application of core definitions and operator properties.
- Analytical transformations preserving structural invariants.
- Systematic reduction to canonical and solvable forms.

## 3. Detailed Step-by-Step Solution
1. **Find Closest Point $Q$ via Projection:**
   Since the line passes through the origin, the closest point $Q$ is the orthogonal projection of vector $\overrightarrow{OP} = (4, 1)$ onto $v$:
   $$Q = \operatorname{proj}_v P = \frac{P \cdot v}{\|v\|^2} v = \frac{4(1) + 1(2)}{1^2 + 2^2}(1, 2) = \frac{6}{5}(1, 2) = \left(\frac{6}{5}, \frac{12}{5}\right) = (1.2, 2.4).$$

2. **Compute Distance from $P$ to the Line:**
   The error vector $\overrightarrow{QP} = P - Q$:
   $$\overrightarrow{QP} = (4 - 1.2, 1 - 2.4) = (2.8, -1.4) = \left(\frac{14}{5}, -\frac{7}{5}\right).$$
   $$d = \|\overrightarrow{QP}\| = \sqrt{\left(\frac{14}{5}\right)^2 + \left(-\frac{7}{5}\right)^2} = \sqrt{\frac{196 + 49}{25}} = \sqrt{\frac{245}{25}} = \frac{7\sqrt{5}}{5} \approx 3.1305.$$

3. **Verify Perpendicularity:**
   $$\overrightarrow{QP} \cdot v = \frac{14}{5}(1) + \left(-\frac{7}{5}\right)(2) = \frac{14}{5} - \frac{14}{5} = 0.$$
   The displacement vector between $P$ and $Q$ is strictly orthogonal to the line direction $v$, confirming $Q$ minimizes the distance.

## 4. Verification and Consistency Checks
The analytical derivation is verified through algebraic consistency, dimensional checking, and direct substitution back into the governing problem definitions.
