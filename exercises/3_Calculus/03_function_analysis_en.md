# Function Analysis

## Goal of the Problem Set

The student should be able to combine the domain, zeros, limits, derivatives, monotonicity, extrema, convexity, and asymptotes into one coherent description of a function and, on this basis, sketch its graph.

## Basic Problems

### Problem 1. A Cubic Polynomial
Analyze the monotonicity and extrema of
$$f(x)=x^3-3x^2+2.$$
Sketch the graph based on the results and mark the critical points.

> **Why this problem:** it teaches how to use the first derivative to describe the shape of a polynomial.

#### Solution

1. **Compute Derivative and Critical Points:**
   $$f'(x) = 3x^2 - 6x = 3x(x - 2).$$
   Set $f'(x) = 0 \implies x = 0$ or $x = 2$.

2. **Sign of $f'(x)$ and Monotonicity:**
   - On $(-\infty, 0)$: $x < 0$ and $x - 2 < 0 \implies f'(x) > 0 \implies f$ is **strictly increasing**.
   - On $(0, 2)$: $x > 0$ and $x - 2 < 0 \implies f'(x) < 0 \implies f$ is **strictly decreasing**.
   - On $(2, \infty)$: $x > 0$ and $x - 2 > 0 \implies f'(x) > 0 \implies f$ is **strictly increasing**.

3. **Determine Extrema:**
   - At $x = 0$: $f'$ changes from positive to negative $\implies$ **Local Maximum**:
     $$f(0) = 0^3 - 3(0)^2 + 2 = 2 \implies (0, 2).$$
   - At $x = 2$: $f'$ changes from negative to positive $\implies$ **Local Minimum**:
     $$f(2) = 2^3 - 3(2)^2 + 2 = 8 - 12 + 2 = -2 \implies (2, -2).$$

4. **Inflection Point:**
   $$f''(x) = 6x - 6 = 0 \implies x = 1, \qquad f(1) = 1 - 3 + 2 = 0 \implies (1, 0).$$

---

### Problem 2. A Parabola from the Perspective of the Derivative
For $f(x)=x^2-4x+1$, find the minimum using the derivative. Compare the result with the vertex form and explain why both approaches lead to the same point.

> **Why this problem:** it connects a new tool with the familiar geometry of a parabola.

#### Solution

1. **Derivative Method:**
   $$f'(x) = 2x - 4.$$
   Setting $f'(x) = 0 \implies 2x = 4 \implies x = 2$.
   Second derivative: $f''(x) = 2 > 0$, confirming a local and global minimum.
   $$f(2) = 2^2 - 4(2) + 1 = 4 - 8 + 1 = -3.$$
   Minimum point: $(2, -3)$.

2. **Vertex Form Method:**
   Complete the square:
   $$f(x) = (x^2 - 4x + 4) - 4 + 1 = (x - 2)^2 - 3.$$
   Since $(x - 2)^2 \ge 0$ for all real $x$, the minimum value $-3$ is attained when $(x - 2)^2 = 0 \iff x = 2$.
   Vertex: $(2, -3)$.

