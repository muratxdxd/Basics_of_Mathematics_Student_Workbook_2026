# Limits of Sequences and Functions

## Goal of the Set

After completing this set, the student should understand the common idea of a limit: studying the behavior of an object as its argument approaches a specified value or grows without bound. We first practice limits of sequences and then move to limits of functions, one-sided limits, and continuity.

The set deliberately combines two topics that were previously separate. Computational techniques should be transferred between sequences and functions rather than learned as two independent catalogs of examples.

## Basic Exercises

### Exercise 1. Dominant Terms in a Sequence
Compute
$$\lim_{n\to\infty}\frac{4n^2-3n+1}{2n^2+5n-7}.$$
Explain why the highest-degree terms determine the result.

> **Why this exercise:** introduces the idea of a dominant term and teaches how to simplify the behavior of expressions for large arguments.

#### Solution

1. **Computation:**
   Divide both numerator and denominator by the highest power of $n$, which is $n^2$:
   $$\lim_{n\to\infty}\frac{4n^2-3n+1}{2n^2+5n-7} = \lim_{n\to\infty}\frac{4 - \frac{3}{n} + \frac{1}{n^2}}{2 + \frac{5}{n} - \frac{7}{n^2}}.$$
   Since $\lim_{n\to\infty}\frac{1}{n} = 0$ and $\lim_{n\to\infty}\frac{1}{n^2} = 0$:
   $$= \frac{4 - 0 + 0}{2 + 0 - 0} = \frac{4}{2} = 2.$$

2. **Why Highest-Degree Terms Determine the Result:**
   As $n \to \infty$, $n^2$ grows orders of magnitude faster than linear or constant terms ($n^2 \gg n \gg 1$). Factoring out $n^2$ from the numerator and denominator reveals that all sub-dominant terms vanish to $0$ in the limit. The asymptotic behavior of the entire rational expression is governed entirely by the ratio of leading coefficients: $\frac{4n^2}{2n^2} = 2$.

---

### Exercise 2. Different Growth Rates
Compute
$$\lim_{n\to\infty}\frac{3n+1}{n^2+4},\qquad \lim_{n\to\infty}\frac{2n^3-n}{5n^2+1}.$$
Compare the two cases and formulate a general observation about the degrees of the polynomials in the numerator and denominator.

> **Why this exercise:** teaches how to compare growth rates and recognize qualitatively different cases.

#### Solution

1. **Computation of First Limit:**
   Divide numerator and denominator by $n^2$:
   $$\lim_{n\to\infty}\frac{3n+1}{n^2+4} = \lim_{n\to\infty}\frac{\frac{3}{n} + \frac{1}{n^2}}{1 + \frac{4}{n^2}} = \frac{0 + 0}{1 + 0} = \frac{0}{1} = 0.$$

2. **Computation of Second Limit:**
   Divide numerator and denominator by $n^2$:
   $$\lim_{n\to\infty}\frac{2n^3-n}{5n^2+1} = \lim_{n\to\infty}\frac{2n - \frac{1}{n}}{5 + \frac{1}{n^2}} = \frac{\infty - 0}{5 + 0} = +\infty.$$

3. **General Observation for Rational Sequences $\frac{P(n)}{Q(n)}$:**
   Let $p = \deg(P)$ and $q = \deg(Q)$:
   - If $p < q$ (denominator grows faster), the limit is always **$0$**.
   - If $p = q$ (numerator and denominator grow at the same rate), the limit is the finite non-zero ratio of leading coefficients $\frac{a_p}{b_q}$.
   - If $p > q$ (numerator grows faster), the sequence diverges to **$\pm\infty$** (or does not exist if sign oscillates).

---

### Exercise 3. A Square Root and Removing an Indeterminate Form
Compute
$$\lim_{n\to\infty}\left(\sqrt{n^2+5n}-n\right).$$
Use the conjugate expression and explain why this transformation removes the difficulty.

> **Why this exercise:** introduces conjugation as a deliberate technique for removing an indeterminate form.

#### Solution

1. **Identify Indeterminate Form:**
   As $n \to \infty$, $\sqrt{n^2+5n} \to \infty$ and $n \to \infty$, giving the indeterminate form $\infty - \infty$.

