# Derivatives

## Goal of the Problem Set

The student should understand the derivative as a rate of change and the slope of a tangent line, and should be able to apply the basic differentiation rules: the sum rule, product rule, quotient rule, chain rule, and derivatives of trigonometric, exponential, and logarithmic functions.

Obtaining a formula for the derivative is not the end of the task. The student should be able to explain **why a particular rule is being used** and, in at least some problems, connect the result with slope, the sign of the derivative, or a simple verification.

## Basic Problems

### Problem 1. Derivative of a Polynomial and the Slope of a Tangent Line
For
$$f(x)=3x^5-2x^3+7x-4$$
find $f'(x)$. Then compute $f'(0)$ and $f'(1)$, determine the signs of the obtained values, and explain what they say about the slope of the tangent line to the graph at these two points.

> **Why this problem:** it reinforces the power rule and connects the value of the derivative at a point with the geometric meaning of the tangent slope.

#### Solution

1. **Differentiate using Power and Sum Rules:**
   $$\frac{d}{dx}(x^n) = n x^{n-1}, \qquad \frac{d}{dx}(c) = 0.$$
   $$f'(x) = 3(5x^4) - 2(3x^2) + 7(1) - 0 = 15x^4 - 6x^2 + 7.$$

2. **Evaluate at Points $x=0$ and $x=1$:**
   $$f'(0) = 15(0)^4 - 6(0)^2 + 7 = 7.$$
   $$f'(1) = 15(1)^4 - 6(1)^2 + 7 = 15 - 6 + 7 = 16.$$

3. **Signs and Geometric Meaning:**
   - Both $f'(0) = 7 > 0$ and $f'(1) = 16 > 0$ are **strictly positive**.
   - A positive derivative indicates that the function is strictly increasing at both points, meaning the tangent lines tilt upward from left to right.
   - At $x = 0$, the tangent line has slope $m = 7$. At $x = 1$, the tangent line has slope $m = 16$, which is more than twice as steep as at $x = 0$.

---

### Problem 2. Powers, Roots, and the Domain
For
$$f(x)=2\sqrt{x}-\frac{3}{x^2}+x^{3/2}$$
1. rewrite the function using powers,
2. determine the domain,
3. compute the derivative,
4. compare the domain of the function with the domain of its derivative.

> **Why this problem:** it teaches how to rewrite different forms so that the power rule can be applied and how to keep track of the domain.

#### Solution

1. **Rewrite Using Fractional and Negative Powers:**
   $$f(x) = 2x^{1/2} - 3x^{-2} + x^{3/2}.$$

2. **Domain of $f(x)$:**
   - $2\sqrt{x} = 2x^{1/2}$ requires $x \ge 0$.
   - $-\frac{3}{x^2} = -3x^{-2}$ requires denominator $x \neq 0$.
   - $x^{3/2} = (\sqrt{x})^3$ requires $x \ge 0$.
   Intersecting these conditions gives:
   $$D_f = (0, \infty) = \{x \in \mathbb{R} : x > 0\}.$$

3. **Compute the Derivative:**
   $$f'(x) = 2\left(\frac{1}{2}x^{-1/2}\right) - 3\left(-2x^{-3}\right) + \frac{3}{2}x^{1/2} = x^{-1/2} + 6x^{-3} + \frac{3}{2}x^{1/2} = \frac{1}{\sqrt{x}} + \frac{6}{x^3} + \frac{3}{2}\sqrt{x}.$$

