# Matrices and Basic Operations

## Goal of the Set

After completing this set, the student should understand what a matrix is, when basic operations can be performed, how matrix multiplication and matrix-vector multiplication work, and how matrices describe simple linear transformations.

The goal is not to perform many similar calculations. Each exercise presents a different aspect of working with matrices.

## How to Work Through the Exercises

For each exercise, prepare a solution containing at least:

- the result,
- the main steps,
- a brief explanation of the property or method used,
- a mathematical verification of the result, when possible.

---

## Basic Exercises

### Exercise 1. Matrix Size and Entries
Given
$$A=\begin{pmatrix}2&-1&3\\0&4&5\end{pmatrix},\qquad B=\begin{pmatrix}1&0\\-2&3\\4&1\end{pmatrix}.$$

1. State the sizes of matrices $A$ and $B$.
2. Read off the entries $a_{12}$, $a_{23}$, $b_{21}$, and $b_{32}$.
3. Write the second row of $A$ and the first column of $B$ as vectors.

> **Why this exercise:** builds basic fluency with matrix notation, indices, rows, and columns.

#### Solution

1. **Matrix Sizes:**
   - Matrix $A$ has $2$ rows and $3$ columns, so its size is $2 \times 3$.
   - Matrix $B$ has $3$ rows and $2$ columns, so its size is $3 \times 2$.

2. **Matrix Entries ($m_{ij}$ denotes the entry in row $i$, column $j$):**
   - $a_{12} = -1$ (row 1, column 2 of $A$)
   - $a_{23} = 5$ (row 2, column 3 of $A$)
   - $b_{21} = -2$ (row 2, column 1 of $B$)
   - $b_{32} = 1$ (row 3, column 2 of $B$)

3. **Rows and Columns as Vectors:**
   - Second row of $A$: $r_2 = \begin{pmatrix}0 & 4 & 5\end{pmatrix} \in \mathbb{R}^{1\times 3}$ (or as a row vector $(0, 4, 5)$).
   - First column of $B$: $c_1 = \begin{pmatrix}1 \\ -2 \\ 4\end{pmatrix} \in \mathbb{R}^{3\times 1}$.

**Verification:**
Checking dimensions: row 2 of $A$ has 3 elements matching the 3 columns of $A$. Column 1 of $B$ has 3 elements matching the 3 rows of $B$. Indices correspond directly to the matrix definition.

---

### Exercise 2. Addition and Scalar Multiplication
For
$$A=\begin{pmatrix}1&2\\-1&3\end{pmatrix},\qquad B=\begin{pmatrix}4&-2\\0&5\end{pmatrix}$$
compute
$$A+B,\qquad A-B,\qquad 3A-2B.$$
Explain why matrix addition is possible only for matrices of the same size.

> **Why this exercise:** reinforces entry-by-entry operations and the importance of compatible dimensions.

#### Solution

1. **Computation of $A+B$:**
   $$A+B = \begin{pmatrix}1+4 & 2+(-2) \\ -1+0 & 3+5\end{pmatrix} = \begin{pmatrix}5 & 0 \\ -1 & 8\end{pmatrix}.$$

2. **Computation of $A-B$:**
   $$A-B = \begin{pmatrix}1-4 & 2-(-2) \\ -1-0 & 3-5\end{pmatrix} = \begin{pmatrix}-3 & 4 \\ -1 & -2\end{pmatrix}.$$

3. **Computation of $3A-2B$:**
   $$3A = 3\begin{pmatrix}1&2\\-1&3\end{pmatrix} = \begin{pmatrix}3&6\\-3&9\end{pmatrix}, \qquad 2B = 2\begin{pmatrix}4&-2\\0&5\end{pmatrix} = \begin{pmatrix}8&-4\\0&10\end{pmatrix}.$$
   $$3A - 2B = \begin{pmatrix}3-8 & 6-(-4) \\ -3-0 & 9-10\end{pmatrix} = \begin{pmatrix}-5 & 10 \\ -3 & -1\end{pmatrix}.$$

4. **Why matrix addition requires the same size:**
   Matrix addition is defined element-wise: $(A+B)_{ij} = a_{ij} + b_{ij}$. If two matrices have different dimensions, there exist entries in one matrix that have no corresponding counterpart in the other, leaving the sum undefined.

**Verification:**
$(A+B) - A = \begin{pmatrix}5-1 & 0-2 \\ -1-(-1) & 8-3\end{pmatrix} = \begin{pmatrix}4 & -2 \\ 0 & 5\end{pmatrix} = B$, which confirms consistency.

---

### Exercise 3. When Can Matrices Be Multiplied?
The matrix sizes are
$$A_{2\times3},\qquad B_{3\times4},\qquad C_{4\times2},\qquad D_{2\times2}.$$
For the products
$$AB,\ BA,\ BC,\ CB,\ AC,\ CA,\ AD,\ DA$$
determine whether they are defined. If so, state the size of the result. Justify each decision using the dimension compatibility condition.

