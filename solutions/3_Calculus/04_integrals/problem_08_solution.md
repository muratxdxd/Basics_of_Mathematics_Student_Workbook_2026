# Problem 8: Choosing the Factors in Integration by Parts

## 1. Problem Statement
Compute
$$\int x\cos x\,dx.$$
Before calculating, justify why it is convenient to differentiate $x$ and integrate $\cos x$, rather than the other way around.

## 2. Theoretical Background and Concepts
> it teaches that integration by parts requires a deliberate choice of factors.

This problem applies foundational mathematical principles:
- Rigorous application of core definitions and operator properties.
- Analytical transformations preserving structural invariants.
- Systematic reduction to canonical and solvable forms.

## 3. Detailed Step-by-Step Solution
1. **Justification of Factor Choice:**
   - If we set $u = x$ and $v' = \cos x$:
     Differentiating $u$ gives $u' = 1$ (reducing polynomial degree from $1$ to $0$), while integrating $v'$ yields $v = \sin x$ (which stays at the same level of complexity). The new integral $\int u' v\,dx = \int \sin x\,dx$ is immediately solvable.
   - If we chose the opposite ($u = \cos x$ and $v' = x$):
     Differentiating gives $u' = -\sin x$ and integrating gives $v = \frac{x^2}{2}$. The new integral would be $-\frac{1}{2}\int x^2\sin x\,dx$, which has a higher power $x^2$ and is more difficult than the original integral!

2. **Calculation:**
   - $u = x \implies u' = 1$.
   - $v' = \cos x \implies v = \sin x$.
   $$\int x\cos x\,dx = x\sin x - \int (1)\sin x\,dx = x\sin x - (-\cos x) + C = x\sin x + \cos x + C.$$

## 4. Verification and Consistency Checks
3. **Verification:**
   $$\frac{d}{dx}(x\sin x + \cos x + C) = (1\cdot\sin x + x\cos x) - \sin x = x\cos x.$$
