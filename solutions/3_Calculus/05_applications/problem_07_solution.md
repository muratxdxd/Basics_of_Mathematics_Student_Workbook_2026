# Problem 7: Exponential Growth

## 1. Problem Statement
Assume the model
$$
N(t)=N_0e^{kt},\qquad k>0.
$$

1. Verify by differentiation that the model satisfies the relation $N'(t)=kN(t)$.
2. Find the population doubling time.
3. Explain why the doubling time does not depend on $N_0$.

## 2. Theoretical Background and Concepts
> it shows the connection between the exponential function and a growth rate proportional to the current value, without introducing a separate technique for solving differential equations.

This problem applies foundational mathematical principles:
- Rigorous application of core definitions and operator properties.
- Analytical transformations preserving structural invariants.
- Systematic reduction to canonical and solvable forms.

## 3. Detailed Step-by-Step Solution
1. **Verify $N'(t) = kN(t)$:**
   Differentiate using the chain rule:
   $$N'(t) = \frac{d}{dt}\left(N_0 e^{kt}\right) = N_0 \cdot \left(e^{kt} \cdot k\right) = k\left(N_0 e^{kt}\right) = k N(t).$$
   The derivative is directly proportional to the current population with constant of proportionality $k$.

2. **Find Doubling Time $T$:**
   The population doubles when $N(T) = 2N_0$:
   $$N_0 e^{kT} = 2N_0 \implies e^{kT} = 2 \implies kT = \ln 2 \implies T = \frac{\ln 2}{k} \approx \frac{0.69315}{k}.$$

3. **Why Doubling Time Does Not Depend on $N_0$:**
   In the equation $N_0 e^{kT} = 2N_0$, the initial population $N_0$ divides out completely. Exponential growth is scale-invariant: growing by a fixed percentage or factor requires multiplying the current size, which takes the exact same amount of time regardless of whether the population starts at $10$ organisms or $10\,000\,000$.

## 4. Verification and Consistency Checks
The analytical derivation is verified through algebraic consistency, dimensional checking, and direct substitution back into the governing problem definitions.