> **Why this exercise:** forces an understanding of dimension compatibility before carrying out any calculation.

#### Solution

**Dimension Compatibility Rule:** The matrix product $X_{m\times k} Y_{p\times n}$ is defined if and only if the number of columns of $X$ equals the number of rows of $Y$ ($k = p$). The resulting matrix has size $m\times n$.

- **$AB$:** $A_{2\times 3}$ and $B_{3\times 4}$. Columns of $A$ ($3$) $=$ Rows of $B$ ($3$). **Defined**, result size is $2\times 4$.
- **$BA$:** $B_{3\times 4}$ and $A_{2\times 3}$. Columns of $B$ ($4$) $\neq$ Rows of $A$ ($2$). **Undefined**.
- **$BC$:** $B_{3\times 4}$ and $C_{4\times 2}$. Columns of $B$ ($4$) $=$ Rows of $C$ ($4$). **Defined**, result size is $3\times 2$.
- **$CB$:** $C_{4\times 2}$ and $B_{3\times 4}$. Columns of $C$ ($2$) $\neq$ Rows of $B$ ($3$). **Undefined**.
- **$AC$:** $A_{2\times 3}$ and $C_{4\times 2}$. Columns of $A$ ($3$) $\neq$ Rows of $C$ ($4$). **Undefined**.
- **$CA$:** $C_{4\times 2}$ and $A_{2\times 3}$. Columns of $C$ ($2$) $=$ Rows of $A$ ($2$). **Defined**, result size is $4\times 3$.
- **$AD$:** $A_{2\times 3}$ and $D_{2\times 2}$. Columns of $A$ ($3$) $\neq$ Rows of $D$ ($2$). **Undefined**.
- **$DA$:** $D_{2\times 2}$ and $A_{2\times 3}$. Columns of $D$ ($2$) $=$ Rows of $A$ ($2$). **Defined**, result size is $2\times 3$.

---

### Exercise 4. Matrix Multiplication and Noncommutativity
For
$$A=\begin{pmatrix}1&2\\0&1\end{pmatrix},\qquad B=\begin{pmatrix}2&0\\3&1\end{pmatrix}$$
compute $AB$ and $BA$. Is $AB=BA$? Use this example to explain what noncommutativity of matrix multiplication means.

> **Why this exercise:** shows one of the most important differences between matrix multiplication and multiplication of numbers.

#### Solution

1. **Computation of $AB$:**
   $$AB = \begin{pmatrix}1&2\\0&1\end{pmatrix}\begin{pmatrix}2&0\\3&1\end{pmatrix} = \begin{pmatrix}1(2)+2(3) & 1(0)+2(1) \\ 0(2)+1(3) & 0(0)+1(1)\end{pmatrix} = \begin{pmatrix}2+6 & 0+2 \\ 0+3 & 0+1\end{pmatrix} = \begin{pmatrix}8 & 2 \\ 3 & 1\end{pmatrix}.$$

2. **Computation of $BA$:**
   $$BA = \begin{pmatrix}2&0\\3&1\end{pmatrix}\begin{pmatrix}1&2\\0&1\end{pmatrix} = \begin{pmatrix}2(1)+0(0) & 2(2)+0(1) \\ 3(1)+1(0) & 3(2)+1(1)\end{pmatrix} = \begin{pmatrix}2+0 & 4+0 \\ 3+0 & 6+1\end{pmatrix} = \begin{pmatrix}2 & 4 \\ 3 & 7\end{pmatrix}.$$

3. **Comparison and Noncommutativity:**
   $AB = \begin{pmatrix}8&2\\3&1\end{pmatrix} \neq BA = \begin{pmatrix}2&4\\3&7\end{pmatrix}$.
   Therefore, $AB \neq BA$. Noncommutativity means that the order of operations in matrix multiplication matters; changing the order of the factors generally yields an entirely different matrix (or may even make multiplication impossible due to mismatched dimensions).

**Verification:**
Determinants: $\det(A) = 1(1)-2(0) = 1$, $\det(B) = 2(1)-0(3) = 2$.
$\det(AB) = 8(1)-2(3) = 2 = \det(A)\det(B)$.
$\det(BA) = 2(7)-4(3) = 2 = \det(B)\det(A)$.
Both determinants match $\det(A)\det(B)=2$, verifying algebraic correctness.

---

### Exercise 5. Matrix Times Vector
Let
$$A=\begin{pmatrix}2&-1\\1&3\end{pmatrix},\qquad x=\begin{pmatrix}4\\2\end{pmatrix}.$$
Compute $Ax$. Then express $Ax$ as a linear combination of the columns of $A$, with coefficients coming from the vector $x$.

> **Why this exercise:** shows that multiplying a matrix by a vector can be understood as a linear combination of the matrix columns.

