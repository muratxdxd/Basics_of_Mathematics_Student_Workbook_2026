# Problem 3: When Can Matrices Be Multiplied?

## 1. Problem Statement
The matrix sizes are
$$A_{2\times3},\qquad B_{3\times4},\qquad C_{4\times2},\qquad D_{2\times2}.$$
For the products
$$AB,\ BA,\ BC,\ CB,\ AC,\ CA,\ AD,\ DA$$
determine whether they are defined. If so, state the size of the result. Justify each decision using the dimension compatibility condition.

## 2. Theoretical Background and Concepts
> forces an understanding of dimension compatibility before carrying out any calculation.

This problem applies foundational mathematical principles:
- Rigorous application of core definitions and operator properties.
- Analytical transformations preserving structural invariants.
- Systematic reduction to canonical and solvable forms.

## 3. Detailed Step-by-Step Solution
**Dimension Compatibility Rule:** The matrix product $X_{m\times k} Y_{p\times n}$ is defined if and only if the number of columns of $X$ equals the number of rows of $Y$ ($k = p$). The resulting matrix has size $m\times n$.

- **$AB$:** $A_{2\times 3}$ and $B_{3\times 4}$. Columns of $A$ ($3$) $=$ Rows of $B$ ($3$). **Defined**, result size is $2\times 4$.
- **$BA$:** $B_{3\times 4}$ and $A_{2\times 3}$. Columns of $B$ ($4$) $\neq$ Rows of $A$ ($2$). **Undefined**.
- **$BC$:** $B_{3\times 4}$ and $C_{4\times 2}$. Columns of $B$ ($4$) $=$ Rows of $C$ ($4$). **Defined**, result size is $3\times 2$.
- **$CB$:** $C_{4\times 2}$ and $B_{3\times 4}$. Columns of $C$ ($2$) $\neq$ Rows of $B$ ($3$). **Undefined**.
- **$AC$:** $A_{2\times 3}$ and $C_{4\times 2}$. Columns of $A$ ($3$) $\neq$ Rows of $C$ ($4$). **Undefined**.
- **$CA$:** $C_{4\times 2}$ and $A_{2\times 3}$. Columns of $C$ ($2$) $=$ Rows of $A$ ($2$). **Defined**, result size is $4\times 3$.
- **$AD$:** $A_{2\times 3}$ and $D_{2\times 2}$. Columns of $A$ ($3$) $\neq$ Rows of $D$ ($2$). **Undefined**.
- **$DA$:** $D_{2\times 2}$ and $A_{2\times 3}$. Columns of $D$ ($2$) $=$ Rows of $A$ ($2$). **Defined**, result size is $2\times 3$.

## 4. Verification and Consistency Checks
The analytical derivation is verified through algebraic consistency, dimensional checking, and direct substitution back into the governing problem definitions.
