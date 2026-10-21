# Applications of Differential and Integral Calculus

## Goal of the Problem Set

This problem set is cross-sectional in nature and is intentionally shorter than the others. The student should be able to choose variables from a problem description, build a model, decide whether a derivative, an integral, or both tools are needed, and then interpret the result in the context of the problem.

The problem set may be completed flexibly near the end of the semester. It is not intended to repeat all the calculus from the previous problem sets, but rather to check whether the student can use the methods learned in a problem that does not immediately suggest a ready-made formula.

## Basic Problems

### Problem 1. Motion — from Position to Velocity
The position of a point is described by
$$
s(t)=t^3-6t^2+9t+2,\qquad t\ge0.
$$

1. Determine the velocity and acceleration.
2. Find the times at which the point stops.
3. Determine on which intervals the point moves in the positive direction of the axis and on which intervals it moves in the negative direction.

> **Why this problem:** it shows the derivative as a real rate of change and requires interpretation of the sign of the derivative in the context of motion.

#### Solution

1. **Velocity and Acceleration:**
   - Velocity is the first derivative of position:
     $$v(t) = s'(t) = 3t^2 - 12t + 9 = 3(t^2 - 4t + 3) = 3(t - 1)(t - 3).$$
   - Acceleration is the derivative of velocity:
     $$a(t) = v'(t) = s''(t) = 6t - 12 = 6(t - 2).$$

2. **Times at Which the Point Stops:**
   The point stops instantaneously when its velocity is zero ($v(t) = 0$):
   $$3(t - 1)(t - 3) = 0 \iff t = 1 \quad \text{and} \quad t = 3.$$
   The point stops at $t = 1\text{ s}$ and at $t = 3\text{ s}$.

3. **Direction of Motion:**
   The direction of motion is governed by the sign of velocity $v(t)$:
   - For $t \in [0, 1)$: $v(t) > 0 \implies$ moving in the **positive direction**.
   - For $t \in (1, 3)$: $v(t) < 0 \implies$ moving in the **negative direction** (moving backward).
   - For $t \in (3, \infty)$: $v(t) > 0 \implies$ moving in the **positive direction**.
   (At $t = 1$, the particle turns around from positive to negative; at $t = 3$, it turns around from negative to positive).

---

### Problem 2. Maximum Area of a Rectangle
A rectangle has perimeter $40$.

1. Write its area as a function of the length of one side.
2. Determine the domain of this function resulting from the geometry of the problem.
3. Find the dimensions that give the maximum area.
4. Justify that the point found actually gives a maximum.

> **Why this problem:** it teaches the complete optimization scheme: model → domain → derivative → verification and interpretation of the maximum.

#### Solution

1. **Area Function:**
   Let the rectangle side lengths be $x$ and $y$.
   Perimeter constraint:
   $$2x + 2y = 40 \implies x + y = 20 \implies y = 20 - x.$$
   Area as a function of $x$:
   $$A(x) = x y = x(20 - x) = 20x - x^2.$$

2. **Domain Resulting from Geometry:**
   Both side lengths must be strictly positive:
   $$x > 0 \quad \text{and} \quad 20 - x > 0 \implies x < 20.$$
   $$D_A = (0, 20).$$

3. **Find Dimensions for Maximum Area:**
   Differentiate with respect to $x$:
   $$A'(x) = 20 - 2x.$$
   Setting $A'(x) = 0$:
   $$20 - 2x = 0 \implies 2x = 20 \implies x = 10.$$
   Then $y = 20 - 10 = 10$.
   The optimal dimensions are $x = 10$ and $y = 10$ (a square), giving maximum area $A(10) = 100$.

4. **Justification of Maximum:**
   - Second derivative test: $A''(x) = -2 < 0$ for all $x$. Since the second derivative is strictly negative everywhere, the function is strictly concave, proving that $x = 10$ is the unique global maximum on $(0, 20)$.

---

### Problem 3. A Box Made from Cardboard
From a $30\text{ cm}\times40\text{ cm}$ sheet, squares of side length $x$ are cut from the corners and the edges are folded up to form an open box.

Write the volume as a function of $x$, determine the physically meaningful domain, and find the value of $x$ for which the volume is greatest.

> **Why this problem:** it develops optimization modeling in a situation where the objective function is not given and must be built independently from the geometry.

