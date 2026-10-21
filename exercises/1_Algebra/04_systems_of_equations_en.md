# Systems of Linear Equations

## Goal of the Set

After completing this set, the student should be able to write a system in the form $Ax=b$, solve it using Gaussian elimination, and recognize the three basic cases: exactly one solution, infinitely many solutions, and no solution.

## Basic Exercises

### Exercise 1. From a System to a Matrix
Write the system
$$\begin{cases}2x-y+z=4,\\x+3y-2z=1,\\3x+y+z=7.\end{cases}$$
in the form $Ax=b$.
Identify the coefficient matrix, the vector of unknowns, and the right-hand side vector. Explain how each row of the matrix corresponds to one equation.

> **Why this exercise:** teaches how to move between a system of equations and matrix notation.

#### Solution

1. **Matrix Form $Ax = b$:**
   $$\begin{pmatrix}2 & -1 & 1 \\ 1 & 3 & -2 \\ 3 & 1 & 1\end{pmatrix}\begin{pmatrix}x \\ y \\ z\end{pmatrix} = \begin{pmatrix}4 \\ 1 \\ 7\end{pmatrix}.$$

2. **Components:**
   - **Coefficient matrix:** $A = \begin{pmatrix}2 & -1 & 1 \\ 1 & 3 & -2 \\ 3 & 1 & 1\end{pmatrix}$.
   - **Vector of unknowns:** $x = \begin{pmatrix}x \\ y \\ z\end{pmatrix}$.
   - **Right-hand side vector:** $b = \begin{pmatrix}4 \\ 1 \\ 7\end{pmatrix}$.

3. **Correspondence of Rows to Equations:**
   By definition of matrix-vector multiplication, the $i$-th entry of $Ax$ is the dot product of the $i$-th row of $A$ with the vector of unknowns:
   $$\operatorname{Row}_i(A) \cdot x = a_{i1}x + a_{i2}y + a_{i3}z = b_i.$$
   Thus, row 1 encodes $2x - y + z = 4$, row 2 encodes $x + 3y - 2z = 1$, and row 3 encodes $3x + y + z = 7$.

---

### Exercise 2. Gaussian Elimination — One Solution
Solve using Gaussian elimination:
$$\begin{cases}x+y+z=6,\\2x-y+z=3,\\x+2y-z=2.\end{cases}$$
After solving, substitute the result into all equations and check consistency.

> **Why this exercise:** introduces the basic method for solving a system and builds the habit of checking the result.

#### Solution

1. **Augmented Matrix:**
   $$\left[\begin{array}{ccc|c} 1 & 1 & 1 & 6 \\ 2 & -1 & 1 & 3 \\ 1 & 2 & -1 & 2 \end{array}\right].$$

2. **Forward Elimination:**
   - $R_2 \leftarrow R_2 - 2R_1$:
     Row 2 becomes $(2-2, -1-2, 1-2 \mid 3-12) = (0, -3, -1 \mid -9)$.
   - $R_3 \leftarrow R_3 - R_1$:
     Row 3 becomes $(1-1, 2-1, -1-1 \mid 2-6) = (0, 1, -2 \mid -4)$.
     $$\left[\begin{array}{ccc|c} 1 & 1 & 1 & 6 \\ 0 & -3 & -1 & -9 \\ 0 & 1 & -2 & -4 \end{array}\right].$$
   - Swap $R_2 \leftrightarrow R_3$:
     $$\left[\begin{array}{ccc|c} 1 & 1 & 1 & 6 \\ 0 & 1 & -2 & -4 \\ 0 & -3 & -1 & -9 \end{array}\right].$$
   - $R_3 \leftarrow R_3 + 3R_2$:
     Row 3 becomes $(0, -3+3, -1+3(-2) \mid -9+3(-4)) = (0, 0, -7 \mid -21)$.
     $$\left[\begin{array}{ccc|c} 1 & 1 & 1 & 6 \\ 0 & 1 & -2 & -4 \\ 0 & 0 & -7 & -21 \end{array}\right].$$

3. **Back-Substitution:**
   - From Row 3: $-7z = -21 \implies z = 3$.
   - From Row 2: $y - 2(3) = -4 \implies y - 6 = -4 \implies y = 2$.
   - From Row 1: $x + 2 + 3 = 6 \implies x + 5 = 6 \implies x = 1$.
   Unique solution: $(x, y, z) = (1, 2, 3)$.

