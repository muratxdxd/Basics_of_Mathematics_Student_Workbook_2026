# Problem 10: Paraboloids

## 1. Problem Statement
Compare
$$z=x^2+y^2$$
and
$$z=x^2-y^2.$$
For each surface, describe the cross-sections $x=0$, $y=0$, and $z=c$, then make a qualitative sketch.

## 2. Theoretical Background and Concepts
> teaches how to distinguish two basic types of paraboloids from their cross-sections.

This problem applies foundational mathematical principles:
- Rigorous application of core definitions and operator properties.
- Analytical transformations preserving structural invariants.
- Systematic reduction to canonical and solvable forms.

## 3. Detailed Step-by-Step Solution
1. **Surface 1: $z = x^2 + y^2$ (Elliptic Paraboloid):**
   - **Cross-section $x = 0$:** $z = y^2$ (a parabola in the $yz$-plane opening upward with vertex at $(0,0,0)$).
   - **Cross-section $y = 0$:** $z = x^2$ (a parabola in the $xz$-plane opening upward with vertex at $(0,0,0)$).
   - **Cross-sections $z = c$:**
     - For $c > 0$: $x^2 + y^2 = c$ (circles of radius $\sqrt{c}$ that widen as $z$ increases).
     - For $c = 0$: $x^2 + y^2 = 0$ (the single vertex point $(0, 0, 0)$).
     - For $c < 0$: no real points (the surface lies entirely in the upper half-space $z \ge 0$).
   - **Shape:** A rotationally symmetric "bowl".

2. **Surface 2: $z = x^2 - y^2$ (Hyperbolic Paraboloid):**
   - **Cross-section $x = 0$:** $z = -y^2$ (a parabola in the $yz$-plane opening **downward**).
   - **Cross-section $y = 0$:** $z = x^2$ (a parabola in the $xz$-plane opening **upward**).
   - **Cross-sections $z = c$:**
     - For $c > 0$: $x^2 - y^2 = c$ (hyperbolas with vertices on the $x$-axis at $(\pm\sqrt{c}, 0, c)$).
     - For $c = 0$: $x^2 - y^2 = 0 \iff y = \pm x$ (a pair of intersecting straight lines through the origin).
     - For $c < 0$: $y^2 - x^2 = -c = |c|$ (hyperbolas with vertices on the $y$-axis at $(0, \pm\sqrt{|c|}, c)$).
   - **Shape:** A "saddle" (or mountain pass). At $(0,0,0)$, the surface curves up along $x$ and down along $y$.

## 4. Qualitative Sketches and Coordinate Traces

1. **Surface 1: $z = x^2 + y^2$ (Elliptic Paraboloid — Upward-Opening Bowl):**
   The minimum is at the origin $O(0,0,0)$, and the surface opens upward into $z \ge 0$. Every vertical coordinate section ($z=x^2$ for $y=0$, and $z=y^2$ for $x=0$) is an upward parabola opening from $O$, and horizontal sections $z=c > 0$ are circles of radius $\sqrt{c}$:

```text
       Perspective View:                         Coordinate Section (y=0 or x=0):
              z                                           z
              ^     z=c: circular rim                     ^
              |        .-------.                          |   z = x²  (or z = y²)
          \   |   /  .'         '.                    \   |   /
           \  |  /  (             )                    \  |  /  upward parabola
            \ | /    '.         .'                      \ | /   minimum at O
             \|/       '-------'                         \|/
              O-------------------> x                     O--------------> x (or y)
             /                                      minimum (0,0,0)
            v y
       minimum at origin (0,0,0)
```

2. **Surface 2: $z = x^2 - y^2$ (Hyperbolic Paraboloid — Saddle Surface):**
   The origin $O(0,0,0)$ is a saddle point. The two coordinate traces through $O$ demonstrate the opposing curvatures:
   - **Along the $x$-axis ($y = 0$, $xz$-plane):** $z = x^2$, an **upward-opening parabola** (curves upward with minimum at $O$).
   - **Along the $y$-axis ($x = 0$, $yz$-plane):** $z = -y^2$, a **downward-opening parabola** (curves downward with maximum at $O$).

```text
   Trace in y=0 (xz-plane):                Trace in x=0 (yz-plane):
              z                                           z
              ^                                           ^
              |   z = x² (upward)                         |   maximum at O
          \   |   /                                       O--------------> y
           \  |  /   minimum at O                        /|\
            \ | /                                       / | \   z = -y² (downward)
             \|/                                       /  |  \
              O--------------> x                      /   v   \

   Combined 3D Perspective (Saddle):
              z
              ^          upward trace z = x² (along x)
          \   |   /      . - '
           \  |  /   . - '
            \ | /.-'
             \|O'-------------------> x
            .'|\
        .-'   | \  downward trace z = -y² (along y)
    .-'       |  \
   v y        v
```

## More Challenging Exercises

## 5. Verification and Consistency Checks
The analytical derivation is verified through algebraic consistency, dimensional checking, and direct substitution back into the governing problem definitions.