2. **Multiply and Divide by the Conjugate:**
   Multiply by $\frac{\sqrt{n^2+5n} + n}{\sqrt{n^2+5n} + n}$:
   $$\lim_{n\to\infty}\left(\sqrt{n^2+5n}-n\right) = \lim_{n\to\infty}\frac{(\sqrt{n^2+5n}-n)(\sqrt{n^2+5n}+n)}{\sqrt{n^2+5n}+n} = \lim_{n\to\infty}\frac{(n^2+5n) - n^2}{\sqrt{n^2+5n}+n} = \lim_{n\to\infty}\frac{5n}{\sqrt{n^2(1 + \frac{5}{n})} + n}.$$
   Divide numerator and denominator by $n$:
   $$= \lim_{n\to\infty}\frac{5}{\sqrt{1 + \frac{5}{n}} + 1} = \frac{5}{\sqrt{1 + 0} + 1} = \frac{5}{1 + 1} = \frac{5}{2} = 2.5.$$

3. **Why Conjugation Removes the Difficulty:**
   Conjugate multiplication utilizes the difference of squares identity $(A-B)(A+B) = A^2 - B^2$. This eliminates the square root and cancels out the leading quadratic terms ($n^2 - n^2 = 0$), converting an indeterminate subtraction of two nearly equal large quantities ($\infty - \infty$) into a determinate ratio where dominant linear powers can be evaluated cleanly.

---

### Exercise 4. Powers and Oscillation
Analyze
$$\left(\frac23\right)^n,\qquad \left(\frac32\right)^n,\qquad (-1)^n,\qquad \frac{(-1)^n}{n}.$$
For each sequence, describe the type of behavior and justify your answer.

> **Why this exercise:** organizes the basic types of sequence behavior and shows that oscillation does not always rule out convergence.

#### Solution

1. **$\left(\frac{2}{3}\right)^n$:**
   - **Behavior:** Converges monotonically to **$0$**.
   - **Justification:** This is a geometric sequence $r^n$ with base $|r| = \frac{2}{3} < 1$. Successive powers shrink toward 0: $\lim_{n\to\infty}\left(\frac{2}{3}\right)^n = 0$.

2. **$\left(\frac{3}{2}\right)^n$:**
   - **Behavior:** Diverges monotonically to **$+\infty$**.
   - **Justification:** Geometric sequence with base $r = 1.5 > 1$. Each term is $1.5$ times the previous one, growing without bound.

3. **$(-1)^n$:**
   - **Behavior:** Diverges by bounded oscillation.
   - **Justification:** Terms alternate strictly between $-1$ (for odd $n$) and $+1$ (for even $n$): $\{-1, 1, -1, 1, \dots\}$. The sequence has two distinct subsequential limits ($+1$ and $-1$), so no single limit exists.

4. **$\frac{(-1)^n}{n}$:**
   - **Behavior:** Converges to **$0$** with damped oscillation.
   - **Justification:** Bounded above and below: $-\frac{1}{n} \le \frac{(-1)^n}{n} \le \frac{1}{n}$. Since $\lim_{n\to\infty}\left(-\frac{1}{n}\right) = 0$ and $\lim_{n\to\infty}\frac{1}{n} = 0$, by the **Squeeze Theorem**, $\lim_{n\to\infty}\frac{(-1)^n}{n} = 0$. Oscillation does not prevent convergence if the oscillation amplitude shrinks to zero.

---

### Exercise 5. The Classical Limit Leading to the Number $e$
Compute
$$\lim_{n\to\infty}\left(1+\frac1n\right)^n.$$
Calculate several values for increasing $n$ and compare the observed behavior with the value of the limit. Explain why a few values do not constitute a proof.

> **Why this exercise:** connects a central limit with intuition based on concrete terms of a sequence.

#### Solution

1. **Analytical Limit:**
   By definition, $\lim_{n\to\infty}\left(1+\frac{1}{n}\right)^n = e \approx 2.718281828\dots$

2. **Table of Values for Increasing $n$:**
   - $n = 1$: $(1 + 1)^1 = 2$
   - $n = 2$: $(1 + 0.5)^2 = 2.25$
   - $n = 5$: $(1 + 0.2)^5 = 1.2^5 \approx 2.48832$
   - $n = 10$: $(1 + 0.1)^{10} \approx 2.59374$
   - $n = 100$: $(1 + 0.01)^{100} \approx 2.70481$
   - $n = 1\,000$: $(1 + 0.001)^{1\,000} \approx 2.71692$
   - $n = 10\,000$: $(1 + 0.0001)^{10\,000} \approx 2.71815$
   The computed values are strictly increasing and visibly approach Euler's number $e \approx 2.71828$.

