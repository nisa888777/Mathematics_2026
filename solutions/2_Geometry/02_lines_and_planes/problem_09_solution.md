# Exercise 9. Distances

## Question

Compute:

1. the distance from $P = (2, 3)$ to the line $3x + 4y - 10 = 0$,
2. the distance from $Q = (2, -1, 3)$ to the plane $2x - 2y + z - 4 = 0$.

Compare the two formulas and explain their common connection with the normal direction.

---

## Solution

Both point-to-line distance in $\mathbb{R}^2$ and point-to-plane distance in $\mathbb{R}^3$ measure the **shortest (perpendicular) distance** from an external point to a hyperplane, obtained by projecting any displacement vector onto the unit normal vector.

---

### 1. Distance From $P = (2, 3)$ to the Line $3x + 4y - 10 = 0$ in $\mathbb{R}^2$

For a point $P = (x_0, y_0)$ and a line $L: ax + by + c = 0$ with normal vector $n_L = (a, b)$, the perpendicular distance is:

$$
d(P, L) = \frac{|a x_0 + b y_0 + c|}{\sqrt{a^2 + b^2}}
$$

* **Step 1 — Identify parameters:**
  * Point: $P = (2, 3)$
  * Coefficients and normal vector: $a = 3, \; b = 4, \; c = -10$, so $n_L = (3, 4)$

* **Step 2 — Evaluate numerator and normal length:**

$$
|3(2) + 4(3) - 10| = |6 + 12 - 10| = |8| = 8
$$

$$
\|n_L\| = \sqrt{3^2 + 4^2} = \sqrt{9 + 16} = \sqrt{25} = 5
$$

* **Step 3 — Compute the distance:**

$$
d(P, L) = \frac{8}{5} = 1.6
$$

* **Orthogonal Foot Verification:** Choosing the point $A = (2, 1)$ on the line (since $3(2) + 4(1) - 10 = 0$) gives $\overrightarrow{AP} = (0, 2)$. Projecting onto $n_L = (3, 4)$ yields $\frac{|\overrightarrow{AP} \cdot n_L|}{\|n_L\|} = \frac{|(0)(3) + (2)(4)|}{5} = \frac{8}{5}$.

---

### 2. Distance From $Q = (2, -1, 3)$ to the Plane $2x - 2y + z - 4 = 0$ in $\mathbb{R}^3$

For a point $Q = (x_0, y_0, z_0)$ and a plane $\Pi: ax + by + cz + d = 0$ with normal vector $n_\Pi = (a, b, c)$, the perpendicular distance is:

$$
d(Q, \Pi) = \frac{|a x_0 + b y_0 + c z_0 + d|}{\sqrt{a^2 + b^2 + c^2}}
$$

* **Step 1 — Identify parameters:**
  * Point: $Q = (2, -1, 3)$
  * Coefficients and normal vector: $a = 2, \; b = -2, \; c = 1, \; d = -4$, so $n_\Pi = (2, -2, 1)$

* **Step 2 — Evaluate numerator and normal length:**

$$
|2(2) + (-2)(-1) + 1(3) - 4| = |4 + 2 + 3 - 4| = |5| = 5
$$

$$
\|n_\Pi\| = \sqrt{2^2 + (-2)^2 + 1^2} = \sqrt{4 + 4 + 1} = \sqrt{9} = 3
$$

* **Step 3 — Compute the distance:**

$$
d(Q, \Pi) = \frac{5}{3}
$$

* **Orthogonal Foot Verification:** Choosing the point $B = (2, 0, 0)$ on the plane (since $2(2) - 2(0) + 0 - 4 = 0$) gives $\overrightarrow{BQ} = (0, -1, 3)$. Projecting onto $n_\Pi = (2, -2, 1)$ yields $\frac{|\overrightarrow{BQ} \cdot n_\Pi|}{\|n_\Pi\|} = \frac{|(0)(2) + (-1)(-2) + (3)(1)|}{3} = \frac{5}{3}$.

---

### 3. Comparison of the Two Formulas and Connection With the Normal Direction

* **Side-by-Side Structural Comparison:**
  * **In $\mathbb{R}^2$ (line):** $d(P, L) = \dfrac{|n_L \cdot P + c|}{\|n_L\|} = \dfrac{|a x_0 + b y_0 + c|}{\sqrt{a^2 + b^2}}$
  * **In $\mathbb{R}^3$ (plane):** $d(Q, \Pi) = \dfrac{|n_\Pi \cdot Q + d|}{\|n_\Pi\|} = \dfrac{|a x_0 + b y_0 + c z_0 + d|}{\sqrt{a^2 + b^2 + c^2}}$

* **Common Geometric Mechanism (Orthogonal Projection Onto the Normal):**
  1. **Single Normal Direction:** Both a line in $\mathbb{R}^2$ and a plane in $\mathbb{R}^3$ are codimension-1 objects (hyperplanes), meaning each has a unique perpendicular direction spanned by its normal vector $n$ whose components are the linear equation's coefficients.
  2. **Scalar Projection Onto $\hat{n} = \frac{n}{\|n\|}$:** Pick any anchor point $X_0$ on the line or plane (so $n \cdot X_0 + \text{const} = 0$). The shortest distance from an external point $P$ to the set is the length of the orthogonal projection of $\overrightarrow{X_0 P} = P - X_0$ onto the unit normal $\hat{n}$:

$$
\text{Distance} = \left|\overrightarrow{X_0 P} \cdot \frac{n}{\|n\|}\right| = \frac{|n \cdot P - n \cdot X_0|}{\|n\|} = \frac{|n \cdot P + \text{const}|}{\|n\|}
$$

  3. **Why Division by $\|n\|$ Is Essential:** Scaling a linear equation by a nonzero constant $k$ changes the raw residual $|k(n \cdot P + \text{const})|$ by $|k|$, while the geometric distance remains unchanged. Dividing by $\|n\|$ normalizes $n$ to unit length, making the formula scale-invariant.

---

### Conclusion

* **Distance from $P = (2, 3)$ to $3x + 4y - 10 = 0$:** $d(P, L) = \frac{8}{5}$ ($1.6$)[span_2](start_span)[span_2](end_span).
* **Distance from $Q = (2, -1, 3)$ to $2x - 2y + z - 4 = 0$:** $d(Q, \Pi) = \frac{5}{3}$[span_3](start_span)[span_3](end_span).
* **Unified principle:** Both formulas are the exact same operation—the absolute scalar projection $\left|\overrightarrow{X_0 P} \cdot \frac{n}{\|n\|}\right|$ of a displacement vector onto the unit normal vector—differing only in the ambient dimension ($\mathbb{R}^2$ vs. $\mathbb{R}^3$)[span_4](start_span)[span_4](end_span).
