# Inverse Matrix

## Goal of the Set

After completing this set, the student should understand what an inverse matrix is, when it exists, be able to find it using basic methods, check the result, and use the inverse to solve simple problems.

## Basic Exercises

### Exercise 1. Definition of the Inverse
For
$$A=\begin{pmatrix}2&1\\1&1\end{pmatrix},\qquad B=\begin{pmatrix}1&-1\\-1&2\end{pmatrix}$$
check, without using a formula, whether $B=A^{-1}$. Compute $AB$ and $BA$ and relate the result to the definition of the inverse.

> **Why this exercise:** starts from the definition of the inverse through multiplication before any formulas or computational methods are introduced.

#### Solution

1. **Definition:**
   A square matrix $B$ is the inverse of $A$ if and only if $AB = BA = I$, where $I$ is the identity matrix.

2. **Compute $AB$:**
   $$AB = \begin{pmatrix}2&1\\1&1\end{pmatrix}\begin{pmatrix}1&-1\\-1&2\end{pmatrix} = \begin{pmatrix}2(1)+1(-1) & 2(-1)+1(2) \\ 1(1)+1(-1) & 1(-1)+1(2)\end{pmatrix} = \begin{pmatrix}2-1 & -2+2 \\ 1-1 & -1+2\end{pmatrix} = \begin{pmatrix}1&0\\0&1\end{pmatrix} = I.$$

3. **Compute $BA$:**
   $$BA = \begin{pmatrix}1&-1\\-1&2\end{pmatrix}\begin{pmatrix}2&1\\1&1\end{pmatrix} = \begin{pmatrix}1(2)+(-1)(1) & 1(1)+(-1)(1) \\ -1(2)+2(1) & -1(1)+2(1)\end{pmatrix} = \begin{pmatrix}2-1 & 1-1 \\ -2+2 & -1+2\end{pmatrix} = \begin{pmatrix}1&0\\0&1\end{pmatrix} = I.$$

4. **Conclusion:**
   Because both $AB = I$ and $BA = I$, $B$ satisfies the definition of the inverse matrix, so $B = A^{-1}$.

---

### Exercise 2. Formula for a 2×2 Matrix
Find the inverse of
$$A=\begin{pmatrix}3&2\\5&4\end{pmatrix}$$
using the formula for a $2\times2$ matrix. At the end, check the result by computing one product with $A$.

> **Why this exercise:** teaches the simplest explicit formula for an inverse and requires verification using the definition.

#### Solution

1. **Formula:**
   For $M = \begin{pmatrix}a&b\\c&d\end{pmatrix}$ with $\det M = ad - bc \neq 0$:
   $$M^{-1} = \frac{1}{\det M} \begin{pmatrix}d & -b \\ -c & a\end{pmatrix}.$$

2. **Determinant of $A$:**
   $$\det A = 3(4) - 2(5) = 12 - 10 = 2 \neq 0.$$

3. **Compute $A^{-1}$:**
   $$A^{-1} = \frac{1}{2} \begin{pmatrix}4 & -2 \\ -5 & 3\end{pmatrix} = \begin{pmatrix}2 & -1 \\ -\frac{5}{2} & \frac{3}{2}\end{pmatrix}.$$

4. **Verification via $AA^{-1}$:**
   $$A A^{-1} = \begin{pmatrix}3&2\\5&4\end{pmatrix} \begin{pmatrix}2&-1\\-\frac{5}{2}&\frac{3}{2}\end{pmatrix} = \begin{pmatrix}3(2) + 2\left(-\frac{5}{2}\right) & 3(-1) + 2\left(\frac{3}{2}\right) \\ 5(2) + 4\left(-\frac{5}{2}\right) & 5(-1) + 4\left(\frac{3}{2}\right)\end{pmatrix} = \begin{pmatrix}6 - 5 & -3 + 3 \\ 10 - 10 & -5 + 6\end{pmatrix} = \begin{pmatrix}1&0\\0&1\end{pmatrix} = I.$$
   The inverse is verified.

---

### Exercise 3. When Does the Inverse Not Exist?
For
$$A=\begin{pmatrix}2&4\\1&2\end{pmatrix}$$
explain in two ways why $A^{-1}$ does not exist: using the determinant and using dependence between the rows.

