# Integrals

## Goal of the Problem Set

The student should understand the indefinite integral as a family of antiderivatives, the definite integral as a tool for summation and area, and should be able to apply the basic techniques: direct integration, simple substitution, and integration by parts.

In the solutions, the result itself is not the only important part. The student should be able to explain **how they recognize the appropriate method**, verify an antiderivative by differentiation, and distinguish the meaning of an indefinite calculation from the interpretation of a definite integral.

## Basic Problems

### Problem 1. Antiderivative and Verification
For
$$f(x)=3x^2-4x+5$$
find one antiderivative $F(x)$. Write the entire family of antiderivatives, verify the result by differentiation, and explain the meaning of the constant $C$.

> **Why this problem:** it introduces integration as the inverse operation to differentiation.

#### Solution

1. **Find One Antiderivative $F(x)$:**
   Apply the power rule of integration $\int x^n\,dx = \frac{x^{n+1}}{n+1}$:
   $$F(x) = 3\left(\frac{x^3}{3}\right) - 4\left(\frac{x^2}{2}\right) + 5x = x^3 - 2x^2 + 5x.$$

2. **Entire Family of Antiderivatives:**
   $$\int (3x^2 - 4x + 5)\,dx = x^3 - 2x^2 + 5x + C, \qquad C \in \mathbb{R}.$$

3. **Verification by Differentiation:**
   $$\frac{d}{dx}\left(x^3 - 2x^2 + 5x + C\right) = 3x^2 - 4x + 5 + 0 = f(x).$$
   The derivative equals the original integrand.

4. **Meaning of the Constant $C$:**
   Because the derivative of any constant is zero ($\frac{d}{dx}C = 0$), adding a constant shifts the graph of the antiderivative vertically without changing its slope at any point $x$. On a connected interval, if two functions share the exact same derivative, their difference must be a constant. Thus, $C$ indexes all possible vertical offsets that satisfy the slope prescription $f(x)$.

---

### Problem 2. Powers, Roots, and the Domain
Compute
$$\int\left(2\sqrt{x}+\frac{3}{x^2}-x^{1/3}\right)\,dx.$$
First rewrite the terms as powers, determine the domain of the original expression, and verify the result by differentiation.

> **Why this problem:** it reinforces the power rule and reminds the student to keep track of the domain.

#### Solution

1. **Rewrite as Powers:**
   $$f(x) = 2x^{1/2} + 3x^{-2} - x^{1/3}.$$

2. **Domain of Integrand:**
   - $\sqrt{x} = x^{1/2}$ requires $x \ge 0$.
   - $\frac{3}{x^2} = 3x^{-2}$ requires $x \neq 0$.
   - $x^{1/3}$ is defined on all of $\mathbb{R}$.
   Intersecting these conditions gives:
   $$D_f = (0, \infty).$$

3. **Compute the Integral:**
   $$\int 2x^{1/2}\,dx = 2 \cdot \frac{x^{3/2}}{3/2} = \frac{4}{3}x^{3/2} = \frac{4}{3}x\sqrt{x}.$$
   $$\int 3x^{-2}\,dx = 3 \cdot \frac{x^{-1}}{-1} = -\frac{3}{x}.$$
   $$\int -x^{1/3}\,dx = -\frac{x^{4/3}}{4/3} = -\frac{3}{4}x^{4/3}.$$
   Result:
   $$\int\left(2\sqrt{x}+\frac{3}{x^2}-x^{1/3}\right)\,dx = \frac{4}{3}x^{3/2} - \frac{3}{x} - \frac{3}{4}x^{4/3} + C, \qquad x > 0.$$

4. **Verification by Differentiation:**
   $$\frac{d}{dx}\left(\frac{4}{3}x^{3/2} - 3x^{-1} - \frac{3}{4}x^{4/3} + C\right) = \frac{4}{3}\left(\frac{3}{2}x^{1/2}\right) - 3\left(-1x^{-2}\right) - \frac{3}{4}\left(\frac{4}{3}x^{1/3}\right) = 2x^{1/2} + 3x^{-2} - x^{1/3} = 2\sqrt{x} + \frac{3}{x^2} - x^{1/3}.$$

---

### Problem 3. Recognizing Basic Antiderivatives
Compute
$$\int\left(2e^x+3\cos x-4\sin x\right)\,dx.$$
Match each term with a known derivative and verify the entire result with one differentiation.

> **Why this problem:** it builds a catalogue of basic antiderivatives from known derivatives.

#### Solution