4. **Domain of $f'(x)$ and Comparison:**
   - In $f'(x)$, $\frac{1}{\sqrt{x}}$ requires $x > 0$, $\frac{6}{x^3}$ requires $x \neq 0$, and $\sqrt{x}$ requires $x \ge 0$.
   - Thus, $D_{f'} = (0, \infty)$.
   - **Comparison:** $D_f = D_{f'} = (0, \infty)$. While the square root function $\sqrt{x}$ alone is defined at $x=0$ but not differentiable there, in this combined function the term $-\frac{3}{x^2}$ already excluded $x = 0$ from the domain of $f$, making the domains of $f$ and $f'$ identical.

---

### Problem 3. The Product Rule — Why Is It Needed?
For
$$f(x)=(x^2+1)e^x$$
compute the derivative. Then compare the correct result with the incorrect idea
$$f'(x)\stackrel{?}{=}(2x)e^x$$
and explain which term is missing.

> **Why this problem:** it teaches the product rule by analyzing a common mistake.

#### Solution

1. **Product Rule Application:**
   $$(uv)' = u'v + uv'.$$
   Let $u(x) = x^2 + 1 \implies u'(x) = 2x$.
   Let $v(x) = e^x \implies v'(x) = e^x$.
   $$f'(x) = (2x)e^x + (x^2 + 1)e^x = (x^2 + 2x + 1)e^x = (x + 1)^2 e^x.$$

2. **Comparison with the Incorrect Formula:**
   The erroneous conjecture $f'(x) \stackrel{?}{=} (2x)e^x$ differentiates only the first factor ($u'$) and multiplies it by the un-differentiated second factor ($v$), assuming $(uv)' \stackrel{?}{=} u'v$.

3. **The Missing Term:**
   The missing term is:
   $$u v' = (x^2 + 1)\frac{d}{dx}(e^x) = (x^2 + 1)e^x.$$
   When two quantities vary simultaneously, the total rate of change must account for the change in both factors: the change in $u$ while $v$ is held fixed ($u'v$), plus the change in $v$ while $u$ is held fixed ($uv'$).

---

### Problem 4. A Quotient and Domain Control
For
$$f(x)=\frac{x^2+1}{x-1}$$
determine the domain, compute the derivative, simplify the result, and explain why the restriction $x\neq1$ remains important.

> **Why this problem:** it practices the quotient rule together with domain control.

#### Solution

1. **Domain:**
   The denominator cannot vanish: $x - 1 \neq 0 \implies x \neq 1$.
   $$D_f = \mathbb{R} \setminus \{1\} = (-\infty, 1) \cup (1, \infty).$$

2. **Compute Derivative via Quotient Rule:**
   $$\left(\frac{u}{v}\right)' = \frac{u'v - uv'}{v^2}.$$
   Let $u = x^2 + 1 \implies u' = 2x$, and $v = x - 1 \implies v' = 1$.
   $$f'(x) = \frac{2x(x - 1) - (x^2 + 1)(1)}{(x - 1)^2} = \frac{2x^2 - 2x - x^2 - 1}{(x - 1)^2} = \frac{x^2 - 2x - 1}{(x - 1)^2}.$$

3. **Why the Restriction $x \neq 1$ Remains Important:**
   At $x = 1$, the function has a vertical asymptote and is discontinuous. A function cannot have a derivative at a point where it is not even defined. Even though algebraic operations might yield a formal expression, $f'(x)$ is undefined at $x=1$, preserving $D_{f'} = D_f = \mathbb{R} \setminus \{1\}$.

---

### Problem 5. The Chain Rule as Working Through Layers
For
$$f(x)=(3x^2-2x+1)^5$$
identify the inner and outer functions, compute their derivatives, and combine the result according to the chain rule. Explain the origin of the additional factor.

> **Why this problem:** it teaches how to recognize the structure of a composition instead of memorizing the rule as a meaningless pattern.

#### Solution

1. **Identify Layers:**
   - **Outer function:** $g(u) = u^5$.
   - **Inner function:** $u(x) = 3x^2 - 2x + 1$.

2. **Compute Derivatives:**
   - Outer derivative: $g'(u) = 5u^4$.
   - Inner derivative: $u'(x) = 6x - 2 = 2(3x - 1)$.

3. **Combine via Chain Rule:**
   $$f'(x) = g'(u(x)) \cdot u'(x) = 5(3x^2 - 2x + 1)^4 \cdot (6x - 2) = 10(3x - 1)(3x^2 - 2x + 1)^4.$$

4. **Origin of the Additional Factor:**
   By the chain rule $\frac{df}{dx} = \frac{df}{du} \cdot \frac{du}{dx}$, a small nudge $\Delta x$ in $x$ causes an internal change $\Delta u \approx u'(x)\Delta x = (6x-2)\Delta x$. In turn, the outer power function responds to changes in $u$ by scaling them by $5u^4$. The total derivative with respect to $x$ must multiply these two sensitivities together. The factor $(6x - 2)$ is the rate at which the inner expression transmits change from $x$ to $u$.

