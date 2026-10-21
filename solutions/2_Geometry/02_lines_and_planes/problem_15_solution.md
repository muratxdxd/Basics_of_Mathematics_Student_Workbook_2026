# Problem 15: Complete Classification of a Line Relative to a Plane

## 1. Problem Statement
Let
$$L:p+tv,\qquad \Pi:n\cdot x=d.$$
State the conditions distinguishing the three cases: one intersection point, parallel with no common points, and the line contained in the plane. Then illustrate each case with your own simple numerical example.

## 2. Theoretical Background and Concepts
> requires formulating a general mathematical criterion instead of carrying out one isolated calculation.

This problem applies foundational mathematical principles:
- Rigorous application of core definitions and operator properties.
- Analytical transformations preserving structural invariants.
- Systematic reduction to canonical and solvable forms.

## 3. Detailed Step-by-Step Solution
1. **General Mathematical Criteria:**
   Substituting $L$ into $\Pi$ gives $n \cdot (p + tv) = d \implies (n \cdot v) t = d - n \cdot p$.
   - **Case 1: One unique intersection point.**
     Condition: $n \cdot v \neq 0$.
     The parameter is uniquely determined: $t = \frac{d - n \cdot p}{n \cdot v}$.
   - **Case 2: Parallel with no common points ($L \cap \Pi = \emptyset$).**
     Condition: $n \cdot v = 0$ and $n \cdot p \neq d$.
     The equation becomes $0 \cdot t = \text{non-zero}$, which has no solution.
   - **Case 3: Line contained in the plane ($L \subset \Pi$).**
     Condition: $n \cdot v = 0$ and $n \cdot p = d$.
     The equation becomes $0 \cdot t = 0$, which holds for every $t \in \mathbb{R}$.

2. **Numerical Examples:**
   Let the plane be $\Pi: z = 0$, so $n = (0, 0, 1)$ and $d = 0$.
   - **Example 1 (Unique intersection):**
     $p = (0, 0, 1)$, $v = (0, 0, 1)$.
     $n \cdot v = 1 \neq 0$. Intersection occurs at $t = -1 \implies (0, 0, 0)$.
   - **Example 2 (Parallel, no intersection):**
     $p = (0, 0, 1)$, $v = (1, 0, 0)$.
     $n \cdot v = 0$, but $n \cdot p = 1 \neq 0$. The line lies at elevation $z = 1$, strictly parallel to $z = 0$.
   - **Example 3 (Line contained in the plane):**
     $p = (1, 1, 0)$, $v = (1, 0, 0)$.
     $n \cdot v = 0$ and $n \cdot p = 0 = d$. The line lies entirely within the plane $z = 0$.

## 4. Verification and Consistency Checks
The analytical derivation is verified through algebraic consistency, dimensional checking, and direct substitution back into the governing problem definitions.