3. **Why Numerical Values Do Not Constitute a Proof:**
   A finite set of numerical calculations only tests isolated inputs. It cannot prove that the sequence does not plateau prematurely, oscillate wildly at enormous $n$, or slowly drift off to infinity. A rigorous proof requires proving two analytical properties:
   1. The sequence $a_n = \left(1 + \frac{1}{n}\right)^n$ is strictly increasing.
   2. The sequence is bounded from above (e.g., $a_n < 3$).
   By the Monotone Convergence Theorem, any sequence that is monotonically increasing and bounded from above is guaranteed to converge to a finite limit.

---

### Exercise 6. From a Sequence to a Function — Limit at Infinity
Compute
$$\lim_{x\to\infty}\frac{3x^2-x+1}{5x^2+4x-2}.$$
Compare the method with Exercise 1. Explain what changes when moving from $n$ to a real variable $x$, and what stays the same.

> **Why this exercise:** deliberately transfers a technique from sequence limits to function limits.

#### Solution

1. **Computation:**
   Divide numerator and denominator by $x^2$:
   $$\lim_{x\to\infty}\frac{3x^2-x+1}{5x^2+4x-2} = \lim_{x\to\infty}\frac{3 - \frac{1}{x} + \frac{1}{x^2}}{5 + \frac{4}{x} - \frac{2}{x^2}} = \frac{3 - 0 + 0}{5 + 0 - 0} = \frac{3}{5} = 0.6.$$

2. **Comparison with Exercise 1:**
   - **What stays the same:** The algebraic method is identical: identifying the highest power of the variable ($x^2$), dividing through, and using the fact that reciprocal powers approach $0$ as the argument grows without bound.
   - **What changes:** The variable $n$ is discrete ($n \in \{1, 2, 3, \dots\}$), whereas $x$ is a continuous real variable ($x \in \mathbb{R}$). For a function limit $\lim_{x\to\infty} f(x) = L$ to hold, $f(x)$ must approach $L$ along *all* continuous paths to infinity, not just at integer checkpoints. By the Heine definition of a limit, if $\lim_{x\to\infty} f(x) = L$, then for every sequence $x_n \to \infty$, $f(x_n) \to L$.

---

### Exercise 7. Limit at a Point and Canceling a Factor
Compute
$$\lim_{x\to3}\frac{x^2-4x+3}{x-3}.$$
Explain why the value of the function at $x=3$ is not needed to compute the limit.

> **Why this exercise:** separates the concept of a limit from the value of a function at a point.

#### Solution

1. **Factor and Simplify:**
   Factor the quadratic numerator:
   $$x^2 - 4x + 3 = (x - 3)(x - 1).$$
   For $x \neq 3$, the factor $(x - 3)$ is non-zero, allowing valid cancellation:
   $$\frac{x^2 - 4x + 3}{x - 3} = \frac{(x - 3)(x - 1)}{x - 3} = x - 1.$$

2. **Compute the Limit:**
   $$\lim_{x\to3}\frac{x^2-4x+3}{x-3} = \lim_{x\to3}(x - 1) = 3 - 1 = 2.$$

3. **Why the Value at $x=3$ is Not Needed:**
   The definition of the limit $\lim_{x\to c} f(x)$ examines the values of $f(x)$ as $x$ gets arbitrarily close to $c$ in a punctured neighborhood $0 < |x - c| < \delta$. The value $f(c)$ at the point itself is completely irrelevant to the limit. At $x = 3$, $f(3) = \frac{0}{0}$ is undefined; nevertheless, the function approaches $2$ continuously from both sides.

---

### Exercise 8. A Square Root in a Function Limit
Compute
$$\lim_{x\to4}\frac{\sqrt{x}-2}{x-4}$$
by rationalizing the numerator. Compare the idea with Exercise 3 involving a sequence.

> **Why this exercise:** reinforces transferring the same algebraic technique between two types of limits.

#### Solution

1. **Rationalize Numerator:**
   Multiply numerator and denominator by the conjugate $(\sqrt{x} + 2)$:
   $$\lim_{x\to4}\frac{\sqrt{x}-2}{x-4} = \lim_{x\to4}\frac{(\sqrt{x}-2)(\sqrt{x}+2)}{(x-4)(\sqrt{x}+2)} = \lim_{x\to4}\frac{x - 4}{(x-4)(\sqrt{x}+2)}.$$
   For $x \neq 4$, cancel the common factor $(x - 4)$:
   $$= \lim_{x\to4}\frac{1}{\sqrt{x} + 2} = \frac{1}{\sqrt{4} + 2} = \frac{1}{2 + 2} = \frac{1}{4} = 0.25.$$

