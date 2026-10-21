# Vectors

## Goal of the Set

After completing this set, the student should be comfortable performing vector operations in $\mathbb R^2$ and $\mathbb R^3$, understand length, angle, dot product, cross product, projection, and linear dependence. Vectors should be treated both computationally and geometrically.

Giving only the final result is not a complete solution. In every exercise, the student should show **which mechanism is being used**, and whenever possible, check the result or give it a geometric interpretation.

## Basic Exercises

### Exercise 1. Vector Operations and Their Meaning
For $u=(2,-1,3)$ and $v=(-1,4,2)$ compute
$$u+v,\qquad u-v,\qquad 3u-2v.$$
Then verify that $(u+v)-v=u$, and explain geometrically what adding two vectors means.

> **Why this exercise:** reinforces basic operations and immediately connects them with their geometric meaning.

#### Solution

1. **Computations:**
   $$u+v = (2 + (-1), -1 + 4, 3 + 2) = (1, 3, 5).$$
   $$u-v = (2 - (-1), -1 - 4, 3 - 2) = (3, -5, 1).$$
   $$3u - 2v = 3(2, -1, 3) - 2(-1, 4, 2) = (6, -3, 9) - (-2, 8, 4) = (6 - (-2), -3 - 8, 9 - 4) = (8, -11, 5).$$

2. **Verification of $(u+v)-v = u$:**
   $$(u+v)-v = (1, 3, 5) - (-1, 4, 2) = (1 - (-1), 3 - 4, 5 - 2) = (2, -1, 3) = u.$$
   The identity holds.

3. **Geometric Meaning of Addition:**
   Geometrically, adding vectors corresponds to the triangle rule or parallelogram rule: place the initial point (tail) of $v$ at the terminal point (tip) of $u$. The sum $u+v$ is the vector running from the tail of $u$ directly to the tip of $v$, representing the combined resultant displacement.

---

### Exercise 2. Distance as the Length of a Vector
The points are $A=(1,2,3)$ and $B=(4,-2,6)$.

1. Construct $\overrightarrow{AB}$.
2. Compute its length.
3. Compute the distance between the points using the coordinate formula.
4. Explain why both calculations give the same result.

> **Why this exercise:** shows that the point-distance formula comes directly from the length of a difference vector.

#### Solution

1. **Construct $\overrightarrow{AB}$:**
   $$\overrightarrow{AB} = B - A = (4 - 1, -2 - 2, 6 - 3) = (3, -4, 3).$$

2. **Compute its Length:**
   $$\|\overrightarrow{AB}\| = \sqrt{3^2 + (-4)^2 + 3^2} = \sqrt{9 + 16 + 9} = \sqrt{34}.$$

3. **Compute Distance Using Coordinate Formula:**
   $$d(A, B) = \sqrt{(x_B - x_A)^2 + (y_B - y_A)^2 + (z_B - z_A)^2} = \sqrt{(4-1)^2 + (-2-2)^2 + (6-3)^2} = \sqrt{3^2 + (-4)^2 + 3^2} = \sqrt{34}.$$

4. **Why Both Give the Same Result:**
   The displacement vector $\overrightarrow{AB}$ has components precisely equal to the coordinate differences $(\Delta x, \Delta y, \Delta z) = (x_B-x_A, y_B-y_A, z_B-z_A)$. By the Pythagorean Theorem in 3D Euclidean space, the straight-line distance between two points is defined as the magnitude of this displacement vector, so $d(A, B) = \|\overrightarrow{AB}\| = \sqrt{34}$.

---

### Exercise 3. Vector Normalization
For $v=(3,4)$ find a unit vector $e$ with the same direction and orientation. Check that $\|e\|=1$, reconstruct $v$ in the form $v=\|v\|e$, and explain what changes during normalization and what remains unchanged.

> **Why this exercise:** teaches how to separate direction from vector length.

#### Solution

1. **Compute Length:**
   $$\|v\| = \sqrt{3^2 + 4^2} = \sqrt{9 + 16} = \sqrt{25} = 5.$$

2. **Unit Vector $e$:**
   $$e = \frac{v}{\|v\|} = \frac{1}{5}(3, 4) = \left(\frac{3}{5}, \frac{4}{5}\right) = (0.6, 0.8).$$

3. **Check $\|e\| = 1$:**
   $$\|e\| = \sqrt{\left(\frac{3}{5}\right)^2 + \left(\frac{4}{5}\right)^2} = \sqrt{\frac{9}{25} + \frac{16}{25}} = \sqrt{\frac{25}{25}} = 1.$$

