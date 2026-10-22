# Problem 10: A Cable Through Water and Land

## 1. Problem Statement
Point $A$ lies on one bank of a river of width $100$ m, and point $B$ lies on the other bank, $500$ m along the bank from the point directly opposite $A$.

The cost per meter of cable underwater is twice the cost per meter of cable on land.

Build a cost function depending on the point where the cable comes out of the water, determine the domain, and find the solution that minimizes the cost.

## 2. Theoretical Background and Concepts
> it checks whether the student can independently translate a spatial description and two different costs into a single function to be optimized.

This problem applies foundational mathematical principles:
- Rigorous application of core definitions and operator properties.
- Analytical transformations preserving structural invariants.
- Systematic reduction to canonical and solvable forms.

## 3. Detailed Step-by-Step Solution
1. **Geometry and Cost Function:**
   Let $A = (0, 100)$ and let the point directly opposite on the other bank be the origin $(0, 0)$. Point $B$ lies at $(500, 0)$.
   Suppose the underwater cable runs in a straight line from $A(0, 100)$ to a point $P(x, 0)$ on the opposite bank ($0 \le x \le 500$), and then runs along land from $P(x, 0)$ to $B(500, 0)$.
   - Underwater length: $d_w = \sqrt{100^2 + x^2}$.
   - Land length: $d_L = 500 - x$.
   Let the cost per meter on land be $c$, and underwater be $2c$.
   Define the normalized cost (total cost divided by $c$) as
   $$C(x) = 2\sqrt{10\,000 + x^2} + (500 - x).$$
   Thus the actual total cost is $cC(x)$.

2. **Domain:**
   The cable emergence point $x$ must lie between the perpendicular crossing and target $B$:
   $$D_C = [0, 500].$$

3. **Minimize Cost:**
   Differentiate with respect to $x$:
   $$C'(x) = 2 \cdot \frac{2x}{2\sqrt{10\,000 + x^2}} - 1 = \frac{2x}{\sqrt{10\,000 + x^2}} - 1.$$
   Setting $C'(x) = 0$:
   $$\frac{2x}{\sqrt{10\,000 + x^2}} = 1 \implies 2x = \sqrt{10\,000 + x^2}.$$
   Square both sides:
   $$4x^2 = 10\,000 + x^2 \implies 3x^2 = 10\,000 \implies x^2 = \frac{10\,000}{3} \implies x = \frac{100}{\sqrt{3}} = \frac{100\sqrt{3}}{3} \approx 57.74\text{ m}.$$
   Notice $x \approx 57.74 \in [0, 500]$.

## 4. Verification and Consistency Checks
4. **Verification of Minimum:**
   - At critical point $x \approx 57.74\text{ m}$, the normalized cost is $C(57.74)\approx673.2$, so the actual cost is $cC(57.74)\approx673.2c$.
   - At boundary $x = 0$ (perpendicular water crossing, then all land):
     $$C(0) = 2(100) + 500 = 700,$$
     so the actual cost $cC(0)=700c$ is greater.
   - At boundary $x = 500$ (direct water diagonal to $B$):
     $$C(500) = 2\sqrt{100^2 + 500^2} \approx 1019.8,$$
     so the actual cost $cC(500)\approx1019.8c$ is greater.
   The minimum cost is achieved when the cable emerges at $x = \frac{100\sqrt{3}}{3} \approx 57.74\text{ m}$ downstream from the point opposite $A$. The underwater segment makes a $60^\circ$ angle with the bank (equivalently, $30^\circ$ with the normal to the bank): its adjacent-to-hypotenuse ratio is $x/\sqrt{10000+x^2}=1/2$.