#### Solution

1. **Volume Function:**
   Cutting squares of side $x$ from each corner and folding creates a box with:
   - Height: $h = x$
   - Width: $w = 30 - 2x$
   - Length: $l = 40 - 2x$
   $$V(x) = x(30 - 2x)(40 - 2x) = x(1200 - 140x + 4x^2) = 4x^3 - 140x^2 + 1200x.$$

2. **Domain:**
   All physical dimensions must be strictly positive:
   $$x > 0, \qquad 30 - 2x > 0 \implies x < 15, \qquad 40 - 2x > 0 \implies x < 20.$$
   Intersecting these conditions yields:
   $$D_V = (0, 15).$$

3. **Find Maximum Volume:**
   $$V'(x) = 12x^2 - 280x + 1200 = 4(3x^2 - 70x + 300) = 0.$$
   Solve the quadratic equation $3x^2 - 70x + 300 = 0$:
   $$\Delta = (-70)^2 - 4(3)(300) = 4900 - 3600 = 1300.$$
   $$\sqrt{\Delta} = 10\sqrt{13} \approx 36.0555.$$
   $$x = \frac{70 \pm 10\sqrt{13}}{2(3)} = \frac{35 \pm 5\sqrt{13}}{3}.$$
   - Candidate 1: $x_1 = \frac{35 - 5\sqrt{13}}{3} \approx \frac{35 - 18.028}{3} \approx 5.657\text{ cm} \in (0, 15)$.
   - Candidate 2: $x_2 = \frac{35 + 5\sqrt{13}}{3} \approx \frac{35 + 18.028}{3} \approx 17.676\text{ cm} \notin (0, 15)$.
   Check second derivative at $x_1$:
   $$V''(x) = 24x - 280 \implies V''(5.657) \approx 24(5.657) - 280 = 135.77 - 280 = -144.23 < 0.$$
   The maximum volume occurs at $x = \frac{35 - 5\sqrt{13}}{3} \approx 5.66\text{ cm}$, yielding volume $V \approx 3032.3\text{ cm}^3$.

---

### Problem 4. Area Between Curves
Find the area of the region bounded by the graphs
$$
y=x
$$
and
$$
y=x^2.
$$

First find the intersection points and justify which function is greater on the relevant interval.

> **Why this problem:** it teaches that before integrating, one must first determine the geometry of the region and the correct order of the functions.

#### Solution

1. **Find Intersection Points:**
   Set the functions equal:
   $$x = x^2 \iff x^2 - x = 0 \iff x(x - 1) = 0 \implies x_1 = 0, \quad x_2 = 1.$$
   The intersection points are $(0, 0)$ and $(1, 1)$.

2. **Justify Which Function Is Greater on $(0, 1)$:**
   For any $x \in (0, 1)$, multiplying both sides of $x < 1$ by positive $x$ yields $x^2 < x$.
   Testing a sample point $x = 0.5$:
   $$y_{\text{line}} = 0.5, \qquad y_{\text{parabola}} = 0.5^2 = 0.25 < 0.5.$$
   Thus, on $[0, 1]$, $x \ge x^2$. The line forms the upper boundary and the parabola forms the lower boundary.

3. **Compute Area:**
   $$A = \int_0^1 (y_{\text{upper}} - y_{\text{lower}})\,dx = \int_0^1 (x - x^2)\,dx = \left[\frac{x^2}{2} - \frac{x^3}{3}\right]_0^1 = \left(\frac{1}{2} - \frac{1}{3}\right) - 0 = \frac{1}{6} \approx 0.1667.$$

---

### Problem 5. Distance from Velocity
The velocity of a car during the first five seconds is described by the function
$$
v(t)=4t+2\quad [\mathrm{m/s}].
$$

Compute the distance traveled and explain why the integral of velocity gives the change in position.

Then answer what would have to be changed in the reasoning if the velocity also took negative values.

> **Why this problem:** it connects the integral with accumulation and distinguishes displacement from the actual distance traveled.

#### Solution

1. **Compute Distance Traveled on $[0, 5]$:**
   Since $v(t) = 4t + 2 > 0$ for all $t \in [0, 5]$, the car moves in one direction only:
   $$s = \int_0^5 v(t)\,dt = \int_0^5 (4t + 2)\,dt = \left[2t^2 + 2t\right]_0^5 = 2(5^2) + 2(5) = 2(25) + 10 = 50 + 10 = 60\text{ meters}.$$

