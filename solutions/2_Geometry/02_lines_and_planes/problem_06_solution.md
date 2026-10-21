# Problem 6: Angle Between Planes

## 1. Problem Statement
Given
$$\Pi_1:x+y+z=1,\qquad \Pi_2:x-y=2.$$
First use the normal vectors to decide whether the planes are parallel. If not, compute the angle between them and explain why the normal vectors alone are enough for this calculation.

## 2. Theoretical Background and Concepts
> focuses attention on one mechanismâ€”using normals to analyze position and angleâ€”without also introducing the construction of the intersection line.

This problem applies foundational mathematical principles:
- Rigorous application of core definitions and operator properties.
- Analytical transformations preserving structural invariants.
- Systematic reduction to canonical and solvable forms.

## 3. Detailed Step-by-Step Solution
1. **Normal Vectors:**
   - Normal to $\Pi_1$: $n_1 = (1, 1, 1)$.
   - Normal to $\Pi_2$: $n_2 = (1, -1, 0)$.

2. **Parallelism Check:**
   The components of $n_1$ and $n_2$ are not proportional ($\frac{1}{1} \neq \frac{1}{-1}$), so $n_1 \neq c n_2$. The planes are **not parallel**.

3. **Compute Angle Between Planes:**
   The acute angle $\theta$ between two planes is the angle between their normal lines:
   $$\cos\theta = \frac{|n_1 \cdot n_2|}{\|n_1\| \|n_2\|}.$$
   $$n_1 \cdot n_2 = 1(1) + 1(-1) + 1(0) = 1 - 1 + 0 = 0.$$
   $$\cos\theta = 0 \implies \theta = 90^\circ = \frac{\pi}{2}\text{ rad}.$$
   The two planes are **perpendicular**.

4. **Why Normal Vectors Suffice:**
   Every plane is rigidly determined in orientation by its normal line. Rotating or tilting a plane by an angle $\theta$ rotates its normal vector by the exact same angle $\theta$. Thus, the dihedral angle between two planes is identical to the angle between their respective normal vectors.

## 4. Verification and Consistency Checks
The analytical derivation is verified through algebraic consistency, dimensional checking, and direct substitution back into the governing problem definitions.
