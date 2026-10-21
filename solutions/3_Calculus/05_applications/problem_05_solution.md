# Problem 5: Distance from Velocity

## 1. Problem Statement
The velocity of a car during the first five seconds is described by the function
$$
v(t)=4t+2\quad [\mathrm{m/s}].
$$

Compute the distance traveled and explain why the integral of velocity gives the change in position.

Then answer what would have to be changed in the reasoning if the velocity also took negative values.

## 2. Theoretical Background and Concepts
> it connects the integral with accumulation and distinguishes displacement from the actual distance traveled.

This problem applies foundational mathematical principles:
- Rigorous application of core definitions and operator properties.
- Analytical transformations preserving structural invariants.
- Systematic reduction to canonical and solvable forms.

## 3. Detailed Step-by-Step Solution
1. **Compute Distance Traveled on $[0, 5]$:**
   Since $v(t) = 4t + 2 > 0$ for all $t \in [0, 5]$, the car moves in one direction only:
   $$s = \int_0^5 v(t)\,dt = \int_0^5 (4t + 2)\,dt = \left[2t^2 + 2t\right]_0^5 = 2(5^2) + 2(5) = 2(25) + 10 = 50 + 10 = 60\text{ meters}.$$

2. **Why the Integral of Velocity Gives Change in Position:**
   By definition, velocity is the instantaneous rate of change of position: $v(t) = \frac{ds}{dt}$.
   Over an infinitesimal time interval $dt$, the incremental displacement is $ds = v(t)dt$.
   By the Fundamental Theorem of Calculus, integrating this rate accumulates all the tiny displacements over the full time interval:
   $$\int_{t_1}^{t_2} v(t)\,dt = \int_{t_1}^{t_2} s'(t)\,dt = s(t_2) - s(t_1) = \Delta s.$$

3. **Modification if Velocity Took Negative Values:**
   If velocity takes negative values, $\int_{t_1}^{t_2} v(t)\,dt$ calculates **net displacement** (where backward travel cancels out forward travel).
   To compute the actual **total physical distance traveled** (odometer distance), one must integrate the absolute speed:
   $$s_{\text{distance}} = \int_{t_1}^{t_2} |v(t)|\,dt.$$

## 4. Verification and Consistency Checks
The analytical derivation is verified through algebraic consistency, dimensional checking, and direct substitution back into the governing problem definitions.
