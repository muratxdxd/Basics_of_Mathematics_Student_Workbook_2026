# Second-Degree Curves and Surfaces

## Goal of the Set

After completing this set, the student should be able to recognize the basic second-degree curves in the plane and the basic second-degree surfaces in space, read their most important features from equations, reduce simple equations to canonical form, and interpret geometric cross-sections.

The main goal is not to memorize a catalog of detailed properties, but to learn how to move from an algebraic equation to a geometric picture and back again.

## Basic Exercises

### Exercise 1. Recognizing Curves from Canonical Form
Recognize the curves
$$x^2+y^2=9,$$
$$\frac{x^2}{16}+\frac{y^2}{9}=1,$$
$$y^2=8x,$$
$$\frac{x^2}{9}-\frac{y^2}{4}=1.$$
For each one, identify the most important features and make a sketch. Explain which parts of the equation let you recognize the type of curve.

> **Why this exercise:** builds the basic dictionary: canonical equation → type of curve → shape and scale.

#### Solution

1. **$x^2 + y^2 = 9 = 3^2$ (Circle):**
   - **Type:** Circle centered at the origin $(0, 0)$.
   - **Features:** Radius $R = 3$. Intercepts at $(\pm 3, 0)$ and $(0, \pm 3)$.
   - **Recognition:** Both $x$ and $y$ are squared, have identical positive coefficients ($+1$), and sum to a positive constant.

2. **$\frac{x^2}{16} + \frac{y^2}{9} = 1$ (Ellipse):**
   - **Type:** Ellipse centered at $(0, 0)$.
   - **Features:** Horizontal major semiaxis $a = \sqrt{16} = 4$, vertical minor semiaxis $b = \sqrt{9} = 3$. Intercepts at $(\pm 4, 0)$ and $(0, \pm 3)$.
   - **Recognition:** Both variables are squared, have positive coefficients with different denominators, and sum to $1$.

3. **$y^2 = 8x$ (Parabola):**
   - **Type:** Parabola opening along the $x$-axis.
   - **Features:** Vertex at $(0, 0)$, axis of symmetry is the $x$-axis ($y = 0$). Opens to the right ($x \ge 0$). Focal parameter $2p = 8 \implies p = 4$, focus at $(2, 0)$, directrix $x = -2$.
   - **Recognition:** Exactly one variable is squared ($y^2$), while the other is linear ($x^1$).

4. **$\frac{x^2}{9} - \frac{y^2}{4} = 1$ (Hyperbola):**
   - **Type:** Horizontal hyperbola centered at $(0, 0)$.
   - **Features:** Vertices at $(\pm 3, 0)$, real semiaxis $a = 3$, imaginary semiaxis $b = 2$. Asymptotes: $y = \pm \frac{b}{a}x = \pm \frac{2}{3}x$. Opens to the left and right.
   - **Recognition:** Both variables are squared, but with opposite signs (difference of squares equals $1$).

---

### Exercise 2. Circle by Completing the Square
Reduce
$$x^2+y^2-6x+4y-3=0$$
to canonical form. Find the center and radius, then substitute two simple points from the circle into both forms of the equation.

> **Why this exercise:** practices completing the square as a transition from a general equation to the geometry of the object.

#### Solution

1. **Complete the Square:**
   Group $x$ and $y$ terms:
   $$(x^2 - 6x) + (y^2 + 4y) - 3 = 0.$$
   $$(x^2 - 6x + 9) - 9 + (y^2 + 4y + 4) - 4 - 3 = 0.$$
   $$(x - 3)^2 + (y + 2)^2 - 16 = 0.$$
   **Canonical Form:**
   $$(x - 3)^2 + (y + 2)^2 = 16 = 4^2.$$

2. **Center and Radius:**
   - Center: $(x_0, y_0) = (3, -2)$.
   - Radius: $R = \sqrt{16} = 4$.

