# Lines and Planes

## Goal of the Set

After completing this set, the student should be able to describe lines and planes using points, direction vectors, and normal vectors; move between the most important forms of equations; analyze the relative position of geometric objects; and compute intersections, angles, distances, and projections.

The set deliberately combines material on lines, planes, and line–plane relationships. The goal is not to master separate catalogs of formulas, but to recognize the common vector geometry behind them.

## Basic Exercises

### Exercise 1. Line Through Two Points
Find the equation of the line through $A=(1,2)$ and $B=(4,-1)$ in parametric and general form. Identify a direction vector and an example of a normal vector. Check that both points satisfy the equation you obtain.

> **Why this exercise:** teaches how to move between equivalent descriptions of a line and connect them with the appropriate vectors.

#### Solution

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

5. **Verification:**
   - For $A(1, 2)$: $1 + 2 - 3 = 0$ (holds).
   - For $B(4, -1)$: $4 + (-1) - 3 = 0$ (holds).

---

### Exercise 2. A Line in Space
Given
$$L:(x,y,z)=(2,-1,3)+t(1,2,-2).$$
State a point on the line and its direction vector, check whether $P=(4,3,-1)$ lies on $L$, and find the point corresponding to $t=-1$.

> **Why this exercise:** reinforces the interpretation of parametric form as “point + direction.”

#### Solution

1. **Base Point and Direction Vector:**
   - Base point (for $t=0$): $P_0 = (2, -1, 3)$.
   - Direction vector: $v = (1, 2, -2)$.

2. **Check whether $P = (4, 3, -1)$ lies on $L$:**
   Set the coordinates equal to $(2+t, -1+2t, 3-2t)$:
   - $x$-coordinate: $2 + t = 4 \implies t = 2$.
   - $y$-coordinate: $-1 + 2t = 3 \implies 2t = 4 \implies t = 2$.
   - $z$-coordinate: $3 - 2t = -1 \implies -2t = -4 \implies t = 2$.
   Since $t = 2$ consistently satisfies all three coordinate equations, **$P$ lies on line $L$**.

3. **Point corresponding to $t = -1$:**
   $$(x, y, z) = (2 + (-1)(1), -1 + (-1)(2), 3 + (-1)(-2)) = (2 - 1, -1 - 2, 3 + 2) = (1, -3, 5).$$

---

### Exercise 3. Plane Through a Point with a Given Normal Vector
Find the equation of the plane through $P=(1,-2,3)$ and perpendicular to $n=(2,1,-1)$. Check the result by substituting the point $P$ and explain the role of the normal vector.

> **Why this exercise:** shows the basic construction of a plane from a point and a normal vector.

#### Solution

1. **Equation of the Plane:**
   A point $(x, y, z)$ lies in the plane if and only if the displacement vector from $P$ to $(x, y, z)$ is orthogonal to the normal vector $n$:
   $$n \cdot \begin{pmatrix}x - x_0 \\ y - y_0 \\ z - z_0\end{pmatrix} = 0.$$
   $$2(x - 1) + 1(y - (-2)) - 1(z - 3) = 0$$
   $$2x - 2 + y + 2 - z + 3 = 0 \implies 2x + y - z + 3 = 0.$$

2. **Check with Point $P(1, -2, 3)$:**
   $$2(1) + (-2) - (3) + 3 = 2 - 2 - 3 + 3 = 0.$$
   The equation is satisfied.

3. **Role of the Normal Vector:**
   The normal vector $n$ establishes the spatial tilt and orientation of the plane. Any vector lying entirely within the plane is orthogonal to $n$. Once the orientation is fixed by $n$, specifying the point $P$ fixes the plane's precise position in space.

---

### Exercise 4. Plane Through Three Points
Find the equation of the plane through
$$A=(1,0,0),\quad B=(0,1,0),\quad C=(0,0,1).$$
First construct two vectors lying in the plane, and then use the cross product. Check the resulting equation on all three points.

> **Why this exercise:** connects earlier vector tools with constructing the equation of a plane.

#### Solution

1. **Construct Two In-Plane Vectors:**
   $$u = \overrightarrow{AB} = B - A = (0 - 1, 1 - 0, 0 - 0) = (-1, 1, 0).$$
   $$v = \overrightarrow{AC} = C - A = (0 - 1, 0 - 0, 1 - 0) = (-1, 0, 1).$$

