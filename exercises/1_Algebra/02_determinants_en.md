# Determinants

## Goal of the Set

After completing this set, the student should be able to compute determinants of small matrices, understand their connection with invertibility, know how row operations affect the determinant, and recognize situations in which the determinant gives quick information about a matrix or a system of equations.

## Basic Exercises

### Exercise 1. Determinant of a 2×2 Matrix
Compute
$$\det\begin{pmatrix}3&-2\\5&4\end{pmatrix},\qquad \det\begin{pmatrix}1&7\\2&14\end{pmatrix}.$$
Which matrix is invertible? Justify your answer.

> **Why this exercise:** introduces the simplest determinant calculation and immediately connects it with invertibility.

#### Solution

1. **Calculations:**
   $$\det\begin{pmatrix}3&-2\\5&4\end{pmatrix} = 3\cdot 4 - (-2)\cdot 5 = 12 - (-10) = 12 + 10 = 22.$$
   $$\det\begin{pmatrix}1&7\\2&14\end{pmatrix} = 1\cdot 14 - 7\cdot 2 = 14 - 14 = 0.$$

2. **Invertibility:**
   - A square matrix $M$ is invertible if and only if $\det M \neq 0$.
   - $\begin{pmatrix}3&-2\\5&4\end{pmatrix}$ is **invertible** because its determinant is $22 \neq 0$.
   - $\begin{pmatrix}1&7\\2&14\end{pmatrix}$ is **not invertible** (singular) because its determinant is $0$.

**Verification:**
For the second matrix, Row 2 is exactly twice Row 1: $(2, 14) = 2(1, 7)$. Linear dependence between rows confirms the determinant must be 0 and the matrix is non-invertible.

---

### Exercise 2. Determinant of a 3×3 Matrix
For
$$A=\begin{pmatrix}1&2&-1\\0&3&4\\2&1&5\end{pmatrix}$$
compute $\det A$ using Sarrus' rule. Then perform one simple check using a chosen property of the determinant.

> **Why this exercise:** teaches a basic method for $3\times3$ matrices and builds the habit of checking the result without adding a second full solution.

#### Solution

1. **Sarrus' Rule:**
   Write the three columns, repeating the first two:
   $$\begin{matrix} 1 & 2 & -1 & 1 & 2 \\ 0 & 3 & 4 & 0 & 3 \\ 2 & 1 & 5 & 2 & 1 \end{matrix}$$
   - Sum of products along main diagonals:
     $$(1\cdot 3\cdot 5) + (2\cdot 4\cdot 2) + ((-1)\cdot 0\cdot 1) = 15 + 16 + 0 = 31.$$
   - Sum of products along anti-diagonals:
     $$(2\cdot 3\cdot (-1)) + (1\cdot 4\cdot 1) + (5\cdot 0\cdot 2) = -6 + 4 + 0 = -2.$$
   - Determinant:
     $$\det A = 31 - (-2) = 31 + 2 = 33.$$

2. **Check via Cofactor Expansion along Column 1:**
   Expanding along the first column (which contains an entry 0):
   $$\det A = 1\cdot \det\begin{pmatrix}3&4\\1&5\end{pmatrix} - 0\cdot \det\begin{pmatrix}2&-1\\1&5\end{pmatrix} + 2\cdot \det\begin{pmatrix}2&-1\\3&4\end{pmatrix}$$
   $$= 1(15 - 4) - 0 + 2(8 - (-3)) = 11 + 2(11) = 11 + 22 = 33.$$
   Both methods yield $33$, verifying the calculation.

---

### Exercise 3. Swapping Two Rows
For
$$A=\begin{pmatrix}1&2&0\\0&3&1\\2&1&1\end{pmatrix}$$
compute $\det A$. Then form a matrix $B$ by swapping the first and second rows of $A$.

First predict $\det B$ using a determinant property, and then verify your prediction by calculation.

> **Why this exercise:** gives a second classical calculation with a $3\times3$ determinant while teaching the precise effect of a row swap on the sign of the determinant.

#### Solution

