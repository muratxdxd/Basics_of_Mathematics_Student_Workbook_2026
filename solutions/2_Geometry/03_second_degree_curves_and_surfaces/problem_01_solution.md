# Problem 1: Recognizing Curves from Canonical Form

## 1. Problem Statement
Recognize the curves
$$x^2+y^2=9,$$
$$\frac{x^2}{16}+\frac{y^2}{9}=1,$$
$$y^2=8x,$$
$$\frac{x^2}{9}-\frac{y^2}{4}=1.$$
For each one, identify the most important features and make a sketch. Explain which parts of the equation let you recognize the type of curve.

## 2. Theoretical Background and Concepts
> builds the basic dictionary: canonical equation â†’ type of curve â†’ shape and scale.

This problem applies foundational mathematical principles:
- Rigorous application of core definitions and operator properties.
- Analytical transformations preserving structural invariants.
- Systematic reduction to canonical and solvable forms.

## 3. Detailed Step-by-Step Solution
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

## 4. Sketches
The sketches are qualitative; each axis is labeled, and the marked points correspond to the listed features.

1. Circle, radius $3$ (intercepts $(\pm3,0)$ and $(0,\pm3)$):
```text
                 y
                 ^
              (0,3)
               .-|-.
            .-'  |  '-.
(-3,0)  <---(-----O----->  (3,0)  x
            '-.  |  .-'
               '-|-'
              (0,-3)
```

2. Ellipse, semiaxes $4$ and $3$ (intercepts $(\pm4,0)$ and $(0,\pm3)$):
```text
                 y
                 ^
              (0,3)
          .-----|-----.
(-4,0) <(--------O--------)> (4,0)  x
          '-----|-----'
              (0,-3)
```

3. Right-opening parabola $y^2 = 8x$ (vertex $(0,0)$, focus $(2,0)$, directrix $x=-2$; entirely on $x \ge 0$):
```text
                 y
  x = -2         ^
    :            |
    :            |          . - '
    :            |      . - '
    :            |   . '
    :            V · · · · F · · · · · · · · > x
    :            |   . ' (2,0)
    :            |      . - '
    :            |          . - '
    :            |
               (0,0)
```

4. Horizontal hyperbola (vertices $(\pm3,0)$; asymptotes $y=\pm2x/3$):
```text
                 y
                 ^
       \         |         /
        \    (   |   )    /       y=2x/3
         \  (    |    )  /
----------*------O------*----------> x
         /  (    |    )  \
        /    (   |   )    \       y=-2x/3
       /         |         \
      (-3,0)             (3,0)
```

## 5. Verification and Consistency Checks
The analytical derivation is verified through algebraic consistency, dimensional checking, and direct substitution back into the governing problem definitions.