4. **Consistency Verification:**
   - Equation 1: $1 + 2 + 3 = 6$ (holds).
   - Equation 2: $2(1) - 2 + 3 = 2 - 2 + 3 = 3$ (holds).
   - Equation 3: $1 + 2(2) - 3 = 1 + 4 - 3 = 2$ (holds).

---

### Exercise 3. Inconsistent System
Solve or show that the system is inconsistent:
$$\begin{cases}x+2y=3,\\2x+4y=7.\end{cases}$$
Show how the contradiction appears in the matrix after elimination and interpret it in terms of equations.

> **Why this exercise:** teaches how to recognize that a system has no solution without guessing.

#### Solution

1. **Augmented Matrix:**
   $$\left[\begin{array}{cc|c} 1 & 2 & 3 \\ 2 & 4 & 7 \end{array}\right].$$

2. **Elimination Step:**
   $R_2 \leftarrow R_2 - 2R_1$:
   Row 2 becomes $(2 - 2(1), 4 - 2(2) \mid 7 - 2(3)) = (0, 0 \mid 1)$.
   $$\left[\begin{array}{cc|c} 1 & 2 & 3 \\ 0 & 0 & 1 \end{array}\right].$$

3. **Contradiction and Geometric Interpretation:**
   - Row 2 translates to the algebraic equation:
     $$0\cdot x + 0\cdot y = 1 \iff 0 = 1.$$
     Since $0 = 1$ is never true for any real values of $x$ and $y$, the system has **no solution** (it is inconsistent).
   - Geometrically, both equations represent straight lines in $\mathbb{R}^2$ with identical slope ($-\frac{1}{2}$), but different $y$-intercepts:
     $$L_1: y = -\frac{1}{2}x + \frac{3}{2}, \qquad L_2: y = -\frac{1}{2}x + \frac{7}{4}.$$
     The lines are strictly parallel and never intersect.

---

### Exercise 4. Infinitely Many Solutions
Solve
$$\begin{cases}x+y+z=2,\\2x+2y+2z=4,\\x-y+z=0.\end{cases}$$
Give the solution in parametric form, identify a free variable, and for one chosen parameter value check that the resulting point really satisfies the system.

> **Why this exercise:** shows the case of multiple solutions and teaches a simple parametric description.

#### Solution

1. **Augmented Matrix and Elimination:**
   $$\left[\begin{array}{ccc|c} 1 & 1 & 1 & 2 \\ 2 & 2 & 2 & 4 \\ 1 & -1 & 1 & 0 \end{array}\right].$$
   - $R_2 \leftarrow R_2 - 2R_1 \implies (0, 0, 0 \mid 0)$.
   - $R_3 \leftarrow R_3 - R_1 \implies (0, -2, 0 \mid -2)$.
   Swap $R_2 \leftrightarrow R_3$:
   $$\left[\begin{array}{ccc|c} 1 & 1 & 1 & 2 \\ 0 & -2 & 0 & -2 \\ 0 & 0 & 0 & 0 \end{array}\right].$$

2. **Parametric Solution:**
   - From Row 2: $-2y = -2 \implies y = 1$.
   - The third column has no pivot, so $z$ is the **free variable**. Let $z = t \in \mathbb{R}$.
   - From Row 1: $x + 1 + t = 2 \implies x = 1 - t$.
   $$\begin{pmatrix}x \\ y \\ z\end{pmatrix} = \begin{pmatrix}1 - t \\ 1 \\ t\end{pmatrix} = \begin{pmatrix}1 \\ 1 \\ 0\end{pmatrix} + t\begin{pmatrix}-1 \\ 0 \\ 1\end{pmatrix}, \quad t \in \mathbb{R}.$$

3. **Check for Parameter Value $t = 2$:**
   Point: $(x, y, z) = (1-2, 1, 2) = (-1, 1, 2)$.
   - Eq 1: $-1 + 1 + 2 = 2$ (holds).
   - Eq 2: $2(-1) + 2(1) + 2(2) = -2 + 2 + 4 = 4$ (holds).
   - Eq 3: $-1 - 1 + 2 = 0$ (holds).

