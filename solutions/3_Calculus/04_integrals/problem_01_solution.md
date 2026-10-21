# Problem 1: Antiderivative and Verification

## 1. Problem Statement
For
$$f(x)=3x^2-4x+5$$
find one antiderivative $F(x)$. Write the entire family of antiderivatives, verify the result by differentiation, and explain the meaning of the constant $C$.

## 2. Theoretical Background and Concepts
> it introduces integration as the inverse operation to differentiation.

This problem applies foundational mathematical principles:
- Rigorous application of core definitions and operator properties.
- Analytical transformations preserving structural invariants.
- Systematic reduction to canonical and solvable forms.

## 3. Detailed Step-by-Step Solution
1. **Find One Antiderivative $F(x)$:**
   Apply the power rule of integration $\int x^n\,dx = \frac{x^{n+1}}{n+1}$:
   $$F(x) = 3\left(\frac{x^3}{3}\right) - 4\left(\frac{x^2}{2}\right) + 5x = x^3 - 2x^2 + 5x.$$

2. **Entire Family of Antiderivatives:**
   $$\int (3x^2 - 4x + 5)\,dx = x^3 - 2x^2 + 5x + C, \qquad C \in \mathbb{R}.$$

## 4. Verification and Consistency Checks
3. **Verification by Differentiation:**
   $$\frac{d}{dx}\left(x^3 - 2x^2 + 5x + C\right) = 3x^2 - 4x + 5 + 0 = f(x).$$
   The derivative equals the original integrand.

4. **Meaning of the Constant $C$:**
   Because the derivative of any constant is zero ($\frac{d}{dx}C = 0$), adding a constant shifts the graph of the antiderivative vertically without changing its slope at any point $x$. On a connected interval, if two functions share the exact same derivative, their difference must be a constant. Thus, $C$ indexes all possible vertical offsets that satisfy the slope prescription $f(x)$.