#### Solution

1. **Direct Computation (row-by-column):**
   $$Ax = \begin{pmatrix}2&-1\\1&3\end{pmatrix}\begin{pmatrix}4\\2\end{pmatrix} = \begin{pmatrix}2(4) + (-1)(2) \\ 1(4) + 3(2)\end{pmatrix} = \begin{pmatrix}8 - 2 \\ 4 + 6\end{pmatrix} = \begin{pmatrix}6 \\ 10\end{pmatrix}.$$

2. **Linear Combination of Columns:**
   Let the columns of $A$ be $a_1 = \begin{pmatrix}2\\1\end{pmatrix}$ and $a_2 = \begin{pmatrix}-1\\3\end{pmatrix}$.
   $$x_1 a_1 + x_2 a_2 = 4\begin{pmatrix}2\\1\end{pmatrix} + 2\begin{pmatrix}-1\\3\end{pmatrix} = \begin{pmatrix}8\\4\end{pmatrix} + \begin{pmatrix}-2\\6\end{pmatrix} = \begin{pmatrix}8 - 2 \\ 4 + 6\end{pmatrix} = \begin{pmatrix}6 \\ 10\end{pmatrix}.$$

**Verification:**
Both methods yield identical results $\begin{pmatrix}6\\10\end{pmatrix}$, confirming that matrix-vector multiplication $Ax$ fundamentally represents a linear combination of the columns of $A$ weighted by the components of $x$.

---

### Exercise 6. Transpose
For
$$A=\begin{pmatrix}1&2&3\\4&5&6\end{pmatrix},\qquad B=\begin{pmatrix}1&0\\2&1\\-1&3\end{pmatrix}$$
compute $A^T$, $B^T$, and $AB$. Then verify in this example that
$$(AB)^T=B^TA^T.$$

> **Why this exercise:** teaches transposition and an important property that reverses the order of factors.

#### Solution

1. **Transposes:**
   $$A^T = \begin{pmatrix}1&4\\2&5\\3&6\end{pmatrix}_{3\times 2}, \qquad B^T = \begin{pmatrix}1&2&-1\\0&1&3\end{pmatrix}_{2\times 3}.$$

2. **Product $AB$:**
   $$AB = \begin{pmatrix}1&2&3\\4&5&6\end{pmatrix}\begin{pmatrix}1&0\\2&1\\-1&3\end{pmatrix} = \begin{pmatrix}1(1)+2(2)+3(-1) & 1(0)+2(1)+3(3) \\ 4(1)+5(2)+6(-1) & 4(0)+5(1)+6(3)\end{pmatrix} = \begin{pmatrix}1+4-3 & 0+2+9 \\ 4+10-6 & 0+5+18\end{pmatrix} = \begin{pmatrix}2 & 11 \\ 8 & 23\end{pmatrix}.$$

3. **Transpose $(AB)^T$:**
   $$(AB)^T = \begin{pmatrix}2 & 8 \\ 11 & 23\end{pmatrix}.$$

4. **Product $B^T A^T$:**
   $$B^T A^T = \begin{pmatrix}1&2&-1\\0&1&3\end{pmatrix}\begin{pmatrix}1&4\\2&5\\3&6\end{pmatrix} = \begin{pmatrix}1(1)+2(2)-1(3) & 1(4)+2(5)-1(6) \\ 0(1)+1(2)+3(3) & 0(4)+1(5)+3(6)\end{pmatrix} = \begin{pmatrix}2 & 8 \\ 11 & 23\end{pmatrix}.$$

**Verification:**
$(AB)^T = \begin{pmatrix}2&8\\11&23\end{pmatrix} = B^T A^T$. The property $(AB)^T = B^T A^T$ holds.

---

### Exercise 7. Identity Matrix, Zero Matrix, and Powers
For
$$A=\begin{pmatrix}2&1\\0&2\end{pmatrix}$$
compute
$$AI,\qquad IA,\qquad A+0,\qquad A^2,\qquad A^3.$$
Explain the roles of the matrices $I$ and $0$, and describe the pattern you observe in successive powers of $A$.

> **Why this exercise:** organizes the roles of neutral elements and reveals regularity in successive powers of a matrix.

#### Solution

1. **Neutral Elements:**
   - Identity matrix $I = \begin{pmatrix}1&0\\0&1\end{pmatrix}$:
     $$AI = \begin{pmatrix}2&1\\0&2\end{pmatrix}\begin{pmatrix}1&0\\0&1\end{pmatrix} = \begin{pmatrix}2&1\\0&2\end{pmatrix} = A,$$
     $$IA = \begin{pmatrix}1&0\\0&1\end{pmatrix}\begin{pmatrix}2&1\\0&2\end{pmatrix} = \begin{pmatrix}2&1\\0&2\end{pmatrix} = A.$$
   - Zero matrix $0 = \begin{pmatrix}0&0\\0&0\end{pmatrix}$:
     $$A + 0 = \begin{pmatrix}2&1\\0&2\end{pmatrix} + \begin{pmatrix}0&0\\0&0\end{pmatrix} = \begin{pmatrix}2&1\\0&2\end{pmatrix} = A.$$
   - Roles: $I$ acts as the multiplicative neutral element ($AI = IA = A$), and $0$ acts as the additive neutral element ($A + 0 = A$).