---

### Exercise 5. Row Echelon Form and Number of Solutions
For the augmented matrix
$$\left[\begin{array}{ccc|c}1&2&-1&3\\0&1&2&1\\0&0&0&0\end{array}\right]$$
determine the number of solutions and write them in parametric form. Explain how you know how many variables may be chosen freely.

> **Why this exercise:** teaches how to read information about solutions directly from row echelon form.

#### Solution

1. **Number of Free Variables:**
   - Number of unknowns: $n = 3$ ($x_1, x_2, x_3$).
   - Pivots: Row 1 pivot is in column 1 ($x_1$), Row 2 pivot is in column 2 ($x_2$).
   - Rank of coefficient matrix: $\operatorname{rank}(A) = 2$.
   - Since $\operatorname{rank}([A\mid b]) = \operatorname{rank}(A) = 2$ and there is no contradiction row, the system is consistent.
   - Number of free variables $= n - \operatorname{rank}(A) = 3 - 2 = 1$.
   Because there is 1 free variable, the system has **infinitely many solutions**.

2. **Parametric Form:**
   Let $x_3 = t \in \mathbb{R}$ (free variable).
   - Row 2: $x_2 + 2x_3 = 1 \implies x_2 = 1 - 2t$.
   - Row 1: $x_1 + 2x_2 - x_3 = 3 \implies x_1 + 2(1 - 2t) - t = 3 \implies x_1 + 2 - 5t = 3 \implies x_1 = 1 + 5t$.
   $$\begin{pmatrix}x_1 \\ x_2 \\ x_3\end{pmatrix} = \begin{pmatrix}1 + 5t \\ 1 - 2t \\ t\end{pmatrix} = \begin{pmatrix}1 \\ 1 \\ 0\end{pmatrix} + t\begin{pmatrix}5 \\ -2 \\ 1\end{pmatrix}, \quad t \in \mathbb{R}.$$

---

### Exercise 6. A System with a Parameter — Which Cases Actually Occur?
Analyze, depending on the parameter $a$, the system
$$\begin{cases}x+y=2,\\ax+ay=4.\end{cases}$$

Among the three possibilities — exactly one solution, infinitely many solutions, no solution — determine which actually occur and for which values of $a$. If one type cannot occur, explain why.

> **Why this exercise:** teaches how to analyze a parameter without assuming in advance that all theoretically possible cases must occur in a specific system.

#### Solution

1. **Augmented Matrix and Elimination:**
   $$\left[\begin{array}{cc|c} 1 & 1 & 2 \\ a & a & 4 \end{array}\right].$$
   $R_2 \leftarrow R_2 - aR_1$:
   $$\left[\begin{array}{cc|c} 1 & 1 & 2 \\ 0 & 0 & 4 - 2a \end{array}\right].$$

2. **Analysis of Cases:**
   - **Case 1: $a = 2$:**
     $4 - 2(2) = 0$. The second row becomes $[0\ 0 \mid 0]$.
     The system reduces to $x+y=2$. There are **infinitely many solutions**: $(x, y) = (2-t, t)$ for $t \in \mathbb{R}$.
   - **Case 2: $a \neq 2$:**
     $4 - 2a \neq 0$. The second row states $0\cdot x + 0\cdot y = 4 - 2a \neq 0$, which is impossible ($0 = \text{non-zero}$).
     There is **no solution** (inconsistent).

3. **Why "Exactly One Solution" Cannot Occur:**
   For a $2\times 2$ system to have a unique solution, the coefficient matrix must have rank 2, meaning its determinant must be non-zero:
   $$\det\begin{pmatrix}1&1\\a&a\end{pmatrix} = 1\cdot a - 1\cdot a = 0 \quad \text{for all } a \in \mathbb{R}.$$
   Since the determinant is identically zero for every value of $a$, the coefficient rows are always linearly dependent ($R_2 = a R_1$), making it impossible to obtain a unique solution.

---

### Exercise 7. Choosing a Method Deliberately
Do not solve all of the following systems completely. For each situation, choose the method that best uses its structure and justify your choice:

1. one system with a triangular coefficient matrix
   $$\begin{cases}2x-y=3,\\4y=8;\end{cases}$$
