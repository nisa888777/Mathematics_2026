# Exercise 8. Intersection Point of a Line and a Plane

## Question

Find the intersection point of

$$
(x, y, z) = (1, 0, 2) + t(1, 2, -1)
$$

with the plane $x + y + z = 4$. Check the result by substituting it into both descriptions.

---

## Solution

To find the intersection of a parametric line $L: (x, y, z) = P_0 + t v$ and a plane $\Pi: ax + by + cz = d$ in $\mathbb{R}^3$, we express $x, y, z$ in terms of the single parameter $t$, substitute them into the plane equation to solve for $t$, and then evaluate the line at that parameter value.

---

### 1. Check Transversality ($v \cdot n \neq 0$) and Write Parametric Coordinates

* **Line data:** Base point $P_0 = (1, 0, 2)$ and direction vector $v = (1, 2, -1)$, giving the component equations:

$$
\begin{cases}
x(t) = 1 + t \\
y(t) = 0 + 2t = 2t \\
z(t) = 2 - t
\end{cases}, \qquad t \in \mathbb{R}
$$

* **Plane data:** Normal vector $n = (1, 1, 1)$ and constant $d = 4$.
* **Unique intersection check:**

$$
v \cdot n = (1)(1) + (2)(1) + (-1)(1) = 1 + 2 - 1 = 2 \neq 0
$$

Because $v \cdot n = 2 \neq 0$, the line is not parallel to the plane and intersects it at **exactly one point**.

---

### 2. Substitute Into the Plane Equation and Solve for $t$

Substitute $x(t) = 1 + t$, $y(t) = 2t$, and $z(t) = 2 - t$ into $x + y + z = 4$:

$$
(1 + t) + (2t) + (2 - t) = 4
$$

Combine like terms on the left-hand side:

$$
(1 + 2) + (t + 2t - t) = 4 \implies 3 + 2t = 4
$$

Solve for $t$:

$$
2t = 4 - 3 = 1 \implies t = \frac{1}{2}
$$

---

### 3. Compute the Intersection Point

Substitute $t = \frac{1}{2}$ back into the parametric equation $(x, y, z) = (1, 0, 2) + t(1, 2, -1)$:

$$
P = (1, 0, 2) + \frac{1}{2}(1, 2, -1) = \left(1 + \frac{1}{2}, \; 0 + 1, \; 2 - \frac{1}{2}\right) = \left(\frac{3}{2}, \; 1, \; \frac{3}{2}\right)
$$

---

### 4. Check the Result in Both Descriptions

* **Check 1 — Substitute into the Plane Equation ($x + y + z = 4$):**

$$
\frac{3}{2} + 1 + \frac{3}{2} = \frac{3 + 2 + 3}{2} = \frac{8}{2} = 4 \quad \checkmark
$$

Thus, $P = \left(\frac{3}{2}, 1, \frac{3}{2}\right)$ lies on the plane.

* **Check 2 — Verify Membership on the Line ($(x, y, z) = (1, 0, 2) + t(1, 2, -1)$):**

Solve each coordinate equation for $t$:
* **$x$-coordinate:** $1 + t = \frac{3}{2} \implies t = \frac{3}{2} - 1 = \frac{1}{2}$
* **$y$-coordinate:** $2t = 1 \implies t = \frac{1}{2}$
* **$z$-coordinate:** $2 - t = \frac{3}{2} \implies t = 2 - \frac{3}{2} = \frac{1}{2}$

All three coordinates yield the exact same parameter $t = \frac{1}{2}$, confirming $P = \left(\frac{3}{2}, 1, \frac{3}{2}\right)$ lies on the line.

---

### Conclusion

* **Intersection parameter:** $t = \frac{1}{2}$ (unique because $v \cdot n = 2 \neq 0$).
* **Intersection point:** $P = \left(\frac{3}{2}, 1, \frac{3}{2}\right)$ (or $(1.5, 1, 1.5)$).
* **Dual verification:** Substituting $P$ gives $\frac{3}{2} + 1 + \frac{3}{2} = 4$ in the plane equation and corresponds consistently to $t = \frac{1}{2}$ across all three coordinates of the line.