2. **Comparison with Exercise 3:**
   Both problems resolve an indeterminate form using the difference of squares identity $(A-B)(A+B) = A^2 - B^2$. In Exercise 3, conjugation resolved an $(\infty - \infty)$ indeterminate form by canceling dominant leading powers at infinity; here, it resolves a $(0/0)$ indeterminate form by explicitly creating and canceling the factor $(x - 4)$ responsible for the zero in the denominator.

---

### Exercise 9. One-Sided Limits and an Asymptote
Analyze the left-hand and right-hand limits of
$$f(x)=\frac1{x-2}$$
as $x\to2$. Does the two-sided limit exist? Interpret the result on a sketch of the graph and identify the vertical asymptote.

> **Why this exercise:** teaches how to distinguish one-sided limits and connect them with the geometry of an asymptote.

#### Solution

1. **One-Sided Limits:**
   - **Left-hand limit ($x \to 2^-$):**
     As $x$ approaches $2$ from below ($x < 2$), $(x - 2)$ is negative and approaches $0$:
     $$\lim_{x\to2^-}\frac{1}{x-2} = \frac{1}{0^-} = -\infty.$$
   - **Right-hand limit ($x \to 2^+$):**
     As $x$ approaches $2$ from above ($x > 2$), $(x - 2)$ is positive and approaches $0$:
     $$\lim_{x\to2^+}\frac{1}{x-2} = \frac{1}{0^+} = +\infty.$$

2. **Existence of Two-Sided Limit:**
   A two-sided limit exists if and only if both one-sided limits exist and are equal. Since $\lim_{x\to2^-} f(x) = -\infty \neq +\infty = \lim_{x\to2^+} f(x)$, the two-sided limit **does not exist**.

3. **Geometric Interpretation and Asymptote:**
   The line $x = 2$ is a **vertical asymptote**.
   On a graph, as the curve approaches $x = 2$ from the left, it plunges steeply downwards toward $-\infty$. As it approaches from the right, it shoots steeply upwards toward $+\infty$, forming the characteristic opposing branches of a hyperbola.

---

### Exercise 10. Continuity of a Piecewise Function
Find $a$ so that
$$f(x)=\begin{cases}ax+1,&x<2,\\x^2-1,&x\ge2\end{cases}$$
is continuous at $x=2$. Explicitly compare the left-hand limit, right-hand limit, and function value.

> **Why this exercise:** organizes the definition of continuity as agreement among three quantities.

#### Solution

1. **Definition of Continuity:**
   A function $f$ is continuous at $x = c$ if and only if:
   $$\lim_{x\to c^-} f(x) = \lim_{x\to c^+} f(x) = f(c).$$

2. **Evaluate the Three Quantities at $x = 2$:**
   - **Left-hand limit:**
     $$\lim_{x\to2^-} f(x) = \lim_{x\to2^-}(ax + 1) = a(2) + 1 = 2a + 1.$$
   - **Right-hand limit:**
     $$\lim_{x\to2^+} f(x) = \lim_{x\to2^+}(x^2 - 1) = 2^2 - 1 = 4 - 1 = 3.$$
   - **Function value:**
     $$f(2) = 2^2 - 1 = 3.$$

3. **Solve for $a$:**
   Equating the left-hand limit to the right-hand limit and function value:
   $$2a + 1 = 3 \implies 2a = 2 \implies a = 1.$$
   For $a = 1$, the two pieces meet seamlessly at the point $(2, 3)$, making $f(x)$ continuous on all of $\mathbb{R}$.

---

## More Challenging Exercises

### Exercise 11. An n-th Root
Compute
$$\lim_{n\to\infty}\sqrt[n]{5^n+2^n}.$$
Explain which term dominates and why the transformation looks different from the case of a quotient of polynomials.

> **Why this exercise:** extends the idea of dominance to exponential expressions.

#### Solution

1. **Identify Dominant Term:**
   Between $5^n$ and $2^n$, the base $5 > 2$, so $5^n$ grows much faster than $2^n$. The ratio $\left(\frac{2}{5}\right)^n \to 0$ as $n \to \infty$. Thus, $5^n$ is the dominant term.

