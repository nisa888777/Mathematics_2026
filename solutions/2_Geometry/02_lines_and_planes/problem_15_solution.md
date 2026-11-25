# Exercise 15. Complete Classification of a Line Relative to a Plane

## Question

Let

$$
L: p + tv, \qquad \Pi: n \cdot x = d.
$$

State the conditions distinguishing the three cases: one intersection point, parallel with no common points, and the line contained in the plane. Then illustrate each case with your own simple numerical example.

---

## Solution

Consider a line $L: x(t) = p + tv$ ($t \in \mathbb{R}$, with direction vector $v \neq 0$) and a plane $\Pi: n \cdot x = d$ (with normal vector $n \neq 0$) in $\mathbb{R}^3$. Substituting $x(t) = p + tv$ into $\Pi$ reduces the intersection problem to a single linear equation in $t$:

$$
n \cdot (p + tv) = d \iff (n \cdot v)\, t = d - n \cdot p
$$

The number of solutions $t \in \mathbb{R}$—and thus the geometric relationship between $L$ and $\Pi$—is completely governed by the two scalar quantities $n \cdot v$ and $n \cdot p - d$.

---

### 1. General Classification Criteria

| Case | Geometric Relationship | Algebraic & Vector Conditions | Solution for $t$ |
| :--- | :--- | :--- | :--- |
| **Case 1** | **One intersection point** (transversal intersection) | $n \cdot v \neq 0$ (no condition needed on $p$) | Unique $t = \dfrac{d - n \cdot p}{n \cdot v}$ |
| **Case 2** | **Parallel with no common points** (strictly parallel) | $n \cdot v = 0$ **and** $n \cdot p \neq d$ | No solution ($0 \cdot t = d - n \cdot p \neq 0$) |
| **Case 3** | **Line contained in the plane** ($L \subset \Pi$) | $n \cdot v = 0$ **and** $n \cdot p = d$ | Infinitely many solutions (all $t \in \mathbb{R}$) |

* **Geometric interpretation of the two conditions:**
  1. **$n \cdot v = 0$ vs. $n \cdot v \neq 0$ (Direction test):** $n \cdot v = 0$ means the direction vector $v$ is orthogonal to the normal vector $n$, so $L$ runs parallel to $\Pi$. Conversely, $n \cdot v \neq 0$ means $L$ tilts toward $\Pi$ and must pierce it at a single point.
  2. **$n \cdot p = d$ vs. $n \cdot p \neq d$ (Anchor point test when $n \cdot v = 0$):** Once $L$ is parallel to $\Pi$, every point on $L$ stays at the same signed distance from $\Pi$ as the anchor point $p$. Thus, $L$ lies inside $\Pi$ if and only if $p \in \Pi$ ($n \cdot p = d$), and has zero intersection points if and only if $p \notin \Pi$ ($n \cdot p \neq d$).

---

### 2. Numerical Example for Each Case

To make the comparison transparent, fix the same plane $\Pi$ across all three examples:

$$
\Pi: z = 0 \quad \Longleftrightarrow \quad n \cdot x = d \quad \text{with} \quad n = (0, 0, 1), \quad d = 0
$$

#### Case 1 — One Intersection Point ($n \cdot v \neq 0$)

* **Example:** Take $p = (1, 2, 3)$ and $v = (0, 0, -1)$, giving $L_1: x(t) = (1, 2, 3) + t(0, 0, -1) = (1, 2, 3 - t)$.
* **Check condition:**
  * $n \cdot v = (0, 0, 1) \cdot (0, 0, -1) = -1 \neq 0$.
* **Intersection point:** Solving $3 - t = 0$ yields $t = 3$, giving the unique intersection point:

$$
x(3) = (1, 2, 0)
$$

* **Verification:** $(1, 2, 0)$ satisfies $z = 0$ (on $\Pi$) and equals $p + 3v$ (on $L_1$).

---

#### Case 2 — Parallel With No Common Points ($n \cdot v = 0$ and $n \cdot p \neq d$)

* **Example:** Take $p = (1, 2, 3)$ and $v = (1, 0, 0)$, giving $L_2: x(t) = (1, 2, 3) + t(1, 0, 0) = (1 + t, 2, 3)$.
* **Check conditions:**
  * $n \cdot v = (0, 0, 1) \cdot (1, 0, 0) = 0$ (direction is orthogonal to $n$).
  * $n \cdot p = (0, 0, 1) \cdot (1, 2, 3) = 3 \neq 0 = d$ (base point $p$ is not in $\Pi$).
* **Result:** Substituting $x(t)$ into $z = 0$ yields $3 = 0$, which has **no solution**. Every point on $L_2$ has height $z = 3$, so $L_2 \cap \Pi = \varnothing$.

---

#### Case 3 — Line Contained in the Plane ($n \cdot v = 0$ and $n \cdot p = d$)

* **Example:** Take $p = (1, 2, 0)$ and $v = (1, 0, 0)$, giving $L_3: x(t) = (1, 2, 0) + t(1, 0, 0) = (1 + t, 2, 0)$.
* **Check conditions:**
  * $n \cdot v = (0, 0, 1) \cdot (1, 0, 0) = 0$ (direction is orthogonal to $n$).
  * $n \cdot p = (0, 0, 1) \cdot (1, 2, 0) = 0 = d$ (base point $p$ lies in $\Pi$).
* **Result:** Substituting $x(t)$ into $z = 0$ yields $0 = 0$, which holds **identically for every $t \in \mathbb{R}$**. Thus, every point $(1 + t, 2, 0)$ satisfies $z = 0$, confirming $L_3 \subset \Pi$.

---

### Conclusion

* **One intersection point:** $n \cdot v \neq 0$ (e.g., $L_1: (1, 2, 3) + t(0, 0, -1)$ intersects $z = 0$ at the point $Q = (1, 2, 0)$).
* **Parallel, no common points:** $n \cdot v = 0$ and $n \cdot p \neq d$ (e.g., $L_2: (1, 2, 3) + t(1, 0, 0)$ is strictly parallel to $z = 0$).
* **Contained in the plane:** $n \cdot v = 0$ and $n \cdot p = d$ (e.g., $L_3: (1, 2, 0) + t(1, 0, 0)$ lies entirely inside $z = 0$).