2. **Why the Integral of Velocity Gives Change in Position:**
   By definition, velocity is the instantaneous rate of change of position: $v(t) = \frac{ds}{dt}$.
   Over an infinitesimal time interval $dt$, the incremental displacement is $ds = v(t)dt$.
   By the Fundamental Theorem of Calculus, integrating this rate accumulates all the tiny displacements over the full time interval:
   $$\int_{t_1}^{t_2} v(t)\,dt = \int_{t_1}^{t_2} s'(t)\,dt = s(t_2) - s(t_1) = \Delta s.$$

3. **Modification if Velocity Took Negative Values:**
   If velocity takes negative values, $\int_{t_1}^{t_2} v(t)\,dt$ calculates **net displacement** (where backward travel cancels out forward travel).
   To compute the actual **total physical distance traveled** (odometer distance), one must integrate the absolute speed:
   $$s_{\text{distance}} = \int_{t_1}^{t_2} |v(t)|\,dt.$$

---

### Problem 6. Average Value of a Function
Compute the average value of the function
$$
f(x)=x^2
$$
on the interval $[0,3]$.

Find a point $c\in[0,3]$ for which $f(c)$ is equal to this average value, and interpret the result geometrically.

> **Why this problem:** it gives the integral the interpretation of an average value and connects the numerical result with a level of the function on the graph.

#### Solution

1. **Compute Average Value:**
   $$f_{\text{avg}} = \frac{1}{b - a}\int_a^b f(x)\,dx = \frac{1}{3 - 0}\int_0^3 x^2\,dx = \frac{1}{3}\left[\frac{x^3}{3}\right]_0^3 = \frac{1}{3}\left(\frac{27}{3} - 0\right) = \frac{1}{3}(9) = 3.$$

2. **Find Point $c \in [0, 3]$:**
   Set $f(c) = f_{\text{avg}}$:
   $$c^2 = 3 \implies c = \sqrt{3} \approx 1.732.$$
   Notice that $\sqrt{3} \in [0, 3]$.

3. **Geometric Interpretation:**
   By the Mean Value Theorem for Integrals, the area under the parabolic curve $y = x^2$ over $[0, 3]$ ($\text{Area} = 9$) is exactly equal to the area of a rectangle of base width $3$ and constant height $f_{\text{avg}} = 3$ ($3 \times 3 = 9$). The value $c = \sqrt{3}$ is the exact coordinate where the curve intersects the horizontal ceiling of this equivalent area rectangle.

---

### Problem 7. Exponential Growth
Assume the model
$$
N(t)=N_0e^{kt},\qquad k>0.
$$

1. Verify by differentiation that the model satisfies the relation $N'(t)=kN(t)$.
2. Find the population doubling time.
3. Explain why the doubling time does not depend on $N_0$.

> **Why this problem:** it shows the connection between the exponential function and a growth rate proportional to the current value, without introducing a separate technique for solving differential equations.

#### Solution

1. **Verify $N'(t) = kN(t)$:**
   Differentiate using the chain rule:
   $$N'(t) = \frac{d}{dt}\left(N_0 e^{kt}\right) = N_0 \cdot \left(e^{kt} \cdot k\right) = k\left(N_0 e^{kt}\right) = k N(t).$$
   The derivative is directly proportional to the current population with constant of proportionality $k$.

2. **Find Doubling Time $T$:**
   The population doubles when $N(T) = 2N_0$:
   $$N_0 e^{kT} = 2N_0 \implies e^{kT} = 2 \implies kT = \ln 2 \implies T = \frac{\ln 2}{k} \approx \frac{0.69315}{k}.$$

3. **Why Doubling Time Does Not Depend on $N_0$:**
   In the equation $N_0 e^{kT} = 2N_0$, the initial population $N_0$ divides out completely. Exponential growth is scale-invariant: growing by a fixed percentage or factor requires multiplying the current size, which takes the exact same amount of time regardless of whether the population starts at $10$ organisms or $10\,000\,000$.

---