1. **Compute $\det A$:**
   Expanding along row 1:
   $$\det A = 1\cdot \det\begin{pmatrix}3&1\\1&1\end{pmatrix} - 2\cdot \det\begin{pmatrix}0&1\\2&1\end{pmatrix} + 0$$
   $$= 1(3-1) - 2(0-2) = 1(2) - 2(-2) = 2 + 4 = 6.$$

2. **Form Matrix $B$ and Predict $\det B$:**
   Swapping rows 1 and 2:
   $$B = \begin{pmatrix}0&3&1\\1&2&0\\2&1&1\end{pmatrix}.$$
   *Prediction:* Swapping two rows of a matrix negates its determinant. Therefore, $\det B = -\det A = -6$.

3. **Verify Prediction by Direct Calculation:**
   Expanding along row 1 of $B$:
   $$\det B = 0 - 3\cdot \det\begin{pmatrix}1&0\\2&1\end{pmatrix} + 1\cdot \det\begin{pmatrix}1&2\\2&1\end{pmatrix}$$
   $$= -3(1 - 0) + 1(1 - 4) = -3(1) + 1(-3) = -3 - 3 = -6.$$
   The prediction $\det B = -6$ is confirmed.

---

### Exercise 4. Triangular Matrix
Without expanding the determinant, compute
$$\det\begin{pmatrix}2&4&1\\0&-3&5\\0&0&7\end{pmatrix}.$$
State the rule for an arbitrary triangular matrix and explain it using this example.

> **Why this exercise:** reinforces an important property of triangular matrices.

#### Solution

1. **Calculation:**
   $$\det\begin{pmatrix}2&4&1\\0&-3&5\\0&0&7\end{pmatrix} = 2 \cdot (-3) \cdot 7 = -42.$$

2. **Rule for Triangular Matrices:**
   For any upper triangular, lower triangular, or diagonal matrix $T = (t_{ij})_{n\times n}$, the determinant is the product of its main diagonal entries:
   $$\det T = \prod_{i=1}^n t_{ii} = t_{11} t_{22} \cdots t_{nn}.$$

3. **Explanation:**
   Performing cofactor expansion along the first column of an upper triangular matrix:
   $$\det T = t_{11} \cdot \det\begin{pmatrix}-3&5\\0&7\end{pmatrix} - 0 + 0.$$
   The remaining $2\times 2$ submatrix is also upper triangular, so expanding along its first column yields $(-3) \cdot 7$. Thus, all off-diagonal products in the permutation expansion contain at least one zero factor, leaving only the product along the main diagonal.

---

### Exercise 5. Row Operations
For
$$A=\begin{pmatrix}1&2&3\\2&1&0\\-1&4&2\end{pmatrix}$$
find $\det A$ by simplifying the matrix with row operations. At each step, indicate whether and how the determinant changes.

> **Why this exercise:** connects determinants with row operations and requires conscious tracking of every step.

#### Solution

1. **Step 1: Eliminate below $a_{11}$:**
   - $R_2 \leftarrow R_2 - 2R_1$: Adding a multiple of one row to another **leaves the determinant unchanged** ($\det A_1 = \det A$).
     Row 2: $(2 - 2, 1 - 4, 0 - 6) = (0, -3, -6)$.
   - $R_3 \leftarrow R_3 + R_1$: **Determinant unchanged** ($\det A_2 = \det A_1$).
     Row 3: $(-1 + 1, 4 + 2, 2 + 3) = (0, 6, 5)$.
   $$A_2 = \begin{pmatrix}1&2&3\\0&-3&-6\\0&6&5\end{pmatrix}.$$

2. **Step 2: Eliminate below $a_{22}$:**
   - $R_3 \leftarrow R_3 + 2R_2$: **Determinant unchanged**.
     Row 3: $(0 + 0, 6 + 2(-3), 5 + 2(-6)) = (0, 0, -7)$.
   $$A_3 = \begin{pmatrix}1&2&3\\0&-3&-6\\0&0&-7\end{pmatrix}.$$

3. **Compute Determinant of the Upper Triangular Matrix:**
   Since no row swaps or row scalings were used, the determinant is unchanged throughout:
   $$\det A = \det A_3 = 1 \cdot (-3) \cdot (-7) = 21.$$

