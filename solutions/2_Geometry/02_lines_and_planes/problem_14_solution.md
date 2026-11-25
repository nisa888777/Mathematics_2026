# Exercise 14. Contrast: Intersection and Parallelism

## Question

From the point $P = (0, 0, 1)$, two lines are drawn with direction vectors

$$
v_1 = (2, 1, -1), \qquad v_2 = (2, 1, 0).
$$

For each line, analyze its position relative to the plane $z = 0$.

For the line that intersects the plane, find the intersection point. For the other line, explain how you can recognize parallelism without solving an equation.

---

## Solution

Let $\Pi$ be the $xy$-coordinate plane defined by $z = 0$, whose standard unit normal vector is $n = (0, 0, 1)$. Both lines pass through the same base point $P = (0, 0, 1)$, which lies at height $z = 1$ strictly above $\Pi$ (since $1 \neq 0$). Whether a line $L_i: X(t) = P + t v_i$ meets $\Pi$ depends entirely on the dot product $v_i \cdot n$ (the $z$-component of $v_i$).

---

### 1. Analyze Both Lines Relative to the Plane $z = 0$

Write the parametric equations of both lines passing through $P = (0, 0, 1)$:

$$
L_1: (x, y, z) = (0, 0, 1) + t(2, 1, -1) = (2t, \, t, \, 1 - t), \qquad t \in \mathbb{R}
$$

$$
L_2: (x, y, z) = (0, 0, 1) + s(2, 1, 0) = (2s, \, s, \, 1), \qquad s \in \mathbb{R}
$$

Test the orthogonality condition $v_i \cdot n$ against the plane normal $n = (0, 0, 1)$:

* **For $L_1$ with $v_1 = (2, 1, -1)$:**

$$
v_1 \cdot n = (2)(0) + (1)(0) + (-1)(1) = -1 \neq 0
$$

Because $v_1 \cdot n \neq 0$, $v_1$ is **not perpendicular** to $n$ (it is not parallel to $\Pi$). Therefore, **$L_1$ intersects the plane $z = 0$ at a single unique point**.

* **For $L_2$ with $v_2 = (2, 1, 0)$:**

$$
v_2 \cdot n = (2)(0) + (1)(0) + (0)(1) = 0
$$

Because $v_2 \cdot n = 0$ and the base point $P = (0, 0, 1)$ does not lie in $z = 0$ ($1 \neq 0$), **$L_2$ is strictly parallel to the plane $z = 0$** (they have no points in common).

---

### 2. Find the Intersection Point of $L_1$ With the Plane $z = 0$

Substitute the parametric coordinates $(x(t), y(t), z(t)) = (2t, \, t, \, 1 - t)$ of $L_1$ into the plane equation $z = 0$:

$$
1 - t = 0 \implies t = 1
$$

Evaluate $L_1$ at $t = 1$:

$$
Q = (0, 0, 1) + 1(2, 1, -1) = (2, 1, 0)
$$

* **Dual verification:**
  * **On the plane $z = 0$:** The $z$-coordinate of $Q = (2, 1, 0)$ is $0$, so $Q$ lies in $\Pi$.
  * **On the line $L_1$:** At $t = 1$, $(2(1), 1, 1 - 1) = (2, 1, 0) = Q$.

---

### 3. How to Recognize Parallelism of $L_2$ Without Solving an Equation

1. **Zero Dot Product With the Normal ($v_2 \cdot n = 0$):** Because $n = (0, 0, 1)$ points strictly along the $z$-axis and $v_2 = (2, 1, 0)$ has $z$-component $0$, $v_2$ is immediately orthogonal to $n$ ($v_2 \cdot n = 0$). Any vector orthogonal to a plane's normal vector lies parallel to the plane.
2. **Constant Height Invariance ($z \equiv 1$):** The plane $z = 0$ consists of all points at height $z = 0$. The line $L_2$ starts at $P = (0, 0, 1)$ (height $z = 1$) and moves exclusively along $v_2 = (2, 1, 0)$, which produces **zero vertical displacement** ($\Delta z = 0$). Consequently, every point on $L_2$ remains locked at constant height $z = 1$ and can never reach $z = 0$.

---

### Conclusion

* **Relative position of $L_1$ with $v_1 = (2, 1, -1)$:** Intersects the plane $z = 0$ at a single point because $v_1 \cdot n = -1 \neq 0$.
* **Intersection point of $L_1$:** $Q = (2, 1, 0)$ (obtained at $t = 1$).
* **Relative position of $L_2$ with $v_2 = (2, 1, 0)$:** Strictly parallel to the plane $z = 0$ (no intersection).
* **Equation-free recognition:** $v_2$ has zero $z$-component ($v_2 \cdot n = 0$), so moving from $P = (0, 0, 1)$ along $v_2$ never changes the height $z = 1$, keeping the entire line strictly above $z = 0$.