4. **Reconstruct $v$:**
   $$\|v\|e = 5 \left(\frac{3}{5}, \frac{4}{5}\right) = (3, 4) = v.$$

5. **What Changes and What Remains Unchanged:**
   - **What changes:** The length (magnitude) is scaled from $5$ to exactly $1$.
   - **What remains unchanged:** The line of action (direction) and the pointing sense (orientation along the line) remain completely identical, as $e$ is a positive scalar multiple of $v$.

---

### Exercise 4. Dot Product and Perpendicularity
For $u=(1,2,-1)$ and $v=(2,-1,3)$ compute $u\cdot v$ and determine whether the vectors are perpendicular. Then find $a$ so that $w=(2,-1,a)$ is perpendicular to $u$, and check the result.

> **Why this exercise:** shows the dot product as both a test and a tool for constructing a perpendicularity condition.

#### Solution

1. **Compute $u \cdot v$:**
   $$u \cdot v = 1(2) + 2(-1) + (-1)(3) = 2 - 2 - 3 = -3.$$
   Since $u \cdot v = -3 \neq 0$, the vectors are **not perpendicular** (their dot product is negative, meaning the angle between them is obtuse).

2. **Find $a$ so that $w = (2, -1, a) \perp u$:**
   Perpendicularity condition: $u \cdot w = 0$.
   $$1(2) + 2(-1) + (-1)(a) = 0 \implies 2 - 2 - a = 0 \implies -a = 0 \implies a = 0.$$
   So $w = (2, -1, 0)$.

3. **Verification:**
   $$u \cdot w = 1(2) + 2(-1) + (-1)(0) = 2 - 2 + 0 = 0.$$
   The vectors $u$ and $w$ are strictly perpendicular.

---

### Exercise 5. Angle Between Vectors
Given $u=(1,1,0)$ and $v=(1,0,1)$:

1. Use the sign of $u\cdot v$ to predict the type of angle.
2. Compute the angle.
3. Compare the result with the prediction.

> **Why this exercise:** teaches how to extract qualitative information first and only then perform the exact calculation.

#### Solution

1. **Predict Type of Angle from Sign of $u \cdot v$:**
   $$u \cdot v = 1(1) + 1(0) + 0(1) = 1.$$
   Since $u \cdot v > 0$, $\cos\theta = \frac{u \cdot v}{\|u\|\|v\|} > 0$. Therefore, the angle $\theta$ must be **acute** ($0^\circ \le \theta < 90^\circ$).

2. **Compute the Exact Angle:**
   $$\|u\| = \sqrt{1^2 + 1^2 + 0^2} = \sqrt{2}, \qquad \|v\| = \sqrt{1^2 + 0^2 + 1^2} = \sqrt{2}.$$
   $$\cos\theta = \frac{u \cdot v}{\|u\|\|v\|} = \frac{1}{\sqrt{2}\sqrt{2}} = \frac{1}{2}.$$
   $$\theta = \arccos\left(\frac{1}{2}\right) = 60^\circ = \frac{\pi}{3}\text{ rad}.$$

3. **Comparison:**
   The angle $60^\circ$ is strictly between $0^\circ$ and $90^\circ$, matching the acute angle prediction.

---

### Exercise 6. Projection and Perpendicular Component
Find the projection of $u=(4,2)$ onto the direction $v=(1,1)$. Then compute
$$r=u-\operatorname{proj}_v u$$
and verify that $r\cdot v=0$. Explain this result geometrically.

> **Why this exercise:** shows projection as a decomposition into parallel and perpendicular components.

#### Solution

1. **Compute Projection $\operatorname{proj}_v u$:**
   $$\operatorname{proj}_v u = \frac{u \cdot v}{\|v\|^2} v.$$
   $$u \cdot v = 4(1) + 2(1) = 6, \qquad \|v\|^2 = 1^2 + 1^2 = 2.$$
   $$\operatorname{proj}_v u = \frac{6}{2}(1, 1) = 3(1, 1) = (3, 3).$$

2. **Compute Perpendicular Component $r$:**
   $$r = u - \operatorname{proj}_v u = (4, 2) - (3, 3) = (1, -1).$$

3. **Verify $r \cdot v = 0$:**
   $$r \cdot v = 1(1) + (-1)(1) = 1 - 1 = 0.$$

4. **Geometric Explanation:**
   The vector $u$ is decomposed into two orthogonal components: $u = \operatorname{proj}_v u + r$. The projection $\operatorname{proj}_v u$ is the orthogonal shadow of $u$ along the line defined by $v$. The vector $r$ connects the tip of the shadow to the tip of $u$; by construction of orthogonal projection, this connecting segment must be strictly perpendicular to the direction line $v$.

