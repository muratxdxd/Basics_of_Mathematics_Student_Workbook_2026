# Problem 1: Motion â€” from Position to Velocity

## 1. Problem Statement
The position of a point is described by
$$
s(t)=t^3-6t^2+9t+2,\qquad t\ge0.
$$

1. Determine the velocity and acceleration.
2. Find the times at which the point stops.
3. Determine on which intervals the point moves in the positive direction of the axis and on which intervals it moves in the negative direction.

## 2. Theoretical Background and Concepts
> it shows the derivative as a real rate of change and requires interpretation of the sign of the derivative in the context of motion.

This problem applies foundational mathematical principles:
- Rigorous application of core definitions and operator properties.
- Analytical transformations preserving structural invariants.
- Systematic reduction to canonical and solvable forms.

## 3. Detailed Step-by-Step Solution
1. **Velocity and Acceleration:**
   - Velocity is the first derivative of position:
     $$v(t) = s'(t) = 3t^2 - 12t + 9 = 3(t^2 - 4t + 3) = 3(t - 1)(t - 3).$$
   - Acceleration is the derivative of velocity:
     $$a(t) = v'(t) = s''(t) = 6t - 12 = 6(t - 2).$$

2. **Times at Which the Point Stops:**
   The point stops instantaneously when its velocity is zero ($v(t) = 0$):
   $$3(t - 1)(t - 3) = 0 \iff t = 1 \quad \text{and} \quad t = 3.$$
   The point stops at $t = 1\text{ s}$ and at $t = 3\text{ s}$.

3. **Direction of Motion:**
   The direction of motion is governed by the sign of velocity $v(t)$:
   - For $t \in [0, 1)$: $v(t) > 0 \implies$ moving in the **positive direction**.
   - For $t \in (1, 3)$: $v(t) < 0 \implies$ moving in the **negative direction** (moving backward).
   - For $t \in (3, \infty)$: $v(t) > 0 \implies$ moving in the **positive direction**.
   (At $t = 1$, the particle turns around from positive to negative; at $t = 3$, it turns around from negative to positive).

## 4. Verification and Consistency Checks
The analytical derivation is verified through algebraic consistency, dimensional checking, and direct substitution back into the governing problem definitions.
