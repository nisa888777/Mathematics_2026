# Exercise 11. Plane Containing a Line and a Point

## Question

Find the equation of the plane containing

$$
(x, y, z) = (1, 0, 2) + t(1, 1, -1)
$$

and the point $P = (0, 2, 1)$. Check that both the entire line and the point lie in the plane you obtain.

---

## Solution

A line $L: X(t) = P_0 + t v$ and an external point $P \notin L$ uniquely determine a plane $\Pi$ in $\mathbb{R}^3$. Because both $L$ and $P$ lie in $\Pi$, the direction vector $v$ of the line and the displacement vector $\overrightarrow{P_0 P} = P - P_0$ are two linearly independent vectors spanning the direction of $\Pi$. Taking their cross product yields a normal vector $n = v \times \overrightarrow{P_0 P}$.

---

### 1. Construct Two Linearly Independent Vectors in the Plane

* **Extract line data from $L: (x, y, z) = (1, 0, 2) + t(1, 1, -1)$:**
  * Base point on the line: $P_0 = (1, 0, 2)$
  * Direction vector of the line: $v = (1, 1, -1)$

* **Construct the second in-plane vector from $P_0 = (1, 0, 2)$ to $P = (0, 2, 1)$:**

$$
\overrightarrow{P_0 P} = P - P_0 = (0 - 1, \; 2 - 0, \; 1 - 2) = (-1, 2, -1)
$$

Since $\overrightarrow{P_0 P} = (-1, 2, -1)$ is not a scalar multiple of $v = (1, 1, -1)$, $P$ does not lie on $L$, and the two vectors $v$ and $\overrightarrow{P_0 P}$ are linearly independent.

---

### 2. Compute a Normal Vector via the Cross Product

Compute $n = v \times \overrightarrow{P_0 P}$ using $v = (1, 1, -1)$ and $\overrightarrow{P_0 P} = (-1, 2, -1)$:

* **First component:** $(1)(-1) - (-1)(2) = -1 - (-2) = 1$
* **Second component:** $(-1)(-1) - (1)(-1) = 1 - (-1) = 2$
* **Third component:** $(1)(2) - (1)(-1) = 2 - (-1) = 3$

Thus, a normal vector to the plane is:

$$
n = v \times \overrightarrow{P_0 P} = (1, 2, 3)
$$

* **Orthogonality check:**
  * $n \cdot v = (1)(1) + (2)(1) + (3)(-1) = 1 + 2 - 3 = 0 \quad \checkmark$
  * $n \cdot \overrightarrow{P_0 P} = (1)(-1) + (2)(2) + (3)(-1) = -1 + 4 - 3 = 0 \quad \checkmark$

---

### 3. Construct the Equation of the Plane

Substitute $P_0 = (1, 0, 2)$ and $n = (1, 2, 3)$ into the point-normal form $n \cdot (X - P_0) = 0$:

$$
1(x - 1) + 2(y - 0) + 3(z - 2) = 0
$$

Expand and simplify:

$$
x - 1 + 2y + 3z - 6 = 0 \implies x + 2y + 3z = 7 \qquad (\text{or } x + 2y + 3z - 7 = 0)
$$

---

### 4. Check That Both the Entire Line and the Point Lie in the Plane

* **Check 1 — Verify the point $P = (0, 2, 1)$ lies in $x + 2y + 3z = 7$:**

$$
0 + 2(2) + 3(1) = 0 + 4 + 3 = 7 \quad \checkmark
$$

Since $7 = 7$ holds, $P = (0, 2, 1)$ lies in the plane.

* **Check 2 — Verify the entire line $(x, y, z) = (1 + t, \, t, \, 2 - t)$ lies in $x + 2y + 3z = 7$:**

Substitute $x(t) = 1 + t$, $y(t) = t$, and $z(t) = 2 - t$ into the left-hand side of the plane equation:

$$
(1 + t) + 2(t) + 3(2 - t) = 1 + t + 2t + 6 - 3t = (1 + 6) + (1 + 2 - 3)t = 7 + 0t = 7
$$

Because $7 = 7$ holds identically for **every** $t \in \mathbb{R}$, every point on the line satisfies the plane equation, confirming the entire line lies in the plane.

---

### Conclusion

* **Two in-plane direction vectors:** $v = (1, 1, -1)$ and $\overrightarrow{P_0 P} = (-1, 2, -1)$.
* **Normal vector:** $n = v \times \overrightarrow{P_0 P} = (1, 2, 3)$.
* **Plane equation:** $x + 2y + 3z = 7$ (equivalently, $x + 2y + 3z - 7 = 0$).
* **Verification:** $P = (0, 2, 1)$ gives $0 + 4 + 3 = 7$, and substituting $X(t) = (1 + t, t, 2 - t)$ yields $(1 + t) + 2t + 3(2 - t) = 7$ identically for all $t \in \mathbb{R}$.
