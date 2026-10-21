# Problem 7: Integration by Parts as Reversing the Product Rule

## 1. Problem Statement
Compute
$$\int xe^x\,dx.$$
First write the product differentiation rule and, on that basis, explain the meaning of the integration-by-parts formula. Verify the result by differentiation.

## 2. Theoretical Background and Concepts
> it connects a new technique with the familiar product rule.

This problem applies foundational mathematical principles:
- Rigorous application of core definitions and operator properties.
- Analytical transformations preserving structural invariants.
- Systematic reduction to canonical and solvable forms.

## 3. Detailed Step-by-Step Solution
1. **Origin from Product Rule:**
   $$\frac{d}{dx}\left(u(x)v(x)\right) = u'(x)v(x) + u(x)v'(x).$$
   Integrating both sides with respect to $x$:
   $$u(x)v(x) = \int u'(x)v(x)\,dx + \int u(x)v'(x)\,dx.$$
   Rearranging terms gives the **integration by parts formula**:
   $$\int u(x)v'(x)\,dx = u(x)v(x) - \int u'(x)v(x)\,dx.$$
   Integration by parts transfers differentiation from one factor ($u$) to the other ($v'$), simplifying integrals where a power of $x$ can be diminished to a constant.

2. **Compute $\int x e^x\,dx$:**
   Choose:
   - $u = x \implies u' = 1$.
   - $v' = e^x \implies v = e^x$.
   $$\int x e^x\,dx = x e^x - \int (1)e^x\,dx = x e^x - e^x + C = (x - 1)e^x + C.$$

## 4. Verification and Consistency Checks
3. **Verification by Differentiation:**
   $$\frac{d}{dx}\left((x - 1)e^x + C\right) = (1)e^x + (x - 1)e^x = e^x + xe^x - e^x = xe^x.$$