---

### Exercise 7. Linear Dependence Without Heavy Computation
Given
$$u=(1,2,3),\qquad v=(2,4,6),\qquad w=(0,1,1).$$
Identify a specific relation between $u$ and $v$, decide whether the three vectors can be linearly independent, and explain why no long calculation is needed.

> **Why this exercise:** develops the habit of recognizing structure before applying a computational procedure.

#### Solution

1. **Relation Between $u$ and $v$:**
   $$v = (2, 4, 6) = 2(1, 2, 3) = 2u.$$
   Vector $v$ is an exact scalar multiple of $u$.

2. **Linear Independence Decision:**
   The three vectors **cannot be linearly independent**; they are **linearly dependent**.

3. **Explanation (No heavy computation needed):**
   By definition, vectors are linearly dependent if there exists a linear combination $c_1 u + c_2 v + c_3 w = 0$ with not all coefficients zero.
   Setting $c_1 = 2$, $c_2 = -1$, and $c_3 = 0$:
   $$2u - 1v + 0w = (2, 4, 6) - (2, 4, 6) + (0, 0, 0) = (0, 0, 0).$$
   Since a non-trivial linear combination vanishes, the entire set is linearly dependent. Any set containing collinear vectors is automatically dependent.

---

### Exercise 8. Linear Combination and Checking the Result
Check whether $w=(5,1)$ can be written as
$$w=au+bv,$$
where $u=(1,1)$ and $v=(2,-1)$. If so, find $a,b$, reconstruct $w$ from them, and explain the geometric meaning of the existence of such coefficients.

> **Why this exercise:** connects linear combinations with the geometry of directions.

#### Solution

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

---

### Exercise 9. Cross Product as a Perpendicular Direction
For $u=(1,2,0)$ and $v=(0,1,3)$ compute $u\times v$. Use dot products to check perpendicularity to both vectors, compute $v\times u$, and compare the results.

> **Why this exercise:** teaches the geometric meaning of the cross product and the effect of changing the order of its arguments.

#### Solution

1. **Compute $u \times v$:**
   $$u \times v = \det\begin{pmatrix}i & j & k \\ 1 & 2 & 0 \\ 0 & 1 & 3\end{pmatrix} = i(2\cdot 3 - 0\cdot 1) - j(1\cdot 3 - 0\cdot 0) + k(1\cdot 1 - 2\cdot 0) = 6i - 3j + k = (6, -3, 1).$$

2. **Perpendicularity Checks via Dot Products:**
   $$(u \times v) \cdot u = 6(1) + (-3)(2) + 1(0) = 6 - 6 + 0 = 0.$$
   $$(u \times v) \cdot v = 6(0) + (-3)(1) + 1(3) = 0 - 3 + 3 = 0.$$
   Both dot products are zero, verifying that $u \times v$ is strictly perpendicular to both $u$ and $v$.

3. **Compute $v \times u$ and Compare:**
   $$v \times u = \det\begin{pmatrix}i & j & k \\ 0 & 1 & 3 \\ 1 & 2 & 0\end{pmatrix} = i(0 - 6) - j(0 - 3) + k(0 - 1) = (-6, 3, -1) = -(u \times v).$$
   The cross product is **anticommutative**: $v \times u = -(u \times v)$. Reversing the order of vectors reverses the direction of the resulting vector by the right-hand rule.

---

### Exercise 10. Triangle Area from Vectors
The points $A=(0,0,0)$, $B=(2,1,0)$, and $C=(1,3,2)$ form a triangle. Construct $\overrightarrow{AB}$ and $\overrightarrow{AC}$, compute the area of the parallelogram using the cross product, and then find the area of the triangle. Explain the factor $\frac12$.

> **Why this exercise:** shows the interpretation of the length of the cross product as area.

#### Solution

1. **Construct Vectors:**
   $$\overrightarrow{AB} = B - A = (2 - 0, 1 - 0, 0 - 0) = (2, 1, 0).$$
   $$\overrightarrow{AC} = C - A = (1 - 0, 3 - 0, 2 - 0) = (1, 3, 2).$$

2. **Cross Product $\overrightarrow{AB} \times \overrightarrow{AC}$:**
   $$\overrightarrow{AB} \times \overrightarrow{AC} = \det\begin{pmatrix}i & j & k \\ 2 & 1 & 0 \\ 1 & 3 & 2\end{pmatrix} = i(1\cdot 2 - 0\cdot 3) - j(2\cdot 2 - 0\cdot 1) + k(2\cdot 3 - 1\cdot 1) = (2, -4, 5).$$

