# Problem 8: Number of Requests Handled by a Server

## 1. Problem Statement
The rate at which requests arrive at a server during the first 5 minutes is described by the function
$$
r(t)=100+20t\quad [\text{requests/min}],\qquad 0\le t\le5.
$$

1. Compute the total number of requests that arrived during this time.
2. Compute the average rate of incoming requests over this interval.
3. Compare the average rate with the values $r(0)$ and $r(5)$.

## 2. Theoretical Background and Concepts
> it shows the integral as summation of a varying rate in an example directly related to computer science.

This problem applies foundational mathematical principles:
- Rigorous application of core definitions and operator properties.
- Analytical transformations preserving structural invariants.
- Systematic reduction to canonical and solvable forms.

## 3. Detailed Step-by-Step Solution
1. **Total Number of Requests:**
   Accumulate the rate over time via integration:
   $$R = \int_0^5 r(t)\,dt = \int_0^5 (100 + 20t)\,dt = \left[100t + 10t^2\right]_0^5 = 100(5) + 10(5^2) = 500 + 250 = 750\text{ requests}.$$

2. **Average Rate of Incoming Requests:**
   $$r_{\text{avg}} = \frac{R}{5 - 0} = \frac{750}{5} = 150\text{ requests/min}.$$

3. **Comparison with $r(0)$ and $r(5)$:**
   - $r(0) = 100 + 20(0) = 100\text{ requests/min}$.
   - $r(5) = 100 + 20(5) = 200\text{ requests/min}$.
   - Arithmetic mean of endpoint rates:
     $$\frac{r(0) + r(5)}{2} = \frac{100 + 200}{2} = 150\text{ requests/min} = r_{\text{avg}}.$$
   Because $r(t)$ is a linear function, its rate increases uniformly, making the integral average identical to the arithmetic midpoint of the starting and ending rates.

## More Difficult and Cross-Sectional Problems

## 4. Verification and Consistency Checks
The analytical derivation is verified through algebraic consistency, dimensional checking, and direct substitution back into the governing problem definitions.
