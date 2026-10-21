# Problem 11: Decomposition into Parallel and Perpendicular Components

## 1. Problem Statement
Decompose $u=(3,4)$ into components parallel and perpendicular to $v=(1,2)$. Check
$$u=u_{\parallel}+u_{\perp},\qquad u_{\perp}\cdot v=0.$$
Explain why these are two independent checks of correctness.

## 2. Theoretical Background and Concepts
> deepens the idea of projection through construction and verification.

This problem applies foundational mathematical principles:
- Rigorous application of core definitions and operator properties.
- Analytical transformations preserving structural invariants.
- Systematic reduction to canonical and solvable forms.

## 3. Detailed Step-by-Step Solution
1. **Parallel Component $u_\parallel$:**
   $$u_\parallel = \operatorname{proj}_v u = \frac{u \cdot v}{\|v\|^2} v.$$
   $$u \cdot v = 3(1) + 4(2) = 11, \qquad \|v\|^2 = 1^2 + 2^2 = 5.$$
   $$u_\parallel = \frac{11}{5}(1, 2) = \left(\frac{11}{5}, \frac{22}{5}\right) = (2.2, 4.4).$$

2. **Perpendicular Component $u_\perp$:**
   $$u_\perp = u - u_\parallel = (3, 4) - \left(\frac{11}{5}, \frac{22}{5}\right) = \left(\frac{15-11}{5}, \frac{20-22}{5}\right) = \left(\frac{4}{5}, -\frac{2}{5}\right) = (0.8, -0.4).$$

## 4. Verification and Consistency Checks
3. **Verification Checks:**
   - **Check 1 (Sum consistency):**
     $$u_\parallel + u_\perp = (2.2, 4.4) + (0.8, -0.4) = (3.0, 4.0) = u.$$
   - **Check 2 (Orthogonality):**
     $$u_\perp \cdot v = \frac{4}{5}(1) + \left(-\frac{2}{5}\right)(2) = \frac{4}{5} - \frac{4}{5} = 0.$$

4. **Why These Are Two Independent Checks:**
   Check 1 verifies that the decomposition is complete and preserves the entire vector $u$ without any loss of magnitude or component. Check 2 verifies that $u_\perp$ is genuinely orthogonal to the subspace spanned by $v$. One could easily pick an incorrect vector that adds up to $u$ but fails orthogonality, or a vector that is orthogonal to $v$ but does not sum to $u$. Satisfying both proves uniqueness and correctness.