2. three systems $Ax=b_i$ with the same invertible matrix $A$, when $A^{-1}$ is already known;
3. one $3\times3$ system for which the inverse matrix is not given and the goal is only to find one solution vector.

For case 1, carry out the chosen method completely. For cases 2 and 3, describe the plan and indicate which part of the computation would be reusable or unnecessary. Do not judge a method by its name alone — refer to the number of right-hand sides and the structure of the matrix.

> **Why this exercise:** practices choosing a method based on the structure of the problem instead of solving another small system by two methods.

#### Solution

1. **Case 1: Triangular system:**
   - *Best Method:* **Direct Back-Substitution**.
   - *Justification:* The matrix is already in upper triangular form. Running elimination or computing inverses would add unnecessary work.
   - *Execution:*
     From equation 2: $4y = 8 \implies y = 2$.
     Substitute into equation 1: $2x - 2 = 3 \implies 2x = 5 \implies x = \frac{5}{2} = 2.5$.
     Result: $(x, y) = (2.5, 2)$.

2. **Case 2: Three systems with same $A$ and known $A^{-1}$:**
   - *Best Method:* **Matrix-Vector Multiplication** ($x_i = A^{-1}b_i$).
   - *Plan:* Compute $x_1 = A^{-1}b_1$, $x_2 = A^{-1}b_2$, $x_3 = A^{-1}b_3$.
   - *Reusable vs Unnecessary:* The precomputed $A^{-1}$ is reused directly for all three vectors. Running Gaussian elimination from scratch three times would redundantly repeat the exact same row transformations on $A$ three times.

3. **Case 3: Single $3\times 3$ system, $A^{-1}$ not given:**
   - *Best Method:* **Gaussian Elimination**.
   - *Plan:* Form $[A \mid b]$, apply row operations to reach upper triangular form, and back-substitute to find $x$.
   - *Unnecessary:* Computing $A^{-1}$ would require solving $[A \mid I]$ (which is equivalent to running elimination for three right-hand sides). For a single solution vector, computing the full matrix inverse requires roughly triple the operations of simple Gaussian elimination.

---

### Exercise 8. Two Systems with the Same Coefficient Matrix
Solve by elimination the two systems
$$\begin{cases}2x+y=5,\\x-y=1,\end{cases}$$
$$\begin{cases}2x+y=1,\\x-y=4.\end{cases}$$
Compare the successive elimination steps. Which part of the calculation is the same in both cases, and why?

> **Why this exercise:** shows the role of the coefficient matrix independently of the right-hand side.

#### Solution

1. **Joint Augmented Matrix:**
   Since both systems share $A = \begin{pmatrix}2&1\\1&-1\end{pmatrix}$, we can solve them simultaneously using $[A \mid b_1 \mid b_2]$:
   $$\left[\begin{array}{cc|cc} 2 & 1 & 5 & 1 \\ 1 & -1 & 1 & 4 \end{array}\right].$$

2. **Elimination Steps:**
   - Swap $R_1 \leftrightarrow R_2$:
     $$\left[\begin{array}{cc|cc} 1 & -1 & 1 & 4 \\ 2 & 1 & 5 & 1 \end{array}\right].$$
   - $R_2 \leftarrow R_2 - 2R_1$:
     Row 2 left: $(2-2, 1-2(-1)) = (0, 3)$.
     Row 2 right for $b_1$: $5 - 2(1) = 3$.
     Row 2 right for $b_2$: $1 - 2(4) = -7$.
     $$\left[\begin{array}{cc|cc} 1 & -1 & 1 & 4 \\ 0 & 3 & 3 & -7 \end{array}\right].$$

3. **Back-Substitution:**
   - **System 1:** $3y = 3 \implies y = 1$. Then $x - 1 = 1 \implies x = 2$.
     Solution 1: $(x, y) = (2, 1)$.
   - **System 2:** $3y = -7 \implies y = -\frac{7}{3}$. Then $x - (-\frac{7}{3}) = 4 \implies x = 4 - \frac{7}{3} = \frac{5}{3}$.
     Solution 2: $(x, y) = \left(\frac{5}{3}, -\frac{7}{3}\right)$.

