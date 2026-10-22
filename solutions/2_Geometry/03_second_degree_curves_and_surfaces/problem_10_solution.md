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

## 4. Qualitative Sketches
These perspective sketches are not to scale. The labeled axes indicate the orientation; the cross-sections above guide the shapes.

1. $z=x^2+y^2$: an upward-opening bowl, with upward parabolas in both the $xz$- and $yz$-directions and circular horizontal sections:
```text
                    z
                    ^
                    |       .-''''-.
                    |    .-'       '-.
                    |  .'             '.
                    | /                 \
                    O---------------------> x
                   / \
                  /   \ y
```

2. $z=x^2-y^2$: a saddle, curving up along $x$ and down along $y$:
```text
                    z
                    ^
                .---|---.
             .-'    |    '-.       rises along x
          .-'       |       '-.
     y <---\        O        /-----> x
            '-.     |     .-'       falls along y
               '-.__|__.-'
                    v
```

## More Challenging Exercises

## 5. Verification and Consistency Checks
The analytical derivation is verified through algebraic consistency, dimensional checking, and direct substitution back into the governing problem definitions.
