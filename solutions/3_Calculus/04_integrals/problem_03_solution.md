# Problem 3: Recognizing Basic Antiderivatives

## 1. Problem Statement
Compute
$$\int\left(2e^x+3\cos x-4\sin x\right)\,dx.$$
Match each term with a known derivative and verify the entire result with one differentiation.

## 2. Theoretical Background and Concepts
> it builds a catalogue of basic antiderivatives from known derivatives.

This problem applies foundational mathematical principles:
- Rigorous application of core definitions and operator properties.
- Analytical transformations preserving structural invariants.
- Systematic reduction to canonical and solvable forms.

## 3. Detailed Step-by-Step Solution
1. **Match Each Term with Known Derivatives:**
   - Since $\frac{d}{dx}(e^x) = e^x$, we have $\int 2e^x\,dx = 2e^x$.
   - Since $\frac{d}{dx}(\sin x) = \cos x$, we have $\int 3\cos x\,dx = 3\sin x$.
   - Since $\frac{d}{dx}(-\cos x) = \sin x$, we have $\int -4\sin x\,dx = 4\cos x$.

2. **Combine Results:**
   $$\int\left(2e^x+3\cos x-4\sin x\right)\,dx = 2e^x + 3\sin x + 4\cos x + C.$$

## 4. Verification and Consistency Checks
3. **Verification by Differentiation:**
   $$\frac{d}{dx}\left(2e^x + 3\sin x + 4\cos x + C\right) = 2e^x + 3\cos x + 4(-\sin x) + 0 = 2e^x + 3\cos x - 4\sin x.$$