> **Why this exercise:** connects two signs of noninvertibility instead of treating them as unrelated facts.

#### Solution

1. **Method 1: Using the Determinant:**
   $$\det A = 2(2) - 4(1) = 4 - 4 = 0.$$
   By the Invertible Matrix Theorem, a matrix has an inverse if and only if $\det A \neq 0$. If an inverse $A^{-1}$ existed, then $\det(A)\det(A^{-1}) = \det(I) = 1$, which is impossible when $\det A = 0$ ($0 \cdot \det(A^{-1}) = 0 \neq 1$). Thus $A^{-1}$ does not exist.

2. **Method 2: Using Row Dependence:**
   Let $R_1 = (2, 4)$ and $R_2 = (1, 2)$. Clearly:
   $$R_1 = 2 R_2.$$
   Row 1 is linearly dependent on Row 2. This implies $\operatorname{rank}(A) = 1 < 2$.
   Because the rank is less than 2, the kernel is non-trivial: $A \begin{pmatrix}-2\\1\end{pmatrix} = \begin{pmatrix}2(-2)+4(1)\\1(-2)+2(1)\end{pmatrix} = \begin{pmatrix}0\\0\end{pmatrix}$.
   Since a non-zero vector maps to the zero vector, the transformation is not injective (information is collapsed), so no inverse mapping can exist.

---

### Exercise 4. Gauss–Jordan
Find $A^{-1}$ using the Gauss–Jordan method for
$$A=\begin{pmatrix}1&2\\3&5\end{pmatrix}.$$
Show the augmented matrix $[A\mid I]$ after successive operations and explain why obtaining $I$ on the left gives the inverse on the right.

> **Why this exercise:** introduces the Gauss–Jordan method together with its meaning, not merely as a sequence of operations.

#### Solution

1. **Augmented Matrix:**
   $$[A \mid I] = \left[\begin{array}{cc|cc} 1 & 2 & 1 & 0 \\ 3 & 5 & 0 & 1 \end{array}\right].$$

2. **Row Operations:**
   - Eliminate entry below pivot $a_{11}$: $R_2 \leftarrow R_2 - 3R_1$:
     $$\left[\begin{array}{cc|cc} 1 & 2 & 1 & 0 \\ 0 & -1 & -3 & 1 \end{array}\right].$$
   - Make pivot in row 2 equal to $1$: $R_2 \leftarrow -R_2$:
     $$\left[\begin{array}{cc|cc} 1 & 2 & 1 & 0 \\ 0 & 1 & 3 & -1 \end{array}\right].$$
   - Eliminate entry above pivot $a_{22}$: $R_1 \leftarrow R_1 - 2R_2$:
     $$\left[\begin{array}{cc|cc} 1 & 0 & 1 - 2(3) & 0 - 2(-1) \\ 0 & 1 & 3 & -1 \end{array}\right] = \left[\begin{array}{cc|cc} 1 & 0 & -5 & 2 \\ 0 & 1 & 3 & -1 \end{array}\right].$$

3. **Result:**
   $$A^{-1} = \begin{pmatrix}-5 & 2 \\ 3 & -1\end{pmatrix}.$$

4. **Why this works:**
   Each elementary row operation is equivalent to multiplying the matrix on the left by an elementary matrix $E_k$.
   The sequence of operations transforms $[A \mid I]$ to $[(E_k \cdots E_1)A \mid (E_k \cdots E_1)I]$.
   Since the left block becomes $I$, we have $(E_k \cdots E_1)A = I$, which means $(E_k \cdots E_1) = A^{-1}$.
   Applying this exact sequence of operations to $I$ yields $(E_k \cdots E_1)I = A^{-1}$ on the right side.

---

### Exercise 5. A 3×3 Matrix
Use Gauss–Jordan elimination to find the inverse of
$$A=\begin{pmatrix}1&1&0\\0&1&1\\1&0&1\end{pmatrix}.$$
Check the result by multiplication.

> **Why this exercise:** provides necessary practice with the full method in a situation where the $2\times2$ formula no longer applies.

