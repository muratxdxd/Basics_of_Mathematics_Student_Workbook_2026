# Problem 15: Recovering a Function from Its Derivative and a Condition

## 1. Problem Statement
The function $F$ satisfies
$$F'(x)=2xe^{x^2}$$
and
$$F(0)=3.$$

1. Recognize the method needed to find the function $F$.
2. Determine the entire family of functions with the given derivative.
3. Use the condition $F(0)=3$ to determine the correct constant.
4. Verify the final result by differentiation and substitution of $x=0$.

## 2. Theoretical Background and Concepts
> it combines recognition of substitution, the meaning of the constant of integration, and an initial condition in one problem, using only mechanisms introduced earlier.

This problem applies foundational mathematical principles:
- Rigorous application of core definitions and operator properties.
- Analytical transformations preserving structural invariants.
- Systematic reduction to canonical and solvable forms.

## 3. Detailed Step-by-Step Solution
1. **Recognize the Method:**
   To find $F(x)$, we must compute the indefinite integral $\int 2x e^{x^2}\,dx$. Because the integrand consists of an exponential function with argument $x^2$ multiplied by $2x$ (which is the exact derivative of $x^2$), the appropriate method is **Substitution** with $u = x^2$.

2. **Entire Family of Antiderivatives:**
   Let $u = x^2 \implies du = 2x\,dx$.
   $$F(x) = \int 2x e^{x^2}\,dx = \int e^u\,du = e^u + C = e^{x^2} + C, \qquad C \in \mathbb{R}.$$

3. **Determine the Constant using $F(0) = 3$:**
   Substitute $x = 0$:
   $$F(0) = e^{0^2} + C = e^0 + C = 1 + C.$$
   Setting $F(0) = 3$:
   $$1 + C = 3 \implies C = 2.$$
   The specific function is:
   $$F(x) = e^{x^2} + 2.$$

## 4. Verification and Consistency Checks
4. **Verification:**
   - **Check derivative:**
     $$F'(x) = \frac{d}{dx}\left(e^{x^2} + 2\right) = e^{x^2}\cdot\frac{d}{dx}(x^2) + 0 = 2x e^{x^2} \quad (\text{matches } F'(x)).$$
   - **Check initial condition:**
     $$F(0) = e^{0^2} + 2 = 1 + 2 = 3 \quad (\text{matches } F(0) = 3).$$
   The solution is verified.