4. **Comparison:**
   The row operations applied to the coefficient columns (swapping rows, subtracting $2R_1$) were **identical** in both systems. This is because the row operations needed to produce pivots and zeros are determined entirely by the entries of $A$, completely independent of the right-hand side vector $b$.

---

### Exercise 9. A System from a Sum Condition
Find numbers $x,y$ satisfying
$$x+y=10,\qquad 2x+5y=32.$$
Solve the system and explain geometrically why the solution is unique.

> **Why this exercise:** reinforces the transition from two linear conditions to the intersection point of two lines.

#### Solution

1. **Solve by Substitution / Elimination:**
   From equation 1: $x = 10 - y$.
   Substitute into equation 2:
   $$2(10 - y) + 5y = 32 \implies 20 - 2y + 5y = 32 \implies 3y = 12 \implies y = 4.$$
   Then $x = 10 - 4 = 6$.
   Solution: $(x, y) = (6, 4)$.

2. **Geometric Explanation of Uniqueness:**
   - Equation 1 ($x+y=10$) is a line with slope $m_1 = -1$ and $y$-intercept $10$.
   - Equation 2 ($2x+5y=32$) is a line with slope $m_2 = -\frac{2}{5} = -0.4$ and $y$-intercept $\frac{32}{5} = 6.4$.
   Since $m_1 \neq m_2$, the two lines have different directions and are not parallel. In the Euclidean plane, any two non-parallel lines intersect at exactly one unique point, which corresponds to the unique algebraic solution $(6, 4)$.

---

### Exercise 10. A Polynomial Through Three Points
Find a polynomial $p(x)=ax^2+bx+c$ whose graph passes through $(0,1)$, $(1,3)$, and $(2,9)$. Reduce the problem to a system of equations and check the result by substituting all three points.

> **Why this exercise:** shows that finding unknown coefficients can be reduced to solving a linear system.

#### Solution

1. **Set Up the System:**
   Substitute each point $(x, y)$ into $p(x) = ax^2 + bx + c$:
   - For $(0, 1)$: $a(0)^2 + b(0) + c = 1 \implies c = 1$.
   - For $(1, 3)$: $a(1)^2 + b(1) + 1 = 3 \implies a + b = 2$.
   - For $(2, 9)$: $a(2)^2 + b(2) + 1 = 9 \implies 4a + 2b = 8 \iff 2a + b = 4$.

2. **Solve the System:**
   Subtract $(a+b=2)$ from $(2a+b=4)$:
   $$(2a + b) - (a + b) = 4 - 2 \implies a = 2.$$
   Then $b = 2 - a = 2 - 2 = 0$.
   The polynomial is:
   $$p(x) = 2x^2 + 1.$$

3. **Verification:**
   - $p(0) = 2(0)^2 + 1 = 1$ (matches $(0,1)$).
   - $p(1) = 2(1)^2 + 1 = 3$ (matches $(1,3)$).
   - $p(2) = 2(2)^2 + 1 = 2(4) + 1 = 9$ (matches $(2,9)$).
   All three points lie on the graph of $p(x)$.

---

## More Challenging Exercises

### Exercise 11. A Parameter in a System of Three Equations
Analyze the number of solutions depending on $t$:
$$\begin{cases}x+y+z=1,\\x+ty+z=2,\\x+y+tz=3.\end{cases}$$
Use elimination and separately analyze the parameter values for which a standard calculation step ceases to be valid.

> **Why this exercise:** develops parametric analysis while still relying only on elimination.

#### Solution

1. **Augmented Matrix and Elimination:**
   $$\left[\begin{array}{ccc|c} 1 & 1 & 1 & 1 \\ 1 & t & 1 & 2 \\ 1 & 1 & t & 3 \end{array}\right].$$
   - $R_2 \leftarrow R_2 - R_1 \implies (0, t-1, 0 \mid 1)$.
   - $R_3 \leftarrow R_3 - R_1 \implies (0, 0, t-1 \mid 2)$.
   $$\left[\begin{array}{ccc|c} 1 & 1 & 1 & 1 \\ 0 & t-1 & 0 & 1 \\ 0 & 0 & t-1 & 2 \end{array}\right].$$