2. **Normal Vector via Cross Product:**
   $$n = u \times v = \det\begin{pmatrix}i & j & k \\ -1 & 1 & 0 \\ -1 & 0 & 1\end{pmatrix} = i(1\cdot 1 - 0) - j(-1\cdot 1 - 0) + k(0 - (-1)(1)) = (1, 1, 1).$$

3. **Plane Equation:**
   Using point $A(1, 0, 0)$:
   $$1(x - 1) + 1(y - 0) + 1(z - 0) = 0 \implies x + y + z - 1 = 0 \iff x + y + z = 1.$$

4. **Verification on All Three Points:**
   - Point $A(1, 0, 0)$: $1 + 0 + 0 = 1$ (holds).
   - Point $B(0, 1, 0)$: $0 + 1 + 0 = 1$ (holds).
   - Point $C(0, 0, 1)$: $0 + 0 + 1 = 1$ (holds).

---

### Exercise 5. Relative Position of Two Lines
Analyze the position of
$$L_1:(x,y,z)=(1,1,0)+t(1,2,1),$$
$$L_2:(x,y,z)=(2,0,1)+s(0,1,-1).$$
If they intersect, give the intersection point. If not, determine whether they are parallel or skew. Justify the classification.

> **Why this exercise:** teaches how to distinguish qualitatively different relationships between lines in space.

#### Solution

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

---

### Exercise 6. Angle Between Planes
Given
$$\Pi_1:x+y+z=1,\qquad \Pi_2:x-y=2.$$
First use the normal vectors to decide whether the planes are parallel. If not, compute the angle between them and explain why the normal vectors alone are enough for this calculation.

> **Why this exercise:** focuses attention on one mechanism—using normals to analyze position and angle—without also introducing the construction of the intersection line.

#### Solution

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

---

### Exercise 7. A Line Relative to a Plane
For
$$L:(x,y,z)=(1,1,0)+t(1,-1,0),\qquad \Pi:x+y+z=2,$$
determine whether the line intersects the plane at one point, is parallel to it, or lies in it. Explain the role of the dot product of the direction vector and the normal vector.

> **Why this exercise:** builds a universal test for the relative position of a line and a plane.

#### Solution

1. **Vectors:**
   - Line direction: $v = (1, -1, 0)$.
   - Plane normal: $n = (1, 1, 1)$.

2. **Dot Product Test:**
   $$v \cdot n = 1(1) + (-1)(1) + 0(1) = 1 - 1 + 0 = 0.$$
   - **Role of the dot product:** $v \cdot n$ measures whether the direction of the line has any component along the plane's normal.
     - If $v \cdot n \neq 0$, the line pierces the plane at a single unique point.
     - If $v \cdot n = 0$, the line direction is orthogonal to the normal, which means the line is parallel to the plane.

3. **Determine if the Line Lies in the Plane:**
   Check whether the line's base point $P_0(1, 1, 0)$ satisfies the plane equation:
   $$x + y + z = 1 + 1 + 0 = 2.$$
   The base point lies on the plane.
   Since the line is parallel to the plane and shares at least one point with it, the **entire line lies in the plane**.

---

### Exercise 8. Intersection Point of a Line and a Plane
Find the intersection point of
$$(x,y,z)=(1,0,2)+t(1,2,-1)$$
with the plane $x+y+z=4$. Check the result by substituting it into both descriptions.

> **Why this exercise:** practices the most important computational case of the line–plane relationship.

#### Solution

1. **Substitute Parametric Coordinates into Plane Equation:**
   $$x = 1 + t, \qquad y = 2t, \qquad z = 2 - t.$$
   $$(1 + t) + (2t) + (2 - t) = 4.$$
   $$3 + 2t = 4 \implies 2t = 1 \implies t = \frac{1}{2} = 0.5.$$

2. **Compute the Intersection Point:**
   $$x = 1 + 0.5 = 1.5 = \frac{3}{2},$$
   $$y = 2(0.5) = 1,$$
   $$z = 2 - 0.5 = 1.5 = \frac{3}{2}.$$
   Intersection point: $P = \left(\frac{3}{2}, 1, \frac{3}{2}\right) = (1.5, 1, 1.5)$.

3. **Verification:**
   - **On the line:** For $t = 0.5$, $(1, 0, 2) + 0.5(1, 2, -1) = (1.5, 1, 1.5)$ (matches).
   - **In the plane:** $1.5 + 1 + 1.5 = 4$ (holds).

---

### Exercise 9. Distances
Compute:
1. the distance from $P=(2,3)$ to the line $3x+4y-10=0$,
2. the distance from $Q=(2,-1,3)$ to the plane $2x-2y+z-4=0$.

