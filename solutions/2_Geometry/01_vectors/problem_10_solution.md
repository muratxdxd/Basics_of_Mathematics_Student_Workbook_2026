# Problem 10: Triangle Area from Vectors

## 1. Problem Statement
The points $A=(0,0,0)$, $B=(2,1,0)$, and $C=(1,3,2)$ form a triangle. Construct $\overrightarrow{AB}$ and $\overrightarrow{AC}$, compute the area of the parallelogram using the cross product, and then find the area of the triangle. Explain the factor $\frac12$.

## 2. Theoretical Background and Concepts
> shows the interpretation of the length of the cross product as area.

This problem applies foundational mathematical principles:
- Rigorous application of core definitions and operator properties.
- Analytical transformations preserving structural invariants.
- Systematic reduction to canonical and solvable forms.

## 3. Detailed Step-by-Step Solution
1. **Construct Vectors:**
   $$\overrightarrow{AB} = B - A = (2 - 0, 1 - 0, 0 - 0) = (2, 1, 0).$$
   $$\overrightarrow{AC} = C - A = (1 - 0, 3 - 0, 2 - 0) = (1, 3, 2).$$

2. **Cross Product $\overrightarrow{AB} \times \overrightarrow{AC}$:**
   $$\overrightarrow{AB} \times \overrightarrow{AC} = \det\begin{pmatrix}i & j & k \\ 2 & 1 & 0 \\ 1 & 3 & 2\end{pmatrix} = i(1\cdot 2 - 0\cdot 3) - j(2\cdot 2 - 0\cdot 1) + k(2\cdot 3 - 1\cdot 1) = (2, -4, 5).$$

3. **Area of Parallelogram:**
   $$\text{Area}_{\text{parallelogram}} = \|\overrightarrow{AB} \times \overrightarrow{AC}\| = \sqrt{2^2 + (-4)^2 + 5^2} = \sqrt{4 + 16 + 25} = \sqrt{45} = 3\sqrt{5}.$$

4. **Area of Triangle:**
   $$\text{Area}_{\Delta ABC} = \frac{1}{2} \|\overrightarrow{AB} \times \overrightarrow{AC}\| = \frac{3\sqrt{5}}{2} \approx 3.354.$$

5. **Explanation of the Factor $\frac{1}{2}$:**
   A parallelogram is divided into two congruent triangles by either of its diagonals. The triangle formed by vertices $A, B, C$ has base $\|\overrightarrow{AB}\|$ and height $h = \|\overrightarrow{AC}\|\sin\theta$. Its area is $\frac{1}{2}\text{base}\times\text{height}$, which is precisely half the area of the full parallelogram spanned by $\overrightarrow{AB}$ and $\overrightarrow{AC}$.

## More Challenging Exercises

## 4. Verification and Consistency Checks
The analytical derivation is verified through algebraic consistency, dimensional checking, and direct substitution back into the governing problem definitions.