3. **Substitution of Two Points on the Circle:**
   - **Point 1:** $(x_0 + R, y_0) = (3 + 4, -2) = (7, -2)$:
     - *Canonical form:* $(7 - 3)^2 + (-2 + 2)^2 = 4^2 + 0^2 = 16$ (holds).
     - *General form:* $7^2 + (-2)^2 - 6(7) + 4(-2) - 3 = 49 + 4 - 42 - 8 - 3 = 53 - 53 = 0$ (holds).
   - **Point 2:** $(x_0, y_0 + R) = (3, -2 + 4) = (3, 2)$:
     - *Canonical form:* $(3 - 3)^2 + (2 + 2)^2 = 0^2 + 4^2 = 16$ (holds).
     - *General form:* $3^2 + 2^2 - 6(3) + 4(2) - 3 = 9 + 4 - 18 + 8 - 3 = 21 - 21 = 0$ (holds).

---

### Exercise 3. Ellipse
For
$$\frac{x^2}{25}+\frac{y^2}{9}=1,$$
find the semiaxis lengths, the intercepts with the coordinate axes, and make a sketch. Explain along which axis the ellipse is more stretched and how this is visible in the equation.

> **Why this exercise:** teaches how to read the size and orientation of an ellipse without additional conceptual machinery.

#### Solution

1. **Semiaxis Lengths:**
   - Horizontal semiaxis: $a = \sqrt{25} = 5$.
   - Vertical semiaxis: $b = \sqrt{9} = 3$.

2. **Intercepts with the Coordinate Axes:**
   - $x$-intercepts ($y = 0$): $\frac{x^2}{25} = 1 \implies x = \pm 5$, giving points $(-5, 0)$ and $(5, 0)$.
   - $y$-intercepts ($x = 0$): $\frac{y^2}{9} = 1 \implies y = \pm 3$, giving points $(0, -3)$ and $(0, 3)$.

3. **Orientation and Stretching:**
   The ellipse is elongated along the **horizontal $x$-axis** ($a = 5 > b = 3$).
   In the canonical equation $\frac{x^2}{a^2} + \frac{y^2}{b^2} = 1$, the denominator under each variable represents the square of the maximum excursion (semiaxis) along that coordinate axis. Since $25 > 9$, the maximum extent along $x$ ($\pm 5$) is greater than along $y$ ($\pm 3$).

---

### Exercise 4. Parabola
For
$$y^2=12x,$$
identify the vertex, axis of symmetry, and opening direction. Find points on the parabola for $x=3$ and use them to make a sketch.

> **Why this exercise:** teaches how to move from the equation of a parabola to its basic geometry.

#### Solution

1. **Geometric Features:**
   - **Vertex:** $(0, 0)$.
   - **Axis of Symmetry:** The line $y = 0$ (the $x$-axis), because substituting $-y$ leaves the equation unchanged ($(-y)^2 = y^2 = 12x$).
   - **Opening Direction:** Opens to the **right** (along the positive $x$-axis), since $x = \frac{y^2}{12} \ge 0$ for all real $y$.
   - **Focal Parameter:** In standard form $y^2 = 2px$, $2p = 12 \implies p = 6$. The focus is at $\left(\frac{p}{2}, 0\right) = (3, 0)$ and directrix is $x = -3$.

2. **Points for $x = 3$:**
   $$y^2 = 12(3) = 36 \implies y = \pm\sqrt{36} = \pm 6.$$
   The points on the parabola are $(3, 6)$ and $(3, -6)$.
   (Notice that the focal width / latus rectum at $x = 3$ is $|6 - (-6)| = 12 = 2p$).

---

### Exercise 5. Hyperbola and Asymptotes
For
$$\frac{x^2}{16}-\frac{y^2}{9}=1,$$
find the intercepts with the $x$-axis, the asymptotes, and make a sketch. Explain why the asymptotes describe the behavior of the curve far from the center.

> **Why this exercise:** shows the role of asymptotes in understanding the global shape of a hyperbola.

#### Solution

1. **Intercepts with $x$-axis ($y = 0$):**
   $$\frac{x^2}{16} = 1 \implies x^2 = 16 \implies x = \pm 4.$$
   Vertices: $(-4, 0)$ and $(4, 0)$.
   (Note: For $x = 0$, $-\frac{y^2}{9} = 1 \implies y^2 = -9$, which has no real solutions, so there are no $y$-intercepts).

2. **Asymptotes:**
   Replace $1$ by $0$ in the canonical equation:
   $$\frac{x^2}{16} - \frac{y^2}{9} = 0 \implies \frac{y^2}{9} = \frac{x^2}{16} \implies y = \pm \frac{3}{4}x.$$