Compare the two formulas and explain their common connection with the normal direction.

> **Why this exercise:** organizes two similar formulas through one geometric idea.

#### Solution

1. **Distance from Point to Line in $\mathbb{R}^2$:**
   $$d(P, L) = \frac{|A x_0 + B y_0 + C|}{\sqrt{A^2 + B^2}} = \frac{|3(2) + 4(3) - 10|}{\sqrt{3^2 + 4^2}} = \frac{|6 + 12 - 10|}{\sqrt{25}} = \frac{8}{5} = 1.6.$$

2. **Distance from Point to Plane in $\mathbb{R}^3$:**
   $$d(Q, \Pi) = \frac{|A x_0 + B y_0 + C z_0 + D|}{\sqrt{A^2 + B^2 + C^2}} = \frac{|2(2) - 2(-1) + 1(3) - 4|}{\sqrt{2^2 + (-2)^2 + 1^2}} = \frac{|4 + 2 + 3 - 4|}{\sqrt{4 + 4 + 1}} = \frac{5}{\sqrt{9}} = \frac{5}{3} \approx 1.667.$$

3. **Comparison and Common Connection:**
   Both formulas are instances of the exact same geometric projection:
   $$d = \frac{|\overrightarrow{P_0 P} \cdot n|}{\|n\|} = \left| \overrightarrow{P_0 P} \cdot \frac{n}{\|n\|} \right|.$$
   The shortest distance from a point to a hyperplane (a line in 2D or a plane in 3D) is measured along the perpendicular path, which is parallel to the normal vector $n$. The formula computes the scalar projection of the displacement vector onto the unit normal vector $\hat{n} = \frac{n}{\|n\|}$.

---

### Exercise 10. Projection of a Point onto a Plane
Find the orthogonal projection of $P=(2,1,3)$ onto the plane $x+y+z=3$, and then find the reflection of $P$ across this plane. Check that the midpoint of the segment joining the point and its reflection lies on the plane.

> **Why this exercise:** combines the normal, intersection, and distance into the construction of a projection and reflection.

#### Solution

1. **Orthogonal Projection $P_0$:**
   The line through $P(2, 1, 3)$ perpendicular to the plane has direction $n = (1, 1, 1)$:
   $$(x, y, z) = (2 + t, 1 + t, 3 + t).$$
   Substitute into $x + y + z = 3$:
   $$(2 + t) + (1 + t) + (3 + t) = 3 \implies 6 + 3t = 3 \implies 3t = -3 \implies t = -1.$$
   Thus, the projection point is:
   $$P_0 = (2 + (-1), 1 + (-1), 3 + (-1)) = (1, 0, 2).$$

2. **Reflection $P'$ Across the Plane:**
   The reflected point corresponds to stepping twice the distance along the normal line ($t = 2(-1) = -2$):
   $$P' = (2 - 2, 1 - 2, 3 - 2) = (0, -1, 1).$$

