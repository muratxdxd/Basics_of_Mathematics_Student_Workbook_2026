# Problem 4: Plane Through Three Points

## 1. Problem Statement
Find the equation of the plane through
$$A=(1,0,0),\quad B=(0,1,0),\quad C=(0,0,1).$$
First construct two vectors lying in the plane, and then use the cross product. Check the resulting equation on all three points.

## 2. Theoretical Background and Concepts
> connects earlier vector tools with constructing the equation of a plane.

This problem applies foundational mathematical principles:
- Rigorous application of core definitions and operator properties.
- Analytical transformations preserving structural invariants.
- Systematic reduction to canonical and solvable forms.

## 3. Detailed Step-by-Step Solution
1. **Construct Two In-Plane Vectors:**
   $$u = \overrightarrow{AB} = B - A = (0 - 1, 1 - 0, 0 - 0) = (-1, 1, 0).$$
   $$v = \overrightarrow{AC} = C - A = (0 - 1, 0 - 0, 1 - 0) = (-1, 0, 1).$$

2. **Normal Vector via Cross Product:**
   $$n = u \times v = \det\begin{pmatrix}i & j & k \\ -1 & 1 & 0 \\ -1 & 0 & 1\end{pmatrix} = i(1\cdot 1 - 0) - j(-1\cdot 1 - 0) + k(0 - (-1)(1)) = (1, 1, 1).$$
   The vectors $u$ and $v$ are independent directions in the plane. Their cross product is perpendicular to both, so $n$ is a normal vector to the plane.

3. **Plane Equation:**
   Let $X=(x,y,z)$ be any point in the plane. Its displacement $X-A$ lies in the plane, so it is perpendicular to the normal $n$; hence $n\cdot(X-A)=0$. Using $A=(1,0,0)$ and $n=(1,1,1)$:
   $$1(x - 1) + 1(y - 0) + 1(z - 0) = 0 \implies x + y + z - 1 = 0 \iff x + y + z = 1.$$

## 4. Verification and Consistency Checks
4. **Verification on All Three Points:**
   Substituting each required point into the plane equation checks that all three lie on the plane:
   - Point $A(1, 0, 0)$: $1 + 0 + 0 = 1$ (holds).
   - Point $B(0, 1, 0)$: $0 + 1 + 0 = 1$ (holds).
   - Point $C(0, 0, 1)$: $0 + 0 + 1 = 1$ (holds).