3. **Why Both Approaches Agree:**
   The vertex of an upward-opening parabola is its turning point where the slope of the curve transitions from negative to positive. At this exact turning point, the tangent line is horizontal ($f'(x) = 0$). Differentiating identifies the location of zero slope, which is identical to setting the squared term in vertex form to zero.

---

### Problem 3. A Rational Function
Analyze the domain, zeros, asymptotes, and monotonicity of
$$f(x)=\frac{x+1}{x-2}.$$
Finally, sketch a graph consistent with all the information obtained.

> **Why this problem:** it teaches how to combine the domain, limits, and derivative in the analysis of a rational function.

#### Solution

1. **Domain:**
   $$x - 2 \neq 0 \implies D_f = (-\infty, 2) \cup (2, \infty) = \mathbb{R} \setminus \{2\}.$$

2. **Zeros and Intercepts:**
   - $f(x) = 0 \iff x + 1 = 0 \implies x = -1$. Point: $(-1, 0)$.
   - $y$-intercept: $f(0) = \frac{0 + 1}{0 - 2} = -\frac{1}{2} = -0.5$. Point: $(0, -0.5)$.

3. **Asymptotes:**
   - **Vertical Asymptote at $x = 2$:**
     $$\lim_{x\to2^-}\frac{x+1}{x-2} = \frac{3}{0^-} = -\infty, \qquad \lim_{x\to2^+}\frac{x+1}{x-2} = \frac{3}{0^+} = +\infty.$$
   - **Horizontal Asymptote:**
     $$\lim_{x\to\pm\infty}\frac{x+1}{x-2} = \lim_{x\to\pm\infty}\frac{1 + \frac{1}{x}}{1 - \frac{2}{x}} = 1 \implies y = 1.$$

4. **Derivative and Monotonicity:**
   $$f'(x) = \frac{1(x - 2) - (x + 1)(1)}{(x - 2)^2} = \frac{x - 2 - x - 1}{(x - 2)^2} = -\frac{3}{(x - 2)^2}.$$
   Since $(x - 2)^2 > 0$ for all $x \in D_f$, $f'(x) < 0$ everywhere on its domain.
   The function is **strictly decreasing on $(-\infty, 2)$** and **strictly decreasing on $(2, \infty)$**. It has no local extrema.

---

### Problem 4. A Function with Two Vertical Asymptotes
Analyze
$$f(x)=\frac1{x^2-1}.$$
Determine the domain, asymptotes, sign, and monotonicity on the intervals of the domain. Explain why each interval must be analyzed separately.

> **Why this problem:** it practices the analysis of a function on several disjoint intervals.

#### Solution

1. **Domain:**
   $$x^2 - 1 \neq 0 \iff x \neq \pm 1 \implies D_f = (-\infty, -1) \cup (-1, 1) \cup (1, \infty).$$

2. **Asymptotes:**
   - Vertical at $x = -1$: $\lim_{x\to -1^-} f(x) = +\infty$, $\lim_{x\to -1^+} f(x) = -\infty$.
   - Vertical at $x = 1$: $\lim_{x\to 1^-} f(x) = -\infty$, $\lim_{x\to 1^+} f(x) = +\infty$.
   - Horizontal: $\lim_{x\to\pm\infty}\frac{1}{x^2-1} = 0 \implies y = 0$.

3. **Sign of $f(x)$:**
   - On $(-\infty, -1)$: $x^2 - 1 > 0 \implies f(x) > 0$.
   - On $(-1, 1)$: $x^2 - 1 < 0 \implies f(x) < 0$.
   - On $(1, \infty)$: $x^2 - 1 > 0 \implies f(x) > 0$.

4. **Derivative and Monotonicity:**
   $$f'(x) = -\frac{2x}{(x^2 - 1)^2}.$$
   Since $(x^2 - 1)^2 > 0$ on $D_f$, the sign of $f'(x)$ is opposite to the sign of $x$:
   - On $(-\infty, -1)$: $x < 0 \implies f'(x) > 0 \implies$ **strictly increasing**.
   - On $(-1, 0)$: $x < 0 \implies f'(x) > 0 \implies$ **strictly increasing**.
   - At $x = 0$: $f'(0) = 0$, giving a **local maximum** at $(0, -1)$.
   - On $(0, 1)$: $x > 0 \implies f'(x) < 0 \implies$ **strictly decreasing**.
   - On $(1, \infty)$: $x > 0 \implies f'(x) < 0 \implies$ **strictly decreasing**.

5. **Why Intervals Must Be Analyzed Separately:**
   The function domain is disconnected, split by two infinite singularities. A function cannot be called "decreasing on $(-\infty, -1) \cup (1, \infty)$" because comparing a point from the first interval (where $f > 0$) with a point from the second could falsely contradict monotonicity. Monotonicity theorems apply strictly to connected intervals.

---

### Problem 5. An Exponential Function with a Maximum
Analyze the monotonicity and extrema of
$$f(x)=xe^{-x}.$$
Also examine the behavior as $x\to\infty$ and explain how the limit affects the shape of the graph on the right-hand side.

> **Why this problem:** it combines the derivative with a limit in the description of the global behavior of a function.

#### Solution

1. **Derivative and Critical Points:**
   $$f'(x) = 1\cdot e^{-x} + x(-e^{-x}) = (1 - x)e^{-x}.$$
   Since $e^{-x} > 0$ for all $x \in \mathbb{R}$, $f'(x) = 0 \iff 1 - x = 0 \iff x = 1$.

2. **Monotonicity and Extrema:**
   - For $x < 1$: $1 - x > 0 \implies f'(x) > 0 \implies f$ is **strictly increasing**.
   - For $x > 1$: $1 - x < 0 \implies f'(x) < 0 \implies f$ is **strictly decreasing**.
   - At $x = 1$: $f'$ changes from positive to negative, giving a **global maximum**:
     $$f(1) = 1 \cdot e^{-1} = \frac{1}{e} \approx 0.3679 \implies \left(1, \frac{1}{e}\right).$$

3. **Behavior as $x \to \infty$:**
   $$\lim_{x\to\infty} x e^{-x} = \lim_{x\to\infty}\frac{x}{e^x} = \lim_{x\to\infty}\frac{1}{e^x} = 0 \quad (\text{by l'Hôpital's Rule}).$$
   Also notice that for all $x > 0$, $f(x) > 0$.
   - **Effect on the graph:** After reaching its peak at $\left(1, \frac{1}{e}\right)$, the graph decreases smoothly, asymptotically flattening against the horizontal axis $y = 0$ from above without ever crossing it. (An inflection point occurs at $x = 2$, where $f''(x) = (x-2)e^{-x} = 0$, transitioning the curve from concave down to concave up).

---

### Problem 6. A Logarithmic Function
Analyze the domain, zero, and monotonicity of
$$f(x)=\ln x-x+1.$$
Explain why the analysis must begin with the domain.

> **Why this problem:** it reinforces the role of the domain and derivative in the analysis of a logarithmic function.

#### Solution

1. **Domain:**
   The natural logarithm is defined strictly for positive arguments:
   $$D_f = (0, \infty).$$
   - **Why analysis must begin with the domain:** Mathematical expressions cannot be analyzed in regions where they do not exist. Ignoring the domain could lead to false conclusions such as attempting to evaluate limits at negative numbers, looking for nonexistent zeros at $x \le 0$, or assuming the function is defined on all of $\mathbb{R}$.

2. **Derivative and Critical Points:**
   $$f'(x) = \frac{1}{x} - 1 = \frac{1 - x}{x}.$$
   On $D_f = (0, \infty)$, the denominator $x > 0$ is always positive.
   $$f'(x) = 0 \iff 1 - x = 0 \iff x = 1.$$

3. **Monotonicity:**
   - On $(0, 1)$: $1 - x > 0 \implies f'(x) > 0 \implies f$ is **strictly increasing**.
   - On $(1, \infty)$: $1 - x < 0 \implies f'(x) < 0 \implies f$ is **strictly decreasing**.
   Thus, $f(x)$ has an absolute global maximum at $x = 1$.

4. **Zeros:**
   Evaluate at the maximum point:
   $$f(1) = \ln(1) - 1 + 1 = 0 - 0 = 0.$$
   Because the maximum value of the function is $0$, we have $f(x) \le 0$ for all $x > 0$. Consequently, $x = 1$ is the **unique zero** of the function.

---

### Problem 7. A Trigonometric Function
On $[0,2\pi]$, find the intervals of monotonicity and the extrema of
$$f(x)=\sin x+\cos x.$$
Include the endpoints of the interval and compare the function values at the critical points and at the endpoints.

> **Why this problem:** it practices the analysis of a periodic function on a bounded interval.

#### Solution

1. **Derivative and Critical Points on $[0, 2\pi]$:**
   $$f'(x) = \cos x - \sin x.$$
   $$f'(x) = 0 \iff \cos x = \sin x \iff \tan x = 1.$$
   On $[0, 2\pi]$, the critical points are:
   $$x_1 = \frac{\pi}{4}, \qquad x_2 = \frac{5\pi}{4}.$$

2. **Monotonicity Intervals:**
   - On $\left[0, \frac{\pi}{4}\right)$: $\cos x > \sin x \implies f'(x) > 0 \implies$ **increasing**.
   - On $\left(\frac{\pi}{4}, \frac{5\pi}{4}\right)$: $\cos x < \sin x \implies f'(x) < 0 \implies$ **decreasing**.
   - On $\left(\frac{5\pi}{4}, 2\pi\right]$: $\cos x > \sin x \implies f'(x) > 0 \implies$ **increasing**.

3. **Evaluate Function at Critical Points and Endpoints:**
   - At left endpoint $x = 0$: $f(0) = \sin 0 + \cos 0 = 1$.
   - At critical point $x = \frac{\pi}{4}$:
     $$f\left(\frac{\pi}{4}\right) = \sin\frac{\pi}{4} + \cos\frac{\pi}{4} = \frac{\sqrt{2}}{2} + \frac{\sqrt{2}}{2} = \sqrt{2} \approx 1.414 \quad (\textbf{Absolute Maximum}).$$
   - At critical point $x = \frac{5\pi}{4}$:
     $$f\left(\frac{5\pi}{4}\right) = \sin\frac{5\pi}{4} + \cos\frac{5\pi}{4} = -\frac{\sqrt{2}}{2} - \frac{\sqrt{2}}{2} = -\sqrt{2} \approx -1.414 \quad (\textbf{Absolute Minimum}).$$
   - At right endpoint $x = 2\pi$: $f(2\pi) = \sin 2\pi + \cos 2\pi = 1$.

---

### Problem 8. The Second Derivative
For
$$f(x)=x^4-4x^2$$
find the local extrema, intervals of convexity and concavity, and inflection points. Sketch the graph and mark all the identified features on it.

> **Why this problem:** it introduces the second derivative as a tool for describing the curvature of a graph.

#### Solution

1. **First Derivative and Local Extrema:**
   $$f'(x) = 4x^3 - 8x = 4x(x^2 - 2) = 4x(x - \sqrt{2})(x + \sqrt{2}).$$
   Critical points: $x = -\sqrt{2}, 0, \sqrt{2}$.
   - At $x = \pm\sqrt{2}$: $f(\pm\sqrt{2}) = (\sqrt{2})^4 - 4(\sqrt{2})^2 = 4 - 8 = -4 \implies$ **Local Minima** at $(-\sqrt{2}, -4)$ and $(\sqrt{2}, -4)$.
   - At $x = 0$: $f(0) = 0 \implies$ **Local Maximum** at $(0, 0)$.

2. **Second Derivative, Inflection Points, and Convexity:**
   $$f''(x) = 12x^2 - 8 = 4(3x^2 - 2).$$
   $$f''(x) = 0 \iff 3x^2 = 2 \iff x = \pm\sqrt{\frac{2}{3}} = \pm\frac{\sqrt{6}}{3} \approx \pm 0.8165.$$
   - On $\left(-\infty, -\sqrt{\frac{2}{3}}\right)$: $f''(x) > 0 \implies$ **Convex (concave up)**.
   - On $\left(-\sqrt{\frac{2}{3}}, \sqrt{\frac{2}{3}}\right)$: $f''(x) < 0 \implies$ **Concave (concave down)**.
   - On $\left(\sqrt{\frac{2}{3}}, \infty\right)$: $f''(x) > 0 \implies$ **Convex (concave up)**.
   **Inflection Points:**
   $$f\left(\pm\sqrt{\frac{2}{3}}\right) = \left(\frac{2}{3}\right)^2 - 4\left(\frac{2}{3}\right) = \frac{4}{9} - \frac{8}{3} = -\frac{20}{9} \approx -2.22.$$
   Points: $\left(-\sqrt{\frac{2}{3}}, -\frac{20}{9}\right)$ and $\left(\sqrt{\frac{2}{3}}, -\frac{20}{9}\right)$.

---

### Problem 9. An Oblique Asymptote
Analyze the asymptotes of
$$f(x)=\frac{x^2+1}{x-1}.$$
Perform polynomial division and explain why the remainder term vanishes for large $|x|$.

> **Why this problem:** it teaches how to recognize an oblique asymptote and interpret the decomposition of a function.

#### Solution

1. **Polynomial Division:**
   Divide $(x^2 + 1)$ by $(x - 1)$:
   $$x^2 + 1 = (x + 1)(x - 1) + 2.$$
   $$f(x) = \frac{x^2+1}{x-1} = x + 1 + \frac{2}{x - 1}.$$

2. **Asymptotes Analysis:**
   - **Vertical Asymptote:** At $x = 1$, the denominator vanishes:
     $$\lim_{x\to1^-} f(x) = -\infty, \qquad \lim_{x\to1^+} f(x) = +\infty.$$
   - **Oblique (Slant) Asymptote:** $y = x + 1$.

3. **Why the Remainder Vanishes for Large $|x|$:**
   The difference between the curve $f(x)$ and the line $y = x + 1$ is precisely the remainder term:
   $$f(x) - (x + 1) = \frac{2}{x - 1}.$$
   Taking the limit as $|x| \to \infty$:
   $$\lim_{x\to\pm\infty}\left[f(x) - (x + 1)\right] = \lim_{x\to\pm\infty}\frac{2}{x - 1} = 0.$$
   As $x$ becomes very large, the constant numerator $2$ is divided by an arbitrarily large number, driving the vertical separation to zero. The curve becomes indistinguishable from the straight line $y = x + 1$.

---

### Problem 10. Complete Function Analysis
Perform a complete analysis of
$$f(x)=\frac{x}{x^2+1}.$$
Include the domain, symmetry, zeros, limits, monotonicity, extrema, and convexity. Finally, produce a sketch based only on this information.

> **Why this problem:** it combines all the basic elements of function analysis into one organized process.

#### Solution

1. **Domain:**
   Since $x^2 + 1 \ge 1 > 0$ for all $x$, there are no real zeros in the denominator:
   $$D_f = \mathbb{R}.$$

2. **Symmetry:**
   $$f(-x) = \frac{-x}{(-x)^2 + 1} = -\frac{x}{x^2 + 1} = -f(x).$$
   The function is **odd**, which means its graph is symmetric with respect to the origin $(0, 0)$.

3. **Zeros and Intercepts:**
   $$f(x) = 0 \iff x = 0 \implies (0, 0).$$

4. **Limits and Asymptotes:**
   $$\lim_{x\to\pm\infty}\frac{x}{x^2+1} = \lim_{x\to\pm\infty}\frac{\frac{1}{x}}{1 + \frac{1}{x^2}} = 0.$$
   Horizontal asymptote: $y = 0$ as $x \to \pm\infty$. No vertical asymptotes exist.

5. **First Derivative, Monotonicity, and Extrema:**
   $$f'(x) = \frac{1(x^2+1) - x(2x)}{(x^2+1)^2} = \frac{1 - x^2}{(x^2+1)^2} = \frac{(1 - x)(1 + x)}{(x^2+1)^2}.$$
   Critical points: $x = -1$ and $x = 1$.
   - On $(-\infty, -1)$: $f'(x) < 0 \implies$ decreasing.
   - On $(-1, 1)$: $f'(x) > 0 \implies$ increasing.
   - On $(1, \infty)$: $f'(x) < 0 \implies$ decreasing.
   - **Local and global minimum:** at $x = -1$, $f(-1) = -\frac{1}{2} \implies \left(-1, -\frac{1}{2}\right)$.
   - **Local and global maximum:** at $x = 1$, $f(1) = \frac{1}{2} \implies \left(1, \frac{1}{2}\right)$.

6. **Second Derivative, Inflection Points, and Convexity:**
   $$f''(x) = \frac{-2x(x^2+1)^2 - (1 - x^2)\cdot 2(x^2+1)(2x)}{(x^2+1)^4} = \frac{-2x(x^2+1) - 4x(1 - x^2)}{(x^2+1)^3} = \frac{2x(x^2 - 3)}{(x^2+1)^3}.$$
   Inflection points: $x = -\sqrt{3}, 0, \sqrt{3}$.
   - Concave on $(-\infty, -\sqrt{3})$ and $(0, \sqrt{3})$.
   - Convex on $(-\sqrt{3}, 0)$ and $(\sqrt{3}, \infty)$.
   Inflection coordinates: $\left(-\sqrt{3}, -\frac{\sqrt{3}}{4}\right)$, $(0, 0)$, and $\left(\sqrt{3}, \frac{\sqrt{3}}{4}\right)$.

---

## More Difficult Problems

### Problem 11. A Parameter and the Number of Extrema
For
$$f_a(x)=x^3-3ax$$
depending on $a$, determine the number of critical points and their character. Separate the parameter cases and justify why the structure of the graph changes.

> **Why this problem:** it teaches how to analyze an entire family of functions instead of a single example.

#### Solution

1. **Compute Derivative:**
   $$f_a'(x) = 3x^2 - 3a = 3(x^2 - a).$$
   Critical points satisfy $x^2 = a$.

2. **Case Analysis by Parameter $a$:**
   - **Case 1: $a > 0$:**
     $x^2 = a$ has two distinct real solutions: $x = -\sqrt{a}$ and $x = \sqrt{a}$.
     Second derivative: $f_a''(x) = 6x$.
     - At $x = -\sqrt{a}$: $f_a''(-\sqrt{a}) = -6\sqrt{a} < 0 \implies$ **Local Maximum** ($y = 2a\sqrt{a}$).
     - At $x = \sqrt{a}$: $f_a''(\sqrt{a}) = 6\sqrt{a} > 0 \implies$ **Local Minimum** ($y = -2a\sqrt{a}$).
     *Structure:* Classic two-turn cubic curve with two local extrema.
   - **Case 2: $a = 0$:**
     $f_0(x) = x^3$, $f_0'(x) = 3x^2 \ge 0$.
     The only critical point is $x = 0$. Since $f_0'(x) > 0$ for all $x \neq 0$, the function is strictly increasing on all of $\mathbb{R}$.
     *Structure:* $x = 0$ is a stationary inflection point, **no local extrema**.
   - **Case 3: $a < 0$:**
     $x^2 - a = x^2 + |a| > 0$ for all real $x$.
     $f_a'(x) > 0$ everywhere.
     *Structure:* The function is strictly monotonically increasing with **no critical points and no local extrema**.

3. **Why the Graph Structure Changes:**
   Varying $a$ shifts the quadratic derivative $3(x^2 - a)$ vertically. When $a > 0$, the parabola $y = 3x^2 - 3a$ dips below the $x$-axis, creating two crossings (sign changes from positive to negative and back). At $a = 0$, the parabola touches the axis at a single point without crossing it. When $a < 0$, the derivative parabola is lifted entirely above the $x$-axis, eliminating all critical points.

---

### Problem 12. A Function with an Absolute Value
Analyze
$$f(x)=|x^2-4|.$$
First sketch $x^2-4$, then explain the effect of the absolute value. Indicate the points where the derivative does not exist and justify the reason geometrically.

> **Why this problem:** it shows the limits of mechanical application of calculus and the importance of the geometry of the graph.

#### Solution

1. **Base Function $g(x) = x^2 - 4$:**
   This is a standard parabola opening upwards with vertex at $(0, -4)$, axis of symmetry $x = 0$, and roots at $x = -2$ and $x = 2$.

2. **Effect of Absolute Value:**
   $$f(x) = |x^2 - 4| = \begin{cases} x^2 - 4, & \text{if } |x| \ge 2, \\ 4 - x^2, & \text{if } |x| < 2. \end{cases}$$
   The absolute value leaves the positive portions ($|x| \ge 2$) unchanged, while reflecting the negative dip ($x \in (-2, 2)$) vertically across the $x$-axis, turning the valley at $(0, -4)$ into an inverted parabolic peak at $(0, 4)$.

3. **Points Where the Derivative Does Not Exist:**
   The derivative does not exist at **$x = -2$** and **$x = 2$**.
   - **Analytical Justification at $x = 2$:**
     $$\lim_{x\to2^+}\frac{f(x) - f(2)}{x - 2} = \lim_{x\to2^+}\frac{(x^2 - 4) - 0}{x - 2} = \lim_{x\to2^+}(x + 2) = 4.$$
     $$\lim_{x\to2^-}\frac{f(x) - f(2)}{x - 2} = \lim_{x\to2^-}\frac{-(x^2 - 4) - 0}{x - 2} = \lim_{x\to2^-}-(x + 2) = -4.$$
     Since $f'_+(2) = 4 \neq -4 = f'_-(2)$, the derivative does not exist. (Similarly, $f'_+(-2) = 4 \neq -4 = f'_-(-2)$).
   - **Geometric Justification:**
     The sharp reflection at $y = 0$ creates sharp, non-smooth "creases" or corner points (cusps) at $(-2, 0)$ and $(2, 0)$. At these corners, the curve changes slope abruptly without turning smoothly, meaning no unique tangent line can be defined.

---

### Problem 13. A Logarithm and an Asymptote
Perform a complete analysis of
$$f(x)=\frac{\ln x}{x},\qquad x>0.$$
Find the maximum and the behavior at the ends of the domain. Explain which information is necessary for a correct sketch.

> **Why this problem:** it combines the domain, limits, and derivative in a less obvious example.

#### Solution

1. **Domain and Zeros:**
   - Domain: $D_f = (0, \infty)$.
   - Zero: $\ln x = 0 \iff x = 1 \implies (1, 0)$.
   - Sign: $f(x) < 0$ for $x \in (0, 1)$, and $f(x) > 0$ for $x \in (1, \infty)$.

2. **Behavior at Ends of Domain:**
   - As $x \to 0^+$:
     $$\lim_{x\to0^+}\frac{\ln x}{x} = \frac{-\infty}{0^+} = -\infty.$$
     Vertical asymptote: $x = 0$ (the $y$-axis).
   - As $x \to \infty$:
     $$\lim_{x\to\infty}\frac{\ln x}{x} = \lim_{x\to\infty}\frac{\frac{1}{x}}{1} = 0 \quad (\text{by l'Hôpital's Rule}).$$
     Horizontal asymptote: $y = 0$ as $x \to \infty$.

3. **Derivative, Monotonicity, and Maximum:**
   $$f'(x) = \frac{\left(\frac{1}{x}\right)x - (\ln x)(1)}{x^2} = \frac{1 - \ln x}{x^2}.$$
   Critical point: $1 - \ln x = 0 \iff \ln x = 1 \iff x = e \approx 2.718$.
   - On $(0, e)$: $1 - \ln x > 0 \implies f'(x) > 0 \implies$ **strictly increasing**.
   - On $(e, \infty)$: $1 - \ln x < 0 \implies f'(x) < 0 \implies$ **strictly decreasing**.
   - **Absolute Maximum:** At $x = e$,
     $$f(e) = \frac{\ln e}{e} = \frac{1}{e} \approx 0.3679 \implies \left(e, \frac{1}{e}\right).$$

4. **Curvature and Inflection:**
   $$f''(x) = \frac{\left(-\frac{1}{x}\right)x^2 - (1 - \ln x)(2x)}{x^4} = \frac{-x - 2x + 2x\ln x}{x^4} = \frac{2\ln x - 3}{x^3}.$$
   Inflection point: $2\ln x - 3 = 0 \implies \ln x = \frac{3}{2} \implies x = e^{3/2} \approx 4.48$, with $y = \frac{1.5}{e^{3/2}} \approx 0.335$.

5. **Information Necessary for a Correct Sketch:**
   - Vertical asymptote plunging toward $-\infty$ as $x \to 0^+$.
   - Zero crossing at $(1, 0)$.
   - Global peak at $\left(e, \frac{1}{e}\right)$.
   - Inflection point at $x = e^{3/2}$ where concavity changes from downward to upward.
   - Long right-hand tail remaining positive while asymptotically approaching $y = 0$.

---

### Problem 14. Reconstructing Information from the Derivative
It is known that
$$f'(x)=(x-1)(x+2).$$
Determine the monotonicity and the locations of the extrema, and sketch a possible qualitative shape of the function. Then, for
$$g(x)=\frac{x^3}{3}+\frac{x^2}{2}-2x$$
verify that $g'(x)=(x-1)(x+2)$, and compare the specific graph with the earlier qualitative sketch.

> **Why this problem:** it teaches how to read the behavior of a function directly from its derivative.

#### Solution

1. **Monotonicity and Extrema from $f'(x) = (x - 1)(x + 2)$:**
   Roots of $f'(x)$: $x = -2$ and $x = 1$.
   The derivative is an upward-opening parabola ($x^2 + x - 2$):
   - On $(-\infty, -2)$: $f'(x) > 0 \implies f$ is **strictly increasing**.
   - On $(-2, 1)$: $f'(x) < 0 \implies f$ is **strictly decreasing**.
   - On $(1, \infty)$: $f'(x) > 0 \implies f$ is **strictly increasing**.
   **Extrema:**
   - At $x = -2$: $f'$ changes from $+$ to $-$ $\implies$ **Local Maximum**.
   - At $x = 1$: $f'$ changes from $-$ to $+$ $\implies$ **Local Minimum**.

2. **Qualitative Shape:**
   The function rises from $-\infty$ to a local peak at $x = -2$, drops down to a local valley at $x = 1$, and then rises toward $+\infty$.

3. **Verify $g'(x)$:**
   $$g(x) = \frac{x^3}{3} + \frac{x^2}{2} - 2x.$$
   $$g'(x) = \frac{3x^2}{3} + \frac{2x}{2} - 2 = x^2 + x - 2 = (x - 1)(x + 2).$$
   The derivative matches $f'(x)$ identically.

4. **Specific Values for $g(x)$:**
   - Local maximum value at $x = -2$:
     $$g(-2) = \frac{(-2)^3}{3} + \frac{(-2)^2}{2} - 2(-2) = -\frac{8}{3} + 2 + 4 = -\frac{8}{3} + 6 = \frac{10}{3} \approx 3.33.$$
   - Local minimum value at $x = 1$:
     $$g(1) = \frac{1}{3} + \frac{1}{2} - 2 = \frac{5}{6} - 2 = -\frac{7}{6} \approx -1.17.$$
   - Intercept: $g(0) = 0$.
   The concrete graph of $g(x)$ has its peak at $\left(-2, \frac{10}{3}\right)$ and its valley at $\left(1, -\frac{7}{6}\right)$, perfectly validating the qualitative sketch deduced from the derivative.

---

### Problem 15. Find the Error in the Monotonicity Analysis
For the function
$$f(x)=x^3-3x$$
the derivative was correctly computed as
$$f'(x)=3(x-1)(x+1).$$

However, a student wrote the following conclusion:

> The derivative is positive between its zeros and negative outside them. Therefore, the function is decreasing on $(-\infty,-1)\cup(1,\infty)$, increasing on $(-1,1)$, has a local minimum at $x=-1$, and a local maximum at $x=1$.

1. Without differentiating again, explain why merely identifying the zeros of the derivative does not justify the stated sign chart, and find the error in the student's reasoning.
2. Construct the correct sign chart for $f'(x)$.
3. Give the correct intervals of monotonicity and the character of the extrema.
4. In each of the three intervals, choose one simple test point and show that the sign of the derivative confirms your classification.

> **Why this problem:** it teaches how to diagnose an error in a completed argument and shows that a correct derivative formula is not enough if its sign is interpreted incorrectly.

#### Solution

1. **Diagnosis of the Error:**
   The derivative $f'(x) = 3(x^2 - 1) = 3x^2 - 3$ is a quadratic polynomial with a positive leading coefficient ($a = 3 > 0$). The graph of $f'(x)$ is an upward-opening parabola.
   An upward-opening parabola is **negative between its roots** (below the $x$-axis) and **positive outside its roots** (above the $x$-axis).
   The student made the fundamental error of reversing the sign chart, assuming the parabola was positive inside the roots, which resulted in asserting exactly the opposite behavior for monotonicity and misidentifying maxima as minima.

2. **Correct Sign Chart for $f'(x) = 3(x - 1)(x + 1)$:**
   $$\begin{array}{c|c|c|c|c|c}
   x & (-\infty, -1) & -1 & (-1, 1) & 1 & (1, \infty) \\ \hline
   f'(x) & + & 0 & - & 0 & + \\ \hline
   f(x) & \nearrow & \text{Local Max} & \searrow & \text{Local Min} & \nearrow
   \end{array}$$

3. **Correct Monotonicity and Extrema:**
   - $f$ is **strictly increasing** on $(-\infty, -1]$ and on $[1, \infty)$.
   - $f$ is **strictly decreasing** on $[-1, 1]$.
   - At $x = -1$: derivative changes from positive to negative $\implies$ **Local Maximum** at $(-1, f(-1)) = (-1, 2)$.
   - At $x = 1$: derivative changes from negative to positive $\implies$ **Local Minimum** at $(1, f(1)) = (1, -2)$.

4. **Confirmation via Test Points:**
   - **Interval $(-\infty, -1)$:** Choose $x = -2$:
     $$f'(-2) = 3(-2 - 1)(-2 + 1) = 3(-3)(-1) = +9 > 0 \quad (\text{increasing, confirms }+).$$
   - **Interval $(-1, 1)$:** Choose $x = 0$:
     $$f'(0) = 3(0 - 1)(0 + 1) = 3(-1)(1) = -3 < 0 \quad (\text{decreasing, confirms }-).$$
   - **Interval $(1, \infty)$:** Choose $x = 2$:
     $$f'(2) = 3(2 - 1)(2 + 1) = 3(1)(3) = +9 > 0 \quad (\text{increasing, confirms }+).$$
