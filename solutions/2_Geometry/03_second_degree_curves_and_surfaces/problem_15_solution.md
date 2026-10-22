# Problem 15: Recognition and Sketch Without a Given Name

## 1. Problem Statement
Consider the two equations:

$$4x^2+9y^2-8x+36y+4=0,$$

$$4x^2+y^2=z^2.$$

For the first equation, reduce it to canonical form, recognize the curve, give its most important features, and make a sketch.

For the second equation, do not begin by using a ready-made name for the surface. First describe the cross-sections $z=c$ and the cross-sections by the planes $x=0$ and $y=0$, paying attention to the different scales along the axes. Only then identify the surface and make a sketch.

## 2. Theoretical Background and Concepts
> tests transfer of the two main mechanisms of the setâ€”moving to canonical form and recognizing an object through cross-sectionsâ€”without allowing the easiest example to be chosen.

This problem applies foundational mathematical principles:
- Rigorous application of core definitions and operator properties.
- Analytical transformations preserving structural invariants.
- Systematic reduction to canonical and solvable forms.

## 3. Detailed Step-by-Step Solution
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
   - **Sketch:** The ellipse is centered at $(1,-2)$, with horizontal major axis and the four vertices/co-vertices shown:
```text
                 y
                 ^
                 |                 * (1,0)
      ------------O----------------------------> x
                 |        .-------' '-.
                 |     .-'      |      '-.
      (-2,-2) *--|----C-------------------* (4,-2)
                 |     '-.      |      .-'
                 |        '-----*-----'
                 |            (1,-4)
                 v          C=(1,-2)
```

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
   - **Sketch:** At each nonzero height $z=c$, the horizontal ellipse has $x$-semiaxis $|c|/2$ and $y$-semiaxis $|c|$, so its $y$-semiaxis is twice its $x$-semiaxis:
```text
                            z
                            ^
                 .----------|----------.   z=c: y semiaxis |c|,
              .-'           |           '-.       x semiaxis |c|/2
             /              |              \
             \              |              /
              '-.           |           .-'
                  '-.       |       .-'
                      '-.   |   .-'
                          \  |  /
                           \ | /
                            \|/
                             O----------------> x
                            /|\
                           / | \
                          /  |  \
                         /   |   \
                        v    y
                   apex (0,0,0)
```

## 4. Verification and Consistency Checks
The analytical derivation is verified through algebraic consistency, dimensional checking, and direct substitution back into the governing problem definitions.