3. **Area of Parallelogram:**
   $$\text{Area}_{\text{parallelogram}} = \|\overrightarrow{AB} \times \overrightarrow{AC}\| = \sqrt{2^2 + (-4)^2 + 5^2} = \sqrt{4 + 16 + 25} = \sqrt{45} = 3\sqrt{5}.$$

4. **Area of Triangle:**
   $$\text{Area}_{\Delta ABC} = \frac{1}{2} \|\overrightarrow{AB} \times \overrightarrow{AC}\| = \frac{3\sqrt{5}}{2} \approx 3.354.$$

5. **Explanation of the Factor $\frac{1}{2}$:**
   A parallelogram is divided into two congruent triangles by either of its diagonals. The triangle formed by vertices $A, B, C$ has base $\|\overrightarrow{AB}\|$ and height $h = \|\overrightarrow{AC}\|\sin\theta$. Its area is $\frac{1}{2}\text{base}\times\text{height}$, which is precisely half the area of the full parallelogram spanned by $\overrightarrow{AB}$ and $\overrightarrow{AC}$.

---

## More Challenging Exercises

### Exercise 11. Decomposition into Parallel and Perpendicular Components
Decompose $u=(3,4)$ into components parallel and perpendicular to $v=(1,2)$. Check
$$u=u_{\parallel}+u_{\perp},\qquad u_{\perp}\cdot v=0.$$
Explain why these are two independent checks of correctness.

> **Why this exercise:** deepens the idea of projection through construction and verification.

#### Solution

1. **Parallel Component $u_\parallel$:**
   $$u_\parallel = \operatorname{proj}_v u = \frac{u \cdot v}{\|v\|^2} v.$$
   $$u \cdot v = 3(1) + 4(2) = 11, \qquad \|v\|^2 = 1^2 + 2^2 = 5.$$
   $$u_\parallel = \frac{11}{5}(1, 2) = \left(\frac{11}{5}, \frac{22}{5}\right) = (2.2, 4.4).$$

2. **Perpendicular Component $u_\perp$:**
   $$u_\perp = u - u_\parallel = (3, 4) - \left(\frac{11}{5}, \frac{22}{5}\right) = \left(\frac{15-11}{5}, \frac{20-22}{5}\right) = \left(\frac{4}{5}, -\frac{2}{5}\right) = (0.8, -0.4).$$

3. **Verification Checks:**
   - **Check 1 (Sum consistency):**
     $$u_\parallel + u_\perp = (2.2, 4.4) + (0.8, -0.4) = (3.0, 4.0) = u.$$
   - **Check 2 (Orthogonality):**
     $$u_\perp \cdot v = \frac{4}{5}(1) + \left(-\frac{2}{5}\right)(2) = \frac{4}{5} - \frac{4}{5} = 0.$$

4. **Why These Are Two Independent Checks:**
   Check 1 verifies that the decomposition is complete and preserves the entire vector $u$ without any loss of magnitude or component. Check 2 verifies that $u_\perp$ is genuinely orthogonal to the subspace spanned by $v$. One could easily pick an incorrect vector that adds up to $u$ but fails orthogonality, or a vector that is orthogonal to $v$ but does not sum to $u$. Satisfying both proves uniqueness and correctness.

---

### Exercise 12. A Normal Vector to a Plane
Given $A=(1,0,2)$, $B=(2,1,0)$, and $C=(0,3,1)$. Construct two vectors lying in the plane, find a vector perpendicular to both, and check the perpendicularity using dot products.

> **Why this exercise:** creates a direct bridge from vectors to the description of a plane.

#### Solution

1. **Construct Two In-Plane Vectors:**
   $$u = \overrightarrow{AB} = B - A = (2 - 1, 1 - 0, 0 - 2) = (1, 1, -2).$$
   $$v = \overrightarrow{AC} = C - A = (0 - 1, 3 - 0, 1 - 2) = (-1, 3, -1).$$

2. **Find Normal Vector $n = u \times v$:**
   $$n = \det\begin{pmatrix}i & j & k \\ 1 & 1 & -2 \\ -1 & 3 & -1\end{pmatrix} = i(1(-1) - (-2)(3)) - j(1(-1) - (-2)(-1)) + k(1(3) - 1(-1))$$
   $$= i(-1 + 6) - j(-1 - 2) + k(3 + 1) = 5i + 3j + 4k = (5, 3, 4).$$