1. **Match Each Term with Known Derivatives:**
   - Since $\frac{d}{dx}(e^x) = e^x$, we have $\int 2e^x\,dx = 2e^x$.
   - Since $\frac{d}{dx}(\sin x) = \cos x$, we have $\int 3\cos x\,dx = 3\sin x$.
   - Since $\frac{d}{dx}(-\cos x) = \sin x$, we have $\int -4\sin x\,dx = 4\cos x$.

2. **Combine Results:**
   $$\int\left(2e^x+3\cos x-4\sin x\right)\,dx = 2e^x + 3\sin x + 4\cos x + C.$$

3. **Verification by Differentiation:**
   $$\frac{d}{dx}\left(2e^x + 3\sin x + 4\cos x + C\right) = 2e^x + 3\cos x + 4(-\sin x) + 0 = 2e^x + 3\cos x - 4\sin x.$$

---

### Problem 4. Substitution as Reversing the Chain Rule
Compute
$$\int 2x(x^2+1)^4\,dx.$$
Before calculating, identify a candidate for the new variable $u$ and show that its derivative appears in the integral. Finally, verify the result by differentiation.

> **Why this problem:** it teaches how to recognize substitution as reversing the chain rule.

#### Solution

1. **Identify Substitution Candidate:**
   - Candidate for new variable: $u = x^2 + 1$.
   - Differentiate: $du = 2x\,dx$.
   - Notice that the factor $2x\,dx$ appears directly in the integrand.

2. **Substitute and Integrate:**
   $$\int 2x(x^2+1)^4\,dx = \int (x^2+1)^4 \cdot (2x\,dx) = \int u^4\,du = \frac{u^5}{5} + C.$$
   Substitute back $u = x^2 + 1$:
   $$= \frac{(x^2 + 1)^5}{5} + C.$$

3. **Verification by Differentiation:**
   $$\frac{d}{dx}\left(\frac{(x^2+1)^5}{5} + C\right) = \frac{1}{5} \cdot 5(x^2+1)^4 \cdot \frac{d}{dx}(x^2+1) = (x^2+1)^4 \cdot (2x) = 2x(x^2+1)^4.$$

---

### Problem 5. The Same Substitution in a Different Context
Compute
$$\int xe^{x^2}\,dx.$$
First compare the structure with Problem 4 and explain what is common despite the different appearance of the function.

> **Why this problem:** it shows that the substitution mechanism is recognized by structure, not by the type of function.

#### Solution

1. **Structural Comparison with Problem 4:**
   In both problems, the integrand contains an inner expression $g(x) = x^2$ (or $x^2+1$) encapsulated inside an outer function (a power $(\cdot)^4$ in Problem 4, an exponential $e^{(\cdot)}$ here), multiplied by a factor $x$ proportional to the inner derivative $g'(x) = 2x$. Even though the outer functions are different, both integrals possess the universal substitution structure $\int f(g(x))g'(x)\,dx$.

2. **Compute via Substitution:**
   Let $u = x^2 \implies du = 2x\,dx \implies x\,dx = \frac{1}{2}du$.
   $$\int x e^{x^2}\,dx = \int e^{x^2}(x\,dx) = \int e^u \left(\frac{1}{2}du\right) = \frac{1}{2}\int e^u\,du = \frac{1}{2}e^u + C = \frac{1}{2}e^{x^2} + C.$$

3. **Verification:**
   $$\frac{d}{dx}\left(\frac{1}{2}e^{x^2} + C\right) = \frac{1}{2}e^{x^2}\cdot(2x) = x e^{x^2}.$$

---

### Problem 6. When Does a Logarithm Appear from an Integral?
Compute
$$\int\frac{2x}{x^2+5}\,dx.$$
Identify the denominator as a candidate for substitution, compare the numerator with its derivative, and explain the source of the logarithm in the result.

> **Why this problem:** it teaches how to recognize the structure “derivative of the denominator over the denominator.”

#### Solution

1. **Identify Substitution Candidate:**
   - Let denominator be $u = x^2 + 5$.
   - Derivative: $du = 2x\,dx$.
   - The numerator $2x\,dx$ is **exactly** the derivative of the denominator.

2. **Compute the Integral:**
   $$\int\frac{2x}{x^2+5}\,dx = \int\frac{1}{u}\,du = \ln|u| + C = \ln(x^2 + 5) + C.$$
   (The absolute value is omitted because $x^2 + 5 > 0$ for all real $x$).