### Problem 8. Number of Requests Handled by a Server
The rate at which requests arrive at a server during the first 5 minutes is described by the function
$$
r(t)=100+20t\quad [\text{requests/min}],\qquad 0\le t\le5.
$$

1. Compute the total number of requests that arrived during this time.
2. Compute the average rate of incoming requests over this interval.
3. Compare the average rate with the values $r(0)$ and $r(5)$.

> **Why this problem:** it shows the integral as summation of a varying rate in an example directly related to computer science.

#### Solution

1. **Total Number of Requests:**
   Accumulate the rate over time via integration:
   $$R = \int_0^5 r(t)\,dt = \int_0^5 (100 + 20t)\,dt = \left[100t + 10t^2\right]_0^5 = 100(5) + 10(5^2) = 500 + 250 = 750\text{ requests}.$$

2. **Average Rate of Incoming Requests:**
   $$r_{\text{avg}} = \frac{R}{5 - 0} = \frac{750}{5} = 150\text{ requests/min}.$$

3. **Comparison with $r(0)$ and $r(5)$:**
   - $r(0) = 100 + 20(0) = 100\text{ requests/min}$.
   - $r(5) = 100 + 20(5) = 200\text{ requests/min}$.
   - Arithmetic mean of endpoint rates:
     $$\frac{r(0) + r(5)}{2} = \frac{100 + 200}{2} = 150\text{ requests/min} = r_{\text{avg}}.$$
   Because $r(t)$ is a linear function, its rate increases uniformly, making the integral average identical to the arithmetic midpoint of the starting and ending rates.

---

## More Difficult and Cross-Sectional Problems

### Problem 9. Minimizing the Material Used for a Can
A closed cylinder has fixed volume $V$.

1. Write the volume constraint.
2. Eliminate one of the variables.
3. Express the surface area as a function of the radius $r$.
4. Find the relation between the height $h$ and the radius $r$ for which the material usage is minimal.

Interpret the obtained relation geometrically.

> **Why this problem:** it requires independent reduction of a problem with two variables to one objective function and control of the geometric constraint.

#### Solution

1. **Volume Constraint:**
   $$V = \pi r^2 h = \text{constant}.$$

2. **Eliminate Variable $h$:**
   $$h = \frac{V}{\pi r^2}.$$

3. **Surface Area Function $A(r)$:**
   Total surface area consists of two circular bases plus the lateral cylinder wall:
   $$A = 2(\pi r^2) + 2\pi r h = 2\pi r^2 + 2\pi r\left(\frac{V}{\pi r^2}\right) = 2\pi r^2 + \frac{2V}{r}, \qquad r > 0.$$

4. **Minimize Surface Area:**
   Differentiate with respect to $r$:
   $$A'(r) = 4\pi r - \frac{2V}{r^2}.$$
   Setting $A'(r) = 0$:
   $$4\pi r = \frac{2V}{r^2} \implies 4\pi r^3 = 2V \implies 2\pi r^3 = V.$$
   Substitute back $V = \pi r^2 h$:
   $$2\pi r^3 = \pi r^2 h \implies 2r = h \iff h = 2r.$$
   (Second derivative check: $A''(r) = 4\pi + \frac{4V}{r^3} > 0$ for all $r > 0$, confirming a strict global minimum).

5. **Geometric Interpretation:**
   The material usage is minimal when the cylinder's height $h$ is exactly equal to its diameter $2r$ ($h = 2r = d$). An axial cross-section through the center of such a cylinder is a square of dimensions $2r \times 2r$. This makes the 3D shape maximally compact, minimizing exposure of surface area relative to enclosed volume.

---

### Problem 10. A Cable Through Water and Land
Point $A$ lies on one bank of a river of width $100$ m, and point $B$ lies on the other bank, $500$ m along the bank from the point directly opposite $A$.

The cost per meter of cable underwater is twice the cost per meter of cable on land.

Build a cost function depending on the point where the cable comes out of the water, determine the domain, and find the solution that minimizes the cost.

> **Why this problem:** it checks whether the student can independently translate a spatial description and two different costs into a single function to be optimized.

#### Solution