3. **Why Asymptotes Describe Far-Field Behavior:**
   Solve the hyperbola equation for $y$:
   $$y^2 = 9\left(\frac{x^2}{16} - 1\right) = \frac{9x^2}{16}\left(1 - \frac{16}{x^2}\right) \implies y = \pm \frac{3}{4}x \sqrt{1 - \frac{16}{x^2}}.$$
   As $|x| \to \infty$, the term $\frac{16}{x^2} \to 0$, so $\sqrt{1 - \frac{16}{x^2}} \to 1$.
   Thus, for large $|x|$, the vertical difference $|y_{\text{curve}} - y_{\text{asymptote}}| \to 0$. The hyperbola approaches closer and closer to the straight lines $y = \pm \frac{3}{4}x$.

---

### Exercise 6. Shifted Ellipse
Reduce
$$4x^2+9y^2-16x+18y-11=0$$
to canonical form. Give the center and semiaxis lengths. Check that substituting the coordinates of the center into the left-hand side gives a value consistent with the form you obtained.

> **Why this exercise:** reinforces completing the square and recognizing a shift of the coordinate system.

#### Solution

1. **Complete the Square:**
   $$4(x^2 - 4x) + 9(y^2 + 2y) - 11 = 0.$$
   $$4\left[(x - 2)^2 - 4\right] + 9\left[(y + 1)^2 - 1\right] - 11 = 0.$$
   $$4(x - 2)^2 - 16 + 9(y + 1)^2 - 9 - 11 = 0.$$
   $$4(x - 2)^2 + 9(y + 1)^2 = 36.$$
   Divide both sides by $36$:
   $$\frac{(x - 2)^2}{9} + \frac{(y + 1)^2}{4} = 1.$$

2. **Center and Semiaxis Lengths:**
   - Center: $(x_0, y_0) = (2, -1)$.
   - Semiaxis along $x$: $a = \sqrt{9} = 3$.
   - Semiaxis along $y$: $b = \sqrt{4} = 2$.

3. **Check Center Substitution:**
   In canonical form, the LHS before dividing was $4(x-2)^2 + 9(y+1)^2 - 36$.
   Substituting the center $(2, -1)$ into the original LHS:
   $$4(2)^2 + 9(-1)^2 - 16(2) + 18(-1) - 11 = 16 + 9 - 32 - 18 - 11 = 25 - 61 = -36.$$
   At the center, $(x-2)=0$ and $(y+1)=0$, so $4(0)^2 + 9(0)^2 - 36 = -36$. The value $-36$ matches the constant on the other side.

---

### Exercise 7. Classifying a Second-Degree Equation
Determine the type of object described by:
1. $4x^2+9y^2=36$,
2. $x^2-y^2=1$,
3. $x^2-4y=0$,
4. $x^2+y^2+1=0$.

In the last case, explain why there are no real points.

> **Why this exercise:** develops quick recognition of the curve type and checking whether real solutions exist.

#### Solution

1. **$4x^2 + 9y^2 = 36 \iff \frac{x^2}{9} + \frac{y^2}{4} = 1$:**
   **Ellipse** centered at $(0, 0)$ with semiaxes $a = 3, b = 2$.

2. **$x^2 - y^2 = 1$:**
   **Equilateral (rectangular) hyperbola** centered at $(0, 0)$ with vertices $(\pm 1, 0)$ and asymptotes $y = \pm x$.

3. **$x^2 - 4y = 0 \iff y = \frac{1}{4}x^2$:**
   **Parabola** with vertex at $(0, 0)$, axis of symmetry $x = 0$, opening upwards.

4. **$x^2 + y^2 + 1 = 0 \iff x^2 + y^2 = -1$:**
   **Empty set ($\emptyset$) / imaginary circle**.
   *Explanation:* For all real numbers $x, y \in \mathbb{R}$, squares are non-negative: $x^2 \ge 0$ and $y^2 \ge 0$. The sum of two non-negative numbers must be non-negative: $x^2 + y^2 \ge 0$. It is mathematically impossible for this sum to equal the negative number $-1$. Hence, there are no real coordinates satisfying the equation.

---

### Exercise 8. Sphere
Reduce
$$x^2+y^2+z^2-4x+2y-6z-2=0$$
to canonical form. Find the center and radius. Give two points on the sphere and check them in the equation.