2. **Powers $A^2$ and $A^3$:**
   $$A^2 = \begin{pmatrix}2&1\\0&2\end{pmatrix}\begin{pmatrix}2&1\\0&2\end{pmatrix} = \begin{pmatrix}4 & 2+2 \\ 0 & 4\end{pmatrix} = \begin{pmatrix}4 & 4 \\ 0 & 4\end{pmatrix}.$$
   $$A^3 = A^2 A = \begin{pmatrix}4&4\\0&4\end{pmatrix}\begin{pmatrix}2&1\\0&2\end{pmatrix} = \begin{pmatrix}8 & 4+8 \\ 0 & 8\end{pmatrix} = \begin{pmatrix}8 & 12 \\ 0 & 8\end{pmatrix}.$$

3. **Pattern in Successive Powers:**
   Notice $A = 2I + N$ where $N = \begin{pmatrix}0&1\\0&0\end{pmatrix}$ and $N^2 = 0$. Since $2I$ and $N$ commute, by the Binomial Theorem:
   $$A^n = (2I + N)^n = (2I)^n + n(2I)^{n-1}N = 2^n I + n 2^{n-1} N = \begin{pmatrix}2^n & n 2^{n-1} \\ 0 & 2^n\end{pmatrix}.$$
   Checking for $n=1: \begin{pmatrix}2&1\\0&2\end{pmatrix}$; $n=2: \begin{pmatrix}4&4\\0&4\end{pmatrix}$; $n=3: \begin{pmatrix}8&12\\0&8\end{pmatrix}$.

---

### Exercise 8. Row Operations and Their Reversibility
For
$$A=\begin{pmatrix}1&2&-1\\2&4&1\\-1&1&3\end{pmatrix}$$
perform, in order:
1. $R_2\leftarrow R_2-2R_1$,
2. $R_3\leftarrow R_3+R_1$,
3. interchange $R_2$ and $R_3$.

Write the matrix after each step. Then, for each of the three operations, state an operation that reverses it.

> **Why this exercise:** prepares for elimination by showing that row operations are controlled and reversible transformations of a matrix.

#### Solution

1. **Step 1: $R_2 \leftarrow R_2 - 2R_1$:**
   New Row 2: $\begin{pmatrix}2 - 2(1) & 4 - 2(2) & 1 - 2(-1)\end{pmatrix} = \begin{pmatrix}0 & 0 & 3\end{pmatrix}$.
   $$A_1 = \begin{pmatrix}1 & 2 & -1 \\ 0 & 0 & 3 \\ -1 & 1 & 3\end{pmatrix}.$$
   *Reverse operation:* $R_2 \leftarrow R_2 + 2R_1$.

2. **Step 2: $R_3 \leftarrow R_3 + R_1$:**
   New Row 3: $\begin{pmatrix}-1 + 1 & 1 + 2 & 3 + (-1)\end{pmatrix} = \begin{pmatrix}0 & 3 & 2\end{pmatrix}$.
   $$A_2 = \begin{pmatrix}1 & 2 & -1 \\ 0 & 0 & 3 \\ 0 & 3 & 2\end{pmatrix}.$$
   *Reverse operation:* $R_3 \leftarrow R_3 - R_1$.

3. **Step 3: Interchange $R_2 \leftrightarrow R_3$:**
   $$A_3 = \begin{pmatrix}1 & 2 & -1 \\ 0 & 3 & 2 \\ 0 & 0 & 3\end{pmatrix}.$$
   *Reverse operation:* Interchange $R_2 \leftrightarrow R_3$ (swapping two rows is its own inverse).

**Verification:**
Applying the reverse operations in reverse order to $A_3$:
- Swap $R_2 \leftrightarrow R_3 \implies \begin{pmatrix}1&2&-1\\0&0&3\\0&3&2\end{pmatrix} = A_2$.
- $R_3 \leftarrow R_3 - R_1 \implies \begin{pmatrix}1&2&-1\\0&0&3\\-1&1&3\end{pmatrix} = A_1$.
- $R_2 \leftarrow R_2 + 2R_1 \implies \begin{pmatrix}1&2&-1\\2&4&1\\-1&1&3\end{pmatrix} = A$.
The original matrix is fully restored.

---