#### Solution

1. **Set up the Augmented Matrix:**
   $$[A \mid I] = \left[\begin{array}{ccc|ccc} 1&1&0 & 1&0&0 \\ 0&1&1 & 0&1&0 \\ 1&0&1 & 0&0&1 \end{array}\right].$$

2. **Forward Elimination:**
   - $R_3 \leftarrow R_3 - R_1$:
     $$\left[\begin{array}{ccc|ccc} 1&1&0 & 1&0&0 \\ 0&1&1 & 0&1&0 \\ 0&-1&1 & -1&0&1 \end{array}\right].$$
   - $R_3 \leftarrow R_3 + R_2$:
     $$\left[\begin{array}{ccc|ccc} 1&1&0 & 1&0&0 \\ 0&1&1 & 0&1&0 \\ 0&0&2 & -1&1&1 \end{array}\right].$$

3. **Scale Pivot and Back Substitution:**
   - $R_3 \leftarrow \frac{1}{2} R_3$:
     $$\left[\begin{array}{ccc|ccc} 1&1&0 & 1&0&0 \\ 0&1&1 & 0&1&0 \\ 0&0&1 & -\frac{1}{2}&\frac{1}{2}&\frac{1}{2} \end{array}\right].$$
   - $R_2 \leftarrow R_2 - R_3$:
     $$\left[\begin{array}{ccc|ccc} 1&1&0 & 1&0&0 \\ 0&1&0 & \frac{1}{2}&\frac{1}{2}&-\frac{1}{2} \\ 0&0&1 & -\frac{1}{2}&\frac{1}{2}&\frac{1}{2} \end{array}\right].$$
   - $R_1 \leftarrow R_1 - R_2$:
     $$\left[\begin{array}{ccc|ccc} 1&0&0 & \frac{1}{2}&-\frac{1}{2}&\frac{1}{2} \\ 0&1&0 & \frac{1}{2}&\frac{1}{2}&-\frac{1}{2} \\ 0&0&1 & -\frac{1}{2}&\frac{1}{2}&\frac{1}{2} \end{array}\right].$$

4. **Result:**
   $$A^{-1} = \frac{1}{2} \begin{pmatrix}1 & -1 & 1 \\ 1 & 1 & -1 \\ -1 & 1 & 1\end{pmatrix}.$$

5. **Verification via $AA^{-1}$:**
   $$AA^{-1} = \begin{pmatrix}1&1&0\\0&1&1\\1&0&1\end{pmatrix} \cdot \frac{1}{2}\begin{pmatrix}1&-1&1\\1&1&-1\\-1&1&1\end{pmatrix} = \frac{1}{2}\begin{pmatrix}1+1+0 & -1+1+0 & 1-1+0 \\ 0+1-1 & 0+1+1 & 0-1+1 \\ 1+0-1 & -1+0+1 & 1+0+1\end{pmatrix} = \frac{1}{2}\begin{pmatrix}2&0&0\\0&2&0\\0&0&2\end{pmatrix} = I.$$

---

### Exercise 6. Solving a System Using the Inverse
Solve
$$Ax=b,$$
where
$$A=\begin{pmatrix}2&1\\1&3\end{pmatrix},\qquad b=\begin{pmatrix}5\\7\end{pmatrix},$$
using $x=A^{-1}b$. Then substitute the resulting vector back into the equation and check the result.

> **Why this exercise:** shows the connection between inverse matrices and solving a linear system.

#### Solution

1. **Find $A^{-1}$:**
   $$\det A = 2(3) - 1(1) = 6 - 1 = 5 \neq 0.$$
   $$A^{-1} = \frac{1}{5} \begin{pmatrix}3 & -1 \\ -1 & 2\end{pmatrix}.$$

2. **Compute $x = A^{-1} b$:**
   $$x = \frac{1}{5}\begin{pmatrix}3 & -1 \\ -1 & 2\end{pmatrix}\begin{pmatrix}5 \\ 7\end{pmatrix} = \frac{1}{5}\begin{pmatrix}3(5) + (-1)(7) \\ -1(5) + 2(7)\end{pmatrix} = \frac{1}{5}\begin{pmatrix}15 - 7 \\ -5 + 14\end{pmatrix} = \frac{1}{5}\begin{pmatrix}8 \\ 9\end{pmatrix} = \begin{pmatrix}1.6 \\ 1.8\end{pmatrix}.$$

