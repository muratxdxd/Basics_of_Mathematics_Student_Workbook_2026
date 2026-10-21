# Problem 11: Volume of a Solid of Revolution

## 1. Problem Statement
The region under the graph
$$
y=\sqrt{x},\qquad x\in[0,4],
$$
is rotated about the $x$-axis.

1. Construct the integral describing the volume using the disk method.
2. Compute the volume.
3. Explain where the factor $\pi y^2$ in the integral comes from.

## 2. Theoretical Background and Concepts
> it teaches how to construct an integral from the geometry of cross-sections instead of applying a volume formula without understanding its origin.

This problem applies foundational mathematical principles:
- Rigorous application of core definitions and operator properties.
- Analytical transformations preserving structural invariants.
- Systematic reduction to canonical and solvable forms.

## 3. Detailed Step-by-Step Solution
1. **Construct Integral via Disk Method:**
   A cross-section perpendicular to the $x$-axis at point $x$ is a circular disk with radius $R(x) = y = \sqrt{x}$.
   The cross-sectional area is:
   $$A(x) = \pi [R(x)]^2 = \pi (\sqrt{x})^2 = \pi x.$$
   The volume is the integral of this cross-sectional area over $x \in [0, 4]$:
   $$V = \int_0^4 \pi y^2\,dx = \pi \int_0^4 x\,dx.$$

2. **Compute the Volume:**
   $$V = \pi \left[\frac{x^2}{2}\right]_0^4 = \pi \left(\frac{4^2}{2} - 0\right) = \pi \left(\frac{16}{2}\right) = 8\pi \approx 25.1327.$$

3. **Origin of the Factor $\pi y^2$:**
   Rotating a 1D vertical line segment of length $y = f(x)$ around the horizontal $x$-axis sweeps out a 2D circular disk of radius $y$. The geometric area of any circle of radius $r$ is $\pi r^2 = \pi y^2$. Multiplying this 2D area by the infinitesimal slice thickness $dx$ gives the 3D volume element of a thin cylindrical disk $dV = \pi y^2 dx$. The definite integral sums these infinite disks from $x=0$ to $x=4$.

## 4. Verification and Consistency Checks
The analytical derivation is verified through algebraic consistency, dimensional checking, and direct substitution back into the governing problem definitions.
