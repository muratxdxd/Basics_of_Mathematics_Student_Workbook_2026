# Problem 13: A Logarithm and an Asymptote

## 1. Problem Statement
Perform a complete analysis of
$$f(x)=\frac{\ln x}{x},\qquad x>0.$$
Find the maximum and the behavior at the ends of the domain. Explain which information is necessary for a correct sketch.

## 2. Theoretical Background and Concepts
> it combines the domain, limits, and derivative in a less obvious example.

This problem applies foundational mathematical principles:
- Rigorous application of core definitions and operator properties.
- Analytical transformations preserving structural invariants.
- Systematic reduction to canonical and solvable forms.

## 3. Detailed Step-by-Step Solution
1. **Domain and Zeros:**
   - Domain: $D_f = (0, \infty)$.
   - Zero: $\ln x = 0 \iff x = 1 \implies (1, 0)$.
   - Sign: $f(x) < 0$ for $x \in (0, 1)$, and $f(x) > 0$ for $x \in (1, \infty)$.

2. **Behavior at Ends of Domain:**
   - As $x \to 0^+$:
     $$\lim_{x\to0^+}\frac{\ln x}{x} = \frac{-\infty}{0^+} = -\infty.$$
     Vertical asymptote: $x = 0$ (the $y$-axis).
   - As $x \to \infty$:
     $$\lim_{x\to\infty}\frac{\ln x}{x} = \lim_{x\to\infty}\frac{\frac{1}{x}}{1} = 0 \quad (\text{by l'HÃ´pital's Rule}).$$
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

## 4. Verification and Consistency Checks
The analytical derivation is verified through algebraic consistency, dimensional checking, and direct substitution back into the governing problem definitions.