1. **Geometry and Cost Function:**
   Let $A = (0, 100)$ and let the point directly opposite on the other bank be the origin $(0, 0)$. Point $B$ lies at $(500, 0)$.
   Suppose the underwater cable runs in a straight line from $A(0, 100)$ to a point $P(x, 0)$ on the opposite bank ($0 \le x \le 500$), and then runs along land from $P(x, 0)$ to $B(500, 0)$.
   - Underwater length: $d_w = \sqrt{100^2 + x^2}$.
   - Land length: $d_L = 500 - x$.
   Let the cost per meter on land be $c$, and underwater be $2c$.
   Total cost (divided by $c$):
   $$C(x) = 2\sqrt{10\,000 + x^2} + (500 - x).$$

2. **Domain:**
   The cable emergence point $x$ must lie between the perpendicular crossing and target $B$:
   $$D_C = [0, 500].$$

3. **Minimize Cost:**
   Differentiate with respect to $x$:
   $$C'(x) = 2 \cdot \frac{2x}{2\sqrt{10\,000 + x^2}} - 1 = \frac{2x}{\sqrt{10\,000 + x^2}} - 1.$$
   Setting $C'(x) = 0$:
   $$\frac{2x}{\sqrt{10\,000 + x^2}} = 1 \implies 2x = \sqrt{10\,000 + x^2}.$$
   Square both sides:
   $$4x^2 = 10\,000 + x^2 \implies 3x^2 = 10\,000 \implies x^2 = \frac{10\,000}{3} \implies x = \frac{100}{\sqrt{3}} = \frac{100\sqrt{3}}{3} \approx 57.74\text{ m}.$$
   Notice $x \approx 57.74 \in [0, 500]$.

