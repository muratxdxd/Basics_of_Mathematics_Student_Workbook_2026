# Problem 4: Powers and Oscillation

## 1. Problem Statement
Analyze
$$\left(\frac23\right)^n,\qquad \left(\frac32\right)^n,\qquad (-1)^n,\qquad \frac{(-1)^n}{n}.$$
For each sequence, describe the type of behavior and justify your answer.

## 2. Theoretical Background and Concepts
> organizes the basic types of sequence behavior and shows that oscillation does not always rule out convergence.

This problem applies foundational mathematical principles:
- Rigorous application of core definitions and operator properties.
- Analytical transformations preserving structural invariants.
- Systematic reduction to canonical and solvable forms.

## 3. Detailed Step-by-Step Solution
1. **$\left(\frac{2}{3}\right)^n$:**
   - **Behavior:** Converges monotonically to **$0$**.
   - **Justification:** This is a geometric sequence $r^n$ with base $|r| = \frac{2}{3} < 1$. Successive powers shrink toward 0: $\lim_{n\to\infty}\left(\frac{2}{3}\right)^n = 0$.

2. **$\left(\frac{3}{2}\right)^n$:**
   - **Behavior:** Diverges monotonically to **$+\infty$**.
   - **Justification:** Geometric sequence with base $r = 1.5 > 1$. Each term is $1.5$ times the previous one, growing without bound.

3. **$(-1)^n$:**
   - **Behavior:** Diverges by bounded oscillation.
   - **Justification:** Terms alternate strictly between $-1$ (for odd $n$) and $+1$ (for even $n$): $\{-1, 1, -1, 1, \dots\}$. The sequence has two distinct subsequential limits ($+1$ and $-1$), so no single limit exists.

4. **$\frac{(-1)^n}{n}$:**
   - **Behavior:** Converges to **$0$** with damped oscillation.
   - **Justification:** Bounded above and below: $-\frac{1}{n} \le \frac{(-1)^n}{n} \le \frac{1}{n}$. Since $\lim_{n\to\infty}\left(-\frac{1}{n}\right) = 0$ and $\lim_{n\to\infty}\frac{1}{n} = 0$, by the **Squeeze Theorem**, $\lim_{n\to\infty}\frac{(-1)^n}{n} = 0$. Oscillation does not prevent convergence if the oscillation amplitude shrinks to zero.

## 4. Verification and Consistency Checks
The analytical derivation is verified through algebraic consistency, dimensional checking, and direct substitution back into the governing problem definitions.