**Verification:**
Via Sarrus' Rule: $(1\cdot 1\cdot 2 + 2\cdot 0\cdot (-1) + 3\cdot 2\cdot 4) - (3\cdot 1\cdot (-1) + 1\cdot 0\cdot 4 + 2\cdot 2\cdot 2) = (2 + 0 + 24) - (-3 + 0 + 8) = 26 - 5 = 21$. Confirmed.

---

### Exercise 6. Parameter and Invertibility
For
$$A(t)=\begin{pmatrix}t&1\\2&t\end{pmatrix}$$
find all values of $t$ for which the matrix is not invertible. Explain how your answer is related to the determinant being zero.

> **Why this exercise:** shows how the determinant can be used to study a family of matrices depending on a parameter.

#### Solution

1. **Compute Determinant:**
   $$\det A(t) = t\cdot t - 1\cdot 2 = t^2 - 2.$$

2. **Condition for Non-Invertibility:**
   A matrix $A(t)$ is not invertible if and only if $\det A(t) = 0$.
   $$t^2 - 2 = 0 \iff t^2 = 2 \iff t = \sqrt{2} \quad \text{or} \quad t = -\sqrt{2}.$$

3. **Connection to Determinant Being Zero:**
   When $\det A(t) = 0$, the rows (and columns) of $A(t)$ are linearly dependent.
   - For $t = \sqrt{2}$: $R_1 = (\sqrt{2}, 1)$ and $R_2 = (2, \sqrt{2}) = \sqrt{2}(\sqrt{2}, 1) = \sqrt{2}R_1$.
   The linear map represented by $A(t)$ compresses $\mathbb{R}^2$ onto a 1-dimensional line, giving a non-trivial kernel ($\ker A(t) \neq \{0\}$). Hence, the transformation has no inverse.

---

### Exercise 7. Using Properties Instead of Recomputing
Suppose that for a $3\times3$ matrix, $\det A=-4$. Compute
$$\det(2A),\qquad \det(A^T),\qquad \det(A^2),\qquad \det(-A).$$
Justify each answer using the appropriate property.

> **Why this exercise:** teaches how to use determinant properties instead of repeating a full calculation.

#### Solution

1. **$\det(2A)$:**
   *Property:* For an $n\times n$ matrix, multiplying the matrix by scalar $c$ multiplies every row by $c$, so $\det(cA) = c^n \det A$.
   Here $n=3$, so:
   $$\det(2A) = 2^3 \det A = 8 \cdot (-4) = -32.$$

2. **$\det(A^T)$:**
   *Property:* Transposition does not alter the determinant: $\det(A^T) = \det A$.
   $$\det(A^T) = -4.$$

3. **$\det(A^2)$:**
   *Property:* Determinant of a product equals the product of determinants: $\det(XY) = \det(X)\det(Y)$.
   $$\det(A^2) = \det(A \cdot A) = (\det A)^2 = (-4)^2 = 16.$$

4. **$\det(-A)$:**
   *Property:* This is scalar multiplication by $c = -1$ for an $n=3$ matrix: $\det(-A) = (-1)^3 \det A$.
   $$\det(-A) = (-1) \cdot (-4) = 4.$$

---

### Exercise 8. Determinant of a Product
Let $A,B$ be square matrices such that $\det A=3$ and $\det B=-5$. Compute $\det(AB)$, $\det(BA)$ and, if it exists, $\det(A^{-1}B)$. Explain why the first two results are equal even though usually $AB\neq BA$.

> **Why this exercise:** organizes how determinants behave with respect to products and inverses.

#### Solution

1. **Computations:**
   - $\det(AB) = \det A \cdot \det B = 3 \cdot (-5) = -15$.
   - $\det(BA) = \det B \cdot \det A = (-5) \cdot 3 = -15$.
   - Since $\det A = 3 \neq 0$, $A$ is invertible, and $\det(A^{-1}) = \frac{1}{\det A} = \frac{1}{3}$.
     $$\det(A^{-1}B) = \det(A^{-1}) \cdot \det B = \frac{1}{3} \cdot (-5) = -\frac{5}{3}.$$