> **Why this exercise:** transfers the technique known from circles from two dimensions to three.

#### Solution

1. **Complete the Square:**
   $$(x^2 - 4x + 4) + (y^2 + 2y + 1) + (z^2 - 6z + 9) - 4 - 1 - 9 - 2 = 0.$$
   $$(x - 2)^2 + (y + 1)^2 + (z - 3)^2 = 16 = 4^2.$$

2. **Center and Radius:**
   - Center: $(x_0, y_0, z_0) = (2, -1, 3)$.
   - Radius: $R = \sqrt{16} = 4$.

3. **Two Points and Verification:**
   - **Point 1:** $(x_0 + R, y_0, z_0) = (2 + 4, -1, 3) = (6, -1, 3)$:
     - *Canonical:* $(6-2)^2 + (-1+1)^2 + (3-3)^2 = 4^2 + 0 + 0 = 16$ (holds).
     - *General:* $6^2 + (-1)^2 + 3^2 - 4(6) + 2(-1) - 6(3) - 2 = 36 + 1 + 9 - 24 - 2 - 18 - 2 = 46 - 46 = 0$ (holds).
   - **Point 2:** $(x_0, y_0, z_0 + R) = (2, -1, 3 + 4) = (2, -1, 7)$:
     - *Canonical:* $(2-2)^2 + (-1+1)^2 + (7-3)^2 = 0 + 0 + 4^2 = 16$ (holds).
     - *General:* $2^2 + (-1)^2 + 7^2 - 4(2) + 2(-1) - 6(7) - 2 = 4 + 1 + 49 - 8 - 2 - 42 - 2 = 54 - 54 = 0$ (holds).

---

### Exercise 9. Ellipsoid and Its Cross-Sections
Consider
$$\frac{x^2}{9}+\frac{y^2}{4}+\frac{z^2}{16}=1.$$
Give the semiaxis lengths, describe the cross-section $z=0$, and explain how the cross-sections $z=c$ change for $|c|<4$.

> **Why this exercise:** teaches how to understand a 3D surface through a family of simpler 2D cross-sections.

#### Solution

1. **Semiaxis Lengths:**
   - Along $x$: $a = \sqrt{9} = 3$.
   - Along $y$: $b = \sqrt{4} = 2$.
   - Along $z$: $c_0 = \sqrt{16} = 4$.

2. **Cross-Section $z = 0$ (the $xy$-plane):**
   $$\frac{x^2}{9} + \frac{y^2}{4} = 1.$$
   This is an **ellipse** in the $xy$-plane with semiaxes $3$ and $2$.

3. **Cross-Sections $z = c$ for $|c| < 4$:**
   $$\frac{x^2}{9} + \frac{y^2}{4} = 1 - \frac{c^2}{16}.$$
   Since $|c| < 4$, the factor $k^2 = 1 - \frac{c^2}{16}$ is strictly positive ($0 < k^2 \le 1$).
   Dividing through by $k^2$:
   $$\frac{x^2}{9k^2} + \frac{y^2}{4k^2} = 1.$$
   Each cross-section is an ellipse with semiaxes $a(c) = 3\sqrt{1 - \frac{c^2}{16}}$ and $b(c) = 2\sqrt{1 - \frac{c^2}{16}}$.
   - At $c = 0$, the cross-sectional ellipse has maximum area.
   - As $|c|$ increases towards $4$, the semiaxes shrink continuously.
   - At $|c| = 4$, the semiaxes become $0$, reducing the ellipse to a single point $(0, 0, \pm 4)$ (the north and south poles).
   - For $|c| > 4$, the RHS is negative, so there are no real points.

---

### Exercise 10. Paraboloids
Compare
$$z=x^2+y^2$$
and
$$z=x^2-y^2.$$
For each surface, describe the cross-sections $x=0$, $y=0$, and $z=c$, then make a qualitative sketch.

> **Why this exercise:** teaches how to distinguish two basic types of paraboloids from their cross-sections.

#### Solution

