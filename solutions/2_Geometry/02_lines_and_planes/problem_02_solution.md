# Exercise 2. A Line in Space

## Question

Given

$$
L: (x, y, z) = (2, -1, 3) + t(1, 2, -2).
$$

State a point on the line and its direction vector, check whether $P = (4, 3, -1)$ lies on $L$, and find the point corresponding to $t = -1$.

---

## Solution

In $\mathbb{R}^3$, a vector parametric equation of the form $(x, y, z) = P_0 + t v$ ($t \in \mathbb{R}$) describes a line passing through the base point $P_0$ in the direction of the vector $v$, with component equations:

$$
\begin{cases}
x(t) = 2 + t \\
y(t) = -1 + 2t \\
z(t) = 3 - 2t
\end{cases}, \qquad t \in \mathbb{R}
$$

---

### 1. Identify a Point on the Line and Its Direction Vector

Comparing $L: (x, y, z) = (2, -1, 3) + t(1, 2, -2)$ directly with $(x, y, z) = P_0 + t v$:

* **A point on the line (corresponding to $t = 0$):**

$$
P_0 = (2, -1, 3)
$$

* **Direction vector of the line:**

$$
v = (1, 2, -2)
$$

---

### 2. Check Whether $P = (4, 3, -1)$ Lies on $L$

A point $P = (4, 3, -1)$ lies on $L$ if and only if there exists a **single** scalar parameter $t \in \mathbb{R}$ that simultaneously satisfies all three coordinate equations:

$$
(4, 3, -1) = (2 + t, \, -1 + 2t, \, 3 - 2t)
$$

Solve each coordinate equation for $t$:

* **From the $x$-coordinate:**

$$
2 + t = 4 \implies t = 4 - 2 = 2
$$

* **From the $y$-coordinate:**

$$
-1 + 2t = 3 \implies 2t = 4 \implies t = 2
$$

* **From the $z$-coordinate:**

$$
3 - 2t = -1 \implies -2t = -4 \implies t = 2
$$

Because all three equations yield the exact same parameter value $t = 2$, the point **$P = (4, 3, -1)$ lies on $L$** (specifically at $t = 2$).

---

### 3. Find the Point Corresponding to $t = -1$

Substitute $t = -1$ into the vector equation $(x, y, z) = (2, -1, 3) + t(1, 2, -2)$:

$$
(x(-1), \, y(-1), \, z(-1)) = (2, -1, 3) + (-1)(1, 2, -2)
$$

Compute component by component:

* **$x$-coordinate:** $2 + (-1)(1) = 2 - 1 = 1$
* **$y$-coordinate:** $-1 + (-1)(2) = -1 - 2 = -3$
* **$z$-coordinate:** $3 + (-1)(-2) = 3 + 2 = 5$

Thus, the point on $L$ corresponding to $t = -1$ is:

$$
Q = (1, -3, 5)
$$

---

### Conclusion

* **Point on the line:** $P_0 = (2, -1, 3)$ (at $t = 0$).
* **Direction vector:** $v = (1, 2, -2)$.
* **Membership check for $P = (4, 3, -1)$:** Yes, $P$ **lies on $L$**, because $t = 2$ satisfies all three coordinate equations simultaneously.
* **Point at $t = -1$:** $(1, -3, 5)$.