2. **Analysis of Parameter $t$:**
   The standard back-substitution step requires dividing by $t - 1$, which is valid if and only if $t - 1 \neq 0 \iff t \neq 1$.
   - **Case 1: $t = 1$:**
     Row 2 becomes $[0\ 0\ 0 \mid 1]$, which translates to $0\cdot x + 0\cdot y + 0\cdot z = 1 \iff 0 = 1$.
     Row 3 becomes $[0\ 0\ 0 \mid 2]$, which translates to $0 = 2$.
     Both rows produce contradictions. Therefore, for $t = 1$, the system has **no solution** (inconsistent).
   - **Case 2: $t \neq 1$:**
     Since $t - 1 \neq 0$, division is valid:
     $$z = \frac{2}{t-1}, \qquad y = \frac{1}{t-1}.$$
     $$x = 1 - y - z = 1 - \frac{1}{t-1} - \frac{2}{t-1} = 1 - \frac{3}{t-1} = \frac{t-4}{t-1}.$$
     For every $t \neq 1$, there is **exactly one unique solution**:
     $$(x, y, z) = \left(\frac{t-4}{t-1}, \frac{1}{t-1}, \frac{2}{t-1}\right).$$

---

### Exercise 12. Homogeneous System
Solve
$$\begin{cases}x+2y-z=0,\\2x+4y-2z=0,\\x-y+2z=0.\end{cases}$$
Give all solutions in parametric form and explain why $(0,0,0)$ always satisfies a homogeneous system.

> **Why this exercise:** shows the special case of a system with a zero right-hand side without introducing additional theory.

#### Solution

1. **Augmented Matrix and Elimination:**
   $$\left[\begin{array}{ccc|c} 1 & 2 & -1 & 0 \\ 2 & 4 & -2 & 0 \\ 1 & -1 & 2 & 0 \end{array}\right].$$
   - $R_2 \leftarrow R_2 - 2R_1 \implies (0, 0, 0 \mid 0)$.
   - $R_3 \leftarrow R_3 - R_1 \implies (0, -3, 3 \mid 0)$.
   Swap $R_2 \leftrightarrow R_3$ and divide new $R_2$ by $-3$:
   $$\left[\begin{array}{ccc|c} 1 & 2 & -1 & 0 \\ 0 & 1 & -1 & 0 \\ 0 & 0 & 0 & 0 \end{array}\right].$$

2. **Parametric Solution:**
   - From Row 2: $y - z = 0 \implies y = z$.
   - Free variable: $z = t \in \mathbb{R}$.
   - From Row 1: $x + 2y - z = 0 \implies x + 2t - t = 0 \implies x = -t$.
   $$\begin{pmatrix}x \\ y \\ z\end{pmatrix} = t \begin{pmatrix}-1 \\ 1 \\ 1\end{pmatrix}, \quad t \in \mathbb{R}.$$

3. **Why $(0,0,0)$ Always Satisfies a Homogeneous System:**
   In matrix notation, a homogeneous system is $Ax = 0$. For any matrix $A$:
   $$A \cdot \mathbf{0} = \mathbf{0}$$
   because each entry is a sum of products where every product involves 0: $\sum_j a_{ij}\cdot 0 = 0$. Hence $x = (0,0,0)$ is always a solution (the trivial solution).

---

### Exercise 13. Does Every Equation Add New Information?
Consider the system
$$x_1+x_2=10,\qquad x_2+x_3=8,\qquad x_1-x_3=2.$$
Solve it and check whether all three equations are independently necessary to describe the solution set. If one follows from the others, show this by calculation.

> **Why this exercise:** teaches how to recognize redundant equations within a system.

#### Solution

1. **Check for Redundancy:**
   Subtract the second equation from the first:
   $$(x_1 + x_2) - (x_2 + x_3) = 10 - 8 \implies x_1 - x_3 = 2.$$
   This is precisely the third equation.
   Therefore, Equation 3 follows directly from Equation 1 and Equation 2 ($E_3 = E_1 - E_2$). It is **redundant** and adds no new constraints to the solution set.

