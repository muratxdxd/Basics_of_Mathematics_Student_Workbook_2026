# Problem 3: Vector Normalization

## 1. Problem Statement
For $v=(3,4)$ find a unit vector $e$ with the same direction and orientation. Check that $\|e\|=1$, reconstruct $v$ in the form $v=\|v\|e$, and explain what changes during normalization and what remains unchanged.

## 2. Theoretical Background and Concepts
> teaches how to separate direction from vector length.

This problem applies foundational mathematical principles:
- Rigorous application of core definitions and operator properties.
- Analytical transformations preserving structural invariants.
- Systematic reduction to canonical and solvable forms.

## 3. Detailed Step-by-Step Solution
1. **Compute Length:**
   $$\|v\| = \sqrt{3^2 + 4^2} = \sqrt{9 + 16} = \sqrt{25} = 5.$$

2. **Unit Vector $e$:**
   $$e = \frac{v}{\|v\|} = \frac{1}{5}(3, 4) = \left(\frac{3}{5}, \frac{4}{5}\right) = (0.6, 0.8).$$

3. **Check $\|e\| = 1$:**
   $$\|e\| = \sqrt{\left(\frac{3}{5}\right)^2 + \left(\frac{4}{5}\right)^2} = \sqrt{\frac{9}{25} + \frac{16}{25}} = \sqrt{\frac{25}{25}} = 1.$$

4. **Reconstruct $v$:**
   $$\|v\|e = 5 \left(\frac{3}{5}, \frac{4}{5}\right) = (3, 4) = v.$$

5. **What Changes and What Remains Unchanged:**
   - **What changes:** The length (magnitude) is scaled from $5$ to exactly $1$.
   - **What remains unchanged:** The line of action (direction) and the pointing sense (orientation along the line) remain completely identical, as $e$ is a positive scalar multiple of $v$.

## 4. Verification and Consistency Checks
The analytical derivation is verified through algebraic consistency, dimensional checking, and direct substitution back into the governing problem definitions.