2. **Factor out $5^n$:**
   $$\sqrt[n]{5^n + 2^n} = \sqrt[n]{5^n\left(1 + \left(\frac{2}{5}\right)^n\right)} = 5 \left(1 + \left(\frac{2}{5}\right)^n\right)^{1/n}.$$
   Since $\left(\frac{2}{5}\right)^n \to 0$, $1 + \left(\frac{2}{5}\right)^n \to 1$.
   Therefore, $\lim_{n\to\infty} 5 \cdot 1^{0} = 5 \cdot 1 = 5$.

3. **Formal Proof via Squeeze Theorem:**
   $$5^n < 5^n + 2^n < 5^n + 5^n = 2 \cdot 5^n.$$
   Taking the $n$-th root:
   $$5 < \sqrt[n]{5^n + 2^n} < 5 \cdot \sqrt[n]{2}.$$
   Since $\lim_{n\to\infty} \sqrt[n]{2} = 1$, the lower and upper bounds both converge to $5$:
   $$\lim_{n\to\infty}\sqrt[n]{5^n+2^n} = 5.$$

4. **Why the Transformation Looks Different:**
   In polynomial quotients, dominance is governed by power degrees ($n^k$), and we factor out $n^k$ to create terms like $\frac{1}{n^p} \to 0$. In exponential expressions, dominance is determined by the geometric base ($b^n$), and taking an $n$-th root $(\cdot)^{1/n}$ naturally extracts the largest base $b$ outside the radical while crushing the bounded remaining factor to $1$ because $\lim_{n\to\infty} C^{1/n} = 1$.

---

### Exercise 12. Exponential Function Limit
Compute
$$\lim_{x\to0}(1+3x)^{1/x}.$$
Connect the result with the limit from Exercise 5 and show the appropriate transformation.

> **Why this exercise:** teaches how to recognize the classical pattern after a transformation.

#### Solution

1. **Recall Fundamental Exponential Limit:**
   From Exercise 5, $\lim_{u\to0}(1 + u)^{1/u} = e$ (or equivalently $\lim_{n\to\infty}(1 + \frac{1}{n})^n = e$).

2. **Algebraic Transformation:**
   Set $u = 3x$. As $x \to 0$, $u \to 0$.
   Notice the exponent can be rewritten as:
   $$\frac{1}{x} = \frac{3}{3x} = 3 \cdot \frac{1}{u}.$$
   Rewrite the expression:
   $$(1 + 3x)^{1/x} = (1 + u)^{3/u} = \left[(1 + u)^{1/u}\right]^3.$$

3. **Evaluate the Limit:**
   By continuity of the power function $g(t) = t^3$:
   $$\lim_{x\to0}(1+3x)^{1/x} = \left[\lim_{u\to0}(1+u)^{1/u}\right]^3 = e^3 \approx 20.0855.$$

---

### Exercise 13. Fundamental Trigonometric Limit
Using
$$\lim_{x\to0}\frac{\sin x}{x}=1,$$
compute
$$\lim_{x\to0}\frac{\sin5x}{x},\qquad \lim_{x\to0}\frac{\sin2x}{\sin3x}.$$
In each case, show how you reduce the expression to the fundamental limit.

> **Why this exercise:** teaches how to reduce new limits to one known pattern.

#### Solution

1. **First Limit:**
   Multiply and divide by $5$:
   $$\lim_{x\to0}\frac{\sin5x}{x} = \lim_{x\to0} 5 \cdot \frac{\sin5x}{5x}.$$
   Let $u = 5x$. As $x \to 0$, $u \to 0$.
   $$= 5 \cdot \lim_{u\to0}\frac{\sin u}{u} = 5 \cdot 1 = 5.$$

2. **Second Limit:**
   Multiply and divide numerator and denominator by their respective arguments ($2x$ and $3x$):
   $$\lim_{x\to0}\frac{\sin2x}{\sin3x} = \lim_{x\to0}\frac{\frac{\sin2x}{2x}\cdot 2x}{\frac{\sin3x}{3x}\cdot 3x} = \lim_{x\to0}\left(\frac{2x}{3x} \cdot \frac{\frac{\sin2x}{2x}}{\frac{\sin3x}{3x}}\right) = \frac{2}{3} \cdot \frac{\lim_{x\to0}\frac{\sin2x}{2x}}{\lim_{x\to0}\frac{\sin3x}{3x}}.$$
   Since $\lim_{x\to0}\frac{\sin2x}{2x} = 1$ and $\lim_{x\to0}\frac{\sin3x}{3x} = 1$:
   $$= \frac{2}{3} \cdot \frac{1}{1} = \frac{2}{3}.$$