1. **Surface 1: $z = x^2 + y^2$ (Elliptic Paraboloid):**
   - **Cross-section $x = 0$:** $z = y^2$ (a parabola in the $yz$-plane opening upward with vertex at $(0,0,0)$).
   - **Cross-section $y = 0$:** $z = x^2$ (a parabola in the $xz$-plane opening upward with vertex at $(0,0,0)$).
   - **Cross-sections $z = c$:**
     - For $c > 0$: $x^2 + y^2 = c$ (circles of radius $\sqrt{c}$ that widen as $z$ increases).
     - For $c = 0$: $x^2 + y^2 = 0$ (the single vertex point $(0, 0, 0)$).
     - For $c < 0$: no real points (the surface lies entirely in the upper half-space $z \ge 0$).
   - **Shape:** A rotationally symmetric "bowl".

2. **Surface 2: $z = x^2 - y^2$ (Hyperbolic Paraboloid):**
   - **Cross-section $x = 0$:** $z = -y^2$ (a parabola in the $yz$-plane opening **downward**).
   - **Cross-section $y = 0$:** $z = x^2$ (a parabola in the $xz$-plane opening **upward**).
   - **Cross-sections $z = c$:**
     - For $c > 0$: $x^2 - y^2 = c$ (hyperbolas with vertices on the $x$-axis at $(\pm\sqrt{c}, 0, c)$).
     - For $c = 0$: $x^2 - y^2 = 0 \iff y = \pm x$ (a pair of intersecting straight lines through the origin).
     - For $c < 0$: $y^2 - x^2 = -c = |c|$ (hyperbolas with vertices on the $y$-axis at $(0, \pm\sqrt{|c|}, c)$).
   - **Shape:** A "saddle" (or mountain pass). At $(0,0,0)$, the surface curves up along $x$ and down along $y$.

---

## More Challenging Exercises

### Exercise 11. Two Similar Surfaces
Compare
$$x^2+y^2-z^2=1$$
and
$$x^2+y^2-z^2=-1.$$
For several values $z=c$, check whether the cross-section exists and what its radius is. Based on this, describe qualitatively the difference between the surfaces and make sketches.

> **Why this exercise:** teaches how to recognize the shape of a surface from cross-sections instead of from a memorized catalog of names.

#### Solution

1. **Surface 1: $x^2 + y^2 - z^2 = 1 \iff x^2 + y^2 = 1 + z^2$ (Hyperboloid of One Sheet):**
   - For $z = 0$: $x^2 + y^2 = 1$, circle of radius $R = 1$.
   - For $z = \pm 1$: $x^2 + y^2 = 2$, circle of radius $R = \sqrt{2} \approx 1.414$.
   - For $z = \pm 2$: $x^2 + y^2 = 5$, circle of radius $R = \sqrt{5} \approx 2.236$.
   - For any $z = c \in \mathbb{R}$: $1 + c^2 \ge 1 > 0$, so cross-sections are **always non-empty circles** of radius $R(c) = \sqrt{1 + c^2}$.
   - **Qualitative shape:** A single, unbroken, connected tube with a narrow "waist" of radius $1$ at the equator $z = 0$, flaring outward as $|z| \to \infty$.

2. **Surface 2: $x^2 + y^2 - z^2 = -1 \iff x^2 + y^2 = z^2 - 1$ (Hyperboloid of Two Sheets):**
   - For $z = 0$: $x^2 + y^2 = -1 \implies$ **no real cross-section**.
   - For $|z| < 1$: $z^2 - 1 < 0 \implies$ no real points exist in the slab $-1 < z < 1$.
   - For $z = \pm 1$: $x^2 + y^2 = 0 \implies$ two isolated vertex points $(0, 0, 1)$ and $(0, 0, -1)$.
   - For $z = \pm 2$: $x^2 + y^2 = 3$, circle of radius $R = \sqrt{3} \approx 1.732$.
   - **Qualitative shape:** Two disconnected, separate sheets (an upper bowl for $z \ge 1$ opening upward, and a lower bowl for $z \le -1$ opening downward), separated by an empty gap of height $2$.

---

### Exercise 12. Recognizing a Surface from Cross-Sections
A certain surface has the following properties:
- the cross-section $z=0$ is a point,
- for $z>0$, the cross-sections $z=\text{const}$ are circles with increasing radius,
- vertical cross-sections through the $Oz$ axis are parabolas.

Propose a simple equation for such a surface and justify your choice.

> **Why this exercise:** reverses the usual reasoning: from geometry to an equation.

#### Solution

1. **Proposed Equation:**
   $$z = x^2 + y^2.$$