3. **Verification by Back Substitution ($Ax = b$):**
   $$Ax = \begin{pmatrix}2&1\\1&3\end{pmatrix}\begin{pmatrix}1.6\\1.8\end{pmatrix} = \begin{pmatrix}2(1.6) + 1(1.8) \\ 1(1.6) + 3(1.8)\end{pmatrix} = \begin{pmatrix}3.2 + 1.8 \\ 1.6 + 5.4\end{pmatrix} = \begin{pmatrix}5 \\ 7\end{pmatrix} = b.$$
   The solution is confirmed.

---

### Exercise 7. Inverse of a Product
For
$$A=\begin{pmatrix}1&1\\0&1\end{pmatrix},\qquad B=\begin{pmatrix}2&0\\0&3\end{pmatrix}$$
compute $(AB)^{-1}$ and $B^{-1}A^{-1}$. Check that the results are the same and explain the meaning of the reversed order.

> **Why this exercise:** reinforces the inverse-of-a-product property and requires its interpretation.

#### Solution

1. **Compute $(AB)^{-1}$:**
   $$AB = \begin{pmatrix}1&1\\0&1\end{pmatrix}\begin{pmatrix}2&0\\0&3\end{pmatrix} = \begin{pmatrix}2 & 3 \\ 0 & 3\end{pmatrix}.$$
   $$\det(AB) = 2(3) - 3(0) = 6.$$
   $$(AB)^{-1} = \frac{1}{6}\begin{pmatrix}3 & -3 \\ 0 & 2\end{pmatrix} = \begin{pmatrix}\frac{1}{2} & -\frac{1}{2} \\ 0 & \frac{1}{3}\end{pmatrix}.$$

2. **Compute $B^{-1}A^{-1}$:**
   $$A^{-1} = \begin{pmatrix}1 & -1 \\ 0 & 1\end{pmatrix}, \qquad B^{-1} = \begin{pmatrix}\frac{1}{2} & 0 \\ 0 & \frac{1}{3}\end{pmatrix}.$$
   $$B^{-1}A^{-1} = \begin{pmatrix}\frac{1}{2} & 0 \\ 0 & \frac{1}{3}\end{pmatrix}\begin{pmatrix}1 & -1 \\ 0 & 1\end{pmatrix} = \begin{pmatrix}\frac{1}{2}(1) + 0 & \frac{1}{2}(-1) + 0 \\ 0 + \frac{1}{3}(0) & 0 + \frac{1}{3}(1)\end{pmatrix} = \begin{pmatrix}\frac{1}{2} & -\frac{1}{2} \\ 0 & \frac{1}{3}\end{pmatrix}.$$

3. **Comparison and Meaning of Reversed Order:**
   Both computations give the exact same matrix.
   The product $AB$ represents applying transformation $B$ first, then transformation $A$. To undo this composite operation, the last applied transformation ($A$) must be undone first using $A^{-1}$, and only then can $B$ be undone using $B^{-1}$. Algebraically:
   $$(B^{-1}A^{-1})(AB) = B^{-1}(A^{-1}A)B = B^{-1}IB = B^{-1}B = I.$$

---

### Exercise 8. Inverse of a Transformation
The matrix
$$S=\begin{pmatrix}2&0\\0&\frac12\end{pmatrix}$$
describes a scaling of the plane. Find $S^{-1}$ and explain geometrically what the inverse transformation does. Check the action of the pair $S,S^{-1}$ on one simple vector.

> **Why this exercise:** gives the inverse the interpretation of undoing a transformation.

#### Solution

1. **Find $S^{-1}$:**
   Since $S$ is diagonal, its inverse has the reciprocal diagonal entries:
   $$S^{-1} = \begin{pmatrix}\frac{1}{2} & 0 \\ 0 & 2\end{pmatrix}.$$