---

### Exercise 14. A $0/0$ Limit with Trigonometry
Compute
$$\lim_{x\to0}\frac{1-\cos x}{x^2}.$$
Justify the result without using l'Hôpital's rule, using a trigonometric identity and the fundamental limit.

> **Why this exercise:** requires combining two known tools in one argument.

#### Solution

1. **Trigonometric Half-Angle Identity:**
   Recall the half-angle identity:
   $$1 - \cos x = 2\sin^2\left(\frac{x}{2}\right).$$

2. **Substitute and Reorganize:**
   $$\lim_{x\to0}\frac{1-\cos x}{x^2} = \lim_{x\to0}\frac{2\sin^2(x/2)}{x^2}.$$
   Rewrite the denominator to match $(x/2)^2$:
   $$x^2 = 4 \cdot \left(\frac{x}{2}\right)^2.$$
   Substitute into the fraction:
   $$= \lim_{x\to0}\frac{2\sin^2(x/2)}{4(x/2)^2} = \frac{2}{4} \lim_{x\to0}\left(\frac{\sin(x/2)}{x/2}\right)^2 = \frac{1}{2} \left[\lim_{x\to0}\frac{\sin(x/2)}{x/2}\right]^2.$$

3. **Evaluate:**
   Setting $u = \frac{x}{2}$, as $x \to 0$ we have $u \to 0$:
   $$= \frac{1}{2} \cdot (1)^2 = \frac{1}{2} = 0.5.$$

---

### Exercise 15. Observation Versus Proof
Choose one sequence and one function from this set. For the sequence, compute several values for increasingly large $n$. For the function, prepare a table of values with arguments approaching the limit point from the left and right. Sketch the behavior of both objects.

Compare the observation with the analytical result and explain why a finite number of calculations or a sketch does not constitute a proof that the limit exists.

> **Why this exercise:** teaches how to distinguish intuition and observation from mathematical argument.

#### Solution

1. **Chosen Sequence: $a_n = \frac{4n^2-3n+1}{2n^2+5n-7}$ (from Exercise 1):**
   - $n = 10$: $a_{10} = \frac{4(100)-30+1}{2(100)+50-7} = \frac{371}{243} \approx 1.5267$
   - $n = 100$: $a_{100} = \frac{40000-300+1}{20000+500-7} = \frac{39701}{20493} \approx 1.9373$
   - $n = 1\,000$: $a_{1000} = \frac{4000000-3000+1}{2000000+5000-7} = \frac{3997001}{2004993} \approx 1.9935$
   - $n = 10\,000$: $a_{10000} \approx 1.99935$
   *Observation:* As $n$ grows, $a_n$ monotonically increases toward $2$.

2. **Chosen Function: $f(x) = \frac{x^2-4x+3}{x-3}$ as $x \to 3$ (from Exercise 7):**
   - **Approaching from the left ($x \to 3^-$):**
     - $x = 2.9 \implies f(2.9) = 2.9 - 1 = 1.9$
     - $x = 2.99 \implies f(2.99) = 1.99$
     - $x = 2.999 \implies f(2.999) = 1.999$
   - **Approaching from the right ($x \to 3^+$):**
     - $x = 3.1 \implies f(3.1) = 3.1 - 1 = 2.1$
     - $x = 3.01 \implies f(3.01) = 2.01$
     - $x = 3.001 \implies f(3.001) = 2.001$
   *Observation:* From both sides, the values symmetrically converge to $2.0$.

3. **Observation Versus Mathematical Proof:**
   - **Why empirical data is not a proof:** Calculating a table of values or observing a plot tests only a tiny finite sample of points. It cannot reveal if a function has high-frequency microscopic oscillations near the limit point (such as $\sin(1/x)$), nor can it detect if a sequence alters its behavior for numbers larger than tested (e.g., $n > 10^{100}$). Numerical evaluations are also subject to machine floating-point rounding errors.
   - **What constitutes a proof:** A mathematical proof provides a universal deduction valid across all infinitely many numbers in the domain—demonstrating rigorously via algebraic identities, inequalities, and the formal $(\varepsilon, \delta)$ or $(\varepsilon, N)$ definitions that the distance between the expression and the limit can be made arbitrarily small for *all* points sufficiently close to the limit.