2. **Justification of All Three Properties:**
   - **Property 1 ($z = 0$ is a point):**
     Substituting $z = 0$ gives $x^2 + y^2 = 0$. In real coordinates, this holds only when $x = 0$ and $y = 0$. Hence, the cross-section is the single point $(0, 0, 0)$.
   - **Property 2 ($z = \text{const} > 0$ are circles of increasing radius):**
     Setting $z = c > 0$ gives $x^2 + y^2 = c = (\sqrt{c})^2$. This is a circle in the plane $z = c$ centered on the $z$-axis with radius $R(c) = \sqrt{c}$. As $c$ increases, the radius $\sqrt{c}$ increases strictly monotonically.
   - **Property 3 (vertical cross-sections through $Oz$ are parabolas):**
     Any vertical plane through the $z$-axis can be parameterized by angle $\theta$: $x = r\cos\theta, y = r\sin\theta$.
     Substituting these into the surface equation:
     $$z = (r\cos\theta)^2 + (r\sin\theta)^2 = r^2(\cos^2\theta + \sin^2\theta) = r^2.$$
     In the coordinate plane $(r, z)$, the equation is $z = r^2$, which is an upward-opening parabola with vertex at the origin.
   This surface is an elliptic (circular) paraboloid of revolution.

---

### Exercise 13. Intersection of a Sphere and a Plane
Given the sphere
$$x^2+y^2+z^2=25$$
and the plane $z=3$, find the equation of the intersection curve and its radius. Then describe what happens for $z=c$ depending on $c$.

> **Why this exercise:** connects a surface equation with the geometry of its intersection.

#### Solution

1. **Intersection with $z = 3$:**
   Substitute $z = 3$ into the sphere equation:
   $$x^2 + y^2 + 3^2 = 25 \implies x^2 + y^2 + 9 = 25 \implies x^2 + y^2 = 16 = 4^2.$$
   - **Equation of the curve:** $x^2 + y^2 = 16$ lying in the plane $z = 3$.
   - **Center:** $(0, 0, 3)$.
   - **Radius:** $R = \sqrt{16} = 4$.

2. **General Behavior for Plane $z = c$:**
   Substitute $z = c$:
   $$x^2 + y^2 = 25 - c^2.$$
   - **Case $|c| < 5$ (Secant Plane):**
     $25 - c^2 > 0$. The intersection is a **circle** in the plane $z = c$ centered at $(0, 0, c)$ with radius $R = \sqrt{25 - c^2}$. (The maximum radius $R = 5$ occurs at the equator $c = 0$).
   - **Case $|c| = 5$ (Tangent Plane):**
     $25 - (\pm 5)^2 = 0 \implies x^2 + y^2 = 0$. The plane touches the sphere at a single point: the north pole $(0, 0, 5)$ for $c = 5$ or the south pole $(0, 0, -5)$ for $c = -5$.
   - **Case $|c| > 5$ (Disjoint Plane):**
     $25 - c^2 < 0$. The equation has no real solutions; the plane does not intersect the sphere.

---

### Exercise 14. Cone and Cylinder
Compare
$$x^2+y^2=z^2$$
and
$$x^2+y^2=4.$$
For each surface, describe the cross-sections $z=c$, $x=0$, and $y=0$, make a sketch, and explain why the radius of the cross-section depends on $z$ in the first case but is constant in the second.

> **Why this exercise:** teaches how to distinguish a cone from a cylinder by the behavior of their cross-sections.

#### Solution

1. **Surface 1: $x^2 + y^2 = z^2$ (Double Circular Cone):**
   - **Cross-sections $z = c$:**
     $x^2 + y^2 = c^2$. For $c \neq 0$, these are circles of radius $R(c) = |c|$. At $z = 0$, $x^2 + y^2 = 0$, which is the single apex point $(0, 0, 0)$.
   - **Cross-section $x = 0$:**
     $y^2 = z^2 \implies y = \pm z$, a pair of straight lines intersecting at $(0, 0, 0)$.
   - **Cross-section $y = 0$:**
     $x^2 = z^2 \implies x = \pm z$, a pair of straight lines intersecting at $(0, 0, 0)$.

