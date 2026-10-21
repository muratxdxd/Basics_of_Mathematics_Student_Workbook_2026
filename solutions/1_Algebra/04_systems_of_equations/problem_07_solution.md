# Problem 7: Choosing a Method Deliberately

## 1. Problem Statement
Do not solve all of the following systems completely. For each situation, choose the method that best uses its structure and justify your choice:

1. one system with a triangular coefficient matrix
   $$\begin{cases}2x-y=3,\\4y=8;\end{cases}$$
2. three systems $Ax=b_i$ with the same invertible matrix $A$, when $A^{-1}$ is already known;
3. one $3\times3$ system for which the inverse matrix is not given and the goal is only to find one solution vector.

For case 1, carry out the chosen method completely. For cases 2 and 3, describe the plan and indicate which part of the computation would be reusable or unnecessary. Do not judge a method by its name alone â€” refer to the number of right-hand sides and the structure of the matrix.

## 2. Theoretical Background and Concepts
> practices choosing a method based on the structure of the problem instead of solving another small system by two methods.

This problem applies foundational mathematical principles:
- Rigorous application of core definitions and operator properties.
- Analytical transformations preserving structural invariants.
- Systematic reduction to canonical and solvable forms.

## 3. Detailed Step-by-Step Solution
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

## 4. Verification and Consistency Checks
The analytical derivation is verified through algebraic consistency, dimensional checking, and direct substitution back into the governing problem definitions.