2. **Explanation of $\det(AB) = \det(BA)$:**
   While matrix multiplication is generally noncommutative ($AB \neq BA$), the determinant maps matrices to real numbers: $\det(AB) = \det A \cdot \det B$ and $\det(BA) = \det B \cdot \det A$.
   Multiplication of real numbers is commutative ($\det A \cdot \det B = \det B \cdot \det A$), so the determinants are always equal.

---

### Exercise 9. Area and the Determinant
The vectors
$$u=\begin{pmatrix}3\\1\end{pmatrix},\qquad v=\begin{pmatrix}1\\4\end{pmatrix}$$
span a parallelogram. Compute its area using a determinant. Then reverse the order of the vectors and explain what changes in the determinant and what does not change in the area.

> **Why this exercise:** gives the determinant a geometric interpretation and distinguishes its sign from the value of the area.

#### Solution

1. **Area Computation:**
   Form the matrix with columns $u$ and $v$:
   $$\det \begin{pmatrix}3&1\\1&4\end{pmatrix} = 3(4) - 1(1) = 12 - 1 = 11.$$
   $$\text{Area} = |\det(u, v)| = |11| = 11.$$

2. **Reversing the Order:**
   $$\det \begin{pmatrix}1&3\\4&1\end{pmatrix} = 1(1) - 3(4) = 1 - 12 = -11.$$
   $$\text{Area} = |-11| = 11.$$

3. **Comparison:**
   - **What changes:** The sign of the determinant reverses from $+11$ to $-11$. The determinant computes *signed area*: a positive sign indicates a counterclockwise orientation from the first vector to the second, while a negative sign indicates a clockwise orientation.
   - **What does not change:** The geometric area remains $11$, because geometric area is the absolute magnitude $|\det|$, which is unaffected by orientation.

---

### Exercise 10. Detecting Dependence
Without carrying out a full determinant calculation, explain why
$$\det\begin{pmatrix}1&2&3\\2&4&6\\0&1&5\end{pmatrix}=0.$$
Identify a specific dependence between the rows and connect it with noninvertibility of the matrix.

> **Why this exercise:** teaches how to recognize a zero determinant from the structure of a matrix.

#### Solution

1. **Identifying Dependence:**
   Look at row 1 ($R_1 = (1, 2, 3)$) and row 2 ($R_2 = (2, 4, 6)$):
   $$R_2 = 2 R_1.$$
   Row 2 is an exact scalar multiple of Row 1.

2. **Connection to Determinant:**
   Performing the row operation $R_2 \leftarrow R_2 - 2R_1$ (which does not alter the determinant) produces a row of zeros:
   $$\begin{pmatrix}1&2&3\\0&0&0\\0&1&5\end{pmatrix}.$$
   Expanding along this zero row immediately yields $\det = 0$.

3. **Connection to Noninvertibility:**
   Because the rows are linearly dependent, the matrix has rank at most 2, which is less than full rank ($3$). By the Invertible Matrix Theorem, an $n\times n$ matrix is invertible if and only if its rank is $n$ (or equivalently, $\det \neq 0$). Thus, the matrix is singular and not invertible.

---

## More Challenging Exercises

### Exercise 11. Shortening the Calculation with Row Operations
Compute
$$\det\begin{pmatrix}1&2&3\\1&3&4\\1&4&6\end{pmatrix}$$
by first performing row operations that create as many zeros as possible. State which operations do not change the determinant.

> **Why this exercise:** develops planning instead of mechanically repeating the same procedure.

#### Solution

1. **Operations that do not change the determinant:**
   Replacing row $R_i$ with $R_i + c R_j$ ($i \neq j$) leaves the determinant unchanged.