2. **Surface 2: $x^2 + y^2 = 4$ (Circular Cylinder):**
   - **Cross-sections $z = c$:**
     $x^2 + y^2 = 4 = 2^2$. For every $c \in \mathbb{R}$, this is a circle of constant radius $R = 2$.
   - **Cross-section $x = 0$:**
     $y^2 = 4 \implies y = \pm 2$, a pair of vertical parallel lines.
   - **Cross-section $y = 0$:**
     $x^2 = 4 \implies x = \pm 2$, a pair of vertical parallel lines.

3. **Why Radius Depends on $z$ in the Cone but Not the Cylinder:**
   - In the cone equation $x^2 + y^2 = z^2$, the coordinate $z$ is explicitly coupled to the horizontal coordinates. As elevation $|z|$ increases, the right-hand side grows proportionally, forcing the cross-sectional circle to expand linearly with $|z|$.
   - In the cylinder equation $x^2 + y^2 = 4$, the variable $z$ is completely absent (free). The algebraic constraint applies strictly to $x$ and $y$, requiring the exact same circle of radius $2$ at every horizontal slice regardless of $z$.

---

### Exercise 15. Recognition and Sketch Without a Given Name
Consider the two equations:

$$4x^2+9y^2-8x+36y+4=0,$$

$$4x^2+y^2=z^2.$$

For the first equation, reduce it to canonical form, recognize the curve, give its most important features, and make a sketch.

For the second equation, do not begin by using a ready-made name for the surface. First describe the cross-sections $z=c$ and the cross-sections by the planes $x=0$ and $y=0$, paying attention to the different scales along the axes. Only then identify the surface and make a sketch.

> **Why this exercise:** tests transfer of the two main mechanisms of the set—moving to canonical form and recognizing an object through cross-sections—without allowing the easiest example to be chosen.

#### Solution

1. **Equation 1: $4x^2 + 9y^2 - 8x + 36y + 4 = 0$:**
   - **Complete the square:**
     $$4(x^2 - 2x) + 9(y^2 + 4y) + 4 = 0.$$
     $$4\left[(x - 1)^2 - 1\right] + 9\left[(y + 2)^2 - 4\right] + 4 = 0.$$
     $$4(x - 1)^2 - 4 + 9(y + 2)^2 - 36 + 4 = 0.$$
     $$4(x - 1)^2 + 9(y + 2)^2 = 36.$$
     Divide by $36$:
     $$\frac{(x - 1)^2}{9} + \frac{(y + 2)^2}{4} = 1.$$
   - **Recognition:** **Ellipse**.
   - **Key features:**
     - Center: $(x_0, y_0) = (1, -2)$.
     - Horizontal semiaxis: $a = \sqrt{9} = 3$.
     - Vertical semiaxis: $b = \sqrt{4} = 2$.
     - Vertices: $(1 \pm 3, -2) \implies (-2, -2)$ and $(4, -2)$.
     - Co-vertices: $(1, -2 \pm 2) \implies (1, -4)$ and $(1, 0)$.

2. **Equation 2: $4x^2 + y^2 = z^2$:**
   - **Cross-sections $z = c$:**
     $$4x^2 + y^2 = c^2 \iff \frac{x^2}{(|c|/2)^2} + \frac{y^2}{|c|^2} = 1 \quad (\text{for } c \neq 0).$$
     For any non-zero height $z = c$, the cross-section is an **ellipse** with horizontal semiaxis $a(c) = \frac{|c|}{2}$ and vertical semiaxis $b(c) = |c|$.
     Notice the vertical semiaxis along $y$ is twice as long as the horizontal semiaxis along $x$ ($b = 2a$).
     For $z = 0$, $4x^2 + y^2 = 0 \implies (0, 0, 0)$ (a single apex point).
   - **Cross-section $x = 0$ (the $yz$-plane):**
     $$y^2 = z^2 \implies z = \pm y.$$
     A pair of intersecting lines with slope $\pm 1$.
   - **Cross-section $y = 0$ (the $xz$-plane):**
     $$4x^2 = z^2 \implies z = \pm 2x.$$
     A pair of intersecting lines with steeper slope $\pm 2$.
   - **Identification:**
     Combining elliptical horizontal cross-sections that scale linearly with $|z|$ and linear triangular vertical profiles, the surface is an **Elliptic Cone** with vertex at the origin $(0, 0, 0)$ and central axis along the $z$-axis.
