# Exercise 7. A Line Relative to a Plane

## Question

For

$$
L: (x, y, z) = (1, 1, 0) + t(1, -1, 0), \qquad \Pi: x + y + z = 2,
$$

determine whether the line intersects the plane at one point, is parallel to it, or lies in it. Explain the role of the dot product of the direction vector and the normal vector.

---

## Solution

In $\mathbb{R}^3$, let a line $L$ pass through a base point $P_0$ with nonzero direction vector $v$, and let a plane $\Pi$ be defined by $n \cdot X = d$ with nonzero normal vector $n$. Substituting $X(t) = P_0 + t v$ into the plane equation yields a single linear equation in $t$:

$$
n \cdot (P_0 + t v) = d \iff (v \cdot n)t = d - n \cdot P_0
$$

This equation completely classifies the relative position of $L$ and $\Pi$ into three mutually exclusive cases:
1. **$v \cdot n \neq 0$:** Unique solution $t = \frac{d - n \cdot P_0}{v \cdot n}$, so $L$ intersects $\Pi$ at **exactly one point**.
2. **$v \cdot n = 0$ and $n \cdot P_0 \neq d$:** Contradiction ($0 \cdot t = \text{nonzero}$), so $L$ is **strictly parallel** to $\Pi$ (no intersection).
3. **$v \cdot n = 0$ and $n \cdot P_0 = d$:** Identity ($0 \cdot t = 0$ for all $t \in \mathbb{R}$), so $L$ **lies entirely in $\Pi$**.

---

### 1. Extract the Geometric Data of $L$ and $\Pi$

* **From $L: (x, y, z) = (1, 1, 0) + t(1, -1, 0)$:**
  * Base point: $P_0 = (1, 1, 0)$
  * Direction vector: $v = (1, -1, 0)$
  * Parametric coordinates: $x(t) = 1 + t, \; y(t) = 1 - t, \; z(t) = 0$

* **From $\Pi: x + y + z = 2$:**
  * Normal vector: $n = (1, 1, 1)$
  * Constant term: $d = 2$

---

### 2. Compute $v \cdot n$ and Test the Base Point $P_0$

* **Step 1 — Compute the dot product $v \cdot n$:**

$$
v \cdot n = (1)(1) + (-1)(1) + (0)(1) = 1 - 1 + 0 = 0
$$

Since $v \cdot n = 0$, the direction vector $v$ is orthogonal to the normal vector $n$, meaning $L$ runs parallel to the plane $\Pi$ (it either lies inside $\Pi$ or is strictly parallel to $\Pi$ with zero intersection).

* **Step 2 — Check whether the base point $P_0 = (1, 1, 0)$ lies in $\Pi$:**

Substitute $P_0 = (1, 1, 0)$ into the left-hand side of $x + y + z = 2$:

$$
1 + 1 + 0 = 2
$$

Since $2 = 2$ holds, $P_0 = (1, 1, 0)$ lies on $\Pi$.

* **Step 3 — Verify via direct parametric substitution for all $t \in \mathbb{R}$:**

Substitute $(x(t), y(t), z(t)) = (1 + t, \, 1 - t, \, 0)$ into $\Pi: x + y + z = 2$:

$$
(1 + t) + (1 - t) + 0 = 2 \implies 2 = 2
$$

Because the parameter $t$ cancels out and leaves a true identity for **every** $t \in \mathbb{R}$, every point on $L$ satisfies the equation of $\Pi$. Therefore, **the line $L$ lies entirely in the plane $\Pi$**.

---

### 3. Explain the Role of the Dot Product $v \cdot n$

1. **Measures Alignment Between the Line's Direction and the Plane's Normal:** Because $n$ is perpendicular to $\Pi$, a line travels along (or parallel to) $\Pi$ if and only if its direction vector $v$ is perpendicular to $n$. The dot product $v \cdot n$ directly tests this orthogonality condition.
2. **Acts as the Coefficient of $t$ in the Intersection Equation:** Substituting $X(t) = P_0 + tv$ into $n \cdot X = d$ gives $(v \cdot n)t = d - n \cdot P_0$.
   * When **$v \cdot n \neq 0$**, the line crosses the plane at a nonzero angle, guaranteeing a **unique** intersection parameter $t$ (one intersection point).
   * When **$v \cdot n = 0$**, the line never changes its signed distance from $\Pi$ as $t$ varies ($n \cdot X(t) = n \cdot P_0$ is constant). Whether $L$ has zero points in common with $\Pi$ (strictly parallel) or infinitely many points in common (lies in $\Pi$) then depends solely on whether a single point $P_0$ satisfies $n \cdot P_0 = d$.

---

### Conclusion

* **Dot product check:** $v \cdot n = (1, -1, 0) \cdot (1, 1, 1) = 0$.
* **Point check:** $P_0 = (1, 1, 0)$ satisfies $1 + 1 + 0 = 2$, and $(1 + t) + (1 - t) + 0 = 2$ holds identically for all $t \in \mathbb{R}$.
* **Relative position:** The line **$L$ lies in the plane $\Pi$**.
* **Role of $v \cdot n$:** Determines whether the line cuts across the plane at a unique point ($v \cdot n \neq 0$) or maintains a constant distance from the plane ($v \cdot n = 0$), reducing the remaining distinction between strict parallelism and containment to testing a single point $P_0$.