2. **Step-by-step Elimination:**
   $$M = \begin{pmatrix}1&2&3\\1&3&4\\1&4&6\end{pmatrix}.$$
   - Subtract $R_1$ from $R_2$ ($R_2 \leftarrow R_2 - R_1$):
     Row 2 becomes $(1-1, 3-2, 4-3) = (0, 1, 1)$.
   - Subtract $R_1$ from $R_3$ ($R_3 \leftarrow R_3 - R_1$):
     Row 3 becomes $(1-1, 4-2, 6-3) = (0, 2, 3)$.
   $$M_1 = \begin{pmatrix}1&2&3\\0&1&1\\0&2&3\end{pmatrix}.$$
   - Subtract $2R_2$ from $R_3$ ($R_3 \leftarrow R_3 - 2R_2$):
     Row 3 becomes $(0, 2 - 2(1), 3 - 2(1)) = (0, 0, 1)$.
   $$M_2 = \begin{pmatrix}1&2&3\\0&1&1\\0&0&1\end{pmatrix}.$$

3. **Determinant:**
   $M_2$ is upper triangular. Since all row operations preserved the determinant:
   $$\det M = \det M_2 = 1 \cdot 1 \cdot 1 = 1.$$

---

### Exercise 12. A Parameter Revealed by a Row Operation
For
$$A(t)=\begin{pmatrix}1&2&3\\2&4&t\\0&1&1\end{pmatrix}$$
find the values of $t$ for which the matrix is not invertible.

Before computing the determinant, perform the operation
$$R_2\leftarrow R_2-2R_1$$
and use the resulting structure. At the end, explain what special thing happens to the rows for the value of the parameter you found.

> **Why this exercise:** combines a parameter, row operations, and recognition of dependence in one short argument.

#### Solution

1. **Perform $R_2 \leftarrow R_2 - 2R_1$:**
   Row 2 becomes:
   $$(2 - 2(1), 4 - 2(2), t - 2(3)) = (0, 0, t-6).$$
   The determinant is unchanged:
   $$A_1(t) = \begin{pmatrix}1&2&3\\0&0&t-6\\0&1&1\end{pmatrix}.$$

2. **Compute Determinant:**
   Expand along Row 2 (which has two zeros):
   $$\det A(t) = -(0) + 0 - (t-6)\cdot \det\begin{pmatrix}1&2\\0&1\end{pmatrix} = -(t-6)(1\cdot 1 - 2\cdot 0) = -(t-6) = 6-t.$$

3. **Find Non-Invertible Values:**
   The matrix is not invertible $\iff \det A(t) = 0 \iff 6 - t = 0 \iff t = 6$.

4. **Row Behavior at $t=6$:**
   When $t=6$, Row 2 of the original matrix is $(2, 4, 6) = 2(1, 2, 3) = 2R_1$. Row 2 is exactly twice Row 1. The rows are linearly dependent, producing the all-zero row $(0, 0, 0)$ after the row operation.

---

### Exercise 13. Determinant by Elimination
Compute the determinant
$$A=\begin{pmatrix}1&2&3\\2&5&7\\1&0&2\end{pmatrix}$$
using elimination. Record the effect of every row operation used on the value of the determinant.

> **Why this exercise:** reinforces organizing a determinant calculation through row operations without introducing an unnecessary second procedure.

#### Solution

1. **Elimination Steps and Determinant Tracking:**
   - **Step 1:** $R_2 \leftarrow R_2 - 2R_1$.
     *Effect:* Row addition does not change the determinant ($\times 1$).
     New Row 2: $(2-2, 5-4, 7-6) = (0, 1, 1)$.
   - **Step 2:** $R_3 \leftarrow R_3 - R_1$.
     *Effect:* Row addition does not change the determinant ($\times 1$).
     New Row 3: $(1-1, 0-2, 2-3) = (0, -2, -1)$.
     $$\text{Matrix: } \begin{pmatrix}1&2&3\\0&1&1\\0&-2&-1\end{pmatrix}.$$
   - **Step 3:** $R_3 \leftarrow R_3 + 2R_2$.
     *Effect:* Row addition does not change the determinant ($\times 1$).
     New Row 3: $(0, -2+2, -1+2(1)) = (0, 0, 1)$.
     $$\text{Upper triangular matrix: } U = \begin{pmatrix}1&2&3\\0&1&1\\0&0&1\end{pmatrix}.$$

2. **Compute Result:**
   $$\det A = \det U = 1 \cdot 1 \cdot 1 = 1.$$