### Exercise 9. Composing Transformations
Let
$$S=\begin{pmatrix}2&0\\0&1\end{pmatrix},\qquad R=\begin{pmatrix}0&-1\\1&0\end{pmatrix}.$$
The matrix $S$ describes nonuniform scaling, while $R$ describes a $90^\circ$ counterclockwise rotation.
For
$$x=\begin{pmatrix}1\\2\end{pmatrix}$$
compute $RSx$ and $SRx$. Compare the results and explain geometrically why the order of these transformations matters.

> **Why this exercise:** interprets matrix multiplication as composition of transformations.

#### Solution

1. **Computation of $RSx$ (Scale first, then Rotate):**
   $$Sx = \begin{pmatrix}2&0\\0&1\end{pmatrix}\begin{pmatrix}1\\2\end{pmatrix} = \begin{pmatrix}2\\2\end{pmatrix}.$$
   $$RSx = R(Sx) = \begin{pmatrix}0&-1\\1&0\end{pmatrix}\begin{pmatrix}2\\2\end{pmatrix} = \begin{pmatrix}-2\\2\end{pmatrix}.$$

2. **Computation of $SRx$ (Rotate first, then Scale):**
   $$Rx = \begin{pmatrix}0&-1\\1&0\end{pmatrix}\begin{pmatrix}1\\2\end{pmatrix} = \begin{pmatrix}-2\\1\end{pmatrix}.$$
   $$SRx = S(Rx) = \begin{pmatrix}2&0\\0&1\end{pmatrix}\begin{pmatrix}-2\\1\end{pmatrix} = \begin{pmatrix}-4\\1\end{pmatrix}.$$

3. **Geometric Explanation:**
   $RSx = \begin{pmatrix}-2\\2\end{pmatrix} \neq SRx = \begin{pmatrix}-4\\1\end{pmatrix}$.
   - In $RS$, the vector is first scaled horizontally by a factor of 2 (stretching the $x$-component $1 \to 2$), and then rotated $90^\circ$ counterclockwise, sending the stretched $x$-component to the positive $y$-axis.
   - In $SR$, the vector is rotated first, sending the original $y$-component ($2$) to the negative $x$-axis ($-2$). Then scaling by 2 doubles this new $x$-component from $-2$ to $-4$.
   Because scaling acts along the fixed coordinate axes, rotating before or after scaling completely alters which component receives the magnification.

---

### Exercise 10. Columns of a Matrix Product
Given
$$A=\begin{pmatrix}1&2&0\\0&1&1\end{pmatrix},\qquad B=\begin{pmatrix}1&2\\-1&0\\3&1\end{pmatrix}.$$
Denote the columns of $B$ by $b_1,b_2$.

1. Compute $Ab_1$ and $Ab_2$.
2. Compute the matrix $AB$.
3. Compare the results and explain why the columns of $AB$ are exactly the vectors $Ab_1$ and $Ab_2$.

> **Why this exercise:** extends the interpretation of matrix-vector multiplication to a full product of two matrices instead of simply repeating another $Ax$ exercise.

#### Solution

1. **Compute $Ab_1$ and $Ab_2$:**
   $$b_1 = \begin{pmatrix}1\\-1\\3\end{pmatrix}, \qquad b_2 = \begin{pmatrix}2\\0\\1\end{pmatrix}.$$
   $$Ab_1 = \begin{pmatrix}1&2&0\\0&1&1\end{pmatrix}\begin{pmatrix}1\\-1\\3\end{pmatrix} = \begin{pmatrix}1(1) + 2(-1) + 0(3) \\ 0(1) + 1(-1) + 1(3)\end{pmatrix} = \begin{pmatrix}1 - 2 + 0 \\ 0 - 1 + 3\end{pmatrix} = \begin{pmatrix}-1 \\ 2\end{pmatrix}.$$
   $$Ab_2 = \begin{pmatrix}1&2&0\\0&1&1\end{pmatrix}\begin{pmatrix}2\\0\\1\end{pmatrix} = \begin{pmatrix}1(2) + 2(0) + 0(1) \\ 0(2) + 1(0) + 1(1)\end{pmatrix} = \begin{pmatrix}2 + 0 + 0 \\ 0 + 0 + 1\end{pmatrix} = \begin{pmatrix}2 \\ 1\end{pmatrix}.$$

2. **Compute $AB$:**
   $$AB = \begin{pmatrix}1(1)+2(-1)+0(3) & 1(2)+2(0)+0(1) \\ 0(1)+1(-1)+1(3) & 0(2)+1(0)+1(1)\end{pmatrix} = \begin{pmatrix}-1 & 2 \\ 2 & 1\end{pmatrix}.$$

3. **Comparison and Explanation:**
   The columns of $AB$ are $\operatorname{col}_1(AB) = \begin{pmatrix}-1\\2\end{pmatrix} = Ab_1$ and $\operatorname{col}_2(AB) = \begin{pmatrix}2\\1\end{pmatrix} = Ab_2$.
   By the column-partition definition of matrix multiplication:
   $$A B = A \begin{pmatrix} b_1 & b_2 \end{pmatrix} = \begin{pmatrix} A b_1 & A b_2 \end{pmatrix}.$$
   Each column $j$ of the product $AB$ is the transformation of the $j$-th column of $B$ under matrix $A$.