2. **Geometric Interpretation:**
   - $S$ scales the horizontal axis ($x$) by a factor of $2$ and compresses the vertical axis ($y$) by a factor of $\frac{1}{2}$.
   - The inverse $S^{-1}$ undoes this action completely: it compresses the horizontal axis by $\frac{1}{2}$ and stretches the vertical axis by a factor of $2$.

3. **Test on Vector $v = \begin{pmatrix}2\\4\end{pmatrix}$:**
   - Applying $S$:
     $$w = Sv = \begin{pmatrix}2&0\\0&\frac{1}{2}\end{pmatrix}\begin{pmatrix}2\\4\end{pmatrix} = \begin{pmatrix}4\\2\end{pmatrix}.$$
   - Applying $S^{-1}$:
     $$S^{-1}w = \begin{pmatrix}\frac{1}{2}&0\\0&2\end{pmatrix}\begin{pmatrix}4\\2\end{pmatrix} = \begin{pmatrix}2\\4\end{pmatrix} = v.$$
   The original vector is completely restored: $S^{-1}(Sv) = v$.

---

### Exercise 9. Matrix Equation
Given
$$A=\begin{pmatrix}1&2\\0&1\end{pmatrix},\qquad B=\begin{pmatrix}3&1\\2&4\end{pmatrix}.$$
Solve the equation $AX=B$ for $X$. Before calculating, decide on which side of the equation $A^{-1}$ must be used. Then check the result by computing $AX$.

> **Why this exercise:** teaches that order matters in matrix equations and must guide the solution.

#### Solution

1. **Deciding the Multiplication Side:**
   In $AX = B$, matrix $A$ appears on the left of $X$. Since matrix multiplication is noncommutative, we must multiply both sides on the **left** by $A^{-1}$:
   $$A^{-1}(AX) = A^{-1}B \implies (A^{-1}A)X = A^{-1}B \implies IX = A^{-1}B \implies X = A^{-1}B.$$

2. **Find $A^{-1}$:**
   $$\det A = 1(1) - 2(0) = 1 \implies A^{-1} = \begin{pmatrix}1 & -2 \\ 0 & 1\end{pmatrix}.$$

3. **Compute $X = A^{-1}B$:**
   $$X = \begin{pmatrix}1 & -2 \\ 0 & 1\end{pmatrix}\begin{pmatrix}3 & 1 \\ 2 & 4\end{pmatrix} = \begin{pmatrix}1(3) + (-2)(2) & 1(1) + (-2)(4) \\ 0(3) + 1(2) & 0(1) + 1(4)\end{pmatrix} = \begin{pmatrix}3 - 4 & 1 - 8 \\ 2 & 4\end{pmatrix} = \begin{pmatrix}-1 & -7 \\ 2 & 4\end{pmatrix}.$$

4. **Verification via $AX$:**
   $$AX = \begin{pmatrix}1&2\\0&1\end{pmatrix}\begin{pmatrix}-1&-7\\2&4\end{pmatrix} = \begin{pmatrix}1(-1)+2(2) & 1(-7)+2(4) \\ 0(-1)+1(2) & 0(-7)+1(4)\end{pmatrix} = \begin{pmatrix}-1+4 & -7+8 \\ 2 & 4\end{pmatrix} = \begin{pmatrix}3 & 1 \\ 2 & 4\end{pmatrix} = B.$$
   Verified.

---

### Exercise 10. Inverse of a Diagonal Matrix
Given
$$D=\begin{pmatrix}2&0&0\\0&-3&0\\0&0&5\end{pmatrix},\qquad E=\begin{pmatrix}2&0&0\\0&0&0\\0&0&5\end{pmatrix}.$$
Without using Gauss–Jordan elimination, decide which matrix is invertible. For the invertible matrix, give the inverse and check the result by multiplication.

> **Why this exercise:** teaches how to recognize invertibility and the inverse without using a full procedure when the matrix structure gives the answer immediately.

#### Solution

1. **Deciding Invertibility:**
   For a diagonal matrix, the determinant is the product of its diagonal entries:
   - $\det D = 2 \cdot (-3) \cdot 5 = -30 \neq 0 \implies$ **$D$ is invertible**.
   - $\det E = 2 \cdot 0 \cdot 5 = 0 \implies$ **$E$ is not invertible** (singular, row 2 is all zeros).

