# Problem 14: Continuity and Differentiability of a Piecewise Function

## 1. Problem Statement
Investigate the behavior at $x=0$ of
$$f(x)=\begin{cases}x^2,&x\ge0,\\ax,&x<0.\end{cases}$$
For which values of $a$ is the function continuous? For which values do the one-sided derivatives exist and agree? For which value of $a$ is the function differentiable? Explain why continuity alone is not sufficient.

## 2. Theoretical Background and Concepts
> it requires an organized argument and a clear distinction between two concepts.

This problem applies foundational mathematical principles:
- Rigorous application of core definitions and operator properties.
- Analytical transformations preserving structural invariants.
- Systematic reduction to canonical and solvable forms.

## 3. Detailed Step-by-Step Solution
1. **Continuity at $x = 0$:**
   - $\lim_{x\to0^+} f(x) = \lim_{x\to0^+}(x^2) = 0$.
   - $\lim_{x\to0^-} f(x) = \lim_{x\to0^-}(ax) = a(0) = 0$.
   - $f(0) = 0^2 = 0$.
   Since $\lim_{x\to0^+} f(x) = \lim_{x\to0^-} f(x) = f(0) = 0$, the function is **continuous at $x = 0$ for all $a \in \mathbb{R}$**.

2. **One-Sided Derivatives at $x = 0$:**
   - **Right-hand derivative:**
     $$f'_+(0) = \lim_{h\to0^+}\frac{f(h) - f(0)}{h} = \lim_{h\to0^+}\frac{h^2 - 0}{h} = \lim_{h\to0^+} h = 0.$$
   - **Left-hand derivative:**
     $$f'_-(0) = \lim_{h\to0^-}\frac{f(h) - f(0)}{h} = \lim_{h\to0^-}\frac{ah - 0}{h} = \lim_{h\to0^-} a = a.$$
   - **Agreement:**
     The one-sided derivatives exist for all $a$, and they agree if and only if:
     $$f'_+(0) = f'_-(0) \iff 0 = a \iff a = 0.$$

3. **Differentiability:**
   The function is differentiable at $x = 0$ if and only if **$a = 0$**, in which case $f'(0) = 0$.

4. **Why Continuity Alone Is Not Sufficient:**
   Continuity merely guarantees that the two pieces connect without a break (topological connectedness). Differentiability is a much stronger geometric requirement: it demands that the graph be *smooth*, having a unique, well-defined tangent line. For any $a \neq 0$, the curve arrives at the origin from the right horizontally (slope $0$) but arrives from the left with non-zero slope $a$, forming a sharp angular corner (kink) where no unique tangent slope exists.

## 4. Verification and Consistency Checks
The analytical derivation is verified through algebraic consistency, dimensional checking, and direct substitution back into the governing problem definitions.