**Verification:**
Cofactor expansion along column 1 of original matrix:
$$\det A = 1\cdot(10-0) - 2\cdot(4-0) + 1\cdot(14-15) = 10 - 8 - 1 = 1.$$
Confirmed.

---

### Exercise 14. A System of Equations and the Determinant
Consider the system $Ax=b$, where
$$A=\begin{pmatrix}1&2\\k&4\end{pmatrix}.$$
For which values of $k$ does the system have exactly one solution for every $b$? For the remaining value, give an example of a right-hand side $b$ for which the system has infinitely many solutions, and an example for which it has no solution.

> **Why this exercise:** connects the determinant with uniqueness of solutions and requires distinguishing the exceptional cases.

#### Solution

1. **Determinant and Uniqueness:**
   $$\det A = 1\cdot 4 - 2\cdot k = 4 - 2k.$$
   By Cramer's rule / Invertible Matrix Theorem, a square system $Ax=b$ has a unique solution for every $b$ if and only if $\det A \neq 0$:
   $$4 - 2k \neq 0 \iff k \neq 2.$$

2. **Exceptional Case $k = 2$:**
   When $k = 2$, $A = \begin{pmatrix}1&2\\2&4\end{pmatrix}$, and the equations are:
   $$\begin{cases} x + 2y = b_1, \\ 2x + 4y = b_2. \end{cases}$$
   Notice the left-hand side of equation 2 is exactly $2 \times$ the left-hand side of equation 1.

   - **Infinitely many solutions:** Choose $b_2 = 2b_1$, for example $b = \begin{pmatrix}3\\6\end{pmatrix}$.
     $$\begin{cases} x+2y=3, \\ 2x+4y=6 \iff x+2y=3. \end{cases}$$
     Both equations describe the same line, giving infinitely many solutions: $(x, y) = (3-2y, y)$ for $y \in \mathbb{R}$.
   - **No solution (inconsistent):** Choose $b_2 \neq 2b_1$, for example $b = \begin{pmatrix}3\\7\end{pmatrix}$.
     $$\begin{cases} x+2y=3, \\ 2x+4y=7 \implies 2(x+2y) = 2(3) = 6 \neq 7. \end{cases}$$
     This is a direct contradiction ($6 = 7$), so there is no solution.

---

### Exercise 15. Combining Determinant Properties
Let $A$ and $B$ be invertible $2\times2$ matrices with
$$\det A=-2,\qquad \det B=3.$$
Without finding the entries of the matrices, compute
$$\det\left(B^{-1}A^TB\right).$$
State the determinant properties you use in order and explain why the factors involving $B$ eventually cancel.

> **Why this exercise:** tests the transfer of several known properties into one short problem instead of checking a single property again with numbers.

#### Solution

1. **Sequence of Determinant Properties:**
   - **Property 1 (Multiplicativity):** $\det(XYZ) = \det(X) \det(Y) \det(Z)$.
     $$\det(B^{-1}A^TB) = \det(B^{-1}) \cdot \det(A^T) \cdot \det(B).$$
   - **Property 2 (Determinant of Inverse):** $\det(B^{-1}) = \frac{1}{\det B}$.
   - **Property 3 (Determinant of Transpose):** $\det(A^T) = \det(A)$.

2. **Calculation:**
   $$\det(B^{-1}A^TB) = \frac{1}{\det B} \cdot \det(A) \cdot \det(B) = \frac{1}{3} \cdot (-2) \cdot 3 = -2.$$

3. **Why the Factors Involving $B$ Cancel:**
   In the expression $\frac{1}{\det B} \cdot \det A \cdot \det B$, the determinants are scalar real numbers. In $\mathbb{R}$, multiplication is commutative and associative, so:
   $$\left(\frac{1}{\det B} \cdot \det B\right) \cdot \det A = 1 \cdot \det A = \det A.$$
   Geometrically, $B^{-1} A^T B$ represents a change of basis (similarity transformation) of $A^T$. Determinants measure the factor by which a transformation scales volume, which is an intrinsic geometric property independent of the choice of coordinate system.