2. **Inverse of $D$:**
   The inverse of an invertible diagonal matrix has entries equal to the reciprocals of the diagonal elements:
   $$D^{-1} = \begin{pmatrix}\frac{1}{2} & 0 & 0 \\ 0 & -\frac{1}{3} & 0 \\ 0 & 0 & \frac{1}{5}\end{pmatrix}.$$

3. **Verification by Multiplication:**
   $$D D^{-1} = \begin{pmatrix}2&0&0\\0&-3&0\\0&0&5\end{pmatrix}\begin{pmatrix}\frac{1}{2}&0&0\\0&-\frac{1}{3}&0\\0&0&\frac{1}{5}\end{pmatrix} = \begin{pmatrix}2\cdot\frac{1}{2} & 0 & 0 \\ 0 & (-3)\cdot\left(-\frac{1}{3}\right) & 0 \\ 0 & 0 & 5\cdot\frac{1}{5}\end{pmatrix} = \begin{pmatrix}1&0&0\\0&1&0\\0&0&1\end{pmatrix} = I.$$

---

## More Challenging Exercises

### Exercise 11. Parameter and Invertibility
For
$$A(t)=\begin{pmatrix}1&t\\t&1\end{pmatrix}$$
find all $t$ for which the matrix is invertible, and then give a formula for $A(t)^{-1}$. Explain what happens to this formula at the excluded values.

> **Why this exercise:** combines a parameter, determinant, and an explicit inverse formula in one problem.

#### Solution

1. **Determinant and Invertibility Condition:**
   $$\det A(t) = 1(1) - t(t) = 1 - t^2.$$
   $A(t)$ is invertible if and only if $\det A(t) \neq 0$:
   $$1 - t^2 \neq 0 \iff t^2 \neq 1 \iff t \neq 1 \quad \text{and} \quad t \neq -1.$$

2. **Formula for $A(t)^{-1}$:**
   Using the $2\times 2$ inverse formula:
   $$A(t)^{-1} = \frac{1}{1 - t^2} \begin{pmatrix}1 & -t \\ -t & 1\end{pmatrix}.$$

3. **Behavior at Excluded Values:**
   - At $t = 1$: $A(1) = \begin{pmatrix}1&1\\1&1\end{pmatrix}$. The rows are identical ($R_1 = R_2$), meaning they are linearly dependent. In the formula, the denominator $1-t^2 = 1 - 1 = 0$, leading to division by zero.
   - At $t = -1$: $A(-1) = \begin{pmatrix}1&-1\\-1&1\end{pmatrix}$. Row 2 is $-1 \times$ Row 1 ($R_2 = -R_1$), so the rows are again dependent. In the formula, $1 - (-1)^2 = 0$, again causing division by zero.
   In both cases, the image of $\mathbb{R}^2$ collapses to a line, so the map is non-invertible.

---

### Exercise 12. Finding Inverses Without Starting from Scratch
It is known that
$$A^{-1}=\begin{pmatrix}2&-1\\-3&2\end{pmatrix}.$$
Without finding $A$, compute $(3A)^{-1}$, $(A^T)^{-1}$, and $(A^2)^{-1}$. Justify each result using the appropriate property.

> **Why this exercise:** teaches how to use inverse properties instead of carrying out unnecessary full calculations.

#### Solution

1. **Compute $(3A)^{-1}$:**
   *Property:* $(cA)^{-1} = \frac{1}{c} A^{-1}$ for any scalar $c \neq 0$.
   $$(3A)^{-1} = \frac{1}{3} A^{-1} = \frac{1}{3}\begin{pmatrix}2 & -1 \\ -3 & 2\end{pmatrix} = \begin{pmatrix}\frac{2}{3} & -\frac{1}{3} \\ -1 & \frac{2}{3}\end{pmatrix}.$$

2. **Compute $(A^T)^{-1}$:**
   *Property:* The inverse of the transpose is the transpose of the inverse: $(A^T)^{-1} = (A^{-1})^T$.
   $$(A^T)^{-1} = \begin{pmatrix}2 & -1 \\ -3 & 2\end{pmatrix}^T = \begin{pmatrix}2 & -3 \\ -1 & 2\end{pmatrix}.$$