3. **Source of the Logarithm:**
   By the chain rule, $\frac{d}{dx}\ln|g(x)| = \frac{g'(x)}{g(x)}$.
   Whenever an integrand has the structure $\frac{\text{derivative of denominator}}{\text{denominator}}$, integrating it inverts this logarithmic derivative rule, yielding $\ln|\text{denominator}| + C$.

---

### Problem 7. Integration by Parts as Reversing the Product Rule
Compute
$$\int xe^x\,dx.$$
First write the product differentiation rule and, on that basis, explain the meaning of the integration-by-parts formula. Verify the result by differentiation.

> **Why this problem:** it connects a new technique with the familiar product rule.

#### Solution

1. **Origin from Product Rule:**
   $$\frac{d}{dx}\left(u(x)v(x)\right) = u'(x)v(x) + u(x)v'(x).$$
   Integrating both sides with respect to $x$:
   $$u(x)v(x) = \int u'(x)v(x)\,dx + \int u(x)v'(x)\,dx.$$
   Rearranging terms gives the **integration by parts formula**:
   $$\int u(x)v'(x)\,dx = u(x)v(x) - \int u'(x)v(x)\,dx.$$
   Integration by parts transfers differentiation from one factor ($u$) to the other ($v'$), simplifying integrals where a power of $x$ can be diminished to a constant.

2. **Compute $\int x e^x\,dx$:**
   Choose:
   - $u = x \implies u' = 1$.
   - $v' = e^x \implies v = e^x$.
   $$\int x e^x\,dx = x e^x - \int (1)e^x\,dx = x e^x - e^x + C = (x - 1)e^x + C.$$

3. **Verification by Differentiation:**
   $$\frac{d}{dx}\left((x - 1)e^x + C\right) = (1)e^x + (x - 1)e^x = e^x + xe^x - e^x = xe^x.$$

---

### Problem 8. Choosing the Factors in Integration by Parts
Compute
$$\int x\cos x\,dx.$$
Before calculating, justify why it is convenient to differentiate $x$ and integrate $\cos x$, rather than the other way around.

> **Why this problem:** it teaches that integration by parts requires a deliberate choice of factors.

#### Solution

1. **Justification of Factor Choice:**
   - If we set $u = x$ and $v' = \cos x$:
     Differentiating $u$ gives $u' = 1$ (reducing polynomial degree from $1$ to $0$), while integrating $v'$ yields $v = \sin x$ (which stays at the same level of complexity). The new integral $\int u' v\,dx = \int \sin x\,dx$ is immediately solvable.
   - If we chose the opposite ($u = \cos x$ and $v' = x$):
     Differentiating gives $u' = -\sin x$ and integrating gives $v = \frac{x^2}{2}$. The new integral would be $-\frac{1}{2}\int x^2\sin x\,dx$, which has a higher power $x^2$ and is more difficult than the original integral!

2. **Calculation:**
   - $u = x \implies u' = 1$.
   - $v' = \cos x \implies v = \sin x$.
   $$\int x\cos x\,dx = x\sin x - \int (1)\sin x\,dx = x\sin x - (-\cos x) + C = x\sin x + \cos x + C.$$

3. **Verification:**
   $$\frac{d}{dx}(x\sin x + \cos x + C) = (1\cdot\sin x + x\cos x) - \sin x = x\cos x.$$

---

### Problem 9. Definite Integral and Geometric Area
Compute
$$\int_{-1}^{2}x\,dx.$$
Then separately compute the areas of the parts of the graph below and above the $x$-axis and explain the difference between the definite integral and geometric area.

> **Why this problem:** it clarifies the difference between signed accumulation and area.

#### Solution

1. **Compute Definite Integral:**
   $$\int_{-1}^{2}x\,dx = \left[\frac{x^2}{2}\right]_{-1}^{2} = \frac{2^2}{2} - \frac{(-1)^2}{2} = \frac{4}{2} - \frac{1}{2} = 2 - 0.5 = 1.5.$$

2. **Geometric Area of Both Parts:**
   - **Region below $x$-axis ($x \in [-1, 0]$):**
     Right triangle with base $1$ (from $-1$ to $0$) and height $1$ (from $y=0$ to $y=-1$):
     $$\text{Area}_1 = \frac{1}{2}\text{base}\times\text{height} = \frac{1}{2}(1)(1) = 0.5.$$
   - **Region above $x$-axis ($x \in [0, 2]$):**
     Right triangle with base $2$ (from $0$ to $2$) and height $2$ (from $y=0$ to $y=2$):
     $$\text{Area}_2 = \frac{1}{2}\text{base}\times\text{height} = \frac{1}{2}(2)(2) = 2.0.$$
   - **Total Geometric Area:**
     $$\text{Area}_{\text{total}} = \text{Area}_1 + \text{Area}_2 = 0.5 + 2.0 = 2.5.$$

3. **Difference Between Definite Integral and Geometric Area:**
   The definite integral computes **signed net accumulation**: regions above the $x$-axis are counted with positive signs ($+2.0$), while regions below the $x$-axis are counted with negative signs ($-0.5$). Thus:
   $$\int_{-1}^2 x\,dx = \text{Area}_2 - \text{Area}_1 = 2.0 - 0.5 = 1.5.$$
   Geometric area is the total physical area of the surface, defined as the integral of the absolute value $\int_{-1}^2 |x|\,dx = 2.5$.

---

### Problem 10. Definite Integral and Checking the Result
Before carrying out the exact calculation, estimate the possible range of values of the integral
$$\int_0^2(x^2+1)\,dx,$$
using
$$1\le x^2+1\le5$$
on $[0,2]$. Only then compute the integral exactly, compare the result with the earlier estimate, and explain what type of computational error such a check can detect.

> **Why this problem:** it teaches how to predict the possible range of a result and check the calculation.

#### Solution

1. **A Priori Estimate:**
   On the interval $[0, 2]$, $f(x) = x^2 + 1$ is strictly increasing:
   - Minimum value: $m = f(0) = 0^2 + 1 = 1$.
   - Maximum value: $M = f(2) = 2^2 + 1 = 5$.
   By the bounding property of definite integrals:
   $$m(b - a) \le \int_a^b f(x)\,dx \le M(b - a).$$
   $$1(2 - 0) \le \int_0^2 (x^2 + 1)\,dx \le 5(2 - 0) \implies 2 \le \int_0^2 (x^2 + 1)\,dx \le 10.$$

2. **Exact Calculation:**
   $$\int_0^2 (x^2 + 1)\,dx = \left[\frac{x^3}{3} + x\right]_0^2 = \left(\frac{2^3}{3} + 2\right) - (0 + 0) = \frac{8}{3} + 2 = \frac{14}{3} = 4\frac{2}{3} \approx 4.667.$$

3. **Comparison and Error Detection:**
   - The exact value $4.667$ lies within the estimated range $[2, 10]$.
   - **Errors detected by bounding checks:** Such checks instantly catch catastrophic mistakes like incorrect antiderivative powers (e.g. integrating $x^2 \to x^3$ without dividing by 3, yielding $10$), sign errors in the Fundamental Theorem of Calculus ($F(a) - F(b)$ instead of $F(b) - F(a)$, yielding negative numbers for a positive function), or arithmetic slips that produce values outside the geometrically allowable bounds.

---

## More Difficult Problems

### Problem 11. Choose the Method First
For each integral, first write which method you choose and how you recognize it, and then compute:
1. $\int\sin(3x)\,dx$,
2. $\int x\ln x\,dx$,
3. $\int\frac{x}{\sqrt{x^2+1}}\,dx$.

> **Why this problem:** it tests the choice of method based on the structure of the problem.

#### Solution

1. **Integral 1: $\int\sin(3x)\,dx$:**
   - **Chosen Method:** Linear Substitution.
   - **Recognition:** The argument of the sine is a linear function $ax = 3x$.
   - **Computation:**
     Let $u = 3x \implies du = 3\,dx \implies dx = \frac{1}{3}du$.
     $$\int\sin(3x)\,dx = \frac{1}{3}\int\sin u\,du = -\frac{1}{3}\cos u + C = -\frac{1}{3}\cos(3x) + C.$$

2. **Integral 2: $\int x\ln x\,dx$:**
   - **Chosen Method:** Integration by Parts.
   - **Recognition:** Product of a polynomial ($x$) and a logarithm ($\ln x$). Logarithm cannot be easily integrated directly, but differentiating it yields an algebraic term $\frac{1}{x}$ that cancels powers of $x$.
   - **Computation:**
     Let $u = \ln x \implies u' = \frac{1}{x}$.
     Let $v' = x \implies v = \frac{x^2}{2}$.
     $$\int x\ln x\,dx = \frac{x^2}{2}\ln x - \int \frac{x^2}{2}\cdot\frac{1}{x}\,dx = \frac{x^2}{2}\ln x - \frac{1}{2}\int x\,dx = \frac{x^2}{2}\ln x - \frac{x^2}{4} + C = \frac{x^2}{4}(2\ln x - 1) + C.$$

3. **Integral 3: $\int\frac{x}{\sqrt{x^2+1}}\,dx$:**
   - **Chosen Method:** Substitution.
   - **Recognition:** The expression under the radical is quadratic ($x^2+1$), and the outside multiplying factor is linear ($x\,dx$), which is proportional to the derivative of the inner expression.
   - **Computation:**
     Let $u = x^2 + 1 \implies du = 2x\,dx \implies x\,dx = \frac{1}{2}du$.
     $$\int\frac{x}{\sqrt{x^2+1}}\,dx = \int\frac{\frac{1}{2}du}{\sqrt{u}} = \frac{1}{2}\int u^{-1/2}\,du = \frac{1}{2}\left(\frac{u^{1/2}}{1/2}\right) + C = \sqrt{u} + C = \sqrt{x^2 + 1} + C.$$

---

### Problem 12. Symmetry, Sign, and Absolute Value
Compare
$$\int_{-2}^{2}x\,dx$$
and
$$\int_{-2}^{2}|x|\,dx.$$
Before calculating, predict the results from symmetry and a sketch, then carry out the calculation and explain the difference.

> **Why this problem:** it teaches how to use symmetry and geometry before applying a computational procedure.

#### Solution

1. **Prediction from Symmetry:**
   - $f(x) = x$ is an **odd function** ($f(-x) = -f(x)$). Its graph is symmetric with respect to the origin $(0, 0)$. Over the symmetric interval $[-2, 2]$, the negative signed area on $[-2, 0]$ cancels the positive signed area on $[0, 2]$. **Prediction: $0$**.
   - $g(x) = |x|$ is an **even function** ($g(-x) = g(x)$). Its graph is symmetric with respect to the $y$-axis, and $g(x) \ge 0$ everywhere. The area on $[-2, 0]$ equals the area on $[0, 2]$. Each side is a triangle of base $2$ and height $2$ (area $2$). **Prediction: $2 + 2 = 4$**.

2. **Calculations:**
   $$\int_{-2}^{2}x\,dx = \left[\frac{x^2}{2}\right]_{-2}^{2} = \frac{2^2}{2} - \frac{(-2)^2}{2} = 2 - 2 = 0.$$
   For $|x|$, split at $x = 0$:
   $$\int_{-2}^{2}|x|\,dx = \int_{-2}^0 (-x)\,dx + \int_0^2 x\,dx = \left[-\frac{x^2}{2}\right]_{-2}^0 + \left[\frac{x^2}{2}\right]_0^2 = \left(0 - \left(-\frac{4}{2}\right)\right) + \left(\frac{4}{2} - 0\right) = 2 + 2 = 4.$$

3. **Explanation of the Difference:**
   The absolute value operator acts as a geometric reflector: it flips the negative left triangle from below the $x$-axis to above the $x$-axis. This turns destructive cancellation (where $-2$ canceled $+2$ to yield $0$) into constructive accumulation (where $+2$ adds to $+2$ to yield $4$).

---

### Problem 13. An Integral Depending on the Upper Limit
Let
$$F(x)=\int_0^x(t^2+1)\,dt.$$
Determine $F(x)$, compute $F'(x)$, and compare the result with the integrand. Explain in your own words why the height of the function describes the local rate of increase of the accumulated area.

> **Why this problem:** it connects differentiation and integration through the idea of accumulation.

#### Solution

1. **Determine $F(x)$:**
   $$F(x) = \left[\frac{t^3}{3} + t\right]_0^x = \left(\frac{x^3}{3} + x\right) - 0 = \frac{x^3}{3} + x.$$

2. **Compute $F'(x)$:**
   $$F'(x) = \frac{d}{dx}\left(\frac{x^3}{3} + x\right) = 3\left(\frac{x^2}{3}\right) + 1 = x^2 + 1.$$

3. **Comparison with Integrand:**
   Notice that $F'(x) = x^2 + 1$ is **identically equal to the original integrand $f(t) = t^2 + 1$ evaluated at $t = x$**. This is the concrete realization of the **Fundamental Theorem of Calculus**:
   $$\frac{d}{dx}\int_a^x f(t)\,dt = f(x).$$

4. **Explanation of Why Height Describes the Rate of Area Increase:**
   $F(x)$ represents the total area accumulated under the curve from $0$ to $x$. When the upper bound $x$ is nudged forward by a small increment $\Delta x$, the new area added is a thin vertical strip of width $\Delta x$ and height approximately $f(x)$. The change in area is:
   $$\Delta F \approx f(x) \Delta x \implies \frac{\Delta F}{\Delta x} \approx f(x).$$
   Taking the limit as $\Delta x \to 0$, the instantaneous rate of area growth with respect to the boundary position is precisely the height of the curve $f(x)$ at that boundary.

---

### Problem 14. A Piecewise-Defined Function
Let
$$f(x)=\begin{cases}x+1,&-1\le x<1,\\2,&1\le x\le3.\end{cases}$$
Sketch the graph, decide where to split the integral, compute
$$\int_{-1}^{3}f(x)\,dx$$
and verify the result geometrically.

> **Why this problem:** it requires understanding the definition of the function before carrying out the calculation.

#### Solution

1. **Splitting the Integral:**
   Because the analytical formula changes definition at $x = 1$, the integral must be split at $x = 1$:
   $$\int_{-1}^3 f(x)\,dx = \int_{-1}^1 (x + 1)\,dx + \int_1^3 2\,dx.$$

2. **Calculations:**
   - First piece:
     $$\int_{-1}^1 (x + 1)\,dx = \left[\frac{x^2}{2} + x\right]_{-1}^1 = \left(\frac{1}{2} + 1\right) - \left(\frac{(-1)^2}{2} - 1\right) = \frac{3}{2} - \left(-\frac{1}{2}\right) = \frac{3}{2} + \frac{1}{2} = 2.$$
   - Second piece:
     $$\int_1^3 2\,dx = [2x]_1^3 = 2(3) - 2(1) = 6 - 2 = 4.$$
   - Total integral:
     $$\int_{-1}^3 f(x)\,dx = 2 + 4 = 6.$$

3. **Geometric Verification:**
   - For $x \in [-1, 1]$, the function is a straight line rising from $(-1, 0)$ to $(1, 2)$. The region under the curve is a right triangle with base $b = 1 - (-1) = 2$ and height $h = 2$.
     $$\text{Area}_{\text{triangle}} = \frac{1}{2} b h = \frac{1}{2}(2)(2) = 2.$$
   - For $x \in [1, 3]$, the function is horizontal at height $y = 2$. The region is a rectangle with base $b = 3 - 1 = 2$ and height $h = 2$.
     $$\text{Area}_{\text{rectangle}} = b \times h = 2 \times 2 = 4.$$
   - Total geometric area:
     $$\text{Area}_{\text{total}} = 2 + 4 = 6.$$
   The geometric area matches the analytical integral result.

---

### Problem 15. Recovering a Function from Its Derivative and a Condition
The function $F$ satisfies
$$F'(x)=2xe^{x^2}$$
and
$$F(0)=3.$$

1. Recognize the method needed to find the function $F$.
2. Determine the entire family of functions with the given derivative.
3. Use the condition $F(0)=3$ to determine the correct constant.
4. Verify the final result by differentiation and substitution of $x=0$.

> **Why this problem:** it combines recognition of substitution, the meaning of the constant of integration, and an initial condition in one problem, using only mechanisms introduced earlier.

#### Solution

1. **Recognize the Method:**
   To find $F(x)$, we must compute the indefinite integral $\int 2x e^{x^2}\,dx$. Because the integrand consists of an exponential function with argument $x^2$ multiplied by $2x$ (which is the exact derivative of $x^2$), the appropriate method is **Substitution** with $u = x^2$.

2. **Entire Family of Antiderivatives:**
   Let $u = x^2 \implies du = 2x\,dx$.
   $$F(x) = \int 2x e^{x^2}\,dx = \int e^u\,du = e^u + C = e^{x^2} + C, \qquad C \in \mathbb{R}.$$

3. **Determine the Constant using $F(0) = 3$:**
   Substitute $x = 0$:
   $$F(0) = e^{0^2} + C = e^0 + C = 1 + C.$$
   Setting $F(0) = 3$:
   $$1 + C = 3 \implies C = 2.$$
   The specific function is:
   $$F(x) = e^{x^2} + 2.$$

4. **Verification:**
   - **Check derivative:**
     $$F'(x) = \frac{d}{dx}\left(e^{x^2} + 2\right) = e^{x^2}\cdot\frac{d}{dx}(x^2) + 0 = 2x e^{x^2} \quad (\text{matches } F'(x)).$$
   - **Check initial condition:**
     $$F(0) = e^{0^2} + 2 = 1 + 2 = 3 \quad (\text{matches } F(0) = 3).$$
   The solution is verified.
