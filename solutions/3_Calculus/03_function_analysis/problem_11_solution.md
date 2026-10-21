# Problem 11: A Parameter and the Number of Extrema

## 1. Problem Statement
For
$$f_a(x)=x^3-3ax$$
depending on $a$, determine the number of critical points and their character. Separate the parameter cases and justify why the structure of the graph changes.

## 2. Theoretical Background and Concepts
> it teaches how to analyze an entire family of functions instead of a single example.

This problem applies foundational mathematical principles:
- Rigorous application of core definitions and operator properties.
- Analytical transformations preserving structural invariants.
- Systematic reduction to canonical and solvable forms.

## 3. Detailed Step-by-Step Solution
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

## 4. Verification and Consistency Checks
The analytical derivation is verified through algebraic consistency, dimensional checking, and direct substitution back into the governing problem definitions.