---

### Problem 6. Product Rule and Trigonometry
For
$$f(x)=x\sin x+\cos x$$
compute the derivative and simplify the result. Then compute $f'(0)$ and interpret the direction of the tangent line at that point.

> **Why this problem:** it combines the product rule with trigonometric derivatives and geometric interpretation.

#### Solution

1. **Compute Derivative:**
   Apply the product rule to $x\sin x$:
   $$\frac{d}{dx}(x\sin x) = (1)\sin x + x(\cos x) = \sin x + x\cos x.$$
   Differentiate $\cos x$:
   $$\frac{d}{dx}(\cos x) = -\sin x.$$
   Combine:
   $$f'(x) = (\sin x + x\cos x) - \sin x = x\cos x.$$

2. **Evaluate $f'(0)$:**
   $$f'(0) = 0 \cdot \cos(0) = 0 \cdot 1 = 0.$$

3. **Interpretation of Tangent Line:**
   Because the derivative at $x = 0$ is zero ($m = f'(0) = 0$), the tangent line to the graph at the point $(0, f(0)) = (0, 1)$ is **horizontal** (equation: $y = 1$). The function has a stationary point at $x = 0$.

---

### Problem 7. A Trigonometric Composition
For
$$f(x)=\sin(x^2+1)$$
compute the derivative. Explicitly identify the outer function, the inner function, and the derivative of the inner function. Finally, determine the sign of $f'(0)$.

> **Why this problem:** it reinforces the chain rule in a different type of composition.

#### Solution

1. **Identify Components:**
   - **Outer function:** $g(u) = \sin u \implies g'(u) = \cos u$.
   - **Inner function:** $u(x) = x^2 + 1$.
   - **Derivative of the inner function:** $u'(x) = 2x$.

2. **Combine via Chain Rule:**
   $$f'(x) = g'(u(x)) \cdot u'(x) = \cos(x^2 + 1) \cdot (2x) = 2x\cos(x^2 + 1).$$

3. **Sign of $f'(0)$:**
   $$f'(0) = 2(0)\cos(0^2 + 1) = 0 \cdot \cos(1) = 0.$$
   The value is **zero** (neither strictly positive nor negative).

---

### Problem 8. Two Exponential Functions
For
$$f(x)=e^{2x-3}+5^x$$
compute the derivative. Explain why the factor $2$ appears in the first term and why $\ln5$ appears in the second.

> **Why this problem:** it organizes two different mechanisms that produce additional factors.

#### Solution

1. **Compute Derivative:**
   $$f'(x) = 2e^{2x-3} + 5^x \ln 5.$$

2. **Why the Factor $2$ Appears in the First Term:**
   The function $e^{2x-3}$ is a composite function with outer $e^u$ and inner $u(x) = 2x - 3$. By the chain rule:
   $$\frac{d}{dx}(e^{2x-3}) = e^{2x-3} \cdot \frac{d}{dx}(2x - 3) = e^{2x-3} \cdot 2 = 2e^{2x-3}.$$
   The factor $2$ is the derivative of the linear exponent.

3. **Why the Factor $\ln 5$ Appears in the Second Term:**
   The base of the exponential is $5$, not the natural base $e$. Using the identity $5 = e^{\ln 5}$, we write $5^x = (e^{\ln 5})^x = e^{x\ln 5}$. Differentiating with respect to $x$ using the chain rule:
   $$\frac{d}{dx}(5^x) = \frac{d}{dx}(e^{x\ln 5}) = e^{x\ln 5} \cdot \frac{d}{dx}(x\ln 5) = 5^x \ln 5.$$
   The factor $\ln 5$ is the scaling constant required to convert growth rates from base $5$ to the natural logarithmic scale.

---

### Problem 9. A Logarithm and the Chain Rule
For
$$f(x)=\ln(x^2+1)$$
compute the derivative. Then determine the sign of $f'(x)$ for $x<0$, $x=0$, and $x>0$, and describe qualitatively how the function behaves around zero.

> **Why this problem:** it connects differentiation with sign analysis and the behavior of a function.

#### Solution

1. **Compute Derivative via Chain Rule:**
   Outer function $\ln(u)$ with inner $u = x^2 + 1 > 0$:
   $$f'(x) = \frac{1}{x^2 + 1} \cdot \frac{d}{dx}(x^2 + 1) = \frac{2x}{x^2 + 1}.$$

2. **Sign Analysis of $f'(x)$:**
   Notice that the denominator $x^2 + 1 \ge 1 > 0$ is strictly positive for all real $x$. Thus, the sign of $f'(x)$ is identical to the sign of its numerator $2x$:
   - For $x < 0$: $f'(x) < 0$ (the function is **strictly decreasing**).
   - For $x = 0$: $f'(0) = 0$ (stationary point).
   - For $x > 0$: $f'(x) > 0$ (the function is **strictly increasing**).

3. **Qualitative Behavior Around Zero:**
   As $x$ approaches $0$ from negative values, $f(x)$ decreases smoothly until it reaches a global minimum at $(0, f(0)) = (0, 0)$. At $x = 0$, the tangent line is completely horizontal. For $x > 0$, the function increases symmetrically, forming an upward-opening cup symmetric about the $y$-axis ($f(-x) = f(x)$).

---

### Problem 10. The Tangent Line as an Application of the Derivative
For
$$f(x)=x^2-3x+1$$
find the equation of the tangent line at the point with $x=2$. Give the point of tangency, the value $f'(2)$, the equation of the line, and verify that the point lies on the obtained tangent line.

> **Why this problem:** it combines the derivative and the equation of a line into a complete geometric problem.

#### Solution

1. **Point of Tangency:**
   $$x_0 = 2 \implies y_0 = f(2) = 2^2 - 3(2) + 1 = 4 - 6 + 1 = -1.$$
   Point: $(x_0, y_0) = (2, -1)$.

2. **Compute Derivative and Slope:**
   $$f'(x) = 2x - 3.$$
   $$m = f'(2) = 2(2) - 3 = 4 - 3 = 1.$$

3. **Equation of the Tangent Line:**
   $$y - y_0 = f'(x_0)(x - x_0) \implies y - (-1) = 1(x - 2) \implies y + 1 = x - 2 \implies y = x - 3.$$
   (In general form: $x - y - 3 = 0$).

4. **Verification:**
   Substitute the tangency point $(2, -1)$ into the tangent equation:
   $$-1 = 2 - 3 = -1.$$
   The point of tangency lies on the tangent line.

---

## More Difficult Problems

### Problem 11. Derivative from the Definition
Using only
$$f'(x)=\lim_{h\to0}\frac{f(x+h)-f(x)}h,$$
find the derivative of $f(x)=x^2$. Compare the result with the power rule and indicate where the limit is used in the calculation.

> **Why this problem:** it shows the origin of the power rule and the direct connection between the derivative and a limit.

#### Solution

1. **Setup Difference Quotient:**
   $$f(x+h) = (x+h)^2 = x^2 + 2xh + h^2.$$
   $$\frac{f(x+h) - f(x)}{h} = \frac{(x^2 + 2xh + h^2) - x^2}{h} = \frac{2xh + h^2}{h}.$$

2. **Algebraic Simplification (for $h \neq 0$):**
   $$\frac{h(2x + h)}{h} = 2x + h.$$

3. **Apply the Limit:**
   $$f'(x) = \lim_{h\to0}(2x + h) = 2x + 0 = 2x.$$

4. **Comparison and Explanation:**
   - **Power rule comparison:** The power rule states $\frac{d}{dx}(x^2) = 2x^{2-1} = 2x$, exactly matching our first-principles result.
   - **Where the limit is used:** The limit is taken in the final step. Before the limit, the difference quotient $\frac{2xh+h^2}{h}$ represents the *average rate of change* (secant slope) over an interval of length $h$. Dividing by $h$ produces $2x + h$. The limit operation then sends $h \to 0$, causing the incremental term $h$ to vanish and yielding the exact *instantaneous rate of change* (tangent slope) $2x$.

---

### Problem 12. Several Rules at Once
For
$$f(x)=(x^2+1)^3e^x$$
compute the derivative. Before calculating, write down a plan: which rule applies to the whole expression and which rule applies to one of its factors. Finally, organize the result by factoring out common factors.

> **Why this problem:** it practices the order of decisions when combining familiar differentiation rules.

#### Solution

1. **Strategic Plan:**
   - **Global level:** The overall expression is the product of two functions: $u(x) = (x^2+1)^3$ and $v(x) = e^x$. The **Product Rule** $(uv)' = u'v + uv'$ governs the entire expression.
   - **Local level:** To find $u'(x)$, the factor $(x^2+1)^3$ is a composition (an inner quadratic inside an outer cubic). The **Chain Rule** must be applied to differentiate $u(x)$.

2. **Differentiate Components:**
   - $u'(x) = 3(x^2 + 1)^2 \cdot \frac{d}{dx}(x^2 + 1) = 3(x^2 + 1)^2 \cdot (2x) = 6x(x^2 + 1)^2$.
   - $v'(x) = e^x$.

3. **Assemble via Product Rule:**
   $$f'(x) = u'(x)v(x) + u(x)v'(x) = 6x(x^2 + 1)^2 e^x + (x^2 + 1)^3 e^x.$$

4. **Factor Out Common Terms:**
   The common factors are $(x^2 + 1)^2 e^x$:
   $$f'(x) = (x^2 + 1)^2 e^x \left[6x + (x^2 + 1)\right] = (x^2 + 1)^2 (x^2 + 6x + 1)e^x.$$

---

### Problem 13. A Multi-Layer Composition
For
$$f(x)=e^{\sin(x^2)}$$
compute the derivative. First write the layers
$$x\longrightarrow x^2\longrightarrow \sin(x^2)\longrightarrow e^{\sin(x^2)}$$
and explain why differentiation moves through them in the reverse order.

> **Why this problem:** it develops the chain rule as a method for working with multiple layers.

#### Solution

1. **Layers of Composition:**
   - Layer 1 (innermost): $u = x^2$
   - Layer 2 (intermediate): $v = \sin(u) = \sin(x^2)$
   - Layer 3 (outermost): $y = e^v = e^{\sin(x^2)}$

2. **Why Differentiation Moves in Reverse Order:**
   By Leibniz's chain rule:
   $$\frac{df}{dx} = \frac{dy}{dv} \cdot \frac{dv}{du} \cdot \frac{du}{dx}.$$
   The outermost function $e^v$ is the outer shell directly visible from the outside. Its derivative measures how the final value responds to the intermediate variable $v$. Then $v$ responds to $u$ by rate $\cos u$, and finally $u$ responds to the original variable $x$ by rate $2x$. We must "peel" the layers from the outside inward to track how small perturbations cascade down to the core argument.

3. **Compute the Derivative:**
   - $\frac{dy}{dv} = e^v = e^{\sin(x^2)}$.
   - $\frac{dv}{du} = \cos(u) = \cos(x^2)$.
   - $\frac{du}{dx} = 2x$.
   Multiplying the layers together:
   $$f'(x) = e^{\sin(x^2)} \cdot \cos(x^2) \cdot 2x = 2x\cos(x^2)e^{\sin(x^2)}.$$

---

### Problem 14. Continuity and Differentiability of a Piecewise Function
Investigate the behavior at $x=0$ of
$$f(x)=\begin{cases}x^2,&x\ge0,\\ax,&x<0.\end{cases}$$
For which values of $a$ is the function continuous? For which values do the one-sided derivatives exist and agree? For which value of $a$ is the function differentiable? Explain why continuity alone is not sufficient.

> **Why this problem:** it requires an organized argument and a clear distinction between two concepts.

#### Solution

1. **Continuity at $x = 0$:**
   - $\lim_{x\to0^+} f(x) = \lim_{x\to0^+}(x^2) = 0$.
   - $\lim_{x\to0^-} f(x) = \lim_{x\to0^-}(ax) = a(0) = 0$.
   - $f(0) = 0^2 = 0$.
   Since $\lim_{x\to0^+} f(x) = \lim_{x\to0^-} f(x) = f(0) = 0$, the function is **continuous at $x = 0$ for all $a \in \mathbb{R}$**.

2. **One-Sided Derivatives at $x = 0$:**
   - **Right-hand derivative:**
     $$f'_+(0) = \lim_{h\to0^+}\frac{f(h) - f(0)}{h} = \lim_{h\to0^+}\frac{h^2 - 0}{h} = \lim_{h\to0^+} h = 0.$$
   - **Left-hand derivative:**
     $$f'_-(0) = \lim_{h\to0^-}\frac{f(h) - f(0)}{h} = \lim_{h\to0^-}\frac{ah - 0}{h} = \lim_{h\to0^-} a = a.$$
   - **Agreement:**
     The one-sided derivatives exist for all $a$, and they agree if and only if:
     $$f'_+(0) = f'_-(0) \iff 0 = a \iff a = 0.$$

3. **Differentiability:**
   The function is differentiable at $x = 0$ if and only if **$a = 0$**, in which case $f'(0) = 0$.

4. **Why Continuity Alone Is Not Sufficient:**
   Continuity merely guarantees that the two pieces connect without a break (topological connectedness). Differentiability is a much stronger geometric requirement: it demands that the graph be *smooth*, having a unique, well-defined tangent line. For any $a \neq 0$, the curve arrives at the origin from the right horizontally (slope $0$) but arrives from the left with non-zero slope $a$, forming a sharp angular corner (kink) where no unique tangent slope exists.

---

### Problem 15. The Difference Quotient as a Check of the Derivative
Choose one function from the problem set and a point $x_0$ at which the derivative exists. Compute $f'(x_0)$ exactly, and then calculate
$$\frac{f(x_0+h)-f(x_0)}h$$
for $h=1$, $0.1$, and $0.01$. Compare the values with $f'(x_0)$ and explain why the difference quotient approaching a single number is consistent with the definition of the derivative, while a few computations do not replace a limit argument.

> **Why this problem:** it connects the definition of the derivative with concrete calculations and teaches the distinction between observation and proof.

#### Solution

1. **Chosen Function and Point:**
   Let $f(x) = x^2$ from Problem 11, evaluated at $x_0 = 1$.
   Exact derivative:
   $$f'(x) = 2x \implies f'(1) = 2(1) = 2.$$

2. **Difference Quotient Calculations:**
   $$Q(h) = \frac{f(1+h) - f(1)}{h} = \frac{(1+h)^2 - 1^2}{h} = \frac{1 + 2h + h^2 - 1}{h} = 2 + h.$$
   - For $h = 1$:
     $$Q(1) = \frac{(1+1)^2 - 1}{1} = \frac{4 - 1}{1} = 3.0.$$
   - For $h = 0.1$:
     $$Q(0.1) = \frac{(1.1)^2 - 1}{0.1} = \frac{1.21 - 1}{0.1} = \frac{0.21}{0.1} = 2.1.$$
   - For $h = 0.01$:
     $$Q(0.01) = \frac{(1.01)^2 - 1}{0.01} = \frac{1.0201 - 1}{0.01} = \frac{0.0201}{0.01} = 2.01.$$

3. **Comparison:**
   As $h$ shrinks from $1 \to 0.1 \to 0.01$, the difference quotients $3.0 \to 2.1 \to 2.01$ converge systematically toward the exact derivative value $2.0$.

4. **Consistency vs Proof:**
   - **Consistency:** The progressive approach of the secant slopes $Q(h)$ to the number $2$ illustrates the geometric definition of the tangent line as the limiting position of secant lines.
   - **Why discrete computations do not replace a limit:** Evaluating three discrete step sizes only checks three points; it cannot rule out wild oscillations, singularities, or discontinuous jumps for smaller intermediate values of $h$. Only a rigorous algebraic limit argument $(\lim_{h\to0}(2+h) = 2)$ accounts for every possible sequence of $h$ approaching zero continuously, establishing a definitive mathematical truth.