2. **Solve the System:**
   We only need the first two equations:
   - $x_1 = 10 - x_2$.
   - $x_3 = 8 - x_2$.
   Let $x_2 = t \in \mathbb{R}$ be the free parameter:
   $$\begin{pmatrix}x_1 \\ x_2 \\ x_3\end{pmatrix} = \begin{pmatrix}10 - t \\ t \\ 8 - t\end{pmatrix} = \begin{pmatrix}10 \\ 0 \\ 8\end{pmatrix} + t\begin{pmatrix}-1 \\ 1 \\ -1\end{pmatrix}, \quad t \in \mathbb{R}.$$
   The solution set is a 1-dimensional line in $\mathbb{R}^3$, confirming that only two equations were independent.

---

### Exercise 14. A Small Change in the Right-Hand Side
Compare the systems
$$\begin{cases}x+y=2,\\2x-y=1,\\3x=3\end{cases}$$
and
$$\begin{cases}x+y=2,\\2x-y=1,\\3x=3.1.\end{cases}$$
Check the consistency of each system and explain why a small change in one number can change the type of the system.

> **Why this exercise:** shows the difference between a consistent and an inconsistent system without introducing new theory.

#### Solution

1. **System 1:**
   From equation 3: $3x = 3 \implies x = 1$.
   Substitute $x=1$ into equation 1: $1 + y = 2 \implies y = 1$.
   Test $(1, 1)$ in equation 2: $2(1) - 1 = 1$ (satisfied!).
   All three equations hold simultaneously. The system is **consistent** with unique solution $(x, y) = (1, 1)$.

2. **System 2:**
   From equation 1 and equation 2, adding them gives:
   $$(x+y) + (2x-y) = 2 + 1 \implies 3x = 3.$$
   However, equation 3 asserts that:
   $$3x = 3.1.$$
   This yields the contradiction $3 = 3.1$, which is impossible.
   Thus, System 2 is **inconsistent** (no solution).

3. **Geometric Explanation:**
   This is an overdetermined system (3 lines for 2 unknowns). In System 1, all three lines intersect concurrently at the single point $(1, 1)$. Changing the constant from $3$ to $3.1$ shifts the third vertical line $x = 1.0333$ away from the intersection point of the first two lines, creating a triangular region of pairwise intersections with no common point of concurrency.

---

### Exercise 15. Classifying Three Systems
For each of the following systems, perform only as much elimination as necessary to recognize its type:

1. $\begin{cases}x+y=2,\\x-y=0,\end{cases}$
2. $\begin{cases}x+y=2,\\2x+2y=4,\end{cases}$
3. $\begin{cases}x+y=2,\\2x+2y=5.\end{cases}$

For each, justify the classification: one solution, infinitely many solutions, or no solution.

> **Why this exercise:** brings together the three basic cases and requires recognizing them from the structure after elimination.

#### Solution

1. **System 1:**
   Augmented matrix: $\left[\begin{array}{cc|c}1&1&2\\1&-1&0\end{array}\right]$.
   $R_2 \leftarrow R_2 - R_1 \implies \left[\begin{array}{cc|c}1&1&2\\0&-2&-2\end{array}\right]$.
   - Both rows have non-zero pivots on the left ($a_{11}=1, a_{22}=-2$), giving full rank ($2$).
   - **Classification: Exactly one unique solution** ($(x, y) = (1, 1)$).

2. **System 2:**
   Augmented matrix: $\left[\begin{array}{cc|c}1&1&2\\2&2&4\end{array}\right]$.
   $R_2 \leftarrow R_2 - 2R_1 \implies \left[\begin{array}{cc|c}1&1&2\\0&0&0\end{array}\right]$.
   - The second row is entirely zero ($[0\ 0 \mid 0]$). There is $1$ pivot and $1$ free variable, with no contradiction.
   - **Classification: Infinitely many solutions** ($(x, y) = (2-y, y)$ for $y \in \mathbb{R}$).

3. **System 3:**
   Augmented matrix: $\left[\begin{array}{cc|c}1&1&2\\2&2&5\end{array}\right]$.
   $R_2 \leftarrow R_2 - 2R_1 \implies \left[\begin{array}{cc|c}1&1&2\\0&0&1\end{array}\right]$.
   - The second row is $[0\ 0 \mid 1]$, meaning $0\cdot x + 0\cdot y = 1 \iff 0 = 1$.
   - **Classification: No solution (inconsistent)**.