3. **Check Perpendicularity:**
   $$n \cdot u = 5(1) + 3(1) + 4(-2) = 5 + 3 - 8 = 0.$$
   $$n \cdot v = 5(-1) + 3(3) + 4(-1) = -5 + 9 - 4 = 0.$$
   Vector $n = (5, 3, 4)$ is perpendicular to both in-plane directions, serving as a valid normal vector to the plane.

---

### Exercise 13. Do Four Points Lie in One Plane?
Given
$$A=(0,0,0),\qquad B=(1,2,0),\qquad C=(0,1,1),\qquad D=(2,5,1).$$

1. Construct $\overrightarrow{AB}$ and $\overrightarrow{AC}$.
2. Find $n=\overrightarrow{AB}\times\overrightarrow{AC}$.
3. Construct $\overrightarrow{AD}$ and check whether $\overrightarrow{AD}\cdot n=0$.
4. Based on this, decide whether $D$ lies in the plane determined by $A,B,C$, and justify the criterion.

> **Why this exercise:** combines the known cross and dot products into a geometric criterion needed for planes, without introducing a separate concept used only once.

#### Solution

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

---

### Exercise 14. Closest Point on a Line
Given a point $P=(4,1)$ and a line through the origin with direction $v=(1,2)$. Using projection, find the closest point on the line, the distance from $P$ to the line, and verify that the appropriate vector is perpendicular to the direction of the line.

> **Why this exercise:** shows projection as a complete solution to a minimum-distance problem.

#### Solution

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

---

### Exercise 15. Comparing Directions Using the Cosine of the Angle
Given
$$a=(1,2,1),\qquad b=(2,4,2),\qquad c=(2,0,3).$$
For each pair, compute
$$\frac{u\cdot v}{\|u\|\,\|v\|}.$$
Order the pairs by increasing angle between the vectors. Explain why for $a$ and $b$ the value is $1$ even though the vectors have different lengths.

> **Why this exercise:** reinforces the connection between the dot product and angle, and the distinction between direction and length.

#### Solution

1. **Magnitudes:**
   $$\|a\| = \sqrt{1^2 + 2^2 + 1^2} = \sqrt{6}.$$
   $$\|b\| = \sqrt{2^2 + 4^2 + 2^2} = \sqrt{4 + 16 + 4} = \sqrt{24} = 2\sqrt{6}.$$
   $$\|c\| = \sqrt{2^2 + 0^2 + 3^2} = \sqrt{4 + 9} = \sqrt{13}.$$

2. **Cosine Calculations:**
   - **Pair $(a, b)$:**
     $$a \cdot b = 1(2) + 2(4) + 1(2) = 12.$$
     $$\cos\theta_{ab} = \frac{12}{\sqrt{6} \cdot 2\sqrt{6}} = \frac{12}{2 \cdot 6} = \frac{12}{12} = 1 \implies \theta_{ab} = 0^\circ.$$
   - **Pair $(a, c)$:**
     $$a \cdot c = 1(2) + 2(0) + 1(3) = 2 + 0 + 3 = 5.$$
     $$\cos\theta_{ac} = \frac{5}{\sqrt{6}\sqrt{13}} = \frac{5}{\sqrt{78}} \approx 0.5661 \implies \theta_{ac} \approx 55.52^\circ.$$
   - **Pair $(b, c)$:**
     $$b \cdot c = 2(2) + 4(0) + 2(3) = 4 + 0 + 6 = 10.$$
     $$\cos\theta_{bc} = \frac{10}{2\sqrt{6}\sqrt{13}} = \frac{10}{2\sqrt{78}} = \frac{5}{\sqrt{78}} \approx 0.5661 \implies \theta_{bc} \approx 55.52^\circ.$$

3. **Ordering by Increasing Angle:**
   $$\theta_{ab} = 0^\circ < \theta_{ac} = \theta_{bc} \approx 55.52^\circ.$$
   Order: Pair $(a, b)$, followed by pairs $(a, c)$ and $(b, c)$.

4. **Why $\cos = 1$ for $a$ and $b$:**
   Notice $b = (2, 4, 2) = 2(1, 2, 1) = 2a$. Vector $b$ is a positive scalar multiple of $a$, meaning both vectors lie along the same line pointing in the exact same orientation. The cosine formula normalizes by the vector lengths ($\|b\| = 2\|a\|$), so the length factor of 2 cancels out entirely ($\frac{2\|a\|^2}{2\|a\|^2} = 1$). The cosine measures directional alignment, which is independent of magnitude.