4. **Verification of Minimum:**
   - At critical point $x \approx 57.74\text{ m}$:
     $$C(57.74) = 2\sqrt{10000 + 3333.33} + (500 - 57.74) = 2(115.47) + 442.26 = 230.94 + 442.26 = 673.2c.$$
   - At boundary $x = 0$ (perpendicular water crossing, then all land):
     $$C(0) = 2(100) + 500 = 700c > 673.2c.$$
   - At boundary $x = 500$ (direct water diagonal to $B$):
     $$C(500) = 2\sqrt{100^2 + 500^2} + 0 = 2\sqrt{260\,000} \approx 2(509.90) = 1019.8c > 673.2c.$$
   The minimum cost is achieved when the cable emerges at $x = \frac{100\sqrt{3}}{3} \approx 57.74\text{ m}$ downstream from the point opposite $A$. (This corresponds to an underwater trajectory angled at $\theta = 30^\circ$ to the river bank, satisfying Snell's Law $\cos\theta = \frac{c_{\text{land}}}{c_{\text{water}}} = \frac{1}{2}$).

---

### Problem 11. Volume of a Solid of Revolution
The region under the graph
$$
y=\sqrt{x},\qquad x\in[0,4],
$$
is rotated about the $x$-axis.

1. Construct the integral describing the volume using the disk method.
2. Compute the volume.
3. Explain where the factor $\pi y^2$ in the integral comes from.

> **Why this problem:** it teaches how to construct an integral from the geometry of cross-sections instead of applying a volume formula without understanding its origin.

#### Solution

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

---

### Problem 12. Complete Model and Computer Verification
A museum wants to create a rectangular exhibition room next to an existing straight wall. The side along the wall does not need to be built. The remaining three sides are to be constructed to two different standards: the two sides perpendicular to the wall cost $300\ \mathrm{PLN/m}$ each, while the side parallel to the wall costs $500\ \mathrm{PLN/m}$. The budget is $30\,000\ \mathrm{PLN}$.

Build a model that maximizes the area of the room and prepare a complete analysis containing:

- definition of variables and units,
- mathematical model,
- domain resulting from the problem statement,
- computation of the derivative,
- determination and verification of the optimum,
- interpretation of the result,
- graph of the objective function,
- numerical verification of several values near the optimum found.

Finally, indicate which part of the solution required modeling the problem and which part was only the execution of the calculation. Produce the graph and computer calculations only after completing the mathematical solution, and treat them as verification.

> **Why this problem:** it checks full transfer to a new problem with unequal side costs and integrates the process from model construction to independent verification.

#### Solution

1. **Definition of Variables and Units:**
   - $x$: length of the side parallel to the existing wall, measured in meters ($\mathrm{m}$).
   - $y$: length of each of the two sides perpendicular to the existing wall, measured in meters ($\mathrm{m}$).
   - $A$: enclosed area of the room, measured in square meters ($\mathrm{m}^2$).
   - Costs: $c_{\parallel} = 500\ \mathrm{PLN/m}$, $c_{\perp} = 300\ \mathrm{PLN/m}$. Total budget $B = 30\,000\ \mathrm{PLN}$.

2. **Mathematical Model:**
   - Objective: Maximize Area $A = x y$.
   - Budget constraint:
     $$500x + 2(300)y = 30\,000 \implies 500x + 600y = 30\,000.$$
     Divide by $100$:
     $$5x + 6y = 300 \implies y = \frac{300 - 5x}{6} = 50 - \frac{5}{6}x.$$
   - Area objective function in one variable:
     $$A(x) = x\left(50 - \frac{5}{6}x\right) = 50x - \frac{5}{6}x^2.$$

3. **Domain:**
   Physical lengths must be strictly positive:
   $$x > 0 \quad \text{and} \quad y = 50 - \frac{5}{6}x > 0 \implies 5x < 300 \implies x < 60.$$
   $$D_A = (0, 60).$$

4. **Computation of the Derivative:**
   $$A'(x) = \frac{d}{dx}\left(50x - \frac{5}{6}x^2\right) = 50 - \frac{5}{3}x.$$

5. **Determination and Verification of the Optimum:**
   Set $A'(x) = 0$:
   $$50 - \frac{5}{3}x = 0 \implies \frac{5}{3}x = 50 \implies x = 50 \cdot \frac{3}{5} = 30\ \mathrm{m}.$$
   Corresponding perpendicular dimension:
   $$y = 50 - \frac{5}{6}(30) = 50 - 25 = 25\ \mathrm{m}.$$
   - Verification of Maximum:
     $$A''(x) = -\frac{5}{3} < 0 \quad \text{for all } x.$$
     Because $A''(x) < 0$ globally on $(0, 60)$, $x = 30\ \mathrm{m}$ yields a strict global maximum.
   - Maximum Area:
     $$A_{\max} = 30 \times 25 = 750\ \mathrm{m}^2.$$

6. **Interpretation of the Result:**
   - Cost of parallel side: $30\ \mathrm{m} \times 500\ \mathrm{PLN/m} = 15\,000\ \mathrm{PLN}$.
   - Cost of two perpendicular sides: $2 \times (25\ \mathrm{m} \times 300\ \mathrm{PLN/m}) = 15\,000\ \mathrm{PLN}$.
   - The optimum splits the budget exactly in half ($50\%$ to the parallel side, $50\%$ to the perpendicular sides combined).

7. **Numerical Verification Near the Optimum:**
   - At $x = 26$: $y = 50 - \frac{130}{6} \approx 28.333\ \mathrm{m} \implies A = 26(28.333) \approx 736.67\ \mathrm{m}^2 < 750$.
   - At $x = 28$: $y = 50 - \frac{140}{6} \approx 26.667\ \mathrm{m} \implies A = 28(26.667) \approx 746.67\ \mathrm{m}^2 < 750$.
   - At **$x = 30$**: $y = 25.000\ \mathrm{m} \implies A = 30(25) = \mathbf{750.00\ \mathrm{m}^2}$ (**Global Maximum**).
   - At $x = 32$: $y = 50 - \frac{160}{6} \approx 23.333\ \mathrm{m} \implies A = 32(23.333) \approx 746.67\ \mathrm{m}^2 < 750$.
   - At $x = 34$: $y = 50 - \frac{170}{6} \approx 21.667\ \mathrm{m} \implies A = 34(21.667) \approx 736.67\ \mathrm{m}^2 < 750$.
   The values fall off symmetrically on either side of $x = 30$.

8. **Modeling vs. Execution:**
   - **Modeling Phase:** Identifying the variables $x, y$, interpreting the verbal budget constraint ($500x + 600y = 30\,000$), expressing $y$ in terms of $x$, establishing the objective function $A(x) = 50x - \frac{5}{6}x^2$, and recognizing the geometric domain $x \in (0, 60)$. This requires mathematical abstraction and translation.
   - **Execution Phase:** Computing $A'(x)$, setting it to $0$, solving the linear equation $x = 30$, and evaluating $A''(x) = -5/3 < 0$. This is purely algorithmic calculation.