3. **Compute $(A^2)^{-1}$:**
   *Property:* $(A^2)^{-1} = (A \cdot A)^{-1} = A^{-1} A^{-1} = (A^{-1})^2$.
   $$(A^2)^{-1} = \begin{pmatrix}2&-1\\-3&2\end{pmatrix}\begin{pmatrix}2&-1\\-3&2\end{pmatrix} = \begin{pmatrix}2(2)+(-1)(-3) & 2(-1)+(-1)(2) \\ -3(2)+2(-3) & -3(-1)+2(2)\end{pmatrix} = \begin{pmatrix}4+3 & -2-2 \\ -6-6 & 3+4\end{pmatrix} = \begin{pmatrix}7 & -4 \\ -12 & 7\end{pmatrix}.$$

---

### Exercise 13. Undoing a Composite Transformation
The matrices
$$S=\begin{pmatrix}2&0\\0&1\end{pmatrix},\qquad H=\begin{pmatrix}1&1\\0&1\end{pmatrix}$$
describe nonuniform scaling and shear. For $T=HS$, find $T^{-1}$ in two ways:

1. first compute $T$, then its inverse,
2. use $(HS)^{-1}=S^{-1}H^{-1}$.

Compare the results. Additionally compute $H^{-1}S^{-1}$ and verify that the incorrect order gives a different matrix. Explain the rule: “when undoing a composition of operations, we undo them from the end.”

> **Why this exercise:** reinforces the inverse of a product in a less direct configuration.

#### Solution

1. **Method 1: Compute $T$ then $T^{-1}$:**
   $$T = HS = \begin{pmatrix}1&1\\0&1\end{pmatrix}\begin{pmatrix}2&0\\0&1\end{pmatrix} = \begin{pmatrix}2 & 1 \\ 0 & 1\end{pmatrix}.$$
   $$\det T = 2(1) - 1(0) = 2.$$
   $$T^{-1} = \frac{1}{2}\begin{pmatrix}1 & -1 \\ 0 & 2\end{pmatrix} = \begin{pmatrix}\frac{1}{2} & -\frac{1}{2} \\ 0 & 1\end{pmatrix}.$$

2. **Method 2: Use $(HS)^{-1} = S^{-1}H^{-1}$:**
   $$S^{-1} = \begin{pmatrix}\frac{1}{2} & 0 \\ 0 & 1\end{pmatrix}, \qquad H^{-1} = \begin{pmatrix}1 & -1 \\ 0 & 1\end{pmatrix}.$$
   $$S^{-1}H^{-1} = \begin{pmatrix}\frac{1}{2} & 0 \\ 0 & 1\end{pmatrix}\begin{pmatrix}1 & -1 \\ 0 & 1\end{pmatrix} = \begin{pmatrix}\frac{1}{2} & -\frac{1}{2} \\ 0 & 1\end{pmatrix}.$$
   Both methods produce the exact same matrix.

3. **Compute Incorrect Order $H^{-1}S^{-1}$:**
   $$H^{-1}S^{-1} = \begin{pmatrix}1 & -1 \\ 0 & 1\end{pmatrix}\begin{pmatrix}\frac{1}{2} & 0 \\ 0 & 1\end{pmatrix} = \begin{pmatrix}\frac{1}{2} & -1 \\ 0 & 1\end{pmatrix} \neq T^{-1}.$$

4. **Explanation of the Rule:**
   When transforming an object via $T = HS$, $S$ acts first and $H$ acts second: $y = H(Sx)$. To recover the initial state $x$, one must first undo the last layer applied ($H$) using $H^{-1}$, which leaves $Sx$. Only then can $S$ be undone by applying $S^{-1}$. Applying inverses in the wrong order attempts to undo the earlier transformation before the later one has been removed, distorting the coordinates incorrectly.

---

### Exercise 14. A Matrix That Is Its Own Inverse
Assume that a square matrix $A$ satisfies
$$A^2=I.$$
Show that
$$A^{-1}=A.$$
Then give an example of a $2\times2$ matrix different from $I$ and $-I$ that satisfies this condition, and verify it by multiplication.

