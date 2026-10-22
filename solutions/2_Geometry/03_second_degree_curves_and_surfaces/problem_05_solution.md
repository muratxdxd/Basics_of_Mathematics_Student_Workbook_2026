# Problem 5: Hyperbola and Asymptotes

## 1. Problem Statement
For
$$\frac{x^2}{16}-\frac{y^2}{9}=1,$$
find the intercepts with the $x$-axis, the asymptotes, and make a sketch. Explain why the asymptotes describe the behavior of the curve far from the center.

## 2. Theoretical Background and Concepts
> shows the role of asymptotes in understanding the global shape of a hyperbola.

This problem applies foundational mathematical principles:
- Rigorous application of core definitions and operator properties.
- Analytical transformations preserving structural invariants.
- Systematic reduction to canonical and solvable forms.

## 3. Detailed Step-by-Step Solution
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
   Relative closeness of the curve to a line alone does not show that their absolute vertical difference tends to zero. On the corresponding branch, rationalize that difference:
   $$|y_{\text{curve}}-y_{\text{asymptote}}|=\frac{3}{4}|x|\left(1-\sqrt{1-\frac{16}{x^2}}\right)
   =\frac{12}{|x|\left(1+\sqrt{1-\frac{16}{x^2}}\right)}\longrightarrow 0
   \quad\text{as }|x|\to\infty.$$
   Hence the two branches approach the asymptotes $y=\pm\frac{3}{4}x$ with absolute vertical distance tending to zero.

## 4. Sketch
Both branches, their vertices, axes, and asymptotes are shown schematically:
```text
                 y
                 ^
       \         |         /
        \      .'|'.      /    y=3x/4
         \   .'  |  '.   /
          \.'    |    '. /
<--- branch *----O----* branch ---> x
          /'.    |    .'\
         /   '.  |  .'   \         y=-3x/4
        /      '.|.'      \
       /         |         \
            (-4,0) (4,0)
```

## 5. Verification and Consistency Checks
The analytical derivation is verified through algebraic consistency, dimensional checking, and direct substitution back into the governing problem definitions.