3. **Midpoint Verification:**
   $$M = \frac{P + P'}{2} = \left(\frac{2 + 0}{2}, \frac{1 + (-1)}{2}, \frac{3 + 1}{2}\right) = (1, 0, 2) = P_0.$$
   Substitute $M(1, 0, 2)$ into the plane equation:
   $$1 + 0 + 2 = 3.$$
   The midpoint coincides with the projection $P_0$ and lies on the plane.

---

## More Challenging Exercises

### Exercise 11. Plane Containing a Line and a Point
Find the equation of the plane containing
$$(x,y,z)=(1,0,2)+t(1,1,-1)$$
and the point $P=(0,2,1)$. Check that both the entire line and the point lie in the plane you obtain.

> **Why this exercise:** requires independently constructing two linearly independent directions in the plane.

#### Solution

1. **Construct Two In-Plane Vectors:**
   - Direction of the line: $v_1 = (1, 1, -1)$.
   - Base point of the line: $Q = (1, 0, 2)$.
   - Vector from $Q$ to $P(0, 2, 1)$:
     $$v_2 = P - Q = (0 - 1, 2 - 0, 1 - 2) = (-1, 2, -1).$$

2. **Normal Vector via Cross Product:**
   $$n = v_1 \times v_2 = \det\begin{pmatrix}i & j & k \\ 1 & 1 & -1 \\ -1 & 2 & -1\end{pmatrix} = i(1(-1) - (-1)(2)) - j(1(-1) - (-1)(-1)) + k(1(2) - 1(-1))$$
   $$= i(-1 + 2) - j(-1 - 1) + k(2 + 1) = 1i + 2j + 3k = (1, 2, 3).$$

3. **Plane Equation:**
   Using point $Q(1, 0, 2)$:
   $$1(x - 1) + 2(y - 0) + 3(z - 2) = 0 \implies x - 1 + 2y + 3z - 6 = 0 \implies x + 2y + 3z - 7 = 0.$$

4. **Verification:**
   - **Point $P(0, 2, 1)$:** $0 + 2(2) + 3(1) - 7 = 4 + 3 - 7 = 0$ (holds).
   - **Entire line:** Substitute $(1 + t, t, 2 - t)$:
     $$(1 + t) + 2(t) + 3(2 - t) - 7 = 1 + t + 2t + 6 - 3t - 7 = 0 \quad \text{for all } t \in \mathbb{R}.$$
   Both the line and the point lie on the plane.

---

### Exercise 12. Intersection Line of Two Planes
Find a parametric equation of the line that is the intersection of
$$x+y+z=3,\qquad x-y+z=1.$$
Find its direction vector in two ways: from the system of equations and from the cross product of the normal vectors. Compare the results.

> **Why this exercise:** shows the equivalence of the algebraic and geometric approaches to constructing an intersection line.

#### Solution

1. **Method 1: From the System of Equations:**
   Add the two equations:
   $$(x + y + z) + (x - y + z) = 3 + 1 \implies 2x + 2z = 4 \implies x + z = 2 \implies x = 2 - z.$$
   Subtract the second equation from the first:
   $$(x + y + z) - (x - y + z) = 3 - 1 \implies 2y = 2 \implies y = 1.$$
   Setting $z = t \in \mathbb{R}$ as the parameter:
   $$\begin{pmatrix}x\\y\\z\end{pmatrix} = \begin{pmatrix}2 - t \\ 1 \\ t\end{pmatrix} = \begin{pmatrix}2\\1\\0\end{pmatrix} + t\begin{pmatrix}-1\\0\\1\end{pmatrix}.$$
   Direction vector: $v_1 = (-1, 0, 1)$.

2. **Method 2: Cross Product of Normal Vectors:**
   Normal vectors: $n_1 = (1, 1, 1)$ and $n_2 = (1, -1, 1)$.
   $$v_2 = n_1 \times n_2 = \det\begin{pmatrix}i & j & k \\ 1 & 1 & 1 \\ 1 & -1 & 1\end{pmatrix} = i(1 - (-1)) - j(1 - 1) + k(-1 - 1) = (2, 0, -2).$$
   Simplifying by factoring out $-2$: $v_2 = -2(-1, 0, 1) \sim (-1, 0, 1)$.

3. **Comparison:**
   Both methods yield collinear direction vectors: $v_2 = -2 v_1$. The line is parallel to both planes, meaning its direction vector must be simultaneously perpendicular to both normal vectors, precisely defining the cross product $n_1 \times n_2$.

---

### Exercise 13. Closest Point on a Plane
Find the point on the plane $x+2y+2z=4$ closest to $P=(3,0,0)$. Give the distance and check that the segment joining the two points is perpendicular to the plane.

> **Why this exercise:** combines projection, distance, and the normal direction in one problem.

#### Solution

1. **Find Closest Point $Q$:**
   The closest point is the orthogonal projection of $P$ onto the plane.
   Normal vector: $n = (1, 2, 2)$.
   Normal line through $P(3, 0, 0)$:
   $$(x, y, z) = (3 + t, 2t, 2t).$$
   Substitute into plane equation:
   $$(3 + t) + 2(2t) + 2(2t) = 4 \implies 3 + 9t = 4 \implies 9t = 1 \implies t = \frac{1}{9}.$$
   Closest point:
   $$Q = \left(3 + \frac{1}{9}, \frac{2}{9}, \frac{2}{9}\right) = \left(\frac{28}{9}, \frac{2}{9}, \frac{2}{9}\right).$$

2. **Distance:**
   $$d(P, \Pi) = \frac{|1(3) + 2(0) + 2(0) - 4|}{\sqrt{1^2 + 2^2 + 2^2}} = \frac{|-1|}{\sqrt{9}} = \frac{1}{3}.$$

3. **Perpendicularity Check:**
   Displacement segment:
   $$\overrightarrow{PQ} = Q - P = \left(\frac{28}{9} - 3, \frac{2}{9} - 0, \frac{2}{9} - 0\right) = \left(\frac{1}{9}, \frac{2}{9}, \frac{2}{9}\right) = \frac{1}{9}(1, 2, 2) = \frac{1}{9}n.$$
   Since $\overrightarrow{PQ}$ is a scalar multiple of the normal vector $n$, the line segment connecting $P$ and $Q$ is perpendicular to the plane.

---

### Exercise 14. Contrast: Intersection and Parallelism
From the point $P=(0,0,1)$, two lines are drawn with direction vectors
$$v_1=(2,1,-1),\qquad v_2=(2,1,0).$$
For each line, analyze its position relative to the plane $z=0$.

For the line that intersects the plane, find the intersection point. For the other line, explain how you can recognize parallelism without solving an equation.

> **Why this exercise:** compares two very similar data sets that lead to different outcomes and forces recognition of the geometric condition before calculation.

#### Solution

1. **Relative Position to the Plane $z = 0$ ($n = (0, 0, 1)$):**
   - **Line 1 ($v_1 = (2, 1, -1)$):**
     $$v_1 \cdot n = 2(0) + 1(0) + (-1)(1) = -1 \neq 0.$$
     Because $v_1 \cdot n \neq 0$, Line 1 is not parallel to the plane and **intersects the plane at exactly one point**.
   - **Line 2 ($v_2 = (2, 1, 0)$):**
     $$v_2 \cdot n = 2(0) + 1(0) + 0(1) = 0.$$
     Because $v_2 \cdot n = 0$, Line 2 is **parallel to the plane**.

2. **Intersection Point for Line 1:**
   Parametric form: $(x, y, z) = (0, 0, 1) + t(2, 1, -1) = (2t, t, 1-t)$.
   Intersection with $z = 0$:
   $$1 - t = 0 \implies t = 1.$$
   Intersection point:
   $$(x, y, z) = (2(1), 1, 1 - 1) = (2, 1, 0).$$

3. **Recognizing Parallelism for Line 2 Without Solving:**
   The $z$-component of direction vector $v_2$ is $0$. This means that along Line 2, the rate of change of $z$ is zero: $\Delta z = 0 \cdot t = 0$. Since the line originates at $P(0, 0, 1)$, every single point on Line 2 has $z = 1$. The plane is $z = 0$. Since $1 \neq 0$, the line maintains a constant vertical distance of $1$ from the plane and can never intersect it.

---

### Exercise 15. Complete Classification of a Line Relative to a Plane
Let
$$L:p+tv,\qquad \Pi:n\cdot x=d.$$
State the conditions distinguishing the three cases: one intersection point, parallel with no common points, and the line contained in the plane. Then illustrate each case with your own simple numerical example.

> **Why this exercise:** requires formulating a general mathematical criterion instead of carrying out one isolated calculation.

#### Solution

1. **General Mathematical Criteria:**
   Substituting $L$ into $\Pi$ gives $n \cdot (p + tv) = d \implies (n \cdot v) t = d - n \cdot p$.
   - **Case 1: One unique intersection point.**
     Condition: $n \cdot v \neq 0$.
     The parameter is uniquely determined: $t = \frac{d - n \cdot p}{n \cdot v}$.
   - **Case 2: Parallel with no common points ($L \cap \Pi = \emptyset$).**
     Condition: $n \cdot v = 0$ and $n \cdot p \neq d$.
     The equation becomes $0 \cdot t = \text{non-zero}$, which has no solution.
   - **Case 3: Line contained in the plane ($L \subset \Pi$).**
     Condition: $n \cdot v = 0$ and $n \cdot p = d$.
     The equation becomes $0 \cdot t = 0$, which holds for every $t \in \mathbb{R}$.

2. **Numerical Examples:**
   Let the plane be $\Pi: z = 0$, so $n = (0, 0, 1)$ and $d = 0$.
   - **Example 1 (Unique intersection):**
     $p = (0, 0, 1)$, $v = (0, 0, 1)$.
     $n \cdot v = 1 \neq 0$. Intersection occurs at $t = -1 \implies (0, 0, 0)$.
   - **Example 2 (Parallel, no intersection):**
     $p = (0, 0, 1)$, $v = (1, 0, 0)$.
     $n \cdot v = 0$, but $n \cdot p = 1 \neq 0$. The line lies at elevation $z = 1$, strictly parallel to $z = 0$.
   - **Example 3 (Line contained in the plane):**
     $p = (1, 1, 0)$, $v = (1, 0, 0)$.
     $n \cdot v = 0$ and $n \cdot p = 0 = d$. The line lies entirely within the plane $z = 0$.
