# Problem 11: Plane Containing a Line and a Point

## 1. Problem Statement
Find the equation of the plane containing
$$(x,y,z)=(1,0,2)+t(1,1,-1)$$
and the point $P=(0,2,1)$. Check that both the entire line and the point lie in the plane you obtain.

## 2. Theoretical Background and Concepts
> requires independently constructing two linearly independent directions in the plane.

This problem applies foundational mathematical principles:
- Rigorous application of core definitions and operator properties.
- Analytical transformations preserving structural invariants.
- Systematic reduction to canonical and solvable forms.

## 3. Detailed Step-by-Step Solution
1. **Construct Two In-Plane Vectors:**
   - Direction of the line: $v_1 = (1, 1, -1)$.
   - Base point of the line: $Q = (1, 0, 2)$.
   - Vector from $Q$ to $P(0, 2, 1)$:
     $$v_2 = P - Q = (0 - 1, 2 - 0, 1 - 2) = (-1, 2, -1).$$
   The vectors $v_1$ and $v_2$ are independent directions in the plane: $v_1$ follows the line and $v_2$ joins a point on it to $P$. Thus their cross product is perpendicular to the plane.

2. **Normal Vector via Cross Product:**
   $$n = v_1 \times v_2 = \det\begin{pmatrix}i & j & k \\ 1 & 1 & -1 \\ -1 & 2 & -1\end{pmatrix} = i(1(-1) - (-1)(2)) - j(1(-1) - (-1)(-1)) + k(1(2) - 1(-1))$$
   $$= i(-1 + 2) - j(-1 - 1) + k(2 + 1) = 1i + 2j + 3k = (1, 2, 3).$$

3. **Plane Equation:**
   For any point $X=(x,y,z)$ in the plane, the displacement $X-Q$ lies in the plane and is perpendicular to its normal. Therefore $n\cdot(X-Q)=0$. Using $Q=(1,0,2)$ and $n=(1,2,3)$:
   $$1(x - 1) + 2(y - 0) + 3(z - 2) = 0 \implies x - 1 + 2y + 3z - 6 = 0 \implies x + 2y + 3z - 7 = 0.$$

## 4. Verification and Consistency Checks
4. **Verification:**
   - **Point $P(0, 2, 1)$:** $0 + 2(2) + 3(1) - 7 = 4 + 3 - 7 = 0$ (holds).
   - **Entire line:** Every line point has coordinates $(1+t,t,2-t)$. Substituting these into the plane equation gives the identity below for every $t\in\mathbb R$, which verifies the entire line is in the plane:
     $$(1 + t) + 2(t) + 3(2 - t) - 7 = 1 + t + 2t + 6 - 3t - 7 = 0 \quad \text{for all } t \in \mathbb{R}.$$
   Both the line and the point lie on the plane.