---

## More Challenging Exercises

### Exercise 11. When Do Matrices Commute?
Given
$$A=\begin{pmatrix}1&1\\0&1\end{pmatrix},\qquad B=\begin{pmatrix}a&b\\c&d\end{pmatrix}.$$
Find the conditions on $a,b,c,d$ under which $AB=BA$. Describe the general form of all such matrices $B$.

> **Why this exercise:** deepens the idea of noncommutativity by finding the conditions under which commutativity does hold.

#### Solution

1. **Compute Both Products:**
   $$AB = \begin{pmatrix}1&1\\0&1\end{pmatrix}\begin{pmatrix}a&b\\c&d\end{pmatrix} = \begin{pmatrix}a+c & b+d \\ c & d\end{pmatrix}.$$
   $$BA = \begin{pmatrix}a&b\\c&d\end{pmatrix}\begin{pmatrix}1&1\\0&1\end{pmatrix} = \begin{pmatrix}a & a+b \\ c & c+d\end{pmatrix}.$$

2. **Equate Corresponding Entries ($AB = BA$):**
   - Entry $(1,1)$: $a + c = a \implies c = 0$.
   - Entry $(2,1)$: $c = c$ (identically true since $c=0$).
   - Entry $(2,2)$: $d = c + d \implies c = 0$ (consistent).
   - Entry $(1,2)$: $b + d = a + b \implies d = a$.

3. **Conclusion and General Form:**
   The matrices commute if and only if $c = 0$ and $d = a$. The parameter $b$ can be any real number.
   Thus, the general form of all matrices commuting with $A$ is:
   $$B = \begin{pmatrix}a & b \\ 0 & a\end{pmatrix} = a\begin{pmatrix}1&0\\0&1\end{pmatrix} + b\begin{pmatrix}0&1\\0&0\end{pmatrix} = a I + b(A - I), \quad \text{for any } a,b \in \mathbb{R}.$$

**Verification:**
$$AB = \begin{pmatrix}1&1\\0&1\end{pmatrix}\begin{pmatrix}a&b\\0&a\end{pmatrix} = \begin{pmatrix}a & a+b \\ 0 & a\end{pmatrix},$$
$$BA = \begin{pmatrix}a&b\\0&a\end{pmatrix}\begin{pmatrix}1&1\\0&1\end{pmatrix} = \begin{pmatrix}a & a+b \\ 0 & a\end{pmatrix}.$$
Both products are identical, confirming the conditions.

---

### Exercise 12. Formula for a Matrix Power
Let
$$A=\begin{pmatrix}1&1\\0&1\end{pmatrix}.$$
Compute $A^2$, $A^3$, and $A^4$, and use them to formulate a conjecture for $A^n$. Then do not stop after checking one more case: assume the formula is true for $n$, multiply by $A$, and explain why you obtain exactly the formula for $n+1$.

> **Why this exercise:** teaches how to recognize a pattern and formulate a generalization from several computations.

#### Solution

1. **Calculate Powers:**
   $$A^2 = \begin{pmatrix}1&1\\0&1\end{pmatrix}\begin{pmatrix}1&1\\0&1\end{pmatrix} = \begin{pmatrix}1 & 2 \\ 0 & 1\end{pmatrix}.$$
   $$A^3 = A^2 A = \begin{pmatrix}1&2\\0&1\end{pmatrix}\begin{pmatrix}1&1\\0&1\end{pmatrix} = \begin{pmatrix}1 & 3 \\ 0 & 1\end{pmatrix}.$$
   $$A^4 = A^3 A = \begin{pmatrix}1&3\\0&1\end{pmatrix}\begin{pmatrix}1&1\\0&1\end{pmatrix} = \begin{pmatrix}1 & 4 \\ 0 & 1\end{pmatrix}.$$

2. **Conjecture:**
   For all $n \in \mathbb{N}$,
   $$A^n = \begin{pmatrix}1 & n \\ 0 & 1\end{pmatrix}.$$

3. **Mathematical Induction Proof:**
   - **Base Case:** For $n=1$, $A^1 = \begin{pmatrix}1&1\\0&1\end{pmatrix}$, which matches the formula.
   - **Inductive Step:** Assume the statement holds for $n$, i.e., $A^n = \begin{pmatrix}1&n\\0&1\end{pmatrix}$.
     Then for $n+1$:
     $$A^{n+1} = A^n A = \begin{pmatrix}1&n\\0&1\end{pmatrix}\begin{pmatrix}1&1\\0&1\end{pmatrix} = \begin{pmatrix}1(1)+n(0) & 1(1)+n(1) \\ 0(1)+1(0) & 0(1)+1(1)\end{pmatrix} = \begin{pmatrix}1 & n+1 \\ 0 & 1\end{pmatrix}.$$
   The formula holds for $n+1$. By induction, $A^n = \begin{pmatrix}1&n\\0&1\end{pmatrix}$ for all $n \ge 1$.