> **Why this exercise:** requires using the definition of the inverse in a short argument and constructing an example independently, without introducing a new topic.

#### Solution

1. **Proof:**
   By assumption, $A^2 = A \cdot A = I$.
   By the definition of the inverse matrix, if a matrix $B$ satisfies $A B = I$ and $B A = I$, then $B = A^{-1}$.
   Taking $B = A$, we have:
   $$A \cdot A = I.$$
   Therefore, by definition, $A^{-1} = A$. (Such a matrix is called *involutory*).

2. **Example Different from $\pm I$:**
   Consider the reflection matrix across the line $y = x$:
   $$A = \begin{pmatrix}0 & 1 \\ 1 & 0\end{pmatrix}.$$
   Notice $A \neq I$ and $A \neq -I$.

3. **Verification by Multiplication:**
   $$A^2 = \begin{pmatrix}0 & 1 \\ 1 & 0\end{pmatrix}\begin{pmatrix}0 & 1 \\ 1 & 0\end{pmatrix} = \begin{pmatrix}0(0) + 1(1) & 0(1) + 1(0) \\ 1(0) + 0(1) & 1(1) + 0(0)\end{pmatrix} = \begin{pmatrix}1 & 0 \\ 0 & 1\end{pmatrix} = I.$$
   Hence $A^{-1} = A$.

---

### Exercise 15. Two Methods for Solving the Same System
For
$$A=\begin{pmatrix}2&1\\1&3\end{pmatrix},\qquad b=\begin{pmatrix}7\\8\end{pmatrix}$$
solve $Ax=b$ in two ways:
1. using $A^{-1}b$,
2. using Gaussian elimination.

Compare both solutions, the number of essential steps, and state which method was simpler in this example.

> **Why this exercise:** compares two known methods and prepares the student to choose a solution method consciously.

#### Solution

1. **Method 1: Using $A^{-1}b$:**
   - $\det A = 2(3) - 1(1) = 5$.
   - $A^{-1} = \frac{1}{5}\begin{pmatrix}3 & -1 \\ -1 & 2\end{pmatrix}$.
   - $x = A^{-1}b = \frac{1}{5}\begin{pmatrix}3 & -1 \\ -1 & 2\end{pmatrix}\begin{pmatrix}7 \\ 8\end{pmatrix} = \frac{1}{5}\begin{pmatrix}3(7)-1(8) \\ -1(7)+2(8)\end{pmatrix} = \frac{1}{5}\begin{pmatrix}13 \\ 9\end{pmatrix} = \begin{pmatrix}2.6 \\ 1.8\end{pmatrix}$.

2. **Method 2: Using Gaussian Elimination:**
   - Augmented matrix:
     $$\left[\begin{array}{cc|c} 2 & 1 & 7 \\ 1 & 3 & 8 \end{array}\right].$$
   - Swap $R_1 \leftrightarrow R_2$:
     $$\left[\begin{array}{cc|c} 1 & 3 & 8 \\ 2 & 1 & 7 \end{array}\right].$$
   - Eliminate below pivot: $R_2 \leftarrow R_2 - 2R_1$:
     $$\left[\begin{array}{cc|c} 1 & 3 & 8 \\ 0 & -5 & -9 \end{array}\right].$$
   - Back-substitution:
     $$-5y = -9 \implies y = \frac{9}{5} = 1.8.$$
     $$x + 3y = 8 \implies x = 8 - 3(1.8) = 8 - 5.4 = 2.6 = \frac{13}{5}.$$
     $$x = \begin{pmatrix}2.6 \\ 1.8\end{pmatrix}.$$

3. **Comparison:**
   - Both methods produce identical results: $x = 2.6, y = 1.8$.
   - **Simplicity:** Gaussian elimination was simpler here because it directly solved the specific system in just two row operations and back-substitution. Finding $A^{-1}$ required computing the determinant, finding all four matrix entries, and then performing an additional matrix-vector product.
   - Finding $A^{-1}$ is only preferred when one needs to solve $Ax = b$ for many different vectors $b$.