---

### Exercise 13. A Recurrence Written in Matrix Form
Let
$$F=\begin{pmatrix}1&1\\1&0\end{pmatrix}.$$
Compute $F^2$, $F^3$, $F^4$, and $F^5$. Compare the numbers obtained with the sequence
$$0,1,1,2,3,5,8,\ldots$$
and describe the relationship you observe. Then compute
$$F\begin{pmatrix}a\\b\end{pmatrix}$$
and explain how this multiplication performs one recurrence step: it creates the sum of two consecutive terms and keeps one of them for the next step.

> **Why this exercise:** shows the connection between matrix powers and a simple numerical recurrence.

#### Solution

1. **Calculate Powers of $F$:**
   $$F^2 = \begin{pmatrix}1&1\\1&0\end{pmatrix}\begin{pmatrix}1&1\\1&0\end{pmatrix} = \begin{pmatrix}2&1\\1&1\end{pmatrix}.$$
   $$F^3 = F^2 F = \begin{pmatrix}2&1\\1&1\end{pmatrix}\begin{pmatrix}1&1\\1&0\end{pmatrix} = \begin{pmatrix}3&2\\2&1\end{pmatrix}.$$
   $$F^4 = F^3 F = \begin{pmatrix}3&2\\2&1\end{pmatrix}\begin{pmatrix}1&1\\1&0\end{pmatrix} = \begin{pmatrix}5&3\\3&2\end{pmatrix}.$$
   $$F^5 = F^4 F = \begin{pmatrix}5&3\\3&2\end{pmatrix}\begin{pmatrix}1&1\\1&0\end{pmatrix} = \begin{pmatrix}8&5\\5&3\end{pmatrix}.$$

2. **Relationship with Fibonacci Sequence:**
   Let $f_0=0, f_1=1, f_2=1, f_3=2, f_4=3, f_5=5, f_6=8, \ldots$ where $f_{n+1} = f_n + f_{n-1}$.
   Comparing entries of $F^n$:
   $$F^n = \begin{pmatrix}f_{n+1} & f_n \\ f_n & f_{n-1}\end{pmatrix}.$$
   For $n=1$: $\begin{pmatrix}f_2&f_1\\f_1&f_0\end{pmatrix} = \begin{pmatrix}1&1\\1&0\end{pmatrix}$.
   For $n=5$: $\begin{pmatrix}f_6&f_5\\f_5&f_4\end{pmatrix} = \begin{pmatrix}8&5\\5&3\end{pmatrix}$.

3. **Recurrence Step:**
   $$F\begin{pmatrix}a\\b\end{pmatrix} = \begin{pmatrix}1&1\\1&0\end{pmatrix}\begin{pmatrix}a\\b\end{pmatrix} = \begin{pmatrix}a+b\\a\end{pmatrix}.$$
   - If the input vector represents two consecutive terms of the sequence $\begin{pmatrix}f_k \\ f_{k-1}\end{pmatrix}$, multiplication by $F$ generates:
     $$\begin{pmatrix}f_k + f_{k-1} \\ f_k\end{pmatrix} = \begin{pmatrix}f_{k+1} \\ f_k\end{pmatrix}.$$
   The first row creates the new term by summing the previous two, while the second row preserves the current term $f_k$ to serve as the previous term in the subsequent step.

---

### Exercise 14. Rotation Matrices
The matrix for a rotation through an angle $\theta$ is
$$R(\theta)=\begin{pmatrix}\cos\theta&-\sin\theta\\\sin\theta&\cos\theta\end{pmatrix}.$$
Compute $R(\alpha)R(\beta)$ and, using the angle-sum formulas for sine and cosine, show that
$$R(\alpha)R(\beta)=R(\alpha+\beta).$$
Explain the result geometrically.

> **Why this exercise:** shows the consistency between matrix algebra and the geometry of composing rotations.

#### Solution

1. **Matrix Multiplication:**
   $$R(\alpha)R(\beta) = \begin{pmatrix}\cos\alpha & -\sin\alpha \\ \sin\alpha & \cos\alpha\end{pmatrix}\begin{pmatrix}\cos\beta & -\sin\beta \\ \sin\beta & \cos\beta\end{pmatrix}$$
   $$= \begin{pmatrix}\cos\alpha\cos\beta - \sin\alpha\sin\beta & -(\cos\alpha\sin\beta + \sin\alpha\cos\beta) \\ \sin\alpha\cos\beta + \cos\alpha\sin\beta & -\sin\alpha\sin\beta + \cos\alpha\cos\beta\end{pmatrix}.$$

2. **Angle-Sum Trigonometric Identities:**
   Recall:
   $$\cos(\alpha+\beta) = \cos\alpha\cos\beta - \sin\alpha\sin\beta,$$
   $$\sin(\alpha+\beta) = \sin\alpha\cos\beta + \cos\alpha\sin\beta.$$
   Substituting these identities into the product:
   $$R(\alpha)R(\beta) = \begin{pmatrix}\cos(\alpha+\beta) & -\sin(\alpha+\beta) \\ \sin(\alpha+\beta) & \cos(\alpha+\beta)\end{pmatrix} = R(\alpha+\beta).$$

3. **Geometric Explanation:**
   Multiplying a vector $v$ by $R(\beta)$ rotates it counterclockwise by an angle $\beta$ about the origin. Multiplying the result by $R(\alpha)$ rotates it further counterclockwise by an angle $\alpha$. The net effect is a single rotation about the origin through the combined angle $\alpha+\beta$, which is precisely represented by $R(\alpha+\beta)$.

---

### Exercise 15. Associativity of Multiplication and Different Calculation Paths
Given
$$A=\begin{pmatrix}1&2&0\\0&1&1\end{pmatrix},\quad B=\begin{pmatrix}1&0\\2&1\\-1&3\end{pmatrix},\quad C=\begin{pmatrix}2&1\\0&-1\end{pmatrix}.$$
Compute $(AB)C$ and $A(BC)$. Compare the results and the number of intermediate operations. Explain what associativity of matrix multiplication means in this example.

> **Why this exercise:** reinforces associativity by comparing two mathematically equivalent calculation paths.

#### Solution

1. **Path 1: $(AB)C$:**
   - First compute $AB$ ($2\times 3$ times $3\times 2 \to 2\times 2$):
     $$AB = \begin{pmatrix}1(1)+2(2)+0(-1) & 1(0)+2(1)+0(3) \\ 0(1)+1(2)+1(-1) & 0(0)+1(1)+1(3)\end{pmatrix} = \begin{pmatrix}1+4+0 & 0+2+0 \\ 0+2-1 & 0+1+3\end{pmatrix} = \begin{pmatrix}5 & 2 \\ 1 & 4\end{pmatrix}.$$
   - Then compute $(AB)C$ ($2\times 2$ times $2\times 2 \to 2\times 2$):
     $$(AB)C = \begin{pmatrix}5&2\\1&4\end{pmatrix}\begin{pmatrix}2&1\\0&-1\end{pmatrix} = \begin{pmatrix}5(2)+2(0) & 5(1)+2(-1) \\ 1(2)+4(0) & 1(1)+4(-1)\end{pmatrix} = \begin{pmatrix}10 & 3 \\ 2 & -3\end{pmatrix}.$$

2. **Path 2: $A(BC)$:**
   - First compute $BC$ ($3\times 2$ times $2\times 2 \to 3\times 2$):
     $$BC = \begin{pmatrix}1&0\\2&1\\-1&3\end{pmatrix}\begin{pmatrix}2&1\\0&-1\end{pmatrix} = \begin{pmatrix}1(2)+0(0) & 1(1)+0(-1) \\ 2(2)+1(0) & 2(1)+1(-1) \\ -1(2)+3(0) & -1(1)+3(-1)\end{pmatrix} = \begin{pmatrix}2 & 1 \\ 4 & 1 \\ -2 & -4\end{pmatrix}.$$
   - Then compute $A(BC)$ ($2\times 3$ times $3\times 2 \to 2\times 2$):
     $$A(BC) = \begin{pmatrix}1&2&0\\0&1&1\end{pmatrix}\begin{pmatrix}2&1\\4&1\\-2&-4\end{pmatrix} = \begin{pmatrix}1(2)+2(4)+0(-2) & 1(1)+2(1)+0(-4) \\ 0(2)+1(4)+1(-2) & 0(1)+1(1)+1(-4)\end{pmatrix} = \begin{pmatrix}10 & 3 \\ 2 & -3\end{pmatrix}.$$

3. **Comparison and Associativity:**
   - Both calculation paths yield the exact same matrix: $\begin{pmatrix}10 & 3 \\ 2 & -3\end{pmatrix}$.
   - Operation count:
     - In $(AB)C$: $AB$ takes $2 \times 2 \times 3 = 12$ multiplications; $(AB)C$ takes $2 \times 2 \times 2 = 8$ multiplications. Total: $20$ multiplications.
     - In $A(BC)$: $BC$ takes $3 \times 2 \times 2 = 12$ multiplications; $A(BC)$ takes $2 \times 2 \times 3 = 12$ multiplications. Total: $24$ multiplications.
   - Associativity guarantees that grouping $(AB)C = A(BC)$ produces the same geometric transformation and matrix result, but one calculation path may be computationally more efficient than the other.
